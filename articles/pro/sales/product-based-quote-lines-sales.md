---
title: Pregled podrobnosti ponudb, ki temeljijo na izdelkih – poenostavljeno
description: V tej temi so na voljo informacije o delu z vrsticami ponudb, ki temeljijo na izdelkih.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272588"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="93aab-103">Pregled podrobnosti ponudb, ki temeljijo na izdelkih – poenostavljeno</span><span class="sxs-lookup"><span data-stu-id="93aab-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="93aab-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="93aab-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="93aab-105">V aplikaciji Dynamics 365 Project Operations lahko ustvarite vrstice ponudb, ki temeljijo na izdelku.</span><span class="sxs-lookup"><span data-stu-id="93aab-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="93aab-106">Vrstice ponudb, ki temeljijo na izdelkih, lahko ročno dodate ali pa izberete izdelke iz kataloga izdelkov.</span><span class="sxs-lookup"><span data-stu-id="93aab-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="93aab-107">Katalog izdelkov</span><span class="sxs-lookup"><span data-stu-id="93aab-107">Product catalog</span></span>

<span data-ttu-id="93aab-108">Vsak izdelek v katalogu izdelkov ima privzeto enoto in skupino enot.</span><span class="sxs-lookup"><span data-stu-id="93aab-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="93aab-109">Če ima več izdelkov enak nabor atributov, lahko ustvarite družino izdelkov, ki ima prav tako te atribute.</span><span class="sxs-lookup"><span data-stu-id="93aab-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="93aab-110">Podjetje na primer prodaja naročniške licence za različne vrste programske opreme.</span><span class="sxs-lookup"><span data-stu-id="93aab-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="93aab-111">Vsa naročniška programska oprema ima ta dva atributa:</span><span class="sxs-lookup"><span data-stu-id="93aab-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="93aab-112">Število uporabnikov</span><span class="sxs-lookup"><span data-stu-id="93aab-112">Number of users</span></span>
- <span data-ttu-id="93aab-113">Trajanje naročnine, merjene v mesecih</span><span class="sxs-lookup"><span data-stu-id="93aab-113">A subscription duration measured in months</span></span>

<span data-ttu-id="93aab-114">To vrsto kataloga upravljajte tako, da ustvarite družino izdelkov, ki se imenuje **Naročniška programska oprema**, in kot atributa dodate število uporabnikov in trajanje naročnine.</span><span class="sxs-lookup"><span data-stu-id="93aab-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="93aab-115">Nato lahko posamezne elemente dodate v družino izdelkov **Naročniška programska oprema**.</span><span class="sxs-lookup"><span data-stu-id="93aab-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="93aab-116">Dodajanje elementov kataloga izdelkov v projektno ponudbo</span><span class="sxs-lookup"><span data-stu-id="93aab-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="93aab-117">Strani **Ponudba za projekt** in **Projektna pogodba** imata razdelke za vrstice, ki temeljijo na projektih, in vrstice, ki temeljijo na izdelkih.</span><span class="sxs-lookup"><span data-stu-id="93aab-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="93aab-118">Pri vrsticah, ki temeljijo na izdelku, spustni seznam v vrstici ponudbe ali vrstici projekte pogodbe vključuje vse izdelke in enote na ceniku izdelkov.</span><span class="sxs-lookup"><span data-stu-id="93aab-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="93aab-119">Dodajate lahko tudi izdelke, ki niso del cenika izdelkov.</span><span class="sxs-lookup"><span data-stu-id="93aab-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="93aab-120">Poleg tega lahko izberete izdelke iz drugih cenikov ali pa neposredno iz kataloga izdelkov.</span><span class="sxs-lookup"><span data-stu-id="93aab-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="93aab-121">Ko izberete izdelke neposredno iz kataloga izdelkov, se za prikaz prodajne cene izdelka uporabi privzeti cenik tega izdelka.</span><span class="sxs-lookup"><span data-stu-id="93aab-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="93aab-122">Če privzeti cenik ni nastavljen, je cena nastavljena na nič (0).</span><span class="sxs-lookup"><span data-stu-id="93aab-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="93aab-123">Če vrstica ponudbe temelji na katalogu izdelkov, lahko prodajno ceno preglasite neposredno v vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="93aab-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="93aab-124">Vrstica ponudbe v polju **Cene** z dvema razpoložljivima vrednostma:</span><span class="sxs-lookup"><span data-stu-id="93aab-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="93aab-125">**Preglasi oblikovanje cene**</span><span class="sxs-lookup"><span data-stu-id="93aab-125">**Override Pricing**</span></span>
- <span data-ttu-id="93aab-126">**Uporabi privzeto**</span><span class="sxs-lookup"><span data-stu-id="93aab-126">**Use Default**</span></span>

<span data-ttu-id="93aab-127">Če izberete možnost **Preglasi oblikovanje cene**, privzeta cena ni nastavljena.</span><span class="sxs-lookup"><span data-stu-id="93aab-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="93aab-128">Namesto tega morate ceno za izdelek vnesti v vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="93aab-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="93aab-129">Če izberete možnost **Uporabi privzeto**, je uporabljena privzeta prodajna cena in polje je zaklenjeno za urejanje.</span><span class="sxs-lookup"><span data-stu-id="93aab-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="93aab-130">Privzete prodajne cene se vnesejo v vrstice, ki temeljijo na izdelkih, v ponudbi.</span><span class="sxs-lookup"><span data-stu-id="93aab-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="93aab-131">Polje **Oblikovanje cen** je nato nastavljeno na **Preglasi oblikovanje cene**, tako da lahko uredite privzeto ceno v vrsticah ponudbe.</span><span class="sxs-lookup"><span data-stu-id="93aab-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="93aab-132">Ta preglasitev vedenja podrobnosti, ki temeljijo na izdelkih, v aplikaciji Dynamics 365 Sales je značilna za aplikacijo Project Operations.</span><span class="sxs-lookup"><span data-stu-id="93aab-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]