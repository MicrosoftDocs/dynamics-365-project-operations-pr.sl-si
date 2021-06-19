---
title: Krmarjenje po uporabniškem vmesniku
description: Ta tema vsebuje informacije o vodenju projektov v postopkih aplikacije Dynamics 365 Project.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 715a8bdb9a1f38f71b4c42f5307ed4a5c7170ef6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014271"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="69245-103">Krmarjenje po uporabniškem vmesniku</span><span class="sxs-lookup"><span data-stu-id="69245-103">Navigating the user interface</span></span>

<span data-ttu-id="69245-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="69245-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="69245-105">Pregled</span><span class="sxs-lookup"><span data-stu-id="69245-105">Overview</span></span>

<span data-ttu-id="69245-106">Glavni obrazec projekta je razdeljen na več zavihkov.</span><span class="sxs-lookup"><span data-stu-id="69245-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="69245-107">Vsak zavihek predstavlja drugačno raven podrobnosti v projektu.</span><span class="sxs-lookup"><span data-stu-id="69245-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="69245-108">**Povzetek**: ponuja opis projekta ter združuje načrtovano in dejansko učinkovitost projekta.</span><span class="sxs-lookup"><span data-stu-id="69245-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Zavihek »Povzetek« in polja](media/navigation7.png)

- <span data-ttu-id="69245-110">**Opravila**: zagotavlja podrobnosti o strukturirani členitvi dela, ki jo predstavljajo pogled mreže, pogled plošče in Ganttov grafikon.</span><span class="sxs-lookup"><span data-stu-id="69245-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Zavihek »Opravilo« in polja](media/navigation8.png)

- <span data-ttu-id="69245-112">**Ekipa**: vsebuje podrobnosti o udeležencih v projektu.</span><span class="sxs-lookup"><span data-stu-id="69245-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="69245-113">V tem pogledu so povzete tudi dodeljene naloge vsakega člana ekipe.</span><span class="sxs-lookup"><span data-stu-id="69245-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Zavihek »Ekipa« in polja](media/navigation9.png)

- <span data-ttu-id="69245-115">**Dodelitve virov**: omogočajo časovno razporejen pogled nalog za vsak vir v projektu.</span><span class="sxs-lookup"><span data-stu-id="69245-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Zavihek »Dodelitve virov« in polja](media/navigation10.png)

- <span data-ttu-id="69245-117">**Uskladitev virov**: omogoča časovno razporejen prikaz razlik med dodelitvami vsakega imenovanega vira in njihovimi rezervacijami.</span><span class="sxs-lookup"><span data-stu-id="69245-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Zavihek »Uskladitev virov« in polja](media/navigation11.png)

- <span data-ttu-id="69245-119">**Ocene**: omogoča časovno razporejen prikaz stroškov in ocen prodaje projekta.</span><span class="sxs-lookup"><span data-stu-id="69245-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Zavihek »Ocene« in polja](media/navigation12.png)

- <span data-ttu-id="69245-121">**Sledenje**: omogoča pogled, ki prikazuje napredek pri opravilih v strukturirani členitvi dela glede za naloge, stroške in prodajo.</span><span class="sxs-lookup"><span data-stu-id="69245-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Zavihek »Sledenje« in polja](media/navigation13.png)

- <span data-ttu-id="69245-123">**Prodaja**: ponuja globoke povezave do ponudb in pogodb, povezanih s projektom.</span><span class="sxs-lookup"><span data-stu-id="69245-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="69245-124">**Ocena stroškov**: ponuja mrežo, ki opredeljuje stroške projekta na podlagi kategorij organizacijskih stroškov.</span><span class="sxs-lookup"><span data-stu-id="69245-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Zavihek »Ocena stroškov« in polja](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="69245-126">Kontrolniki mreže</span><span class="sxs-lookup"><span data-stu-id="69245-126">Grid controls</span></span>

<span data-ttu-id="69245-127">Sledi kratek pregled tipičnih kontrolnikov, ki jih najdemo na različnih zavihkih za načrtovanje projektov.</span><span class="sxs-lookup"><span data-stu-id="69245-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="69245-128">Osveži</span><span class="sxs-lookup"><span data-stu-id="69245-128">Refresh</span></span>

<span data-ttu-id="69245-129">**Osveži**: pridobi najnovejše podatke s strežnika, če je prišlo do sprememb po nalaganju mreže.</span><span class="sxs-lookup"><span data-stu-id="69245-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Gumb »Osveži«](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="69245-131">Združi po</span><span class="sxs-lookup"><span data-stu-id="69245-131">Group by</span></span>

<span data-ttu-id="69245-132">**Razvrsti po**: posodobi združevanje vrstic v mreži tako, da odraža vire, vloge ali kategorije glede na potrebe uporabnika.</span><span class="sxs-lookup"><span data-stu-id="69245-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Gumb »Združi po«](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="69245-134">Nazaj/naprej</span><span class="sxs-lookup"><span data-stu-id="69245-134">Previous/Next</span></span>

<span data-ttu-id="69245-135">**Nazaj**/**naprej** : posodobite vidna časovna obdobja na časovno razporejenih mrežah.</span><span class="sxs-lookup"><span data-stu-id="69245-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Gumba »Nazaj« in »Naprej«](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="69245-137">Časovno merilo</span><span class="sxs-lookup"><span data-stu-id="69245-137">Timescale</span></span>

<span data-ttu-id="69245-138">**Časovno merilo** : spremenite združevanje časovno razporejenih podatkov med dnevi, tedni, meseci in leti.</span><span class="sxs-lookup"><span data-stu-id="69245-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Gumb »Časovno merilo«](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="69245-140">Razširi</span><span class="sxs-lookup"><span data-stu-id="69245-140">Expand</span></span>

<span data-ttu-id="69245-141">**Razširi**: upodobi vidno mrežo na celozaslonski način in tako omogoči prikaz več dodatnih vlog.</span><span class="sxs-lookup"><span data-stu-id="69245-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Gumb »Razširi«](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="69245-143">Časovno razporedi po</span><span class="sxs-lookup"><span data-stu-id="69245-143">Time-phase by</span></span>

<span data-ttu-id="69245-144">**Časovno razporedi po**: posodobite združevanje vrstic v mrežo tako, da odraža ocene stroškov za ocene prodaje.</span><span class="sxs-lookup"><span data-stu-id="69245-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="69245-145">Ta kontrolnik velja tudi za ocenjevalni skript in mrežo za sledenje.</span><span class="sxs-lookup"><span data-stu-id="69245-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Gumb »Časovno razporedi po«](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="69245-147">Dodaj stolpec</span><span class="sxs-lookup"><span data-stu-id="69245-147">Add column</span></span>

<span data-ttu-id="69245-148">**Dodaj stolpec**: uporabniku omogoča, da določi vidne stolpce v mreži.</span><span class="sxs-lookup"><span data-stu-id="69245-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="69245-149">V mreže na obrazcu **Načrtovanje projekta** lahko dodate samo vnaprej pripravljene stolpce.</span><span class="sxs-lookup"><span data-stu-id="69245-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Gumb »Dodaj stolpec«](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]