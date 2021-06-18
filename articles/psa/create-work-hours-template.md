---
title: Ustvarjanje predloge delovnih ur
description: V tej temi so opisana navodila za ustvarjanje predloge delovnih ur v storitvi Project Service.
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997216"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="20f89-103">Ustvarjanje predloge delovnih ur (rešitev Project Service)</span><span class="sxs-lookup"><span data-stu-id="20f89-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="20f89-104">Če želite ustvariti projekt in ga upravljati, morate za projekt uporabiti predlogo koledarja.</span><span class="sxs-lookup"><span data-stu-id="20f89-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="20f89-105">Predloga koledarja opredeljuje naslednje atribute projekta:</span><span class="sxs-lookup"><span data-stu-id="20f89-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="20f89-106">Delovni čas, vključno z začetnim in končnim časom</span><span class="sxs-lookup"><span data-stu-id="20f89-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="20f89-107">Delovni dnevi</span><span class="sxs-lookup"><span data-stu-id="20f89-107">Working days</span></span>
- <span data-ttu-id="20f89-108">Izjeme v koledarju, kot so prosti dnevi</span><span class="sxs-lookup"><span data-stu-id="20f89-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="20f89-109">Predloga koledarja, ki se uporablja za projekt, je kopija predloge koledarja, določene v nastavitvah vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="20f89-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="20f89-110">Če spremenite predlogo koledarja, se te spremembe ne bodo razširile na delovni čas projekta.</span><span class="sxs-lookup"><span data-stu-id="20f89-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="20f89-111">Za spremembo delovnega časa projekta je treba uporabiti novo predlogo.</span><span class="sxs-lookup"><span data-stu-id="20f89-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="20f89-112">Če želite ustvariti predlogo koledarja za svojo organizacijo, je treba upoštevati ključni zahtevi:</span><span class="sxs-lookup"><span data-stu-id="20f89-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="20f89-113">Določite želeni delovni čas predloge z novim ali obstoječim virom, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="20f89-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="20f89-114">Ustvarite novo predlogo koledarja in jo povežite z virom, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="20f89-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="20f89-115">**Določanje delovnega časa predloge**</span><span class="sxs-lookup"><span data-stu-id="20f89-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="20f89-116">Odprite možnost **Viri** \> **Viri**.</span><span class="sxs-lookup"><span data-stu-id="20f89-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="20f89-117">Ustvarite nov vir za sklicevanje v predlogi koledarja ali izberite obstoječega.</span><span class="sxs-lookup"><span data-stu-id="20f89-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="20f89-118">Izberite zavihek **Delovni čas** vira in upoštevajte navodila v članku [Nastavitev delovnih ur za vir](/dynamics365/field-service/set-work-hours-resource.md), da konfigurirate pravila koledarja.</span><span class="sxs-lookup"><span data-stu-id="20f89-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="20f89-119">**Ustvarjanje nove predloge koledarja**</span><span class="sxs-lookup"><span data-stu-id="20f89-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="20f89-120">Odprite razdelek **Nastavitve** \> **Predloga koledarja**.</span><span class="sxs-lookup"><span data-stu-id="20f89-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="20f89-121">Izberite možnost **Novo** in vnesite ime, opis in vir predloge.</span><span class="sxs-lookup"><span data-stu-id="20f89-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="20f89-122">Ko je vir naveden v predlogi koledarja, je kopija koledarja vira povezana s predlogo koledarja.</span><span class="sxs-lookup"><span data-stu-id="20f89-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="20f89-123">Če se delovni časi kopije predloge spremenijo, se te spremembe ne bodo razširile na predlogo projekta.</span><span class="sxs-lookup"><span data-stu-id="20f89-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="20f89-124">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="20f89-124">See Also</span></span>  
 [<span data-ttu-id="20f89-125">Nastavitev virov</span><span class="sxs-lookup"><span data-stu-id="20f89-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
