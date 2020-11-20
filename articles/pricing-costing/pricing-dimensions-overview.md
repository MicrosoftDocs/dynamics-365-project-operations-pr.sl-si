---
title: Pregled cenovnih razsežnosti
description: Ta tema vsebuje informacije o cenovnih razsežnostih v storitvi Dynamics 365 Project Operations.
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
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128483"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="9c5b4-103">Pregled cenovnih razsežnosti</span><span class="sxs-lookup"><span data-stu-id="9c5b4-103">Pricing dimensions overview</span></span>

<span data-ttu-id="9c5b4-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="9c5b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9c5b4-105">Razsežnosti, ki se uporabljajo v človeških virih za nastavitev določanja cen in stroškov, se delijo v dve kategoriji:</span><span class="sxs-lookup"><span data-stu-id="9c5b4-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="9c5b4-106">Osebe</span><span class="sxs-lookup"><span data-stu-id="9c5b4-106">People</span></span>
- <span data-ttu-id="9c5b4-107">Načrtovano delo</span><span class="sxs-lookup"><span data-stu-id="9c5b4-107">Planned work</span></span>

<span data-ttu-id="9c5b4-108">Zaradi tega obstajata dve vrsti vrednosti cenovnih razsežnosti, ki so na voljo:</span><span class="sxs-lookup"><span data-stu-id="9c5b4-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="9c5b4-109">**Nabori možnosti**: razsežnosti, ki so nespremenljiva oštevilčenja za nabor vrednosti.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="9c5b4-110">**Vrednosti, ki temeljijo na entitetah**: razsežnosti, ki so lahko spremenljiv nabor vrednosti.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="9c5b4-111">Cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="9c5b4-111">Pricing dimensions</span></span>

<span data-ttu-id="9c5b4-112">Dynamics 365 Project Operations vključuje privzet nabor cenovnih razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="9c5b4-113">Te cenovne razsežnosti si lahko ogledate v **Project Operations** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="9c5b4-114">V zapisu parametra na zavihku **Cenovna razsežnost na podlagi zneska** preverite, ali sta pri vlogi **msdyn_resourcecategory** in organizacijski enoti za vire **msdyn_organizationalunit** polji **Mogoče uporabiti za prodajo** in **Mogoče uporabiti za ceno** nastavljeni na **Da**.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="9c5b4-115">Z omogočenimi temi polji lahko nastavite ceno in strošek za vsako kombinacijo vloge in organizacijske enote.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="9c5b4-116">Če morate zagotoviti ceno ali strošek za svoje vire z dodatnimi atributi, lahko ustvarite polja, entitete in razsežnosti po meri.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="9c5b4-117">Določanje cene časa človeških virov</span><span class="sxs-lookup"><span data-stu-id="9c5b4-117">Pricing human resource time</span></span>
<span data-ttu-id="9c5b4-118">Kako organizacija določi cene za čas človeških virov je pogosto pomemben strateški vidik, ki neposredno vpliva na dobičkonosnost organizacije.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="9c5b4-119">Ko se je vaša organizacija pripravljena opredeliti, kako želi nastaviti mere stroškov in deleže obračunavanja za čas človeških virov, sodelujte s finančnimi ekipami in vodji praks.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="9c5b4-120">Drugi vidiki določanja cen vključujejo tudi to, ali naj se znova uporabijo polja ali entitete, ki trenutno niso cenovne razsežnosti, vendar se uporabljajo kot cenovna razsežnost za vašo organizacijo.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="9c5b4-121">Polja, kot sta **Kategorija transakcije** (**msdyn_transactioncategory**) in **Viri, ki jih je mogoče rezervirati** (**bookableresource**), so primeri možnih razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="9c5b4-122">Razmislite, ali naj bo vaša cenovna razsežnost tabela ali nabor možnosti.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="9c5b4-123">Če predvidevate spremembe vrednosti razsežnosti, ki bodo presegle 10 ali 12, in potrebujete dodatne atribute v teh vrednosti, namesto nabora možnosti raje ustvarite entiteto.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="9c5b4-124">Vzdrževanje nabora možnosti, na primer dodajanje ali odstranjevanje vrednosti, zahteva skrbnika ali razvijalca, dodajanje novih vrstic v tabelo pa lahko opravi večina uporabnikov.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="9c5b4-125">Spodnji primer prikazuje deleže obračunavanja, ki so nastavljeni na podlagi vloge in organizacijske enote organizacije vira, ki ji pripada vir.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="9c5b4-126">Mere stroškov običajno temeljijo na razponu plače zaposlenega in organizacijski enoti, ki ji pripada.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="9c5b4-127">V tem primeru bodo tabele z deležem obračunavanja in mero stroškov videti, kot je prikazano spodaj.</span><span class="sxs-lookup"><span data-stu-id="9c5b4-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="9c5b4-128">**Vzorčni deleži obračunavanja**</span><span class="sxs-lookup"><span data-stu-id="9c5b4-128">**Sample bill rates**</span></span>

