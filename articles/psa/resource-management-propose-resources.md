---
title: Predlaganje projektnih virov
description: Ta tema vsebuje informacije o predlaganju projektnih virov.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 2003f6f06912b0c47eb942aae17e509b00e19487
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283028"
---
# <a name="propose-project-resources"></a><span data-ttu-id="692d4-103">Predlaganje projektnih virov</span><span class="sxs-lookup"><span data-stu-id="692d4-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="692d4-104">Upravitelji virov lahko vodji projekta predlagajo vir prek zahteve za vir.</span><span class="sxs-lookup"><span data-stu-id="692d4-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="692d4-105">V mreži zahtev ali sami zahtevi izberite **Poišči vire**.</span><span class="sxs-lookup"><span data-stu-id="692d4-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="692d4-106">Na strani **Pomočnik za razporejanje** izberite vir in nato v polju **Stanje rezervacije** v podoknu **Ustvari rezervacijo vira** izberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="692d4-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Izbran predlagani vir](media/Resource-Management-image62.png)

<span data-ttu-id="692d4-108">Pojavijo se naslednje posodobitve stanja:</span><span class="sxs-lookup"><span data-stu-id="692d4-108">The following status updates occur:</span></span>

- <span data-ttu-id="692d4-109">Na strani **Pomočnik za razporejanje** se kazalniki stanja posodobijo in sporočajo, da je rezervacija šele predlagana in ne potrjena.</span><span class="sxs-lookup"><span data-stu-id="692d4-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Kazalniki stanja za predlagano rezervacijo na strani pomočnika za razporejanje](media/Resource-Management-image63.png)

- <span data-ttu-id="692d4-111">V zahtevi za vir se stanje spremeni v **Potreben pregled**.</span><span class="sxs-lookup"><span data-stu-id="692d4-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Sprememba stanja zahteve za vir v »Potreben pregled«](media/Resource-Management-image64.png)

- <span data-ttu-id="692d4-113">Na zavihku **Ekipa** izbranega projekta se vrednost splošnega člana ekipe **Stanje zahteve** spremeni v **Potreben pregled**.</span><span class="sxs-lookup"><span data-stu-id="692d4-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Sprememba stanja zahteve splošnega člana ekipe v »Potreben pregled« na zavihku »Ekipa«](media/Resource-Management-image48.png)

<span data-ttu-id="692d4-115">Vodja projekta lahko predlog sprejme ali zavrne.</span><span class="sxs-lookup"><span data-stu-id="692d4-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="692d4-116">Upravitelji virov lahko za obdelavo zahtev za vire uporabijo katerega koli od spodaj navedenih pristopov:</span><span class="sxs-lookup"><span data-stu-id="692d4-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="692d4-117">Predlagajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil zahtevane ure.</span><span class="sxs-lookup"><span data-stu-id="692d4-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="692d4-118">Predlagane ure se nato razdelijo med več virov, ki lahko opravijo zahtevane ure.</span><span class="sxs-lookup"><span data-stu-id="692d4-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="692d4-119">V tem primeru se ure ne morejo prekrivati.</span><span class="sxs-lookup"><span data-stu-id="692d4-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="692d4-120">Predlagajo manj virov, kot jih zahtevajo.</span><span class="sxs-lookup"><span data-stu-id="692d4-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="692d4-121">V tem primeru je predlagana zmogljivost vira manjša od zahtevanih ur, ki jih je določila oseba, ki je podala zahtevo.</span><span class="sxs-lookup"><span data-stu-id="692d4-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="692d4-122">Ko torej oseba, ki je podala zahtevo, sprejme predlagane vire, se ustvari neizpolnjena zahteva za vir, ki predstavlja preostalo povpraševanje.</span><span class="sxs-lookup"><span data-stu-id="692d4-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="692d4-123">Rezervirajo več virov, da zadostijo povpraševanju, če ni vira, ki bi lahko sam opravil delo.</span><span class="sxs-lookup"><span data-stu-id="692d4-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="692d4-124">Rezervirajo manj virov, kot jih zahtevajo.</span><span class="sxs-lookup"><span data-stu-id="692d4-124">Book fewer resources than are required.</span></span> <span data-ttu-id="692d4-125">V tem primeru bo število rezerviranih ur manjše od zahtevanih ur.</span><span class="sxs-lookup"><span data-stu-id="692d4-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="692d4-126">Sistem vas vodi k predlaganju virov namesto rezervacij, da lahko oseba, ki je podala zahtevo, preveri in spremlja preostalo povpraševanje.</span><span class="sxs-lookup"><span data-stu-id="692d4-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="692d4-127">Zaračunana uporaba</span><span class="sxs-lookup"><span data-stu-id="692d4-127">Billable utilization</span></span>

