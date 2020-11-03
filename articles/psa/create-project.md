---
title: Ustvari projekt
description: Navodila za ustvarjanje projekta v rešitvi Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: a1a229641d0694311ecb7019e3915d0e8e6783c3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084768"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="bb911-103">Ustvarjanje projekta (rešitev Project Service)</span><span class="sxs-lookup"><span data-stu-id="bb911-103">Create a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="bb911-104">Z zmogljivostmi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v programu [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] ustvarite projekt, ko želite ustvariti priložnost, ponudbo ali pogodbo za storitve na podlagi projektov.</span><span class="sxs-lookup"><span data-stu-id="bb911-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="bb911-105">Z zmogljivostmi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] lahko upravljate projekt vse od ustvarjanja priložnosti do zaključka projekta.</span><span class="sxs-lookup"><span data-stu-id="bb911-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="bb911-106">Ko ustvarite projekt, boste prav tako ustvarili strukturirano členitev dela, ki vpliva na vaše ponudbe, ocene stroškov in upravljanje virov.</span><span class="sxs-lookup"><span data-stu-id="bb911-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="bb911-107">Pojdite na **Project Service > Projekti**.</span><span class="sxs-lookup"><span data-stu-id="bb911-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="bb911-108">Kliknite **Nov projekt**.</span><span class="sxs-lookup"><span data-stu-id="bb911-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="bb911-109">V območje **Povzetek** vnesite ime projekta, nato vnesite čim več podatkov.</span><span class="sxs-lookup"><span data-stu-id="bb911-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="bb911-110">Elementi, ki so označeni z rdečo zvezdico (\*), so obvezni.</span><span class="sxs-lookup"><span data-stu-id="bb911-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="bb911-111">Kliknite **Shrani** , da ustvarite projekt, ki ga nato lahko urejate.</span><span class="sxs-lookup"><span data-stu-id="bb911-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="bb911-112">Nato ustvarite strukturirano členitev dela za projekt, da določite opravila, časovni razpored in vloge virov, ki jih potrebujete za ta projekt.</span><span class="sxs-lookup"><span data-stu-id="bb911-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="bb911-113">Project Service Automation pri načrtovanju upošteva časovni pas uporabljene predloge **Delovna ura**.</span><span class="sxs-lookup"><span data-stu-id="bb911-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="bb911-114">Vendar pa bosta pri ogledu načrtovanih opravil začetni in končni datum prikazana v časovnem pasu uporabnika.</span><span class="sxs-lookup"><span data-stu-id="bb911-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="bb911-115">To velja za druge časovno razporejene poglede na obrazcu **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="bb911-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="bb911-116">Če se uporabnikov časovni pas ne ujema s časovnim pasom predloge za delovne ure, ki se uporablja za projekt, se pojavi opozorilo, ki pojasnjuje razliko.</span><span class="sxs-lookup"><span data-stu-id="bb911-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="bb911-117">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="bb911-117">See Also</span></span>  
 [<span data-ttu-id="bb911-118">Priročnik za vodje projektov</span><span class="sxs-lookup"><span data-stu-id="bb911-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
