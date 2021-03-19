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
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286448"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="ffa1e-103">Posodobitev ocene končnih stroškov</span><span class="sxs-lookup"><span data-stu-id="ffa1e-103">Update estimate at completion</span></span>

<span data-ttu-id="ffa1e-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="ffa1e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ffa1e-105">Vodja projekta pogosto popravi prvotne ocene v opravilu.</span><span class="sxs-lookup"><span data-stu-id="ffa1e-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="ffa1e-106">Vnovične projekcije projekta so dojemanje ocen vodje projekta glede na trenutno stanje projekta.</span><span class="sxs-lookup"><span data-stu-id="ffa1e-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="ffa1e-107">Vendar pa ne priporočamo, da vodje projektov spreminjajo osnovne številke, saj osnova projekta predstavlja zanesljiv vir ocene razporeda in stroškov za projekt, s katerim so se strinjale vse zainteresirane skupine, ki sodelujejo v projektu.</span><span class="sxs-lookup"><span data-stu-id="ffa1e-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="ffa1e-108">Projektni vodja lahko znova projicira obseg dela v opravilih na dva načina:</span><span class="sxs-lookup"><span data-stu-id="ffa1e-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="ffa1e-109">Preglasi lahko privzeti predvideni obseg dela do zaključka (ETC) z novo oceno dejanskega preostalega obsega dela v opravilu.</span><span class="sxs-lookup"><span data-stu-id="ffa1e-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="ffa1e-110">Preglasi lahko privzeti odstotek napredka z novo oceno dejanskega napredka v opravilu.</span><span class="sxs-lookup"><span data-stu-id="ffa1e-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="ffa1e-111">Oba pristopa povzročita ponoven izračun ETC, ocena končnih stroškov (EAC) in odstotka napredka ter predvidenega odmika od obsega dela v opravilu.</span><span class="sxs-lookup"><span data-stu-id="ffa1e-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="ffa1e-112">Ponovno se izračunajo EAC, ETC in odstotek napredka v opravilih povzetkov, kar ustvari novo projekcijo odmika od obsega dela.</span><span class="sxs-lookup"><span data-stu-id="ffa1e-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]