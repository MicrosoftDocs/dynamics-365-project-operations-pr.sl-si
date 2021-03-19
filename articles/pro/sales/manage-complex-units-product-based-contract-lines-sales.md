---
title: Upravljanje kompleksnih enot za podrobnosti pogodbe, ki temeljijo na izdelkih – poenostavljena različica
description: V tej temi so na voljo informacije o podpori prodaje naročniških izdelkov.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273353"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="74518-103">Upravljanje kompleksnih enot za podrobnosti pogodbe, ki temeljijo na izdelkih – poenostavljena različica</span><span class="sxs-lookup"><span data-stu-id="74518-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="74518-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="74518-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="74518-105">Aplikacija Dynamics 365 Project Operations uporablja količnike za količino, ki podpirajo prodajo naročniških izdelkov.</span><span class="sxs-lookup"><span data-stu-id="74518-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="74518-106">Pri naročniških izdelkih je količina v pogodbi ali podrobnostih pogodbe projekta izražena kot število mesecev uporabe.</span><span class="sxs-lookup"><span data-stu-id="74518-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="74518-107">Cena naročniške programske opreme je shranjena v katalogu kot cena na uporabnika na mesec.</span><span class="sxs-lookup"><span data-stu-id="74518-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="74518-108">Med prodajnim postopkom je cena v podrobnostih pogodbe običajno cena na uporabnika na mesec, ki jo je izpogajal in znižal prodajni agent.</span><span class="sxs-lookup"><span data-stu-id="74518-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="74518-109">Vsak posel ima različno število uporabnikov in različno število naročniških mesecev.</span><span class="sxs-lookup"><span data-stu-id="74518-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="74518-110">Količina, ki se uporablja za izračun zneska podrobnosti pogodbe, je produkt števila uporabnikov in števila mesecev naročnine.</span><span class="sxs-lookup"><span data-stu-id="74518-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="74518-111">Za podporo te vrste prodaje rešitev Project Operations podpira koncept *količniki za količino*.</span><span class="sxs-lookup"><span data-stu-id="74518-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="74518-112">Količniki za količino temeljijo na atributih izdelka.</span><span class="sxs-lookup"><span data-stu-id="74518-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="74518-113">Ko konfigurirate določene lastnosti za izdelek, lahko označite podmnožico teh lastnosti ali vseh lastnosti kot količnike za količino.</span><span class="sxs-lookup"><span data-stu-id="74518-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="74518-114">Project Operations preveri, da so kot količniki za količino označene samo številske lastnosti ali lastnosti izdelka s številskim podatkovnim tipom.</span><span class="sxs-lookup"><span data-stu-id="74518-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="74518-115">Ko je izdelek s konfiguriranimi količniki za količino dodan v podrobnosti pogodbe, polje **Količina** postane samo za branje.</span><span class="sxs-lookup"><span data-stu-id="74518-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="74518-116">Ko vnesete vrednosti za lastnosti izdelka, ki so količniki za količino, Project Operations izračuna količino podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="74518-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="74518-117">Dynamics 365 Sales ima lahko na primer te lastnosti:</span><span class="sxs-lookup"><span data-stu-id="74518-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="74518-118">**Št. uporabnikov**: število uporabnikov.</span><span class="sxs-lookup"><span data-stu-id="74518-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="74518-119">**Št. mesecev**: število mesecev naročnine.</span><span class="sxs-lookup"><span data-stu-id="74518-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="74518-120">**Inventarna številka izdelka**: inventarna številka (SKU) za izdelek</span><span class="sxs-lookup"><span data-stu-id="74518-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="74518-121">Lastnosti **Št. uporabnikov** in **Št. mesecev** lahko označite kot količnike za količino tako, da uredite lastnosti vrstice izdelkov.</span><span class="sxs-lookup"><span data-stu-id="74518-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="74518-122">Za ustvarjanje količnikov za količino za lastnosti izdelkov, izvedite naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="74518-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="74518-123">V možnosti **Project Operations** izberite **Sales-Products**.</span><span class="sxs-lookup"><span data-stu-id="74518-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="74518-124">Odprite izdelek, za katerega morate nastaviti količnike za količino.</span><span class="sxs-lookup"><span data-stu-id="74518-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="74518-125">Prepričajte se, da ima izdelek že nastavljene lastnosti.</span><span class="sxs-lookup"><span data-stu-id="74518-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="74518-126">Na strani **Podatki o projektu** izberite zavihek **Količniki za količino**.</span><span class="sxs-lookup"><span data-stu-id="74518-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="74518-127">V podmreži izberite **+ Nov izračun polja**.</span><span class="sxs-lookup"><span data-stu-id="74518-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="74518-128">Vnesite ime za **Količnik za količino** in izberite vrednost lastnosti, ki se preslika v izračun polja.</span><span class="sxs-lookup"><span data-stu-id="74518-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="74518-129">Shranite in zaprite obrazec.</span><span class="sxs-lookup"><span data-stu-id="74518-129">Save and close the form.</span></span>
7. <span data-ttu-id="74518-130">Ponovite korake 2–6 za vse lastnosti, ki skupaj predstavljajo količino za podrobnosti pogodbe, ki temeljijo na izdelkih.</span><span class="sxs-lookup"><span data-stu-id="74518-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="74518-131">Z nastavljenimi količniki za količino, ko uporabnik ustvari podrobnosti pogodbe za ta izdelek, je količina podrobnosti pogodbe zaklenjena.</span><span class="sxs-lookup"><span data-stu-id="74518-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="74518-132">Količina je nato izračunana kot izdelke vrednosti lastnosti za te podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="74518-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]