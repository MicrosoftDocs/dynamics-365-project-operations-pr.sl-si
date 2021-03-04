---
title: Domača stran razsežnosti za določanje cen in razčlenitev stroškov
description: V tej temi je na voljo pregled cenovnih razsežnosti.
author: rumant
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
ms.openlocfilehash: 65516784c6787fa5f3c08297f4d161d52c2ea4a9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151318"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="0ba52-103">Domača stran razsežnosti za določanje cen in razčlenitev stroškov</span><span class="sxs-lookup"><span data-stu-id="0ba52-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0ba52-104">Na dimenzije, ki se uporabljajo za določanje cen dela in stroškov v organizacijah, ki temeljijo na projektih, vplivajo naslednji atributi:</span><span class="sxs-lookup"><span data-stu-id="0ba52-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="0ba52-105">Ljudje, ki opravljajo delo v skladu z njihovimi izkušnjami, vlogo ali zemljepisno lokacijo</span><span class="sxs-lookup"><span data-stu-id="0ba52-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="0ba52-106">Delo, ki se izvaja v skladu z zahtevnostjo in časom v dnevu</span><span class="sxs-lookup"><span data-stu-id="0ba52-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="0ba52-107">Glede na naravo teh atributov dela in ljudi, ki so potrebni za izvedbo dela, sta v rešitvi Project Service Automation na voljo dve vrsti vrednosti cenovnih razsežnosti:</span><span class="sxs-lookup"><span data-stu-id="0ba52-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="0ba52-108">**Nabori možnosti** – atributi, ki so nespremenljiva oštevilčenja za nabor vrednosti.</span><span class="sxs-lookup"><span data-stu-id="0ba52-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="0ba52-109">**Vrednosti, ki temeljijo na entitetah** – atributi, ki imajo lahko različne nabore vrednosti, ki so končne, vendar se lahko sčasoma spreminjajo.</span><span class="sxs-lookup"><span data-stu-id="0ba52-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="0ba52-110">Cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="0ba52-110">Pricing dimensions</span></span>

