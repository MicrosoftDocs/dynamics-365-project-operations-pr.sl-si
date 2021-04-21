---
title: Ceniki za izdelke
description: Ta tema vsebuje informacije o cenikih pri določanju cen v katalogu, ki se uporabljajo za ponudbe in pogodbe za projekte.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877510"
---
# <a name="product-price-lists"></a><span data-ttu-id="03934-103">Ceniki za izdelke</span><span class="sxs-lookup"><span data-stu-id="03934-103">Product price lists</span></span>

<span data-ttu-id="03934-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="03934-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="03934-105">V aplikaciji Project Operations **ceniki izdelkov** in s tem povezane entitete elementa cenika podpirajo funkcionalnost določanja cen izdelkov na podlagi ponudb in pogodbenih postavk izdelka.</span><span class="sxs-lookup"><span data-stu-id="03934-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="03934-106">Za izdelke, ki se uporabljajo na projektih, se uporabljajo zapisi elementa cenika za cenike projekta.</span><span class="sxs-lookup"><span data-stu-id="03934-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="03934-107">Izdelke morate nastaviti tako, da imajo v katalogu izdelkov privzete stroške in cenike.</span><span class="sxs-lookup"><span data-stu-id="03934-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="03934-108">Če želite konfigurirati privzete stroške in cenike, uporabite cenik, standardne stroške in trenutne stroške.</span><span class="sxs-lookup"><span data-stu-id="03934-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="03934-109">Privzeti ceniki se v vrstici ponudbe ali v vrstici projektne pogodbe uporabljajo le, če sistem ne najde vrstice cenika za izdelek na ceniku izdelkov za ponudbo ali projektno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="03934-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="03934-110">Lastno ceno v vrsticah kataloga izdelkov lahko spremenite v različnih ponudbah.</span><span class="sxs-lookup"><span data-stu-id="03934-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="03934-111">Ta možnost je pomembna, saj ne morete določiti dobička iz poslovanja v projektnih obveznostih, če ne spremljate natančno stroškov.</span><span class="sxs-lookup"><span data-stu-id="03934-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="03934-112">Kot lastna cena se privzeto uporablja standardna cena.</span><span class="sxs-lookup"><span data-stu-id="03934-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="03934-113">Vendar pa privzeto lastno ceno lahko posodobite v vrstici ponudbe, če za to ponudbo obstaja druga lastna cena.</span><span class="sxs-lookup"><span data-stu-id="03934-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="03934-114">Elementi cenika</span><span class="sxs-lookup"><span data-stu-id="03934-114">Price list items</span></span>

<span data-ttu-id="03934-115">Izdelke iz kataloga izdelkov lahko dodajate različnim cenikom.</span><span class="sxs-lookup"><span data-stu-id="03934-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="03934-116">Vrstice cenika za izdelke se vedno sklicujejo na določeno enoto.</span><span class="sxs-lookup"><span data-stu-id="03934-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="03934-117">Ceno za izdelek v elementih cenika lahko konfigurirate kot znesek valute.</span><span class="sxs-lookup"><span data-stu-id="03934-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="03934-118">Lahko pa jo konfigurirate kot funkcijo cenika, trenutnih stroškov ali standardnih stroškov.</span><span class="sxs-lookup"><span data-stu-id="03934-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="03934-119">Funkcionalnost določanja cen podpira različne načine zaokroževanja, ko so cene izdelka konfigurirane kot funkcija cenika, standardnih stroškov ali trenutnih stroškov.</span><span class="sxs-lookup"><span data-stu-id="03934-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="03934-120">Izkoristite lahko več načinov oblikovanja cen in zaokroževanja ter tudi povežete sezname popustov z elementi cenika.</span><span class="sxs-lookup"><span data-stu-id="03934-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="03934-121">Privzeti cenik izdelkov</span><span class="sxs-lookup"><span data-stu-id="03934-121">Default product price list</span></span>
<span data-ttu-id="03934-122">Vsak zapis stranke ima polje **Privzeti cenik**, kjer lahko navedete cenik, ki ustreza valuti stranke.</span><span class="sxs-lookup"><span data-stu-id="03934-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="03934-123">Privzeta vrednost ni samodejno vnesena v to polje.</span><span class="sxs-lookup"><span data-stu-id="03934-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="03934-124">Če imate z določeno stranko poseben dogovor o cenah, lahko uporabite to polje, da povežete cenik s to stranko.</span><span class="sxs-lookup"><span data-stu-id="03934-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="03934-125">Entitete »Priložnost«, »Ponudba« in »Projektna pogodba« uporabljajo spodnji vrstni red za vnos privzetih cenikov izdelkov.</span><span class="sxs-lookup"><span data-stu-id="03934-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="03934-126">Isti vrstni red se uporablja za cenike projekta.</span><span class="sxs-lookup"><span data-stu-id="03934-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="03934-127">Citat</span><span class="sxs-lookup"><span data-stu-id="03934-127">Quote</span></span>
2.  <span data-ttu-id="03934-128">Priložnost</span><span class="sxs-lookup"><span data-stu-id="03934-128">Opportunity</span></span>
3.  <span data-ttu-id="03934-129">Stranki</span><span class="sxs-lookup"><span data-stu-id="03934-129">Customer</span></span>
4.  <span data-ttu-id="03934-130">Globalne nastavitve</span><span class="sxs-lookup"><span data-stu-id="03934-130">Global settings</span></span> 

<span data-ttu-id="03934-131">Polje **Izdelek** v vrstici ponudbe privzeto navaja vse dejavne izdelke v ceniku izdelkov za ponudbo.</span><span class="sxs-lookup"><span data-stu-id="03934-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="03934-132">Če je bil izdelek dezaktiviran ali če gre za osnutek izdelka, ga ni na seznamu, tudi če je na ceniku.</span><span class="sxs-lookup"><span data-stu-id="03934-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="03934-133">Vrstice kataloga izdelkov se dodajo kot vrstice računa na prvem računu, ki je ustvarjen za projektno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="03934-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="03934-134">Na osnutku računa lahko izbrišete te vrstice računa.</span><span class="sxs-lookup"><span data-stu-id="03934-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="03934-135">V tem primeru se vrstice prikažejo na naslednjem računu, dokler ni fakturiran oz. dokler se ne pošlje stranki.</span><span class="sxs-lookup"><span data-stu-id="03934-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="03934-136">Ne morete fakturirati delne količine vrstice računa izdelka.</span><span class="sxs-lookup"><span data-stu-id="03934-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="03934-137">Ko so vrstice izdelka iz projektne pogodbe fakturirane, se ustvarijo dejanske vrednosti.</span><span class="sxs-lookup"><span data-stu-id="03934-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="03934-138">Vendar pa te dejanske vrednosti niso povezane s povezano entiteto projekta.</span><span class="sxs-lookup"><span data-stu-id="03934-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="03934-139">Z drugimi besedami, vrstice projektne pogodbe, ki temeljijo na izdelku, so neodvisne od uporabe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="03934-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
