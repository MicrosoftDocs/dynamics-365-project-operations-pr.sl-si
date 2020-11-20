---
title: Ustvarjanje polj in entitet po meri kot cenovnih razsežnosti
description: Ta tema vsebuje informacije o tem, kako ustvariti nabore možnosti ali entitete po meri.
author: rumant
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
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130913"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="59c57-103">Ustvarjanje polj in entitet po meri kot cenovnih razsežnosti</span><span class="sxs-lookup"><span data-stu-id="59c57-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="59c57-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="59c57-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="59c57-105">Če želite ustvariti nabor možnosti ali entiteto po meri, upoštevajte spodnje korake.</span><span class="sxs-lookup"><span data-stu-id="59c57-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59c57-106">Priporočamo, da vse cenovne razsežnosti po meri spremenite v ločeni rešitvi.</span><span class="sxs-lookup"><span data-stu-id="59c57-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="59c57-107">Ta pomembna najboljša praksa zagotavlja nadaljnjo prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi, pomaga pri ponovni uporabi vašega dela in olajša prenos teh sprememb v drug primerek.</span><span class="sxs-lookup"><span data-stu-id="59c57-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="59c57-108">Ko naredite vse zahtevane spremembe, izvozite to rešitev kot **upravljano rešitev** in jo uvozite v druge primerke, da znova uporabite nastavitev cen.</span><span class="sxs-lookup"><span data-stu-id="59c57-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="59c57-109">Ustvarjanje rešitve po meri za cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="59c57-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="59c57-110">Odprite **Nastavitve** > **Rešitve** in nato izberite **Novo**, da ustvarite novo rešitev.</span><span class="sxs-lookup"><span data-stu-id="59c57-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="59c57-111">Poimenujte rešitev **Cenovne razsežnosti za \<your organization name>**, vnesite ostale zahtevane podatke in izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="59c57-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="59c57-112">Ustvarjanje polj po meri in naborov možnosti v rešitvi za cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="59c57-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="59c57-113">Cenovna razsežnost je lahko nabor možnosti ali entiteta.</span><span class="sxs-lookup"><span data-stu-id="59c57-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="59c57-114">Oboje morate ustvariti v svoji rešitvi za določanje cen.</span><span class="sxs-lookup"><span data-stu-id="59c57-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="59c57-115">Koraki v tem postopku pojasnjujejo, kako ustvarite razsežnosti, ki temeljijo na entiteti, in razsežnosti, ki temeljijo na naboru možnosti.</span><span class="sxs-lookup"><span data-stu-id="59c57-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="59c57-116">Razsežnosti na osnovi entitete</span><span class="sxs-lookup"><span data-stu-id="59c57-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="59c57-117">Odprite **Nastavitve** > **Rešitve**, nato dvokliknite **\<your organization name> cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="59c57-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="59c57-118">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete**.</span><span class="sxs-lookup"><span data-stu-id="59c57-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="59c57-119">Izberite **Novo**, da ustvarite novo entiteto **Standardni naziv**.</span><span class="sxs-lookup"><span data-stu-id="59c57-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="59c57-120">Vnesite ostale zahtevane informacije in nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="59c57-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="59c57-121">Razsežnosti na osnovi nabora možnosti</span><span class="sxs-lookup"><span data-stu-id="59c57-121">Option set-based dimensions</span></span> 
<span data-ttu-id="59c57-122">Ustvarite lahko dve razsežnosti na osnovi nabora možnosti.</span><span class="sxs-lookup"><span data-stu-id="59c57-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="59c57-123">Uporabite **Lokacija dela vira**, da sledite ceni za lokacijo dela **Doma** in **Na lokaciji**, ter **Delovni čas vira** z vrednostmi **Redno** in **Nadure**, da uporabite pribitek, ko je delo končano.</span><span class="sxs-lookup"><span data-stu-id="59c57-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="59c57-124">Odprite **Nastavitve** > **Rešitve**, nato dvokliknite **\<your organization name> cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="59c57-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="59c57-125">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Nabori možnosti**.</span><span class="sxs-lookup"><span data-stu-id="59c57-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="59c57-126">Izberite **Novo**, da ustvarite nov nabor možnosti, vnesite ostale zahtevane podatke in nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="59c57-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="59c57-127">Ustvarjanje podatkov za razsežnosti na osnovi entitete</span><span class="sxs-lookup"><span data-stu-id="59c57-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="59c57-128">Podatke za razsežnosti na osnovi entitete lahko ustvarite ročno ali z uvozom v aplikaciji Microsoft Excel oz. s klici storitve.</span><span class="sxs-lookup"><span data-stu-id="59c57-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="59c57-129">Uporabite korake v tem postopku, da iz razsežnosti na osnovi entitete **Standardni naziv** ustvarite dva standardna naziva, in sicer **Sistemski inženir** in **Višji sistemi inženir**.</span><span class="sxs-lookup"><span data-stu-id="59c57-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="59c57-130">Če je količina podatkov, ki jih želite ustvariti, majhna, kot v spodnjem primeru, lahko uporabite standardni obrazec.</span><span class="sxs-lookup"><span data-stu-id="59c57-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="59c57-131">Izberite **Napredno iskanje**, izberite entiteto **Standardni naslov** in nato izberite **Rezultati**.</span><span class="sxs-lookup"><span data-stu-id="59c57-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="59c57-132">Prikazane bodo vse vrstice v entiteti **Standardni naziv**.</span><span class="sxs-lookup"><span data-stu-id="59c57-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="59c57-133">Izberite **Novo** in v polje **Ime** vnesite »Sistemski inženir« in nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="59c57-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="59c57-134">Zaprite obrazec.</span><span class="sxs-lookup"><span data-stu-id="59c57-134">Close the form.</span></span> 
4. <span data-ttu-id="59c57-135">Ponovite korake od 1 do 3, da ustvarite drug standardni naziv za »Višji sistemski inženir«.</span><span class="sxs-lookup"><span data-stu-id="59c57-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="59c57-136">Dodajanje vseh zahtevanih entitet in povezanih komponent v rešitev za cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="59c57-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="59c57-137">V svojo rešitev za določanje cen boste morali dodati spodnje entitete.</span><span class="sxs-lookup"><span data-stu-id="59c57-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="59c57-138">S koraki v tem postopku naredite nekaj pomembnih sprememb sheme v rešitvi za določanje cen, tako da se entitete seznanijo z novimi cenovnimi razsežnostmi.</span><span class="sxs-lookup"><span data-stu-id="59c57-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="59c57-139">Izberite **Nastavitve** > **Rešitve**, nato dvokliknite **\<your organization name> cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="59c57-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="59c57-140">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Dodaj obstoječe** > **Entitete**.</span><span class="sxs-lookup"><span data-stu-id="59c57-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="59c57-141">V pogovornem oknu **Komponente rešitve** izberite eno od teh entitet:</span><span class="sxs-lookup"><span data-stu-id="59c57-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="59c57-142">Dejansko</span><span class="sxs-lookup"><span data-stu-id="59c57-142">Actual</span></span>
  - <span data-ttu-id="59c57-143">Vir, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="59c57-143">Bookable Resource</span></span>
  - <span data-ttu-id="59c57-144">Vrstica ocene</span><span class="sxs-lookup"><span data-stu-id="59c57-144">Estimate Line</span></span>
  - <span data-ttu-id="59c57-145">Podrobnosti vrstice računa</span><span class="sxs-lookup"><span data-stu-id="59c57-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="59c57-146">Vrstica dnevnika</span><span class="sxs-lookup"><span data-stu-id="59c57-146">Journal Line</span></span>
  - <span data-ttu-id="59c57-147">Podrobnost vrstice projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="59c57-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="59c57-148">Član projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="59c57-148">Project Team Member</span></span>
  - <span data-ttu-id="59c57-149">Podrobnosti vrstice ponudbe</span><span class="sxs-lookup"><span data-stu-id="59c57-149">Quote Line Detail</span></span>
  - <span data-ttu-id="59c57-150">Pribitek na ceno vloge</span><span class="sxs-lookup"><span data-stu-id="59c57-150">Role Price Markup</span></span>
  - <span data-ttu-id="59c57-151">Cena vloge</span><span class="sxs-lookup"><span data-stu-id="59c57-151">Role Price</span></span> 
  - <span data-ttu-id="59c57-152">Časovni vnos</span><span class="sxs-lookup"><span data-stu-id="59c57-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="59c57-153">Poskrbite, da boste vključili vse obrazce in poglede za posamezne izbrane entitete.</span><span class="sxs-lookup"><span data-stu-id="59c57-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="59c57-154">Ko ste pozvani, da vključite vse odvisne entitete za zgoraj izbrane entitete, izberite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="59c57-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

