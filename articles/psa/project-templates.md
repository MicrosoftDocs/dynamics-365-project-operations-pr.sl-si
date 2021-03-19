---
title: Projektne predloge
description: Ta tema ponuja informacije o uporabi projektnih predlog za hitro nastavitev projekta.
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
ms.openlocfilehash: d9d208ebcef127062428afdadde2c54eb07ea505
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283613"
---
# <a name="project-templates"></a><span data-ttu-id="10853-103">Projektne predloge</span><span class="sxs-lookup"><span data-stu-id="10853-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="10853-104">Projektna predloga je vnaprej določeno ogrodje, ki vam pomaga hitro in enostavno zagnati projekt.</span><span class="sxs-lookup"><span data-stu-id="10853-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="10853-105">Uporabite lahko vnaprej določeno predlogo in ustvarite nov projekt z enim klikom.</span><span class="sxs-lookup"><span data-stu-id="10853-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="10853-106">Enako kot pri projektih morate določiti pogoje za projektne predloge.</span><span class="sxs-lookup"><span data-stu-id="10853-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="10853-107">Za vsako projektno predlogo morate določiti koledar projekta, vloge in ceniki pa morajo biti vnaprej določeni v organizaciji, tako da imajo komponente predloge uporabne podatke.</span><span class="sxs-lookup"><span data-stu-id="10853-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="10853-108">Projektna predloga je sestavljena iz treh komponent: razporeda, ocen projekta in članov projektne ekipe.</span><span class="sxs-lookup"><span data-stu-id="10853-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="10853-109">Urnik</span><span class="sxs-lookup"><span data-stu-id="10853-109">Schedule</span></span>

<span data-ttu-id="10853-110">Razpored v projektni predlogi ima enak nabor elementov kot razpored v projektu.</span><span class="sxs-lookup"><span data-stu-id="10853-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="10853-111">Ustvarite lahko hierarhijo opravil, povežete vloge z opravili, določite atribute za razporejanje in nastavite odvisnosti.</span><span class="sxs-lookup"><span data-stu-id="10853-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="10853-112">Razpored v projektni predlogi podpira tudi načine opravil za vsako opravilo.</span><span class="sxs-lookup"><span data-stu-id="10853-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="10853-113">Zato podpira mehanizem razporejanja.</span><span class="sxs-lookup"><span data-stu-id="10853-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="10853-114">Koledar projekta morate povezati s projektom.</span><span class="sxs-lookup"><span data-stu-id="10853-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="10853-115">Ko ustvarite razpored dela, med projektno predlogo in projektom ni razlik.</span><span class="sxs-lookup"><span data-stu-id="10853-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="10853-116">Projektne ocene</span><span class="sxs-lookup"><span data-stu-id="10853-116">Project estimates</span></span>

<span data-ttu-id="10853-117">Projektne ocene v projektni predlogi delujejo na enak način kot projektne ocene v projektu.</span><span class="sxs-lookup"><span data-stu-id="10853-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="10853-118">Vendar pa se lastne in prodajne cene pridobijo iz privzetih cenikov z lastnimi in prodajnimi cenami, ki so določeni v parametrih.</span><span class="sxs-lookup"><span data-stu-id="10853-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="10853-119">Ustvarjanje projekta iz predloge</span><span class="sxs-lookup"><span data-stu-id="10853-119">Creating a project from a template</span></span>
 
<span data-ttu-id="10853-120">Projekt lahko iz projektne naloge ustvarite na več načinov:</span><span class="sxs-lookup"><span data-stu-id="10853-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="10853-121">Če ustvarite projekt iz ponudbe, lahko projektno predlogo izberete v pogovornem oknu **Hitro ustvarjanje: projekt**.</span><span class="sxs-lookup"><span data-stu-id="10853-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Pogovorno okno »Hitro ustvarjanje: projekt«](media/project-11.png)

- <span data-ttu-id="10853-123">Če ustvarite projekt tako, da izberete **Nov projekt**, se stran **Projekt** prikaže, preden je zapis shranjen.</span><span class="sxs-lookup"><span data-stu-id="10853-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="10853-124">V polju **Izberi predlogo** izberite eno od vnaprej določenih projektnih predlog v organizaciji.</span><span class="sxs-lookup"><span data-stu-id="10853-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="10853-125">Uporabite **Ustvari projekt iz predloge** na strani **Entiteta predloge**.</span><span class="sxs-lookup"><span data-stu-id="10853-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="10853-126">Kopiranje komponent predloge v projekt</span><span class="sxs-lookup"><span data-stu-id="10853-126">Copying components of template to project</span></span>

<span data-ttu-id="10853-127">Ko kopirate komponente projektne predloge v projekt, lahko pride do preglasitev, odvisno od nastavitev v projektu.</span><span class="sxs-lookup"><span data-stu-id="10853-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="10853-128">Kopiranje razporeda</span><span class="sxs-lookup"><span data-stu-id="10853-128">Copying the schedule</span></span>

<span data-ttu-id="10853-129">Če ima projekt drugačen projektni koledar kot predloga, bodo pri kopiranju razporeda iz projektne predloge za razpored opravil uporabljene delovne ure iz koledarja projekta.</span><span class="sxs-lookup"><span data-stu-id="10853-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="10853-130">Tako se razpored prilagodi osnovnemu koledarju projekta.</span><span class="sxs-lookup"><span data-stu-id="10853-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="10853-131">Podobno ima tudi prvo opravilo v razporedu začetni datum projekta, razpored za preostalo hierarhijo pa se posodobi glede na trajanje in odvisnosti, ki so navedene v predlogi.</span><span class="sxs-lookup"><span data-stu-id="10853-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="10853-132">Kopiranje projektnih ocen</span><span class="sxs-lookup"><span data-stu-id="10853-132">Copying project estimates</span></span> 

<span data-ttu-id="10853-133">Ko kopirate v vrsticah ocen projekta, se ceniki posodobijo.</span><span class="sxs-lookup"><span data-stu-id="10853-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="10853-134">Pri ceniku z lastnimi cenami te posodobitve temeljijo na lastniški enoti projekta.</span><span class="sxs-lookup"><span data-stu-id="10853-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="10853-135">Pri prodajnem ceniku temeljijo na stranki.</span><span class="sxs-lookup"><span data-stu-id="10853-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="10853-136">Pri projektih, ki so povezani z entiteto prodaje, se lastne in prodajne cene enote določijo na podlagi teh cenikov.</span><span class="sxs-lookup"><span data-stu-id="10853-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="10853-137">Kopiranje projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="10853-137">Copying a project team</span></span>

<span data-ttu-id="10853-138">Ko projektno ekipo kopirate iz projektne predloge v projekt, se prekopirajo tudi splošni viri skupaj z znanji in usposobljenostmi, opredeljenimi v predlogi.</span><span class="sxs-lookup"><span data-stu-id="10853-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="10853-139">Ohranijo se tudi dodelitve splošnega vira iz projektne predloge.</span><span class="sxs-lookup"><span data-stu-id="10853-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="10853-140">Poimenovani viri niso podprti v projektnih predlogah.</span><span class="sxs-lookup"><span data-stu-id="10853-140">Named resources aren't supported in project templates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]