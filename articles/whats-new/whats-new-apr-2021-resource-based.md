---
title: 'Novosti pri izdaji: April 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi'
description: Ta tema vsebuje informacije o posodobitvah kakovosti, ki so bile na voljo v izdaji Project Operations aprila 2021 za scenarije, ki temeljijo na virih/nezalogi.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 07622ed798fd8d70e0ce5cc42297bd5056402474
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589124"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti pri izdaji: April 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta tema velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

- Project Operations v okolju Dataverse različice 4.9.0.221
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance različica 10.0.17

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

V to izdajo so vključene naslednje funkcije:

- Materiali, ki niso na zalogi, za projekte. Ključne zmožnosti vključujejo:
  - Ocenjevanje in določanje cen materialov, ki niso na zalogi, med prodajnim ciklom za projekt. Za več informacij glejte [Nastavitev cen in stopenj prodaje za izdelke iz kataloga – poenostavljena različica](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Sledenje uporabi materialov, ki niso na zalogi, med izvajanjem projekta. Za več informacij glejte [Beleženje uporabe materiala v projektih in projektnih nalogah](../material/material-usage-log.md).
  - Izdajanje računov za stroške materialov, ki niso na zalogi. Za več informacij glejte [Upravljanje nedokončanih opravil obračunavanja](../proforma-invoicing/manage-billing-backlog.md).
  - Za informacije o načinu konfiguracije to funkcijo preberite razdelek [Konfiguracija materialov, ki niso na zalogi, in čakajočih računov dobavitelja](../procurement/configure-materials-nonstocked.md)
- Obračun na podlagi opravil: dodana je možnost povezovanja projektnih opravil s podrobnostmi projektne pogodbe, s čimer jih podvržemo enakemu načinu obračunavanja, pogostosti računov in strankam kot pri podrobnostih pogodbe. Ta povezava zagotavlja natančno izdajanje računov, računovodstvo, oceno prihodkov in priznanje za delovanje v skladu s to nastavitvijo pri projektnih opravilih.
- Novi API-ji v storitvi Dynamics 365 Dataverse omogočajo postopke ustvarjanja, posodabljanja in brisanja z **entitetami razporejanja**. Za več informacij glejte [Uporaba API-jev razporeda za izvajanje opravil z entitetami razporejanja](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

Na naslednjem seznamu so prikazane preslikave za dvojno zapisovanje, ki so spremenjene ali dodane v izdaji različice Project Operations iz aprila 2021.

| **Preslikava entitete** | **Posodobljena različica** | **Pripombe** |
| --- | --- | --- |
| Dejanske vrednosti integracije storitve Project Operations (msdyn\_actuals) | 1.0.0.14 | Prelikava je spremenjena tako, da sinhronizira dejanske vrednosti materialov projekta. |
| Integracijska entiteta za ocene stroškov v storitvi Project Operations (msdyn\_estimateslines) | 1.0.0.2 | Dodana je sinhronizacija projektne pogodbene vrstice z aplikacijami Finance in Operations za podporo za obračunavanje na podlagi nalog. |
| Integracijska entiteta za oceno časa v storitvi Project Operations (msdyn\_resourceassignments) | 1.0.0.5 | Dodana je sinhronizacija projektne pogodbene vrstice z aplikacijami Finance in Operations za podporo za obračunavanje na podlagi nalog. |
| Integracije tabele aplikacije Project Operations za ocene materiala (msdyn\_estimatelines) | 1.0.0.0 | Nov zemljevid tabele za sinhronizacijo ocen materiala Dataverse v aplikacije Finance in Operations. |
| Entiteta za izvoz računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Nov zemljevid tabele za sinhronizacijo glav računov dobavitelja iz aplikacij Finance in Operations v Dataverse. |
| Entiteta za izvoz vrstice računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Nov zemljevid tabele za sinhronizacijo vrstic računov dobavitelja iz aplikacij Finance in Operations na Dataverse. |

Vedno morate zagnati najnovejšo različico zemljevida v svojem okolju in omogočiti vse povezane zemljevide tabel, ko posodabljate svoje operacije projekta Dataverse rešitev in različica rešitve Finance and Operations. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Novo različico preslikave lahko aktivirate tako, da izberete možnost **Različice preslikave tabele**, izberete najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations v storitvi Dynamics 365 Dataverse

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| Zaračunavanje in cene | 2124532 | Gumb **Pravilni račun** se prikaže na predračunu, ko je na izvornem računu prisoten honorar oz. uporabljen honorar. Gumb je prikazan samo za okolja z različico Finance 10.0.19 ali novejšo. |
| Zaračunavanje in cene | 2224568 | Dodana logika za omogočanje prilagoditev, ki vključujejo priklic vtičnika za potrditev računa. |
| Zaračunavanje in cene | 2101098 | Izboljšana logika privzetih polj za predračun: **Naslov plačnika**, **Ime plačnika** in **Plačilni pogoji** se zdaj privzeto prikažejo iz ustreznega zapisa stranke o pogodbi o projektu. |
| Zaračunavanje in cene | 2021413 | Posodobljeni polji **Dejanski stroški** in **Prodaja** v entiteti **Opravilo**, da se vključi prodajne vrednosti iz naslova neobračunanih in obračunanih stroškov za opravila. |
| Zaračunavanje in cene | 2182110 | Pri kopiranju projektne pogodbe se ID podrobnosti pogodbe znova ustvari v ciljni projektni pogodbi, da se zagotovi njegova edinstvenost. |
| Upravljanje priložnosti | 2186741 | Dodana preverjanja veljavnosti, da se zagotovi, da polj **Izvor** in **Vrsta transakcije** ni mogoče posodobiti pri obstoječih podrobnostih o ponudbi. |
| Upravljanje priložnosti | 2191353 | Mejniki ne smejo biti ustvarjeni v podrobnosti pogodbe za čas in material. |
| Upravljanje priložnosti | 2216956 | Odpravite težave z možnostjo **Posodobi cene**. |
| Načrtovanje in sledenje | 2182979 | Izboljšana je funkcija kopiranja projekta, ki zagotavlja kopiranje vrstic za oceno stroškov iz prvotnega projekta. |
| Načrtovanje in sledenje | 2184144 | Izboljšana je funkcija kopiranja projekta, ki zagotavlja kopiranje imena položaja vira iz prvotnega projekta. |
| Načrtovanje in sledenje | 2184799 | Kopija projekta: poostren nadzor za zagotovitev, da predvidenega začetnega datuma ni mogoče spremeniti med kopiranjem. |
| Načrtovanje in sledenje | 2185134 | Kopija projekta: Predviden datum začetka ciljnega projekta je današnji datum. |
| Načrtovanje in sledenje | 2196373 | Kopija projekta: Zagotovite, da se zapisi vodje projekta in članov ekipe v projektni skupini ne podvajajo. |
| Načrtovanje in sledenje | 2211833 | Kopija projekta: Opravila virov se kopirajo iz izvornega projektnega opravila v ciljni projekt. |
| Načrtovanje in sledenje | 2186541 | Odpravljene težave na mreži **Ocene** pri razvrščanju po virih. |
| Načrtovanje in sledenje | 2166906 | Kategorija transakcije iz opravila je treba kopirati v entiteto **Dodelitev virov**. |
| Upravljanje virov | 2125362 | Odpravljene težave z ustvarjanjem splošnega člana ekipe z uporabo metode dodeljevanja na podlagi ur. |
| Čas in strošek | 2113603 | Odpravljena težava, povezana s prilagoditvijo, z odstranjevanjem atributov iz strani **Vnos časa**. Sistem zdaj preveri, ali atribut obstaja na strani, preden do njih dostopa s pomočjo skripta. |
| Čas in strošek | 2204377 | Ko izberete **Kopiraj teden** med vnosom časa, se kopirani časovni listi morajo prikazati samodejno. |
| Čas in strošek | 2209059 | Polje **Stanje** lahko urejate za časovne vnose Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vodenje projektov in računovodstvo v Dynamics 365 Finance

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| Upravljanje projektov in računovodstvo | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Razveljavitev izločitev ocen ne deluje v razdelku **Redno**.  |
| Upravljanje projektov in računovodstvo | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Funkcija **Računovodski popravek** ustvari težavo z računi glavne knjige, ki jih imajo izbrano možnost **Ne dovoli ročnega vnosa**. |
| Upravljanje projektov in računovodstvo | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Dodana poslovna logika za obdelavo računov za popravke, vključno s honorarjem ali uporabljenim honorarjem. |
| Upravljanje projektov in računovodstvo | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Pri knjiženju zneska prodaje PVT pri medpodjetnem izdajanju računov za projekt je izbran nepričakovan račun. |
| Upravljanje projektov in računovodstvo | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Pri delu s honorarji v storitvi Project Operations spreminjanje privzetega projekta v pogodbi po fakturiranju predplačil povzroča težave z dohodnimi odbitki. |
| Upravljanje projektov in računovodstvo | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Če v storitvi Project Operations odstranite projekt iz pogodbe, bi morali ponastaviti privzeti projekt pogodbe, če je to potrebno. |
| Upravljanje projektov in računovodstvo | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | V storitvi Project Operations so napačne vrstice stroškov prikazane na seznamu **Dodaj vrstico** na medpodjetniškem računu. |
| Upravljanje projektov in računovodstvo | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | V storitvi Project Operations stran **Nakupna pogodba** pri možnosti Finance ni vidna pravnim osebam z integracijo s storitvijo Project Operations. |
| Upravljanje projektov in računovodstvo | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Zaradi napake integracije Dataverse ponudbe ne morete pretvoriti v pridobljeno v storitvi Project Operations. |
| Upravljanje projektov in računovodstvo | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** lahko nastavi naslov računa za vir financiranja pri drugi stranki.  |
| Upravljanje projektov in računovodstvo | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | V storitvi Project Operations nobena dimenzija ni izbrana, ko ustvarite račun za knjiženje za transakcijo. |
| Potovanja in stroški | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Stanje denarnega predplačila se za poročilo o stroških ne posodobi, če je odobreno in objavljeno po vrsticah. |
| Potovanje in strošek | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Davki za razčlenjena poročila o odhodkih med podjetji niso pravilno izračunani. |
| Potovanje in strošek | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Dodatna polja, povezana s projekti, so prikazana na prenovljeni strani **Poročila o odhodkih med podjetji**. |
| Potovanje in strošek | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Na glavi potrdil o poročilih o stroških se prikaže napačno sporočilo o napaki. |
| Potovanje in strošek | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Poročilo o odhodkih je napačno objavljeno v medpodjetniškem scenariju, če je prometni davek knjižen ciljni pravni osebi. |
| Potovanje in strošek | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Datumi predložitve poročila se ne natisnejo na odobrenih poročilih o stroških. |
| Potovanje in strošek | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Polji **Datum odobritve** in **Datum zavrnitve** se po odobritvi stroškov ne zapolnita. |
| Potovanje in strošek | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Zahtevek za potovanje, ustvarjen za enega delavca, se lahko uporabi za poročilo o stroških drugega delavca. |
| Potovanje in strošek | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategorije stroškov se zaklenejo ob dodajanju nove vrstice stroškov. |
| Potovanje in strošek | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Razčlenjevanje že razdeljenih vrstic poročila o stroških povzroči nepopolno knjiženje kupona Obveznosti\Glavna knjiga in onemogoči pravilno delovanje raziskovalca računovodskih virov, ker je podvojen **TRVEXPTRANS.SOURCEDOCUMENTLINE**. |
| Potovanje in strošek | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Pravilnik zahtev za potovanje ne deluje po pričakovanjih. |
| Potovanje in strošek | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Ime računa dobavitelja ni prikazano v objavljenih transakcijah projekta za poročila o stroških. |
| Potovanje in strošek | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | V storitvi Project Operations ne morete odobriti časa z opravilom za medpodjetniški projekt. |
| Potovanje in strošek | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Kategorija vračila gotovinskega predplačila ne posodablja stanja gotovinskega predplačila, ko je objavljeno. |
| Potovanje in strošek | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Prodajna cena je napačno izračunana v poročilih o stroških, ki so bila ustvarjena v tuji valuti z uporabo uvoženih transakcij s kreditnimi karticami in so povezana s projektom. |
| Potovanje in strošek | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Razveljavljena je podatkovna entiteta **TrvRequisitionLine** in s tem povezan edinstven indeks. |
| Potovanje in strošek | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Dodani instrumenti za ustvarjanje **SOURCEDOCUMENTLINE**. |
| Potovanje in strošek | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Napačen dnevnik pomožne poslovne knjige je prikazan v medpodjetniškem scenariju, če je prometni davek knjižen ciljni pravni osebi. |
| Potovanje in strošek | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | V storitvi Project Operations se ocene stroškov ne izbrišejo iz storitve Finance, ko se izbrišejo iz storitve Dataverse. |
| Potovanje in strošek | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Če je kategorija odhodkov kategorija, ki ni projekt, se finančne razsežnosti, izbrane na strani **Stroški** ne kopirajo v poročilo o stroških. |
