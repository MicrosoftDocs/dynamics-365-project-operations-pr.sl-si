---
title: Rezervacija poimenovanih virov, ki jih je mogoče rezervirati, za projektno ekipo in dodelitev opravil
description: Ta tema vsebuje informacije o rezervaciji poimenovanih virov projektne ekipe in njihovi dodelitvi opravilom.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: d8a49b6ae8423cb99c710e40704475b4a71d3724
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145378"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="fa1b9-103">Rezervacija poimenovanih virov, ki jih je mogoče rezervirati, za projektno ekipo in dodelitev opravil</span><span class="sxs-lookup"><span data-stu-id="fa1b9-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fa1b9-104">Poimenovan vir lahko v projektno ekipo lahko dodate tako, da ga neposredno rezervirate v ekipi.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="fa1b9-105">Pri tem upoštevajte spodnja navodila.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="fa1b9-106">V aplikaciji Project Service Automation odprite možnost **Projekti** in odprite projekt, za katerega želite izvesti rezervacijo.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="fa1b9-107">Na strani **Projekt** na zavihku **Ekipa** kliknite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Dodajanje člana ekipe na zavihku ekipe](media/RM-how-to-1.png)

3. <span data-ttu-id="fa1b9-109">V pogovornem oknu **Hitro ustvarjanje člana projektne ekipe** izberite vir, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="fa1b9-110">Polje **Vloga** bo izpolnjeno s privzeto vlogo vira, če ima dodeljeno.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="fa1b9-111">Po potrebi lahko vlogo tudi spremenite.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="fa1b9-112">Izberite začetni in končni datum obdobja, v katerem potrebujete vir, in izberite način dodeljevanja zmogljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="fa1b9-113">Če želite, da je član ekipe odobritelj projekta, v polju možnosti **Odobritelj projekta** izberite **Da**.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="fa1b9-114">To pomeni, da lahko član ekipe odobri poslane časovne vnose in vnose stroškov za ta projekt.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="fa1b9-115">Kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-115">Click **Save**.</span></span>

![Dodajanje člana ekipe v obrazcu za hitro ustvarjanje](media/RM-how-to-2.png)


<span data-ttu-id="fa1b9-117">Rezervirani vir lahko sedaj dodelite opravilom za projekt.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="fa1b9-118">Na strani **Projekt** kliknite zavihek **Razpored** in dodelite opravila novemu viru.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="fa1b9-119">V polju **Viri** na mreži opravil se odpre izbirnik za vire, v katerem so prikazani člani ekipe, ki jih lahko izberete.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Dodeljevanje člana ekipe opravilu na zavihku razporeda](media/RM-how-to-3.png)

<span data-ttu-id="fa1b9-121">V tretji različici aplikacije Project Service Automation (PSA) rezervacije virov in dodelitve opravil niso tesno povezane.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="fa1b9-122">To pomeni, da lahko pri uporabi izbirnika virov v razporedu članom ekipe dodelite opravila za več ur, kot jih je zajetih v rezervacijah za projekt.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="fa1b9-123">Razlike med rezervacijami in dodelitvami člana ekipe lahko vidite na zavihku **Ekipa** ali na zavihku **Uskladitev virov**. Razlike med rezervacijami in dodelitvami virov lahko uskladite tudi na ravni s več podrobnostmi.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Zavihek za uskladitev virov](media/RM-how-to-4.png)

<span data-ttu-id="fa1b9-125">Izbirnik za vire na zavihku **Razpored** lahko uporabite tudi za iskanje in izbiro virov, ki jih je mogoče rezervirati, vendar še niso del projektne ekipe.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="fa1b9-126">Ti so prikazani v izbirniku virov prikazani kot **Drugi viri**.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Dodeljevanje vira, ki ni član ekipe, za opravilo](media/RM-how-to-5.png)

<span data-ttu-id="fa1b9-128">Ko to naredite, je vir dodan projektni ekipi in dodeljen opravilu, vendar se pri tem ne ustvari rezervacija.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Član ekipe z dodelitvami in brez rezervacij](media/RM-how-to-6.png)

<span data-ttu-id="fa1b9-130">Za rezervacijo zmogljivosti vira za projekt lahko uporabite funkcijo razširjanja rezervacij na zavihku **Uskladitev** ali **ploščo razporeda**.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Razširjanje rezervacij za člana ekipe na zavihku za uskladitev virov](media/RM-how-to-7.png)

<span data-ttu-id="fa1b9-132">Ko je član ekipe rezerviran za vaš projekt, lahko uporabite možnost »Upravljanje rezervacij« ali ploščo razporeda ter neposredno urejate njegove rezervacije.</span><span class="sxs-lookup"><span data-stu-id="fa1b9-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
