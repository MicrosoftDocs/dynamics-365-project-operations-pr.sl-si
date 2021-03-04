---
title: Konfiguriranje vloge virov
description: Navodila za konfiguriranje vlog virov v rešitvi Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: deaff0977ebb50382a28494fba2a1c34ed5cc9b4
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144928"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="b9ed2-103">Konfiguriranje vlog virov (rešitev Project Service)</span><span class="sxs-lookup"><span data-stu-id="b9ed2-103">Configure resource roles (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b9ed2-104">Pri določanju zahtev za vire ali stroškov projekta so vloge pomemben del načrtovanja projektov.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="b9ed2-105">Za vsako vlogo, ki jo potrebujete za projekt, morate ustvariti vlogo vira in s to vlogo povezati znanja in usposobljenost.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="b9ed2-106">Ustvarite lahko na primer vloge za razvijalca, projektnega vodjo ali preizkuševalca iger.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="b9ed2-107">Nastavite lahko tudi ravni znanj in usposobljenosti, ki so potrebne za vlogo.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="b9ed2-108">Konfiguracija vlog virov za zagotovitev dejanske ocene projekta za organizacijo.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="b9ed2-109">Prav tako se prepričajte, ali ste pravilno nastavili vrsto obračunavanja.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="b9ed2-110">Element, nastavljen na vrsto obračunavanja, ki je ni mogoče zaračunati, se ne prikaže v podrobnostih pogodbe ali ponudbe.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="b9ed2-111">Ko nastavite vloge virov, lahko s cenikom nastavite stroške in prodajne cene.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="b9ed2-112">Za vsako vlogo, ki jo želite dodati, sledite naslednjim korakom:</span><span class="sxs-lookup"><span data-stu-id="b9ed2-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="b9ed2-113">Pojdite na **Project Service > Vloge virov**.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="b9ed2-114">Kliknite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="b9ed2-115">Na območju **Splošno** lahko v polje **Ime** vnesete ime vloge in po potrebi izpolnite druga polja.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="b9ed2-116">Kliknite **Shrani**, da ustvarite zapis, ki ga nato lahko urejate.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="b9ed2-117">Če želite dodati znanje, na območju **Znanje** kliknite **+**.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="b9ed2-118">V podoknu **Pogoj glede usposobljenosti vloge** kliknite polje **Znanje**, nato kliknite gumb **Išči** in izberite znanje.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="b9ed2-119">Zberite stopnjo za to znanje in kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="b9ed2-120">Po potrebi dodajajte druga znanja.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="b9ed2-121">Ko končate, v spodnjem desnem kotu zaslona kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="b9ed2-122">Če želite omogočiti, da se pri projektih uporablja ta vloga vira, kliknite **Aktiviraj**.</span><span class="sxs-lookup"><span data-stu-id="b9ed2-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b9ed2-123">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="b9ed2-123">See Also</span></span>  
 [<span data-ttu-id="b9ed2-124">Nastavitev virov</span><span class="sxs-lookup"><span data-stu-id="b9ed2-124">Set up resources</span></span>](../psa/set-up-resources.md)
