---
title: Domača stran razsežnosti za določanje cen in razčlenitev stroškov
description: V tej temi je na voljo pregled cenovnih razsežnosti.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368901"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="b1b0f-103">Domača stran razsežnosti za določanje cen in razčlenitev stroškov</span><span class="sxs-lookup"><span data-stu-id="b1b0f-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b1b0f-104">Na dimenzije, ki se uporabljajo za določanje cen dela in stroškov v organizacijah, ki temeljijo na projektih, vplivajo naslednji atributi:</span><span class="sxs-lookup"><span data-stu-id="b1b0f-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="b1b0f-105">Ljudje, ki opravljajo delo v skladu z njihovimi izkušnjami, vlogo ali zemljepisno lokacijo</span><span class="sxs-lookup"><span data-stu-id="b1b0f-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="b1b0f-106">Delo, ki se izvaja v skladu z zahtevnostjo in časom v dnevu</span><span class="sxs-lookup"><span data-stu-id="b1b0f-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="b1b0f-107">Glede na naravo teh atributov dela in ljudi, ki so potrebni za izvedbo dela, sta v rešitvi Project Service Automation na voljo dve vrsti vrednosti cenovnih razsežnosti:</span><span class="sxs-lookup"><span data-stu-id="b1b0f-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="b1b0f-108">**Nabori možnosti** – atributi, ki so nespremenljiva oštevilčenja za nabor vrednosti.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="b1b0f-109">**Vrednosti, ki temeljijo na entitetah** – atributi, ki imajo lahko različne nabore vrednosti, ki so končne, vendar se lahko sčasoma spreminjajo.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="b1b0f-110">Cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="b1b0f-110">Pricing dimensions</span></span>

