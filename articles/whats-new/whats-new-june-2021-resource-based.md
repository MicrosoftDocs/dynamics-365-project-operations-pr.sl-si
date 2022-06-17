---
title: Novosti za junij 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Project Operations junija 2021 za scenarije, ki temeljijo na virih/brez zalog.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bc8475554c4348fa1e88b9090450bd3bfaa924e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910604"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti za junij 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek velja za naslednje Dynamics 365 Project Operations komponente in različice:

- Aplikacija Project Operations v okolju Dynamics 365 Dataverse (različica 4.11.0.156 ali 4.11.0.164).
- Vodenje projektov in računovodstvo v okoljih aplikacij Finance in Operations, različica 10.0.19.

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

V to izdajo so vključene naslednje funkcije:

- Možnost brisanja [Vrstice predloga za račun projekta za scenarije prilagoditve](../invoicing/correct-project-invoice-proposals.md).
- Razčlenjene vrstice s stroški prikazujejo imena podkategorij v poročilu o stroških [Prenovljena poročila o stroških – nove funkcije](../expense/expense-reports-reimagined.md#new-features).
- Ko ustvarjate nov strošek, lahko način plačila izberete v podoknu z novimi stroški.
- Splošna razpoložljivost API-jev razporeda projekta. Ta nova funkcionalnost omogoča strankam, da programsko izvajajo operacije ustvarjanja, posodabljanja in brisanja projektnih opravil, dodelitve virov, odvisnosti opravil in zapise članov projektne skupine. Za več informacij glejte [Uporaba API-jev razporeda projekta za izvajanje operacij z entitetami za načrtovanje](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. 

Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svoje operacije projekta Dataverse rešitev in različica rešitve aplikacij za finance in operacije. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivna različica za preslikovanje se prikaže na strani **Dvojno zapisovanje**, in sicer v stolpcu **Različica**. Novo različico za preslikovanje aktivirajte tako, da izberete možnost **Različica preslikave tabele**, ko ste izbrali najnovejšo različico, pa jo shranite. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težave, upoštevajte navodila iz razdelka [Težava z manjkajočimi stolpci tabele v preslikavi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v vodniku za odpravljanje težav pri dvojnem zapisovanju.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| Zaračunavanje in oblikovanje cen | 2281417 | Odpravljena je bila težava, povezana z neuspešnim samodejnim ustvarjenjem računa s pomočjo razporeda za izdajanje računov. |
| Zaračunavanje in oblikovanje cen | 2287835 | Učinkovitost potrjevanja računa je izboljšana. |
| Upravljanje priložnosti | 2222555 | Ob uporabi funkcije **Uvoz iz ocene projekta** mora biti zaračunavanje ocene materiala ustrezno kopirano v podrobnosti vrstice ponudbe. |
| Upravljanje priložnosti | 2223427 | Na voljo so prilagoditve za dejanje, **GenerateRetainersFromRetainerScheduleOptions**. |
| Upravljanje priložnosti | 2277528 | Izračun fiksne vrednosti mejnika obračunavanja za podrobnosti pogodbe z več strankami. |
| Načrtovanje in sledenje projektov | 2226110 | Odpravljena je bila predhodna težava s funkcijo **Ustvari zahtevo** v mreži **Projektna ekipa**. |
| Načrtovanje in sledenje projektov | 2208109 | Uporabniki ne morejo ustvariti projekta, za katerega je uporabljena drugačna valuta kot za povezana opravila. |
| Načrtovanje in sledenje projektov | 2258228 | Seznam polj, ki jih je ob uporabi API-ja razporeda mogoče spreminjati z entitetami **Razporejanje**, je posodobljen. |
| Načrtovanje in sledenje projektov | 2293989 | Ustrezne jezikovne in področne nastavitve je treba posredovati v mrežo **Projektna opravila**. |
| Upravljanje virov | 2220493 | Izboljšana je bila uporabniška izkušnja v mreži **Opravilo** ob tem, ko zahtevo za vir hitro označite kot zaključeno. |
| Upravljanje virov | 2330496 | Odpravljena je bila težava z nalaganjem elementa **Plošča razporeda**. (Posodobitev kakovosti je na voljo v različici 4.11.0.164) |
| Čas in strošek | 2194431 | Mreža **Vnos časa** mora upoštevati začetek tedna, kot je določeno v nastavitvah **Sistemske nastavitve**. |
| Čas in strošek | 2277311 | Kazalec ostane v mreži **Vnos časa**, ko iz celice v njej izbrišete vrednost. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Vodenje projektov in računovodstvo na Dynamics 365 Finance

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje projektov in računovodstvo | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | Možnosti **Opombe obrazcev** in **Nastavitev obrazca** nista vidni pod možnostjo **Nastavitev upravljanja projektov** pri pravnih osebah storitve Finance, ki so integrirane z aplikacijo Project Operations. |
| Upravljanje projektov in računovodstvo | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Privzeti opis za DDV je prazen, ko za kupone za račun projekta velja **Vrsta knjiženja** = **Prometni davek**. |
| Upravljanje projektov in računovodstvo | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Podvojene transakcije so knjižene, ko je v okolju Dataverse z integracijo za aplikacijo Project Operations uporabljeno obračunavanje, ki temelji na opravilu. |
| Upravljanje projektov in računovodstvo | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Odstotek dokončanega v prepoznavanju prihodkov je neustrezen ob uporabi integracije za aplikacijo Project Operations. |
| Upravljanje projektov in računovodstvo | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Razmejitev prihodkov je v integriranem scenariju aplikacije Project Operations na čakajočem računu dobavitelja podvojena. |
| Upravljanje projektov in računovodstvo | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Dnevnika integracij ni mogoče knjižiti, ko je za pravilo profila prihodkov nastavljena nastavitev **Skupina**. |
| Upravljanje projektov in računovodstvo | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Prejetega računa ni mogoče knjižiti za naročilnice projekta, ki vsebujejo vrstice z več merskimi enotami. |
| Upravljanje projektov in računovodstvo | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Privzete finančne razsežnosti v projektu ni mogoče posodobiti ob uporabi entitete podatkov **V2**. |
| Upravljanje projektov in računovodstvo | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Paketna obdelava za ustvarjenje ocen projekta traja predolgo. |
| Upravljanje projektov in računovodstvo | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Če izbrišete pogodbo, se izbriše tudi s stranko povezan naslov. |
| Pot in stroški | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Pogoj poteka dela za odobritev poročila o stroških ni pravilno ucenjen. |
| Pot in stroški | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Pravilnik za poročilo o stroških ID-ja projekta ne ocenjuje pravilno. |
| Pot in stroški | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Dejanje **Razdeli na osebno za stroškovne transakcije med podjetji** ne deluje pravilno. |
| Pot in stroški | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Utemeljitve za vrstice poročila o stroških se pomotoma izbrišejo skupaj z nekaterimi zahtevami za pot. To se zgodi, ko se recID poročila o stroških ujema z zahtevami za pot. |
| Pot in stroški | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | V mobilni aplikaciji za upravljanje stroškov pride do napake, ko je polje **ID projekta** v pravilnikih za poročilo o stroških obvezno. |
| Pot in stroški | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Medpodjetnih stroškov, povezanih s projektom, ni mogoče urejati. Namesto tega se prikaže naslednje sporočilo o napaki: »Sklic na predmet ni nastavljen na primerek predmeta.« |
| Pot in stroški | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Po knjiženju poročila o stroških sta v podknjigo banke vnesena napačna valuta in znesek. |
| Pot in stroški | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Funkcija *Izbris transakcij s kreditnimi karticami* je bila izboljšana.  |
| Pot in stroški | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Prometni davek, vključen v poročilo o stroških, ni izračunan dosledno, ko je za pravno osebo določena drugačna valuta za poročanje. |
| Pot in stroški | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Dodajanje novih denarnih potnih stroškov vpliva na uspešnost. |
| Pot in stroški | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Pravila iz pravilnika glede stroškov se v poročilu o stroških ne sprožijo. |
| Pot in stroški | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Z nalaganjem nove kategorije v skupni rabi ob uporabi ogrodja za upravljanje podatkov se odstranijo vse podkategorije za kategorije v skupni rabi. |
| Pot in stroški | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Ko ustvarite vrstico stroška, nato pa izberete kategorijo, se prikaže naslednje sporočilo o napaki: »Kombinacija DOM-a skupine prometnega davka in STD-ja skupine davka od prodaje izdelka ni veljavna.« |
| Pot in stroški | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | V mobilni aplikaciji za upravljanje stroškov je prišlo do težav s sinhronizacijo. |
