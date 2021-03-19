---
title: Ocene virov
description: Ta tema vsebuje informacije o načinu izračuna ocene virov v storitvi Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286538"
---
# <a name="resource-estimates"></a><span data-ttu-id="105be-103">Ocene virov</span><span class="sxs-lookup"><span data-stu-id="105be-103">Resource estimates</span></span>

<span data-ttu-id="105be-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="105be-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="105be-105">Ocene virov izhajajo iz časovno razporejenega dela, ki je opredeljeno v strukturirani členitvi dela skupaj z veljavnimi razsežnostmi cen.</span><span class="sxs-lookup"><span data-stu-id="105be-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="105be-106">Običajno je izračun naslednji: **hitrost/uro za vsako vlogo X število ur.**</span><span class="sxs-lookup"><span data-stu-id="105be-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="105be-107">Časovno razporejeno delo za vsak vir je shranjeno v zapisu o dodelitvi vira.</span><span class="sxs-lookup"><span data-stu-id="105be-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="105be-108">Cene so shranjene v vnaprej določenem ceniku.</span><span class="sxs-lookup"><span data-stu-id="105be-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="105be-109">Pretvorba enot se uporablja na podlagi veljavnega cenika.</span><span class="sxs-lookup"><span data-stu-id="105be-109">Unit conversion is applied based on the applicable price list.</span></span>

![Ocene virov](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="105be-111">Privzeta lastna cena in valuta cene</span><span class="sxs-lookup"><span data-stu-id="105be-111">Default cost price and cost currency</span></span>

<span data-ttu-id="105be-112">Lastne cene so privzeto nastavljene iz organizacijske enote.</span><span class="sxs-lookup"><span data-stu-id="105be-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="105be-113">Privzeti delež obračunavanja stroškov in valuta prodaje</span><span class="sxs-lookup"><span data-stu-id="105be-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="105be-114">Prodajne cene se uporabijo enkrat na posel.</span><span class="sxs-lookup"><span data-stu-id="105be-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="105be-115">Hierarhija privzeto nastavljenega prodajnega cenika je naslednja:</span><span class="sxs-lookup"><span data-stu-id="105be-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="105be-116">Organizacija</span><span class="sxs-lookup"><span data-stu-id="105be-116">Organization</span></span>
2. <span data-ttu-id="105be-117">Stranki</span><span class="sxs-lookup"><span data-stu-id="105be-117">Customer</span></span>
3. <span data-ttu-id="105be-118">Ponudba/pogodba</span><span class="sxs-lookup"><span data-stu-id="105be-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]