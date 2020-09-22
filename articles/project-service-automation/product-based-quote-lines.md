---
title: Vrstice ponudb, ki temeljijo na izdelkih
description: V tej temi so na voljo informacije o vrsticah ponudb, ki temeljijo na izdelkih.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 76b90c95-1b3a-4704-a13f-9d7099b83f4c
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d8bb36fbfe8d01aa26faf5515ca218ad836126b7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755776"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="cc661-103">Vrstice ponudb, ki temeljijo na izdelkih</span><span class="sxs-lookup"><span data-stu-id="cc661-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="cc661-104">V aplikaciji Dynamics 365 Project Service Automation lahko ustvarite vrstice ponudb, ki temeljijo na izdelku.</span><span class="sxs-lookup"><span data-stu-id="cc661-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="cc661-105">Vrstice ponudb, ki temeljijo na izdelkih, so lahko vrstice izdelkov, ki niso v katalogu, ali pa artikli iz kataloga izdelkov.</span><span class="sxs-lookup"><span data-stu-id="cc661-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="cc661-106">Katalog izdelkov</span><span class="sxs-lookup"><span data-stu-id="cc661-106">Product catalog</span></span>

<span data-ttu-id="cc661-107">Izdelki v katalogu izdelkov Dynamics 365 imajo privzeto enoto in skupino enot.</span><span class="sxs-lookup"><span data-stu-id="cc661-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="cc661-108">Če ima več izdelkov enak nabor atributov, lahko ustvarite družino izdelkov, ki ima prav tako te atribute.</span><span class="sxs-lookup"><span data-stu-id="cc661-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="cc661-109">Vsi izdelki v eni družini izdelkov podedujejo isti nabor atributov.</span><span class="sxs-lookup"><span data-stu-id="cc661-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="cc661-110">Podjetje na primer prodaja naročniške licence za različno programsko opremo.</span><span class="sxs-lookup"><span data-stu-id="cc661-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="cc661-111">Vsa naročniška programska oprema ima ta dva atributa:</span><span class="sxs-lookup"><span data-stu-id="cc661-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="cc661-112">Število uporabnikov</span><span class="sxs-lookup"><span data-stu-id="cc661-112">Number of users</span></span> 
- <span data-ttu-id="cc661-113">Trajanje naročnine (v mesecih)</span><span class="sxs-lookup"><span data-stu-id="cc661-113">Subscription duration (in months)</span></span>

<span data-ttu-id="cc661-114">Takšno vrsto kataloga najlažje upravljate tako, da ustvarite družino izdelkov, ki se imenuje **Naročniška programska oprema** in ima atributa **Število uporabnikov** in **Trajanje naročnine**.</span><span class="sxs-lookup"><span data-stu-id="cc661-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="cc661-115">Nato lahko dodate posamezne izdelke, na primer **Dynamics 365 Sales** ali **Dynamics 365 Field Service** v družino izdelkov **Naročniška programska oprema**.</span><span class="sxs-lookup"><span data-stu-id="cc661-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="cc661-116">Dodajanje elementov kataloga izdelkov v projektno ponudbo</span><span class="sxs-lookup"><span data-stu-id="cc661-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="cc661-117">Strani projektne ponudbe in projektne pogodbe imajo razdelke za dve vrsti vrstic: vrstice, ki temeljijo na projektih, in vrstice, ki temeljijo na izdelkih.</span><span class="sxs-lookup"><span data-stu-id="cc661-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="cc661-118">Pri vrsticah, ki temeljijo na izdelku, se Dynamics 365 uporablja za dodajanje elementov iz kataloga izdelkov v ponudbo.</span><span class="sxs-lookup"><span data-stu-id="cc661-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="cc661-119">Spustni seznam v vrstici ponudbe ali vrstici projekte pogodbe vključuje vse izdelke in enote na ceniku izdelkov, ki je priložen ponudbi ali projektni pogodbi.</span><span class="sxs-lookup"><span data-stu-id="cc661-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="cc661-120">Dodajate lahko tudi izdelke, ki niso del cenika izdelkov v ponudbi.</span><span class="sxs-lookup"><span data-stu-id="cc661-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="cc661-121">Poleg tega lahko izberete izdelke iz drugih cenikov ali pa neposredno iz kataloga izdelkov.</span><span class="sxs-lookup"><span data-stu-id="cc661-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="cc661-122">Ko izberete izdelke neposredno iz kataloga izdelkov, se za prikaz prodajne cene izdelka uporabi privzeti cenik tega izdelka.</span><span class="sxs-lookup"><span data-stu-id="cc661-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="cc661-123">Če privzeti cenovni seznam ni nastavljen, je cena nastavljena na 0 (nič).</span><span class="sxs-lookup"><span data-stu-id="cc661-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="cc661-124">Če vrstica ponudbe temelji na katalogu izdelkov, lahko prodajno ceno preglasite neposredno v vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="cc661-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="cc661-125">Upoštevajte, da ima vrstica ponudbe v programu Dynamics 365 polje **Oblikovanje cen**.</span><span class="sxs-lookup"><span data-stu-id="cc661-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="cc661-126">Na voljo sta dve vrednosti:</span><span class="sxs-lookup"><span data-stu-id="cc661-126">Two values are available:</span></span>