<span data-ttu-id="0ba52-111">Storitev PSA vključuje privzet nabor cenovnih razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="0ba52-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="0ba52-112">Te si lahko ogledate v **Project Service** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="0ba52-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="0ba52-113">V zapisu parametra na zavihku **Cenovna razsežnost na podlagi zneska** preverite, ali sta pri vlogi **msdyn_resourcecategory** in organizacijski enoti za vire **msdyn_organizationalunit** polji **Mogoče uporabiti za prodajo** in **Mogoče uporabiti za ceno** nastavljeni na **Da**.</span><span class="sxs-lookup"><span data-stu-id="0ba52-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="0ba52-114">To vam bo omogočilo, da nastavite ceno in ceno za vsako kombinacijo vloge in organizacijske enote.</span><span class="sxs-lookup"><span data-stu-id="0ba52-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Prikaz parametrov v aplikaciji Project Service z označeno možnostjo »Mogoče uporabiti za prodajo«](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="0ba52-116">Če ste uporabljali vnaprej pripravljena polja vloge in organizacijske enote kot cenovne razsežnosti pred različico 3 aplikacije PSA, ne bo nobene opazne spremembe.</span><span class="sxs-lookup"><span data-stu-id="0ba52-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="0ba52-117">Project Service lahko še naprej uporabljate kot običajno.</span><span class="sxs-lookup"><span data-stu-id="0ba52-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="0ba52-118">Če morate zagotoviti ceno ali strošek za svoje vire z dodatnimi atributi, lahko ustvarite polja, entitete in razsežnosti po meri.</span><span class="sxs-lookup"><span data-stu-id="0ba52-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="0ba52-119">Če želite več informacij, glejte spodnje teme, vendar upoštevajte, da morate dokončati postopke v spodaj navedenem vrstnem redu:</span><span class="sxs-lookup"><span data-stu-id="0ba52-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="0ba52-120">Ustvarjanje polj in entitet po meri</span><span class="sxs-lookup"><span data-stu-id="0ba52-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="0ba52-121">Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete</span><span class="sxs-lookup"><span data-stu-id="0ba52-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="0ba52-122">Nastavitev polj po meri kot cenovnih razsežnosti </span><span class="sxs-lookup"><span data-stu-id="0ba52-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="0ba52-123">Posodabljanje atributov vtičnikov za vključitev novih cenovnih razsežnosti</span><span class="sxs-lookup"><span data-stu-id="0ba52-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="0ba52-124">Določanje cene časa človeških virov</span><span class="sxs-lookup"><span data-stu-id="0ba52-124">Pricing human resource time</span></span>
<span data-ttu-id="0ba52-125">Kako organizacija določi cene za čas človeških virov je pogosto pomemben strateški vidik, ki neposredno vpliva na dobičkonosnost organizacije.</span><span class="sxs-lookup"><span data-stu-id="0ba52-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="0ba52-126">Ko se je vaša organizacija pripravljena opredeliti, kako želi nastaviti mere stroškov in deleže obračunavanja za čas človeških virov, sodelujte s finančnimi ekipami in vodji praks.</span><span class="sxs-lookup"><span data-stu-id="0ba52-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="0ba52-127">Drugi vidiki določanja cen vključujejo tudi to, ali naj se znova uporabijo polja ali entitete, ki trenutno niso cenovne razsežnosti, vendar se uporabljajo kot cenovna razsežnost za vašo organizacijo.</span><span class="sxs-lookup"><span data-stu-id="0ba52-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="0ba52-128">Polja, kot sta **Kategorija transakcije** (**msdyn_transactioncategory**) in **Viri, ki jih je mogoče rezervirati** (**bookableresource**), so primeri možnih razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="0ba52-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="0ba52-129">Razmislite, ali naj bo vaša cenovna razsežnost tabela ali nabor možnosti.</span><span class="sxs-lookup"><span data-stu-id="0ba52-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="0ba52-130">Če predvidevate spremembe vrednosti razsežnosti, ki bodo presegle vrednost 10 ali 12, in potrebujete dodatne atribute za te vrednosti, namesto nabora možnosti raje ustvarite entiteto.</span><span class="sxs-lookup"><span data-stu-id="0ba52-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="0ba52-131">Za vzdrževanje nabora možnosti, na primer dodajanje ali odstranjevanje vrednosti, je potreben skrbnik ali razvijalec, dodajanje novih vrstic v tabelo pa lahko opravi večina poslovnih uporabnikov.</span><span class="sxs-lookup"><span data-stu-id="0ba52-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="0ba52-132">Spodnji primer prikazuje deleže obračunavanja, ki so nastavljeni na podlagi vloge in organizacijske enote organizacije vira, ki ji pripada vir.</span><span class="sxs-lookup"><span data-stu-id="0ba52-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="0ba52-133">Mere stroškov običajno temeljijo na razponu plače zaposlenega in organizacijski enoti, ki ji pripada.</span><span class="sxs-lookup"><span data-stu-id="0ba52-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="0ba52-134">V tem primeru bodo tabele z deležem obračunavanja in mero stroškov videti, kot je prikazano spodaj.</span><span class="sxs-lookup"><span data-stu-id="0ba52-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="0ba52-135">**Vzorčni deleži obračunavanja**</span><span class="sxs-lookup"><span data-stu-id="0ba52-135">**Sample bill rates**</span></span>

| <span data-ttu-id="0ba52-136">Vloga</span><span class="sxs-lookup"><span data-stu-id="0ba52-136">Role</span></span>        | <span data-ttu-id="0ba52-137">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="0ba52-137">Org Unit</span></span>    |<span data-ttu-id="0ba52-138">Enota</span><span class="sxs-lookup"><span data-stu-id="0ba52-138">Unit</span></span>      |<span data-ttu-id="0ba52-139">Cena</span><span class="sxs-lookup"><span data-stu-id="0ba52-139">Price</span></span>      |<span data-ttu-id="0ba52-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="0ba52-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="0ba52-141">Developer</span><span class="sxs-lookup"><span data-stu-id="0ba52-141">Developer</span></span>   | <span data-ttu-id="0ba52-142">Contoso, ZDA</span><span class="sxs-lookup"><span data-stu-id="0ba52-142">Contoso US</span></span>  |<span data-ttu-id="0ba52-143">Ura</span><span class="sxs-lookup"><span data-stu-id="0ba52-143">Hour</span></span> | <span data-ttu-id="0ba52-144">200</span><span class="sxs-lookup"><span data-stu-id="0ba52-144">200</span></span>|<span data-ttu-id="0ba52-145">USD</span><span class="sxs-lookup"><span data-stu-id="0ba52-145">USD</span></span>     |
| <span data-ttu-id="0ba52-146">Developer</span><span class="sxs-lookup"><span data-stu-id="0ba52-146">Developer</span></span>   | <span data-ttu-id="0ba52-147">Contoso Indija</span><span class="sxs-lookup"><span data-stu-id="0ba52-147">Contoso India</span></span> |<span data-ttu-id="0ba52-148">Ura</span><span class="sxs-lookup"><span data-stu-id="0ba52-148">Hour</span></span>|   <span data-ttu-id="0ba52-149">112</span><span class="sxs-lookup"><span data-stu-id="0ba52-149">112</span></span>|<span data-ttu-id="0ba52-150">USD</span><span class="sxs-lookup"><span data-stu-id="0ba52-150">USD</span></span>     |


<span data-ttu-id="0ba52-151">**Vzorčne mere stroškov**</span><span class="sxs-lookup"><span data-stu-id="0ba52-151">**Sample cost rates**</span></span>

| <span data-ttu-id="0ba52-152">Razpon plače</span><span class="sxs-lookup"><span data-stu-id="0ba52-152">Salary Band</span></span>     | <span data-ttu-id="0ba52-153">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="0ba52-153">Org Unit</span></span>    |<span data-ttu-id="0ba52-154">Enota</span><span class="sxs-lookup"><span data-stu-id="0ba52-154">Unit</span></span>      |<span data-ttu-id="0ba52-155">Cena</span><span class="sxs-lookup"><span data-stu-id="0ba52-155">Price</span></span>      |<span data-ttu-id="0ba52-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="0ba52-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="0ba52-157">Moje podjetje_razpon1</span><span class="sxs-lookup"><span data-stu-id="0ba52-157">My company_Band1</span></span> | <span data-ttu-id="0ba52-158">Contoso, ZDA</span><span class="sxs-lookup"><span data-stu-id="0ba52-158">Contoso US</span></span>  |<span data-ttu-id="0ba52-159">Ura</span><span class="sxs-lookup"><span data-stu-id="0ba52-159">Hour</span></span> | <span data-ttu-id="0ba52-160">145</span><span class="sxs-lookup"><span data-stu-id="0ba52-160">145</span></span>|<span data-ttu-id="0ba52-161">USD</span><span class="sxs-lookup"><span data-stu-id="0ba52-161">USD</span></span>     |
| <span data-ttu-id="0ba52-162">Moje podjetje_razpon2</span><span class="sxs-lookup"><span data-stu-id="0ba52-162">My company_Band2</span></span> | <span data-ttu-id="0ba52-163">Contoso Indija</span><span class="sxs-lookup"><span data-stu-id="0ba52-163">Contoso India</span></span> |<span data-ttu-id="0ba52-164">Ura</span><span class="sxs-lookup"><span data-stu-id="0ba52-164">Hour</span></span>|   <span data-ttu-id="0ba52-165">67</span><span class="sxs-lookup"><span data-stu-id="0ba52-165">67</span></span>|<span data-ttu-id="0ba52-166">USD</span><span class="sxs-lookup"><span data-stu-id="0ba52-166">USD</span></span>     |
