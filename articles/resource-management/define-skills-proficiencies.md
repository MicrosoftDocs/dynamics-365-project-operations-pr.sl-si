---
title: Določanje znanj in usposobljenosti
description: Ta tema vsebuje informacije o tem, kako nastaviti modele usposobljenosti za ocenjevanje virov.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084700"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="50c04-103">Določanje znanj in usposobljenosti</span><span class="sxs-lookup"><span data-stu-id="50c04-103">Define skills and proficiencies</span></span>

<span data-ttu-id="50c04-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="50c04-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="50c04-105">Znanja so značilnosti virov, ki se delijo med storitvama Dynamics 365 Project Operations in, če je nameščena, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="50c04-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="50c04-106">Če želite shraniti skladišče znanj v storitvi Project Operations, pojdite v **Viri** \>**Znanja virov**.</span><span class="sxs-lookup"><span data-stu-id="50c04-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="50c04-107">Uporaba modelov usposobljenosti za ocenjevanje virov</span><span class="sxs-lookup"><span data-stu-id="50c04-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="50c04-108">Znanje virov je ocenjeno z modeli usposobljenosti.</span><span class="sxs-lookup"><span data-stu-id="50c04-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="50c04-109">Individualne ocene so v modelu usposobljenosti.</span><span class="sxs-lookup"><span data-stu-id="50c04-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="50c04-110">Če želite ustvariti model usposobljenosti, pojdite v **Viri** \>**Modeli usposobljenosti** in izberite možnost **Novo**.</span><span class="sxs-lookup"><span data-stu-id="50c04-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="50c04-111">V novem modelu za ocenjevanje določite najnižjo vrednost ocene, najvišjo vrednost ocene in entiteto, ki jo ocenjujete.</span><span class="sxs-lookup"><span data-stu-id="50c04-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="50c04-112">V podmreži **Vrednosti ocene** lahko določite različne vrednosti ocen, od najmanjše do največje.</span><span class="sxs-lookup"><span data-stu-id="50c04-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="50c04-113">Te vrednosti ocen se prikažejo pri filtrih **Zahteve vira** , **Plošča razporeda** in **Pomočnik za razporejanje**.</span><span class="sxs-lookup"><span data-stu-id="50c04-113">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
