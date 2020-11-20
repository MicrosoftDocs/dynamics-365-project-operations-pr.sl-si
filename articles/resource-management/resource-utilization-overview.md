---
title: Pregled uporabe virov
description: V tej temi so na voljo informacije o uporabi virov v storitvi Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401396"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="c7b15-103">Pregled uporabe virov</span><span class="sxs-lookup"><span data-stu-id="c7b15-103">Resource utilization overview</span></span>

<span data-ttu-id="c7b15-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="c7b15-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c7b15-105">Viri lahko imajo ciljno zaračunano uporabo.</span><span class="sxs-lookup"><span data-stu-id="c7b15-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="c7b15-106">Ta ciljna uporaba je opredeljena kot atribut privzete vloge vira ali nastavljena v zapisu posameznega vira, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="c7b15-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="c7b15-107">Izračuni uporabe temeljijo na dejanskih urah, ki so jih viri poročali na podlagi odobrenih časovnih vnosov.</span><span class="sxs-lookup"><span data-stu-id="c7b15-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="c7b15-108">Za izračun uporabe se uporabljajo naslednje enačbe:</span><span class="sxs-lookup"><span data-stu-id="c7b15-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="c7b15-109">Zaračunana uporaba = dejanske zaračunane ure ÷ zmogljivost vira</span><span class="sxs-lookup"><span data-stu-id="c7b15-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="c7b15-110">Nezaračunana uporaba = dejanski čas z ID-jem vrste obračunavanja = se ne zaračuna, brezplačno ali ni na voljo ÷ zmogljivost vira</span><span class="sxs-lookup"><span data-stu-id="c7b15-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="c7b15-111">Za interno uporabo = dejanski čas brez prodajne pogodbe ÷ zmogljivost vira</span><span class="sxs-lookup"><span data-stu-id="c7b15-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="c7b15-112">Zmogljivost vira = delovni čas vira – odsotnost – prosti dnevi</span><span class="sxs-lookup"><span data-stu-id="c7b15-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="c7b15-113">Pogled **Uporaba vira** lahko najdete v podoknu **Viri**.</span><span class="sxs-lookup"><span data-stu-id="c7b15-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="c7b15-114">Vsaka celica v mreži predstavlja delež zaračunane uporabe vira v določenem obdobju, na primer dnevu, tednu ali mesecu.</span><span class="sxs-lookup"><span data-stu-id="c7b15-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="c7b15-115">Za obarvanje celic se uporabljajo naslednje enačbe:</span><span class="sxs-lookup"><span data-stu-id="c7b15-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="c7b15-116">**Zelena**: zaračunana uporaba > = ciljna uporaba za vir</span><span class="sxs-lookup"><span data-stu-id="c7b15-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="c7b15-117">**Rumena**: ciljna uporaba – 20 <= zaračunana uporaba < ciljna uporaba</span><span class="sxs-lookup"><span data-stu-id="c7b15-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="c7b15-118">**Rdeča**: zaračunana uporaba < ciljna uporaba – 20</span><span class="sxs-lookup"><span data-stu-id="c7b15-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="c7b15-119">Ker pogled **Uporaba vira** temelji na plošči razporeda, lahko rezultate filtrirate z možnostmi filtriranja na plošči razporeda.</span><span class="sxs-lookup"><span data-stu-id="c7b15-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="c7b15-120">Zaradi mreže morate nastaviti ciljno uporabo za vlogo ali posamezni vir.</span><span class="sxs-lookup"><span data-stu-id="c7b15-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="c7b15-121">To nastavite v možnosti **Viri** > **Vloge virov**.</span><span class="sxs-lookup"><span data-stu-id="c7b15-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="c7b15-122">Poleg tega morate vsakemu viru, ki ga je mogoče rezervirati, dodati tudi privzeto vlogo.</span><span class="sxs-lookup"><span data-stu-id="c7b15-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="c7b15-123">Odprite možnost **Viri** > **Viri**.</span><span class="sxs-lookup"><span data-stu-id="c7b15-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="c7b15-124">Na zavihku **Project Service** preverite, ali je vloga vira določena in ali je polje **Je privzeto** nastavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="c7b15-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="c7b15-125">Kjer je vrednost **Je privzeto** = **Ne**, lahko dodate dodatne vloge.</span><span class="sxs-lookup"><span data-stu-id="c7b15-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="c7b15-126">Vloga, pri kateri je vrednost **Je privzeto** = **Da**, se uporablja za oceno uporabe vira v primerjavi s ciljem za to vlogo.</span><span class="sxs-lookup"><span data-stu-id="c7b15-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="c7b15-127">Na zavihku **Project Service** lahko nastavite tudi posamično ciljno uporabo za vir.</span><span class="sxs-lookup"><span data-stu-id="c7b15-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="c7b15-128">Izračun uporabe nato uporabi to ciljno uporabo za oceno cilja vira namesto cilja privzete vloge vira.</span><span class="sxs-lookup"><span data-stu-id="c7b15-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="c7b15-129">Uporaba se za posamezen vir prikaže samo, če je vir odobril čas, ki se zaračuna, v obdobju, ki je prikazan v mreži.</span><span class="sxs-lookup"><span data-stu-id="c7b15-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>
