---
title: Ustvarjanje ponudb za projekte iz priložnosti
description: V tej temi najdete informacije o ustvarjanju ponudbe za projekt iz priložnosti.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084668"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="25c9a-103">Ustvarjanje ponudb za projekte iz priložnosti</span><span class="sxs-lookup"><span data-stu-id="25c9a-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="25c9a-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="25c9a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="25c9a-105">Ponudbe je mogoče ustvariti iz priložnosti za projekte na naslednje načine:</span><span class="sxs-lookup"><span data-stu-id="25c9a-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="25c9a-106">V zavihku **Ponudbe** na strani **Priložnost za projekt**</span><span class="sxs-lookup"><span data-stu-id="25c9a-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="25c9a-107">Iz poteka prodajnega postopka za priložnost</span><span class="sxs-lookup"><span data-stu-id="25c9a-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="25c9a-108">S posodobitvijo sklica priložnosti pri obstoječi ponudbi</span><span class="sxs-lookup"><span data-stu-id="25c9a-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="25c9a-109">V zavihku Ponudbe na strani Priložnost za projekt</span><span class="sxs-lookup"><span data-stu-id="25c9a-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="25c9a-110">Če želite iz priložnosti ustvariti ponudbo za projekt, upoštevajte naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="25c9a-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="25c9a-111">Odprite stran **Priložnost za projekt** in izberite zavihek **Ponudbe**.</span><span class="sxs-lookup"><span data-stu-id="25c9a-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="25c9a-112">Na podmreži **Ponudbe** izberite **+** , da na podlagi priložnosti ustvarite ponudbo za nov projekt.</span><span class="sxs-lookup"><span data-stu-id="25c9a-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="25c9a-113">Vse vrstice priložnosti in z njimi povezani ceniki za projekte se kopirajo v novo ponudbo iz priložnosti.</span><span class="sxs-lookup"><span data-stu-id="25c9a-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="25c9a-114">Iz poteka prodajnega postopka za priložnost</span><span class="sxs-lookup"><span data-stu-id="25c9a-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="25c9a-115">Če želite iz poteka prodajnega postopka za priložnost ustvariti ponudbo, upoštevajte naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="25c9a-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="25c9a-116">Pri poteku prodajnega postopka za priložnost odprite priložnost.</span><span class="sxs-lookup"><span data-stu-id="25c9a-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="25c9a-117">Izberite stopnjo **Potrdi**.</span><span class="sxs-lookup"><span data-stu-id="25c9a-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="25c9a-118">Izberite **Naprej** in nato izberite **+ Ustvari** , da ustvarite novo ponudbo.</span><span class="sxs-lookup"><span data-stu-id="25c9a-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="25c9a-119">Večina informacij na zavihku **Povzetek** za to novo ponudbo bo privzeto nastavljenih prek priložnosti.</span><span class="sxs-lookup"><span data-stu-id="25c9a-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="25c9a-120">Vnesite morebitne zahtevane podatke, ki manjkajo, ali po potrebi posodobite privzete vrednosti na zavihku **Povzetek**.</span><span class="sxs-lookup"><span data-stu-id="25c9a-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="25c9a-121">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="25c9a-121">Select **Save**.</span></span> <span data-ttu-id="25c9a-122">Nova ponudba se ustvari in poveže s priložnostjo.</span><span class="sxs-lookup"><span data-stu-id="25c9a-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="25c9a-123">Zdaj si lahko ogledate podatke o ponudbi na zavihku **Ponudbe** na strani **Priložnost**.</span><span class="sxs-lookup"><span data-stu-id="25c9a-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="25c9a-124">Prodajni postopek za priložnost preide na naslednjo stopnjo: **Predlagaj**.</span><span class="sxs-lookup"><span data-stu-id="25c9a-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="25c9a-125">S posodobitvijo sklica priložnosti pri obstoječi ponudbi</span><span class="sxs-lookup"><span data-stu-id="25c9a-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="25c9a-126">Obstoječo ponudbo lahko povežete s priložnostjo.</span><span class="sxs-lookup"><span data-stu-id="25c9a-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="25c9a-127">Upoštevajte naslednje korake za posodobitev podatkov o priložnosti pri obstoječi ponudbi.</span><span class="sxs-lookup"><span data-stu-id="25c9a-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="25c9a-128">Odprite stran **Ponudba** in izberite zavihek **Povzetek**.</span><span class="sxs-lookup"><span data-stu-id="25c9a-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="25c9a-129">V polju **Priložnost** izberite priložnost, ki jo želite povezati s ponudbo.</span><span class="sxs-lookup"><span data-stu-id="25c9a-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="25c9a-130">Ponudbo si lahko ogledate na mreži **Ponudbe** priložnosti.</span><span class="sxs-lookup"><span data-stu-id="25c9a-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="25c9a-131">S prodajnim postopkom za priložnost lahko priložnost premaknete na naslednjo stopnjo: **Predlagaj**.</span><span class="sxs-lookup"><span data-stu-id="25c9a-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="25c9a-132">Ko priložnost premaknete na to stopnjo, lahko to ponudbo izberete s seznama ponudb, povezanih s to priložnostjo.</span><span class="sxs-lookup"><span data-stu-id="25c9a-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="25c9a-133">Izbira te ponudbe pomeni, da jo boste v nadaljevanju postopka uporabljali še naprej.</span><span class="sxs-lookup"><span data-stu-id="25c9a-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="25c9a-134">Vse druge ponudbe, povezane s priložnostjo, bodo še vedno na voljo in bodo aktivne, dokler ne pridobite ene od njih.</span><span class="sxs-lookup"><span data-stu-id="25c9a-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="25c9a-135">Prodajni postopek lahko premaknete nazaj na prejšnjo stopnjo **Potrdi** in izberete drugo ponudbo, s katero želite nadaljevati.</span><span class="sxs-lookup"><span data-stu-id="25c9a-135">You can move the sales process back to the previous stage **Qualify** , and pick another quote to move forward with.</span></span>
