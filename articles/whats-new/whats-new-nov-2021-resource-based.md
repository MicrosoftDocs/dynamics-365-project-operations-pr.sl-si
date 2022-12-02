---
title: Novosti v novembru 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v novembrski izdaji (2021) aplikacije Project Operations za primere uporabe z viri/brez zalog.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932914"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti v novembru 2021 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

*Velja za: scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi*

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155 storitve Dataverse
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.22

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

V to izdajo so vključene naslednje funkcije:

- Vmesniki za programiranje aplikacij (API) za razporejanje projektov zdaj podpirajo možnost ustvarjanja in brisanja veder projekta.

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-in-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Zaračunavanje in oblikovanje cen | 2240080 | Polje **Plačilni pogoji** se ne sme podvajati na predračunu. |
| Zaračunavanje in oblikovanje cen | 2358236 | Popravek računa mora omogočati popravke, ki imajo vrstice z ničelno ceno. |
| Upravljanje virov | 2410072 | Omogočena nastavitev za vir, ki je dodeljen projektnemu opravilu kot vodja projekta. |
| Zaračunavanje in oblikovanje cen | 2430234 | Odpravljena težava z izračunom stroškovne učinkovitosti. |
| Čas in strošek | 2436978 | Omogočena možnost, da se čas vnese v obliki zapisa hh:mm. |
| Zaračunavanje in oblikovanje cen | 2448623 | Omogoča posodobitev cenikov, ko so povezani z organizacijsko enoto. |
| Čas in strošek | 2460396 | Omogoča brisanje časovnega cenika s čiščenjem celice. |
| Zaračunavanje in oblikovanje cen | 2467386 | Omogoča brisanje opravila projekta, tudi če je opravilo povezano s pridobljeno ponudbo. |
| Čas in strošek | 2461744 | Pogled **Moja neuspešna odobritev** vsebuje samo odobritve projektov s stanjem **Poslano**. |
| Čas in strošek | 2464082 | Odstranjena povezava med odobritvami projekta in nizom odobritev, ko se ciljno stanje ujema. |
| Čas in strošek | 2468108 | Posel načrtovanja ne sme nastaviti stanja **V obdelavi** za nabor odobritev. |
| Čas in strošek | 2471503 | Brisanje nizov odobritev, starih sedem dni. |
| Zaračunavanje in oblikovanje cen | 2480687 | Sklic vrstice ponudbe ne sme biti odstranjen, ko je ustvarjen mejnik vrstice ponudbe. |

### <a name="project-management-and-accounting-in-finance"></a>Pregled upravljanja projektov in računovodstva v aplikaciji Finance

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje projektov in računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Zadržani zneski dobavitelja v transakcijah stroškov projekta niso prikazani na seznamu transakcij. |
| Upravljanje projektov in računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Medpodjetni računi dobavitelji so poškodovani, ko je vklopljena integracija računa dobavitelja. |
| Upravljanje projektov in računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Plačilni pogoji na računih projekta ne delujejo po pričakovanjih. |
| Upravljanje projektov in računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Ko je zadrževanje dobavitelja sproščeno, ima knjiženje kupona nepravilne dodatne vrstice. |
| Upravljanje projektov in računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Ko je dnevnik integracije aplikacije Project Operations knjižen, ne uspe, ker računu manjkajo razsežnosti računa, za katerega se ne knjiži. |
| Upravljanje projektov in računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Zavihka **Projekt** ni mogoče urejati na čakajočem računu dobavitelja, ko je kategorija nabave dodeljena elementu. |
| Upravljanje projektov in računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Podokno za krmarjenje manjka, če niste prijavljeni v aplikacijo Project Operations Dataverse. |
| Upravljanje projektov in računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Ko knjižite prihodek z računa dobavitelja v primeru uporabljenega zadržanja, pride do težave, ker stanja transakcij kuponov niso pravilna. |
| Upravljanje projektov in računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Ustvarjanje ocene po knjiženju predloga računa blokira uvoz vrstic popravkov. |
| Upravljanje projektov in računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Spreminjanje popolnoma zaračunanega zapisa mejnika ne bi smelo biti mogoče. |
| Pot in stroški | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Vsa poročila o stroških lahko vidite, ko poiščete kategorijo v mobilni aplikaciji za upravljanje stroškov. |
| Pot in stroški | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nepravilni zneski za transakcije dobavitelja in prometnega davka, ki so knjiženi iz stroška, ki je ustvarjen iz transakcije kreditne kartice. |
| Pot in stroški | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Ko osvežite stran **Poročilo o stroških**, se prikaže nepomembno opozorilo. |
| Pot in stroški | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Napačen vmesni odobritelj se uporabi, ko izbrišete vmesnega odobritelja in nato znova predložite poročilo o stroških skozi potek dela. |
| Pot in stroški | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Pri knjiženju pride do napake, povezane z nastavitvijo prevožene razdalje. |
