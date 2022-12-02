---
title: Novosti za junij 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so bile na voljo v izdaji aplikacije Microsoft Dynamics 365 Project Operations junija 2022 za scenarije, ki temeljijo na virih/nezalogi.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031351"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti za junij 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v okolju Dataverse različice 4.43.0.77 ali 4.43.0.119
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V naslednji tabeli so prikazane preslikave za dvojno zapisovanje, ki so spremenjene ali dodane v izdaji različice Project Operations iz junija 2022.

| Preslikava entitete | Posodobljena različica | Comments |
| --- | --- | --- |
| Entiteta za izvoz računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Opuščeno podedovano polje in preslikano v novo polje za sledenje stanja računa dobavitelja. |

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Podizvajalske pogodbe | 2708885 | Odpravljeno je sporočilo o napaki, ki se prikaže, ko uporabnik ustvari zapis glave za rezervacijo vira, ki ga je mogoče rezervirati, kjer ta ni izpolnjen. |
| Načrtovanje in sledenje projektov | 2629441 | Popravljena logika sprožitve delovnega toka, da bi preprečili neskončno zanko, ko so opravila projekta posodobljena. |
| Čas in strošek | 2641209 | Uvozi časovnih vnosov iz dodelitev/rezervacij morajo ohraniti sklic vira, ki ga je mogoče rezervirati. |
| Načrtovanje in sledenje projektov | 2651148 | Glava dokumenta projekta mora biti varovana.|
| Načrtovanje in sledenje projektov | 2653145 | Dodana preverjanja veljavnosti za preprečevanje ustvarjanja zapisa projekta, ki ima v imenu neveljavne znake. |
| Čas in strošek | 2654710 | Popravljeno filtriranje na strani **Odobritve**. |
| Zaračunavanje in cene | 2667805 | Dodana preverjanja veljavnosti za pomoč pri preprečevanju ustvarjanja obračunanih dejanskih prodajnih vrednosti, če podporne neobračunane dejanske prodajne vrednosti ne obstajajo. |
| Zaračunavanje in cene | 2668378 | Dodana preverjanja veljavnosti za pomoč pri preprečevanju dodajanja razsežnosti cen po meri, razen če sta izpolnjena logično ime in ime polja. |
| Podizvajalske pogodbe | 2677485 | Posodobljena ciljna različica preslikave dvojnega zapisovanja vrstic računa dobavitelja. |
| Čas in strošek | 2700428 | Izboljšana logika odobritev za zagotavljanje obdelave drugih nizov odobritev za projekt, tudi če je eden od nizov odobritev obtičal v sistemskih poslih. |

### <a name="project-management-and-accounting-in-finance"></a>Pregled upravljanja projektov in računovodstva v aplikaciji Finance

Za informacije o popravkih napak, vključenih v tej posodobitvi, se prijavite v storitev Microsoft Dynamics Lifecycle Services (LCS) in si oglejte [Članek zbirke znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
