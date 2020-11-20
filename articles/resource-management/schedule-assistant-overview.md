---
title: Pregled pomočnika za razporejanje
description: Ta tema vsebuje informacije o uporabljanju pomočnika za razporejanje pri rezervaciji virov.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125648"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="5484c-103">Pregled pomočnika za razporejanje</span><span class="sxs-lookup"><span data-stu-id="5484c-103">Schedule assistant overview</span></span>

<span data-ttu-id="5484c-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="5484c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5484c-105">Pomočnik za razporejanje se uporablja za rezerviranje virov na podlagi zahtev, ki jih določi vodja projekta.</span><span class="sxs-lookup"><span data-stu-id="5484c-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="5484c-106">Pomočnik za razporejanje se pri iskanju vira opira na parametre, navedene v zahtevi za vir.</span><span class="sxs-lookup"><span data-stu-id="5484c-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="5484c-107">Pomočnik za razporejanje priporoča vire, ki ustrezajo relevantnim zahtevam, kot so časovni okvirji ali potrebna znanja.</span><span class="sxs-lookup"><span data-stu-id="5484c-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="5484c-108">Ko so določeni ustrezni viri, lahko vodja virov ali projekta rezervira vir za opravilo.</span><span class="sxs-lookup"><span data-stu-id="5484c-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5484c-109">Zahteve</span><span class="sxs-lookup"><span data-stu-id="5484c-109">Prerequisites</span></span>

<span data-ttu-id="5484c-110">Pomočnik za razporejanje je del rešitve Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="5484c-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="5484c-111">Ta rešitev je vključena in nameščena v storitev Dynamics 365 Project Operations, Dynamics 365 Field Service in Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="5484c-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="5484c-112">Usklajevanje zahtev z viri</span><span class="sxs-lookup"><span data-stu-id="5484c-112">Matching requirements and resources</span></span>

<span data-ttu-id="5484c-113">Ustvarjena zahteva za vir temelji na podrobnostih, kot so:</span><span class="sxs-lookup"><span data-stu-id="5484c-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="5484c-114">Značilnosti</span><span class="sxs-lookup"><span data-stu-id="5484c-114">Characteristics</span></span>
-   <span data-ttu-id="5484c-115">Vloge</span><span class="sxs-lookup"><span data-stu-id="5484c-115">Roles</span></span>
-   <span data-ttu-id="5484c-116">Poslovne enote</span><span class="sxs-lookup"><span data-stu-id="5484c-116">Business units</span></span>
-   <span data-ttu-id="5484c-117">Nastavitve virov</span><span class="sxs-lookup"><span data-stu-id="5484c-117">Resource preferences</span></span>
-   <span data-ttu-id="5484c-118">Krivulja obsega dela</span><span class="sxs-lookup"><span data-stu-id="5484c-118">Effort contours</span></span>
-   <span data-ttu-id="5484c-119">Časovni pas</span><span class="sxs-lookup"><span data-stu-id="5484c-119">Time zone</span></span>

<span data-ttu-id="5484c-120">Pomočnik za razporejanje uporabi te podrobnosti za filtriranje virov.</span><span class="sxs-lookup"><span data-stu-id="5484c-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="5484c-121">Zagon pomočnika za razporejanje</span><span class="sxs-lookup"><span data-stu-id="5484c-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="5484c-122">Pomočnika za razporejanje je mogoče zagnati na dva načina.</span><span class="sxs-lookup"><span data-stu-id="5484c-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="5484c-123">Če uporabljate hibridni način, lahko v mreži članov ekipe izberete katerega koli člana ekipe z neizpolnjeno zahtevo za vir in kliknete **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="5484c-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="5484c-124">Če uporabljate osrednji način, bo vir poiskala in izbrala rešitev Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="5484c-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="5484c-125">Filtri pomočnika za razporejanje</span><span class="sxs-lookup"><span data-stu-id="5484c-125">Schedule assistant filters</span></span>

<span data-ttu-id="5484c-126">Po zagonu pomočnika za razporejanje se podrobnosti iz zahteve za vir prikažejo kot filtrirane vrednosti v levem podoknu.</span><span class="sxs-lookup"><span data-stu-id="5484c-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="5484c-127">Rešitev Resource Manager ali vodja projektov lahko natančno prilagodi rezultate tako, da prilagodi filtre, ki ustrezajo potrebam po razporejanju.</span><span class="sxs-lookup"><span data-stu-id="5484c-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="5484c-128">Podokno filtra prikazuje z delom povezane možnosti, kot so:</span><span class="sxs-lookup"><span data-stu-id="5484c-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="5484c-129">Začetek in konec dela</span><span class="sxs-lookup"><span data-stu-id="5484c-129">Work start and end</span></span>
-   <span data-ttu-id="5484c-130">Značilnosti</span><span class="sxs-lookup"><span data-stu-id="5484c-130">Characteristics</span></span>
-   <span data-ttu-id="5484c-131">Vloge</span><span class="sxs-lookup"><span data-stu-id="5484c-131">Roles</span></span>
-   <span data-ttu-id="5484c-132">Organizacijske enote</span><span class="sxs-lookup"><span data-stu-id="5484c-132">Organizational units</span></span>
-   <span data-ttu-id="5484c-133">Podjetje, ki zagotavlja vire</span><span class="sxs-lookup"><span data-stu-id="5484c-133">Resourcing company</span></span>
-   <span data-ttu-id="5484c-134">Vrste virov</span><span class="sxs-lookup"><span data-stu-id="5484c-134">Resource types</span></span>
-   <span data-ttu-id="5484c-135">Prednostni viri</span><span class="sxs-lookup"><span data-stu-id="5484c-135">Preferred resources</span></span>
