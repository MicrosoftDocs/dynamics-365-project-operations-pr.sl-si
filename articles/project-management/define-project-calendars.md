---
title: Določitev koledarjev projektov
description: Ta tema vsebuje informacije o tem, kako uporabiti predlogo koledarja v projektu za sledenje razporedu projekta.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999016"
---
# <a name="define-project-calendars"></a><span data-ttu-id="5c507-103">Določitev koledarjev projektov</span><span class="sxs-lookup"><span data-stu-id="5c507-103">Define project calendars</span></span>

<span data-ttu-id="5c507-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="5c507-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5c507-105">Če želite ustvariti projekt in ga upravljati, morate za projekt uporabiti predlogo koledarja.</span><span class="sxs-lookup"><span data-stu-id="5c507-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="5c507-106">Predloga koledarja opredeljuje naslednje atribute projekta:</span><span class="sxs-lookup"><span data-stu-id="5c507-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="5c507-107">Delovni čas, vključno z začetnim in končnim časom</span><span class="sxs-lookup"><span data-stu-id="5c507-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="5c507-108">Delovni dnevi</span><span class="sxs-lookup"><span data-stu-id="5c507-108">Working days</span></span>
- <span data-ttu-id="5c507-109">Izjeme v koledarju, kot so prosti dnevi</span><span class="sxs-lookup"><span data-stu-id="5c507-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="5c507-110">Predloga koledarja, ki se uporablja za projekt, je kopija predloge koledarja, določene v nastavitvah vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="5c507-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="5c507-111">Če spremenite predlogo koledarja, se te spremembe ne bodo razširile na delovni čas projekta.</span><span class="sxs-lookup"><span data-stu-id="5c507-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="5c507-112">Za spremembo delovnega časa projekta je treba uporabiti novo predlogo.</span><span class="sxs-lookup"><span data-stu-id="5c507-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="5c507-113">Če želite ustvariti predlogo koledarja za svojo organizacijo, je treba upoštevati ključni zahtevi:</span><span class="sxs-lookup"><span data-stu-id="5c507-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="5c507-114">Določite želeni delovni čas predloge z novim ali obstoječim virom, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="5c507-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="5c507-115">Ustvarite novo predlogo koledarja in jo povežite z virom, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="5c507-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="5c507-116">**Določanje delovnega časa predloge**</span><span class="sxs-lookup"><span data-stu-id="5c507-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="5c507-117">Odprite možnost **Viri** \> **Viri**.</span><span class="sxs-lookup"><span data-stu-id="5c507-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="5c507-118">Ustvarite nov vir za sklicevanje v predlogi koledarja ali izberite obstoječega.</span><span class="sxs-lookup"><span data-stu-id="5c507-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="5c507-119">Izberite zavihek **Delovni čas** vira in upoštevajte navodila v članku [Nastavitev delovnih ur za vir](/dynamics365/field-service/set-work-hours-resource.md), da konfigurirate pravila koledarja.</span><span class="sxs-lookup"><span data-stu-id="5c507-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="5c507-120">**Ustvarjanje nove predloge koledarja**</span><span class="sxs-lookup"><span data-stu-id="5c507-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="5c507-121">Odprite razdelek **Nastavitve** \> **Predloga koledarja**.</span><span class="sxs-lookup"><span data-stu-id="5c507-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="5c507-122">Izberite možnost **Novo** in vnesite ime, opis in vir predloge.</span><span class="sxs-lookup"><span data-stu-id="5c507-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="5c507-123">Ko je vir naveden v predlogi koledarja, je kopija koledarja vira povezana s predlogo koledarja.</span><span class="sxs-lookup"><span data-stu-id="5c507-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="5c507-124">Če se delovni časi kopije predloge spremenijo, se te spremembe ne bodo razširile na predlogo projekta.</span><span class="sxs-lookup"><span data-stu-id="5c507-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="5c507-125">Delovno predlogo lahko zdaj povežete s predlogo koledarja projekta.</span><span class="sxs-lookup"><span data-stu-id="5c507-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

