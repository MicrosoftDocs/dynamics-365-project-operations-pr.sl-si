---
title: Določitev koledarjev projektov
description: Ta tema vsebuje informacije o uporabi koledarja projekta za sledenje razporedu projekta.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131678"
---
# <a name="define-project-calendars"></a><span data-ttu-id="f6c71-103">Določitev koledarjev projektov</span><span class="sxs-lookup"><span data-stu-id="f6c71-103">Define project calendars</span></span>

<span data-ttu-id="f6c71-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="f6c71-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f6c71-105">Če želite ustvariti razpored projekta, ustvarite predlogo koledarja za projekt, ki določa število delovnih ur na dan in vse dneve, ko je podjetje zaprto.</span><span class="sxs-lookup"><span data-stu-id="f6c71-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="f6c71-106">Če želite ustvariti predlogo koledarja za projekt, povežite delovno predlogo s poljem **Predloga koledarja** za projekt.</span><span class="sxs-lookup"><span data-stu-id="f6c71-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="f6c71-107">Za ustvarjanje delovne predloge sledite spodnjim korakom.</span><span class="sxs-lookup"><span data-stu-id="f6c71-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="f6c71-108">V podoknu za krmarjenje na levi izberite **Viri**.</span><span class="sxs-lookup"><span data-stu-id="f6c71-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="f6c71-109">Na strani seznama **Viri** odprite zapis uporabnika in nato izberite **Prikaži delovne ure**.</span><span class="sxs-lookup"><span data-stu-id="f6c71-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f6c71-110">Preverite, ali dovolite pojavna okna na strani brskalnika.</span><span class="sxs-lookup"><span data-stu-id="f6c71-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="f6c71-111">Tako lahko vidite delovne ure, nastavljene za vir.</span><span class="sxs-lookup"><span data-stu-id="f6c71-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="f6c71-112">Na zavihku **Mesečni pogled** izberite **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="f6c71-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="f6c71-113">Prikaže se seznam treh možnosti:</span><span class="sxs-lookup"><span data-stu-id="f6c71-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="f6c71-114">Nov tedenski urnik</span><span class="sxs-lookup"><span data-stu-id="f6c71-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="f6c71-115">Urnik dela za en dan</span><span class="sxs-lookup"><span data-stu-id="f6c71-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="f6c71-116">Prosti čas</span><span class="sxs-lookup"><span data-stu-id="f6c71-116">Time Off</span></span>

4. <span data-ttu-id="f6c71-117">Izberite **Nov tedenski urnik** in nato nastavite možnosti za ta razpored virov.</span><span class="sxs-lookup"><span data-stu-id="f6c71-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="f6c71-118">Nastavite lahko ponavljajoči se tedenski razpored, dnevne in urne parametre, čas, ko je podjetje zaprto, in še več.</span><span class="sxs-lookup"><span data-stu-id="f6c71-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="f6c71-119">Nastavite datumski obseg, izberite **Shrani** in nato izberite **Zapri**.</span><span class="sxs-lookup"><span data-stu-id="f6c71-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="f6c71-120">Vrnite se na stran seznama **Viri** in izberite vir, za katerega ste nastavili delovne ure.</span><span class="sxs-lookup"><span data-stu-id="f6c71-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="f6c71-121">Izberite **Nastavi koledar kot**, da nastavite delovno predlogo.</span><span class="sxs-lookup"><span data-stu-id="f6c71-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="f6c71-122">V pogovornem oknu **Delovna predloga** vnesite ime delovne predloge in izberite **Uporabi**.</span><span class="sxs-lookup"><span data-stu-id="f6c71-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="f6c71-123">Delovno predlogo lahko zdaj povežete s predlogo koledarja projekta.</span><span class="sxs-lookup"><span data-stu-id="f6c71-123">You can now associate the work template with a project calendar template.</span></span>
