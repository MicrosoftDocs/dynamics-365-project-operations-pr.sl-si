---
title: Spremljanje stanja projekta
description: Spremljanje stanja projekta v rešitvi Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d57f33cdf240db4cae1f33fe962173790fe0fe7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281948"
---
# <a name="track-a-projects-status-project-service"></a>Spremljajte stanje projekta (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Z [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] sledite napredku strankinega projekta.  

Ko dejavnost napreduje, se stanje projekta posodablja, da prikazuje stanje dejavnosti:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Nov**    | Ko ustvarite projekt, je stanje nastavljeno na **Novo**. Če ste ustvarili projekt iz predloge, ima na tej stopnji projekt morda urnik, ocene in podatke o ekipi. V nasprotnem primeru je na voljo osnutek projekta in morate preostale komponente projekta vnesti ročno. |
|  **Ponudba**   |      Ko povežete projekt s ponudbo ali ga ustvarite iz ponudbe, je stopnja projekta nastavljena na **Ponudba**, pri čemer se posodobita tudi ocenjeni začetek in konec projekta. Ko je projekt v stanju ponudbe, so podrobnosti o ponudbi prikazane na zavihku **Prodaja** na strani **Projekt**.      |
|   **Načrt**   |                                     Ko je ponudba, povezana s projektom, sprejeta, in ko se dejavnost premakne v stanje pogodbe, se stanje projekta posodobi v **Načrt**. Podrobnosti pogodbe so prikazane na zavihku **Prodaja** na strani **Projekt**.                                      |
| **Dokončaj** |                    Ko je delo na projektu končano, lahko stanje preklopite v **Zaključeno**. Ko je projekt zaključen, to pomeni, da je delo v celoti opravljeno, vseeno pa je projekt odprt zaradi čakajočih vnosov, povezanih s časom ali stroški.                     |
|  **Zapri**   |           Ko so vse transakcije, povezane s projektom zabeležene in ne pričakujete nobenih novih, lahko stanje ročno preklopite v **Zaprto**. Ko je projekt nastavljen na **Zaprto**, vanj ni več mogoče zapisovati transakcij, saj je projekt dostopen samo za branje.           |

## <a name="to-track-a-projects-status"></a>Spremljanje stanja projekta  

1.  Pojdite na **Project Service > Projekti**.  

2.  Kliknite projekt, s katerim se želite ukvarjati.  

3.  V vrstici na zgornjem delu zaslona izberite puščico dol poleg imena projekta, nato kliknite **Spremljanje projekta**.  

4.  V spustnem meniju nad seznamom opravil izberite **Spremljanje obsega dela** ali **Spremljanje stroškov**.  

5.  Če želite urediti opravilo, ga kliknite. Lahko tudi premikate stolpce v Ganttovem grafikonu ali spreminjate njihovo velikost, ter tako spremenite čas in napredek opravila.  

### <a name="see-also"></a>Glejte tudi  
 [Priročnik za vodje projektov](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]