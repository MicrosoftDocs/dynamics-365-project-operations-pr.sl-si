---
title: Uporaba obstoječega polja kot cenovne razsežnosti v rešitvi Project Service
description: V tej temi so na voljo informacije o uporabi obstoječih polj rešitve Project Service kot cenovnih razsežnosti.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281588"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="e8dea-103">Uporaba obstoječega polja kot cenovne razsežnosti v rešitvi Project Service</span><span class="sxs-lookup"><span data-stu-id="e8dea-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e8dea-104">Rešitev Project Service Automation (PSA) ima številna polja v entiteti **Dejanske vrednosti**, ki jih je v projektnih organizacijah mogoče uporabiti kot cenovne razsežnosti za cene na podlagi vira.</span><span class="sxs-lookup"><span data-stu-id="e8dea-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="e8dea-105">Eno običajno polje je na primer **Vir, ki ga je mogoče rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="e8dea-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="e8dea-106">Manjša podjetja, ki imajo manj kot 20–30 virov, katerih delo se obračunava po cenah, lahko ugotovijo, da je preprosteje imeti mere stroškov in deleže obračunavanja, značilne za vsak vir.</span><span class="sxs-lookup"><span data-stu-id="e8dea-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="e8dea-107">Ker pa število delovne sile, ki delo obračunava po cenah, raste, je lahko nemogoče ohranjati specifične postavke, saj se mere stroškov in deleži obračunavanja virov spreminjajo, ko so viri povišani, pridobijo več izkušenj ali drugačen nabor znanj.</span><span class="sxs-lookup"><span data-stu-id="e8dea-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="e8dea-108">Ker ta pristop še deluje za podjetja določene velikost, glejte [Uporaba vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti](bookable-resource-pricing-dimension.md), da bi razumeli, kako je mogoče obstoječe polje v storitvi Project Service uporabiti kot cenovno razsežnost.</span><span class="sxs-lookup"><span data-stu-id="e8dea-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="e8dea-109">Drug primer je kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="e8dea-109">Another example is that of transaction category.</span></span> <span data-ttu-id="e8dea-110">Stranke in izvajalci so kategorijo transakcije v rešitvi PSA uporabljali za razvrščanje dela in uporabo polja za ceno in strošek na podlagi kategorije dela.</span><span class="sxs-lookup"><span data-stu-id="e8dea-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="e8dea-111">Za več informacij glejte razdelek [Uporaba kategorije transakcije kot cenovne razsežnosti](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="e8dea-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]