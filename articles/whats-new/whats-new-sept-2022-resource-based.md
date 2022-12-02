---
title: Novosti za september 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so bile na voljo v izdaji storitve Microsoft Dynamics 365 Project Operations septembra 2022 za scenarije, ki temeljijo na virih/nezalogi.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634826"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti za september 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.46.0.60. storitve Dataverse
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.29

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

| Območje funkcij | Ime funkcije | Več informacij |
| --- | --- | --- |
| Upravljanje priložnosti | **Revizija in aktivacija ponudb**<br>Project Operations prinaša popolno podporo prodajnemu procesu. Projektne ponudbe lahko aktivirate, da predstavljajo stanje, kjer je ponudba na voljo samo za branje in je v pregledu. Aktivirane ponudbe lahko revidirate, da se ustvarijo nove ponudbe, ki imajo povečano številko revizije. Aktivirane projektne ponudbe ali revizije ponudbe lahko zaprete kot »pridobljeno« ali »izgubljeno«. | [Aktiviranje in popravljanje projektne ponudbe](/dynamics365/project-operations/sales/activation-and-revision) |
| Zaračunavanje in oblikovanje cen | **Privzeto oblikovanje cen glede na neznani časovni pas**<br>Aplikacija Project Operations je uvedla koncept neznanega datuma glede na časovni pas za vse dejanske vrednosti projekta. Novo polje, **Datum transakcije**, je zdaj na voljo v vrsticah dnevnika in dejanskih vrednostih ter bo uporabljeno za shranjevanje datuma, ko je bila transakcija izvedena, vendar brez pretvorbe tega datuma v usklajen univerzalni čas. Ta datum bo uporabljen za nadaljnje procese, kot sta privzeto nastavljanje cene in ustvarjanje računov. | <p>[Določitev mer stroškov za ocene in dejanske vrednosti, ki temeljijo na projektih](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Določitev prodajnih cen za ocene in dejanske vrednosti, ki temeljijo na projektu](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Zaračunavanje in oblikovanje cen | **Preglasitve cen, ki začnejo veljati na določen datum, v aplikaciji Project Operations**<br>Funkcija preglasitve cen, ki začnejo veljati na določen datum, omogoča način za preglasitev ali spremembo določenih cen v ceniku. | [Preglasitve cen, ki začnejo veljati na določen datum](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Podizvajalske pogodbe | **Usklajevanje računov podizvajalcev in dobaviteljev**<br>Ta funkcija strankam omogoča ustvarjanje podizvajalskih pogodb za nakup časa virov, kategorij stroškov in materialov, ki se uporabljajo za projektno delo. Prav tako strankam omogoča, da v aplikacijah za finance in postopke zapisujejo račune dobaviteljev, ki bodo vodjem projektov na voljo za preverjanje v okolju Dataverse. | <p>[Upravljanje podizvajalskih pogodb](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Ustvari račune dobavitelja](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Čas in strošek | **Globalni odobritelj**<br>Ta funkcija omogoča neodvisnega razvijalca programske opreme (ISV) in centralizirano odobritev, ne glede na stanje projekta ali člana ekipe v projektu. | [Varnost in odobritve](/dynamics365/project-operations/approvals/approvals-security) |
| Upravljanje stroškov | **Možnost knjiženja obveznosti za stroške v valuti dobavitelja**<br>Ta funkcija omogoča knjiženje poročil o stroških v valuti dobavitelja za način gotovinskega plačila. | [Možnost knjiženja obveznosti za stroške v valuti dobavitelja](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Nabava projekta | **Plačila dobavitelju, ki se izvedejo po prejemu plačila**<br>Ta funkcija omogoča uporabo funkcije »Plačilo, ki se izvede po prejemu plačila (PWP)« v okoljih Project Operations brez zaloge. Omogoča blokiranje/zadrževanje plačil dobavitelja na podlagi pogojev zadrževanja, dokler plačilo stranke ni prejeto. | [Plačila dobavitelju, ki se izvedejo po prejemu plačila](/dynamics365/project-operations/procurement/pay-when-paid) |
| Nabava projekta | **Projektne zahteve za nakup**<br>Ta funkcija uporabnikom omogoča ustvarjanje naročilnic, povezanih s projektom, v pravnih entitetah, kjer je omogočena integracija aplikacije Project Operations v Dynamics 365 Customer Engagement. Projektne naročilnice se lahko uporabijo za zapisovanje nabave materiala, ki ni na zalogi, za projekt, ki jo izvaja osebje oddelka za nabavo. Naročilnice za projekte ne bodo sinhronizirane z okoljem Dataverse. Vendar pa lahko uporabite navidezno entiteto, da prikažete vrstice naročilnice za projekt v okolju Dataverse za informacije vodje projekta. Stroški računa dobavitelja, povezani s projektom, so integrirani z entiteto dejanskih vrednosti projekta v okolju Dataverse. Cena projekta je z dnevnikom integracije aplikacije Project Operations zapisana v podknjigo projekta. | |
|Načrtovanje in sledenje projektov|**Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja** </br> </br>API za urejanje krivulj dodelitve virov omogoča razvijalcem, da programsko določijo trud osebe, ki je dodelila opravilo, v katerem koli podprtem časovnem obdobju za bolj natančno načrtovanje truda v časovnih fazah.|[Uporaba API-jev razporejanja projektov za izvajanje postopkov s pomočjo entitet razporejanja](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V naslednji tabeli so prikazane preslikave za dvojno zapisovanje, ki so spremenjene ali dodane v izdaji različice Project Operations iz septembra 2022.

| Preslikava entitete | Posodobljena različica | Comments |
| -------------- | ------------------- | ------------|
| Dejanske vrednosti integracije za Project Operations (msdyn_actuals) | 1.0.0.15 | Ta tabela podpira obdelavo dejanskih vrednosti podizvajalcev z aplikacijo Project Operations za scenarije, ki temeljijo na virih. |
| Entiteta za izvoz računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Ta tabela podpira obdelavo dejanskih vrednosti podizvajalcev z aplikacijo Project Operations za scenarije, ki temeljijo na virih. |
| Entiteta za izvoz vrstice računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Ta tabela podpira obdelavo dejanskih vrednosti podizvajalcev z aplikacijo Project Operations za scenarije, ki temeljijo na virih. |

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Zaračunavanje in oblikovanje cen | 2754422 | Ocene materiala in stroškov ne tečejo v aplikacijo Finance, ko so projekti kopirani v okolje Dataverse. |
| Čas in strošek | 2787409 | Neveljavni odobritelj lahko odobri vnos časa, ki ne temelji na projektu. |
| Upravljanje priložnosti | 2788907 | Posodobljeno sporočilo o napaki pri preverjanju edinstvenosti za vrstice naročila, ki vključujejo zastavice. |
| Čas in strošek | 2842253 | Obravnava izjeme z vrednostjo »null« za odobritev časa. |
| Zaračunavanje in oblikovanje cen | 2844181 | Neuspelo pridobivanje ID-ja korelacije blokira ustvarjanje računa. |
| Zaračunavanje in oblikovanje cen | 2876628 | QLD, CLD – ocena razrešitve cenika bi morala uporabljati podedovana polja obsega datuma za cenik. |
| Podizvajalske pogodbe | 2893222 | Če za podrobnosti podizvajalske pogodbe ni določena nobena vloga, bi moralo biti mogoče to vrstico izbrati pri članu ekipe za katero koli vlogo. |

### <a name="project-management-and-accounting-in-finance"></a>Pregled upravljanja projektov in računovodstva v aplikaciji Finance

Za informacije o popravkih napak, vključenih v tej posodobitvi, se prijavite v storitev Microsoft Dynamics Lifecycle Services in si oglejte [Članek zbirke znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcije so privzeto vklopljene v prihajajoči izdaji

Naslednja tabela navaja funkcije, ki so privzeto vklopljene v različici 10.0.30. Večino funkcij, ki so bile samodejno vklopljene, je mogoče izklopiti v razdelku [Upravljanje funkcij](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). V prihodnosti bodo nekatere funkcije, ki so bile samodejno vklopljene, morda odstranjene iz razdelka »Upravljanje funkcij« in bodo postale obvezne. Ta sprememba strankam zagotavlja uporabo trenutnih funkcionalnosti, da lahko izboljšave, ko so dodane gradijo na trenutni funkcionalnosti. Funkcije ne bodo nikoli samodejno omogočene v manj kot enem letu, razen če se ugotovi, da so bistvene.

| Ime funkcije | Datum omogočanja | Funkcija je dodana | Stanje funkcije | Modul |
| --- | --- | --- |--- |--- |
| Omogočanje asinhronega postopka, ko mora uporabnik preklopiti med sinhronimi in asinhronimi postopki | 21. oktober 2022 | 9. april 2021 | Privzeto vklopljeno | Upravljanje stroškov |
| Potrebna je ocena pravilnika glede stroškov za potrdila | 21. oktober 2022 | 20. december 2021 | Privzeto vklopljeno | Upravljanje stroškov |
| Pogled seznama poročil o stroških, ustvarjenih z dodelitvijo delavcev | 21. oktober 2022 | 19. februar 2020 | Privzeto vklopljeno | Upravljanje stroškov |
| Izračun skupne prevožene razdalje za proračunsko leto | 21. oktober 2022 | 10. maj 2022 | Privzeto vklopljeno | Upravljanje stroškov |
