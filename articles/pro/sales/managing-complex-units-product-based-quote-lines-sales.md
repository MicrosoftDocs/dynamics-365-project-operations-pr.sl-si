---
title: Upravljanje kompleksnih enot, na primer za uporabnika in za vsak mesec posebej, za podrobnosti ponudb, ki temeljijo na izdelkih
description: Ta tema vsebuje informacije o upravljanju kompleksnih enot za podrobnosti ponudb, ki temeljijo na izdelkih.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084688"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a><span data-ttu-id="d11aa-103">Upravljanje kompleksnih enot, na primer za uporabnika in za vsak mesec posebej, za podrobnosti ponudb, ki temeljijo na izdelkih</span><span class="sxs-lookup"><span data-stu-id="d11aa-103">Managing complex units such as per-user, per-month for product-based quote lines</span></span>

<span data-ttu-id="d11aa-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="d11aa-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d11aa-105">Dynamics 365 Project Operations uporablja količnike za količino, ki podpirajo prodajo naročniških izdelkov.</span><span class="sxs-lookup"><span data-stu-id="d11aa-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="d11aa-106">Pri naročniških izdelkih je količina v vrstici ponudbe ali projektne pogodbe izražena kot število mesecev uporabe.</span><span class="sxs-lookup"><span data-stu-id="d11aa-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="d11aa-107">Običajno je cena naročniške programske opreme shranjena v katalogu kot cena na uporabnika na mesec.</span><span class="sxs-lookup"><span data-stu-id="d11aa-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="d11aa-108">Med prodajnim postopkom je cena v vrstici ponudbe običajno cena na uporabnika na mesec, ki jo je izpogajal in znižal prodajni agent za IT.</span><span class="sxs-lookup"><span data-stu-id="d11aa-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="d11aa-109">Vsak posel ima različno število uporabnikov in različno število naročniških mesecev.</span><span class="sxs-lookup"><span data-stu-id="d11aa-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="d11aa-110">Količina, ki se uporablja za izračun vrstice ponudbe, je produkt števila uporabnikov in števila mesecev naročnine.</span><span class="sxs-lookup"><span data-stu-id="d11aa-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="d11aa-111">Za podporo tej vrsti prodaje je Project Operations uvedla koncept količnikov za količino.</span><span class="sxs-lookup"><span data-stu-id="d11aa-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="d11aa-112">Količniki za količino temeljijo na atributih izdelka v aplikaciji Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d11aa-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="d11aa-113">Ko konfigurirate določene lastnosti za izdelek, vam Project Operations omogoči označevanje podmnožice ali vseh lastnosti kot količnikov za količino.</span><span class="sxs-lookup"><span data-stu-id="d11aa-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="d11aa-114">Project Operations preveri, da so kot količniki za količino označene samo številske lastnosti ali lastnosti izdelka s številskim podatkovnim tipom.</span><span class="sxs-lookup"><span data-stu-id="d11aa-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="d11aa-115">Ko v vrstico ponudbe dodate izdelek s količniki za količino, postane polje **Količina** na voljo samo za branje.</span><span class="sxs-lookup"><span data-stu-id="d11aa-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="d11aa-116">Ko vnesete vrednosti za lastnosti izdelka, ki so količniki za količino, Project Operations izračuna količino vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="d11aa-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="d11aa-117">Dynamics 365 Sales ima lahko na primer te lastnosti:</span><span class="sxs-lookup"><span data-stu-id="d11aa-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="d11aa-118">**Št. uporabnikov** : število uporabnikov.</span><span class="sxs-lookup"><span data-stu-id="d11aa-118">**No of users** : The number of users</span></span>
- <span data-ttu-id="d11aa-119">**Št. mesecev** : število mesecev naročnine.</span><span class="sxs-lookup"><span data-stu-id="d11aa-119">**No of Months** : The number of subscription months</span></span>
- <span data-ttu-id="d11aa-120">**Inventarna številka izdelka**</span><span class="sxs-lookup"><span data-stu-id="d11aa-120">**Product SKU**</span></span>

<span data-ttu-id="d11aa-121">Lastnosti **Št. uporabnikov** in **Št. mesecev** lahko označite kot količnike za količino tako, da uredite lastnosti vrstice izdelkov.</span><span class="sxs-lookup"><span data-stu-id="d11aa-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="d11aa-122">Če želite iz lastnosti izdelka ustvariti količnike za količino, upoštevate te korake:</span><span class="sxs-lookup"><span data-stu-id="d11aa-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="d11aa-123">V levem podoknu za krmarjenje Project Operations odprite **Prodaja** > **Izdelki**.</span><span class="sxs-lookup"><span data-stu-id="d11aa-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="d11aa-124">Odprite izdelek, za katerega morate konfigurirati količnike za količino.</span><span class="sxs-lookup"><span data-stu-id="d11aa-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="d11aa-125">Prepričajte se, da ima izdelek že konfigurirane lastnosti.</span><span class="sxs-lookup"><span data-stu-id="d11aa-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="d11aa-126">Na strani **Podatki o projektu** za izdelek izberite zavihek **Količniki za količino**.</span><span class="sxs-lookup"><span data-stu-id="d11aa-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="d11aa-127">V podmreži izberite **+ Nov izračun polja**.</span><span class="sxs-lookup"><span data-stu-id="d11aa-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="d11aa-128">Vnesite ime količnika za količino in izberite vrednost lastnosti, ki se preslika v izračun polja.</span><span class="sxs-lookup"><span data-stu-id="d11aa-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="d11aa-129">Shranite in zaprite obrazec.</span><span class="sxs-lookup"><span data-stu-id="d11aa-129">Save and close the form.</span></span> <span data-ttu-id="d11aa-130">Ponovite te korake za vse lastnosti, ki jih želite uporabiti za izračun količine pri podrobnosti ponudbe, ki temelji na izdelku.</span><span class="sxs-lookup"><span data-stu-id="d11aa-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="d11aa-131">Ko za izdelek ustvarite podrobnost ponudbe, ki temelji na izdelku, se podrobnost ponudbe zaklene.</span><span class="sxs-lookup"><span data-stu-id="d11aa-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="d11aa-132">Količina bo izračunana kot produkt vrednosti lastnosti, ki ste jih vnesli za to podrobnost ponudbe.</span><span class="sxs-lookup"><span data-stu-id="d11aa-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
