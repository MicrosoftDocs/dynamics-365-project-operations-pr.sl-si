---
title: Ustvarjanje rešitev po meri za cenovne razsežnosti
description: V tej temi je opisano, kako pri ustvarjanju cenovnih razsežnosti po meri ustvarite rešitev po meri.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084765"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="7549d-103">Ustvarjanje rešitev po meri za cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="7549d-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7549d-104">Vse spremembe cenovnih razsežnosti morajo biti v ločeni rešitvi.</span><span class="sxs-lookup"><span data-stu-id="7549d-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="7549d-105">Ta pomembna najboljša praksa zagotavlja nadaljnjo prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi, pomaga pri ponovni uporabi vašega dela in olajša prenos teh sprememb v drug primerek.</span><span class="sxs-lookup"><span data-stu-id="7549d-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="7549d-106">Ko naredite vse zahtevane spremembe, izvozite to rešitev kot **upravljano rešitev** in jo uvozite v druge primerke, da znova uporabite nastavitev cen.</span><span class="sxs-lookup"><span data-stu-id="7549d-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="7549d-107">Izberite **Nastavitve** > **Rešitve** in nato izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="7549d-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="7549d-108">Poimenujte rešitev **Cenovne razsežnosti za \<your organization name>** , vnesite ostale zahtevane podatke in izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="7549d-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![Ustvarjanje rešitve po meri za cenovne razsežnosti](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="7549d-110">Dodajanje vseh zahtevanih entitet in povezanih komponent v rešitev za cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="7549d-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="7549d-111">V svojo rešitev za določanje cen boste morali dodati spodnje entitete rešitve Project Service.</span><span class="sxs-lookup"><span data-stu-id="7549d-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="7549d-112">S koraki v tem postopku naredite nekaj pomembnih sprememb sheme v rešitvi za določanje cen, tako da se entitete seznanijo z novimi cenovnimi razsežnostmi.</span><span class="sxs-lookup"><span data-stu-id="7549d-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="7549d-113">Izberite **Nastavitve** > **Rešitve** , nato dvokliknite **\<your organization name> cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="7549d-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="7549d-114">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Dodaj obstoječe** > **Entitete**.</span><span class="sxs-lookup"><span data-stu-id="7549d-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="7549d-115">V pogovornem oknu **Komponente rešitve** izberite eno od teh entitet:</span><span class="sxs-lookup"><span data-stu-id="7549d-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="7549d-116">Dejansko</span><span class="sxs-lookup"><span data-stu-id="7549d-116">Actual</span></span>
- <span data-ttu-id="7549d-117">Vir, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="7549d-117">Bookable Resource</span></span>
- <span data-ttu-id="7549d-118">Vrstica ocene</span><span class="sxs-lookup"><span data-stu-id="7549d-118">Estimate Line</span></span>
- <span data-ttu-id="7549d-119">Projektno opravilo</span><span class="sxs-lookup"><span data-stu-id="7549d-119">Project Task</span></span>
- <span data-ttu-id="7549d-120">Podrobnosti vrstice računa</span><span class="sxs-lookup"><span data-stu-id="7549d-120">Invoice Line Detail</span></span>
- <span data-ttu-id="7549d-121">Vrstica dnevnika</span><span class="sxs-lookup"><span data-stu-id="7549d-121">Journal Line</span></span>
- <span data-ttu-id="7549d-122">Podrobnost vrstice projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="7549d-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="7549d-123">Član projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="7549d-123">Project Team Member</span></span>
- <span data-ttu-id="7549d-124">Podrobnosti vrstice ponudbe</span><span class="sxs-lookup"><span data-stu-id="7549d-124">Quote Line Detail</span></span>
- <span data-ttu-id="7549d-125">Pribitek na ceno vloge</span><span class="sxs-lookup"><span data-stu-id="7549d-125">Role Price Markup</span></span>
- <span data-ttu-id="7549d-126">Cena vloge</span><span class="sxs-lookup"><span data-stu-id="7549d-126">Role Price</span></span> 
- <span data-ttu-id="7549d-127">Časovni vnos</span><span class="sxs-lookup"><span data-stu-id="7549d-127">Time Entry</span></span> 

> ![Dodajanje obstoječih entitet v rešitev za cenovne razsežnosti](media/Existing-entities-to-PD-solution.png)

> ![Izbira komponent rešitve](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="7549d-130">Poskrbite, da boste vključili vse obrazce in poglede za posamezne izbrane entitete.</span><span class="sxs-lookup"><span data-stu-id="7549d-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="7549d-131">Ko ste pozvani, da vključite vse odvisne entitete za izbrane entitete, izberite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="7549d-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Ne vključi vseh povezanih komponent](media/Do-not-include-required.png)


