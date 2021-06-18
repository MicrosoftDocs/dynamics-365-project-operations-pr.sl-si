---
title: Pregled predlaganih virov
description: Ta tema vsebuje informacije o tem, kako predlagati projektne vire.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000771"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="a1d1c-103">Pregled predlaganih virov</span><span class="sxs-lookup"><span data-stu-id="a1d1c-103">Review proposed resources</span></span>

<span data-ttu-id="a1d1c-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="a1d1c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a1d1c-105">Upravitelji virov lahko vodji projekta predlagajo vir prek zahteve za vir.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="a1d1c-106">V mreži zahtev ali sami zahtevi izberite **Poišči vire**.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="a1d1c-107">Na strani **Pomočnik za razporejanje** izberite vir in nato v polju **Stanje rezervacije** v podoknu **Ustvari rezervacijo vira** izberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="a1d1c-108">Pojavijo se naslednje posodobitve stanja:</span><span class="sxs-lookup"><span data-stu-id="a1d1c-108">The following status updates occur:</span></span>

- <span data-ttu-id="a1d1c-109">Na strani **Pomočnik za razporejanje** se kazalniki stanja posodobijo in sporočajo, da je rezervacija šele predlagana in ne potrjena.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="a1d1c-110">V zahtevi za vir se stanje spremeni v **Potreben pregled**.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="a1d1c-111">Na zavihku **Ekipa** izbranega projekta se vrednost splošnega člana ekipe **Stanje zahteve** spremeni v **Potreben pregled**.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="a1d1c-112">Vodja projekta lahko predlog sprejme ali zavrne.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="a1d1c-113">Upravitelji virov lahko za obdelavo zahtev za vire uporabijo katerega koli od spodaj navedenih pristopov:</span><span class="sxs-lookup"><span data-stu-id="a1d1c-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="a1d1c-114">Predlagajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil zahtevane ure.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="a1d1c-115">Predlagane ure se nato razdelijo med več virov, ki lahko opravijo zahtevane ure.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="a1d1c-116">V tem primeru se ure ne morejo prekrivati.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="a1d1c-117">Predlagajo manj virov, kot jih zahtevajo.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="a1d1c-118">V tem primeru je predlagana zmogljivost vira manjša od zahtevanih ur, ki jih je določila oseba, ki je podala zahtevo.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="a1d1c-119">Ko torej oseba, ki je podala zahtevo, sprejme predlagane vire, se ustvari neizpolnjena zahteva za vir, ki predstavlja preostalo povpraševanje.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="a1d1c-120">Rezervirajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil delo.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="a1d1c-121">Rezervirajo manj virov, kot jih zahtevajo.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-121">Book fewer resources than are required.</span></span> <span data-ttu-id="a1d1c-122">V tem primeru bo število rezerviranih ur manjše od zahtevanih ur.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="a1d1c-123">Sistem vas vodi k predlaganju virov namesto rezervacij, da lahko oseba, ki je podala zahtevo, preveri in spremlja preostalo povpraševanje.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="a1d1c-124">razpoložljivosti vira</span><span class="sxs-lookup"><span data-stu-id="a1d1c-124">Resource availability</span></span>

<span data-ttu-id="a1d1c-125">Upravitelji virov morajo imeti možnost ogleda razpoložljivosti virov in posodobitve rezervacij.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="a1d1c-126">V nekaterih primerih ni uradnega povpraševanja (zahteve za vir), vendar se mora upravitelj virov odzvati na nenačrtovano povpraševanje, ki prihaja prek različnih kanalov, na primer elektronske pošte, telefonskih klicev ali neposrednih sporočil.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="a1d1c-127">Upravitelji virov uporabljajo ploščo razporeda za posodabljanje virov in rezervacij.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="a1d1c-128">Delovni čas virov se uporablja kot osnova za izračun razpoložljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="a1d1c-129">Rezervacije virov porabijo del zmogljivosti virov.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="a1d1c-130">Na plošči razporeda so za prikaz rezervacij, razpoložljivosti, prezasedenosti in stanja rezervacij uporabljene različne barve in senčenje.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="a1d1c-131">Z izbiro ustrezne nastavitve v nastavitvah plošče razporeda lahko prikažete tudi legendo.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="a1d1c-132">Če je ob posameznem viru, ki ga je mogoče rezervirati, na plošči razporeda prikazana puščica v desno, lahko vir razširite in s tem prikažete podrobnosti o delu, za katerega je vir rezerviran.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="a1d1c-133">Ker rešitev Dynamics 365 Project Operations uporablja mehanizem Universal Resource Scheduling, si lahko tudi vi ogledate podrobnosti o rezervacijah virov za projekte, delovne naloge in vse druge entitete, na katere ste razširili razporejanje, ob predpostavki, da imate nameščeno aplikacijo Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="a1d1c-134">Če si želite ogledati podrobnosti o posameznem viru, ga kliknite z desno tipko miške, da odprete kartico vira.</span><span class="sxs-lookup"><span data-stu-id="a1d1c-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]