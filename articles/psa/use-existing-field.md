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
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084834"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="d666f-103">Uporaba obstoječega polja kot cenovne razsežnosti v rešitvi Project Service</span><span class="sxs-lookup"><span data-stu-id="d666f-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="d666f-104">Rešitev Project Service Automation (PSA) ima številna polja v entiteti **Dejanske vrednosti** , ki jih je v projektnih organizacijah mogoče uporabiti kot cenovne razsežnosti za cene na podlagi vira.</span><span class="sxs-lookup"><span data-stu-id="d666f-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="d666f-105">Eno običajno polje je na primer **Vir, ki ga je mogoče rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="d666f-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="d666f-106">Manjša podjetja, ki imajo manj kot 20–30 virov, katerih delo se obračunava po cenah, lahko ugotovijo, da je preprosteje imeti mere stroškov in deleže obračunavanja, značilne za vsak vir.</span><span class="sxs-lookup"><span data-stu-id="d666f-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="d666f-107">Ker pa število delovne sile, ki delo obračunava po cenah, raste, je lahko to nemogoče ohranjati, saj se mere stroškov in deleži obračunavanja virov spreminjajo, ko so viri povišani, pridobijo več izkušenj ali drugačne nabore znanj.</span><span class="sxs-lookup"><span data-stu-id="d666f-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="d666f-108">Tak pristop je še vedno primeren za podjetja določene velikosti, zato si oglejte temo [Uporaba vira, ki ga je mogoče rezervirati, kot cenovne razsežnosti](bookable-resource-pricing-dimension.md), da izveste, kako lahko obstoječe polje rešitve Project Service uporabite kot cenovno razsežnost.</span><span class="sxs-lookup"><span data-stu-id="d666f-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="d666f-109">Drug primer je kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="d666f-109">Another example is that of transaction category.</span></span> <span data-ttu-id="d666f-110">Stranke in izvajalci so kategorijo transakcije v rešitvi PSA uporabljali za razvrščanje dela in uporabo polja za ceno in strošek na podlagi kategorije dela.</span><span class="sxs-lookup"><span data-stu-id="d666f-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="d666f-111">Za več informacij glejte razdelek [Uporaba kategorije transakcije kot cenovne razsežnosti](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="d666f-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
