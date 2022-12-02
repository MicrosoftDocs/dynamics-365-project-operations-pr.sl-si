---
title: Ocene prodaje in projekti
description: Ta članek vsebuje informacije o tem, kako izkoristite razpored in ocene v prodajnem procesu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 957c2337cce3b3bf65a0bfef7c1aee6a730971fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925416"
---
# <a name="sales-estimates-and-projects"></a>Ocene prodaje in projekti

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Med prodajnim procesom lahko ustvarite ocene prodaje tako, da povežete projekt s prodajno ponudbo. Na ta način lahko pride do deterministične ocene med prodajnim postopkom in se izkoristijo možnosti razporejanja in ocenjevanja za projekt. Če prodaja uspe, se lahko razpored, ki je bil uporabljen za namene ocenjevanja prodaje, uporabi kot osnova za nadaljnjo izpopolnitev načrta projekta.

## <a name="linking-a-project-to-a-quote-line"></a>Povezovanje projekta z vrstico ponudbe

Ko ustvarite vrstico ponudbe, ki temelji na projektu, lahko ustvarite nov projekt ali povežete obstoječi projekt na strani **Vrstica ponudbe**. 

> ![Obrazec »Vrstica ponudbe«.](media/project-8.png)
 
Ko ustvarite nov projekt iz podrobnosti vrstice ponudbe, lahko izkoristite predloge projekta. Projektne predloge so vzorčni projekti, ki predstavljajo standardne načrte projektov in tipične finančne ocene v organizaciji. Predstavljajo lahko tudi kopije projektnih načrtov in ocen iz preteklih projektov.

> ![Podrobnosti vrstice ponudb.](media/project-9.png)
  
Če ustvarite projekt iz ponudbe, je ta projekt samodejno povezan z vrstico ponudbe.

## <a name="components-of-estimates-in-a-project"></a>Komponente ocen v projektu

Z razporedom lahko razdelite delo v opravila, ohranite hierarhijo opravil, ugotovite, kateri viri so potrebni za dokončanje opravila, in dodelite oceno obsega dela, potrebnega za dokončanje opravila.

Ocene obsega dela in razporeda lahko določite z uporabo polj na zavihku **Načrtovanje** na strani **Projekt**. Ker je cenik povezan s projektom, se finančne ocene izračunajo na osnovi stroškov in prodajnih cen, ki so določene v ceniku.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Uvažanje ocen iz projekta v ponudbo

Ko določite ocene projekta, jih lahko uvozite v vrstico ponudbe. Na strani **Podrobnosti vrstice ponudbe** na traku izberite **Uvozi iz ocen**, da povzamete ocene projektov po vrsti transakcije, vlogi ali ravni opravila.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
