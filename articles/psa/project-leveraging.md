---
title: Ocene prodaje in projekti
description: Ta tema vsebuje informacije o tem, kako izkoristite razpored in ocene v prodajnem procesu.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 87dc72b76ec4f88684ef2c702718e1ab631ff936
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283928"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="c97c2-103">Ocene prodaje in projekti</span><span class="sxs-lookup"><span data-stu-id="c97c2-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c97c2-104">Med prodajnim procesom lahko ustvarite ocene prodaje tako, da povežete projekt s prodajno ponudbo.</span><span class="sxs-lookup"><span data-stu-id="c97c2-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="c97c2-105">Na ta način lahko pride do deterministične ocene med prodajnim postopkom in se izkoristijo možnosti razporejanja in ocenjevanja za projekt.</span><span class="sxs-lookup"><span data-stu-id="c97c2-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="c97c2-106">Če prodaja uspe, se lahko razpored, ki je bil uporabljen za namene ocenjevanja prodaje, uporabi kot osnova za nadaljnjo izpopolnitev načrta projekta.</span><span class="sxs-lookup"><span data-stu-id="c97c2-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="c97c2-107">Povezovanje projekta z vrstico ponudbe</span><span class="sxs-lookup"><span data-stu-id="c97c2-107">Linking a project to a quote line</span></span>

<span data-ttu-id="c97c2-108">Ko ustvarite vrstico ponudbe, ki temelji na projektu, lahko ustvarite nov projekt ali povežete obstoječi projekt na strani **Vrstica ponudbe**.</span><span class="sxs-lookup"><span data-stu-id="c97c2-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Obrazec »Vrstica ponudbe«](media/project-8.png)
 
<span data-ttu-id="c97c2-110">Ko ustvarite nov projekt iz podrobnosti vrstice ponudbe, lahko izkoristite predloge projekta.</span><span class="sxs-lookup"><span data-stu-id="c97c2-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="c97c2-111">Projektne predloge so vzorčni projekti, ki predstavljajo standardne načrte projektov in tipične finančne ocene v organizaciji.</span><span class="sxs-lookup"><span data-stu-id="c97c2-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="c97c2-112">Predstavljajo lahko tudi kopije projektnih načrtov in ocen iz preteklih projektov.</span><span class="sxs-lookup"><span data-stu-id="c97c2-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Podrobnosti vrstice ponudb](media/project-9.png)
  
<span data-ttu-id="c97c2-114">Če ustvarite projekt iz ponudbe, je ta projekt samodejno povezan z vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="c97c2-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="c97c2-115">Komponente ocen v projektu</span><span class="sxs-lookup"><span data-stu-id="c97c2-115">Components of estimates in a project</span></span>

<span data-ttu-id="c97c2-116">Z razporedom lahko razdelite delo v opravila, ohranite hierarhijo opravil, ugotovite, kateri viri so potrebni za dokončanje opravila, in dodelite oceno obsega dela, potrebnega za dokončanje opravila.</span><span class="sxs-lookup"><span data-stu-id="c97c2-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="c97c2-117">Ocene obsega dela in razporeda lahko določite z uporabo polj na zavihku **Načrtovanje** na strani **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="c97c2-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="c97c2-118">Ker je cenik povezan s projektom, se finančne ocene izračunajo na osnovi stroškov in prodajnih cen, ki so določene v ceniku.</span><span class="sxs-lookup"><span data-stu-id="c97c2-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="c97c2-119">Uvažanje ocen iz projekta v ponudbo</span><span class="sxs-lookup"><span data-stu-id="c97c2-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="c97c2-120">Ko določite ocene projekta, jih lahko uvozite v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="c97c2-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="c97c2-121">Na strani **Podrobnosti vrstice ponudbe** na traku izberite **Uvozi iz ocen**, da povzamete ocene projektov po vrsti transakcije, vlogi ali ravni opravila.</span><span class="sxs-lookup"><span data-stu-id="c97c2-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]