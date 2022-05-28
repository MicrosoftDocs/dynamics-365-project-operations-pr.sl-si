---
title: Učinkovitost API-jev razporeda projekta
description: Ta tema zagotavlja informacije o merilih uspešnosti API-jev razporeda projekta in opredeljuje najboljše prakse za optimalno uporabo.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3c14d27c561a86cd359cbdcbb448ae764dd3d90e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593862"
---
# <a name="project-schedule-api-performance"></a>Učinkovitost API-jev razporeda projekta

_**Velja za:** aplikacija Project Operations za okoliščine, ki temeljijo na virih/nezalogi, poenostavljeno uvajanje – posel do izstavitve predračuna, storitev Project for the web_

Ta tema zagotavlja informacije o merilih uspešnosti API-jev razporeda projekta in opredeljuje najboljše prakse za optimizacijo uporabe.

## <a name="project-scheduling-service"></a>Storitev razporejanja projektov
Storitev razporejanja projektov je storitev z več najemniki, ki se izvaja v Microsoft Azure. Zasnovan je za izboljšanje interakcije z zagotavljanjem hitre in tekoče izkušnje, ko uporabniki delajo na projektih. Ta izboljšava je dosežena tako, da sprejmemo zahtevke za spremembe, jih obdelamo in nato takoj vrnemo rezultat. Storitev asinhrono deluje v okolju Dataverse in uporabnikom ne blokira izvajanja drugih operacij.

API-ji razporeda projekta se zanašajo na storitev razporejanja projektov za izvajanje zahtev, ki so podrobneje opisane v kasnejših razdelkih te teme.

API-ji razporeda projekta so zasnovani za delo z naslednjimi entitetami strukturirane členitve dela (WBS):

  - Project
  - Projektno opravilo
  - Odvisnost projektnega opravila
  - Član projektne ekipe
  - Dodelitev vira
  
Podprta so tako vnaprej pripravljena polja kot polja po meri. Če ni navedeno drugače, so podprte vse običajne operacije, kot so ustvarjanje, posodabljanje in brisanje. Za več informacij glejte [Uporaba API-jev razporeda projekta za izvajanje operacij in razporejanje entitet](schedule-api-preview.md).

Kot del API-jev razporeda projekta je bil dodan vzorec enote dela. Ta vzorec je znan kot OperationSet in ga je mogoče uporabiti, ko je treba v eni transakciji obdelati več zahtev.

Naslednja slika prikazuje tok, skozi katerega bo šel partner, ko bo ta funkcija uporabljena.

![Dataverse in tok storitve razporejanja projektov.](./media/dataverse-project-scheduling-service-flow.png)

**1. korak**: odjemalec opravi klic API-ja v končni točki Open Data Protocol (OData) v okolju Dataverse, da se ustvari OperationSet.

**2. korak**: ko je ustvarjen nov OperationSet, sistem vrne vrednost **OperationSetId**.

**3. korak**: odjemalec uporablja vrednost **OperationSetId**, da naredi drugo zahtevo za API razporeda projekta. Rezultat je zahteva za ustvarjanje, posodobitev ali brisanje entitete za razporejanje. Ko je ta zahteva podana, se opravi preverjanje metapodatkov. Če preverjanje ne uspe, se zahteva prekine in vrne se napaka.

**Koraki 4a–4c**: ti koraki predstavljajo fazo SPREJEMA. Odjemalec pokliče API **ExecuteOperationSetV1**, ki pošlje vse spremembe v storitev razporejanja projektov v enem paketu. Storitev razporejanja projektov izvaja lastna preverjanja za zahteve v paketu. Vse napake pri preverjanju razveljavijo paket in klicatelju vrnejo izjemo. Če storitev razporejanja projektov uspešno sprejme paket, se stanje OperationSet posodobi, da odraža dejstvo, da OperationSet obdeluje storitev za razporejanje virov.

**5. korak**: ta korak predstavlja fazo VZTRAJANJA. Storitev razporejanja projektov asinhrono zapiše paket v okolje Dataverse znotraj transakcije. Če je operacija zapisovanja uspešna, je atribut OperationSet označen kot **Zaključeno**. Vse napake razveljavijo transakcijo in paket, atribut OperationSet pa je označen z oznako **Neuspešno**.

