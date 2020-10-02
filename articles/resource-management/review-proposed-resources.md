---
title: Pregled predlaganih virov
description: Ta tema vsebuje informacije o tem, kako predlagati projektne vire.
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
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897381"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="a7d47-103">Pregled predlaganih virov</span><span class="sxs-lookup"><span data-stu-id="a7d47-103">Review proposed resources</span></span>

<span data-ttu-id="a7d47-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="a7d47-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a7d47-105">Upravitelji virov lahko vodji projekta predlagajo vir prek zahteve za vir.</span><span class="sxs-lookup"><span data-stu-id="a7d47-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="a7d47-106">V mreži zahtev ali sami zahtevi izberite **Poišči vire**.</span><span class="sxs-lookup"><span data-stu-id="a7d47-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="a7d47-107">Na strani **Pomočnik za razporejanje** izberite vir in nato v polju **Stanje rezervacije** v podoknu **Ustvari rezervacijo vira** izberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="a7d47-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="a7d47-108">Pojavijo se naslednje posodobitve stanja:</span><span class="sxs-lookup"><span data-stu-id="a7d47-108">The following status updates occur:</span></span>

- <span data-ttu-id="a7d47-109">Na strani **Pomočnik za razporejanje** se kazalniki stanja posodobijo in sporočajo, da je rezervacija šele predlagana in ne potrjena.</span><span class="sxs-lookup"><span data-stu-id="a7d47-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="a7d47-110">V zahtevi za vir se stanje spremeni v **Potreben pregled**.</span><span class="sxs-lookup"><span data-stu-id="a7d47-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="a7d47-111">Na zavihku **Ekipa** izbranega projekta se vrednost splošnega člana ekipe **Stanje zahteve** spremeni v **Potreben pregled**.</span><span class="sxs-lookup"><span data-stu-id="a7d47-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="a7d47-112">Vodja projekta lahko predlog sprejme ali zavrne.</span><span class="sxs-lookup"><span data-stu-id="a7d47-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="a7d47-113">Upravitelji virov lahko za obdelavo zahtev za vire uporabijo katerega koli od spodaj navedenih pristopov:</span><span class="sxs-lookup"><span data-stu-id="a7d47-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="a7d47-114">Predlagajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil zahtevane ure.</span><span class="sxs-lookup"><span data-stu-id="a7d47-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="a7d47-115">Predlagane ure se nato razdelijo med več virov, ki lahko opravijo zahtevane ure.</span><span class="sxs-lookup"><span data-stu-id="a7d47-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="a7d47-116">V tem primeru se ure ne morejo prekrivati.</span><span class="sxs-lookup"><span data-stu-id="a7d47-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="a7d47-117">Predlagajo manj virov, kot jih zahtevajo.</span><span class="sxs-lookup"><span data-stu-id="a7d47-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="a7d47-118">V tem primeru je predlagana zmogljivost vira manjša od zahtevanih ur, ki jih je določila oseba, ki je podala zahtevo.</span><span class="sxs-lookup"><span data-stu-id="a7d47-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="a7d47-119">Ko torej oseba, ki je podala zahtevo, sprejme predlagane vire, se ustvari neizpolnjena zahteva za vir, ki predstavlja preostalo povpraševanje.</span><span class="sxs-lookup"><span data-stu-id="a7d47-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="a7d47-120">Rezervirajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil delo.</span><span class="sxs-lookup"><span data-stu-id="a7d47-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="a7d47-121">Rezervirajo manj virov, kot jih zahtevajo.</span><span class="sxs-lookup"><span data-stu-id="a7d47-121">Book fewer resources than are required.</span></span> <span data-ttu-id="a7d47-122">V tem primeru bo število rezerviranih ur manjše od zahtevanih ur.</span><span class="sxs-lookup"><span data-stu-id="a7d47-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="a7d47-123">Sistem vas vodi k predlaganju virov namesto rezervacij, da lahko oseba, ki je podala zahtevo, preveri in spremlja preostalo povpraševanje.</span><span class="sxs-lookup"><span data-stu-id="a7d47-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="a7d47-124">Zaračunana uporaba</span><span class="sxs-lookup"><span data-stu-id="a7d47-124">Billable utilization</span></span>

