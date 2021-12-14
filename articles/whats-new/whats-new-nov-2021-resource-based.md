---
title: Novosti v novembru 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta tema ponuja informacije o posodobitvah kakovosti, ki so na voljo v izdaji Project Operations novembra 2021 za scenarije, ki temeljijo na virih/brez zalog.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827346"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti v novembru 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

*Velja za: scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi*

Ta tema velja za naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Operacije projekta v različici okolja Dataverse 4.26.0.145, 4.26.0.148, ali 4.26.0.150
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance različica 10.0.22

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

V to izdajo so vključene naslednje funkcije:

- Programski vmesniki (API) za načrtovanje projektov zdaj podpirajo možnost ustvarjanja in brisanja projektnih segmentov.

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svojo rešitev Project Operations Dataverse in različico rešitve Finance. Nekatere funkcije in zmožnosti morda ne bodo delovale pravilno, če najnovejša različica zemljevida ni aktivirana. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili izključen zemljevid tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu zemljevida naletite na težavo, sledite navodilom v [Težava z manjkajočimi stolpci tabele na zemljevidih](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) razdelek vodnika za odpravljanje težav z dvojnim pisanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-in-dataverse"></a>Delovanje projekta v Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Zaračunavanje in oblikovanje cen | 2240080 | The **Plačilni pogoji** polje na predračunu ne sme biti podvojeno. |
| Zaračunavanje in oblikovanje cen | 2358236 | Popravek računa mora omogočati popravke, ki imajo vrstice z ničelno ceno. |
| Upravljanje virov | 2410072 | Dovoli nastavitev vira, ki je nalogi dodeljen kot vodja projekta. |
| Zaračunavanje in oblikovanje cen | 2430234 | Odpravite težavo pri izračunu stroškovne učinkovitosti. |
| Čas in strošek | 2436978 | Dovolite, da se čas vnese v formatu hh:mm. |
| Zaračunavanje in oblikovanje cen | 2448623 | Dovoli posodobitev cenikov, ko so povezani z organizacijsko enoto. |
| Čas in strošek | 2460396 | Dovolite, da se časovni vnos izbriše tako, da počistite celico. |
| Zaračunavanje in oblikovanje cen | 2467386 | Dovoli izbris projekta, ki ima nalogo, tudi če je naloga povezana z osvojeno ponudbo. |
| Čas in strošek | 2461744 | The **Moja neuspešna odobritev** pogled vsebuje samo odobritve projektov v **Oddano** stopnja. |
| Čas in strošek | 2464082 | Odstranite povezavo iz odobritev projekta do niza odobritev, ko se ujema ciljni status. |
| Čas in strošek | 2468108 | Opravilo Urnik ne sme nastaviti a **Obravnavati** status za komplet odobritev. |
| Čas in strošek | 2471503 | Izbrišite komplete odobritev, ki so stari sedem dni. |
| Zaračunavanje in oblikovanje cen | 2480687 | Referenca vrstice ponudbe se ne sme odstraniti, ko je ustvarjen mejnik vrstice ponudbe. |

### <a name="project-management-and-accounting-in-finance"></a>Vodenje projektov in računovodstvo v financah

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje projektov in računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Zadržani zneski prodajalcev v transakcijah stroškov projekta niso prikazani na seznamu transakcij. |
| Upravljanje projektov in računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Račun dobavitelja med podjetjem je pokvarjen, ko je vklopljena integracija računov dobavitelja. |
| Upravljanje projektov in računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Pogoji plačila na projektnih računih ne delujejo po pričakovanjih. |
| Upravljanje projektov in računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Ko se sprostitev zadrževanja prodajalca, ima objava kupona dodatne vrstice, ki niso pravilne. |
| Upravljanje projektov in računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Ko je integracijski dnevnik Project Operations objavljen, ne uspe zaradi manjkajočih dimenzij za račun, v katerem ni objavljen. |
| Upravljanje projektov in računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | The **Projekt** kartice ni mogoče urejati na čakajočem računu prodajalca, ko je artiklu dodeljena kategorija nabave. |
| Upravljanje projektov in računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Podokno za krmarjenje manjka, če niste prijavljeni v Project Operations Dataverse. |
| Upravljanje projektov in računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Ko knjižite prihodek iz računa projekta v primeru uporabljenega zadrževalnika, pride do težave, ker transakcije na kuponu niso uravnotežene. |
| Upravljanje projektov in računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Ustvarjanje ocene po objavi predloga računa blokira uvoz popravkov. |
| Upravljanje projektov in računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Sprememba v celoti zaračunanega zapisa mejnika ne bi smela biti mogoča. |
| Pot in stroški | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Vsa poročila o stroških so vidna, ko iščete kategorijo v mobilni aplikaciji Expense. |
| Pot in stroški | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepravilni zneski pri transakcijah prodajalcev in prometnih davkah so knjiženi iz odhodka, ki je ustvarjen s transakcijo s kreditno kartico. |
| Pot in stroški | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Ko osvežite datoteko, se prikaže nepomembno opozorilo **Poročilo o izdatkih** stran. |
| Pot in stroški | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Napačen vmesni odobritelj se uporabi, ko izbrišete vmesnega odobritelja in nato znova pošljete poročilo o stroških skozi potek dela. |
| Pot in stroški | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Pojavi se napaka pri objavljanju, ki je povezana z nastavitvijo prevoženih kilometrov. |
