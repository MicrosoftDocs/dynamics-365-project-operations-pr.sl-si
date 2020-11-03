---
title: Ocena prodaje in stroškov projekta, ko vir, ki ga je mogoče rezervirati, zapolni več vlog v projektu
description: V tej temi so na voljo podatki o tem, kako se lahko cenovne razsežnosti uporabijo za podporo cen in stroškov za vir, ki zapolni več vlog v projektu.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084808"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="6eb5a-103">Ocena prodaje in stroškov projekta, ko vir, ki ga je mogoče rezervirati, zapolni več vlog v projektu</span><span class="sxs-lookup"><span data-stu-id="6eb5a-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="6eb5a-104">Podjetja, ki poslujejo na podlagi projektov, pogosto potrebujejo en vir za izvajanje več vlog v projektu.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="6eb5a-105">Za vsako od teh vlog je mogoče določiti različne cene in stroške, kar pomeni, da lahko čas istega vira v projektu dobi različne finančne ocene, odvisno od deležev obračunavanja in stroškov za vsako od vlog.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="6eb5a-106">Project Service Automation omogoča nastavitev vrednosti v zapisu člana ekipe za imenovani vir in omogoča različne razveljavitve za vsako opravilo, kateremu je dodeljen član ekipe.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="6eb5a-107">V naslednjem primeru je pojasnjeno, kako preprosta preglasitev te vrednosti omogoča viru, da ima v projektu več vlog z različnimi stroški in deleži obračunavanja.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="6eb5a-108">Ustvarjanje opravil</span><span class="sxs-lookup"><span data-stu-id="6eb5a-108">Create tasks</span></span>
<span data-ttu-id="6eb5a-109">Ustvarite dve projektni opravili po 40 ur, »Opravilo A« in »Opravilo B«. »Opravilo A« določite kot predhodnika opravila B.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="6eb5a-110">Nastavitev vloge in organizacijske enote za splošnega člana projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="6eb5a-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="6eb5a-111">Na strani **Razpored** izberite vrstico **Opravilo** za opravilo A.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="6eb5a-112">V polju **Viri** na spustnem seznamu izberite možnost **Ustvari**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="6eb5a-113">Na strani **Hitro ustvarjanje člana ekipe** določite atribute splošnega člana ekipe, ki lahko izvaja to opravilo.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="6eb5a-114">Izberite ustrezno vlogo in organizacijsko enoto, nato pa izberite **Shrani in zapri**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="6eb5a-115">Za to opravilo je ustvarjen in dodeljen splošni član ekipe.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="6eb5a-116">Ponovite te korake za opravilo B in se prepričajte, da se vloga in organizacijska enota splošnega člana ekipe, ustvarjenega za opravilo B, razlikujeta od opravila A.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="6eb5a-117">Nastavitev vloge in organizacijske enote za projektno opravilo</span><span class="sxs-lookup"><span data-stu-id="6eb5a-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="6eb5a-118">Ko ustvarite opravilo A, ga izberite in nato izberite **Uredi opravilo**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="6eb5a-119">Na strani **Podrobnosti opravila** poiščite polji **Vloga** in **Organizacijska enota** , nato dodajte vrednosti, potrebne za vir, ki bi opravil to opravilo.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="6eb5a-120">Če ta scenarij izpolnjujete s predstavitvenimi podatki rešitve Project Service Automation, za vlogo izberite **Svetovalni vodja** in za organizacijsko enoto **Fabrikam ZDA**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="6eb5a-121">Izberite opravilo B in nato izberite **Uredi opravilo**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="6eb5a-122">Na strani **Podrobnosti opravila** poiščite polji **Vloga** in **Organizacijska enota** , nato dodajte vrednosti, potrebne za vir, ki bi opravil to opravilo.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="6eb5a-123">Prepričajte se, da se vrednosti v poljih **Vloga** in **Organizacijska enota** za opravilo A in opravilo B razlikujejo.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="6eb5a-124">Če ta scenarij izpolnjujete s predstavitvenimi podatki rešitve Project Service Automation, za vlogo izberite **Omrežni tehnik** in za organizacijsko enoto **Fabrikam ZDA**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="6eb5a-125">Shranite in zaprite stran **Podrobnosti opravila**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="6eb5a-126">Član ekipe in ocenjeno vedenje</span><span class="sxs-lookup"><span data-stu-id="6eb5a-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="6eb5a-127">Na strani **Podrobnosti opravila** v razdelku **Član ekipe** izberite dva splošna člana ekipe, nato pa izberite možnost **Ustvari zahteve**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="6eb5a-128">S tem se bodo ustvarile zahteve za vir.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="6eb5a-129">Izberite vrstico člana ekipe za vlogo **Svetovalni vodja** in nato izberite možnost **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="6eb5a-130">Odpre se plošča razporeda in rezervira vir za to zahtevo.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="6eb5a-131">Izberite vrstico člana ekipe za vlogo **Omrežni tehnik** in nato izberite možnost **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="6eb5a-132">Odpre se plošča razporeda in rezervira isti vir za to zahtevo.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="6eb5a-133">Mreža člana ekipe</span><span class="sxs-lookup"><span data-stu-id="6eb5a-133">Team Member grid</span></span> 
<span data-ttu-id="6eb5a-134">V mreži **Član ekipe** boste opazili, da sta dva zapisa splošnega člana ekipe izbrisana, nadomestil pa ju je en sam vir.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="6eb5a-135">Ta vir ima en nabor vrednosti, ki prikazuje privzeti nabor vrednosti za možnosti **Vloga** in **Organizacijska enota**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="6eb5a-136">Ko razširite vrstico tega zapisa člana ekipe, lahko v zapisu člana ekipe vidite ločene dodelitve za obe opravili.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="6eb5a-137">V vsaki vrstici dodelitve so vrednosti, specifične za opravilo, za možnosti **Vloga** in **Organizacijska enota**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="6eb5a-138">Mreža ocen</span><span class="sxs-lookup"><span data-stu-id="6eb5a-138">Estimates grid</span></span> 
<span data-ttu-id="6eb5a-139">Ko se pomaknete do mreže **Ocene** , boste opazili, da sta za obe dodelitvi za isti vir določeni različni ceni.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="6eb5a-140">Dodelitev za vir v opravilu A je ocenjena na podlagi vrednosti atributa **Vloga** za možnost **Svetovalni vodja**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="6eb5a-141">Dodelitev za isti vir v opravilu B je ocenjena na podlagi vrednosti atributa **Vloga** za možnost **Omrežni tehnik**.</span><span class="sxs-lookup"><span data-stu-id="6eb5a-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





