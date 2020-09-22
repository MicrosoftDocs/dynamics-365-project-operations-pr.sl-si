---
title: Zagotavljanje ocen dela za projekt v času prodajnega postopka
description: Kako zagotavljati ocene dela za projekt v času prodajnega postopka v rešitvi Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755853"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="58559-103">Zagotavljanje ocen dela za projekt v času prodajnega postopka (Project Service)</span><span class="sxs-lookup"><span data-stu-id="58559-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="58559-104">V času prodajnega postopka lahko ocene prodaje izdelate od začetka z vrsticami ponudbe.</span><span class="sxs-lookup"><span data-stu-id="58559-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="58559-105">Zmožnosti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v programu [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] omogočajo bolj znanstven in determinističen način za ustvarjanje ocen prodaje tako, da se razčlenijo delovni nalogi in povežejo ustrezni atributi, ki pripomorejo k oceni projekta v strukturirani členitvi dela.</span><span class="sxs-lookup"><span data-stu-id="58559-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="58559-106">Ko posel sklenete, lahko povezano strukturirano členitev dela uporabite v načrtu projekta ter jo po potrebi dodelate za uspešen zaključek svojega projekta.</span><span class="sxs-lookup"><span data-stu-id="58559-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="58559-107">Povezovanje projekta z vrstico ponudbe</span><span class="sxs-lookup"><span data-stu-id="58559-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="58559-108">Če ustvarjate vrstico ponudbe, ki temelji na projektu, lahko ustvarite nov projekt iz te vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="58559-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="58559-109">Uporabite lahko predloge za projekte, ki so predhodno konfigurirani načrti za standardne projekte in finančne ocene, skupne vaši organizaciji, ali kopija načrta projekta in ocene predhodnega projekta.</span><span class="sxs-lookup"><span data-stu-id="58559-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="58559-110">Ko ustvarite projekt, izbira predloge projekta omogoča osnovo za dodelavo načrta projekta, ocen in zahtev za vlogo.</span><span class="sxs-lookup"><span data-stu-id="58559-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="58559-111">Če iz ponudbe ustvarite svoj projekt, je ta projekt samodejno povezan z vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="58559-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="58559-112">Komponente ocene projekta</span><span class="sxs-lookup"><span data-stu-id="58559-112">Project estimate components</span></span>  
 <span data-ttu-id="58559-113">Strukturirana členitev dela v projektu omogoča način razčlenjevanja dela na opravila, ohranjanje hierarhije opravil in dodeljevanje ocene truda, ki je potrebno za dokončanje posameznega opravila.</span><span class="sxs-lookup"><span data-stu-id="58559-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="58559-114">Vloge lahko opravilu dodelite tudi zato, da določite oceno vrste vira, ki se zahteva za dokončanje opravila in razporeda.</span><span class="sxs-lookup"><span data-stu-id="58559-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="58559-115">Strukturirana členitev dela pomaga pri določanju ocen za trud pri delu in razpored.</span><span class="sxs-lookup"><span data-stu-id="58559-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="58559-116">Privzeto projekt uporablja privzete cenike, ki jih predhodno določite.</span><span class="sxs-lookup"><span data-stu-id="58559-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="58559-117">Stroški in prodajne cene, določeni v ceniku, pomagajo določiti finančne ocene za členitev dela za projekt.</span><span class="sxs-lookup"><span data-stu-id="58559-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="58559-118">Če je vaš projekt povezan s ponudbo in ima ponudba drugačen cenik od privzetega, se za finančne ocene uporabi cenik ponudbe.</span><span class="sxs-lookup"><span data-stu-id="58559-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="58559-119">Uvoz ocen iz projekta v ponudbo</span><span class="sxs-lookup"><span data-stu-id="58559-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="58559-120">Ko so ocene projekta v projektu, lahko te ocene uvozite v vrstico ponudbe:</span><span class="sxs-lookup"><span data-stu-id="58559-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="58559-121">V možnosti **Podrobnosti vrstice ponudbe** kliknite **Uvoz iz ocen**.</span><span class="sxs-lookup"><span data-stu-id="58559-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="58559-122">Izberite, ali želite uvoziti ocene projekta, ki jih povzema vrsta transakcije, vloga ali raven vozlišča strukturirane členitve dela.</span><span class="sxs-lookup"><span data-stu-id="58559-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="58559-123">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="58559-123">See Also</span></span>  
 [<span data-ttu-id="58559-124">Priročnik za vodje projektov</span><span class="sxs-lookup"><span data-stu-id="58559-124">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
