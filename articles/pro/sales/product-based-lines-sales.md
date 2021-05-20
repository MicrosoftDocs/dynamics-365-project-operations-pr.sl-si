---
title: Vrstice priložnosti, ki temeljijo na izdelkih – poenostavljeno
description: Ta tema vsebuje informacije o vrstičnih postavkah priložnosti, ki temeljijo na izdelkih, v storitvi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f7dfabd068e180c7122ede0f79aaebfe220250a1
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949564"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="67007-103">Vrstice priložnosti, ki temeljijo na izdelkih – poenostavljeno</span><span class="sxs-lookup"><span data-stu-id="67007-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="67007-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="67007-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="67007-105">Podrobnosti priložnosti, ki temeljijo na izdelkih, so vrstične postavke za priložnost.</span><span class="sxs-lookup"><span data-stu-id="67007-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="67007-106">Te ločene vrstične postavke so na morebitnem računu, ki je posredovan stranki.</span><span class="sxs-lookup"><span data-stu-id="67007-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="67007-107">Račun ne vključuje nobenih dodatnih storitev.</span><span class="sxs-lookup"><span data-stu-id="67007-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="67007-108">S tem povezani stroški in poraba se ne spremljajo pri opravilih povezanih projektov.</span><span class="sxs-lookup"><span data-stu-id="67007-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="67007-109">Podrobnosti, ki temeljijo na izdelkih, so lahko kataloški izdelki ali izdelki, ki niso v katalogu.</span><span class="sxs-lookup"><span data-stu-id="67007-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="67007-110">Večina funkcij pri podrobnostih priložnosti, ki temeljijo na izdelkih, upoštevajo funkcionalnosti, ki jih ponuja aplikacija Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="67007-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="67007-111">Za več informacij o podrobnostih priložnosti, ki temeljijo na izdelkih, glejte [Dodajanje izdelkov priložnosti](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="67007-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="67007-112">**Proračun stranke** je koncept, ki je značilen za podrobnosti priložnosti, ki temeljijo na projektih.</span><span class="sxs-lookup"><span data-stu-id="67007-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="67007-113">Polje **Proračun stranke** sledi znesku, ki ga je stranka pripravljena plačati za izdelek.</span><span class="sxs-lookup"><span data-stu-id="67007-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="67007-114">Ko je za metodo prihodkov v povzetku priložnosti izbrana možnost **Izračuna sistem**, so vrednosti proračuna strank v podrobnostih priložnosti povzete za izračun predvidenega prihodka.</span><span class="sxs-lookup"><span data-stu-id="67007-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]