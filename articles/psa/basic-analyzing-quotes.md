---
title: Analiza ponudb za projekte
description: Ta tema vsebuje informacije o analizi ponudb za projekte.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 361a940261811467c46222c3d58c9504434ec882
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145243"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="e62fb-103">Analiza ponudb za projekte</span><span class="sxs-lookup"><span data-stu-id="e62fb-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e62fb-104">Dynamics 365 Project Service Automation analizira ponudbe za projekte, da lahko oceni dobičkonosnost.</span><span class="sxs-lookup"><span data-stu-id="e62fb-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="e62fb-105">Analizira tudi, kako dobro je ponudba usklajena s pričakovanji kupcev o datumu dostave ali datum zaključka, in o proračunu.</span><span class="sxs-lookup"><span data-stu-id="e62fb-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="e62fb-106">Analiza dobičkonosnosti</span><span class="sxs-lookup"><span data-stu-id="e62fb-106">Profitability analysis</span></span>

<span data-ttu-id="e62fb-107">Project Service Automation analizira dobičkonosnost tako, da uporabi stopnjo bruto dobička in prilagojeno stopnjo bruto dobička.</span><span class="sxs-lookup"><span data-stu-id="e62fb-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="e62fb-108">Stopnja bruto dobička se izračuna z naslednjo formulo:</span><span class="sxs-lookup"><span data-stu-id="e62fb-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="e62fb-109">Prilagojena stopnja bruto dobička se izračuna z naslednjo formulo:</span><span class="sxs-lookup"><span data-stu-id="e62fb-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="e62fb-110">Če se vrednosti za stopnjo bruto dobička in prilagojeno stopnjo bruto dobička precej razlikujeta, je veliko dela v ponudbi razvrščeno delo, ki se ne zaračuna.</span><span class="sxs-lookup"><span data-stu-id="e62fb-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="e62fb-111">Analiza pričakovanj strank</span><span class="sxs-lookup"><span data-stu-id="e62fb-111">Analysis of customer expectations</span></span>

<span data-ttu-id="e62fb-112">Ponudbe lahko analizirate in ustvarite grafikone pričakovanj strank v zvezi z razporedom in proračunom.</span><span class="sxs-lookup"><span data-stu-id="e62fb-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="e62fb-113">Polje **Zahtevani datum dostave** v glavi ponudbe</span><span class="sxs-lookup"><span data-stu-id="e62fb-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="e62fb-114">Polje **Proračun stranke** za vsako vrstico ponudbe (za vrstice, ki temeljijo na projektih, in vrstice, ki temeljijo na izdelkih)</span><span class="sxs-lookup"><span data-stu-id="e62fb-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="e62fb-115">Analiza pričakovanj strank glede razporeda se izvede s primerjavo najnovejšega končnega datuma podrobnosti vrstice ponudbe z zahtevanim datumom dostave v vseh vrsticah ponudbe v ponudbi.</span><span class="sxs-lookup"><span data-stu-id="e62fb-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="e62fb-116">Analiza pričakovanj strank v zvezi s proračunom se izvede s primerjavo vsote celotnega proračuna kupca z zneskom za ponudbo v vseh vrsticah ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e62fb-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
