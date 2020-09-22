---
title: Izklop cenovne razsežnosti
description: Ta tema vsebuje informacije o tem, kako nastavite cenovne razsežnosti v rešitvi Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755834"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="24337-103">Izklop cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="24337-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="24337-104">Morda boste morali vsakih nekaj let pregledati in posodobiti strategijo za oblikovanje cen.</span><span class="sxs-lookup"><span data-stu-id="24337-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="24337-105">Vsaka izvedena posodobitev lahko zahteva, da izklopite obstoječo cenovno razsežnost in ustvarite novo.</span><span class="sxs-lookup"><span data-stu-id="24337-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="24337-106">Prej ste morda na primer oblikovali ceno po elementu **Vloga**, zdaj pa ste se odločili, da boste oblikovali ceno po elementu **Delovne izkušnje**.</span><span class="sxs-lookup"><span data-stu-id="24337-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="24337-107">Zaradi tega boste morda morali izklopiti element **Vloga** kot cenovno razsežnost in ustvariti **Delovne izkušnje** kot novo cenovno razsežnost.</span><span class="sxs-lookup"><span data-stu-id="24337-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="24337-108">Cenovno razsežnost lahko izklopite tako, da polji **Mogoče uporabiti za ceno** in **Mogoče uporabiti za prodajo** nastavite na **Ne**, ne glede na to, ali je cenovna razsežnost vnaprej pripravljena ali ustvarjena po meri.</span><span class="sxs-lookup"><span data-stu-id="24337-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="24337-109">Po tem se vam bo morda prikazalo to sporočilo o napaki.</span><span class="sxs-lookup"><span data-stu-id="24337-109">However, when you do this, you might receive the following error message.</span></span>

![Napaka v poslovnem procesu, ki se lahko pojavi ob izklopu cenovne razsežnosti](media/Business-Process-Error.png)


<span data-ttu-id="24337-111">To sporočilo o napaki pomeni, da obstajajo zapisi cen, ki so bili predhodno nastavljeni za razsežnost, ki jo želite izklopiti.</span><span class="sxs-lookup"><span data-stu-id="24337-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="24337-112">Vse zapise **Cena vloge** in **Pribitki na ceno vloge**, ki se sklicujejo na razsežnost, je treba izbrisati, preden lahko uporabnost razsežnosti nastavite na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="24337-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="24337-113">To pravilo velja tako za vnaprej pripravljene cenovne razsežnosti kot za vse cenovne razsežnosti po meri, ki ste jih morda ustvarili.</span><span class="sxs-lookup"><span data-stu-id="24337-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="24337-114">To preverjanje je potrebno zato, ker ima rešitev Project Service omejitev, zaradi katere mora imeti vsak zapis **Cena vloge** edinstveno kombinacijo razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="24337-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="24337-115">Na ceniku, imenovanem **Stroški v ZDA, 2018**, so naslednje vrstice **Cena vloge**.</span><span class="sxs-lookup"><span data-stu-id="24337-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="24337-116">Standardni naziv</span><span class="sxs-lookup"><span data-stu-id="24337-116">Standard Title</span></span>         | <span data-ttu-id="24337-117">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="24337-117">Org Unit</span></span>    |<span data-ttu-id="24337-118">Enota</span><span class="sxs-lookup"><span data-stu-id="24337-118">Unit</span></span>   |<span data-ttu-id="24337-119">Cena</span><span class="sxs-lookup"><span data-stu-id="24337-119">Price</span></span>  |<span data-ttu-id="24337-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="24337-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="24337-121">Sistemski inženir</span><span class="sxs-lookup"><span data-stu-id="24337-121">Systems Engineer</span></span>|<span data-ttu-id="24337-122">Contoso, ZDA</span><span class="sxs-lookup"><span data-stu-id="24337-122">Contoso US</span></span>|<span data-ttu-id="24337-123">Ura</span><span class="sxs-lookup"><span data-stu-id="24337-123">Hour</span></span>| <span data-ttu-id="24337-124">100</span><span class="sxs-lookup"><span data-stu-id="24337-124">100</span></span>|<span data-ttu-id="24337-125">USD</span><span class="sxs-lookup"><span data-stu-id="24337-125">USD</span></span>|
| <span data-ttu-id="24337-126">Višji sistemski inženir</span><span class="sxs-lookup"><span data-stu-id="24337-126">Senior Systems Engineer</span></span>|<span data-ttu-id="24337-127">Contoso, ZDA</span><span class="sxs-lookup"><span data-stu-id="24337-127">Contoso US</span></span>|<span data-ttu-id="24337-128">Ura</span><span class="sxs-lookup"><span data-stu-id="24337-128">Hour</span></span>| <span data-ttu-id="24337-129">150</span><span class="sxs-lookup"><span data-stu-id="24337-129">150</span></span>| <span data-ttu-id="24337-130">USD</span><span class="sxs-lookup"><span data-stu-id="24337-130">USD</span></span>|


<span data-ttu-id="24337-131">Če izklopite **Standardni naziv** kot cenovno razsežnost, bo mehanizem za izračunavanje cen rešitve Project Service pri iskanju cene uporabil le vrednost **Organizacijska enota** iz konteksta vnosa.</span><span class="sxs-lookup"><span data-stu-id="24337-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="24337-132">Če je **Organizacijska enota** za kontekst vnosa »Contoso, ZDA«, rezultata ne bo mogoče določiti, saj se bosta obe vrstici ujemali.</span><span class="sxs-lookup"><span data-stu-id="24337-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="24337-133">Če se želite izogniti temu, naredite naslednje: ko ustvarite zapise **Cena vloge**, rešitev Project Service potrdi, da je kombinacija razsežnosti edinstvena.</span><span class="sxs-lookup"><span data-stu-id="24337-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="24337-134">Če razsežnost po ustvarjanju zapisov **Cena vloge** izklopite, je to omejitev mogoče zaobiti.</span><span class="sxs-lookup"><span data-stu-id="24337-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="24337-135">Zato morate pred izklopom razsežnosti izbrisati vse vrstice **Cena vlog** in **Pribitek na ceno vloge**, ki imajo izpolnjeno to vrednost razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="24337-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