## <a name="performance-methodology"></a>Metodologija učinkovitosti
Čas izvajanja je opredeljen kot čas od klica do klica API-ja **ExecuteOperationSetV1**, dokler storitev razporejanja projektov ne zaključi z zapisovanjem v okolje Dataverse. Vse operacije se izvajajo skupno 2200-krat, poročajo pa se meritve časa izvajanja P99. Merijo se operacije z enim zapisom in množične operacije.

Za operacijo z enim zapisom atribut OperationSet vsebuje eno zahtevo. Za množične operacije vsebuje 20, 50 ali 100 zahtev. Vsaka paketna velikost se poroča ločeno.

Te operacije se izvajajo v uvedbi UR 15 Project Operations Lite v Severni Ameriki.

## <a name="results"></a>Rezultati
### <a name="create-operations"></a>Ustvarjanje operacij
#### <a name="single-record-create-operations"></a>Operacije ustvarjanja enega zapisa
Naslednja tabela prikazuje čase izvedbe za ustvarjanje posameznega zapisa. Časi so izraženi v sekundah.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Vrsta&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="2">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax">Zahtevana polja</th>
    <th class="tg-0lax">Vsa podprta polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Opravilo</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dodelitev</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član ekipe</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Odvisnost</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operacije množičnega ustvarjanja
Naslednja tabela prikazuje čase izvedbe za ustvarjanje več zapisov. Natančneje je Microsoft izmeril čase izvedbe za ustvarjanje 20, 50 in 100 zapisov v enem nizu OperationSet. Časi so izraženi v sekundah.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Vrsta&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="6">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 zapisov</th>
    <th class="tg-0lax" colspan="2">50 zapisov</th>
    <th class="tg-0lax" colspan="2">100 zapisov</th>
  </tr>
  <tr>
    <th class="tg-0lax">Zahtevana polja</th>
    <th class="tg-0lax">Vsa podprta polja</th>
    <th class="tg-0lax">Zahtevana polja</th>
    <th class="tg-0lax">Vsa podprta polja</th>
    <th class="tg-0lax">Zahtevana polja</th>
    <th class="tg-0lax">Vsa podprta polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Opravilo</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dodelitev</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Odvisnost</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Operacije množičnega ustvarjanja na v entitetah **Projekt** in **Član ekipe** niso vključene v to tabelo, ker je čas izvajanja teh operacij podoben času izvajanja, ko je API za ustvarjanje enega zapisa klican večkrat. Ti API-ji se v okolju Dataverse zaženejo takoj.

Naslednja slika prikazuje diagram časov izvajanja za entitete **Opravilo**, **Naloga** in **Odvisnost**, ko je ustvarjenih 20, 50 in 100 zapisov in so uporabljena vsa podprta polja.

