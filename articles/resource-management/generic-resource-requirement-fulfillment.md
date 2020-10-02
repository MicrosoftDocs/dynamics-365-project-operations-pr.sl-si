---
title: Izpolnitev zahteve za splošni vir
description: Ta tema vsebuje informacije o rezervaciji imenovanih virov za zahtevo za splošni vir.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897606"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="09325-103">Izpolnitev zahteve za splošni vir</span><span class="sxs-lookup"><span data-stu-id="09325-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="09325-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="09325-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="09325-105">Poimenovani vir lahko rezervirate za zamenjavo splošnega vira, ki ima zahtevani pogoj za vir.</span><span class="sxs-lookup"><span data-stu-id="09325-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="09325-106">Na strani **Projekti** izberite zavihek **Ekipa**.</span><span class="sxs-lookup"><span data-stu-id="09325-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="09325-107">Izberite splošni vir, ki ima zahtevani pogoj za vir, s seznama in nato izberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="09325-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="09325-108">Ali pa odprite zahtevani pogoj za vir in izberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="09325-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="09325-109">Na strani **Pomočnik za razporejanje** izberite poimenovani vir, ki ga želite rezervirati za projektno ekipo in nato izberite **Rezerviraj.**</span><span class="sxs-lookup"><span data-stu-id="09325-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="09325-110">Ko je rezervacija dokončana in izpolnjena s poimenovanim virom, se splošni vir zamenja s poimenovanim virom.</span><span class="sxs-lookup"><span data-stu-id="09325-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="09325-111">S poimenovanim virom se posodobijo tudi dodelitve v razporedu.</span><span class="sxs-lookup"><span data-stu-id="09325-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="09325-112">Izpolnjevanje splošnega vira z več poimenovanimi viri</span><span class="sxs-lookup"><span data-stu-id="09325-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="09325-113">Izpolnjevanje zahtevanega pogoja za splošni vir z več poimenovanimi viri je podobno dodeljevanju enega samega poimenovanega vira.</span><span class="sxs-lookup"><span data-stu-id="09325-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="09325-114">Če imate na primer opravilo, ki ima trajanje pet dni in 120 ur obsega dela.</span><span class="sxs-lookup"><span data-stu-id="09325-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="09325-115">Tega opravila ni mogoče dokončati z enim virom, ki dela osem ur dnevno v petdnevnem tednu.</span><span class="sxs-lookup"><span data-stu-id="09325-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="09325-116">Zahteva velja za 120 ur inženirske robotike v petih dneh, kar je 24 ur na dan.</span><span class="sxs-lookup"><span data-stu-id="09325-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="09325-117">To je primer, ko je za izpolnjevanje zahteve za splošni vir potrebnih več poimenovanih virov.</span><span class="sxs-lookup"><span data-stu-id="09325-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="09325-118">Za izpolnitev zahteve morate rezervirati več virov.</span><span class="sxs-lookup"><span data-stu-id="09325-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="09325-119">Glavna razlika v tem primeru je, da splošni vir ostane v ekipi, ki je dodeljena opravilu, rezervirani člani ekipe poimenovanega vira pa niso dodeljeni kot del položaja.</span><span class="sxs-lookup"><span data-stu-id="09325-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="09325-120">Vodja projekta lahko delo ustrezno dodeli poimenovanim virom.</span><span class="sxs-lookup"><span data-stu-id="09325-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="09325-121">S pogledom **Uskladitev** si lahko vodja projekta pomaga pri razdelitvi rezervacij več virov na dodelitve opravil.</span><span class="sxs-lookup"><span data-stu-id="09325-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="09325-122">To se ne izvede samodejno, ker v vseh bolj zapletenih primerih od enostavnega zgornjega, npr. ko imate paket opravil, ki sestavljajo zahtevo, ali namen, kako želi vodja projekta dodeliti opravila, sistem predpostavlja.</span><span class="sxs-lookup"><span data-stu-id="09325-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="09325-123">Ker sistem ne more razumeti namena, je verjetno, da bodo predpostavke drugačne od nameravanih in lahko pride do napačnega ali nepredvidljivega rezultata.</span><span class="sxs-lookup"><span data-stu-id="09325-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="09325-124">Predvidljiv rezultat je, da splošni vir ostane dodeljen, dokler vodja projekta namenoma ne ustvari dodelitev prek pogleda **Uskladitev**.</span><span class="sxs-lookup"><span data-stu-id="09325-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


