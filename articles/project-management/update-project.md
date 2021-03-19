---
title: Posodobitev projekta
description: Ta tema vsebuje informacije o posodabljanju projektov v aplikacij Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286403"
---
# <a name="update-a-project"></a><span data-ttu-id="4bd84-103">Posodobitev projekta</span><span class="sxs-lookup"><span data-stu-id="4bd84-103">Update a project</span></span>

<span data-ttu-id="4bd84-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="4bd84-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4bd84-105">Spodaj je povzetek polj, ki jih je mogoče po projektu posodobiti, in morebitne posledice posodobitev.</span><span class="sxs-lookup"><span data-stu-id="4bd84-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="4bd84-106">Polja s predvidenimi vrednostmi projekta</span><span class="sxs-lookup"><span data-stu-id="4bd84-106">Project detail fields</span></span>

- <span data-ttu-id="4bd84-107">**Ime**: ime projekta.</span><span class="sxs-lookup"><span data-stu-id="4bd84-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="4bd84-108">**Opis**: pregled projekta.</span><span class="sxs-lookup"><span data-stu-id="4bd84-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="4bd84-109">**Stranka**: podjetje, ki mu bo projekt dostavljen.</span><span class="sxs-lookup"><span data-stu-id="4bd84-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="4bd84-110">**Predloga koledarja**: delovni čas projekta.</span><span class="sxs-lookup"><span data-stu-id="4bd84-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="4bd84-111">Ko se polje spremeni, se celotni urnik preračuna.</span><span class="sxs-lookup"><span data-stu-id="4bd84-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="4bd84-112">**Valuta**: valuto za projekt.</span><span class="sxs-lookup"><span data-stu-id="4bd84-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="4bd84-113">To polje privzeto temelji na valuti, določeni v pogodbeni enoti.</span><span class="sxs-lookup"><span data-stu-id="4bd84-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="4bd84-114">Ko se pogodbena enota posodobi, se posodobi tudi polje.</span><span class="sxs-lookup"><span data-stu-id="4bd84-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="4bd84-115">**Pogodbena enota**: organizacijska enota, ki predstavlja skupino ali oddelek podjetja, ki je primarno odgovoren za izvedbo prodaje in upravljanje zagotavljanja dela in storitev za stranke.</span><span class="sxs-lookup"><span data-stu-id="4bd84-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="4bd84-116">**Vodja projekta**: član projektne skupine, ki je pooblaščen za pregled in odobritev časovnih vnosov in stroškov.</span><span class="sxs-lookup"><span data-stu-id="4bd84-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="4bd84-117">Polja s predvidenimi vrednostmi</span><span class="sxs-lookup"><span data-stu-id="4bd84-117">Estimate fields</span></span>

- <span data-ttu-id="4bd84-118">**Predvideni datum začetka**: datum začetka projekta.</span><span class="sxs-lookup"><span data-stu-id="4bd84-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="4bd84-119">Ko se to polje posodobi, se bodo vsa opravila v projektu sorazmerno premaknila glede na nov datum začetka.</span><span class="sxs-lookup"><span data-stu-id="4bd84-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="4bd84-120">**Datum zaključka**: datum zaključka projekta.</span><span class="sxs-lookup"><span data-stu-id="4bd84-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="4bd84-121">**Obseg dela**: predviden obseg dela.</span><span class="sxs-lookup"><span data-stu-id="4bd84-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="4bd84-122">Ko so opravila dodana projektu, tega polja ni več mogoče urejati.</span><span class="sxs-lookup"><span data-stu-id="4bd84-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="4bd84-123">**Predvideni stroški dela**: predvideni stroški dela za projekt.</span><span class="sxs-lookup"><span data-stu-id="4bd84-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="4bd84-124">Ko so stroški dela dodani projektu, tega polja ni več mogoče urejati.</span><span class="sxs-lookup"><span data-stu-id="4bd84-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="4bd84-125">**Predvideni stroški**: predvideni stroški projekta.</span><span class="sxs-lookup"><span data-stu-id="4bd84-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="4bd84-126">Ko so stroški dodani projektu, tega polja ni več mogoče urejati.</span><span class="sxs-lookup"><span data-stu-id="4bd84-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="4bd84-127">Dejanska polja projekta</span><span class="sxs-lookup"><span data-stu-id="4bd84-127">Project actual fields</span></span>
- <span data-ttu-id="4bd84-128">**Dejanski začetek**: datum začetka projekta.</span><span class="sxs-lookup"><span data-stu-id="4bd84-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="4bd84-129">**Dejanski zaključek**: se posodobi po zaključku projekta.</span><span class="sxs-lookup"><span data-stu-id="4bd84-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="4bd84-130">Polja stanja projekta</span><span class="sxs-lookup"><span data-stu-id="4bd84-130">Project status fields</span></span>

- <span data-ttu-id="4bd84-131">**Splošno stanje projekta**: splošno stanje projekta, ki ga zagotavlja vodja projekta.</span><span class="sxs-lookup"><span data-stu-id="4bd84-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="4bd84-132">**Komentarji**: komentarji o trenutnem stanju projekta, ki jih zagotovi vodja projekta.</span><span class="sxs-lookup"><span data-stu-id="4bd84-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]