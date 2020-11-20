---
title: Rezervacija poimenovanih virov iz zahtevanih pogojev za vire
description: Ta tema vsebuje informacije o rezervaciji imenovanih virov za zahtevo za splošni vir.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: d7ff58ec08661adc702867c6c26805a74a3637c9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125918"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="b472d-103">Rezervacija poimenovanih virov iz zahtevanih pogojev za vire</span><span class="sxs-lookup"><span data-stu-id="b472d-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b472d-104">Poimenovani vir lahko rezervirate za zamenjavo splošnega vira, ki ima zahtevani pogoj za vir.</span><span class="sxs-lookup"><span data-stu-id="b472d-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="b472d-105">V aplikaciji Project Service Automation (PSA) na strani **Projekti** kliknite zavihek **Ekipa**.</span><span class="sxs-lookup"><span data-stu-id="b472d-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="b472d-106">Izberite splošni vir, ki ima zahtevani pogoj za vir, s seznama in nato kliknite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="b472d-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="b472d-107">Ali pa odprite zahtevani pogoj za vir in kliknite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="b472d-107">Or, open the resource requirement and then click **Book**.</span></span>


![Rezervacija splošnega člana ekipe](media/RM-how-to-14.png)


3. <span data-ttu-id="b472d-109">Na strani **Pomočnik za razporejanje** izberite poimenovani vir, ki ga želite rezervirati za projektno ekipo in nato kliknite **Rezerviraj.**</span><span class="sxs-lookup"><span data-stu-id="b472d-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Rezervacija splošnega člana ekipe s pomočnikom za razporejanje](media/RM-how-to-15.png)

<span data-ttu-id="b472d-111">Ko je rezervacija dokončana in izpolnjena s poimenovanim virom, se splošni vir zamenja s poimenovanim virom.</span><span class="sxs-lookup"><span data-stu-id="b472d-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Nadomestitev splošnega člana ekipe s poimenovanim članom ekipe](media/RM-how-to-16.png)

<span data-ttu-id="b472d-113">S poimenovanim virom se posodobijo tudi dodelitve v razporedu.</span><span class="sxs-lookup"><span data-stu-id="b472d-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Dodelitev poimenovanega člana ekipe projektnim opravilom](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="b472d-115">Izpolnjevanje splošnega vira z več poimenovanimi viri</span><span class="sxs-lookup"><span data-stu-id="b472d-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="b472d-116">Izpolnjevanje zahtevanega pogoja za splošni vir z več poimenovanimi viri je podobno dodeljevanju enega samega poimenovanega vira.</span><span class="sxs-lookup"><span data-stu-id="b472d-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="b472d-117">Če imate na primer opravilo, ki ima trajanje pet dni in 120 ur obsega dela.</span><span class="sxs-lookup"><span data-stu-id="b472d-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="b472d-118">Tega opravila ni mogoče dokončati z enim virom, ki dela osem ur dnevno v petdnevnem tednu.</span><span class="sxs-lookup"><span data-stu-id="b472d-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Opravilo, za katero je zahtevanih 120 ur obsega dela v petih dneh](media/RM-how-to-21.png)

<span data-ttu-id="b472d-120">Zahteva velja za 120 ur inženirske robotike v petih dneh, kar je 24 ur na dan.</span><span class="sxs-lookup"><span data-stu-id="b472d-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Zahteva na dan](media/RM-how-to-22.png)

<span data-ttu-id="b472d-122">To je primer, ko je za izpolnjevanje zahteve za splošni vir potrebnih več poimenovanih virov.</span><span class="sxs-lookup"><span data-stu-id="b472d-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="b472d-123">Za izpolnitev zahteve morate rezervirati več virov.</span><span class="sxs-lookup"><span data-stu-id="b472d-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Rezervacija več virov za izpolnjevanje zahteve](media/RM-how-to-23.png)

<span data-ttu-id="b472d-125">Glavna razlika v tem primeru je, da splošni vir ostane v ekipi, ki je dodeljena opravilu, rezervirani člani ekipe poimenovanega vira pa niso dodeljeni kot del položaja.</span><span class="sxs-lookup"><span data-stu-id="b472d-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="b472d-126">Vodja projekta lahko delo ustrezno dodeli poimenovanim virom.</span><span class="sxs-lookup"><span data-stu-id="b472d-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="b472d-127">S pogledom **Uskladitev** si lahko vodja projekta pomaga pri razdelitvi rezervacij več virov na dodelitve opravil.</span><span class="sxs-lookup"><span data-stu-id="b472d-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="b472d-128">To se ne izvede samodejno, ker je v vseh bolj zapletenih primerih od zgornjega, npr. ko imate paket opravil, ki sestavljajo zahtevo, treba domnevati način, na katerega želi vodja projekta dodeliti opravila.</span><span class="sxs-lookup"><span data-stu-id="b472d-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="b472d-129">Ker sistem ne more razumeti tega namena, je mogoče, da bodo predpostavke drugačne od predvidenih in lahko pride do napačnih ali nepredvidljivih rezultatov.</span><span class="sxs-lookup"><span data-stu-id="b472d-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="b472d-130">Predvidljiv rezultat je, da splošni vir ostane dodeljen, dokler vodja projekta namenoma ne ustvari dodelitev prek pogleda **Uskladitev**.</span><span class="sxs-lookup"><span data-stu-id="b472d-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


