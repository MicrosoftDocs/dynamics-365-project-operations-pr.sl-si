---
title: Novosti v novembru 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta Dynamics 365 Project Operations novembra 2022 za scenarije, ki temeljijo na virih/nezaloženih.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831150"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti v novembru 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek velja za naslednje komponente in različice aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations v različici okolja 4.58.0.119. storitve Dataverse
- Upravljanje projektov in računovodstvo v okoljih aplikacije Dynamics 365 Finance različice 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

V tej izdaji ni posodobitev za preslikave dvojnega zapisovanja v aplikaciji Project Operations. Za trenutni seznam in različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations si oglejte [Različice preslikovanja dvojnega zapisovanja v aplikaciji Project Operations](../environment/resource-dual-write-maps.md).

Vedno, ko posodabljate različico rešitev Project Operations Dataverse in Finance, v svojem okolju zaženite najnovejšo verzijo preslikav in omogočite povezane preslikave tabel. Če ne aktivirate najnovejše različice preslikave, nekatere funkcije in zmogljivosti morda ne bodo delovale pravilno. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljeno preslikavo tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu preslikave naletite na težavo, upoštevajte navodila v razdelku [Težava z manjkajočimi stolpci tabele v preslikavah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) iz vodiča za odpravljanje težav z dvojnim zapisovanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Zaračunavanje in oblikovanje cen | 2781818 | Napaka ključa ni bilo mogoče najti pri privzeti ceni za dnevnik porabe materiala. |
| Zaračunavanje in oblikovanje cen | 2922373 | Vrstice s ponudbo ni mogoče povezati s projektom, ki je bil zaprt kot izgubljena ponudba. |
| Zaračunavanje in oblikovanje cen | 2943206 | **Polje** pogodbene vrstice v entiteti projekta bi moralo biti izbirno. |
| Zaračunavanje in oblikovanje cen | 2953182 | Izboljšajte sporočilo o napaki za popravke računov.|
| Zaračunavanje in oblikovanje cen | 2959500 | Vrstice s ponudbo ni mogoče povezati s projektno nalogo, ki je že povezana z izgubljeno ponudbo.|
| Zaračunavanje in oblikovanje cen | 2959560 | Sporočilo »Ta stranka je že vključena v projektno pogodbo«, prejeto med zapiranjem ponudbe, kot je zmagala v določenih območjih. |
| Zaračunavanje in oblikovanje cen | 3031727 | Dodelitve virov niso uspele z napako Zahtevano polje 'msdyn_Company' manjka. |
| Zaračunavanje in oblikovanje cen | 3036905 | Lastništvo podjetja ni nikoli inicializirano na ProjectTeamMember. |
| Upravljanje priložnosti | 2763519 | Napaka Null Reference v EnsureProjectContractAllowsUpdates. |
| Upravljanje priložnosti | 2783798 | Pri uvozu ocen projekta v vrstico ponudb manjkajo opisi nalog za ocene stroškov in materiala.|
| Upravljanje priložnosti | 2988635 | Izboljšajte opis sporočila o napaki pri brisanju stranke na Quote. |
| Upravljanje priložnosti | 3001191 | Ni mogoče ustvariti ponudbe iz Priložnosti, kjer je način obračunavanja naveden kot nič. |
| Nadgradnja | 3012324 | Pretvorba projekta ni uspela pri projektu s kontrolnimi znaki, kot je Tab, v imenu. || Načrtovanje in sledenje projektov | 2790384 | Časovna omejitev Pending OperationSet je prekratka. |
| Načrtovanje in sledenje projektov | 3044275 | Manjka lokalizacija za: missingProjectSchedulerErrorMessage. |
| Načrtovanje in sledenje projektov | 3044277 | Mreža Project Recon se ne naloži, ko razporejevalnik ni nastavljen.|
| Upravljanje virov | 2943153 | Posodobite zavihek Sledenje, da prikažete dve decimalni mesti za Trajanje.|
| Podizvajalske pogodbe | 2932774 | Napaka v vrstici računa dobavitelja samo za branje nepravilno vrže. |
| Podizvajalske pogodbe | 2939556 | Stanje glave računa dobavitelja ne sme biti nastavljeno na Spletno brisanje osnutka, če ni aktivno. |
| Čas in strošek | 2939998 | Prenesite novo različico TESA v ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Pregled upravljanja projektov in računovodstva v aplikaciji Finance

Za informacije o popravkih napak, vključenih v tej posodobitvi, se prijavite v storitev Microsoft Dynamics Lifecycle Services in si oglejte [Članek zbirke znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
