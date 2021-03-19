---
title: Ustvarjanje polj in entitet po meri kot cenovnih razsežnosti
description: Ta tema vsebuje informacije o tem, kako ustvariti nabore možnosti ali entitete po meri.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275648"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="10d32-103">Ustvarjanje polj in entitet po meri kot cenovnih razsežnosti</span><span class="sxs-lookup"><span data-stu-id="10d32-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="10d32-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="10d32-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="10d32-105">Če želite ustvariti nabor možnosti ali entiteto po meri, da bi jo uporabili kot cenovno razsežnost, upoštevajte spodnje korake.</span><span class="sxs-lookup"><span data-stu-id="10d32-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="10d32-106">Za več informacij glejte razdelek [Pregled cenovnih razsežnosti](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="10d32-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="10d32-107">Priporočamo, da vse cenovne razsežnosti po meri spremenite v ločeni rešitvi.</span><span class="sxs-lookup"><span data-stu-id="10d32-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="10d32-108">Ta pomembna najboljša praksa zagotavlja nadaljnjo prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi.</span><span class="sxs-lookup"><span data-stu-id="10d32-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="10d32-109">To bo pomagalo tudi pri ponovni uporabi opravljenega dela in olajšalo prenos teh sprememb na drug primerek. Ko izvedete vse zahtevane spremembe, izvozite to rešitev kot **Upravljano rešitev** in jo uvozite v druge primerke, da ponovno uporabite nastavljeno oblikovanje cen.</span><span class="sxs-lookup"><span data-stu-id="10d32-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="10d32-110">Ustvarjanje polj po meri in naborov možnosti v rešitvi za cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="10d32-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="10d32-111">Cenovna razsežnost je lahko nabor možnosti ali entiteta.</span><span class="sxs-lookup"><span data-stu-id="10d32-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="10d32-112">Oboje morate ustvariti v svoji rešitvi za določanje cen.</span><span class="sxs-lookup"><span data-stu-id="10d32-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="10d32-113">Koraki v tem postopku pojasnjujejo, kako ustvarite razsežnosti, ki temeljijo na entiteti, in razsežnosti, ki temeljijo na naboru možnosti.</span><span class="sxs-lookup"><span data-stu-id="10d32-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="10d32-114">Razsežnosti na osnovi entitete</span><span class="sxs-lookup"><span data-stu-id="10d32-114">Entity-based dimensions</span></span>
<span data-ttu-id="10d32-115">Če želite ustvariti razsežnosti, ki temeljijo na entitetah, sledite tem korakom:</span><span class="sxs-lookup"><span data-stu-id="10d32-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="10d32-116">Odprite **Nastavitve** > **Rešitve**, nato dvokliknite **\<your organization name> cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="10d32-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="10d32-117">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete**.</span><span class="sxs-lookup"><span data-stu-id="10d32-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="10d32-118">Izberite **Novo**, da ustvarite novo entiteto **Standardni naziv**.</span><span class="sxs-lookup"><span data-stu-id="10d32-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="10d32-119">Vnesite ostale zahtevane informacije in nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="10d32-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definicija entitete standardnega naziva](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="10d32-121">Razsežnosti na osnovi nabora možnosti</span><span class="sxs-lookup"><span data-stu-id="10d32-121">Option set-based dimensions</span></span> 
<span data-ttu-id="10d32-122">Ustvarite lahko dve razsežnosti na osnovi nabora možnosti.</span><span class="sxs-lookup"><span data-stu-id="10d32-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="10d32-123">Uporabite **Lokacija dela vira** za sledenje ceni lokacije dela, opravljenega **Doma** in **Na lokaciji**.</span><span class="sxs-lookup"><span data-stu-id="10d32-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="10d32-124">Uporabite **Delovni čas vira** z vrednostmi **Redno** in **Nadure**, da se prikaže oznaka, ko je delo končano.</span><span class="sxs-lookup"><span data-stu-id="10d32-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="10d32-125">Naslednja slika prikazuje pogled razsežnosti **Lokacija dela vira**.</span><span class="sxs-lookup"><span data-stu-id="10d32-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Cenovna razsežnost na osnovi nabora možnosti, imenovana »Lokacija dela vira«](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="10d32-127">Naslednja slika prikazuje pogled razsežnosti **Delovni čas vira**.</span><span class="sxs-lookup"><span data-stu-id="10d32-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Cenovna razsežnost na osnovi nabora možnosti, imenovana »Delovne ure vira«](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="10d32-129">Odprite **Nastavitve** > **Rešitve**, nato dvokliknite **\<your organization name> cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="10d32-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="10d32-130">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Nabori možnosti**.</span><span class="sxs-lookup"><span data-stu-id="10d32-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="10d32-131">Izberite **Novo**, da ustvarite nov nabor možnosti, vnesite ostale zahtevane podatke in nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="10d32-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="10d32-132">Ustvarjanje podatkov za razsežnosti na osnovi entitete</span><span class="sxs-lookup"><span data-stu-id="10d32-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="10d32-133">Podatke za razsežnosti na osnovi entitete lahko ustvarite ročno ali z uvozom v aplikaciji Microsoft Excel oz. s klici storitve.</span><span class="sxs-lookup"><span data-stu-id="10d32-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="10d32-134">Uporabite korake v tem postopku, da iz razsežnosti na osnovi entitete **Standardni naziv** ustvarite dva standardna naziva, in sicer **Sistemski inženir** in **Višji sistemi inženir**.</span><span class="sxs-lookup"><span data-stu-id="10d32-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="10d32-135">Če je količina podatkov, ki jih želite ustvariti, majhna, kot v spodnjem primeru, lahko uporabite standardni obrazec.</span><span class="sxs-lookup"><span data-stu-id="10d32-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="10d32-136">Izberite **Napredno iskanje**.</span><span class="sxs-lookup"><span data-stu-id="10d32-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="10d32-137">Izberite entiteto **Standardni naziv** in nato izberite **Rezultati**.</span><span class="sxs-lookup"><span data-stu-id="10d32-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="10d32-138">Prikazane bodo vse vrstice v entiteti **Standardni naziv**.</span><span class="sxs-lookup"><span data-stu-id="10d32-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="10d32-139">Izberite **Novo** in v polje **Ime** vnesite »Sistemski inženir« in nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="10d32-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="10d32-140">Zaprite stran.</span><span class="sxs-lookup"><span data-stu-id="10d32-140">Close the page.</span></span> 
5. <span data-ttu-id="10d32-141">Ponovite korake od 1 do 3, da ustvarite drug standardni naziv za »Višji sistemski inženir«.</span><span class="sxs-lookup"><span data-stu-id="10d32-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Vzorčni podatki za entiteto standardnega naziva](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]