<span data-ttu-id="692d4-128">Viri lahko imajo ciljno zaračunano uporabo.</span><span class="sxs-lookup"><span data-stu-id="692d4-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="692d4-129">Ta ciljna uporaba je opredeljena kot atribut privzete vloge vira ali nastavljena v zapisu posameznega vira, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="692d4-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="692d4-130">Izračuni uporabe temeljijo na dejanskih urah, ki so jih viri poročali na podlagi odobrenih časovnih vnosov.</span><span class="sxs-lookup"><span data-stu-id="692d4-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="692d4-131">Za izračun uporabe se uporabljajo naslednje enačbe:</span><span class="sxs-lookup"><span data-stu-id="692d4-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="692d4-132">Zaračunana uporaba = dejanske zaračunane ure ÷ zmogljivost vira</span><span class="sxs-lookup"><span data-stu-id="692d4-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="692d4-133">Nezaračunana uporaba = dejanski čas z ID-jem vrste obračunavanja = se ne zaračuna, brezplačno ali ni na voljo ÷ zmogljivost vira</span><span class="sxs-lookup"><span data-stu-id="692d4-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="692d4-134">Za interno uporabo = dejanski čas brez prodajne pogodbe ÷ zmogljivost vira</span><span class="sxs-lookup"><span data-stu-id="692d4-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="692d4-135">Zmogljivost vira = delovni čas vira – odsotnost – prosti dnevi</span><span class="sxs-lookup"><span data-stu-id="692d4-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="692d4-136">Pogled **Uporaba vira** lahko najdete v podoknu **Viri**.</span><span class="sxs-lookup"><span data-stu-id="692d4-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Pogled uporabe virov](media/Resource-Management-image65.png)

<span data-ttu-id="692d4-138">Vsaka celica v mreži predstavlja delež zaračunane uporabe vira v določenem obdobju, na primer dnevu, tednu ali mesecu.</span><span class="sxs-lookup"><span data-stu-id="692d4-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="692d4-139">Za obarvanje celic se uporabljajo naslednje enačbe:</span><span class="sxs-lookup"><span data-stu-id="692d4-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="692d4-140">**Zelena:** zaračunana uporaba \>= ciljna uporaba za vir</span><span class="sxs-lookup"><span data-stu-id="692d4-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="692d4-141">**Rumena:** ciljna uporaba – 20 \<= zaračunana uporaba \< ciljna uporaba</span><span class="sxs-lookup"><span data-stu-id="692d4-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="692d4-142">**Rdeča:** zaračunana uporaba \< ciljna uporaba – 20</span><span class="sxs-lookup"><span data-stu-id="692d4-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="692d4-143">Ker pogled **Uporaba vira** temelji na plošči razporeda, lahko rezultate filtrirate z možnostmi filtriranja na plošči razporeda.</span><span class="sxs-lookup"><span data-stu-id="692d4-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="692d4-144">Zaradi mreže morate nastaviti ciljno uporabo za vlogo ali posamezni vir.</span><span class="sxs-lookup"><span data-stu-id="692d4-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="692d4-145">To nastavite v možnosti **Viri** \> **Vloge virov**.</span><span class="sxs-lookup"><span data-stu-id="692d4-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="692d4-146">Poleg tega morate vsakemu viru, ki ga je mogoče rezervirati, dodati tudi privzeto vlogo.</span><span class="sxs-lookup"><span data-stu-id="692d4-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="692d4-147">Odprite možnost **Viri** \> **Viri**.</span><span class="sxs-lookup"><span data-stu-id="692d4-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="692d4-148">Na zavihku **Project Service** preverite, ali je vloga vira določena in ali je polje **Je privzeto** nastavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="692d4-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="692d4-149">Kjer je vrednost **Je privzeto = Ne**, lahko dodate dodatne vloge.</span><span class="sxs-lookup"><span data-stu-id="692d4-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="692d4-150">Vloga, pri kateri je vrednost **Je privzeto = Da**, se uporablja za oceno uporabe vira v primerjavi s ciljem za to vlogo.</span><span class="sxs-lookup"><span data-stu-id="692d4-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Nastavitev privzete vloge](media/Resource-Management-image67.png)

