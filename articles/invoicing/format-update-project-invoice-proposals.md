---
title: Upravljanje predlogov za račune projekta
description: V tej temi so na voljo podrobnosti o obdelavi računov za stranke v aplikaciji Project Operations za primere uporabe z viri/brez zalog.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 83e5af60d0a3baf0b59da2a97c6b156ef5b2b7ed
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089305"
---
# <a name="manage-project-invoice-proposals"></a>Upravljanje predlogov za račune projekta

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Predloge za račune projekta lahko obdela vaš oddelek za obračunavanje, če sta izpolnjena naslednja dva pogoja:

  - Vodja projekta potrdi predračun v storitvi Microsoft Dataverse.
  - Vse neobračunane časovne in materialne prodajne transakcije, ki so vključene v predračun, se knjižijo v dnevniku **integracij za Project Operations** v storitvi Dynamics 365.

Sledite spodnjim korakom za dokončanje predloga za račun projekta v storitvi Dynamics 365 Finance.

1. Preglejte podatke za obračunavanje za časovne in materialne transakcije in objavite dnevnik **integracij za Project Operations**.
2. Preglejte podatke za obračunavanje za mejnike obračunavanja po fiksni ceni.
3. Preglejte in oblikujte predlog za račun projekta.
4. Knjižite in natisnite račune za projekt.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Upravljanje podatkov za obračunavanje v dnevniku integracij za Project Operations

Opravljena dela projekta, ustvarjena v storitvi Dataverse, pregleda projektni računovodja in jih knjiži. Za več informacij o delu z dnevnikom integracij glejte [Dnevnik integracij v aplikaciji Project Operations](../project-accounting/project-operations-integration-journal.md).

Dejanski stroški in neobračunana dejanska prodaja so dodani v dnevnik integracij kot ločene vrstice:

  - Lastna cena enote in znesek stroškov v dejanski ceni sta privzeto nastavljena iz transakcije dejanskih stroškov projekta v storitvi Dataverse.
  - Prodajna cena enote in znesek prodaje v neobračunani prodajni transakciji sta privzeto nastavljena iz dejanske neobračunane prodajne transakcije v storitvi Dataverse.

### <a name="billing-sales-tax"></a>Obračun prometnega davka

Izračun prometnega davka za obračun je določen s kombinacijo polj **Obračunavanje skupine prometnega davka** in **Obračunavanje skupine davka od prodaje izdelkov** v neobračunanem prodajnem zapisu v vrstici dnevnika **integracij za Project Operations**. Sistem nastavi vrednosti teh polj kot privzete na podlagi nastavitev na zavihku **Finance** na strani **Parametri za upravljanje projektov in računovodstvo**.

- **Metoda skupine prometnega davka** določa logiko za privzeto nastavitev skupine za obračun prometnega davka:
  
  - **Projekt**: kot privzeto vedno nastavi skupino za obračun prometnega davka iz projekta. Privzeto skupino za obračun prometnega davka v projektu lahko pregledate ali spremenite tako, da izberete **Prikaži privzeto računovodstvo** na strani **Vsi projekti**.
  - **Projektna pogodba**: kot privzeto vedno nastavi skupino za obračun prometnega davka iz projektne pogodbe. Privzeto skupino prometnega davka v projektni pogodbi lahko pregledate ali spremenite tako, da izberete **Prikaži privzeto računovodstvo** na strani **Projektne pogodbe**.
  - **Stranka**: kot privzeto vedno nastavi skupino za obračun prometnega davka iz stranke.
  - **Iskanje**: išče po vseh zgornjih entitetah in izbere prvo vrednost, ki je na voljo. Iskanje se začne z entiteto **Projekt**, nato pa sledita entiteti **Projektna pogodba** in **Stranka**.

- **Metoda skupine davka od prodaje izdelkov** določa logiko za privzeto nastavitev skupine za obračun davka od prodaje izdelkov:
  
  - Za vrste transakcij »Čas«, »Stroški« in »Dajatve« je skupina za obračun davka od prodaje izdelkov vedno privzeto nastavljena iz entitete **Kategorija projekta**.
  - Pri materialnih transakcijah je skupina za obračun davka od prodaje izdelkov privzeto nastavljena glede na nastavitev **Metoda skupine davka od prodaje izdelkov** v možnosti **Parametri za upravljanje projektov in računovodstvo**. Številka artikla privzeto nastavi skupino davka od prodaje izdelkov iz entitete **Izdan izdelek**. Kategorija privzeto nastavi skupino davka od prodaje izdelkov iz entitete **Kategorija projekta**.

### <a name="financial-dimensions"></a>Finančne razsežnosti

