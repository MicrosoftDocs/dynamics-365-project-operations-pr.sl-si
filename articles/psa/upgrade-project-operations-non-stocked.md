---
title: Nadgradite s Project Service Automation na Project Operations
description: Ta tema ponuja pregled postopka nadgradnje Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
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
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 01/10/2022
ms.locfileid: "7954303"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Nadgradite s Project Service Automation na Project Operations

Z veseljem objavljamo prvo od treh faz za nadgradnjo Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Project Operations. Ta tema ponuja pregled za stranke, ki se podajajo na to razburljivo potovanje. Prihodnje teme bodo vključevale premisleke razvijalcev in podrobnosti o izboljšavah funkcij. Ne bodo le zagotovili napotkov, ki vam bodo pomagali pri pripravi na nadgradnjo na Project Operations, ampak tudi pojasnili, kaj lahko pričakujete po nadgradnji.

Program dostave nadgradnje bo razdeljen na tri faze.

| Nadgradite dostavo | 1. faza (januar 2022) | 2. faza (aprilski val 2022) | 3. faza (aprilski val 2022) |
|------------------|------------------------|---------------------------|---------------------------|
| Ni odvisnosti od strukture razčlenitve dela (WBS) za projekte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS v okviru trenutno podprtih omejitev projektnega delovanja | | :heavy_check_mark: | :heavy_check_mark: |
| WBS je zunaj trenutno podprtih omejitev Project Operations, vključno s podporo za namizni odjemalca Project | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funkcije postopka nadgradnje 

Kot del postopka nadgradnje smo na zemljevid mesta dodali dnevnike nadgradnje, tako da lahko skrbniki lažje diagnosticirajo napake. Poleg novega vmesnika bodo dodana nova pravila za preverjanje veljavnosti, ki bodo zagotovila celovitost podatkov po nadgradnji. Procesu nadgradnje bodo dodane naslednje potrditve.