<span data-ttu-id="692d4-152">Na zavihku **Project Service** lahko nastavite tudi posamično ciljno uporabo za vir.</span><span class="sxs-lookup"><span data-stu-id="692d4-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="692d4-153">Izračun uporabe nato uporabi to ciljno uporabo za oceno cilja vira namesto cilja privzete vloge vira.</span><span class="sxs-lookup"><span data-stu-id="692d4-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="692d4-154">Uporaba se za posamezen vir prikaže samo, če je vir odobril čas, ki se zaračuna, v obdobju, ki je prikazan v mreži.</span><span class="sxs-lookup"><span data-stu-id="692d4-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="692d4-155">razpoložljivosti vira</span><span class="sxs-lookup"><span data-stu-id="692d4-155">Resource availability</span></span>

<span data-ttu-id="692d4-156">Upravitelji virov morajo imeti možnost ogleda razpoložljivosti virov in posodobitve rezervacij.</span><span class="sxs-lookup"><span data-stu-id="692d4-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="692d4-157">V nekaterih primerih ni uradnega povpraševanja (zahteve za vir), vendar se mora upravitelj virov odzvati na nenačrtovano povpraševanje, ki prihaja prek različnih kanalov, na primer elektronske pošte, telefonskih klicev ali neposrednih sporočil.</span><span class="sxs-lookup"><span data-stu-id="692d4-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="692d4-158">Upravitelji virov uporabljajo ploščo razporeda za posodabljanje virov in rezervacij.</span><span class="sxs-lookup"><span data-stu-id="692d4-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="692d4-159">Delovni čas virov se uporablja kot osnova za izračun razpoložljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="692d4-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="692d4-160">Rezervacije virov porabijo del zmogljivosti virov.</span><span class="sxs-lookup"><span data-stu-id="692d4-160">Resource bookings consume the capacity of the resources.</span></span>

![Plošča razporeda](media/Resource-Management-image68.png)

<span data-ttu-id="692d4-162">Na plošči razporeda so za prikaz rezervacij, razpoložljivosti, prezasedenosti in stanja rezervacij uporabljene različne barve in senčenje.</span><span class="sxs-lookup"><span data-stu-id="692d4-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="692d4-163">Z izbiro ustrezne nastavitve v nastavitvah plošče razporeda lahko prikažete tudi legendo.</span><span class="sxs-lookup"><span data-stu-id="692d4-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="692d4-164">Če je ob posameznem viru, ki ga je mogoče rezervirati, na plošči razporeda prikazana puščica v desno, lahko vir razširite in s tem prikažete podrobnosti o delu, za katerega je vir rezerviran.</span><span class="sxs-lookup"><span data-stu-id="692d4-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Razširitev vira, ki ga je mogoče rezervirati, na plošči razporeda](media/Resource-Management-image69.png)

<span data-ttu-id="692d4-166">Ker rešitev Dynamics 365 Project Service Automation uporablja mehanizem Universal Resource Scheduling, si lahko tudi vi ogledate podrobnosti o rezervacijah virov za projekte, delovne naloge in vse druge entitete, na katere ste razširili razporejanje, ob predpostavki, da imate nameščeno aplikacijo Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="692d4-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Podrobnosti o rezervacijah virov za projekte in delovne naloge](media/Resource-Management-image70.png)

<span data-ttu-id="692d4-168">Če si želite ogledati podrobnosti o posameznem viru, ga kliknite z desno tipko miške, da odprete kartico vira.</span><span class="sxs-lookup"><span data-stu-id="692d4-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Kartica vira](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]