---
title: Izklop cenovne razsežnosti
description: Ta tema vsebuje informacije o tem, kako izklopiti cenovne razsežnosti.
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
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650069"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="a6de4-103">Izklop cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="a6de4-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="a6de4-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="a6de4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a6de4-105">Morda boste morali vsakih nekaj let pregledati in posodobiti strategijo za oblikovanje cen.</span><span class="sxs-lookup"><span data-stu-id="a6de4-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="a6de4-106">Vsaka izvedena posodobitev lahko zahteva, da izklopite obstoječo cenovno razsežnost in ustvarite novo.</span><span class="sxs-lookup"><span data-stu-id="a6de4-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="a6de4-107">Prej ste morda na primer oblikovali ceno po elementu **Vloga**, zdaj pa ste se odločili, da boste oblikovali ceno po elementu **Delovne izkušnje**.</span><span class="sxs-lookup"><span data-stu-id="a6de4-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="a6de4-108">Zaradi tega boste morda morali izklopiti element **Vloga** kot cenovno razsežnost in ustvariti **Delovne izkušnje** kot novo cenovno razsežnost.</span><span class="sxs-lookup"><span data-stu-id="a6de4-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="a6de4-109">Cenovno razsežnost lahko izklopite tako, da polji **Mogoče uporabiti za ceno** in **Mogoče uporabiti za prodajo** nastavite na **Ne**, ne glede na to, ali je cenovna razsežnost vnaprej pripravljena ali ustvarjena po meri.</span><span class="sxs-lookup"><span data-stu-id="a6de4-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="a6de4-110">Ko pa to storite, boste morda prejeli sporočilo o napaki **Cenovne razsežnosti ni mogoče posodobiti ali izbrisati, če obstajajo povezani zapisi cen**.</span><span class="sxs-lookup"><span data-stu-id="a6de4-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Napaka v poslovnem procesu, ki se lahko pojavi ob izklopu cenovne razsežnosti](media/Business-Process-Error.png)

<span data-ttu-id="a6de4-112">To sporočilo o napaki pomeni, da obstajajo zapisi cen, ki so bili predhodno nastavljeni za razsežnost, ki jo želite izklopiti.</span><span class="sxs-lookup"><span data-stu-id="a6de4-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="a6de4-113">Vse zapise **Cena vloge** in **Pribitki na ceno vloge**, ki se sklicujejo na razsežnost, je treba izbrisati, preden lahko uporabnost razsežnosti nastavite na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a6de4-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="a6de4-114">To pravilo velja tako za vnaprej pripravljene cenovne razsežnosti kot za vse cenovne razsežnosti po meri, ki ste jih morda ustvarili.</span><span class="sxs-lookup"><span data-stu-id="a6de4-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="a6de4-115">To preverjanje je potrebno zato, ker mora imeti vsak zapis **Cena vloge** edinstveno kombinacijo razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="a6de4-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="a6de4-116">Na ceniku, imenovanem **Stroški v ZDA, 2018**, so naslednje vrstice **Cena vloge**.</span><span class="sxs-lookup"><span data-stu-id="a6de4-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="a6de4-117">Standardni naziv</span><span class="sxs-lookup"><span data-stu-id="a6de4-117">Standard Title</span></span>         | <span data-ttu-id="a6de4-118">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="a6de4-118">Org Unit</span></span>    |<span data-ttu-id="a6de4-119">Enota</span><span class="sxs-lookup"><span data-stu-id="a6de4-119">Unit</span></span>   |<span data-ttu-id="a6de4-120">Cena</span><span class="sxs-lookup"><span data-stu-id="a6de4-120">Price</span></span>  |<span data-ttu-id="a6de4-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="a6de4-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="a6de4-122">Sistemski inženir</span><span class="sxs-lookup"><span data-stu-id="a6de4-122">Systems Engineer</span></span>|<span data-ttu-id="a6de4-123">Contoso, ZDA</span><span class="sxs-lookup"><span data-stu-id="a6de4-123">Contoso US</span></span>|<span data-ttu-id="a6de4-124">Ura</span><span class="sxs-lookup"><span data-stu-id="a6de4-124">Hour</span></span>| <span data-ttu-id="a6de4-125">100</span><span class="sxs-lookup"><span data-stu-id="a6de4-125">100</span></span>|<span data-ttu-id="a6de4-126">USD</span><span class="sxs-lookup"><span data-stu-id="a6de4-126">USD</span></span>|
| <span data-ttu-id="a6de4-127">Višji sistemski inženir</span><span class="sxs-lookup"><span data-stu-id="a6de4-127">Senior Systems Engineer</span></span>|<span data-ttu-id="a6de4-128">Contoso, ZDA</span><span class="sxs-lookup"><span data-stu-id="a6de4-128">Contoso US</span></span>|<span data-ttu-id="a6de4-129">Ura</span><span class="sxs-lookup"><span data-stu-id="a6de4-129">Hour</span></span>| <span data-ttu-id="a6de4-130">150</span><span class="sxs-lookup"><span data-stu-id="a6de4-130">150</span></span>| <span data-ttu-id="a6de4-131">USD</span><span class="sxs-lookup"><span data-stu-id="a6de4-131">USD</span></span>|


<span data-ttu-id="a6de4-132">Če izklopite **Standardni naziv** kot cenovno razsežnost, bo mehanizem za izračunavanje cen pri iskanju cene uporabil le vrednost **Organizacijska enota** iz konteksta vnosa.</span><span class="sxs-lookup"><span data-stu-id="a6de4-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="a6de4-133">Če je **Organizacijska enota** za kontekst vnosa »Contoso, ZDA«, rezultata ne bo mogoče določiti, saj se bosta obe vrstici ujemali.</span><span class="sxs-lookup"><span data-stu-id="a6de4-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="a6de4-134">Če se želite izogniti temu, naredite naslednje: ko ustvarite zapise **Cena vloge**, sistem potrdi, da je kombinacija razsežnosti edinstvena.</span><span class="sxs-lookup"><span data-stu-id="a6de4-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="a6de4-135">Če razsežnost po ustvarjanju zapisov **Cena vloge** izklopite, je to omejitev mogoče zaobiti.</span><span class="sxs-lookup"><span data-stu-id="a6de4-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="a6de4-136">Zato morate pred izklopom razsežnosti izbrisati vse vrstice **Cena vlog** in **Pribitek na ceno vloge**, ki imajo izpolnjeno to vrednost razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="a6de4-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
