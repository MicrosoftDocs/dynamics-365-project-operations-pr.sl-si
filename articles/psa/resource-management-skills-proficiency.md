---
title: Modeli znanj in usposobljenosti
description: Ta tema vsebuje informacije o uporabi modelov znanj in usposobljenosti.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 82eeab4c9682e5b777da4e66f6c4f3f1afb3c19b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282983"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="771b3-103">Modeli znanj in usposobljenosti</span><span class="sxs-lookup"><span data-stu-id="771b3-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="771b3-104">Znanja so značilnosti virov, ki se delijo med aplikacijama Dynamics 365 Project Service Automation in Dynamics 365 Field Service (če je nameščena).</span><span class="sxs-lookup"><span data-stu-id="771b3-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="771b3-105">Če želite shraniti skladišče znanj v aplikaciji Project Service Automation, pojdite v **Viri** \>**Znanja virov**.</span><span class="sxs-lookup"><span data-stu-id="771b3-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Znanje vira](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="771b3-107">Uporaba modelov usposobljenosti za ocenjevanje virov</span><span class="sxs-lookup"><span data-stu-id="771b3-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="771b3-108">Znanje virov je ocenjeno z modeli usposobljenosti.</span><span class="sxs-lookup"><span data-stu-id="771b3-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="771b3-109">Individualne ocene so v modelu usposobljenosti.</span><span class="sxs-lookup"><span data-stu-id="771b3-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="771b3-110">Če želite ustvariti model usposobljenosti, pojdite v **Viri** \>**Modeli usposobljenosti** in izberite možnost **Novo**.</span><span class="sxs-lookup"><span data-stu-id="771b3-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="771b3-111">V novem modelu za ocenjevanje določite najnižjo vrednost ocene, najvišjo vrednost ocene in entiteto, ki jo ocenjujete.</span><span class="sxs-lookup"><span data-stu-id="771b3-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="771b3-112">V podmreži **Vrednosti ocene** lahko določite različne vrednosti ocen, od najmanjše do največje.</span><span class="sxs-lookup"><span data-stu-id="771b3-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Določene najnižje in najvišje ocene](media/Resource-Management-image85.png)

<span data-ttu-id="771b3-114">Te vrednosti ocen se prikažejo pri filtrih **Zahteve vira**, **Plošča razporeda** in **Pomočnik za razporejanje**.</span><span class="sxs-lookup"><span data-stu-id="771b3-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]