<span data-ttu-id="b1b0f-111">Storitev PSA vključuje privzet nabor cenovnih razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="b1b0f-112">Te si lahko ogledate v **Project Service** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="b1b0f-113">V zapisu parametra na zavihku **Cenovna razsežnost na podlagi zneska** preverite, ali sta pri vlogi **msdyn_resourcecategory** in organizacijski enoti za vire **msdyn_organizationalunit** polji **Mogoče uporabiti za prodajo** in **Mogoče uporabiti za ceno** nastavljeni na **Da**.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="b1b0f-114">To vam bo omogočilo, da nastavite ceno in ceno za vsako kombinacijo vloge in organizacijske enote.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Prikaz parametrov v aplikaciji Project Service z označeno možnostjo »Mogoče uporabiti za prodajo«](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="b1b0f-116">Če ste uporabljali vnaprej pripravljena polja vloge in organizacijske enote kot cenovne razsežnosti pred različico 3 aplikacije PSA, ne bo nobene opazne spremembe.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="b1b0f-117">Project Service lahko še naprej uporabljate kot običajno.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="b1b0f-118">Če morate zagotoviti ceno ali strošek za svoje vire z dodatnimi atributi, lahko ustvarite polja, entitete in razsežnosti po meri.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="b1b0f-119">Če želite več informacij, glejte spodnje teme, vendar upoštevajte, da morate dokončati postopke v spodaj navedenem vrstnem redu:</span><span class="sxs-lookup"><span data-stu-id="b1b0f-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="b1b0f-120">Ustvarjanje polj in entitet po meri</span><span class="sxs-lookup"><span data-stu-id="b1b0f-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="b1b0f-121">Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete</span><span class="sxs-lookup"><span data-stu-id="b1b0f-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="b1b0f-122">Nastavitev polj po meri kot cenovnih razsežnosti </span><span class="sxs-lookup"><span data-stu-id="b1b0f-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="b1b0f-123">Posodabljanje atributov vtičnikov za vključitev novih cenovnih razsežnosti</span><span class="sxs-lookup"><span data-stu-id="b1b0f-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="b1b0f-124">Določanje cene časa človeških virov</span><span class="sxs-lookup"><span data-stu-id="b1b0f-124">Pricing human resource time</span></span>
<span data-ttu-id="b1b0f-125">Kako organizacija določi cene za čas človeških virov je pogosto pomemben strateški vidik, ki neposredno vpliva na dobičkonosnost organizacije.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="b1b0f-126">Ko se je vaša organizacija pripravljena opredeliti, kako želi nastaviti mere stroškov in deleže obračunavanja za čas človeških virov, sodelujte s finančnimi ekipami in vodji praks.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="b1b0f-127">Drugi vidiki določanja cen vključujejo tudi to, ali naj se znova uporabijo polja ali entitete, ki trenutno niso cenovne razsežnosti, vendar se uporabljajo kot cenovna razsežnost za vašo organizacijo.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="b1b0f-128">Polja, kot sta **Kategorija transakcije** (**msdyn_transactioncategory**) in **Viri, ki jih je mogoče rezervirati** (**bookableresource**), so primeri možnih razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="b1b0f-129">Razmislite, ali naj bo vaša cenovna razsežnost tabela ali nabor možnosti.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="b1b0f-130">Če predvidevate spremembe vrednosti razsežnosti, ki bodo presegle vrednost 10 ali 12, in potrebujete dodatne atribute za te vrednosti, namesto nabora možnosti raje ustvarite entiteto.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="b1b0f-131">Za vzdrževanje nabora možnosti, na primer dodajanje ali odstranjevanje vrednosti, je potreben skrbnik ali razvijalec, dodajanje novih vrstic v tabelo pa lahko opravi večina poslovnih uporabnikov.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="b1b0f-132">Spodnji primer prikazuje deleže obračunavanja, ki so nastavljeni na podlagi vloge in organizacijske enote organizacije vira, ki ji pripada vir.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="b1b0f-133">Mere stroškov običajno temeljijo na razponu plače zaposlenega in organizacijski enoti, ki ji pripada.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="b1b0f-134">V tem primeru bodo tabele z deležem obračunavanja in mero stroškov videti, kot je prikazano spodaj.</span><span class="sxs-lookup"><span data-stu-id="b1b0f-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="b1b0f-135">**Vzorčni deleži obračunavanja**</span><span class="sxs-lookup"><span data-stu-id="b1b0f-135">**Sample bill rates**</span></span>

| <span data-ttu-id="b1b0f-136">Vloga</span><span class="sxs-lookup"><span data-stu-id="b1b0f-136">Role</span></span>        | <span data-ttu-id="b1b0f-137">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="b1b0f-137">Org Unit</span></span>    |<span data-ttu-id="b1b0f-138">Enota</span><span class="sxs-lookup"><span data-stu-id="b1b0f-138">Unit</span></span>      |<span data-ttu-id="b1b0f-139">Cena</span><span class="sxs-lookup"><span data-stu-id="b1b0f-139">Price</span></span>      |<span data-ttu-id="b1b0f-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="b1b0f-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="b1b0f-141">Razvijalec</span><span class="sxs-lookup"><span data-stu-id="b1b0f-141">Developer</span></span>   | <span data-ttu-id="b1b0f-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b1b0f-142">Contoso US</span></span>  |<span data-ttu-id="b1b0f-143">Ura</span><span class="sxs-lookup"><span data-stu-id="b1b0f-143">Hour</span></span> | <span data-ttu-id="b1b0f-144">200</span><span class="sxs-lookup"><span data-stu-id="b1b0f-144">200</span></span>|<span data-ttu-id="b1b0f-145">USD</span><span class="sxs-lookup"><span data-stu-id="b1b0f-145">USD</span></span>     |
| <span data-ttu-id="b1b0f-146">Razvijalec</span><span class="sxs-lookup"><span data-stu-id="b1b0f-146">Developer</span></span>   | <span data-ttu-id="b1b0f-147">Contoso Indija</span><span class="sxs-lookup"><span data-stu-id="b1b0f-147">Contoso India</span></span> |<span data-ttu-id="b1b0f-148">Ura</span><span class="sxs-lookup"><span data-stu-id="b1b0f-148">Hour</span></span>|   <span data-ttu-id="b1b0f-149">112</span><span class="sxs-lookup"><span data-stu-id="b1b0f-149">112</span></span>|<span data-ttu-id="b1b0f-150">USD</span><span class="sxs-lookup"><span data-stu-id="b1b0f-150">USD</span></span>     |


<span data-ttu-id="b1b0f-151">**Vzorčne mere stroškov**</span><span class="sxs-lookup"><span data-stu-id="b1b0f-151">**Sample cost rates**</span></span>

| <span data-ttu-id="b1b0f-152">Razpon plače</span><span class="sxs-lookup"><span data-stu-id="b1b0f-152">Salary Band</span></span>     | <span data-ttu-id="b1b0f-153">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="b1b0f-153">Org Unit</span></span>    |<span data-ttu-id="b1b0f-154">Enota</span><span class="sxs-lookup"><span data-stu-id="b1b0f-154">Unit</span></span>      |<span data-ttu-id="b1b0f-155">Cena</span><span class="sxs-lookup"><span data-stu-id="b1b0f-155">Price</span></span>      |<span data-ttu-id="b1b0f-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="b1b0f-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="b1b0f-157">Moje podjetje_razpon1</span><span class="sxs-lookup"><span data-stu-id="b1b0f-157">My company_Band1</span></span> | <span data-ttu-id="b1b0f-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="b1b0f-158">Contoso US</span></span>  |<span data-ttu-id="b1b0f-159">Ura</span><span class="sxs-lookup"><span data-stu-id="b1b0f-159">Hour</span></span> | <span data-ttu-id="b1b0f-160">145</span><span class="sxs-lookup"><span data-stu-id="b1b0f-160">145</span></span>|<span data-ttu-id="b1b0f-161">USD</span><span class="sxs-lookup"><span data-stu-id="b1b0f-161">USD</span></span>     |
| <span data-ttu-id="b1b0f-162">Moje podjetje_razpon2</span><span class="sxs-lookup"><span data-stu-id="b1b0f-162">My company_Band2</span></span> | <span data-ttu-id="b1b0f-163">Contoso Indija</span><span class="sxs-lookup"><span data-stu-id="b1b0f-163">Contoso India</span></span> |<span data-ttu-id="b1b0f-164">Ura</span><span class="sxs-lookup"><span data-stu-id="b1b0f-164">Hour</span></span>|   <span data-ttu-id="b1b0f-165">67</span><span class="sxs-lookup"><span data-stu-id="b1b0f-165">67</span></span>|<span data-ttu-id="b1b0f-166">USD</span><span class="sxs-lookup"><span data-stu-id="b1b0f-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]