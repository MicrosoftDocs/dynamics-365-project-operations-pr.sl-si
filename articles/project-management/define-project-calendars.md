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
ms.openlocfilehash: e25b11b6b947627ca2ac88952e74aecccc346c89
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286988"
---
# <a name="define-project-calendars"></a><span data-ttu-id="34b0b-103">Določitev koledarjev projektov</span><span class="sxs-lookup"><span data-stu-id="34b0b-103">Define project calendars</span></span>

<span data-ttu-id="34b0b-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="34b0b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="34b0b-105">Če želite ustvariti razpored projekta, ustvarite predlogo koledarja za projekt, ki določa število delovnih ur na dan in vse dneve, ko je podjetje zaprto.</span><span class="sxs-lookup"><span data-stu-id="34b0b-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="34b0b-106">Če želite ustvariti predlogo koledarja za projekt, povežite delovno predlogo s poljem **Predloga koledarja** za projekt.</span><span class="sxs-lookup"><span data-stu-id="34b0b-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="34b0b-107">Za ustvarjanje delovne predloge sledite spodnjim korakom.</span><span class="sxs-lookup"><span data-stu-id="34b0b-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="34b0b-108">V podoknu za krmarjenje na levi izberite **Viri**.</span><span class="sxs-lookup"><span data-stu-id="34b0b-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="34b0b-109">Na strani seznama **Viri** odprite zapis uporabnika in nato izberite **Prikaži delovne ure**.</span><span class="sxs-lookup"><span data-stu-id="34b0b-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="34b0b-110">Preverite, ali dovolite pojavna okna na strani brskalnika.</span><span class="sxs-lookup"><span data-stu-id="34b0b-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="34b0b-111">Tako lahko vidite delovne ure, nastavljene za vir.</span><span class="sxs-lookup"><span data-stu-id="34b0b-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="34b0b-112">Na zavihku **Mesečni pogled** izberite **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="34b0b-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="34b0b-113">Prikaže se seznam treh možnosti:</span><span class="sxs-lookup"><span data-stu-id="34b0b-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="34b0b-114">Nov tedenski urnik</span><span class="sxs-lookup"><span data-stu-id="34b0b-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="34b0b-115">Urnik dela za en dan</span><span class="sxs-lookup"><span data-stu-id="34b0b-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="34b0b-116">Prosti čas</span><span class="sxs-lookup"><span data-stu-id="34b0b-116">Time Off</span></span>

4. <span data-ttu-id="34b0b-117">Izberite **Nov tedenski urnik** in nato nastavite možnosti za ta razpored virov.</span><span class="sxs-lookup"><span data-stu-id="34b0b-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="34b0b-118">Nastavite lahko ponavljajoči se tedenski razpored, dnevne in urne parametre, čas, ko je podjetje zaprto, in še več.</span><span class="sxs-lookup"><span data-stu-id="34b0b-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="34b0b-119">Nastavite datumski obseg, izberite **Shrani** in nato izberite **Zapri**.</span><span class="sxs-lookup"><span data-stu-id="34b0b-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="34b0b-120">Vrnite se na stran seznama **Viri** in izberite vir, za katerega ste nastavili delovne ure.</span><span class="sxs-lookup"><span data-stu-id="34b0b-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="34b0b-121">Izberite **Nastavi koledar kot**, da nastavite delovno predlogo.</span><span class="sxs-lookup"><span data-stu-id="34b0b-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="34b0b-122">V pogovornem oknu **Delovna predloga** vnesite ime delovne predloge in izberite **Uporabi**.</span><span class="sxs-lookup"><span data-stu-id="34b0b-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="34b0b-123">Delovno predlogo lahko zdaj povežete s predlogo koledarja projekta.</span><span class="sxs-lookup"><span data-stu-id="34b0b-123">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]