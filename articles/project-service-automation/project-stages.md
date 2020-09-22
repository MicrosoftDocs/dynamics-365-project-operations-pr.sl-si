---
title: Stopnje projekta
description: Ta tema vsebuje informacije o stopnjah projekta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755770"
---
# <a name="project-stages"></a><span data-ttu-id="572e0-103">Stopnje projekta</span><span class="sxs-lookup"><span data-stu-id="572e0-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="572e0-104">Stopnje projekta so posodobljene tako, da odražajo stanje projekta med napredkom.</span><span class="sxs-lookup"><span data-stu-id="572e0-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="572e0-105">Privzeti potek poslovnega procesa samodejno posodobi nekatere stopnje projekta, druge pa ročno posodobi vodja projekta.</span><span class="sxs-lookup"><span data-stu-id="572e0-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="572e0-106">V privzetem poteku poslovnega procesa so določene te stopnje:</span><span class="sxs-lookup"><span data-stu-id="572e0-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="572e0-107">Novo</span><span class="sxs-lookup"><span data-stu-id="572e0-107">New</span></span>
- <span data-ttu-id="572e0-108">Ponudba</span><span class="sxs-lookup"><span data-stu-id="572e0-108">Quote</span></span>
- <span data-ttu-id="572e0-109">Načrt</span><span class="sxs-lookup"><span data-stu-id="572e0-109">Plan</span></span>
- <span data-ttu-id="572e0-110">Dostava</span><span class="sxs-lookup"><span data-stu-id="572e0-110">Deliver</span></span>
- <span data-ttu-id="572e0-111">Dokončano</span><span class="sxs-lookup"><span data-stu-id="572e0-111">Complete</span></span>
- <span data-ttu-id="572e0-112">Zaprto</span><span class="sxs-lookup"><span data-stu-id="572e0-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="572e0-113">Novo</span><span class="sxs-lookup"><span data-stu-id="572e0-113">New</span></span>

<span data-ttu-id="572e0-114">Ko ustvarite projekt, je stopnja projekta nastavljena na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="572e0-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="572e0-115">Če je bil projekt ustvarjen iz predloge, ima morda podatke o razporedu, ocenah in ekipi.</span><span class="sxs-lookup"><span data-stu-id="572e0-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="572e0-116">V nasprotnem primeru je to samo oris projekta, preostale komponente pa morate vnesti sami.</span><span class="sxs-lookup"><span data-stu-id="572e0-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="572e0-117">Ponudba</span><span class="sxs-lookup"><span data-stu-id="572e0-117">Quote</span></span>

<span data-ttu-id="572e0-118">Ko povežete projekt s ponudbo ali ga ustvarite iz ponudbe, je stanje projekta nastavljeno na **Ponudba**, pri čemer se posodobita tudi predvidena začetni in končni datum.</span><span class="sxs-lookup"><span data-stu-id="572e0-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="572e0-119">Ko je projekt na stopnji **Ponudba**, so na zavihku **Prodaja** na strani **Entiteta projekta** prikazane podrobnosti ponudbe.</span><span class="sxs-lookup"><span data-stu-id="572e0-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="572e0-120">Načrt</span><span class="sxs-lookup"><span data-stu-id="572e0-120">Plan</span></span>

<span data-ttu-id="572e0-121">Ko je ponudba, ki je povezana s projektom, sprejeta, in se projekt premakne na stopnjo **Pogodba**, se stopnja projekta posodobi na stopnjo **Načrt**.</span><span class="sxs-lookup"><span data-stu-id="572e0-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="572e0-122">Ko je projekt na stopnji **Načrt**, so na strani **Entiteta projekta** prikazane podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="572e0-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="572e0-123">Dostava</span><span class="sxs-lookup"><span data-stu-id="572e0-123">Deliver</span></span>

<span data-ttu-id="572e0-124">Ko je načrt projekta dokončan in ste pripravljeni na zagon projekta, mora vodja projekta posodobiti stopnjo projekta na **Dostava**, da pokaže, da se je projekt začel.</span><span class="sxs-lookup"><span data-stu-id="572e0-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="572e0-125">Dokončano</span><span class="sxs-lookup"><span data-stu-id="572e0-125">Complete</span></span> 

<span data-ttu-id="572e0-126">Ko je delo za projekt končano, lahko vodja projekta posodobi stopnjo na **Dokončano**.</span><span class="sxs-lookup"><span data-stu-id="572e0-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="572e0-127">Ko vodja projekta posodobi stopnjo projekta na **Dokončano**, to pomeni, da je delo 100-odstotno dokončano, vendar je projekt še vedno odprt, tako da je mogoče zabeležiti vse čakajoče časovne vnose ali vnose stroškov.</span><span class="sxs-lookup"><span data-stu-id="572e0-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="572e0-128">Zaprto</span><span class="sxs-lookup"><span data-stu-id="572e0-128">Close</span></span>

<span data-ttu-id="572e0-129">Ko so za projekt zabeležene vse transakcije, lahko vodja projekta posodobi stopnjo na **Zaprto**.</span><span class="sxs-lookup"><span data-stu-id="572e0-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="572e0-130">Na tej točki ni več mogoče beležiti transakcij in projekt je nastavljen na način samo za branje.</span><span class="sxs-lookup"><span data-stu-id="572e0-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
