---
title: Nastavitve projekta
description: Ta tema vsebuje informacije o nastavitvah upravljanja projektov.
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
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148168"
---
# <a name="project-settings"></a><span data-ttu-id="2231e-103">Nastavitve projekta</span><span class="sxs-lookup"><span data-stu-id="2231e-103">Project settings</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2231e-104">Za dostop do funkcij za načrtovanje projekta uporabite spodnje nastavitve.</span><span class="sxs-lookup"><span data-stu-id="2231e-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="2231e-105">Predloga za delo</span><span class="sxs-lookup"><span data-stu-id="2231e-105">Work template</span></span>

<span data-ttu-id="2231e-106">Če želite ustvariti razpored projekta, ustvarite predlogo koledarja za projekt, ki določa število delovnih ur na dan in vse dneve, ko je podjetje zaprto.</span><span class="sxs-lookup"><span data-stu-id="2231e-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="2231e-107">Če želite ustvariti predlogo koledarja za projekt, povežite delovno predlogo s poljem **Predloga koledarja** za projekt.</span><span class="sxs-lookup"><span data-stu-id="2231e-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="2231e-108">Za ustvarjanje delovne predloge sledite spodnjim korakom.</span><span class="sxs-lookup"><span data-stu-id="2231e-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="2231e-109">V PSA v podoknu za krmarjenje na levi kliknite **Viri**.</span><span class="sxs-lookup"><span data-stu-id="2231e-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="2231e-110">Na strani seznama **Viri** odprite zapis uporabnika in nato izberite **Prikaži delovne ure**.</span><span class="sxs-lookup"><span data-stu-id="2231e-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="2231e-111">Preverite, ali dovolite pojavna okna na strani brskalnika.</span><span class="sxs-lookup"><span data-stu-id="2231e-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="2231e-112">Tako lahko vidite delovne ure, nastavljene za vir.</span><span class="sxs-lookup"><span data-stu-id="2231e-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="2231e-113">Na zavihku **Mesečni pogled** kliknite **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="2231e-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="2231e-114">Prikaže se seznam treh možnosti:</span><span class="sxs-lookup"><span data-stu-id="2231e-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="2231e-115">Nov tedenski urnik</span><span class="sxs-lookup"><span data-stu-id="2231e-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="2231e-116">Urnik dela za en dan</span><span class="sxs-lookup"><span data-stu-id="2231e-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="2231e-117">Prosti čas</span><span class="sxs-lookup"><span data-stu-id="2231e-117">Time Off</span></span>

> ![Nastavitev možnosti](media/project-13.png)

4. <span data-ttu-id="2231e-119">Izberite **Nov tedenski urnik** in nato nastavite možnosti za ta razpored virov.</span><span class="sxs-lookup"><span data-stu-id="2231e-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="2231e-120">Nastavite lahko ponavljajoči se tedenski razpored, dnevne in urne parametre, čas, ko je podjetje zaprto, in še več.</span><span class="sxs-lookup"><span data-stu-id="2231e-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="2231e-121">Nastavite datumski obseg, izberite **Shrani** in nato kliknite **Zapri**.</span><span class="sxs-lookup"><span data-stu-id="2231e-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="2231e-122">Vrnite se na stran seznama **Viri** in izberite vir, za katerega ste nastavili delovne ure.</span><span class="sxs-lookup"><span data-stu-id="2231e-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="2231e-123">Izberite **Nastavi koledar kot**, da nastavite delovno predlogo.</span><span class="sxs-lookup"><span data-stu-id="2231e-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="2231e-124">V pogovornem oknu **Delovna predloga** vnesite ime delovne predloge in izberite **Uporabi**.</span><span class="sxs-lookup"><span data-stu-id="2231e-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="2231e-125">Delovno predlogo lahko zdaj povežete s predlogo koledarja projekta.</span><span class="sxs-lookup"><span data-stu-id="2231e-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="2231e-126">Vloge virov</span><span class="sxs-lookup"><span data-stu-id="2231e-126">Resource roles</span></span>

<span data-ttu-id="2231e-127">Izraz *vloga vira* se nanaša na nabor znanja, sposobnosti in potrdil, ki jih mora imeti oseba, da lahko izvaja določeno skupino opravil v okviru projekta.</span><span class="sxs-lookup"><span data-stu-id="2231e-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="2231e-128">PSA vam omogoča zaračunati in obračunati čas vira na podlagi vloge, s katero je vir povezan.</span><span class="sxs-lookup"><span data-stu-id="2231e-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="2231e-129">Vsaka organizacija mora nastaviti te vloge v podoknu za krmarjenje na levi strani menija **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="2231e-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="2231e-130">Vsaka organizacija mora nastaviti te vloge na strani **Kategorije dejavnih virov**.</span><span class="sxs-lookup"><span data-stu-id="2231e-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="2231e-131">Če želite odpreti to stran, v podoknu za krmarjenje na levi izberite **Vloge virov**.</span><span class="sxs-lookup"><span data-stu-id="2231e-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="2231e-132">Ceniki</span><span class="sxs-lookup"><span data-stu-id="2231e-132">Price lists</span></span>

<span data-ttu-id="2231e-133">S ceniki lahko nastavite lastne in prodajne cene za vloge virov, kategorije stroškov, izdelke in druge elemente v organizaciji.</span><span class="sxs-lookup"><span data-stu-id="2231e-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="2231e-134">Preden nastavite finančne ocene za delo, ki mora biti opravljeno pri projektu, ustvarite osnovni cenik z lastnimi in prodajnimi cenami.</span><span class="sxs-lookup"><span data-stu-id="2231e-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="2231e-135">V razdelku s parametri nastavite tudi privzeti cenik z lastnimi in prodajnimi cenami, ki velja za vse projekte, ustvarjene v organizaciji.</span><span class="sxs-lookup"><span data-stu-id="2231e-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="2231e-136">Na strani **Dejavni projektni parametri** preverite, ali ste nastavili privzeti cenik z lastnimi in prodajnimi cenami.</span><span class="sxs-lookup"><span data-stu-id="2231e-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
