---
title: Pregled pomočnika za razporejanje
description: Ta tema vsebuje informacije o uporabljanju pomočnika za razporejanje pri rezervaciji virov.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 83583c97e4ecb5f1fdc0d8d98098afe8e12d27e4
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368136"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="25909-103">Pregled pomočnika za razporejanje</span><span class="sxs-lookup"><span data-stu-id="25909-103">Schedule assistant overview</span></span>

<span data-ttu-id="25909-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="25909-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25909-105">Pomočnik za razporejanje se uporablja za rezerviranje virov na podlagi zahtev, ki jih določi vodja projekta.</span><span class="sxs-lookup"><span data-stu-id="25909-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="25909-106">Pomočnik za razporejanje se pri iskanju vira opira na parametre, navedene v zahtevi za vir.</span><span class="sxs-lookup"><span data-stu-id="25909-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="25909-107">Pomočnik za razporejanje priporoča vire, ki ustrezajo relevantnim zahtevam, kot so časovni okvirji ali potrebna znanja.</span><span class="sxs-lookup"><span data-stu-id="25909-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="25909-108">Ko so določeni ustrezni viri, lahko vodja virov ali projekta rezervira vir za opravilo.</span><span class="sxs-lookup"><span data-stu-id="25909-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="25909-109">Zahteve</span><span class="sxs-lookup"><span data-stu-id="25909-109">Prerequisites</span></span>

<span data-ttu-id="25909-110">Pomočnik za razporejanje je del rešitve Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="25909-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="25909-111">Ta rešitev je vključena in nameščena v aplikacijah Dynamics 365 Project Operations, Dynamics 365 Field Service in Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="25909-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="25909-112">Usklajevanje zahtev z viri</span><span class="sxs-lookup"><span data-stu-id="25909-112">Matching requirements and resources</span></span>

<span data-ttu-id="25909-113">Ustvarjena zahteva za vir temelji na podrobnostih, kot so:</span><span class="sxs-lookup"><span data-stu-id="25909-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="25909-114">Značilnosti</span><span class="sxs-lookup"><span data-stu-id="25909-114">Characteristics</span></span>
-   <span data-ttu-id="25909-115">Vloge</span><span class="sxs-lookup"><span data-stu-id="25909-115">Roles</span></span>
-   <span data-ttu-id="25909-116">Poslovne enote</span><span class="sxs-lookup"><span data-stu-id="25909-116">Business units</span></span>
-   <span data-ttu-id="25909-117">Nastavitve virov</span><span class="sxs-lookup"><span data-stu-id="25909-117">Resource preferences</span></span>
-   <span data-ttu-id="25909-118">Krivulja obsega dela</span><span class="sxs-lookup"><span data-stu-id="25909-118">Effort contours</span></span>
-   <span data-ttu-id="25909-119">Časovni pas</span><span class="sxs-lookup"><span data-stu-id="25909-119">Time zone</span></span>

<span data-ttu-id="25909-120">Pomočnik za razporejanje uporabi te podrobnosti za filtriranje virov.</span><span class="sxs-lookup"><span data-stu-id="25909-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="25909-121">Zagon pomočnika za razporejanje</span><span class="sxs-lookup"><span data-stu-id="25909-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="25909-122">Pomočnika za razporejanje je mogoče zagnati na dva načina.</span><span class="sxs-lookup"><span data-stu-id="25909-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="25909-123">Če uporabljate hibridni način, lahko v mreži članov ekipe izberete katerega koli člana ekipe z neizpolnjeno zahtevo za vir in kliknete **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="25909-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="25909-124">Če uporabljate osrednji način, bo vir poiskala in izbrala rešitev Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="25909-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="25909-125">Filtri pomočnika za razporejanje</span><span class="sxs-lookup"><span data-stu-id="25909-125">Schedule assistant filters</span></span>

<span data-ttu-id="25909-126">Po zagonu pomočnika za razporejanje se podrobnosti iz zahteve za vir prikažejo kot filtrirane vrednosti v levem podoknu.</span><span class="sxs-lookup"><span data-stu-id="25909-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="25909-127">Rešitev Resource Manager ali vodja projektov lahko natančno prilagodi rezultate tako, da prilagodi filtre, ki ustrezajo potrebam po razporejanju.</span><span class="sxs-lookup"><span data-stu-id="25909-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="25909-128">Podokno filtra prikazuje z delom povezane možnosti, kot so:</span><span class="sxs-lookup"><span data-stu-id="25909-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="25909-129">Začetek in konec dela</span><span class="sxs-lookup"><span data-stu-id="25909-129">Work start and end</span></span>
-   <span data-ttu-id="25909-130">Značilnosti</span><span class="sxs-lookup"><span data-stu-id="25909-130">Characteristics</span></span>
-   <span data-ttu-id="25909-131">Vloge</span><span class="sxs-lookup"><span data-stu-id="25909-131">Roles</span></span>
-   <span data-ttu-id="25909-132">Organizacijske enote</span><span class="sxs-lookup"><span data-stu-id="25909-132">Organizational units</span></span>
-   <span data-ttu-id="25909-133">Podjetje, ki zagotavlja vire</span><span class="sxs-lookup"><span data-stu-id="25909-133">Resourcing company</span></span>
-   <span data-ttu-id="25909-134">Vrste virov</span><span class="sxs-lookup"><span data-stu-id="25909-134">Resource types</span></span>
-   <span data-ttu-id="25909-135">Prednostni viri</span><span class="sxs-lookup"><span data-stu-id="25909-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]