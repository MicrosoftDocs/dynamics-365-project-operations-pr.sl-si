---
title: Priročnik za upravitelje virov
description: Priročnik za upravljanje virov v rešitvi Project Service
author: JohnPBurrows
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
ms.openlocfilehash: cdfac15c45a1c7b40c05c94da9e523f000218977
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997891"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="fdd35-103">Priročnik za upravitelje virov (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fdd35-103">Resource manager guide (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fdd35-104">Zmogljivosti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v programu [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] vam omogočajo, da najdete ustrezne vire ob ustreznem času za ustrezni projekt ter poskrbite, da se vsi viri uporabljajo učinkovito.</span><span class="sxs-lookup"><span data-stu-id="fdd35-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="fdd35-105">Uspešno in učinkovito uvajanje svetovalcev podjetja s programom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fdd35-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="fdd35-106">Te vam zagotavljajo orodja, ki so potrebna za načrtovanje virov na podlagi zahtev in urnikov svetovalskih projektov ter znanja in razpoložljivosti svetovalcev.</span><span class="sxs-lookup"><span data-stu-id="fdd35-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="fdd35-107">Hitro lahko poiščete najbolj usposobljene svetovalce, ki so na voljo za delo s projekti, in dobite vpogled v to, kako jih lahko bolje načrtujete med posameznimi projekti.</span><span class="sxs-lookup"><span data-stu-id="fdd35-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="fdd35-108">Načrtovanje virov omogoča naslednje:</span><span class="sxs-lookup"><span data-stu-id="fdd35-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="fdd35-109">Iskanje virov za projekte na podlagi tega, kako njihovo znanje in stopnje usposobljenosti ustrezajo zahtevam za vir projekta.</span><span class="sxs-lookup"><span data-stu-id="fdd35-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="fdd35-110">Iskanje urnika vira za koledar projekta na podlagi razpoložljivosti in načrtovanega prostega časa vira.</span><span class="sxs-lookup"><span data-stu-id="fdd35-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="fdd35-111">Koledar, označen z barvami, ponazarja razpoložljivost virov.</span><span class="sxs-lookup"><span data-stu-id="fdd35-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="fdd35-112">Pregledovanje zmogljivosti vsakega svetovalca in ugotavljanje, kako je ta zmogljivost izkoriščena.</span><span class="sxs-lookup"><span data-stu-id="fdd35-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="fdd35-113">To vam lahko pomaga pri ugotavljanju, ali so posamezni svetovalci premalo ali preveč obremenjeni oz. ali delajo v skladu s svojimi zmogljivostmi.</span><span class="sxs-lookup"><span data-stu-id="fdd35-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="fdd35-114">Dodeljevanje odstotka ali določenega števila ur delavčeve zmogljivosti projektu.</span><span class="sxs-lookup"><span data-stu-id="fdd35-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="fdd35-115">Rezervacije skupine virov.</span><span class="sxs-lookup"><span data-stu-id="fdd35-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="fdd35-116">Načrtovana ali potrjena rezervacija virov in pretvorba načrtovanih ur v potrjene v enem koraku.</span><span class="sxs-lookup"><span data-stu-id="fdd35-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="fdd35-117">Samodejno oblikovanje projektne ekipe na podlagi virov, določenih v strukturirani členitvi dela za projekt.</span><span class="sxs-lookup"><span data-stu-id="fdd35-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="fdd35-118">Izvrševanje zahtev za vire (rezervacije, predlogi, iskanje nadomestnih virov).</span><span class="sxs-lookup"><span data-stu-id="fdd35-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="fdd35-119">Dodeljevanje virov glede na osrednji model (dodeljuje upravitelj virov) ali hibridni model (poleg upravitelja virov lahko dodeljujejo drugi vodje).</span><span class="sxs-lookup"><span data-stu-id="fdd35-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="fdd35-120">Če želite več informacij o nastavljanju osrednjega ali hibridnega modela upravljanja virov, glejte [Konfiguracija nastavitev dodatnih parametrov (Project Service)](../psa/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="fdd35-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="fdd35-121">Vire lahko učinkovito upravljate za različne projekte in zagotavljate, da je za vse projekte dodeljeno ustrezno osebje.</span><span class="sxs-lookup"><span data-stu-id="fdd35-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="fdd35-122">Izvajati boste morali naslednje naloge:</span><span class="sxs-lookup"><span data-stu-id="fdd35-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="fdd35-123">[Upravljanje zahtev za vire](../psa/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="fdd35-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="fdd35-124">Poiskati ustrezna znanja in usposobljenost svetovalcev za projekte.</span><span class="sxs-lookup"><span data-stu-id="fdd35-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="fdd35-125">[Ogled razpoložljivosti vira](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="fdd35-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="fdd35-126">Preveriti razpoložljivost svetovalcev v pogledu koledarja.</span><span class="sxs-lookup"><span data-stu-id="fdd35-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="fdd35-127">[Ogled uporabe virov](../psa/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="fdd35-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="fdd35-128">Preveriti odstotek časa, ko so svetovalci trenutno rezervirani.</span><span class="sxs-lookup"><span data-stu-id="fdd35-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="fdd35-129">[Razporejanje svetovalcev za projekt](../psa/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="fdd35-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="fdd35-130">Razporedite svetovalce za projekt.</span><span class="sxs-lookup"><span data-stu-id="fdd35-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="fdd35-131">Če želite več informacij o pošiljanju zahtev za vire za posamezne projekte, glejte [Pošiljanje zahtev za vire](../psa/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="fdd35-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fdd35-132">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="fdd35-132">See Also</span></span>  
 <span data-ttu-id="fdd35-133">[Pregled rešitve Project Service](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="fdd35-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="fdd35-134">[Vodnik za skrbnike](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fdd35-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="fdd35-135">[Vodnik za upravitelja kupcev](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fdd35-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="fdd35-136">[Priročnik za vodje projektov](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fdd35-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="fdd35-137">Vodnik po času, stroških in sodelovanju</span><span class="sxs-lookup"><span data-stu-id="fdd35-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]