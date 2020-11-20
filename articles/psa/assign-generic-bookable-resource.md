---
title: Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in projektni ekipi
description: Ta tema vsebuje informacije o rezervaciji splošnih virov za opravila in projektne ekipe.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 19761b3e570ad664522e832069a8ac50fffead64
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127088"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="e2808-103">Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in ustvarjanje pogojev za vir</span><span class="sxs-lookup"><span data-stu-id="e2808-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e2808-104">Poleg rezervacije in dodeljevanja imenovanih ali pravih virov za projekt lahko projektnim opravilom dodelite splošne vire.</span><span class="sxs-lookup"><span data-stu-id="e2808-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="e2808-105">Ti viri lahko označujejo mesto za imenovane vire, dokler niste pripravljeni, da projektu dodelite imenovane vire.</span><span class="sxs-lookup"><span data-stu-id="e2808-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="e2808-106">V aplikaciji Project Service Automation (PSA) odprite stran **Projekt** in na zavihku **Načrtovanje** urnik vnesite ime položaja splošnega vira v celico razporeda **Vir**.</span><span class="sxs-lookup"><span data-stu-id="e2808-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="e2808-107">Lahko pa v celici kliknete ikono **Vir**, da se odpre izbirnik za vire in nato vnesete ime splošnega vira,ki ga želite ustvariti.</span><span class="sxs-lookup"><span data-stu-id="e2808-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Ustvarjanje in dodeljevanje splošnega člana ekipe](media/RM-how-to-9.png)

<span data-ttu-id="e2808-109">Odpre se plošča **Hitro ustvarjanje: član projektne ekipe**.</span><span class="sxs-lookup"><span data-stu-id="e2808-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="e2808-110">Vnesite vlogo in organizacijsko enoto splošnega člana ekipe virov in kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="e2808-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Hitro ustvarjanje splošnega člana ekipe](media/RM-how-to-10.png)

3. <span data-ttu-id="e2808-112">Ko ustvarite novega splošnega člana ekipe virov, se dodeli opravilu.</span><span class="sxs-lookup"><span data-stu-id="e2808-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="e2808-113">Ta splošni vir lahko nato dodelite tudi drugim opravilom v razporedu opravil.</span><span class="sxs-lookup"><span data-stu-id="e2808-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Dodeljevanje obstoječega splošnega člana ekipe opravilom](media/RM-how-to-11.png)

4. <span data-ttu-id="e2808-115">Ko dodelite splošen vir, lahko ustvarite zahtevo za vir in jo izpolnite tako, da neposredno rezervirate ali pošljete zahtevo za vir upravitelju virov.</span><span class="sxs-lookup"><span data-stu-id="e2808-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Ustvarjanje zahteve za splošnega člana ekipe](media/RM-how-to-12.png)

<span data-ttu-id="e2808-117">Poleg uporabe zgoraj omenjenega izbirnika virov lahko na mreži člana ekipe tudi neposredno dodajate splošne vire.</span><span class="sxs-lookup"><span data-stu-id="e2808-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="e2808-118">Sredstva se dodajo z zahtevo za vir, ki temelji na začetnem/končnem datumih in metodi dodelitve, določeni v **hitrem ustvarjanju: panel člana** projektne skupine.</span><span class="sxs-lookup"><span data-stu-id="e2808-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="e2808-119">Razliko lahko vidite, če neposredno dodate splošnega člana ekipe in nato splošnemu viru dodate več opravil, kot ima na voljo delovnih ur.</span><span class="sxs-lookup"><span data-stu-id="e2808-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="e2808-120">Kliknite **Ustvari zahtevo**, da se znova ustvari zahteva za uskladitev zahtevanih ur v povezavi z dodeljenimi opravili.</span><span class="sxs-lookup"><span data-stu-id="e2808-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="e2808-121">Na mreži ekipe lahko kliknete tudi **Zahtevani pogoj za vir**, da se odpre zahteva, nato dodate znanja, prednostne vire itd.</span><span class="sxs-lookup"><span data-stu-id="e2808-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Zahtevani pogoj za vir](media/RM-how-to-13.png)

