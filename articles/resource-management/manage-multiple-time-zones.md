---
title: Upravljanje časovnih pasov
description: Ko je ustvarjen projekt, njegov časovni pas temelji na časovnem pasu, določenem v uporabljeni predlogi za delovne ure.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997756"
---
# <a name="manage-time-zones"></a><span data-ttu-id="b0fc6-103">Upravljanje časovnih pasov</span><span class="sxs-lookup"><span data-stu-id="b0fc6-103">Manage time zones</span></span>

<span data-ttu-id="b0fc6-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="b0fc6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="b0fc6-105">Projekti</span><span class="sxs-lookup"><span data-stu-id="b0fc6-105">Projects</span></span>

<span data-ttu-id="b0fc6-106">Ko je ustvarjen projekt, njegov časovni pas temelji na časovnem pasu, določenem v uporabljeni predlogi za delovne ure.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="b0fc6-107">Pri možnosti **Projekt** so datumi vedno odvisni od časovnega pasu uporabnika, ki je prijavljen v vsak zavihek, z izjemo zavihka **Opravilo**. Ko si ogledate strukturirano členitev dela, bodo datumi vedno prikazani v časovnem pasu projekta.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="b0fc6-108">Opravila</span><span class="sxs-lookup"><span data-stu-id="b0fc6-108">Tasks</span></span>

<span data-ttu-id="b0fc6-109">Ko je ustvarjeno opravilo, so začetni in končni čas ter ure/dan upravljane prek delovnega časa za projekt.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="b0fc6-110">Če na primer ustvarite opravilo s projektom, katerega časovni pas je -8 PST in ima naslednji delovni čas: od 9.00 do 17.00 od ponedeljka do petka, bo vsako opravilo, ustvarjeno brez dodelitev, upoštevalo začetni in končni čas koledarja projekta.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="b0fc6-111">Upravljanje virov s časovnimi pasovi</span><span class="sxs-lookup"><span data-stu-id="b0fc6-111">Manage resources with time zones</span></span>

<span data-ttu-id="b0fc6-112">Za natančne in predvidljive rezultate pri uporabi možnosti **Podaljšaj rezervacijo** morata biti izpolnjena dva ključna predpogoja:</span><span class="sxs-lookup"><span data-stu-id="b0fc6-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="b0fc6-113">Uporabnik mora konfigurirati časovni pas svoje naprave, da se ujema s časovnim pasom, določenim v sistemski možnosti **Nastavitve za prilagoditev**.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Nastavitve časovnega pasu v sistemu Windows 10](media/reconcile-assignments-03.png)

  ![Nastavitve časovnega pasu v nastavitvah za prilagoditev](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="b0fc6-116">Vir, ki ga je mogoče rezervirati, mora imeti najmanj eno minuto delovnega časa, ki se prekriva z obrisi, ki se uporabijo za opredelitev zahtevanega podaljšanja.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="b0fc6-117">Primer: naslednji viri z delovnim časom med 9:00 in 19:00.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Primerjava obrisov virov](media/reconcile-assignments-05.png)

<span data-ttu-id="b0fc6-119">V spodnji tabeli so prikazani:</span><span class="sxs-lookup"><span data-stu-id="b0fc6-119">The following table shows:</span></span>

- <span data-ttu-id="b0fc6-120">Predloga koledarja projekta</span><span class="sxs-lookup"><span data-stu-id="b0fc6-120">A project calendar template</span></span>
- <span data-ttu-id="b0fc6-121">Vir A: ta vir ima isti koledar in je v istem časovnem pasu kot projekt.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="b0fc6-122">Začetni čas rezervacij bo 9.00.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="b0fc6-123">Vir B: ta vir se nahaja v drugačnem časovnem pasu kot projekt in se začne ob 7:00 v svojem časovnem pasu.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="b0fc6-124">Toda rezervacije se bodo začele ob 9.00, saj je to najzgodnejši čas za obris dodelitve.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="b0fc6-125">Vira C in D: vira se nahajata v različnih časovnih pasovih, ki se razlikujeta med seboj in od projekta, njune rezervacije pa se ne začnejo prej kot njihovi razpoložljivi začetni časi.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="b0fc6-126">Entiteta</span><span class="sxs-lookup"><span data-stu-id="b0fc6-126">Entity</span></span>  |<span data-ttu-id="b0fc6-127">Koledar</span><span class="sxs-lookup"><span data-stu-id="b0fc6-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="b0fc6-128">Predloga projektnega koledarja</span><span class="sxs-lookup"><span data-stu-id="b0fc6-128">Project calendar template</span></span>   | ![projektni koledar](media/reconcile-assignments-06.png) |
|<span data-ttu-id="b0fc6-130">Vir A</span><span class="sxs-lookup"><span data-stu-id="b0fc6-130">Resource A</span></span>  | ![Koledar vira A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="b0fc6-132">Vir B</span><span class="sxs-lookup"><span data-stu-id="b0fc6-132">Resource B</span></span>  |  ![Koledar vira B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="b0fc6-134">Vir C</span><span class="sxs-lookup"><span data-stu-id="b0fc6-134">Resource C</span></span>  |  ![Koledar vira C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="b0fc6-136">Vir D</span><span class="sxs-lookup"><span data-stu-id="b0fc6-136">Resource D</span></span>  | ![Koledar vira D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="b0fc6-138">Ko se pomaknete do pogleda **Uskladitev**, so prikazane dodelitve virov in s tem povezani primanjkljaj rezervacij.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Pogleda usklajevanja pred podaljšanjem](media/reconcile-assignments-10.png)

<span data-ttu-id="b0fc6-140">Ko je bila za vsak vir uporabljena funkcija podaljšanja rezervacije, se rezervacije uspešno podaljšajo za vsak vir, ker se delovni čas vsakega vira prekriva z obrisi primanjkljaja.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Pogled usklajevanja po podaljšanju rezervacije](media/reconcile-assignments-11.png) 

<span data-ttu-id="b0fc6-142">Upoštevajte, da natančnejši pregled podrobnosti rezervacij pokaže razlike v začetnih časih rezervacij.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="b0fc6-143">Rezervacije se začnejo šele ob začetnem času obrisa dodelitve in šele ob razpoložljivem začetnem času vira.</span><span class="sxs-lookup"><span data-stu-id="b0fc6-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nove rezervacije virov v plošči razporeda](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]