| Validacije | 1. faza (januar 2022) | 2. faza (aprilski val 2022) | 3. faza (aprilski val 2022) |
|-------------|------------------------|---------------------------|---------------------------|
| WBS bo preverjen glede na pogoste kršitve integritete podatkov (na primer dodelitve sredstev, ki so povezane z isto nadrejeno nalogo, vendar imajo različne nadrejene projekte). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bo potrjena glede na [znane omejitve projekta za splet](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bo preverjen glede na znane omejitve odjemalca namizja Project. | | :heavy_check_mark: | :heavy_check_mark: |
| Viri, ki jih je mogoče rezervirati, in projektni koledarji bodo ocenjeni glede na običajne nezdružljive izjeme koledarskih pravil. | | :heavy_check_mark: | :heavy_check_mark: |

V 2. fazi bodo stranke, ki bodo nadgradile na Project Operations, svoje obstoječe projekte nadgradile na izkušnjo samo za branje za načrtovanje projekta. V tej izkušnji samo za branje bo celoten WBS viden v mreži za sledenje. Za urejanje WBS lahko izberejo vodje projektov **Pretvorba** na glavni **Projekti** stran. Proces v ozadju bo nato posodobil projekt, tako da bo podpiral novo izkušnjo načrtovanja projektov iz Project za splet. Ta faza je primerna za stranke, ki imajo projekte, ki ustrezajo [znane omejitve projekta za splet](/project-for-the-web/project-for-the-web-limits-and-boundaries).

V 3. fazi bo dodana podpora za namizni odjemalec Project v korist strank, ki želijo še naprej urejati svoje projekte iz te aplikacije. Če pa se obstoječi projekti pretvorijo v nov projekt za spletno izkušnjo, bo dostop do dodatka onemogočen za vsak pretvorjen projekt.

## <a name="prerequisites"></a>Zahteve

Da je stranka upravičena do nadgradnje 1. faze, mora izpolnjevati naslednja merila:

- Ciljno okolje ne sme vsebovati nobenih zapisov v **msdyn_projecttask** entiteta.
- Veljavne licence Project Operations morajo biti dodeljene vsem aktivnim uporabnikom stranke. 
- Stranka mora potrditi postopek nadgradnje v vsaj enem neprodukcijskem okolju, ki ima reprezentativen nabor podatkov, ki je usklajen s produkcijskimi podatki.
- Ciljno okolje mora biti posodobljeno na posodobitev Project Service Automation Release 38 ali novejšo.

Predpogoji za fazo 2 in fazo 3 bodo posodobljeni, ko se približujejo datumi splošne razpoložljivosti.

## <a name="licensing"></a>Licenciranje

Če imate aktivne licence za Project Service Automation, lahko namestite in uporabljate Project Operations, ki vključuje vse zmogljivosti Project Service Automation in še več. Na ta način lahko preizkusite zmogljivosti Project Operations, medtem ko še naprej uporabljate Project Service Automation v produkciji. Ko vam potečejo licence za Project Service Automation, boste morali preiti na Project Operations. Ko načrtujete ta prehod, morate upoštevati dejstvo, da licenca Project Operations ne vključuje licence Project Service Automation.

## <a name="testing-and-refactoring-customizations"></a>Testiranje in refaktoriranje prilagoditev

Kot izhodišče uvozite vse prilagoditve v čisto okolje Project Operations (lite), da potrdite, da je uvoz uspešen in da se poslovne operacije obnašajo po pričakovanjih.

Tukaj je nekaj stvari, na katere morate biti pozorni:

- Uvoz morda ne bo uspel zaradi manjkajočih odvisnosti. Z drugimi besedami, referenčna polja za prilagoditve ali druge komponente, ki so bile odstranjene v Project Operations. V tem primeru odstranite te odvisnosti iz razvojnega okolja.
- Če vaše neupravljane in upravljane rešitve vključujejo komponente, ki niso prilagojene, odstranite te komponente iz rešitve. Na primer, ko prilagodite **Projekt** entiteto, svoji rešitvi dodajte samo glavo entitete. Ne dodajte vseh polj. Če ste predhodno dodali vse podkomponente, boste morda morali ročno ustvariti novo rešitev in ji dodati ustrezne komponente.
- Obrazci in pogledi morda ne bodo videti kot nepričakovani. V nekaterih okoliščinah, če ste prilagodili katerega koli od pripravljenih obrazcev ali pogledov, lahko prilagoditve preprečijo, da bi začele veljati nove posodobitve v Project Operations. Če želite ugotoviti te težave, priporočamo, da opravite vzporedni pregled čiste namestitve Project Operations in namestitve Project Operations, ki vključuje vaše prilagoditve. Primerjajte najpogosteje uporabljene obrazce v vašem podjetju, da potrdite, da je vaša različica obrazca še vedno smiselna in da v čisti različici obrazca nekaj ne manjka. Naredite isto vrsto vzporednega pregleda za vse poglede, ki ste jih prilagodili.
- Poslovna logika morda ne uspe med izvajanjem. Ker sklici na polja v vaših vtičnikih v času uvoza niso potrjeni, poslovna logika morda ne bo uspela zaradi sklicevanj na polja, ki ne obstajajo več, in morda boste prejeli sporočilo o napaki, ki je podobno naslednjemu primeru: "'Projekt' entiteta ne vsebuje atributa z Ime = 'msdyn_plannedhours' in NameMapping = 'Logično'." V tem primeru spremenite svoje prilagoditve, tako da bodo uporabljale nova polja. Če v logiki vtičnika uporabljate samodejno ustvarjene razrede proxyja in močne reference tipov, razmislite o ponovni generiranju teh proxyjev iz čiste namestitve. Na ta način lahko preprosto prepoznate vsa mesta, kjer so vaši vtičniki odvisni od zastarelih polj.

Ko posodobite svoje prilagoditve za čist uvoz projektnih operacij, pojdite na naslednje korake.

## <a name="end-to-end-testing-in-lower-environments"></a>Testiranje od konca do konca v nižjih okoljih

### <a name="run-the-upgrade-in-production"></a>Zaženite nadgradnjo v produkciji

1. V Power Platform skrbniško središče, poiščite in izberite svoje okolje. Nato v aplikacijah poiščite in izberite **Dynamics 365 Project Operations**.
2. Izberite **Namestite** za začetek nadgradnje. The Power Platform skrbniški center bo to namestitev predstavil kot novo namestitev. Vendar bo zaznana prisotnost starejše različice Project Service Automation in obstoječa namestitev bo nadgrajena.

    Po končani nadgradnji mora okolje pokazati, da je Project Operations nameščen in da Project Service Automation ni nameščen.

    > [!NOTE]
    > Nadgradnja lahko traja več ur, odvisno od količine podatkov v okolju. Osrednja ekipa, ki upravlja nadgradnjo, bi morala ustrezno načrtovati in izvajati nadgradnjo med izven delovnega časa. V nekaterih primerih, če je količina podatkov velika, je treba nadgradnjo izvesti med vikendom. Odločitev o načrtovanju bi morala temeljiti na rezultatih testiranja v nižjih okoljih.

3. Po potrebi nadgradite rešitve po meri. Na tej točki uvedite vse spremembe, ki ste jih naredili v svojih prilagoditvah v [Testiranje in refaktoriranje prilagoditev](#testing-and-refactoring-customizations) razdelek tega tema.
4. Pojdi do **Nastavitve** \> **Rešitve** in izberite za odstranitev **Operacije projekta Zastarele komponente** rešitev.

    Ta rešitev je začasna rešitev, ki vsebuje obstoječi podatkovni model in komponente, ki so prisotne med nadgradnjo. Če odstranite to rešitev, odstranite vsa polja in komponente, ki se ne uporabljajo več. Na ta način pomagate poenostaviti vmesnik ter olajšati integracijo in razširitev.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Večje spremembe med avtomatizacijo projektnih storitev in projektnim delovanjem

V tem razdelku je povzetek glavnih sprememb, ki jih lahko pričakujete med avtomatizacijo projektnih storitev in projektnim delovanjem.

### <a name="project-planning"></a>Načrtovanje projekta

Zmogljivosti načrtovanja projekta v Project Operations se ne zanašajo več na kombinacijo logike na strani odjemalca in logike na strani strežnika. Namesto tega Project Operations uporablja Project za splet kot mehanizem za razporejanje. Ta sprememba zmožnosti načrtovanja omogoča več novih funkcij, kot so pogledi plošče in Gantt, načrtovanje na podlagi virov, [elemente kontrolnega seznama nalog](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c), in načini načrtovanja projekta. Nove zmožnosti načrtovanja podpira tudi bogat nabor novih [aplikacijski programski vmesniki (API)](../project-management/schedule-api-preview.md). Ti API-ji so namenjeni zagotavljanju, da nobena programska operacija za ustvarjanje, posodabljanje ali brisanje entitete v WBS ne pokvari izračunanih polj v urniku.

## <a name="billing-and-pricing"></a>Zaračunavanje in cene

Kot del nenehnih naložb v projektne operacije je na voljo več novih zmogljivosti za obračunavanje in določanje cen. Tukaj je nekaj primerov:

- [Snemanje porabe materiala pri projektih in projektnih nalogah](../material/material-usage-log.md)
- [Upravljanje podizvajalcev](../pro/subcontracting/managing-subcontracts-overview.md)
- [Pogodbe za predplačila in honorarje](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status pogodbe, ki ne bo presegel in potrditve](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Zaračunavanje na podlagi opravil

## <a name="frequently-asked-questions"></a>Pogosto zastavljena vprašanja

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Katere vrste uvajanja so trenutno podprte za nadgradnjo?

| Vir                                                 | Cilj                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Uvajanje Project Operations Lite                        | Podprto               |
| Dynamics 365 Finance Vodenje projektov in računovodstvo | Uvajanje Project Operations Lite                        | Trenutno ni podprto |
| Finance Projektno vodenje in računovodstvo              | Project Operations za primere uporabe z viri/brez zalog     | Trenutno ni podprto |
| Finance Projektno vodenje in računovodstvo              | Project Operations za primere uporabe z naročili na zalogi/v proizvodnji | Trenutno ni podprto |
| Avtomatizacija projektnih storitev 3.x                         | Project Operations za primere uporabe z viri/brez zalog     | Trenutno ni podprto |
| Projekt za splet (namensko okolje)            | Uvajanje Project Operations Lite                        | Trenutno ni podprto |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kako lahko namestim Project Operations, preden je na voljo orodje za nadgradnjo?

Preden je orodje za nadgradnjo na voljo, obstajata dve možnosti za namestitev Project Operations:

- Zagotovite novo okolje.
- Uvedite Project Operations ločeno v katero koli prodajno organizacijo, kjer ni prisotna Project Service Automation.

> [!NOTE]
> Če je Project Service Automation nameščen v organizaciji, vendar ni bil uporabljen, ga je mogoče odstraniti. Ko popolnoma odstranite Project Service Automation, lahko Project Operations namestite v isto organizacijo.
