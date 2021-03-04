---
title: Dejanske vrednosti
description: Ta tema vsebuje informacije o delu z dejanskimi vrednostmi v storitvi Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126340"
---
# <a name="actuals"></a>Dejanske vrednosti 

_**Velja za:** za scenarije v storitvi Project Operations, ki temeljijo na virih/brez zaloge_

Dejanski podatki se nanašajo na količino dela, ki je bilo opravljeno za projekt. Ustvarjeni so kot rezultat vnosov časa in stroškov ter dnevniških vnosov in računov.

## <a name="journal-lines-and-time-submission"></a>Vrstice dnevnikov in vnos časa

Za več informacij o vnosu časa glejte [Pregled vnosa časa](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Čas in materiali

Ko je predloženi vnos časa, povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in material, sta v sistemu ustvarita dve vrstici dnevnika, ena za ceno in druga za neobračunano prodajo.

### <a name="fixed-price"></a>Fiksna cena

Ko je poslan časovni vnos za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se v sistemu ustvari samo vrstica dnevnika za ceno.

### <a name="default-pricing"></a>Privzete cene

Logika za oblikovanje privzetih cen se nahaja v vrstici dnevnika. Vrednosti polj iz časovnega vnosa se kopirajo v vrstico dnevnika. Te vrednosti vključujejo datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in rezultat valute v skladu z ustreznim cenikom.

Polja, ki vplivajo na privzete cene, kot sta **Vloga** in **Organizacijska enota**, se uporabljajo za določanje ustrezne cene v vrstici dnevnika. Časovnemu vnosu lahko dodate polje po meri. Če za časovni vnos dodate polje po meri in želite, da se vrednost polja razširi na dejanske vrednosti, ustvarite polje v entiteti »Dejanske vrednosti« in za kopiranje polja iz časovnega vnosa v dejanske vrednosti uporabite preslikave polj.

## <a name="journal-lines-and-basic-expense-submission"></a>Oddaja vrstic dnevnika in osnovnih stroškov

Za več informacij o vnosu stroškov glejte [Pregled stroškov](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Čas in materiali

Ko je vnos osnovnega stiška, povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in material, se v sistemu ustvarita dve vrstici dnevnika, ena za ceno in druga za neobračunano prodajo.

### <a name="fixed-price"></a>Fiksna cena

Ko je poslan osnovni strošek za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se v sistemu ustvari samo vrstica dnevnika za ceno.

### <a name="default-pricing"></a>Privzete cene

Logika vnosa privzetih cen za stroške temelji na kategoriji stroškov. Datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in valuta se uporabijo za ugotavljanje ustreznega cenika. Vendar pa je za ceno znesek, ki ga je uporabnik vnesel, privzeto nastavljen neposredno v povezani vrstici dnevnika stroškov za strošek in prodajo.

Vnos privzetih cen na enoto na podlagi kategorije za vnose stroška ni na voljo.

## <a name="use-entry-journals-to-record-costs"></a>Uporaba dnevnikov vnosov za zapisovanje stroškov

V dnevnike lahko beležite stroške ali prihodke v razredih transakcij za material, dajatve, čas, stroške ali davke. Dnevniki se lahko uporabljajo v naslednje namene:

- Beleženje dejanskih stroškov materiala in prodaje za posamezen projekt.
- Prenos dejanskih vrednosti o transakcijah iz drugega sistema v storitev Microsoft Dynamics 365 Project Operations.
- Beleženje stroškov, ki so nastali v drugem sistemu. Ti stroški lahko vključujejo stroške naročanja ali podizvajanja.

> [!IMPORTANT]
> Aplikacija ne preveri veljavnosti vrste vrstice dnevnika ali povezanih cen, ki so vnesene v vrstico dnevnika. Zato mora dnevnike vnosov za ustvarjanje dejanskih vrednosti uporabljati oseba, ki se popolnoma zaveda računovodskega vpliva dejanskih vrednosti na projekt. Zaradi vpliva te vrste dnevnika morate skrbno izbrati, kdo ima dostop do ustvarjanja dnevnikov vnosov.
## <a name="record-actuals-based-on-project-events"></a>Zapisovanje dejanskih vrednosti na podlagi projektnih dogodkov

Aplikacija Project Operations beleži finančne transakcije, do katerih pride med projektom. Te transakcije se zapišejo kot dejanske vrednosti. V spodnjih tabelah so prikazane različne vrste dejanskih vrednosti, ki so ustvarjene, glede na to, ali gre za časovne in materialne transakcije ali transakcije s fiksno ceno ali gre za stopnjo pred prodajo oziroma interni projekt.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Vir pripada isti organizacijski enoti kot pogodbena enota projekta

<table>
<thead>
<tr>
<th rowspan="3">Dogodek</th>
<th colspan="4">Obračunan ali prodan projekt</th>
<th rowspan="3">Projekt v fazi predprodaje</th>
<th rowspan="3">Interni projekt</th>
</tr>
<tr>
<th colspan="2">Čas in materiali</th>
<th colspan="2">Fiksna cena</th>
</tr>
<tr>
<th>Opravljeno delo</th>
<th>Valuta transakcije</th>
<th>Fiksna cena</th>
<th>Valuta transakcije</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ustvari se časovni vnos.</td>
<td colspan="6">V entitetah dejanskih podatkov ni dejavnosti</td>
</tr>
<tr>
<td>Pošlje se časovni vnos.</td>
<td colspan="6">V entitetah dejanskih podatkov ni dejavnosti</td>
</tr>
<tr>
<td rowspan="2">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</td>
<td>Dejanska cena</td>
<td>Valuta pogodbene enote</td>
<td rowspan="2">Dejanska cena</td>
<td rowspan="2">Valuta pogodbene enote
<td rowspan="2">Dejanska cena</td>
<td rowspan="2">Dejanska cena</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – za obračunavanje</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="3">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</td>
<td>Dejanska cena</td>
<td>Valuta pogodbene enote</td>
<td rowspan="3">Dejanska cena</td>
<td rowspan="3">Valuta pogodbene enote</td>
<td rowspan="3">Dejanska cena</td>
<td rowspan="3">Dejanska cena</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – obračuna se za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – za razliko se ne obračuna</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="2">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</td>
<td>Storniranje neobračunane prodaje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="2">Obračunana prodaja za mejnik</td>
<td rowspan="2">Valuta projektne pogodbe</td>
<td rowspan="2">Ni na voljo</td>
<td rowspan="2">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="3">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</td>
<td>Storniranje neobračunane prodaje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja – obračuna se za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Obračunana prodaja – za razliko se ne obračuna</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="2">Račun je popravljen s povečano količino za obračunavanje.</td>
<td>Obračunana prodaja – storniranje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="5">
<ul>
<li>Storniranje obračunane prodaje za mejnik</li>
<li>Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></li>
</ul>
</td>
<td rowspan="5">Valuta projektne pogodbe</td>
<td rowspan="5">Ni na voljo</td>
<td rowspan="5">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="3">Račun je popravljen z zmanjšano količino za obračunavanje.</td>
<td>Obračunana prodaja – storniranje</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Obračunana prodaja za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Neobračunana prodaja – obračuna se za razliko</td>
<td>Valuta projektne pogodbe</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Vir pripada organizacijski enoti, ki se razlikuje od pogodbene enote projekta

<table>
<thead>
<tr>
<th rowspan="3">Dogodek</th>
<th colspan="4">Obračunan ali prodan projekt</th>
<th rowspan="3">Projekt v fazi predprodaje</th>
<th rowspan="3">Interni projekt</th>
</tr>
<tr>
<th colspan="2">Čas in materiali</th>
<th colspan="2">Fiksna cena</th>
</tr>
<tr>
<th>Opravljeno delo</th>
<th>Valuta transakcije</th>
<th>Fiksna cena</th>
<th>Valuta transakcije</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ustvari se časovni vnos.</td>
<td colspan="6">V entitetah dejanskih podatkov ni dejavnosti</td>
</tr>
<tr>
<td>Pošlje se časovni vnos.</td>
<td colspan="6">V entitetah dejanskih podatkov ni dejavnosti</td>
</tr>
<tr>
<td rowspan="4">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</td>
<td>Dejanska cena</td>
<td>Valuta pogodbene enote</td>
<td rowspan="4">Dejanska cena</td>
<td rowspan="4">Valuta pogodbene enote</td>
<td rowspan="4">Dejanska cena</td>
<td rowspan="4">Dejanska cena</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – za obračunavanje</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Cena enote vira</td>
<td>Valuta enote vira</td>
</tr>
<tr>
<td>Prodaja znotraj organizacije</td>
<td>Valuta pogodbene enote</td>
</tr>
<tr>
<td rowspan="5">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</td>
<td>Dejanska cena</td>
<td>Valuta pogodbene enote</td>
<td rowspan="5">Dejanska cena</td>
<td rowspan="5">Valuta pogodbene enote</td>
<td rowspan="5">Dejanska cena</td>
<td rowspan="5">Dejanska cena</td>
</tr>
<tr>
<td>Cena enote vira</td>
<td>Valuta enote vira</td>
</tr>
<tr>
<td>Prodaja znotraj organizacije</td>
<td>Valuta pogodbene enote</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – obračuna se za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Dejanska neobračunana prodaja – za razliko se ne obračuna</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="2">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</td>
<td>Storniranje neobračunane prodaje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="2">Obračunana prodaja za mejnik</td>
<td rowspan="2">Valuta projektne pogodbe</td>
<td rowspan="2">Ni na voljo</td>
<td rowspan="2">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="3">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</td>
<td>Storniranje neobračunane prodaje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
<td rowspan="3">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja – obračuna se za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Obračunana prodaja – za razliko se ne obračuna</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="2">Račun je popravljen s povečano količino za obračunavanje.</td>
<td>Obračunana prodaja – storniranje</td>
<td>Valuta projektne pogodbe</td>
<td rowspan="5">
<ul>
<li>Storniranje obračunane prodaje za mejnik</li>
<li>Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></li>
</ul>
</td>
<td rowspan="5">Valuta projektne pogodbe</td>
<td rowspan="5">Ni na voljo</td>
<td rowspan="5">Ni na voljo</td>
</tr>
<tr>
<td>Obračunana prodaja</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td rowspan="3">Račun je popravljen z zmanjšano količino za obračunavanje.</td>
<td>Obračunana prodaja – storniranje</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Obračunana prodaja za novo količino</td>
<td>Valuta projektne pogodbe</td>
</tr>
<tr>
<td>Neobračunana prodaja – obračuna se za razliko</td>
<td>Valuta projektne pogodbe</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]