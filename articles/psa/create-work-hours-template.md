---
title: Ustvarjanje predloge delovnih ur
description: V tej temi so opisana navodila za ustvarjanje predloge delovnih ur v storitvi Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981275"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="12900-103">Ustvarjanje predloge delovnih ur (rešitev Project Service)</span><span class="sxs-lookup"><span data-stu-id="12900-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="12900-104">Če želite ustvariti projekt in ga upravljati, morate za projekt uporabiti predlogo koledarja.</span><span class="sxs-lookup"><span data-stu-id="12900-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="12900-105">Predloga koledarja opredeljuje naslednje atribute projekta:</span><span class="sxs-lookup"><span data-stu-id="12900-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="12900-106">Delovni čas, vključno z začetnim in končnim časom</span><span class="sxs-lookup"><span data-stu-id="12900-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="12900-107">Delovni dnevi</span><span class="sxs-lookup"><span data-stu-id="12900-107">Working days</span></span>
- <span data-ttu-id="12900-108">Izjeme v koledarju, kot so prosti dnevi</span><span class="sxs-lookup"><span data-stu-id="12900-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="12900-109">Predloga koledarja, ki se uporablja za projekt, je kopija predloge koledarja, določene v nastavitvah vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="12900-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="12900-110">Če spremenite predlogo koledarja, se te spremembe ne bodo razširile na delovni čas projekta.</span><span class="sxs-lookup"><span data-stu-id="12900-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="12900-111">Za spremembo delovnega časa projekta je treba uporabiti novo predlogo.</span><span class="sxs-lookup"><span data-stu-id="12900-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="12900-112">Če želite ustvariti predlogo koledarja za svojo organizacijo, je treba upoštevati ključni zahtevi:</span><span class="sxs-lookup"><span data-stu-id="12900-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="12900-113">Določite želeni delovni čas predloge z novim ali obstoječim virom, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="12900-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="12900-114">Ustvarite novo predlogo koledarja in jo povežite z virom, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="12900-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="12900-115">**Določanje delovnega časa predloge**</span><span class="sxs-lookup"><span data-stu-id="12900-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="12900-116">Odprite možnost **Viri** \> **Viri**.</span><span class="sxs-lookup"><span data-stu-id="12900-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="12900-117">Ustvarite nov vir za sklicevanje v predlogi koledarja ali izberite obstoječega.</span><span class="sxs-lookup"><span data-stu-id="12900-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="12900-118">Izberite zavihek **Delovni čas** vira in upoštevajte navodila v članku [Nastavitev delovnih ur za vir](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource), da konfigurirate pravila koledarja.</span><span class="sxs-lookup"><span data-stu-id="12900-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="12900-119">**Ustvarjanje nove predloge koledarja**</span><span class="sxs-lookup"><span data-stu-id="12900-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="12900-120">Odprite razdelek **Nastavitve** \> **Predloga koledarja**.</span><span class="sxs-lookup"><span data-stu-id="12900-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="12900-121">Izberite možnost **Novo** in vnesite ime, opis in vir predloge.</span><span class="sxs-lookup"><span data-stu-id="12900-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="12900-122">Ko je vir naveden v predlogi koledarja, je kopija koledarja vira povezana s predlogo koledarja.</span><span class="sxs-lookup"><span data-stu-id="12900-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="12900-123">Če se delovni časi kopije predloge spremenijo, se te spremembe ne bodo razširile na predlogo projekta.</span><span class="sxs-lookup"><span data-stu-id="12900-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="12900-124">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="12900-124">See Also</span></span>  
 [<span data-ttu-id="12900-125">Nastavitev virov</span><span class="sxs-lookup"><span data-stu-id="12900-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
