---
title: Ustvarjanje rešitve za cenovne razsežnosti po meri
description: Ta tema vsebuje informacije o ustvarjanju rešitev za cenovne razsežnosti po meri.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278438"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="d83ec-103">Ustvarjanje rešitve za cenovne razsežnosti po meri</span><span class="sxs-lookup"><span data-stu-id="d83ec-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="d83ec-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="d83ec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="d83ec-105">Vse spremembe cenovnih razsežnosti morajo biti v ločeni rešitvi.</span><span class="sxs-lookup"><span data-stu-id="d83ec-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="d83ec-106">Ta pomembna najboljša praksa omogoča prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi, pomaga pri ponovni uporabi vašega dela in olajša prenos teh sprememb v druge primerke.</span><span class="sxs-lookup"><span data-stu-id="d83ec-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="d83ec-107">Ko naredite vse zahtevane spremembe, izvozite to rešitev kot **Upravljano** rešitev in jo nato uvozite še v druge primerke za ponovno uporabo.</span><span class="sxs-lookup"><span data-stu-id="d83ec-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="d83ec-108">Ustvarjanje rešitve za cenovne razsežnosti po meri</span><span class="sxs-lookup"><span data-stu-id="d83ec-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="d83ec-109">Izberite **Nastavitve** > **Rešitve** in nato izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="d83ec-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="d83ec-110">Poimenujte rešitev *Cenovne razsežnosti <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="d83ec-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="d83ec-111">Vnesite ostale zahtevane informacije in nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="d83ec-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Ustvarjanje rešitve za cenovne razsežnosti po meri](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="d83ec-113">Dodajanje vseh zahtevanih entitet in povezanih komponent v rešitev za cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="d83ec-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="d83ec-114">V rešitev za določanje cen dodajte naslednje entitete storitve Project Service, da boste v rešitev za določanje cen lahko uvedli pomembne spremembe sheme.</span><span class="sxs-lookup"><span data-stu-id="d83ec-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="d83ec-115">Ko boste dokončali ta postopek, bodo entitete prepoznale nove cenovne razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="d83ec-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="d83ec-116">Kliknite **Nastavitve** > **Rešitve** in nato dvokliknite **<*ime vaše organizacije*> cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="d83ec-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="d83ec-117">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Dodaj obstoječe** > **Entitete**.</span><span class="sxs-lookup"><span data-stu-id="d83ec-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="d83ec-118">V pogovornem oknu **Komponente rešitve** izberite eno od teh entitet:</span><span class="sxs-lookup"><span data-stu-id="d83ec-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="d83ec-119">**Dejansko**</span><span class="sxs-lookup"><span data-stu-id="d83ec-119">**Actual**</span></span>
   - <span data-ttu-id="d83ec-120">**Vir, ki ga je mogoče rezervirati**</span><span class="sxs-lookup"><span data-stu-id="d83ec-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="d83ec-121">**Vrstica ocene**</span><span class="sxs-lookup"><span data-stu-id="d83ec-121">**Estimate Line**</span></span>
   - <span data-ttu-id="d83ec-122">**Projektno opravilo**</span><span class="sxs-lookup"><span data-stu-id="d83ec-122">**Project Task**</span></span>
   - <span data-ttu-id="d83ec-123">**Podrobnosti vrstice računa**</span><span class="sxs-lookup"><span data-stu-id="d83ec-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="d83ec-124">**Vrstica dnevnika**</span><span class="sxs-lookup"><span data-stu-id="d83ec-124">**Journal Line**</span></span>
   - <span data-ttu-id="d83ec-125">**Podrobnost vrstice projektne pogodbe**</span><span class="sxs-lookup"><span data-stu-id="d83ec-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="d83ec-126">**Član projektne ekipe**</span><span class="sxs-lookup"><span data-stu-id="d83ec-126">**Project Team Member**</span></span>
   - <span data-ttu-id="d83ec-127">**Podrobnosti vrstice ponudbe**</span><span class="sxs-lookup"><span data-stu-id="d83ec-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="d83ec-128">**Pribitek na ceno vloge**</span><span class="sxs-lookup"><span data-stu-id="d83ec-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="d83ec-129">**Cena vloge**</span><span class="sxs-lookup"><span data-stu-id="d83ec-129">**Role Price**</span></span>
   - <span data-ttu-id="d83ec-130">**Časovni vnos**</span><span class="sxs-lookup"><span data-stu-id="d83ec-130">**Time Entry**</span></span>
 
   ![Dodajanje obstoječih entitet po meri v rešitev za cenovne razsežnosti](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="d83ec-132">Za vsako entiteto preglejte komponente, ki jih dodajate, in končni seznam sredstev za vsako entiteto.</span><span class="sxs-lookup"><span data-stu-id="d83ec-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="d83ec-133">Vključite vse obrazce in poglede za posamezne izbrane entitete.</span><span class="sxs-lookup"><span data-stu-id="d83ec-133">Include all forms and views for each of the selected entities.</span></span>

  ![Dodane entitete](./media/solution-component-selection.png)


5.  <span data-ttu-id="d83ec-135">Ko boste pozvani, da v izbrane entitete vključite vse odvisne entitete, izberite **Ne, ne vključi obveznih komponent.**</span><span class="sxs-lookup"><span data-stu-id="d83ec-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Vključno z odvisnimi entitetami](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]