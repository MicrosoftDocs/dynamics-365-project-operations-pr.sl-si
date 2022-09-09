---
title: Novosti za avgust 2022 – storitev Project Operations za scenarije, ki temeljijo na virih/pomanjkanju zaloge
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta avgusta 2022 Dynamics 365 Project Operations za scenarije, ki temeljijo na virih/brez zaloge.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403877"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti za avgust 2022 – storitev Project Operations za scenarije, ki temeljijo na virih/pomanjkanju zaloge

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektne operacije v a Dataverse različica okolja 4.45.0.53
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance verzija 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svoje projektne operacije Dataverse rešitev in različica rešitve Finance. Nekatere funkcije in zmožnosti morda ne bodo delovale pravilno, če najnovejša različica zemljevida ni aktivirana. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljen zemljevid tabel, znova uveljavite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če naletite na težavo, ko zaženete zemljevid, sledite navodilom v [Težava z manjkajočimi stolpci tabele na zemljevidih](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) razdelek vodnika za odpravljanje težav z dvojnim pisanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje priložnosti | 2762089 | Obravnava napake med zapiranjem pogodbe kot izgubljene, če je samodejno shranjevanje onemogočeno v organizaciji.|
|Načrtovanje in sledenje projektov | 2767841 | Posodobitve telemetrije Projektna entiteta Ustvari ali posodobi scenarije.|
|Zaračunavanje in oblikovanje cen | 2771072 | Obravnava izjem ničelne reference med pridobivanjem ponudbe.|
|Zaračunavanje in oblikovanje cen | 2844181 |Napaka pri pridobivanju ID-ja korelacije in blokiranje ustvarjanja računa.|
|Zaračunavanje in oblikovanje cen | 2852836 | Dejanski podatki med podjetji manjkajo za stroške med podjetji, ustvarjeni in odobreni v CE.|


### <a name="project-management-and-accounting-in-finance"></a>Vodenje projektov in računovodstvo v Financah

Za informacije o popravkih napak, ki so vključeni v to posodobitev, se prijavite v Microsoft Dynamics Lifecycle Services (LCS) in si oglejte [Članek KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
