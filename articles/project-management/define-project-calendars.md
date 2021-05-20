---
title: Določitev koledarjev projektov
description: Ta tema vsebuje informacije o tem, kako uporabiti predlogo koledarja v projektu za sledenje razporedu projekta.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981320"
---
# <a name="define-project-calendars"></a><span data-ttu-id="3e5c3-103">Določitev koledarjev projektov</span><span class="sxs-lookup"><span data-stu-id="3e5c3-103">Define project calendars</span></span>

<span data-ttu-id="3e5c3-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="3e5c3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3e5c3-105">Če želite ustvariti projekt in ga upravljati, morate za projekt uporabiti predlogo koledarja.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="3e5c3-106">Predloga koledarja opredeljuje naslednje atribute projekta:</span><span class="sxs-lookup"><span data-stu-id="3e5c3-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="3e5c3-107">Delovni čas, vključno z začetnim in končnim časom</span><span class="sxs-lookup"><span data-stu-id="3e5c3-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="3e5c3-108">Delovni dnevi</span><span class="sxs-lookup"><span data-stu-id="3e5c3-108">Working days</span></span>
- <span data-ttu-id="3e5c3-109">Izjeme v koledarju, kot so prosti dnevi</span><span class="sxs-lookup"><span data-stu-id="3e5c3-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="3e5c3-110">Predloga koledarja, ki se uporablja za projekt, je kopija predloge koledarja, določene v nastavitvah vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="3e5c3-111">Če spremenite predlogo koledarja, se te spremembe ne bodo razširile na delovni čas projekta.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="3e5c3-112">Za spremembo delovnega časa projekta je treba uporabiti novo predlogo.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="3e5c3-113">Če želite ustvariti predlogo koledarja za svojo organizacijo, je treba upoštevati ključni zahtevi:</span><span class="sxs-lookup"><span data-stu-id="3e5c3-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="3e5c3-114">Določite želeni delovni čas predloge z novim ali obstoječim virom, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="3e5c3-115">Ustvarite novo predlogo koledarja in jo povežite z virom, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="3e5c3-116">**Določanje delovnega časa predloge**</span><span class="sxs-lookup"><span data-stu-id="3e5c3-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="3e5c3-117">Odprite možnost **Viri** \> **Viri**.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="3e5c3-118">Ustvarite nov vir za sklicevanje v predlogi koledarja ali izberite obstoječega.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="3e5c3-119">Izberite zavihek **Delovni čas** vira in upoštevajte navodila v članku [Nastavitev delovnih ur za vir](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource), da konfigurirate pravila koledarja.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="3e5c3-120">**Ustvarjanje nove predloge koledarja**</span><span class="sxs-lookup"><span data-stu-id="3e5c3-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="3e5c3-121">Odprite razdelek **Nastavitve** \> **Predloga koledarja**.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="3e5c3-122">Izberite možnost **Novo** in vnesite ime, opis in vir predloge.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="3e5c3-123">Ko je vir naveden v predlogi koledarja, je kopija koledarja vira povezana s predlogo koledarja.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="3e5c3-124">Če se delovni časi kopije predloge spremenijo, se te spremembe ne bodo razširile na predlogo projekta.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="3e5c3-125">Delovno predlogo lahko zdaj povežete s predlogo koledarja projekta.</span><span class="sxs-lookup"><span data-stu-id="3e5c3-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

