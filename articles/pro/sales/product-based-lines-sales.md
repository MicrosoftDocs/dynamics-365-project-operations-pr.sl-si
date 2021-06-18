---
title: Vrstice priložnosti, ki temeljijo na izdelkih – poenostavljeno
description: Ta tema vsebuje informacije o vrstičnih postavkah priložnosti, ki temeljijo na izdelkih, v storitvi Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7865da682ae607f017bf59ce1ae1addc9fefa60b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994516"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="9fa8e-103">Vrstice priložnosti, ki temeljijo na izdelkih – poenostavljeno</span><span class="sxs-lookup"><span data-stu-id="9fa8e-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="9fa8e-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="9fa8e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9fa8e-105">Podrobnosti priložnosti, ki temeljijo na izdelkih, so vrstične postavke za priložnost.</span><span class="sxs-lookup"><span data-stu-id="9fa8e-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="9fa8e-106">Te ločene vrstične postavke so na morebitnem računu, ki je posredovan stranki.</span><span class="sxs-lookup"><span data-stu-id="9fa8e-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="9fa8e-107">Račun ne vključuje nobenih dodatnih storitev.</span><span class="sxs-lookup"><span data-stu-id="9fa8e-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="9fa8e-108">S tem povezani stroški in poraba se ne spremljajo pri opravilih povezanih projektov.</span><span class="sxs-lookup"><span data-stu-id="9fa8e-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="9fa8e-109">Podrobnosti, ki temeljijo na izdelkih, so lahko kataloški izdelki ali izdelki, ki niso v katalogu.</span><span class="sxs-lookup"><span data-stu-id="9fa8e-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="9fa8e-110">Večina funkcij pri podrobnostih priložnosti, ki temeljijo na izdelkih, upoštevajo funkcionalnosti, ki jih ponuja aplikacija Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9fa8e-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="9fa8e-111">Za več informacij o podrobnostih priložnosti, ki temeljijo na izdelkih, glejte [Dodajanje izdelkov priložnosti](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="9fa8e-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="9fa8e-112">**Proračun stranke** je koncept, ki je značilen za podrobnosti priložnosti, ki temeljijo na projektih.</span><span class="sxs-lookup"><span data-stu-id="9fa8e-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="9fa8e-113">Polje **Proračun stranke** sledi znesku, ki ga je stranka pripravljena plačati za izdelek.</span><span class="sxs-lookup"><span data-stu-id="9fa8e-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="9fa8e-114">Ko je za metodo prihodkov v povzetku priložnosti izbrana možnost **Izračuna sistem**, so vrednosti proračuna strank v podrobnostih priložnosti povzete za izračun predvidenega prihodka.</span><span class="sxs-lookup"><span data-stu-id="9fa8e-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]