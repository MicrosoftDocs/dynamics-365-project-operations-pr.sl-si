---
title: Polja storitve Project Operations kot cenovne razsežnosti
description: Ta tema vsebuje informacije o uporabi polj kot cenovnih razsežnosti v aplikaciji Dynamics 365 Project Operations.
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
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274658"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="7f3ca-103">Polja aplikacije Project Operations kot cenovne razsežnosti</span><span class="sxs-lookup"><span data-stu-id="7f3ca-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="7f3ca-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="7f3ca-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7f3ca-105">Entiteta **Dejanske vrednosti** ima mnogo polj, ki se lahko uporabijo kot cenovne razsežnosti za cene na podlagi vira.</span><span class="sxs-lookup"><span data-stu-id="7f3ca-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="7f3ca-106">Eno običajno polje je na primer **Vir, ki ga je mogoče rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="7f3ca-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="7f3ca-107">Manjša podjetja, ki imajo manj kot 20–30 virov, katerih delo se obračunava po cenah, lahko ugotovijo, da je preprosteje imeti mere stroškov in deleže obračunavanja, značilne za vsak vir.</span><span class="sxs-lookup"><span data-stu-id="7f3ca-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="7f3ca-108">S povečevanjem delovne sile, ki obračunava delo, je lahko nemogoče ohranjati tarife, specifične za vir.</span><span class="sxs-lookup"><span data-stu-id="7f3ca-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="7f3ca-109">Tarife stroškov in deleži obračunavanja virov se začnejo spreminjati, ko so viri povišani, pridobijo več izkušenj ali drugačne nabore znanj.</span><span class="sxs-lookup"><span data-stu-id="7f3ca-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="7f3ca-110">Drug primer je kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="7f3ca-110">Another example is that of transaction category.</span></span> <span data-ttu-id="7f3ca-111">Stranke in izvajalci so kategorijo transakcije uporabljali za razvrščanje dela in uporabo polja za ceno in strošek na podlagi kategorije dela.</span><span class="sxs-lookup"><span data-stu-id="7f3ca-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]