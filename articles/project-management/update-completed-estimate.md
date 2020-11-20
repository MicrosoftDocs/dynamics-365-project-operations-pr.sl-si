---
title: Posodobitev ocene končnih stroškov
description: Ta tema vsebuje informacije o posodabljanju projekcije obsega dela za projekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127223"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="ebf30-103">Posodobitev ocene končnih stroškov</span><span class="sxs-lookup"><span data-stu-id="ebf30-103">Update estimate at completion</span></span>

<span data-ttu-id="ebf30-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="ebf30-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ebf30-105">Vodja projekta pogosto popravi prvotne ocene v opravilu.</span><span class="sxs-lookup"><span data-stu-id="ebf30-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="ebf30-106">Vnovične projekcije projekta so dojemanje ocen vodje projekta glede na trenutno stanje projekta.</span><span class="sxs-lookup"><span data-stu-id="ebf30-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="ebf30-107">Vendar pa ne priporočamo, da vodje projektov spreminjajo osnovne številke, saj osnova projekta predstavlja zanesljiv vir ocene razporeda in stroškov za projekt, s katerim so se strinjale vse zainteresirane skupine, ki sodelujejo v projektu.</span><span class="sxs-lookup"><span data-stu-id="ebf30-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="ebf30-108">Projektni vodja lahko znova projicira obseg dela v opravilih na dva načina:</span><span class="sxs-lookup"><span data-stu-id="ebf30-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="ebf30-109">Preglasi lahko privzeti predvideni obseg dela do zaključka (ETC) z novo oceno dejanskega preostalega obsega dela v opravilu.</span><span class="sxs-lookup"><span data-stu-id="ebf30-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="ebf30-110">Preglasi lahko privzeti odstotek napredka z novo oceno dejanskega napredka v opravilu.</span><span class="sxs-lookup"><span data-stu-id="ebf30-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="ebf30-111">Oba pristopa povzročita ponoven izračun ETC, ocena končnih stroškov (EAC) in odstotka napredka ter predvidenega odmika od obsega dela v opravilu.</span><span class="sxs-lookup"><span data-stu-id="ebf30-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="ebf30-112">Ponovno se izračunajo EAC, ETC in odstotek napredka v opravilih povzetkov, kar ustvari novo projekcijo odmika od obsega dela.</span><span class="sxs-lookup"><span data-stu-id="ebf30-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
