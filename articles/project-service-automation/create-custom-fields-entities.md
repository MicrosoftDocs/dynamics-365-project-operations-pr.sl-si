---
title: Ustvarjanje polj in entitet po meri
description: V tej temi je pojasnjeno, kako ustvarite nabor možnosti in entitete v svoji rešitvi v platformi Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755861"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="ccad2-103">Ustvarjanje polj in entitet po meri</span><span class="sxs-lookup"><span data-stu-id="ccad2-103">Create custom fields and entities</span></span> 

<span data-ttu-id="ccad2-104">Če želite ustvariti nabor možnosti ali entiteto po meri v platformi Power Apps, upoštevajte spodnje korake.</span><span class="sxs-lookup"><span data-stu-id="ccad2-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="ccad2-105">Postopke v tej temi morate izvesti s spletnim vmesnikom aplikacije Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="ccad2-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ccad2-106">Priporočamo, da vse cenovne razsežnosti po meri spremenite v ločeni rešitvi.</span><span class="sxs-lookup"><span data-stu-id="ccad2-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="ccad2-107">Ta pomembna najboljša praksa zagotavlja nadaljnjo prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi, pomaga pri ponovni uporabi vašega dela in olajša prenos teh sprememb v drug primerek.</span><span class="sxs-lookup"><span data-stu-id="ccad2-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="ccad2-108">Ko naredite vse zahtevane spremembe, izvozite to rešitev kot **upravljano rešitev** in jo uvozite v druge primerke, da znova uporabite nastavitev cen.</span><span class="sxs-lookup"><span data-stu-id="ccad2-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="ccad2-109">Ustvarjanje rešitve po meri za cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="ccad2-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="ccad2-110">V PSA kliknite **Nastavitve** > **Rešitve** in nato **Novo**, da ustvarite novo rešitev.</span><span class="sxs-lookup"><span data-stu-id="ccad2-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="ccad2-111">Poimenujte rešitev, **\<ime organizacije> cenovne razsežnosti**, vnesite ostale zahtevane podatke in kliknite **Shrani.**</span><span class="sxs-lookup"><span data-stu-id="ccad2-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Ustvarjanje rešitve po meri za cenovne razsežnosti](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="ccad2-113">Ustvarjanje polj po meri in naborov možnosti v rešitvi za cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="ccad2-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="ccad2-114">Cenovna razsežnost je lahko nabor možnosti ali entiteta.</span><span class="sxs-lookup"><span data-stu-id="ccad2-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="ccad2-115">Oboje morate ustvariti v svoji rešitvi za določanje cen.</span><span class="sxs-lookup"><span data-stu-id="ccad2-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="ccad2-116">Koraki v tem postopku pojasnjujejo, kako ustvarite razsežnosti, ki temeljijo na entiteti, in razsežnosti, ki temeljijo na naboru možnosti.</span><span class="sxs-lookup"><span data-stu-id="ccad2-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="ccad2-117">Razsežnosti na osnovi entitete</span><span class="sxs-lookup"><span data-stu-id="ccad2-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="ccad2-118">V PSA kliknite **Nastavitve** > **Rešitve** in nato dvokliknite **\<ime organizacije> cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="ccad2-119">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="ccad2-120">Kliknite **Novo**, da ustvarite novo entiteto **Standardni naziv**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="ccad2-121">Vnesite ostale zahtevane informacije in kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definicija entitete standardnega naziva](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="ccad2-123">Razsežnosti na osnovi nabora možnosti</span><span class="sxs-lookup"><span data-stu-id="ccad2-123">Option set-based dimensions</span></span> 
<span data-ttu-id="ccad2-124">Ustvarite lahko dve razsežnosti na osnovi nabora možnosti.</span><span class="sxs-lookup"><span data-stu-id="ccad2-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="ccad2-125">Uporabite **Lokacija dela vira**, da sledite ceni za lokacijo dela **Doma** in **Na lokaciji**, ter **Delovni čas vira** z vrednostmi **Redno** in **Nadure**, da uporabite pribitek, ko je delo končano.</span><span class="sxs-lookup"><span data-stu-id="ccad2-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="ccad2-126">V PSA kliknite **Nastavitve** > **Rešitve** in nato dvokliknite **\<ime organizacije> cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="ccad2-127">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Nabori možnosti**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="ccad2-128">Kliknite **Novo**, da ustvarite nov nabor možnosti, vnesite ostale zahtevane podatke in kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="ccad2-129">Cenovna razsežnost na osnovi nabora možnosti, imenovana »Lokacija dela vira«</span><span class="sxs-lookup"><span data-stu-id="ccad2-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="ccad2-130">Cenovna razsežnost na osnovi nabora možnosti, imenovana »Delovne ure vira«</span><span class="sxs-lookup"><span data-stu-id="ccad2-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="ccad2-131">Ustvarjanje podatkov za razsežnosti na osnovi entitete</span><span class="sxs-lookup"><span data-stu-id="ccad2-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="ccad2-132">Podatke za razsežnosti na osnovi entitete lahko ustvarite ročno ali z uvozom v aplikaciji Microsoft Excel oz. s klici storitve.</span><span class="sxs-lookup"><span data-stu-id="ccad2-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="ccad2-133">Uporabite korake v tem postopku, da iz razsežnosti na osnovi entitete **Standardni naziv** ustvarite dva standardna naziva, in sicer **Sistemski inženir** in **Višji sistemi inženir**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="ccad2-134">Če je količina podatkov, ki jih želite ustvariti, majhna, kot v spodnjem primeru, lahko uporabite standardni obrazec.</span><span class="sxs-lookup"><span data-stu-id="ccad2-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="ccad2-135">V PSA kliknite **Napredno iskanje**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="ccad2-136">Izberite entiteto **Standardni naziv** in nato kliknite **Rezultati**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="ccad2-137">Prikazane bodo vse vrstice v entiteti **Standardni naziv**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="ccad2-138">Kliknite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-138">Click **New**.</span></span> <span data-ttu-id="ccad2-139">V polje **Ime** vnesite »Sistemski inženir« in nato kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="ccad2-140">Zaprite obrazec.</span><span class="sxs-lookup"><span data-stu-id="ccad2-140">Close the form.</span></span> 
4. <span data-ttu-id="ccad2-141">Ponovite korake od 1 do 3, da ustvarite drug standardni naziv za »Višji sistemski inženir«.</span><span class="sxs-lookup"><span data-stu-id="ccad2-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="ccad2-142">Vzorčni podatki za entiteto standardnega naziva</span><span class="sxs-lookup"><span data-stu-id="ccad2-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="ccad2-143">Dodajanje vseh zahtevanih entitet PSA in povezanih komponent v rešitev za cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="ccad2-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="ccad2-144">V svojo rešitev za določanje cen boste morali dodati spodnje entitete rešitve Project Service.</span><span class="sxs-lookup"><span data-stu-id="ccad2-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="ccad2-145">S koraki v tem postopku naredite nekaj pomembnih sprememb sheme v rešitvi za določanje cen, tako da se entitete seznanijo z novimi cenovnimi razsežnostmi.</span><span class="sxs-lookup"><span data-stu-id="ccad2-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="ccad2-146">V PSA kliknite **Nastavitve** > **Rešitve** in nato dvokliknite **\<ime organizacije> cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="ccad2-147">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Dodaj obstoječe** > **Entitete**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="ccad2-148">V pogovornem oknu **Komponente rešitve** izberite eno od teh entitet:</span><span class="sxs-lookup"><span data-stu-id="ccad2-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="ccad2-149">Dejansko</span><span class="sxs-lookup"><span data-stu-id="ccad2-149">Actual</span></span>
- <span data-ttu-id="ccad2-150">Vir, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="ccad2-150">Bookable Resource</span></span>
- <span data-ttu-id="ccad2-151">Vrstica ocene</span><span class="sxs-lookup"><span data-stu-id="ccad2-151">Estimate Line</span></span>
- <span data-ttu-id="ccad2-152">Podrobnosti vrstice računa</span><span class="sxs-lookup"><span data-stu-id="ccad2-152">Invoice Line Detail</span></span>
- <span data-ttu-id="ccad2-153">Vrstica dnevnika</span><span class="sxs-lookup"><span data-stu-id="ccad2-153">Journal Line</span></span>
- <span data-ttu-id="ccad2-154">Podrobnost vrstice projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="ccad2-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="ccad2-155">Član projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="ccad2-155">Project Team Member</span></span>
- <span data-ttu-id="ccad2-156">Podrobnosti vrstice ponudbe</span><span class="sxs-lookup"><span data-stu-id="ccad2-156">Quote Line Detail</span></span>
- <span data-ttu-id="ccad2-157">Pribitek na ceno vloge</span><span class="sxs-lookup"><span data-stu-id="ccad2-157">Role Price Markup</span></span>
- <span data-ttu-id="ccad2-158">Cena vloge</span><span class="sxs-lookup"><span data-stu-id="ccad2-158">Role Price</span></span> 
- <span data-ttu-id="ccad2-159">Časovni vnos</span><span class="sxs-lookup"><span data-stu-id="ccad2-159">Time Entry</span></span> 

> ![Dodajanje obstoječih entitet v rešitev za cenovne razsežnosti](media/Existing-entities-to-PD-solution.png)

> ![Izbira komponent rešitve](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="ccad2-162">Poskrbite, da boste vključili vse obrazce in poglede za posamezne izbrane entitete.</span><span class="sxs-lookup"><span data-stu-id="ccad2-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="ccad2-163">Ko ste pozvani, da vključite vse odvisne entitete za zgoraj izbrane entitete, kliknite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="ccad2-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Ne vključi vseh povezanih komponent](media/Do-not-include-required.png)


