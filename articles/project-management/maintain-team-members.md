---
title: Vzdrževanje članov ekipe
description: Ta tema vsebuje informacije o rezervaciji poimenovanih virov projektne ekipe in njihovi dodelitvi opravilom.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 60b6788d881518502d314e9ee5daf6bbc0ae8764
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286853"
---
# <a name="maintain-team-members"></a><span data-ttu-id="72795-103">Vzdrževanje članov ekipe</span><span class="sxs-lookup"><span data-stu-id="72795-103">Maintain team members</span></span>

<span data-ttu-id="72795-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="72795-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="72795-105">Poimenovani vir lahko v projektno ekipo dodate tako, da ga neposredno rezervirate v ekipi.</span><span class="sxs-lookup"><span data-stu-id="72795-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="72795-106">V aplikaciji Dynamics 365 Project Operations odprite razdelek **Projekti** in odprite projekt, za katerega želite izvesti rezervacijo.</span><span class="sxs-lookup"><span data-stu-id="72795-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="72795-107">Na strani **Projekt** na zavihku **Ekipa** izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="72795-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="72795-108">V pogovornem oknu **Hitro ustvarjanje člana projektne ekipe** izberite vir, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="72795-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="72795-109">Polje **Vloga** bo izpolnjeno s privzeto vlogo vira, če ima dodeljeno.</span><span class="sxs-lookup"><span data-stu-id="72795-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="72795-110">Vlogo lahko spremenite.</span><span class="sxs-lookup"><span data-stu-id="72795-110">You can change the role.</span></span> 
4. <span data-ttu-id="72795-111">Izberite začetni in končni datum obdobja, v katerem potrebujete vir, in izberite način dodeljevanja zmogljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="72795-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="72795-112">V polju **Odobritelj projekta** izberite **Da**, če želite članu ekipe dodeliti vlogo odobritelja projekta.</span><span class="sxs-lookup"><span data-stu-id="72795-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="72795-113">Član ekipe bo tako lahko odobril poslane časovne vnose in vnose stroškov za ta projekt.</span><span class="sxs-lookup"><span data-stu-id="72795-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="72795-114">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="72795-114">Select **Save**.</span></span>

<span data-ttu-id="72795-115">Rezervirani vir lahko sedaj dodelite opravilom za projekt.</span><span class="sxs-lookup"><span data-stu-id="72795-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="72795-116">Na strani **Projekt** na zavihku **Razpored** dodelite opravila novemu viru.</span><span class="sxs-lookup"><span data-stu-id="72795-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="72795-117">V polju **Viri** na mreži opravil se odpre izbirnik za vire, v katerem so prikazani člani ekipe, ki jih lahko izberete.</span><span class="sxs-lookup"><span data-stu-id="72795-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="72795-118">V storitvi Project Operations rezervacije virov in dodelitve opravil niso tesno povezane.</span><span class="sxs-lookup"><span data-stu-id="72795-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="72795-119">Pri uporabi izbirnika virov v razporedu lahko članom ekipe dodelite opravila za več ur, kot jih je zajetih v rezervacijah za projekt.</span><span class="sxs-lookup"><span data-stu-id="72795-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="72795-120">Razlike med rezervacijami in dodelitvami članov ekipe so prikazane na zavihkih **Ekipa** in **Uskladitev virov**.</span><span class="sxs-lookup"><span data-stu-id="72795-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="72795-121">Razlike med rezervacijami in dodelitvami virov lahko tudi uskladite na podrobnejši ravni.</span><span class="sxs-lookup"><span data-stu-id="72795-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="72795-122">Izbirnik za vire na zavihku **Razpored** lahko uporabite za iskanje in izbiro virov, ki jih je mogoče rezervirati, vendar še niso del projektne ekipe.</span><span class="sxs-lookup"><span data-stu-id="72795-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="72795-123">Ti viri so v izbirniku virov prikazani kot **Drugi viri**.</span><span class="sxs-lookup"><span data-stu-id="72795-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="72795-124">Ko opravite izbor, je vir dodan projektni ekipi in dodeljen opravilu, vendar se pri tem ne ustvari rezervacija.</span><span class="sxs-lookup"><span data-stu-id="72795-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="72795-125">Za rezervacijo zmogljivosti vira za projekt lahko uporabite funkcijo razširjanja rezervacij na zavihku **Uskladitev** ali **ploščo razporeda**.</span><span class="sxs-lookup"><span data-stu-id="72795-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="72795-126">Ko je član ekipe rezerviran za vaš projekt, lahko uporabite možnost **Upravljanje rezervacij** ali **Plošča razporeda** ter neposredno urejate njegove rezervacije.</span><span class="sxs-lookup"><span data-stu-id="72795-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]