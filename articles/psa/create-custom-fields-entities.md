---
title: Ustvarjanje polj in entitet po meri
description: V tej temi je pojasnjeno, kako ustvarite nabor možnosti in entitete v svoji rešitvi v platformi Power Apps.
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
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084825"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="d6722-103">Ustvarjanje polj in entitet po meri</span><span class="sxs-lookup"><span data-stu-id="d6722-103">Create custom fields and entities</span></span> 

<span data-ttu-id="d6722-104">Če želite ustvariti nabor možnosti ali entiteto po meri v platformi Power Apps, upoštevajte spodnje korake.</span><span class="sxs-lookup"><span data-stu-id="d6722-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="d6722-105">Postopke v tej temi morate izvesti s spletnim vmesnikom aplikacije Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="d6722-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6722-106">Priporočamo, da vse cenovne razsežnosti po meri spremenite v ločeni rešitvi.</span><span class="sxs-lookup"><span data-stu-id="d6722-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="d6722-107">Ta pomembna najboljša praksa zagotavlja nadaljnjo prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi, pomaga pri ponovni uporabi vašega dela in olajša prenos teh sprememb v drug primerek.</span><span class="sxs-lookup"><span data-stu-id="d6722-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="d6722-108">Ko naredite vse zahtevane spremembe, izvozite to rešitev kot **upravljano rešitev** in jo uvozite v druge primerke, da znova uporabite nastavitev cen.</span><span class="sxs-lookup"><span data-stu-id="d6722-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="d6722-109">Ustvarjanje polj po meri in naborov možnosti v rešitvi za cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="d6722-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="d6722-110">Cenovna razsežnost je lahko nabor možnosti ali entiteta.</span><span class="sxs-lookup"><span data-stu-id="d6722-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="d6722-111">Oboje morate ustvariti v svoji rešitvi za določanje cen.</span><span class="sxs-lookup"><span data-stu-id="d6722-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="d6722-112">Koraki v tem postopku pojasnjujejo, kako ustvarite razsežnosti, ki temeljijo na entiteti, in razsežnosti, ki temeljijo na naboru možnosti.</span><span class="sxs-lookup"><span data-stu-id="d6722-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="d6722-113">Razsežnosti na osnovi entitete</span><span class="sxs-lookup"><span data-stu-id="d6722-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="d6722-114">V rešitvi PSA kliknite **Nastavitve** > **Rešitve** , nato pa dvokliknite **\<your organization name> – cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="d6722-114">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="d6722-115">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete**.</span><span class="sxs-lookup"><span data-stu-id="d6722-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="d6722-116">Kliknite **Novo** , da ustvarite novo entiteto **Standardni naziv**.</span><span class="sxs-lookup"><span data-stu-id="d6722-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="d6722-117">Vnesite ostale zahtevane informacije in kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="d6722-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definicija entitete standardnega naziva](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="d6722-119">Razsežnosti na osnovi nabora možnosti</span><span class="sxs-lookup"><span data-stu-id="d6722-119">Option set-based dimensions</span></span> 
<span data-ttu-id="d6722-120">Ustvarite lahko dve razsežnosti na osnovi nabora možnosti.</span><span class="sxs-lookup"><span data-stu-id="d6722-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="d6722-121">Uporabite **Lokacija dela vira** , da sledite ceni za lokacijo dela **Doma** in **Na lokaciji** , ter **Delovni čas vira** z vrednostmi **Redno** in **Nadure** , da uporabite pribitek, ko je delo končano.</span><span class="sxs-lookup"><span data-stu-id="d6722-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="d6722-122">V rešitvi PSA kliknite **Nastavitve** > **Rešitve** , nato pa dvokliknite **\<your organization name> – cenovne razsežnosti**.</span><span class="sxs-lookup"><span data-stu-id="d6722-122">In PSA, click **Settings** > **Solutions** , and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d6722-123">V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Nabori možnosti**.</span><span class="sxs-lookup"><span data-stu-id="d6722-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="d6722-124">Kliknite **Novo** , da ustvarite nov nabor možnosti, vnesite ostale zahtevane podatke in kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="d6722-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="d6722-125">Cenovna razsežnost na osnovi nabora možnosti, imenovana »Lokacija dela vira«</span><span class="sxs-lookup"><span data-stu-id="d6722-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="d6722-126">Cenovna razsežnost na osnovi nabora možnosti, imenovana »Delovne ure vira«</span><span class="sxs-lookup"><span data-stu-id="d6722-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="d6722-127">Ustvarjanje podatkov za razsežnosti na osnovi entitete</span><span class="sxs-lookup"><span data-stu-id="d6722-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="d6722-128">Podatke za razsežnosti na osnovi entitete lahko ustvarite ročno ali z uvozom v aplikaciji Microsoft Excel oz. s klici storitve.</span><span class="sxs-lookup"><span data-stu-id="d6722-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="d6722-129">Uporabite korake v tem postopku, da iz razsežnosti na osnovi entitete **Standardni naziv** ustvarite dva standardna naziva, in sicer **Sistemski inženir** in **Višji sistemi inženir**.</span><span class="sxs-lookup"><span data-stu-id="d6722-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="d6722-130">Če je količina podatkov, ki jih želite ustvariti, majhna, kot v spodnjem primeru, lahko uporabite standardni obrazec.</span><span class="sxs-lookup"><span data-stu-id="d6722-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="d6722-131">V PSA kliknite **Napredno iskanje**.</span><span class="sxs-lookup"><span data-stu-id="d6722-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="d6722-132">Izberite entiteto **Standardni naziv** in nato kliknite **Rezultati**.</span><span class="sxs-lookup"><span data-stu-id="d6722-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="d6722-133">Prikazane bodo vse vrstice v entiteti **Standardni naziv**.</span><span class="sxs-lookup"><span data-stu-id="d6722-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="d6722-134">Kliknite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="d6722-134">Click **New**.</span></span> <span data-ttu-id="d6722-135">V polje **Ime** vnesite »Sistemski inženir« in nato kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="d6722-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="d6722-136">Zaprite obrazec.</span><span class="sxs-lookup"><span data-stu-id="d6722-136">Close the form.</span></span> 
4. <span data-ttu-id="d6722-137">Ponovite korake od 1 do 3, da ustvarite drug standardni naziv za »Višji sistemski inženir«.</span><span class="sxs-lookup"><span data-stu-id="d6722-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="d6722-138">Vzorčni podatki za entiteto standardnega naziva</span><span class="sxs-lookup"><span data-stu-id="d6722-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