- <span data-ttu-id="cc661-127">Preglasi oblikovanje cene</span><span class="sxs-lookup"><span data-stu-id="cc661-127">Override pricing</span></span>  
- <span data-ttu-id="cc661-128">Uporabi privzeto</span><span class="sxs-lookup"><span data-stu-id="cc661-128">Use default</span></span>

<span data-ttu-id="cc661-129">Če nastavite to polje na **Preglasi oblikovanje cene**, Dynamics 365 ne nastavi privzete cene.</span><span class="sxs-lookup"><span data-stu-id="cc661-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="cc661-130">Ceno za izdelek morate vnesti v vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="cc661-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="cc661-131">Če nastavite to polje na **Uporabi privzeto**, Dynamics 365 uporabi privzeto prodajno ceno in zaklene polje, da prepreči urejanje.</span><span class="sxs-lookup"><span data-stu-id="cc661-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="cc661-132">Ko namestite PSA, se privzete prodajne cene vnesejo v vrstice v ponudbi, ki temeljijo na izdelkih.</span><span class="sxs-lookup"><span data-stu-id="cc661-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="cc661-133">Polje **Oblikovanje cen** je nato nastavljeno na **Preglasi oblikovanje cene**, tako da lahko uredite privzeto ceno v vrsticah ponudbe.</span><span class="sxs-lookup"><span data-stu-id="cc661-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Nastavitev preglasitve oblikovanja cen](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="cc661-135">Količniki za količino za izdelke</span><span class="sxs-lookup"><span data-stu-id="cc661-135">Quantity factors for products</span></span>

<span data-ttu-id="cc661-136">PSA uporablja količnike za količino, ki podpirajo prodajo naročniških izdelkov.</span><span class="sxs-lookup"><span data-stu-id="cc661-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="cc661-137">Pri naročniških izdelkih je količina v vrstici ponudbe ali projektne pogodbe izražena kot število mesecev uporabe.</span><span class="sxs-lookup"><span data-stu-id="cc661-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="cc661-138">Običajno je cena naročniške programske opreme shranjena v katalogu kot cena na uporabnika na mesec.</span><span class="sxs-lookup"><span data-stu-id="cc661-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="cc661-139">Vendar pa lahko namesto tega uporabite druge opise časa.</span><span class="sxs-lookup"><span data-stu-id="cc661-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="cc661-140">Med prodajnim postopkom je cena v vrstici ponudbe običajno cena na uporabnika na mesec, ki jo je izpogajal in znižal prodajni agent za IT.</span><span class="sxs-lookup"><span data-stu-id="cc661-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="cc661-141">Vsak posel ima različno število uporabnikov in različno število naročniških mesecev.</span><span class="sxs-lookup"><span data-stu-id="cc661-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="cc661-142">Količina, ki se uporablja za izračun zneska vrstice ponudbe, je produkt števila uporabnikov in števila mesecev naročnine.</span><span class="sxs-lookup"><span data-stu-id="cc661-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="cc661-143">Za podporo tej vrsti prodaje je PSA uvedla koncept količnikov za količino.</span><span class="sxs-lookup"><span data-stu-id="cc661-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="cc661-144">Količniki za količino temeljijo na atributih izdelka v aplikaciji Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cc661-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="cc661-145">Ko konfigurirate določene lastnosti za izdelek, vam PSA omogoči označevanje podmnožice teh lastnosti ali vseh lastnosti kot količnikov za količino.</span><span class="sxs-lookup"><span data-stu-id="cc661-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="cc661-146">PSA preveri, da so kot količniki za količino označene samo številske lastnosti ali lastnosti izdelka s številskim podatkovnim tipom.</span><span class="sxs-lookup"><span data-stu-id="cc661-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="cc661-147">Ko je izdelek, za katerega so konfigurirani količniki za količino, dodan v vrstico ponudbe, polje **Količina** v vrstici ponudbe postane polje samo za branje.</span><span class="sxs-lookup"><span data-stu-id="cc661-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="cc661-148">Ko vnesete vrednosti za lastnosti izdelka, ki so količniki za količino, PSA izračuna količino vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="cc661-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="cc661-149">Dynamics 365 ima lahko na primer te lastnosti:</span><span class="sxs-lookup"><span data-stu-id="cc661-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="cc661-150">**Št. uporabnikov** – število uporabnikov.</span><span class="sxs-lookup"><span data-stu-id="cc661-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="cc661-151">**Št. mesecev** – število mesecev naročnine.</span><span class="sxs-lookup"><span data-stu-id="cc661-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="cc661-152">**Inventarna številka izdelka**</span><span class="sxs-lookup"><span data-stu-id="cc661-152">**Product SKU**</span></span> 

<span data-ttu-id="cc661-153">Lastnosti **Št. uporabnikov** in **Št. mesecev** lahko označite kot količnike za količino tako, da uredite lastnosti vrstice izdelkov.</span><span class="sxs-lookup"><span data-stu-id="cc661-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Označevanje lastnosti »Št. uporabnikov« in »Št. mesecev« kot količnikov za količino](media/basic-guide-11.png)
 
