---
title: Polja storitve Project Operations kot cenovne razsežnosti
description: Ta tema vsebuje informacije o uporabi polj kot cenovnih razsežnostih v storitvi Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 59367b35f15f806b109f606e912edc487d9e7685
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119258"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="6343a-103">Polja storitve Project Operations kot cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="6343a-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="6343a-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="6343a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6343a-105">Entiteta **Dejanske vrednosti** ima mnogo polj, ki se lahko uporabijo kot cenovne razsežnosti za cene na podlagi vira.</span><span class="sxs-lookup"><span data-stu-id="6343a-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="6343a-106">Eno običajno polje je na primer **Vir, ki ga je mogoče rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="6343a-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="6343a-107">Manjša podjetja, ki imajo manj kot 20–30 virov, katerih delo se obračunava po cenah, lahko ugotovijo, da je preprosteje imeti mere stroškov in deleže obračunavanja, značilne za vsak vir.</span><span class="sxs-lookup"><span data-stu-id="6343a-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="6343a-108">S povečevanjem delovne sile, ki obračunava delo, je lahko nemogoče ohranjati tarife, specifične za vir.</span><span class="sxs-lookup"><span data-stu-id="6343a-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="6343a-109">Tarife stroškov in deleži obračunavanja virov se začnejo spreminjati, ko so viri povišani, pridobijo več izkušenj ali drugačne nabore znanj.</span><span class="sxs-lookup"><span data-stu-id="6343a-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="6343a-110">Drug primer je kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="6343a-110">Another example is that of transaction category.</span></span> <span data-ttu-id="6343a-111">Stranke in izvajalci so kategorijo transakcije uporabljali za razvrščanje dela in uporabo polja za ceno in strošek na podlagi kategorije dela.</span><span class="sxs-lookup"><span data-stu-id="6343a-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
