---
title: Ustvarjanje projektne predloge
description: Navodila za ustvarjanje predloge projekta v rešitvi Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755755"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="e9629-103">Ustvarjanje predloge projekta (rešitev Project Service)</span><span class="sxs-lookup"><span data-stu-id="e9629-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e9629-104">Če se vaše podjetje redno poteguje za podobne vrste projektov, boste s projektnimi predlogami prihranili čas.</span><span class="sxs-lookup"><span data-stu-id="e9629-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="e9629-105">Vsebujejo standardni nabor vlog in predvidenih ur za določeno vrsto projekta.</span><span class="sxs-lookup"><span data-stu-id="e9629-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="e9629-106">Vodje za upravljanje kupcev in vodje projektov lahko ustvarijo projekte, ki temeljijo na projektni predlogi, ali pa kopirajo predlogo in naredijo svojo.</span><span class="sxs-lookup"><span data-stu-id="e9629-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="e9629-107">Komponente projektne predloge</span><span class="sxs-lookup"><span data-stu-id="e9629-107">Components of project template</span></span>
 <span data-ttu-id="e9629-108">Projektna predloga je sestavljena iz treh delov:</span><span class="sxs-lookup"><span data-stu-id="e9629-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="e9629-109">**Strukturirana členitev dela**: strukturirana členitev dela v projektni predlogi vsebuje enak nabor elementov kot v projektu.</span><span class="sxs-lookup"><span data-stu-id="e9629-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="e9629-110">Ustvarite lahko hierarhijo opravil, povežete vloge z opravilom, določite atribute načrtovanja, nastavite odvisnosti in si vse podatke ogledate v Ganttovem grafikonu.</span><span class="sxs-lookup"><span data-stu-id="e9629-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="e9629-111">Strukturirana členitev dela v projektnih predlogah za vsako opravilo podpira tudi način opravila.</span><span class="sxs-lookup"><span data-stu-id="e9629-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="e9629-112">Če ustvarjate načrtovanje dela, med projektno predlogo in projektom ni razlik.</span><span class="sxs-lookup"><span data-stu-id="e9629-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="e9629-113">**Ocene za projekte**: v predlogah ocene za projekte delujejo na enak način kot v projektih, saj so z izjemo cenikov za privzeto lastne in prodajne cene vedno privzete lastne in prodajne cene cenikov, ki so določeni s parametri [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e9629-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="e9629-114">Preostale funkcije so enake kot v projektu.</span><span class="sxs-lookup"><span data-stu-id="e9629-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="e9629-115">**Oblikovanje projektne ekipe**: ko za projektno predlogo oblikujete projektno ekipo, v predlogi ne morete rezervirati poimenskega vira.</span><span class="sxs-lookup"><span data-stu-id="e9629-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="e9629-116">Če želite ustvariti nabor splošnih virov, lahko v strukturirani členitvi dela uporabite **Ustvari projektno ekipo**.</span><span class="sxs-lookup"><span data-stu-id="e9629-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="e9629-117">Za splošne vire lahko določite tudi zahtevane spretnosti in usposobljenost.</span><span class="sxs-lookup"><span data-stu-id="e9629-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="e9629-118">V predlogah projekta ne morete nadomestiti splošnega vira z virom, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="e9629-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="e9629-119">Ustvari projekt iz predloge</span><span class="sxs-lookup"><span data-stu-id="e9629-119">Create a project from a template</span></span>  
 <span data-ttu-id="e9629-120">Iz predloge lahko projekt ustvarite na naslednje načine:</span><span class="sxs-lookup"><span data-stu-id="e9629-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="e9629-121">Če ustvarjate projekt iz ponudbe, lahko projektno predlogo izberete v obrazcu za hitro ustvarjanje projekta.</span><span class="sxs-lookup"><span data-stu-id="e9629-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="e9629-122">Če ustvarite projekt s klikom **Nov projekt**, se obrazec projekta prikaže, še preden shranite zapis.</span><span class="sxs-lookup"><span data-stu-id="e9629-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="e9629-123">Tukaj lahko kliknete polje **Izberi predlogo** in jo izberete s seznama vnaprej določenih projektnih predlog v vaši organizaciji.</span><span class="sxs-lookup"><span data-stu-id="e9629-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="e9629-124">Na strani **Projektna predloga** kliknite **Ustvari projekt iz predloge**, da ustvarite projekt iz predloge.</span><span class="sxs-lookup"><span data-stu-id="e9629-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="e9629-125">Kopiranje komponent predloge v projekt</span><span class="sxs-lookup"><span data-stu-id="e9629-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="e9629-126">Ko kopirate komponente predloge v projekt, morate vedeti nekaj stvari.</span><span class="sxs-lookup"><span data-stu-id="e9629-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="e9629-127">**Kopiranje strukturirane členitve dela**: če ima projekt drugačen projektni koledar kot predloga, bodo po kopiranju strukturirane členitve dela iz projektne predloge pri načrtovanju opravil uporabljene delovne ure iz koledarja projekta.</span><span class="sxs-lookup"><span data-stu-id="e9629-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="e9629-128">To prilagodi načrtovanje varnostnemu koledarju projekta.</span><span class="sxs-lookup"><span data-stu-id="e9629-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="e9629-129">Podobno ima tudi prvo opravilo v strukturirani členitvi dela začetni datum projekta, da se preostanek načrtovanja hierarhije opravil posodobi glede na trajanje in odvisnosti, ki sta navedena v strukturirani členitvi dela predloge.</span><span class="sxs-lookup"><span data-stu-id="e9629-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="e9629-130">**Kopiranje ocen projekta**: pri kopiranju čez vrstice projektnih ocen se ceniki posodobijo glede na lastniško enoto projekta za cenik z lastnimi cenami in stranke za prodajni cenik.</span><span class="sxs-lookup"><span data-stu-id="e9629-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="e9629-131">Lastne cene in prodajne cene enote se določijo iz teh cenikov za projekte, ki so povezani z entiteto prodaje.</span><span class="sxs-lookup"><span data-stu-id="e9629-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="e9629-132">**Kopiranje projektne ekipe**: Ko projektno ekipo kopirate iz predloga v projekt, se prekopirajo tudi splošni viri, skupaj s spretnostmi in usposobljenostjo, opredeljenimi v predlogi.</span><span class="sxs-lookup"><span data-stu-id="e9629-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="e9629-133">Ohranijo se tudi naloge splošnega vira tako kot v projektni predlogi.</span><span class="sxs-lookup"><span data-stu-id="e9629-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e9629-134">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="e9629-134">See Also</span></span>  
 [<span data-ttu-id="e9629-135">Priročnik za vodje projektov</span><span class="sxs-lookup"><span data-stu-id="e9629-135">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
