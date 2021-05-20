---
title: Pregled načinov upravljanja virov
description: TaTa tema vsebuje informacije o funkciji »Upravljanje virov« v storitvi Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d132bcbef5421202d2f4899091f0dc75166dd66
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949969"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="1b8bd-103">Pregled načinov upravljanja virov</span><span class="sxs-lookup"><span data-stu-id="1b8bd-103">Resource management modes overview</span></span>

<span data-ttu-id="1b8bd-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="1b8bd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1b8bd-105">Dynamics 365 Project Operations podpira dva načina za izvajanje celotnega poteka rezervacije.</span><span class="sxs-lookup"><span data-stu-id="1b8bd-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="1b8bd-106">Način upravljanja je opredeljen kot projektni parameter in ga je mogoče spremeniti ob spremembi vašega poslovanja.</span><span class="sxs-lookup"><span data-stu-id="1b8bd-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="1b8bd-107">Osrednji način</span><span class="sxs-lookup"><span data-stu-id="1b8bd-107">Central mode</span></span>
<span data-ttu-id="1b8bd-108">Organizacijam, ki centralizirajo dodelitev virov projektom, osrednji način omogoča, da lahko vodje projektov določijo zahtevane pogoje za vire na ravni projekta.</span><span class="sxs-lookup"><span data-stu-id="1b8bd-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="1b8bd-109">Izpolnjevanje zahtevanih pogojev za vire je preneseno na upravitelja virov.</span><span class="sxs-lookup"><span data-stu-id="1b8bd-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="1b8bd-110">Vodje projektov lahko sprejmejo ali zavrnejo vire, ki jih predlaga upravitelj virov.</span><span class="sxs-lookup"><span data-stu-id="1b8bd-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Osrednji način](./media/resource-management-central.png)

<span data-ttu-id="1b8bd-112">Za upravljanje virov v osrednjem načinu glejte:</span><span class="sxs-lookup"><span data-stu-id="1b8bd-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="1b8bd-113">Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in ustvarjanje zahtevanih pogojev za vir</span><span class="sxs-lookup"><span data-stu-id="1b8bd-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="1b8bd-114">Rezervacija poimenovanih virov iz zahtevanih pogojev za vire</span><span class="sxs-lookup"><span data-stu-id="1b8bd-114">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="1b8bd-115">Pošiljanje zahteve za vir</span><span class="sxs-lookup"><span data-stu-id="1b8bd-115">Submit a resource request</span></span>](/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="1b8bd-116">Izpolnjevanje zahteve za vir</span><span class="sxs-lookup"><span data-stu-id="1b8bd-116">Fulfill a resource request</span></span>](/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="1b8bd-117">Sprejem ali zavrnitev predlaganega projektnega vira iz zahteve za vir</span><span class="sxs-lookup"><span data-stu-id="1b8bd-117">Accept or reject a proposed project resource from a resource request</span></span>](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="1b8bd-118">Hibridni način</span><span class="sxs-lookup"><span data-stu-id="1b8bd-118">Hybrid mode</span></span>
<span data-ttu-id="1b8bd-119">Organizacijam, ki potrebujejo prilagodljivost pri dodeljevanju virov, hibridni način omogoča, da vodje projektov in upravitelji virov rezervirajo vire.</span><span class="sxs-lookup"><span data-stu-id="1b8bd-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hibridni način](./media/resource-management-hybrid.png)

<span data-ttu-id="1b8bd-121">Poleg podprtega postopka v osrednjem načinu glejte tudi naslednje teme za upravljanje vseh drugih podprtih potekov za rezervacije v hibridnem načinu:</span><span class="sxs-lookup"><span data-stu-id="1b8bd-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="1b8bd-122">Rezervacija vira neposredno iz projekta:</span><span class="sxs-lookup"><span data-stu-id="1b8bd-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="1b8bd-123">Rezervacija poimenovanih virov, ki jih je mogoče rezervirati, za projektno ekipo in dodelitev opravil</span><span class="sxs-lookup"><span data-stu-id="1b8bd-123">Book named bookable resources to a project team and assign tasks</span></span>](/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="1b8bd-124">Rezervacija vira iz zahtevanega pogoja za vir:</span><span class="sxs-lookup"><span data-stu-id="1b8bd-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="1b8bd-125">Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in ustvarjanje zahtevanih pogojev za vir</span><span class="sxs-lookup"><span data-stu-id="1b8bd-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="1b8bd-126">Rezervacija poimenovanih virov iz zahtevanih pogojev za vire</span><span class="sxs-lookup"><span data-stu-id="1b8bd-126">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]