---
title: Novosti za avgust 2022 – storitev Project Operations za scenarije, ki temeljijo na virih/pomanjkanju zaloge
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so bile na voljo v izdaji aplikacije Microsoft Dynamics 365 Project Operations avgusta 2022 za scenarije, ki temeljijo na virih/nezalogi.
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

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.45.0.53. storitve Dataverse
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Upravljanje priložnosti | 2762089 | Obravnava napake kot izgubljene med zapiranjem pogodbe, če je v organizaciji onemogočeno samodejno shranjevanje.|
|Načrtovanje in sledenje projektov | 2767841 | Posodobitve telemetrije projektne entitete ustvarijo ali posodobijo scenarije.|
|Zaračunavanje in oblikovanje cen | 2771072 | Obravnava izjeme sklica z vrednostjo »null« med pridobivanjem ponudbe.|
|Zaračunavanje in oblikovanje cen | 2844181 |Napaka pri pridobivanju ID-ja korelacije in blokiranje ustvarjanja računa.|
|Zaračunavanje in oblikovanje cen | 2852836 | Za medpodjetne stroške manjkajo dejanske medpodjetne vrednosti, ki so bile ustvarjene in odobrene v CE.|


### <a name="project-management-and-accounting-in-finance"></a>Pregled upravljanja projektov in računovodstva v aplikaciji Finance

Za informacije o popravkih napak, vključenih v tej posodobitvi, se prijavite v storitev Microsoft Dynamics Lifecycle Services (LCS) in si oglejte [Članek zbirke znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
