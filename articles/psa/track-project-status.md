---
title: Spremljanje stanja projekta
description: Spremljanje stanja projekta v rešitvi Project Service
author: ruhercul
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
ms.openlocfilehash: 2385f7e52f3b5051b76daa9169f98bd73487e22d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014406"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="f0aff-103">Spremljajte stanje projekta (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f0aff-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f0aff-104">Z [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] sledite napredku strankinega projekta.</span><span class="sxs-lookup"><span data-stu-id="f0aff-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="f0aff-105">Ko dejavnost napreduje, se stanje projekta posodablja, da prikazuje stanje dejavnosti:</span><span class="sxs-lookup"><span data-stu-id="f0aff-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="f0aff-106">**Nov**</span><span class="sxs-lookup"><span data-stu-id="f0aff-106">**New**</span></span>    | <span data-ttu-id="f0aff-107">Ko ustvarite projekt, je stanje nastavljeno na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="f0aff-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="f0aff-108">Če ste ustvarili projekt iz predloge, ima na tej stopnji projekt morda urnik, ocene in podatke o ekipi.</span><span class="sxs-lookup"><span data-stu-id="f0aff-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="f0aff-109">V nasprotnem primeru je na voljo osnutek projekta in morate preostale komponente projekta vnesti ročno.</span><span class="sxs-lookup"><span data-stu-id="f0aff-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="f0aff-110">**Ponudba**</span><span class="sxs-lookup"><span data-stu-id="f0aff-110">**Quote**</span></span>   |      <span data-ttu-id="f0aff-111">Ko povežete projekt s ponudbo ali ga ustvarite iz ponudbe, je stopnja projekta nastavljena na **Ponudba**, pri čemer se posodobita tudi ocenjeni začetek in konec projekta.</span><span class="sxs-lookup"><span data-stu-id="f0aff-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="f0aff-112">Ko je projekt v stanju ponudbe, so podrobnosti o ponudbi prikazane na zavihku **Prodaja** na strani **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="f0aff-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="f0aff-113">**Načrt**</span><span class="sxs-lookup"><span data-stu-id="f0aff-113">**Plan**</span></span>   |                                     <span data-ttu-id="f0aff-114">Ko je ponudba, povezana s projektom, sprejeta, in ko se dejavnost premakne v stanje pogodbe, se stanje projekta posodobi v **Načrt**.</span><span class="sxs-lookup"><span data-stu-id="f0aff-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="f0aff-115">Podrobnosti pogodbe so prikazane na zavihku **Prodaja** na strani **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="f0aff-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="f0aff-116">**Dokončaj**</span><span class="sxs-lookup"><span data-stu-id="f0aff-116">**Complete**</span></span> |                    <span data-ttu-id="f0aff-117">Ko je delo na projektu končano, lahko stanje preklopite v **Zaključeno**.</span><span class="sxs-lookup"><span data-stu-id="f0aff-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="f0aff-118">Ko je projekt zaključen, to pomeni, da je delo v celoti opravljeno, vseeno pa je projekt odprt zaradi čakajočih vnosov, povezanih s časom ali stroški.</span><span class="sxs-lookup"><span data-stu-id="f0aff-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="f0aff-119">**Zapri**</span><span class="sxs-lookup"><span data-stu-id="f0aff-119">**Close**</span></span>   |           <span data-ttu-id="f0aff-120">Ko so vse transakcije, povezane s projektom zabeležene in ne pričakujete nobenih novih, lahko stanje ročno preklopite v **Zaprto**.</span><span class="sxs-lookup"><span data-stu-id="f0aff-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="f0aff-121">Ko je projekt nastavljen na **Zaprto**, vanj ni več mogoče zapisovati transakcij, saj je projekt dostopen samo za branje.</span><span class="sxs-lookup"><span data-stu-id="f0aff-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="f0aff-122">Spremljanje stanja projekta</span><span class="sxs-lookup"><span data-stu-id="f0aff-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="f0aff-123">Pojdite na **Project Service > Projekti**.</span><span class="sxs-lookup"><span data-stu-id="f0aff-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="f0aff-124">Kliknite projekt, s katerim se želite ukvarjati.</span><span class="sxs-lookup"><span data-stu-id="f0aff-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="f0aff-125">V vrstici na zgornjem delu zaslona izberite puščico dol poleg imena projekta, nato kliknite **Spremljanje projekta**.</span><span class="sxs-lookup"><span data-stu-id="f0aff-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="f0aff-126">V spustnem meniju nad seznamom opravil izberite **Spremljanje obsega dela** ali **Spremljanje stroškov**.</span><span class="sxs-lookup"><span data-stu-id="f0aff-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="f0aff-127">Če želite urediti opravilo, ga kliknite.</span><span class="sxs-lookup"><span data-stu-id="f0aff-127">Double-click any task to edit it.</span></span> <span data-ttu-id="f0aff-128">Lahko tudi premikate stolpce v Ganttovem grafikonu ali spreminjate njihovo velikost, ter tako spremenite čas in napredek opravila.</span><span class="sxs-lookup"><span data-stu-id="f0aff-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="f0aff-129">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="f0aff-129">See Also</span></span>  
 [<span data-ttu-id="f0aff-130">Priročnik za vodje projektov</span><span class="sxs-lookup"><span data-stu-id="f0aff-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]