![Ustvarite graf časa izvajanja zapisa.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Posodobitev operacij
#### <a name="single-record-update-operations"></a>Operacije posodobitve enega zapisa
Naslednja tabela prikazuje čase izvedbe za posodobitve posameznega zapisa. Časi so izraženi v sekundah.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Vrsta&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="2">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax">Zahtevana polja </th>
    <th class="tg-0lax">Vsa podprta polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Opravilo</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član ekipe</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacije posodobitev v entitetah **Naloge virov** in **Odvisnost projektnega opravila** niso podprte.

#### <a name="bulk-update-operations"></a>Operacije množičnega posodabljanja
Naslednja tabela prikazuje čase izvedbe za posodobitev več zapisov. Natančneje je Microsoft izmeril čase izvedbe za posodobitev 20, 50 in 100 zapisov v enem nizu OperationSet. Časi so izraženi v sekundah.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Vrsta&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="6">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 zapisov</th>
    <th class="tg-0lax" colspan="2">50 zapisov</th>
    <th class="tg-0lax" colspan="2">100 zapisov</th>
  </tr>
  <tr>
    <th class="tg-0lax">Zahtevana polja</th>
    <th class="tg-0lax">Vsa podprta polja</th>
    <th class="tg-0lax">Zahtevana polja</th>
    <th class="tg-0lax">Vsa podprta polja</th>
    <th class="tg-0lax">Zahtevana polja</th>
    <th class="tg-0lax">Vsa podprta polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Opravilo</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član ekipe</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacije posodobitev v entitetah **Naloge virov** in **Odvisnost projektnega opravila** niso podprte.

Naslednja slika prikazuje diagram časov izvajanja za entitete Opravilo in Član ekipe, ko je posodobljenih 20, 50 in 100 zapisov in so uporabljena vsa podprta polja.

![Posodobite graf časa izvajanja zapisa.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operacije brisanja
#### <a name="single-record-delete-operations"></a>Operacije brisanja posameznega zapisa
Naslednja tabela prikazuje čase izvedbe za brisanje posameznega zapisa. Časi so izraženi v sekundah.

| Vrsta zapisa | Čas  |
|-------------|-------|
| Opravilo        | 20.12 |
| Dodelitev  | 10.86 |
| Član ekipe | 12.52 |
| Odvisnost  | 20.89 |

> [!NOTE]
> Operacije brisanja v entiteti **Projekt** niso podprte.

#### <a name="bulk-delete-operations"></a>Operacije množičnega brisanja
Naslednja tabela prikazuje čase izvedbe za brisanje več zapisov. Natančneje je Microsoft izmeril čase izvedbe za brisanje 20, 50 in 100 zapisov v enem nizu OperationSet. Časi so izraženi v sekundah.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Vrsta&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="3">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 zapisov</th>
    <th class="tg-0lax">50 zapisov</th>
    <th class="tg-0lax">100 zapisov</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Opravilo</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dodelitev</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član ekipe</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Odvisnost</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacije brisanja v entiteti **Projekt** niso podprte.

Naslednja slika prikazuje diagram časov izvajanja za entitete **Opravilo**, **Naloga**, **Član ekipe** in **Odvisnost**, ko je izbrisanih 20, 50 in 100 zapisov.

![Izbrišite graf časa izvajanja zapisa.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Opažanja
Za vsako operacijo zapisa traja približno 800 milisekund, da API **ExecuteOperationSet** pošlje zahtevo storitvi razporejanja projektov. Nato traja približno pet sekund, da storitev razporejanja projektov obdela koristno vsebino in pokliče Dataverse. Preostali čas izvajanja je porabljen za izvajanje poslovne logike in zapisovanje podatkov v zbirko podatkov Dataverse.

Ko je ustvarjenih, posodobljenih ali izbrisanih 100 zapisov, traja približno tri sekunde, da API **ExecuteOperationSet** pošlje zahtevo storitvi razporejanja projektov. Nato traja približno pet sekund, da storitev razporejanja projektov obdela zahteve in pokliče Dataverse. Množične operacije morajo plačati enkratni **davek na storitve razporejanja projektov** in to za vse zapise v OperationSet. Zato imajo množične operacije bistveno krajši povprečni čas izvedbe kot operacije z enim zapisom.

## <a name="scenarios"></a>Scenariji
Naslednja tabela prikazuje čase izvajanja, ko se API-ji razporeda projekta uporabljajo za izvedbo določenih scenarijev. Časi so izraženi v sekundah.

| Scenarij                                                                   | Čas  |
|----------------------------------------------------------------------------|-------|
| Ustvarite projekt s 40 opravili.                                      | 36.01 |
| Ustvarite projekt s 40 opravili in 20 odvisnostmi.                  | 38.11 |
| Ustvarite projekt s 40 opravili in 30 nalogami.                   | 60.17 |
| Ustvarite projekt s 40 opravili, 20 odvisnostmi in 30 nalogami. | 60.27 |

## <a name="best-practices"></a>Najboljše prakse
Na podlagi rezultatov prejšnjega scenarija se API-ji bolje obnesejo v naslednjih pogojih:

  - Združite čim več operacij skupaj. Povprečni čas izvajanja za množične operacije je boljši od povprečnega časa izvajanja za operacije z enim zapisom. Manjše kot je število atributov OperationSets v uporabi, hitrejši bo povprečni čas izvajanja.
  - Nastavite samo minimalne atribute, ki so potrebni za izvedbo vašega scenarija. Bodite pozorni pri izbiri vrste neobveznih polj, vključenih v zahtevo OperationSet. Polja, ki vsebujejo tuje ključe ali polja s skupno vrednostjo, bodo negativno vplivala na zmogljivost.