Finančne razsežnosti za neobračunane prodajne evidence v dnevniku **integracij za Project Operations** so privzeto nastavljene iz entitete **Projekt**. Finančne razsežnosti lahko pregledate in prilagodite z izbiro možnosti **Porazdeli zneske**. Če želite spremeniti finančne razsežnosti neobračunanega prodajnega zapisa po objavi dnevnika integracij, vendar pred potrditvijo predračuna, pojdite na **Vsi projekti** > **Upravljanje** > **Knjižene transakcije**, izberite transakcijo in nato izberite še **Postopek** > **Prilagajanje računovodstva**.

### <a name="exchange-rates"></a>Menjalni tečaji

Valuta neobračunane transakcije v storitvi Dataverse se uporablja kot valuta transakcije v storitvi Finance in se pretvori v računovodsko valuto podjetja po menjalnih tečajih, določenih v storitvi Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Upravljanje finančnih atributov mejnikov obračunavanja 

Podrobnosti projektne pogodbe, ki uporabljajo način obračunavanja po fiksni ceni, so fakturirane v možnosti [Mejniki s fiksno ceno](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Projektni računovodja lahko pregleda mejnike obračunavanja v storitvi Finance, tako da odpre **Upravljanje projektov in računovodstvo** > **Vsi projekti** > **Upravljanje** > **Transakcije za kupca**.

### <a name="billing-sales-tax"></a>Obračun prometnega davka

Vrednosti **Skupina prometnega davka** in **Skupina davka od prodaje izdelkov** so privzeto nastavljene iz nastavitev, ko je v storitvi Dataverse ustvarjen nov mejnik obračunavanja. Sistem nastavi vrednosti za ta polja kot privzete na podlagi nastavitev na zavihku **Finance** na strani **Parametri za upravljanje projektov in računovodstvo**.

- **Metoda skupine prometnega davka** določa logiko za privzeto nastavitev **skupine za obračun prometnega davka**:

    - **Projekt** kot privzeto vedno nastavi skupino za obračun prometnega davka iz projekta. Privzeto skupino prometnega davka v projektu lahko pregledate ali spremenite tako, da izberete **Prikaži privzeto računovodstvo** na strani **Vsi projekti**.
    - **Projektna pogodba** kot privzeto vedno nastavi skupino za obračun prometnega davka iz projektne pogodbe. Privzeto skupino prometnega davka v projektni pogodbi lahko pregledate ali spremenite tako, da izberete **Prikaži privzeto računovodstvo** na strani **Projektne pogodbe**.
    - **Stranka** kot privzeto vedno nastavi skupino za obračun prometnega davka iz stranke.
    - **Iskanje** išče po vseh entitetah na tem seznamu in izbere prvo vrednost, ki je na voljo. Iskanje se začne z entiteto **Projekt**, nato pa sledita entiteti **Projektna pogodba** in **Stranka**.

- **Skupina davka od prodaje izdelkov za mejnik s fiksno ceno** se uporablja za nastavitev privzete vrednosti v polju **Skupina za davek od prodaje izdelkov**.

### <a name="financial-dimensions"></a>Finančne razsežnosti

Privzete finančne razsežnosti za mejnik obračunavanja s fiksno ceno so nastavljene v podrobnostih projektne pogodbe. Odprite **Projektne pogodbe** > **Prikaži privzeto računovodstvo** in na zavihku **Podrobnosti pogodbe** izberite **podrobnost pogodbe za ceno**, nato pa nastavite vrednosti finančne razsežnosti, ki jih želite uporabiti kot privzete.

Projektni računovodja lahko ureja podatke o prometnem davku in finančnih razsežnostih v mejnikih računov, dokler ni ustvarjen predlog za račun projekta.


## <a name="create-project-invoice-proposals"></a>Ustvarjanje predlogov za račune projekta

Predloge za račune projekta lahko pregledate v modulu **Upravljanje projektov in računovodstvo**, tako da odprete **Računi za projekt** > **Predlogi za račune projekta**.

Glava predloga za račun projekta se ustvari v storitvi Finance, ko je predračun potrjen v storitvi Dataverse. Za lažje usklajevanje sistem nastavi številko predloga za račun projekta v storitvi Finance na enako številko kot jo ima ID predračuna v storitvi Dataverse. Ker predračuni niso nujno potrjeni v istem vrstnem redu kot so ustvarjeni, mora zaporedje številk predlogov za račun projekta v storitvi Finance omogočiti spreminjanje na nižje in višje številke. Sledite spodnjim korakom, da konfigurirate zaporedja številk:

1. V storitvi Finance odprite **Skrbništvo organizacije** > **Zaporedja števil** > **Zaporedja števil**.
2. V filtru **Območje** izberite **Projekti**.
3. V filtru **Sklic** izberite **Predlog za račun**.
4. Uporabite polje **Podjetje** in filtrirajte vse pravne osebe z omogočeno integracijo za Project Operations Dataverse.
5. Odprite **Podrobnosti zaporedja števil** in na zavihku **Splošno** nastavite:

    - **Dovoli uporabniške spremembe: na nižjo številko** = **Da**
    - **Dovoli uporabniške spremembe: na višjo številko** = **Da**

Sistem doda vrstice predloga za račun projekta s periodičnim postopkom **Uvoz iz pripravljalne tabele** (**Upravljanje projektov in računovodstvo** > **Redno** > **Integracija za Project Operations** > **Uvoz iz pripravljalne tabele**). Ta postopek lahko izvedete ročno ali z uporabo rednega urnika. Sistem ne bo dodal vrstic v dokument predloga za račun, dokler niso vse vrstice pripravljene za fakturiranje. Časovne in materialne transakcije so pripravljene za fakturiranje šele, ko so knjižene v dnevniku **integracij za Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Oblikovanje in tiskanje predlogov za račune

Projektni računovodja lahko prilagodi izpis računa za projekt z uporabo strani **Oblikovanje predloga za račun** in možnostmi upravljanja tiskanja.

### <a name="format-invoice-proposals"></a>Oblikovanje predlogov za račune

Stran **Oblikovanje predlogov računov** omogoča prikaz razvrščanja transakcij po meri na računu za projekt stranke.

1. Na strani **Predlog za račun projekta** izberite **Natisni** > **Oblikovanje predloga za račun**.
2. Izberite **Novo**, da ustvarite novo skupino za izpis računa za projekt.
3. V polju **Podrobnosti/povzetek** izberite možnosti za to razvrščanje:

    - Izberite **Podrobnost** za tiskanje podrobnosti transakcije za račun stranke.
    - Izberite **Povzetek** za tiskanje povzetka transakcije za račun stranke.

> [!NOTE]
> Izbor v polju **Podrobnosti/povzetek** na strani **Oblikovanje predloga za račun** preglasi možnost, ki je izbrana v polju **Oblika zapisa računa** na strani **Predlogi za račune**, za tiskanje podrobnega računa ali povzetka računa.

- Na zavihku **Razpoložljive transakcije** izberite vrstice transakcij, ki jih želite vključiti v ta razdelek, in nato še **Vključi transakcije**, da jih premaknete na zavihek **Izbrane transakcije**.
- Izberite **Premakni gor** in **Premakni dol**, da spremenite vrstni red razdelkov.
- Izberite **Predogled tiskanja**, da odprete predogled oblikovanega računa.

### <a name="print-management"></a>Upravljanje tiskanja

Upravljanje tiskanja uporablja različne datoteke poročil za tiskanje, določanje ciljev in prilagajanje besedila noge za račun. Upravljanje tiskanja je mogoče nastaviti na ravni modula, vendar je te nastavitve mogoče preglasiti za določeno stranko, pogodbo ali predlog za račun. Za dostop do te funkcije na strani **Predlog za račun projekta** izberite **Natisni** > **Upravljanje tiskanja**.

Nastavitev upravljanja tiskanja je prikazana kot drevesni pogled, kjer vsaka raven vozlišča prikaže razpoložljive dokumente za prilagajanje. Izpise po meri lahko dodelite na ravni modula, stranke, pogodbe ali predloga za račun. Če želite spremeniti izpis izvirnega dokumenta, razširite želeno vozlišče in izberite **Izvirni element**. V polju **Oblika zapisa poročila** izberite obliko zapisa poročila, ki jo želite uporabiti za tiskanje. Za oblike zapisa poročil po meri lahko uporabite [okvir za upravljanje poslovnih dokumentov](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Knjiženje predlogov za račune

Ko je račun pregledan in urejen in so vrstice predloga za računa zadovoljive, preverite skupni znesek računa in prometni davek. V skupini **Podrobnosti** izberite **Skupaj** in nato **Knjiži**, da knjižite račun.

Če si želite račun ogledati pred knjiženjem, počistite potrditveno polje **Knjiženje**. Na računu je natisnjeno **Predračun**, kar pomeni, da gre za vzorec računa. Če želite natisniti račun, izberite potrditveno polje **Natisni račun**.

Poleg strani **Predlog za račun** lahko predloge za račune knjižite tudi tako, da zaženete redno opravilo **Knjiži predloge za račune**. To opravilo najdete v možnosti **Upravljanje projektov in računovodstvo** > **Redno** > **Projektni računi** > **Knjiženje predlogov za račune**.

Ta stran prikaže vse predloge za račune, ki so pripravljeni za knjiženje. Knjiženje predlogov za račune lahko načrtujete tako, da izberete **Paket**. **Parameter za paketno obdelavo** nastavite na **Da** in nato nastavite ponavljanje paketne obdelave tako, da izberete **Ponavljanje**.
