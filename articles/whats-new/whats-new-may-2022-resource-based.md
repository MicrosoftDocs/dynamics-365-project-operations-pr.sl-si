---
title: 'Novosti pri izdaji: Maj 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi'
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so bile na voljo v izdaji aplikacije Microsoft Dynamics 365 Project Operations maja 2022 za scenarije, ki temeljijo na virih/nezalogi.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921414"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti pri izdaji: Maj 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.42.0.70. storitve Dataverse
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti
### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje virov | 2634019 | Izboljšana sporočila o napaki za poslovna preverjanja veljavnosti pri dodajanju splošnih članov ekipe kot virov. |
| Načrtovanje in sledenje projektov | 2648515 | Omejene posodobitve za vrednosti **idlastnika**, **stanje** in **status** v entitetah razporejanja. |
| Zaračunavanje in cene | 2653167 | Decimalno ločilo v mreži **Ocene** mora slediti nastavitvam oblike v razdelku **Osebne možnosti**. |
| Zaračunavanje in cene| 2662251 | Vrednosti v poljih **Popravljena enota** in **Skupina enot** so privzeto pridobljene pri ustvarjanju zapisov v ocenah materiala. |
| Zaračunavanje in cene| 2571408 | Neobračunane dejanske vrednosti prodaje so pri ustvarjanju osnutka računa označene z ID-jem predračuna. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektov in računovodstvo v okoljih aplikacij Dynamics 365 Finance

Za informacije o popravkih napak, vključenih v tej posodobitvi, se prijavite v storitev Microsoft Dynamics Lifecycle Services (LCS) in si oglejte [Članek zbirke znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
