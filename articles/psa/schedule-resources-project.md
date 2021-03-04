---
title: Razporejanje virov za projekt
description: Kako razporejati vire za projekt v rešitvi Project Service
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
ms.openlocfilehash: e39c95386eb2dd31fb54878bc203bd94931274de
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150463"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="2a28a-103">Razporejanje virov za projekt (Project Service)</span><span class="sxs-lookup"><span data-stu-id="2a28a-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2a28a-104">Preverite lahko razpoložljivost virov za hiter pregled nad rezerviranostjo vaših virov, lahko pa filtrirate pogled glede na znanja, ekipo, lokacijo in druge možnosti.</span><span class="sxs-lookup"><span data-stu-id="2a28a-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="2a28a-105">Na plošči razporeda je prikazan seznam virov in njihova razpoložljivost.</span><span class="sxs-lookup"><span data-stu-id="2a28a-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="2a28a-106">Izberite način pogleda za prikaz razpoložljivosti glede na **Ure**, **Dan**, **Teden** ali **Mesec**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="2a28a-107">Preden uporabite ploščo razporeda, je pomembno, da jo nastavite.</span><span class="sxs-lookup"><span data-stu-id="2a28a-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="2a28a-108">Za več informacij glejte [Konfiguriranje plošče razporeda (storitve Field Service ali storitve Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="2a28a-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="2a28a-109">Če uporabljate starejšo različico, za razpoložljivost virov glejte [Ogled razpoložljivosti virov](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="2a28a-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="2a28a-110">Če želite uporabljati funkcijo rezervacij plošče za načrtovanje, geokodiranje in lokacijske storitve, morate vklopiti zemljevide.</span><span class="sxs-lookup"><span data-stu-id="2a28a-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="2a28a-111">V glavnem meniju izberite **Razporejanje virov** > **Skrbništvo**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="2a28a-112">Kliknite **Parametri razporejanja**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="2a28a-113">Odprite zapis in se pomaknite navzdol do razdelka **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="2a28a-114">V polju **Vzpostavi povezavo z zemljevidi** izberite **Da**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="2a28a-115">Sprejmite pogoje in shranite zapis.</span><span class="sxs-lookup"><span data-stu-id="2a28a-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="2a28a-116">V glavnem meniju izberite **Project Service** > **Plošča razporeda**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="2a28a-117">Zdaj lahko zahtevo rezervacije ročno razporedite na več načinov.</span><span class="sxs-lookup"><span data-stu-id="2a28a-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="2a28a-118">Izberite metodo, ki deluje za vas.</span><span class="sxs-lookup"><span data-stu-id="2a28a-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="2a28a-119">Iskanje razpoložljivih virov</span><span class="sxs-lookup"><span data-stu-id="2a28a-119">Find available resources</span></span>

1.  <span data-ttu-id="2a28a-120">Na seznamu **Zahteva rezervacije** z desno tipko miške kliknite nenačrtovano rezervacijo in izberite eno od naslednjih možnosti:</span><span class="sxs-lookup"><span data-stu-id="2a28a-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="2a28a-121">Če želite poiskati razpoložljiv vir s seznama na plošči razporeda, izberite možnost **Iskanje razpoložljivosti – trenutni viri**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="2a28a-122">Če želite poiskati razpoložljiv vir med viri, ki so na voljo v sistemu, izberite možnost **Iskanje razpoložljivosti – vsi viri**</span><span class="sxs-lookup"><span data-stu-id="2a28a-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="2a28a-123">Ko izberete možnost, se prek filtrov prikažejo možnosti za izbrano zahtevo rezervacije.</span><span class="sxs-lookup"><span data-stu-id="2a28a-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="2a28a-124">Ko vidite režo, ki je na voljo, z desno tipko miške kliknite časovni okvir na plošči razporeda in izberite možnost **Rezerviraj tukaj**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="2a28a-125">Ali pa zahtevo rezervacije povlecite in spustite v časovni okvir, ki je na voljo.</span><span class="sxs-lookup"><span data-stu-id="2a28a-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="2a28a-126">Rezervacija vira prek dnevnega pogleda in iskanje oseb s premalo rezervacijami</span><span class="sxs-lookup"><span data-stu-id="2a28a-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="2a28a-127">Na plošči razporeda izberite **Način pogleda** in izberite **Dnevi**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="2a28a-128">Tukaj je prikazan pogled mreže, v katerem je navedeno število ur na dan, ko je vir rezerviran, in so navedeni dnevi, ko je vir prost.</span><span class="sxs-lookup"><span data-stu-id="2a28a-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="2a28a-129">Kliknite ime vira, ki ga želite rezervirati, in nato izberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="2a28a-130">V pogovornem oknu **Rezervacija virov (ustvarjanje)** izberite projekt, za katerega želite rezervirati vir, način rezervacije ter začetni in končni čas rezervacije.</span><span class="sxs-lookup"><span data-stu-id="2a28a-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="2a28a-131">Ko končate, izberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="2a28a-132">Ogled plošče razporeda</span><span class="sxs-lookup"><span data-stu-id="2a28a-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="2a28a-133">S seznama na dnu izberite nerazporejeno zahtevo rezervacije.</span><span class="sxs-lookup"><span data-stu-id="2a28a-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="2a28a-134">Povlecite zahtevo rezervacije do razpoložljivega vira/časovnega okvira na plošči razporeda.</span><span class="sxs-lookup"><span data-stu-id="2a28a-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="2a28a-135">Ko končate, izberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="2a28a-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="2a28a-136">Dodatni viri</span><span class="sxs-lookup"><span data-stu-id="2a28a-136">Additional resources</span></span>  
 [<span data-ttu-id="2a28a-137">Priročnik za upravitelje virov</span><span class="sxs-lookup"><span data-stu-id="2a28a-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
