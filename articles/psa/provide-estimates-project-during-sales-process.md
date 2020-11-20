---
title: Zagotavljanje ocen dela za projekt v času prodajnega postopka
description: Kako zagotavljati ocene dela za projekt v času prodajnega postopka v rešitvi Project Service
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
ms.openlocfilehash: 7bd83b6872d437f1d074d6ea2336c751bdfdd9e6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120608"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Zagotavljanje ocen dela za projekt v času prodajnega postopka (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

V času prodajnega postopka lahko ocene prodaje izdelate od začetka z vrsticami ponudbe. Zmožnosti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v programu [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] omogočajo bolj znanstven in determinističen način za ustvarjanje ocen prodaje tako, da se razčlenijo delovni nalogi in povežejo ustrezni atributi, ki pripomorejo k oceni projekta v strukturirani členitvi dela.  
  
 Ko posel sklenete, lahko povezano strukturirano členitev dela uporabite v načrtu projekta ter jo po potrebi dodelate za uspešen zaključek svojega projekta.  
  
## <a name="link-a-project-to-a-quote-line"></a>Povezovanje projekta z vrstico ponudbe  
 Če ustvarjate vrstico ponudbe, ki temelji na projektu, lahko ustvarite nov projekt iz te vrstice ponudbe. Uporabite lahko predloge za projekte, ki so predhodno konfigurirani načrti za standardne projekte in finančne ocene, skupne vaši organizaciji, ali kopija načrta projekta in ocene predhodnega projekta. Ko ustvarite projekt, izbira predloge projekta omogoča osnovo za dodelavo načrta projekta, ocen in zahtev za vlogo. Če iz ponudbe ustvarite svoj projekt, je ta projekt samodejno povezan z vrstico ponudbe.  
  
## <a name="project-estimate-components"></a>Komponente ocene projekta  
 Strukturirana členitev dela v projektu omogoča način razčlenjevanja dela na opravila, ohranjanje hierarhije opravil in dodeljevanje ocene truda, ki je potrebno za dokončanje posameznega opravila. Vloge lahko opravilu dodelite tudi zato, da določite oceno vrste vira, ki se zahteva za dokončanje opravila in razporeda.  
  
 Strukturirana členitev dela pomaga pri določanju ocen za trud pri delu in razpored. Privzeto projekt uporablja privzete cenike, ki jih predhodno določite. Stroški in prodajne cene, določeni v ceniku, pomagajo določiti finančne ocene za členitev dela za projekt.  
  
 Če je vaš projekt povezan s ponudbo in ima ponudba drugačen cenik od privzetega, se za finančne ocene uporabi cenik ponudbe.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Uvoz ocen iz projekta v ponudbo  
 Ko so ocene projekta v projektu, lahko te ocene uvozite v vrstico ponudbe:  
  
-   V možnosti **Podrobnosti vrstice ponudbe** kliknite **Uvoz iz ocen**. 

-   Izberite, ali želite uvoziti ocene projekta, ki jih povzema vrsta transakcije, vloga ali raven vozlišča strukturirane členitve dela.  
  
### <a name="see-also"></a>Glejte tudi  
 [Priročnik za vodje projektov](../psa/project-manager-guide.md)
