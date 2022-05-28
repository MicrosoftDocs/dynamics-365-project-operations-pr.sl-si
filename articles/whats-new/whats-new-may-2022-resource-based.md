---
title: 'Novosti pri izdaji: Maj 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi'
description: Ta tema vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta maja 2022 Dynamics 365 Project Operations za scenarije, ki temeljijo na virih/brez zalog.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710168"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti pri izdaji: Maj 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta tema velja za naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektno delovanje v a Dataverse različica okolja 4.42.0.70
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance različica 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svoje operacije projekta Dataverse rešitev in različica rešitve Finance. Nekatere funkcije in zmožnosti morda ne bodo delovale pravilno, če najnovejša različica zemljevida ni aktivirana. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili izključen zemljevid tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu zemljevida naletite na težavo, sledite navodilom v [Težava z manjkajočimi stolpci tabele na zemljevidih](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) razdelek vodnika za odpravljanje težav z dvojnim pisanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti
### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje virov | 2634019 | Izboljšana sporočila o napakah za poslovna preverjanja pri dodajanju splošnih članov ekipe kot virov. |
| Načrtovanje in sledenje projektov | 2648515 | Omejene posodobitve za **lastnik**, **·**, in **stanje** v subjektih razporejanja. |
| Zaračunavanje in cene | 2653167 | The **Ocene** mrežni decimalni ločilo mora slediti nastavitvam formata v **Osebne možnosti**. |
| Zaračunavanje in cene| 2662251 | Vrednosti v **Popravljena enota** in **Skupina enot** privzeta polja pri ustvarjanju zapisov v predračunih materiala. |
| Zaračunavanje in cene| 2571408 | Neobračunane dejanske prodajne vrednosti so žigosane z ID-jem predračuna pri izdelavi osnutka računa. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vodenje projektov in računovodstvo v Dynamics 365 Finance

Za informacije o popravkih napak, ki so vključeni v to posodobitev, se prijavite na Microsoft Dynamics Storitve življenjskega cikla (LCS) in si oglejte [KB članek](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
