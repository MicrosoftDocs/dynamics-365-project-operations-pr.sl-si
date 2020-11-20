---
title: Določanje znanj in usposobljenosti
description: Ta tema vsebuje informacije o tem, kako nastaviti modele usposobljenosti za ocenjevanje virov.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8738a4743554704ef76807c81fdefcd74e668e1b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124793"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="0d19e-103">Določanje znanj in usposobljenosti</span><span class="sxs-lookup"><span data-stu-id="0d19e-103">Define skills and proficiencies</span></span>

<span data-ttu-id="0d19e-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="0d19e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0d19e-105">Znanja so značilnosti virov, ki se delijo med storitvama Dynamics 365 Project Operations in, če je nameščena, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="0d19e-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="0d19e-106">Če želite shraniti skladišče znanj v storitvi Project Operations, pojdite v **Viri** \>**Znanja virov**.</span><span class="sxs-lookup"><span data-stu-id="0d19e-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="0d19e-107">Uporaba modelov usposobljenosti za ocenjevanje virov</span><span class="sxs-lookup"><span data-stu-id="0d19e-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="0d19e-108">Znanje virov je ocenjeno z modeli usposobljenosti.</span><span class="sxs-lookup"><span data-stu-id="0d19e-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="0d19e-109">Individualne ocene so v modelu usposobljenosti.</span><span class="sxs-lookup"><span data-stu-id="0d19e-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="0d19e-110">Če želite ustvariti model usposobljenosti, pojdite v **Viri** \>**Modeli usposobljenosti** in izberite možnost **Novo**.</span><span class="sxs-lookup"><span data-stu-id="0d19e-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="0d19e-111">V novem modelu za ocenjevanje določite najnižjo vrednost ocene, najvišjo vrednost ocene in entiteto, ki jo ocenjujete.</span><span class="sxs-lookup"><span data-stu-id="0d19e-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="0d19e-112">V podmreži **Vrednosti ocene** lahko določite različne vrednosti ocen, od najmanjše do največje.</span><span class="sxs-lookup"><span data-stu-id="0d19e-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="0d19e-113">Te vrednosti ocen se prikažejo pri filtrih **Zahteve vira**, **Plošča razporeda** in **Pomočnik za razporejanje**.</span><span class="sxs-lookup"><span data-stu-id="0d19e-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
