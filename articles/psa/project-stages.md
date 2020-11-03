---
title: Vrste stopenj projekta
description: Ta tema vsebuje informacije o stopnjah projekta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 521bf4b3090473a603626a99fded53906b644a7a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084807"
---
# <a name="project-stage-types"></a><span data-ttu-id="217fd-103">Vrste stopenj projekta</span><span class="sxs-lookup"><span data-stu-id="217fd-103">Project stage types</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="217fd-104">Stopnje projekta so zasnovane tako, da odražajo stanje projekta med napredkom.</span><span class="sxs-lookup"><span data-stu-id="217fd-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="217fd-105">Prilagoditve lahko uporabite za samodejno posodabljanje faz s poteki poslovnih procesov, storitvijo Power Automate ali razširitvami vtičnikov.</span><span class="sxs-lookup"><span data-stu-id="217fd-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="217fd-106">V privzetem poteku poslovnega procesa so določene te stopnje:</span><span class="sxs-lookup"><span data-stu-id="217fd-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="217fd-107">Nova</span><span class="sxs-lookup"><span data-stu-id="217fd-107">New</span></span>
- <span data-ttu-id="217fd-108">Citat</span><span class="sxs-lookup"><span data-stu-id="217fd-108">Quote</span></span>
- <span data-ttu-id="217fd-109">Načrt</span><span class="sxs-lookup"><span data-stu-id="217fd-109">Plan</span></span>
- <span data-ttu-id="217fd-110">Dostava</span><span class="sxs-lookup"><span data-stu-id="217fd-110">Deliver</span></span>
- <span data-ttu-id="217fd-111">Dokončano</span><span class="sxs-lookup"><span data-stu-id="217fd-111">Complete</span></span>
- <span data-ttu-id="217fd-112">Zaprto</span><span class="sxs-lookup"><span data-stu-id="217fd-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="217fd-113">Novo</span><span class="sxs-lookup"><span data-stu-id="217fd-113">New</span></span>

<span data-ttu-id="217fd-114">Ko ustvarite projekt, je stopnja projekta nastavljena na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="217fd-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="217fd-115">Če je bil projekt ustvarjen iz predloge, ima morda podatke o razporedu, ocenah in ekipi.</span><span class="sxs-lookup"><span data-stu-id="217fd-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="217fd-116">V nasprotnem primeru je to samo oris projekta, preostale komponente pa morate vnesti sami.</span><span class="sxs-lookup"><span data-stu-id="217fd-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="217fd-117">Ponudba</span><span class="sxs-lookup"><span data-stu-id="217fd-117">Quote</span></span>

<span data-ttu-id="217fd-118">Ko povežete projekt s ponudbo ali ga ustvarite iz ponudbe, je stanje projekta nastavljeno na **Ponudba** , pri čemer se posodobita tudi predvidena začetni in končni datum.</span><span class="sxs-lookup"><span data-stu-id="217fd-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote** , and the estimated start and end dates are updated.</span></span> <span data-ttu-id="217fd-119">Ko je projekt na stopnji **Ponudba** , so na zavihku **Prodaja** na strani **Entiteta projekta** prikazane podrobnosti ponudbe.</span><span class="sxs-lookup"><span data-stu-id="217fd-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="217fd-120">Načrt</span><span class="sxs-lookup"><span data-stu-id="217fd-120">Plan</span></span>

<span data-ttu-id="217fd-121">Ko je ponudba, ki je povezana s projektom, sprejeta, in se projekt premakne na stopnjo **Pogodba** , se stopnja projekta posodobi na stopnjo **Načrt**.</span><span class="sxs-lookup"><span data-stu-id="217fd-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="217fd-122">Ko je projekt na stopnji **Načrt** , so na strani **Entiteta projekta** prikazane podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="217fd-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="217fd-123">Dostava</span><span class="sxs-lookup"><span data-stu-id="217fd-123">Deliver</span></span>

<span data-ttu-id="217fd-124">Ko je načrt projekta dokončan in ste pripravljeni na zagon projekta, mora vodja projekta posodobiti stopnjo projekta na **Dostava** , da pokaže, da se je projekt začel.</span><span class="sxs-lookup"><span data-stu-id="217fd-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="217fd-125">Dokončano</span><span class="sxs-lookup"><span data-stu-id="217fd-125">Complete</span></span> 

<span data-ttu-id="217fd-126">Ko je delo za projekt končano, lahko vodja projekta posodobi stopnjo na **Dokončano**.</span><span class="sxs-lookup"><span data-stu-id="217fd-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="217fd-127">Ko vodja projekta posodobi stopnjo projekta na **Dokončano** , to pomeni, da je delo 100-odstotno dokončano, vendar je projekt še vedno odprt, tako da je mogoče zabeležiti vse čakajoče časovne vnose ali vnose stroškov.</span><span class="sxs-lookup"><span data-stu-id="217fd-127">By updating the project stage to **Complete** , the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="217fd-128">Zaprto</span><span class="sxs-lookup"><span data-stu-id="217fd-128">Close</span></span>

<span data-ttu-id="217fd-129">Ko so za projekt zabeležene vse transakcije, lahko vodja projekta posodobi stopnjo na **Zaprto**.</span><span class="sxs-lookup"><span data-stu-id="217fd-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="217fd-130">Na tej točki ni več mogoče beležiti transakcij in projekt je nastavljen na način samo za branje.</span><span class="sxs-lookup"><span data-stu-id="217fd-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