| <span data-ttu-id="9c5b4-129">Vloga</span><span class="sxs-lookup"><span data-stu-id="9c5b4-129">Role</span></span>        | <span data-ttu-id="9c5b4-130">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="9c5b4-130">Org Unit</span></span>    |<span data-ttu-id="9c5b4-131">Enota</span><span class="sxs-lookup"><span data-stu-id="9c5b4-131">Unit</span></span>      |<span data-ttu-id="9c5b4-132">Cena</span><span class="sxs-lookup"><span data-stu-id="9c5b4-132">Price</span></span>      |<span data-ttu-id="9c5b4-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="9c5b4-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="9c5b4-134">Developer</span><span class="sxs-lookup"><span data-stu-id="9c5b4-134">Developer</span></span>   | <span data-ttu-id="9c5b4-135">Contoso, ZDA</span><span class="sxs-lookup"><span data-stu-id="9c5b4-135">Contoso US</span></span>  |<span data-ttu-id="9c5b4-136">Ura</span><span class="sxs-lookup"><span data-stu-id="9c5b4-136">Hour</span></span> | <span data-ttu-id="9c5b4-137">200</span><span class="sxs-lookup"><span data-stu-id="9c5b4-137">200</span></span>|<span data-ttu-id="9c5b4-138">USD</span><span class="sxs-lookup"><span data-stu-id="9c5b4-138">USD</span></span>     |
| <span data-ttu-id="9c5b4-139">Developer</span><span class="sxs-lookup"><span data-stu-id="9c5b4-139">Developer</span></span>   | <span data-ttu-id="9c5b4-140">Contoso Indija</span><span class="sxs-lookup"><span data-stu-id="9c5b4-140">Contoso India</span></span> |<span data-ttu-id="9c5b4-141">Ura</span><span class="sxs-lookup"><span data-stu-id="9c5b4-141">Hour</span></span>|   <span data-ttu-id="9c5b4-142">112</span><span class="sxs-lookup"><span data-stu-id="9c5b4-142">112</span></span>|<span data-ttu-id="9c5b4-143">USD</span><span class="sxs-lookup"><span data-stu-id="9c5b4-143">USD</span></span>     |


<span data-ttu-id="9c5b4-144">**Vzorčne mere stroškov**</span><span class="sxs-lookup"><span data-stu-id="9c5b4-144">**Sample cost rates**</span></span>

| <span data-ttu-id="9c5b4-145">Razpon plače</span><span class="sxs-lookup"><span data-stu-id="9c5b4-145">Salary Band</span></span>     | <span data-ttu-id="9c5b4-146">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="9c5b4-146">Org Unit</span></span>    |<span data-ttu-id="9c5b4-147">Enota</span><span class="sxs-lookup"><span data-stu-id="9c5b4-147">Unit</span></span>      |<span data-ttu-id="9c5b4-148">Cena</span><span class="sxs-lookup"><span data-stu-id="9c5b4-148">Price</span></span>      |<span data-ttu-id="9c5b4-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="9c5b4-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="9c5b4-150">Moje podjetje_razpon1</span><span class="sxs-lookup"><span data-stu-id="9c5b4-150">My company_Band1</span></span> | <span data-ttu-id="9c5b4-151">Contoso, ZDA</span><span class="sxs-lookup"><span data-stu-id="9c5b4-151">Contoso US</span></span>  |<span data-ttu-id="9c5b4-152">Ura</span><span class="sxs-lookup"><span data-stu-id="9c5b4-152">Hour</span></span> | <span data-ttu-id="9c5b4-153">145</span><span class="sxs-lookup"><span data-stu-id="9c5b4-153">145</span></span>|<span data-ttu-id="9c5b4-154">USD</span><span class="sxs-lookup"><span data-stu-id="9c5b4-154">USD</span></span>     |
| <span data-ttu-id="9c5b4-155">Moje podjetje_razpon2</span><span class="sxs-lookup"><span data-stu-id="9c5b4-155">My company_Band2</span></span> | <span data-ttu-id="9c5b4-156">Contoso Indija</span><span class="sxs-lookup"><span data-stu-id="9c5b4-156">Contoso India</span></span> |<span data-ttu-id="9c5b4-157">Ura</span><span class="sxs-lookup"><span data-stu-id="9c5b4-157">Hour</span></span>|   <span data-ttu-id="9c5b4-158">67</span><span class="sxs-lookup"><span data-stu-id="9c5b4-158">67</span></span>|<span data-ttu-id="9c5b4-159">USD</span><span class="sxs-lookup"><span data-stu-id="9c5b4-159">USD</span></span>     |
