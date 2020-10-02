---
title: Nastavitev prodajnega cenika
description: Ta tema vsebuje informacije o prodajnih cenikih pri določanju cen za projekt.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896481"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="30c7d-103">Nastavitev prodajnega cenika</span><span class="sxs-lookup"><span data-stu-id="30c7d-103">Sales price list setup</span></span>

<span data-ttu-id="30c7d-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="30c7d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="30c7d-105">Za projektne ponudbe in pogodbe ima cenik projekta drugačen vzorec preglasitve cen kot cenik izdelkov.</span><span class="sxs-lookup"><span data-stu-id="30c7d-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="30c7d-106">V vrstici ponudbe, ki temelji na katalogu izdelkov, lahko preglasite ceno za vloge in kategorije neposredno v vrstici ponudbe, saj vsaka vrstica ponudbe predstavlja natanko en kataloški izdelek.</span><span class="sxs-lookup"><span data-stu-id="30c7d-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="30c7d-107">V vrstici ponudbe, ki temelji na projektu, pa ni mogoče preglasiti cene za vloge in kategorije neposredno v vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="30c7d-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="30c7d-108">Cenik projekta lahko uporabite za delo z dvema različnima vzorcema preglasitve.</span><span class="sxs-lookup"><span data-stu-id="30c7d-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="30c7d-109">Priporočamo, da zaradi razlik v delovanju obeh pri preglasitvi cen uporabljate ločen cenik za svoje projektne vire in za katalog izdelkov.</span><span class="sxs-lookup"><span data-stu-id="30c7d-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="30c7d-110">Vsaka od naslednjih entitet ima lahko enega ali več povezanih prodajnih cenikov za cene v okviru projekta:</span><span class="sxs-lookup"><span data-stu-id="30c7d-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="30c7d-111">Stranka (račun)</span><span class="sxs-lookup"><span data-stu-id="30c7d-111">Customer (account)</span></span> 
- <span data-ttu-id="30c7d-112">Priložnost</span><span class="sxs-lookup"><span data-stu-id="30c7d-112">Opportunity</span></span> 
- <span data-ttu-id="30c7d-113">Ponudba</span><span class="sxs-lookup"><span data-stu-id="30c7d-113">Quote</span></span> 
- <span data-ttu-id="30c7d-114">Projektna pogodba</span><span class="sxs-lookup"><span data-stu-id="30c7d-114">Project Contract</span></span>

<span data-ttu-id="30c7d-115">Povezovanje teh entitet s cenikom določajo ceniki projektov.</span><span class="sxs-lookup"><span data-stu-id="30c7d-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="30c7d-116">S prodajnimi entitetami »Stranka«, »Priložnost«, »Ponudba«, »Projektna pogodba« lahko povežete enega ali več cenikov.</span><span class="sxs-lookup"><span data-stu-id="30c7d-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="30c7d-117">Privzeti cenik projekta ni samodejno vnesen v zapisu stranke.</span><span class="sxs-lookup"><span data-stu-id="30c7d-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="30c7d-118">Vendar pa lahko cenik projekta zapisu stranke ročno priložite.</span><span class="sxs-lookup"><span data-stu-id="30c7d-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="30c7d-119">Kljub temu cenik projekta ročno priložite samo, če imate s stranko dogovorjene posebne cene.</span><span class="sxs-lookup"><span data-stu-id="30c7d-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="30c7d-120">Ko je prodajni entiteti priloži cenik projekta, se preverijo naslednje informacije:</span><span class="sxs-lookup"><span data-stu-id="30c7d-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="30c7d-121">Kontekst cenika je **Prodaja**.</span><span class="sxs-lookup"><span data-stu-id="30c7d-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="30c7d-122">Valuta cenika se ujema z valuto stranke.</span><span class="sxs-lookup"><span data-stu-id="30c7d-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="30c7d-123">V projektni pogodbi se za samodejno nastavitev povezanih cenikov projekta uporabi naslednji vrstni red:</span><span class="sxs-lookup"><span data-stu-id="30c7d-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="30c7d-124">Citat</span><span class="sxs-lookup"><span data-stu-id="30c7d-124">Quote</span></span>
2. <span data-ttu-id="30c7d-125">Priložnost</span><span class="sxs-lookup"><span data-stu-id="30c7d-125">Opportunity</span></span>
3. <span data-ttu-id="30c7d-126">Stranki</span><span class="sxs-lookup"><span data-stu-id="30c7d-126">Customer</span></span> 
4. <span data-ttu-id="30c7d-127">Globalne nastavitve</span><span class="sxs-lookup"><span data-stu-id="30c7d-127">Global settings</span></span> 

<span data-ttu-id="30c7d-128">Ko je cenik projekta privzeto vnesen, sistem preveri, ali se valuta ujema z valuto stranke in ali so privzeti ceniki bili vneseni s kontekstom **Prodaja**.</span><span class="sxs-lookup"><span data-stu-id="30c7d-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="30c7d-129">Z entitetami »Stranka«, »Priložnost«, »Ponudba«, »Projektna pogodba« lahko povežete več cenikov projekta.</span><span class="sxs-lookup"><span data-stu-id="30c7d-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="30c7d-130">Ta zmožnost podpira datumsko določene privzete cene za dolgoročne projektne pogodbe, kjer boste morda potrebovali več kot en cenik, da se upošteva posodobitev cen, do katere pride zaradi inflacije.</span><span class="sxs-lookup"><span data-stu-id="30c7d-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="30c7d-131">Če pa imajo ceniki, ki jih povežete z entiteto »Stranka«, »Priložnost«, »Ponudba«, »Projektna pogodba«, prekrivajočo datumsko veljavnost, so lahko privzete cene napačne.</span><span class="sxs-lookup"><span data-stu-id="30c7d-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="30c7d-132">Zato se prepričajte, da ceniki projektov, ki imajo prekrivajočo datumsko veljavnost, niso povezani s temi entitetami.</span><span class="sxs-lookup"><span data-stu-id="30c7d-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
