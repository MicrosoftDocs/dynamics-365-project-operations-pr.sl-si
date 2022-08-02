---
title: 'Novosti pri izdaji: April 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi'
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta aprila 2022 Dynamics 365 Project Operations za scenarije, ki temeljijo na virih/brez zaloge.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110904"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti pri izdaji: April 2022 – Project Operations za scenarije, ki temeljijo na virih/nezalogi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektne operacije v a Dataverse različica okolja 4.41.0.45
- Vodenje projektov in računovodstvo v okolju Dynamics 365 Finance verzija 10.0.26

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

Kategorije javnih naročil lahko uporabite v projektnih naročilnicah in čakajočih računih dobaviteljev. Za več informacij glejte [Uporabite kategorije javnih naročil z naročili za projekt in čakajočimi računi dobavitelja](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Posodobitve preslikave za dvojno zapisovanje za Project Operations

Naslednja tabela prikazuje zemljevide z dvojnim pisanjem, ki so bili spremenjeni ali dodani v izdaji Project Operations marca 2022.

| Preslikava entitete | Posodobljena različica | Comments |
| -------------- | ------------------- | ------------|
| Izvoz entitete msdyn za integracijo projektnih operacij dobavitelja vrstice računa\_ projectvendorinvoicelines | 1.0.0.4 | Ta zemljevid podpira uporabo kategorij javnih naročil z naročili in čakajočimi računi dobavitelja. |

Vedno zaženite najnovejšo različico zemljevida v svojem okolju in omogočite vse povezane zemljevide tabel, ko posodabljate svoje projektne operacije Dataverse rešitev in različica rešitve Finance. Nekatere funkcije in zmožnosti morda ne bodo delovale pravilno, če najnovejša različica zemljevida ni aktivirana. Aktivno različico preslikave si lahko ogledate v stolpcu **Različica** na strani **Dvojno zapisovanje**. Če želite aktivirati novo različico preslikave, izberite možnost **Različice preslikave tabele**, izberite najnovejšo različico in nato shranite izbrano različico. Če ste prilagodili vnaprej pripravljen zemljevid tabel, znova uveljavite spremembe. Za več informacij glejte [Upravljanje življenjskega cikla aplikacij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Če naletite na težavo, ko zaženete zemljevid, sledite navodilom v [Težava z manjkajočimi stolpci tabele na zemljevidih](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) razdelek vodnika za odpravljanje težav z dvojnim pisanjem.

## <a name="quality-updates"></a>Posodobitve kakovosti

### <a name="project-operations-on-dataverse"></a>Project Operations v okolju Dataverse

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| ------------ | ---------------- | -------------- |
| Čas in strošek | 2573900 | The **Sodobna odobritev** funkcija mora biti privzeto omogočena. |
| Zaračunavanje in cene | 2603313 | Odpravljena je napaka podvojenega zapisa, ki je preprečevala dodajanje ponudb in vrstic pogodbe, ki imajo izdelek. |
| Uvajanje in konfiguracija | 2611368 | Stranke morajo imeti možnost, da z uporabo sodobnega oblikovalca aplikacij v rešitev dodajo do pet entitet po meri. |
| Čas in strošek | 2628285 | Odpravljena je težava, ki je vplivala na možnost nastavitve pravilne kategorije vira med uvozom časovnega vnosa. |
| Upravljanje priložnosti| 2628815 | Posodobite omejitev znakov v opisu podrobnosti vrstice narekovajev, da se bo ujemala z omejitvijo znakov predmeta opravila, tako da bo uvoz uspel za opravila, kjer je predmet daljši od 100 znakov. |
| Čas in strošek| 2629547 | The **Poslal avtor** polje soglasij projekta mora kazati na uporabnika, ki je oddal zapis. |
| Čas in strošek| 2629865 | The **Kopiraj kategorijo** polje pri opravilih, ko so projekti kopirani. |
| Čas in strošek| 2636463 | Popravljeni filtri na odobritvah v sodobnih obrazcih odobritev. |
| Načrtovanje in sledenje projektov | 2648300 | Odpravljena je težava, ki preprečuje spremembo lastnika projekta. |
| Zaračunavanje in cene | 2563000 | Vrstice dnevnika za nezaračunano prodajo, kjer se valuta razlikuje od pogodbene valute, ne smejo biti dovoljene. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vodenje projektov in računovodstvo v Dynamics 365 Finance

Za informacije o popravkih napak, ki so vključeni v to posodobitev, se prijavite v Microsoft Dynamics Lifecycle Services (LCS) in si oglejte [Članek KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
