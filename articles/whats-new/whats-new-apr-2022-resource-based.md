---
title: 'Novosti pri izdaji: April 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi'
description: Ta tema vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta aprila 2022 Dynamics 365 Project Operations za scenarije, ki temeljijo na virih/brez zalog.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613350"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti pri izdaji: April 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta tema velja za naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektno delovanje v a Dataverse različica okolja 4.41.0.45
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance različica 10.0.26

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

Kategorije nabave se lahko uporabljajo v projektnih naročilnicah in čakajočih računih prodajalcev. Za več informacij glejte [Uporabite kategorije nabave s projektnimi naročilnicami in čakajočimi računi prodajalcev](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

Naslednja tabela prikazuje zemljevide z dvojnim pisanjem, ki so bili spremenjeni ali dodani v izdaji Project Operations marca 2022.

| Preslikava entitete | Posodobljena različica | Comments |
| -------------- | ------------------- | ------------|
| Integracija projektnih operacij, izvozna entiteta vrstice računa prodajalca projekta msdyn\_ projektvendorinvoicelines | 1.0.0.4 | Ta zemljevid podpira uporabo kategorij nabave z naročili in čakajočimi računi prodajalcev. |

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svoje operacije projekta Dataverse rešitev in različica rešitve Finance. Nekatere funkcije in zmožnosti morda ne bodo delovale pravilno, če najnovejša različica zemljevida ni aktivirana. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili izključen zemljevid tabele, znova uporabite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če pri zagonu zemljevida naletite na težavo, sledite navodilom v [Težava z manjkajočimi stolpci tabele na zemljevidih](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) razdelek vodnika za odpravljanje težav z dvojnim pisanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| ------------ | ---------------- | -------------- |
| Čas in strošek | 2573900 | The **Sodobna odobritev** funkcija mora biti privzeto omogočena. |
| Zaračunavanje in cene | 2603313 | Odpravljena je napaka podvojenega zapisa, ki je preprečila dodajanje ponudbe in pogodbenih vrstic, ki vsebujejo izdelek. |
| Namestitev in konfiguracija | 2611368 | Stranke morajo imeti možnost dodati do pet entitet po meri v rešitev z uporabo sodobnega oblikovalca aplikacij. |
| Čas in strošek | 2628285 | Odpravljena je težava, ki je vplivala na zmožnost nastavitve pravilne kategorije vira med uvozom časovnega vnosa. |
| Upravljanje priložnosti| 2628815 | Posodobite omejitev znakov v podrobnem opisu vrstice narekovaja, da se ujema z omejitvijo znakov predmeta opravila, tako da bo uvoz uspešen za opravila, pri katerih je predmet daljši od 100 znakov. |
| Čas in strošek| 2629547 | The **Predložil** polje odobritev projektov mora kazati na uporabnika, ki je predložil zapis. |
| Čas in strošek| 2629865 | The **Kopiraj kategorijo** polje na nalogah, ko se projekti kopirajo. |
| Čas in strošek| 2636463 | Popravljeni filtri za odobritve v sodobnih obrazcih za odobritev. |
| Načrtovanje in sledenje projektov | 2648300 | Odpravljena je težava, ki preprečuje spremembo lastnika projekta. |
| Zaračunavanje in cene | 2563000 | Dnevniške vrstice za neobračunano prodajo, kjer se valuta razlikuje od pogodbene valute, ne smejo biti dovoljene. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vodenje projektov in računovodstvo v Dynamics 365 Finance

Za informacije o popravkih napak, ki so vključeni v to posodobitev, se prijavite na Microsoft Dynamics Storitve življenjskega cikla (LCS) in si oglejte [KB članek](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
