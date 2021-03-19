---
title: Stopnje projekta
description: Ta tema vsebuje informacije o stopnjah projekta, ki so na voljo v storitvi Microsoft Dynamics Project Operations.
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286808"
---
# <a name="project-stages"></a><span data-ttu-id="70ef8-103">Stopnje projekta</span><span class="sxs-lookup"><span data-stu-id="70ef8-103">Project stages</span></span>

<span data-ttu-id="70ef8-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="70ef8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="70ef8-105">Stopnje projekta so zasnovane tako, da odražajo stanje projekta med napredkom.</span><span class="sxs-lookup"><span data-stu-id="70ef8-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="70ef8-106">Prilagoditve lahko uporabite za samodejno posodabljanje faz s poteki poslovnih procesov, storitvijo Power Automate ali razširitvami vtičnikov.</span><span class="sxs-lookup"><span data-stu-id="70ef8-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="70ef8-107">V privzetem poteku poslovnega procesa so določene te stopnje:</span><span class="sxs-lookup"><span data-stu-id="70ef8-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="70ef8-108">Nova</span><span class="sxs-lookup"><span data-stu-id="70ef8-108">New</span></span>
- <span data-ttu-id="70ef8-109">Citat</span><span class="sxs-lookup"><span data-stu-id="70ef8-109">Quote</span></span>
- <span data-ttu-id="70ef8-110">Paket</span><span class="sxs-lookup"><span data-stu-id="70ef8-110">Plan</span></span>
- <span data-ttu-id="70ef8-111">Dostavi</span><span class="sxs-lookup"><span data-stu-id="70ef8-111">Deliver</span></span>
- <span data-ttu-id="70ef8-112">Popolno</span><span class="sxs-lookup"><span data-stu-id="70ef8-112">Complete</span></span>
- <span data-ttu-id="70ef8-113">Zaprto</span><span class="sxs-lookup"><span data-stu-id="70ef8-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="70ef8-114">Nova</span><span class="sxs-lookup"><span data-stu-id="70ef8-114">New</span></span>

<span data-ttu-id="70ef8-115">Ko ustvarite projekt, je stopnja projekta nastavljena na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="70ef8-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="70ef8-116">Če je bil projekt ustvarjen iz predloge, ima morda podatke o razporedu, ocenah in ekipi.</span><span class="sxs-lookup"><span data-stu-id="70ef8-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="70ef8-117">V nasprotnem primeru je to oris projekta, preostale komponente pa morate vnesti sami.</span><span class="sxs-lookup"><span data-stu-id="70ef8-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="70ef8-118">Ponudba</span><span class="sxs-lookup"><span data-stu-id="70ef8-118">Quote</span></span>

<span data-ttu-id="70ef8-119">Ko povežete projekt s ponudbo ali ga ustvarite iz ponudbe, je stanje projekta nastavljeno na **Ponudba**, pri čemer se posodobita tudi predvidena začetni in končni datum.</span><span class="sxs-lookup"><span data-stu-id="70ef8-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="70ef8-120">Ko je projekt na stopnji **Ponudba**, so na zavihku **Prodaja** na strani **Entiteta projekta** prikazane podrobnosti ponudbe.</span><span class="sxs-lookup"><span data-stu-id="70ef8-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="70ef8-121">Načrt</span><span class="sxs-lookup"><span data-stu-id="70ef8-121">Plan</span></span>

<span data-ttu-id="70ef8-122">Ko je ponudba, ki je povezana s projektom, sprejeta, in se projekt premakne na stopnjo **Pogodba**, se stopnja projekta posodobi na stopnjo **Načrt**.</span><span class="sxs-lookup"><span data-stu-id="70ef8-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="70ef8-123">Ko je projekt na stopnji **Načrt**, so na strani **Entiteta projekta** prikazane podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="70ef8-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="70ef8-124">Dostava</span><span class="sxs-lookup"><span data-stu-id="70ef8-124">Deliver</span></span>

<span data-ttu-id="70ef8-125">Ko je načrt projekta dokončan in ste pripravljeni na zagon projekta, mora vodja projekta posodobiti stopnjo projekta na **Dostava**, da pokaže, da se je projekt začel.</span><span class="sxs-lookup"><span data-stu-id="70ef8-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="70ef8-126">Dokončano</span><span class="sxs-lookup"><span data-stu-id="70ef8-126">Complete</span></span> 

<span data-ttu-id="70ef8-127">Ko je delo za projekt končano, lahko vodja projekta posodobi stopnjo na **Dokončano**.</span><span class="sxs-lookup"><span data-stu-id="70ef8-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="70ef8-128">Ko vodja projekta posodobi stopnjo projekta na **Dokončano**, to pomeni, da je delo 100-odstotno dokončano, vendar je projekt še vedno odprt, tako da je mogoče zabeležiti vse čakajoče časovne vnose ali vnose stroškov.</span><span class="sxs-lookup"><span data-stu-id="70ef8-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="70ef8-129">Zaprto</span><span class="sxs-lookup"><span data-stu-id="70ef8-129">Close</span></span>

<span data-ttu-id="70ef8-130">Ko so za projekt zabeležene vse transakcije, lahko vodja projekta posodobi stopnjo na **Zaprto**.</span><span class="sxs-lookup"><span data-stu-id="70ef8-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="70ef8-131">Na tej točki ni več mogoče beležiti transakcij in projekt je nastavljen na način samo za branje.</span><span class="sxs-lookup"><span data-stu-id="70ef8-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]