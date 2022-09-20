---
title: Nadgradite s Project Service Automation na Project Operations
description: Ta članek nudi pregled postopka nadgradnje Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 43ea29aeafb62f3ecd69b316f2c0a5b791707da5
ms.sourcegitcommit: bc21fbe8547534d2644269f873eb05d509840f23
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446056"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Nadgradite s Project Service Automation na Project Operations

Z veseljem objavljamo prvo od treh faz za nadgradnjo Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Project Operations. Ta članek ponuja pregled za stranke, ki se podajajo na to razburljivo potovanje. Prihodnji članki bodo vključevali razmišljanja razvijalcev in podrobnosti o izboljšavah funkcij. Ne bodo le zagotovili smernic, ki vam bodo pomagale pri pripravi na nadgradnjo na Project Operations, temveč vam bodo tudi pojasnili, kaj lahko pričakujete po nadgradnji.

Program nadgradnje bo razdeljen v tri faze.

| Dostava nadgradnje | 1. faza (januar 2022) | 2. faza (november 2022) | 3. faza (aprilski val 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Brez odvisnosti od strukture razčlenitve dela (WBS) za projekte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS znotraj trenutno podprtih omejitev projektnih operacij | | :heavy_check_mark: | :heavy_check_mark: |
| WBS je zunaj trenutno podprtih omejitev Project Operations, vključno s podporo za namiznega odjemalca Project | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funkcije postopka nadgradnje 

Kot del postopka nadgradnje smo na zemljevid spletnega mesta dodali dnevnike nadgradnje, tako da lahko skrbniki lažje diagnosticirajo napake. Poleg novega vmesnika bodo dodana nova pravila za preverjanje veljavnosti, ki zagotavljajo celovitost podatkov po nadgradnji. V postopek nadgradnje bodo dodane naslednje potrditve.

| Validacije | 1. faza (januar 2022) | 2. faza (november 2022) | Faza 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS bo preverjen glede pogostih kršitev celovitosti podatkov (na primer dodelitve virov, ki so povezane z isto nadrejeno nalogo, vendar imajo različne nadrejene projekte). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bo potrjen glede na [znane omejitve Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bo preverjen glede na znane omejitve namiznega odjemalca Project. | |  | :heavy_check_mark: |
| Viri, ki jih je mogoče rezervirati, in koledarji projektov bodo ovrednoteni glede na pogoste izjeme pravila za nezdružljive koledarje. | | :heavy_check_mark: | :heavy_check_mark: |

V 2. fazi bodo stranke, ki nadgradijo na Project Operations, svoje obstoječe projekte nadgradile na izkušnjo samo za branje za načrtovanje projektov. V tej izkušnji samo za branje bo celoten WBS viden v mreži za sledenje. Za urejanje WBS lahko izberejo vodje projektov **Pretvorba** na glavnem **Projekti** strani. Postopek v ozadju bo nato posodobil projekt, tako da bo podpiral novo izkušnjo razporejanja projekta iz Projecta za splet. Ta faza je primerna za stranke, ki imajo projekte, ki ustrezajo [znane omejitve Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

V fazi 3 bo dodana podpora za namiznega odjemalca Project v korist strank, ki želijo še naprej urejati svoje projekte iz te aplikacije. Če pa so obstoječi projekti pretvorjeni v novo izkušnjo Project for the Web, bo dostop do dodatka onemogočen za vsak pretvorjeni projekt.

## <a name="prerequisites"></a>Zahteve

Da bi bila stranka upravičena do nadgradnje faze 1, mora izpolnjevati naslednja merila:

- Ciljno okolje ne sme vsebovati nobenih zapisov v **msdyn_projecttask** entiteta.
- Veljavne licence Project Operations morajo biti dodeljene vsem aktivnim uporabnikom stranke. 
- Stranka mora potrditi postopek nadgradnje v vsaj enem neprodukcijskem okolju, ki ima reprezentativen nabor podatkov, ki je usklajen s produkcijskimi podatki.
- Ciljno okolje je treba posodobiti na izdajo posodobitve za Project Service Automation 41 (3.10.62.162) ali novejšo.

Predpogoji za fazo 2 in fazo 3 bodo posodobljeni, ko se približujejo datumi splošne razpoložljivosti.

## <a name="licensing"></a>Licenciranje

Če imate aktivne licence za Project Service Automation, lahko namestite in uporabljate Project Operations, ki vključuje vse zmožnosti Project Service Automation in več. Na ta način lahko preizkusite zmogljivosti Project Operations, medtem ko še naprej uporabljate Project Service Automation v proizvodnji. Po poteku licenc za Project Service Automation boste morali preiti na Project Operations. Ko načrtujete ta prehod, morate upoštevati dejstvo, da licenca Project Operations ne vključuje licence Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Testiranje in preoblikovanje prilagoditev

Kot izhodišče uvozite vse prilagoditve v čisto okolje Project Operations (Lite), da potrdite, da je uvoz uspešen in da se poslovne operacije obnašajo po pričakovanjih.

Tukaj je nekaj stvari, na katere morate biti pozorni:

- Uvoz morda ne uspe zaradi manjkajočih odvisnosti. Z drugimi besedami, referenčna polja prilagoditev ali druge komponente, ki so bile odstranjene v Project Operations. V tem primeru odstranite te odvisnosti iz razvojnega okolja.
- Če vaše neupravljane in upravljane rešitve vključujejo komponente, ki niso prilagojene, odstranite te komponente iz rešitve. Na primer, ko prilagodite **Projekt** entiteti, svoji rešitvi dodajte samo glavo entitete. Ne dodajte vseh polj. Če ste predhodno dodali vse podkomponente, boste morda morali ročno ustvariti novo rešitev in ji dodati ustrezne komponente.
- Obrazci in pogledi morda ne bodo prikazani po pričakovanjih. V nekaterih okoliščinah, če ste prilagodili kateri koli od pripravljenih obrazcev ali pogledov, lahko prilagoditve preprečijo, da bi nove posodobitve v Project Operations začele veljati. Za prepoznavanje teh težav priporočamo, da vzporedno pregledate čisto namestitev Project Operations in namestitev Project Operations, ki vključuje vaše prilagoditve. Primerjajte obrazce, ki se najpogosteje uporabljajo v vašem podjetju, da potrdite, da je vaša različica obrazca še vedno smiselna in ji ne manjka ničesar od čiste različice obrazca. Opravite isto vrsto vzporednega pregleda za vse poglede, ki ste jih prilagodili.
- Poslovna logika lahko odpove med izvajanjem. Ker sklicevanja na polja v vaših vtičnikih niso preverjena v času uvoza, lahko poslovna logika odpove zaradi sklicevanj na polja, ki ne obstajajo več, in morda prejmete sporočilo o napaki, ki je podobno temu primeru: »'Projekt' entiteta ne vsebuje atributa z Name = 'msdyn_plannedhours' in NameMapping = 'Logical'." V tem primeru spremenite svoje prilagoditve tako, da bodo uporabljale nova polja. Če v logiki vtičnika uporabljate samodejno ustvarjene razrede proxy in močne reference tipov, razmislite o ponovnem generiranju teh proxyjev iz čiste namestitve. Na ta način lahko preprosto prepoznate vsa mesta, kjer so vaši vtičniki odvisni od zastarelih polj.

Ko posodobite svoje prilagoditve za čist uvoz projektnih operacij, nadaljujte z naslednjimi koraki.

## <a name="end-to-end-testing-in-development-environments"></a>Testiranje od konca do konca v razvojnih okoljih

### <a name="initiate-upgrade"></a>Začni nadgradnjo 

1. V Power Platform skrbniško središče, poiščite in izberite svoje okolje. Nato v aplikacijah poiščite in izberite **Dynamics 365 Project Operations**.
2. Izberite **Namestite** za začetek nadgradnje. The Power Platform skrbniško središče bo to namestitev predstavilo kot novo namestitev. Vendar pa bo zaznana prisotnost prejšnje različice Project Service Automation in obstoječa namestitev bo nadgrajena.

    Ko je nadgradnja končana, bi moralo okolje pokazati, da je Project Operations nameščen in da Project Service Automation ni nameščen.

    > [!NOTE]
    > Odvisno od količine podatkov v okolju lahko nadgradnja traja več ur. Osrednja ekipa, ki upravlja nadgradnjo, mora ustrezno načrtovati in izvajati nadgradnjo med izven delovnega časa. V nekaterih primerih, če je količina podatkov velika, je treba nadgradnjo izvesti med vikendom. Odločitev o razporedu bi morala temeljiti na rezultatih testiranja v nižjih okoljih.

3. Po potrebi nadgradite rešitve po meri. Na tej točki uvedite vse spremembe, ki ste jih naredili v svojih prilagoditvah v [Testiranje in preoblikovanje prilagoditev](#testing-and-refactoring-customizations) razdelek tega članka.
4. Pojdi do **nastavitve** \> **Rešitve** in izberite, da odstranite **Zastarele komponente projektnih operacij** rešitev.

    Ta rešitev je začasna rešitev, ki vsebuje obstoječi podatkovni model in komponente, ki so prisotne med nadgradnjo. Z odstranitvijo te rešitve odstranite vsa polja in komponente, ki se ne uporabljajo več. Na ta način pomagate poenostaviti vmesnik ter olajšati integracijo in razširitev.
    
### <a name="validate-common-scenarios"></a>Potrdite pogoste scenarije

Ko potrdite svoje posebne prilagoditve, priporočamo, da pregledate tudi poslovne procese, ki so podprti v aplikacijah. Ti poslovni procesi vključujejo, vendar niso omejeni na, ustvarjanje prodajnih entitet, kot so ponudbe in pogodbe, ter ustvarjanje projektov, ki vključujejo WBS in odobritev dejanskih vrednosti.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Večje spremembe med Project Service Automation in Project Operations

V tem razdelku je povzetek večjih sprememb, ki jih lahko pričakujete med Project Service Automation in Project Operations.

### <a name="project-planning"></a>Načrtovanje projekta

Zmožnosti načrtovanja projekta v Project Operations se ne zanašajo več na kombinacijo logike na strani odjemalca in logike na strani strežnika. Namesto tega Project Operations uporablja Project za splet kot mehanizem za razporejanje. Ta sprememba v zmožnostih razporejanja omogoča številne nove funkcije, kot so pogledi plošče in Gantt, načrtovanje na podlagi virov, [elemente kontrolnega seznama opravil](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) in načini načrtovanja projektov. Nove zmožnosti razporejanja so podprte tudi z bogatim naborom novih [vmesniki za programiranje aplikacij (API)](../project-management/schedule-api-preview.md). Ti API-ji so namenjeni zagotavljanju, da nobena programska operacija za ustvarjanje, posodabljanje ali brisanje entitete v WBS ne pokvari izračunanih polj v urniku.

## <a name="billing-and-pricing"></a>Zaračunavanje in cene

Kot del nenehnih naložb v projektne operacije je na voljo več novih zmogljivosti pri zaračunavanju in cenah. Tukaj je nekaj primerov:

- [Evidentiranje porabe gradiva na projektih in projektnih nalogah](../material/material-usage-log.md)
- [Upravljanje s podizvajalci](../pro/subcontracting/managing-subcontracts-overview.md)
- [Pogodbe za predplačila in honorarje](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Stanje in potrditve pogodbe o prepovedi prekoračitve](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Zaračunavanje na podlagi nalog

## <a name="frequently-asked-questions"></a>Pogosto zastavljena vprašanja

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Katere vrste uvajanja so trenutno podprte za nadgradnjo?

| Vir                                                 | Cilj                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Uvedba Project Operations Lite                        | Podprto               |
| Dynamics 365 Finance Vodenje projektov in računovodstvo | Uvedba Project Operations Lite                        | Trenutno ni podprto |
| Finance Vodenje projektov in računovodstvo              | Project Operations za primere uporabe z viri/brez zalog     | Trenutno ni podprto |
| Project Service Automation 3.x                         | Project Operations za primere uporabe z viri/brez zalog     | Trenutno ni podprto |
| Projekt za splet (namensko okolje)            | Uvedba Project Operations Lite                        | Trenutno ni podprto |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kako lahko namestim Project Operations, preden je na voljo orodje za nadgradnjo?

Obstajata dve možnosti za namestitev Project Operations, preden je na voljo orodje za nadgradnjo:

- Zagotavljanje novega okolja.
- Razmestite Project Operations ločeno v kateri koli prodajni organizaciji, kjer Project Service Automation ni prisoten.

> [!NOTE]
> Če je Project Service Automation nameščen v organizaciji, vendar ni bil uporabljen, ga je mogoče odstraniti. Ko popolnoma odstranite Project Service Automation, lahko Project Operations namestite v isto organizacijo.
