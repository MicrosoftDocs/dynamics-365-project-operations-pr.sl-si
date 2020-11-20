---
title: Pregled podrobnosti pogodbe, ki temeljijo na izdelkih – poenostavljeno
description: V tej temi so na voljo informacije o podrobnostih pogodb, ki temeljijo na izdelkih.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177891"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="951a3-103">Pregled podrobnosti pogodbe, ki temeljijo na izdelkih – poenostavljeno</span><span class="sxs-lookup"><span data-stu-id="951a3-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="951a3-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="951a3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="951a3-105">V storitvi Dynamics 365 Project Operations lahko ustvarite podrobnosti pogodb, ki temeljijo na izdelkih.</span><span class="sxs-lookup"><span data-stu-id="951a3-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="951a3-106">Podrobnosti pogodb so lahko ročno ustvarjene vrstice ali pa artikli iz kataloga izdelkov.</span><span class="sxs-lookup"><span data-stu-id="951a3-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="951a3-107">Katalog izdelkov</span><span class="sxs-lookup"><span data-stu-id="951a3-107">Product catalog</span></span>

<span data-ttu-id="951a3-108">Izdelki v katalogu izdelkov imajo privzeto enoto in skupino enot.</span><span class="sxs-lookup"><span data-stu-id="951a3-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="951a3-109">Če ima več izdelkov enak nabor atributov, lahko ustvarite družino izdelkov, ki ima prav tako te atribute.</span><span class="sxs-lookup"><span data-stu-id="951a3-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="951a3-110">Vsi izdelki v eni družini izdelkov podedujejo isti nabor atributov.</span><span class="sxs-lookup"><span data-stu-id="951a3-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="951a3-111">Podjetje na primer prodaja naročniške licence za različne vrste programske opreme.</span><span class="sxs-lookup"><span data-stu-id="951a3-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="951a3-112">Vsa naročniška programska oprema ima ta dva atributa:</span><span class="sxs-lookup"><span data-stu-id="951a3-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="951a3-113">Število uporabnikov</span><span class="sxs-lookup"><span data-stu-id="951a3-113">Number of users</span></span>
- <span data-ttu-id="951a3-114">Trajanje naročnine (v mesecih)</span><span class="sxs-lookup"><span data-stu-id="951a3-114">Subscription duration (in months)</span></span>

<span data-ttu-id="951a3-115">Če želite vzdrževati to vrsto kataloga, ustvarite družino izdelkov z imenom **Programska oprema z naročnino**.</span><span class="sxs-lookup"><span data-stu-id="951a3-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="951a3-116">V družino izdelkov dodajte atribute, **število uporabnikov** in **trajanje naročnine**.</span><span class="sxs-lookup"><span data-stu-id="951a3-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="951a3-117">Nato dodajte posamezne izdelke v družino izdelkov **Programska oprema z naročnino**.</span><span class="sxs-lookup"><span data-stu-id="951a3-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="951a3-118">Dodajanje elementov kataloga izdelkov v projektno pogodbo</span><span class="sxs-lookup"><span data-stu-id="951a3-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="951a3-119">Projektne pogodbe imajo razdelke za dve vrsti vrstic: vrstice, ki temeljijo na projektih, in vrstice, ki temeljijo na izdelkih.</span><span class="sxs-lookup"><span data-stu-id="951a3-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="951a3-120">Podrobnosti, ki temeljijo na izdelkih, vključujejo vse izdelke in enote v ceniku izdelkov v pogodbi.</span><span class="sxs-lookup"><span data-stu-id="951a3-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="951a3-121">Dodajate lahko tudi izdelke, ki niso del cenika izdelkov v pogodbi.</span><span class="sxs-lookup"><span data-stu-id="951a3-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="951a3-122">Izberete lahko izdelke iz drugih cenikov ali pa neposredno iz kataloga izdelkov.</span><span class="sxs-lookup"><span data-stu-id="951a3-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="951a3-123">Ko izberete izdelke neposredno iz kataloga izdelkov, se za prodajno ceno izdelka uporabi privzeti cenik tega izdelka.</span><span class="sxs-lookup"><span data-stu-id="951a3-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="951a3-124">Če privzeti cenovni seznam ni nastavljen, je cena nastavljena na 0 (nič).</span><span class="sxs-lookup"><span data-stu-id="951a3-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="951a3-125">Če podrobnost pogodbe temelji na katalogu izdelkov, lahko prodajno ceno preglasite neposredno v podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="951a3-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="951a3-126">Podrobnost pogodbe ima polje **Cene** z dvema vrednostma:</span><span class="sxs-lookup"><span data-stu-id="951a3-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="951a3-127">**Preglasi oblikovanje cene**</span><span class="sxs-lookup"><span data-stu-id="951a3-127">**Override pricing**</span></span>
- <span data-ttu-id="951a3-128">**Uporabi privzeto**</span><span class="sxs-lookup"><span data-stu-id="951a3-128">**Use default**</span></span>

<span data-ttu-id="951a3-129">Če nastavite polje **Cene** na **Preglasi oblikovanje cene**, privzeta cena ni nastavljena.</span><span class="sxs-lookup"><span data-stu-id="951a3-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="951a3-130">Vnesite ceno za izdelek pri podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="951a3-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="951a3-131">Če polje nastavite na **Uporabi privzeto**, se uporablja privzeta prodajna cena in polja ni mogoče urejati.</span><span class="sxs-lookup"><span data-stu-id="951a3-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="951a3-132">Ko namestite Project Operations, se privzete prodajne cene vnesejo v vrstice v pogodbi, ki temeljijo na izdelkih.</span><span class="sxs-lookup"><span data-stu-id="951a3-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="951a3-133">Polje **Oblikovanje cen** je nastavljeno na **Preglasi oblikovanje cene**, tako da lahko uredite privzeto ceno v podrobnostih pogodbe.</span><span class="sxs-lookup"><span data-stu-id="951a3-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="951a3-134">To je preglasitev vedenja podrobnosti, ki temeljijo na izdelkih, v storitvi Dynamics 365 Sales, ki je specifična za Project Operations.</span><span class="sxs-lookup"><span data-stu-id="951a3-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