<span data-ttu-id="a7d47-125">Viri lahko imajo ciljno zaračunano uporabo.</span><span class="sxs-lookup"><span data-stu-id="a7d47-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="a7d47-126">Ta ciljna uporaba je opredeljena kot atribut privzete vloge vira ali nastavljena v zapisu posameznega vira, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="a7d47-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="a7d47-127">Izračuni uporabe temeljijo na dejanskih urah, ki so jih viri poročali na podlagi odobrenih časovnih vnosov.</span><span class="sxs-lookup"><span data-stu-id="a7d47-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="a7d47-128">Za izračun uporabe se uporabljajo naslednje enačbe:</span><span class="sxs-lookup"><span data-stu-id="a7d47-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="a7d47-129">Zaračunana uporaba = dejanske zaračunane ure ÷ zmogljivost vira</span><span class="sxs-lookup"><span data-stu-id="a7d47-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="a7d47-130">Nezaračunana uporaba = dejanski čas z ID-jem vrste obračunavanja = se ne zaračuna, brezplačno ali ni na voljo ÷ zmogljivost vira</span><span class="sxs-lookup"><span data-stu-id="a7d47-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="a7d47-131">Za interno uporabo = dejanski čas brez prodajne pogodbe ÷ zmogljivost vira</span><span class="sxs-lookup"><span data-stu-id="a7d47-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="a7d47-132">Zmogljivost vira = delovni čas vira – odsotnost – prosti dnevi</span><span class="sxs-lookup"><span data-stu-id="a7d47-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="a7d47-133">Pogled **Uporaba vira** lahko najdete v podoknu **Viri**.</span><span class="sxs-lookup"><span data-stu-id="a7d47-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="a7d47-134">Vsaka celica v mreži predstavlja delež zaračunane uporabe vira v določenem obdobju, na primer dnevu, tednu ali mesecu.</span><span class="sxs-lookup"><span data-stu-id="a7d47-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="a7d47-135">Za obarvanje celic se uporabljajo naslednje enačbe:</span><span class="sxs-lookup"><span data-stu-id="a7d47-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="a7d47-136">**Zelena:** zaračunana uporaba \>= ciljna uporaba za vir</span><span class="sxs-lookup"><span data-stu-id="a7d47-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="a7d47-137">**Rumena:** ciljna uporaba – 20 \<= zaračunana uporaba \< ciljna uporaba</span><span class="sxs-lookup"><span data-stu-id="a7d47-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="a7d47-138">**Rdeča:** zaračunana uporaba \< ciljna uporaba – 20</span><span class="sxs-lookup"><span data-stu-id="a7d47-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="a7d47-139">Ker pogled **Uporaba vira** temelji na plošči razporeda, lahko rezultate filtrirate z možnostmi filtriranja na plošči razporeda.</span><span class="sxs-lookup"><span data-stu-id="a7d47-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="a7d47-140">Zaradi mreže morate nastaviti ciljno uporabo za vlogo ali posamezni vir.</span><span class="sxs-lookup"><span data-stu-id="a7d47-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="a7d47-141">To nastavite v možnosti **Viri** \> **Vloge virov**.</span><span class="sxs-lookup"><span data-stu-id="a7d47-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="a7d47-142">Poleg tega morate vsakemu viru, ki ga je mogoče rezervirati, dodati tudi privzeto vlogo.</span><span class="sxs-lookup"><span data-stu-id="a7d47-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="a7d47-143">Odprite možnost **Viri** \> **Viri**.</span><span class="sxs-lookup"><span data-stu-id="a7d47-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="a7d47-144">Na zavihku **Project Service** preverite, ali je vloga vira določena in ali je polje **Je privzeto** nastavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="a7d47-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="a7d47-145">Kjer je vrednost **Je privzeto = Ne**, lahko dodate dodatne vloge.</span><span class="sxs-lookup"><span data-stu-id="a7d47-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="a7d47-146">Vloga, pri kateri je vrednost **Je privzeto = Da**, se uporablja za oceno uporabe vira v primerjavi s ciljem za to vlogo.</span><span class="sxs-lookup"><span data-stu-id="a7d47-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="a7d47-147">Na zavihku **Project Service** lahko nastavite tudi posamično ciljno uporabo za vir.</span><span class="sxs-lookup"><span data-stu-id="a7d47-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="a7d47-148">Izračun uporabe nato uporabi to ciljno uporabo za oceno cilja vira namesto cilja privzete vloge vira.</span><span class="sxs-lookup"><span data-stu-id="a7d47-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="a7d47-149">Uporaba se za posamezen vir prikaže samo, če je vir odobril čas, ki se zaračuna, v obdobju, ki je prikazan v mreži.</span><span class="sxs-lookup"><span data-stu-id="a7d47-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="a7d47-150">razpoložljivosti vira</span><span class="sxs-lookup"><span data-stu-id="a7d47-150">Resource availability</span></span>

<span data-ttu-id="a7d47-151">Upravitelji virov morajo imeti možnost ogleda razpoložljivosti virov in posodobitve rezervacij.</span><span class="sxs-lookup"><span data-stu-id="a7d47-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="a7d47-152">V nekaterih primerih ni uradnega povpraševanja (zahteve za vir), vendar se mora upravitelj virov odzvati na nenačrtovano povpraševanje, ki prihaja prek različnih kanalov, na primer elektronske pošte, telefonskih klicev ali neposrednih sporočil.</span><span class="sxs-lookup"><span data-stu-id="a7d47-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="a7d47-153">Upravitelji virov uporabljajo ploščo razporeda za posodabljanje virov in rezervacij.</span><span class="sxs-lookup"><span data-stu-id="a7d47-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="a7d47-154">Delovni čas virov se uporablja kot osnova za izračun razpoložljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="a7d47-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="a7d47-155">Rezervacije virov porabijo del zmogljivosti virov.</span><span class="sxs-lookup"><span data-stu-id="a7d47-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="a7d47-156">Na plošči razporeda so za prikaz rezervacij, razpoložljivosti, prezasedenosti in stanja rezervacij uporabljene različne barve in senčenje.</span><span class="sxs-lookup"><span data-stu-id="a7d47-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="a7d47-157">Z izbiro ustrezne nastavitve v nastavitvah plošče razporeda lahko prikažete tudi legendo.</span><span class="sxs-lookup"><span data-stu-id="a7d47-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="a7d47-158">Če je ob posameznem viru, ki ga je mogoče rezervirati, na plošči razporeda prikazana puščica v desno, lahko vir razširite in s tem prikažete podrobnosti o delu, za katerega je vir rezerviran.</span><span class="sxs-lookup"><span data-stu-id="a7d47-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="a7d47-159">Ker Dynamics 365 Project Operations uporablja mehanizem Universal Resource Scheduling, si lahko tudi vi ogledate podrobnosti o rezervacijah virov za projekte, delovne naloge in vse druge entitete, na katere ste razširili razporejanje, ob predpostavki, da imate nameščeno aplikacijo Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="a7d47-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="a7d47-160">Če si želite ogledati podrobnosti o posameznem viru, ga kliknite z desno tipko miške, da odprete kartico vira.</span><span class="sxs-lookup"><span data-stu-id="a7d47-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

