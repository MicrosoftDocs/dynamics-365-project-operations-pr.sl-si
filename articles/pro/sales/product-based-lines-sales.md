---
title: Podrobnosti priložnosti, ki temeljijo na izdelkih
description: Ta tema vsebuje informacije o vrstičnih postavkah priložnosti, ki temeljijo na izdelkih, v storitvi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084682"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="be82e-103">Podrobnosti priložnosti, ki temeljijo na izdelkih</span><span class="sxs-lookup"><span data-stu-id="be82e-103">Product-based opportunity lines</span></span>

<span data-ttu-id="be82e-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="be82e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="be82e-105">Podrobnosti priložnosti, ki temeljijo na izdelkih, so vrstične postavke za priložnost.</span><span class="sxs-lookup"><span data-stu-id="be82e-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="be82e-106">Te podrobnosti so stranki dostavljene kot ločene vrstične postavke na morebitnem računu, brez kakršnih koli drugih storitev z dodano vrednostjo.</span><span class="sxs-lookup"><span data-stu-id="be82e-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="be82e-107">S tem povezani stroški in poraba se ne spremljajo pri opravilih povezanih projektov.</span><span class="sxs-lookup"><span data-stu-id="be82e-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="be82e-108">Podrobnosti, ki temeljijo na izdelkih, so lahko kataloški izdelki ali izdelki, ki niso v katalogu.</span><span class="sxs-lookup"><span data-stu-id="be82e-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="be82e-109">Večina funkcij pri podrobnostih priložnosti, ki temeljijo na izdelkih, upoštevajo funkcionalnosti, ki jih ponuja aplikacija Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="be82e-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="be82e-110">Za več informacij o podrobnostih priložnosti, ki temeljijo na izdelkih, glejte [Dodajanje izdelkov priložnosti](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="be82e-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="be82e-111">Eden od konceptov glede podrobnosti priložnosti, ki temeljijo na izdelkih in je značilen za priložnosti, ki temeljijo na projektih, je **Proračun stranke**.</span><span class="sxs-lookup"><span data-stu-id="be82e-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="be82e-112">S tem poljem sledite znesku, ki ga je stranka pripravljena plačati za vrstično postavko.</span><span class="sxs-lookup"><span data-stu-id="be82e-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="be82e-113">Če je metoda prihodka za povzetek priložnosti nastavljena na **Izračuna sistem** , so vrednosti proračuna strank pri podrobnostih, ki temeljijo na izdelkih ali projektih, povzete za izračun ocenjenega prihodka.</span><span class="sxs-lookup"><span data-stu-id="be82e-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
