---
title: Novosti za junij 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta junija 2022 Dynamics 365 Project Operations za scenarije, ki temeljijo na virih/brez zalog.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959724"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti za junij 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektno delovanje v a Dataverse različica okolja 4.43.0.77
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance različica 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

Naslednja tabela prikazuje zemljevide z dvojnim pisanjem, ki so bili spremenjeni ali dodani v izdaji Project Operations junija 2022.

| Preslikava entitete | Posodobljena različica | Comments |
| --- | --- | --- |
| Entiteta za izvoz računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Zastarelo polje je bilo opuščeno in preslikano v novo polje za sledenje stanju računov prodajalca. |

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svoje operacije projekta Dataverse rešitev in različica rešitve Finance. Nekatere funkcije in zmožnosti morda ne bodo delovale pravilno, če najnovejša različica zemljevida ni aktivirana. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili izključen zemljevid tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu zemljevida naletite na težavo, sledite navodilom v [Težava z manjkajočimi stolpci tabele na zemljevidih](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) razdelek vodnika za odpravljanje težav z dvojnim pisanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Podizvajalci | 2708885 | Popravljeno sporočilo o napaki, ki se prikaže, ko uporabnik ustvari zapis glave za rezervacijo vira, ki ga je mogoče rezervirati, kjer ni izpolnjen noben vir, ki ga je mogoče rezervirati. |
| Načrtovanje in sledenje projektov | 2629441 | Popravljena logika sprožitve delovnega toka, da bi preprečili neskončno zanko pri posodabljanju projektnih nalog. |
| Čas in strošek | 2641209 | Uvozi časovnega vnosa iz nalog/rezervacije morajo ohraniti referenco vira, ki jo je mogoče rezervirati. |
| Načrtovanje in sledenje projektov | 2651148 | Glava projektnega dokumenta mora biti varovana.|
| Načrtovanje in sledenje projektov | 2653145 | Dodane potrditve za zagotovitev, da ni mogoče ustvariti zapisa projekta, ki ima v imenu neveljavne znake. |
| Čas in strošek | 2654710 | Popravljeno filtriranje na **Odobritve** stran. |
| Zaračunavanje in cene | 2667805 | Dodane potrditve, ki pomagajo preprečiti ustvarjanje zaračunanih dejanskih prodaj, če ne obstajajo podprte dejanske neobračunane prodaje. |
| Zaračunavanje in cene | 2668378 | Dodane potrditve za preprečevanje dodajanja razsežnosti cen po meri, razen če sta izpolnjena logično ime in ime polja. |
| Podizvajalci | 2677485 | Posodobljena ciljna različica zemljevida dvojnega pisanja vrstic računov prodajalca. |
| Čas in strošek | 2700428 | Izboljšana logika odobritev, da se zagotovi, da se lahko drugi nizi odobritev za projekt obdelajo, tudi če je eden od nizov odobritev obtičal v sistemskih opravilih. |

### <a name="project-management-and-accounting-in-finance"></a>Vodenje projektov in računovodstvo v financah

Za informacije o popravkih napak, ki so vključeni v to posodobitev, se prijavite na Microsoft Dynamics Storitve življenjskega cikla (LCS) in si oglejte [KB članek](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
