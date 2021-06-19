---
title: Pregled rešitve Project Service Automation
description: Ta tema vsebuje informacije o rešitvi za integracijo rešitve Dynamics 365 Project Service Automation v Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ca459b99881b612e4656be112c8a2e420b4196e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005901"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="51081-103">Pregled rešitve Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="51081-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="51081-104">Rešitev za integracijo rešitve Project Service Automation v Finance uporablja funkcijo za integracijo podatkov za sinhronizacijo podatkov med primerki rešitev Dynamics 365 Finance in Dynamics 365 Project Service Automation prek storitve Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="51081-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="51081-105">Predloge za integracijo, ki so na voljo s funkcijo za integracijo podatkov, omogočajo pretok projektov, projektne pogodbe, podrobnosti projektnih pogodb, mejnike podrobnosti projektnih pogodb, opravila projekta, kategorije transakcije stroškov, ocene delovnih ur in ocene stroškov iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="51081-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="51081-106">Če uporabljate različico 7.3.0, morate namestiti KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="51081-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="51081-107">Potem boste lahko vključili projekte s fiksno ceno.</span><span class="sxs-lookup"><span data-stu-id="51081-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="51081-108">Če uporabljate različico 7.3.0 in transakcije s pristojbinami pridobivate iz rešitve Project Service Automation, morate namestiti KB 4345320, da te pristojbine vključite v račun projekta.</span><span class="sxs-lookup"><span data-stu-id="51081-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="51081-109">Če uporabljate različico 8.0, vam je na voljo integracija projektnih opravil, kategorije transakcije stroškov, ocene delovnih ur, ocene stroškov in zaklepanje funkcionalnosti.</span><span class="sxs-lookup"><span data-stu-id="51081-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="51081-110">Če uporabljate različico 8.0.1 ali novejšo, lahko sinhronizirate dejanske podatke.</span><span class="sxs-lookup"><span data-stu-id="51081-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="51081-111">Preden lahko integrirate rešitev Project Service Automation Finance, morate konfigurirati parametre integracije rešitve Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="51081-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="51081-112">Za več informacij glejte [Parametri integracije rešitve Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="51081-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="51081-113">Ta rešitev za integracijo omogoča neposredno sinhronizacijo v naslednjih scenarijih:</span><span class="sxs-lookup"><span data-stu-id="51081-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="51081-114">Vzdrževanje projektnih pogodb v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="51081-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="51081-115">Ustvarjanje projektov v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="51081-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="51081-116">Vzdrževanje podrobnosti projektne pogodbe v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="51081-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="51081-117">Vzdrževanje mejnike podrobnosti projektne pogodbe v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="51081-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="51081-118">Vzdrževanje opravil projekta v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="51081-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="51081-119">Vzdrževanje kategorij transakcije stroškov v rešitvi Finance in njihova sinhronizacija neposredno iz rešitve Finance v Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="51081-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="51081-120">Ustvarjanje ocen delovnih ur projekta v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="51081-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="51081-121">Ustvarjanje ocen stroškov projekta v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="51081-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="51081-122">Ustvarjanje dejanskih podatkov o času, stroških in pristojbinah v rešitvi Project Service Automation in ustvarjanje transakcije projektov v dnevnikih za integracijo rešitve Project Service Automation, tako da jih je mogoče objaviti v rešitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="51081-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="51081-123">Sinhronizacija podatkov</span><span class="sxs-lookup"><span data-stu-id="51081-123">Data synchronization</span></span>

<span data-ttu-id="51081-124">Naslednja ilustracija prikazuje, kako se podatki sinhronizirajo kot del integracije rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="51081-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="51081-125">Na voljo so le nekatere predloge.</span><span class="sxs-lookup"><span data-stu-id="51081-125">Not all templates are currently available.</span></span> <span data-ttu-id="51081-126">Predloge bodo objavljene, ko bodo dokončane.</span><span class="sxs-lookup"><span data-stu-id="51081-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="51081-127">[![Integracija rešitve Project Service Automation v Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="51081-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="51081-128">Sistemske zahteve za Finance</span><span class="sxs-lookup"><span data-stu-id="51081-128">System requirements for Finance</span></span>

<span data-ttu-id="51081-129">Če želite uporabiti rešitev za integracijo rešitve Project Service Automation v Finance, morate namestiti različico Enterprise Edition 7.3 s posodobitvijo platforme na 12 ali novejšo.</span><span class="sxs-lookup"><span data-stu-id="51081-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="51081-130">Sistemske zahteve za Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="51081-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="51081-131">Če želite uporabiti rešitev za integracijo rešitve Project Service Automation v Finance, morate namestiti naslednje komponente:</span><span class="sxs-lookup"><span data-stu-id="51081-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="51081-132">Dynamics 365 Project Service Automation, različica 9.0.0.0 ali novejša</span><span class="sxs-lookup"><span data-stu-id="51081-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="51081-133">Rešitev za pretvorbo možne stranke v stranko za Dynamics 365 Sales, različica 1.14.0.0 (v14) ali novejša</span><span class="sxs-lookup"><span data-stu-id="51081-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="51081-134">Rešitev Project Service Automation v Finance za Dynamics 365 Project Service Automation različice 1.0.0.0 ali novejša</span><span class="sxs-lookup"><span data-stu-id="51081-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="51081-135">Namestite rešitev za integracijo rešitve Project Service Automation v Finance v svoj primerek rešitve Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="51081-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="51081-136">Prenesite rešitev za integracijo rešitve Project Service Automation v Finance iz [Microsoftovega centra za prenose](https://www.microsoft.com/download/details.aspx?id=57016) in upoštevajte navodila, ki so priložena rešitvi.</span><span class="sxs-lookup"><span data-stu-id="51081-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]