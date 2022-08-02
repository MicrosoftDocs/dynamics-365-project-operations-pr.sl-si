---
title: Novosti za junij 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta junija 2022 Dynamics 365 Project Operations za scenarije, ki temeljijo na virih/brez zaloge.
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

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektne operacije v a Dataverse okoljska različica 4.43.0.77 ali 4.43.0.119
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance verzija 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

Naslednja tabela prikazuje zemljevide z dvojnim pisanjem, ki so bili spremenjeni ali dodani v izdaji Project Operations junija 2022.

| Preslikava entitete | Posodobljena različica | Comments |
| --- | --- | --- |
| Entiteta za izvoz računa dobavitelja za projekt za integracijo aplikacije Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Zastarelo podedovano polje in preslikano v novo polje za sledenje stanja računa dobavitelja. |

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svoje projektne operacije Dataverse rešitev in različica rešitve Finance. Nekatere funkcije in zmožnosti morda ne bodo delovale pravilno, če najnovejša različica zemljevida ni aktivirana. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljen zemljevid tabel, znova uveljavite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če naletite na težavo, ko zaženete zemljevid, sledite navodilom v [Težava z manjkajočimi stolpci tabele na zemljevidih](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) razdelek vodnika za odpravljanje težav z dvojnim pisanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Podizvajanje | 2708885 | Odpravljeno je sporočilo o napaki, ki se prikaže, ko uporabnik ustvari zapis glave rezervacije vira, ki ga je mogoče rezervirati, kjer ni izpolnjen vir, ki ga je mogoče rezervirati. |
| Načrtovanje in sledenje projektov | 2629441 | Popravljena je bila logika sprožitve delovnega toka, da bi preprečili neskončno zanko, ko so projektne naloge posodobljene. |
| Čas in strošek | 2641209 | Uvozi časovnih vnosov iz dodelitev/rezervacij morajo ohraniti referenco vira, ki ga je mogoče rezervirati. |
| Načrtovanje in sledenje projektov | 2651148 | Glava projektnega dokumenta mora biti varovana.|
| Načrtovanje in sledenje projektov | 2653145 | Dodana preverjanja veljavnosti za zagotovitev, da ni mogoče ustvariti zapisa projekta, ki ima v imenu neveljavne znake. |
| Čas in strošek | 2654710 | Popravljeno filtriranje na **Odobritve** strani. |
| Zaračunavanje in cene | 2667805 | Dodana preverjanja veljavnosti za pomoč pri preprečevanju ustvarjanja zaračunanih dejanskih prodajnih vrednosti, če podporne nezaračunane dejanske prodajne vrednosti ne obstajajo. |
| Zaračunavanje in cene | 2668378 | Dodana preverjanja veljavnosti za pomoč pri preprečevanju dodajanja dimenzij cen po meri, razen če sta izpolnjena logično ime in ime polja. |
| Podizvajanje | 2677485 | Posodobljena ciljna različica zemljevida dvojnega pisanja vrstic računa dobavitelja. |
| Čas in strošek | 2700428 | Izboljšana je logika odobritev za zagotovitev, da je mogoče obdelati druge nize odobritev za projekt, tudi če je eden od nizov odobritev obtičal v sistemskih opravilih. |

### <a name="project-management-and-accounting-in-finance"></a>Vodenje projektov in računovodstvo v Financah

Za informacije o popravkih napak, ki so vključeni v to posodobitev, se prijavite v Microsoft Dynamics Lifecycle Services (LCS) in si oglejte [Članek KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
