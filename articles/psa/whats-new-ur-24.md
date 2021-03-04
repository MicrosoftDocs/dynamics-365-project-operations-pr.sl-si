---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 24, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 24.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146728"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="1f9d8-103">Izdaja posodobitve 24 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="1f9d8-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1f9d8-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1f9d8-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1f9d8-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1f9d8-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1f9d8-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1f9d8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1f9d8-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 24.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="1f9d8-110">Ta različica ima številko graditve V 3.10.42.43 in je splošno na voljo s samostojno posodobitvijo od oktobra 2020.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="1f9d8-111">Izdaja posodobitve 24</span><span class="sxs-lookup"><span data-stu-id="1f9d8-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1f9d8-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="1f9d8-112">Bug fixes</span></span>

<span data-ttu-id="1f9d8-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1f9d8-113">**Sales**</span></span>

<span data-ttu-id="1f9d8-114">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="1f9d8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="1f9d8-115">Težava pri nastavljanju privzetega cenika izdelkov.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="1f9d8-116">Pridobivanje ponudb je počasno zaradi vdelanega cenika in kopij zapisov o cenah vlog.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="1f9d8-117">**Projektna pogodba/središče za prodajo** > **Vrstična postavka izdelka/količina vrstice naročila** se samodejno zaokroži na najbližje celo število.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="1f9d8-118">Povišanje sistemskih pravic pri branju cenikov.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="1f9d8-119">Kopiranje polj naslova stranke **address1_freighttermscode** in **address1_shippingmethodcode** v ponudbo/naročilo.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="1f9d8-120">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="1f9d8-120">**Time and Expense**</span></span>

<span data-ttu-id="1f9d8-121">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="1f9d8-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="1f9d8-122">**Mreža časovnih vnosov** ne podpira vedenja časa **Samo datum**.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="1f9d8-123">**Časovni vnos** se ne osvežuje samodejno.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="1f9d8-124">Potrebno je ročno osveževanje.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-124">A manual refresh is required.</span></span>
- <span data-ttu-id="1f9d8-125">Časovnih vnosov iz dodelitve ni mogoče uvoziti, ko je v dodelitvah vira premor (0 ur).</span><span class="sxs-lookup"><span data-stu-id="1f9d8-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="1f9d8-126">Nastavitev začetka, da bo enak kot **msdyn_date**, pri ustvarjanju časovnega vnosa.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="1f9d8-127">Ponovno omogočanje množičnega urejanja časovnih vnosov.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="1f9d8-128">**Upravljanje virov**</span><span class="sxs-lookup"><span data-stu-id="1f9d8-128">**Resource Management**</span></span>

<span data-ttu-id="1f9d8-129">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="1f9d8-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="1f9d8-130">Poskus posodobitve stanja dnevne rezervacije brez zahteve povzroči izjemo sklica »null«.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="1f9d8-131">Pri nalaganju možnosti **Pogled za usklajevanje** se pojavi napaka.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="1f9d8-132">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="1f9d8-132">**Project Management**</span></span>

<span data-ttu-id="1f9d8-133">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="1f9d8-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="1f9d8-134">Pri preklopu z možnosti **Ročno** na **Samodejno** v možnosti **Razpored projektov** se samodejno shranjevanje ne dokonča.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="1f9d8-135">Stroški ne bi smeli biti vračunani v odstopanje v razdelku **Mreža za sledenje projektom**.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="1f9d8-136">Nedosledno vedenje stolpcev **Oznaka ocene** med obremenitvijo v primerjavi s spremembo vrste **Časovni razpored**.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="1f9d8-137">Dejanski stroški projekta morda ne odražajo skupnega zneska v razdelku **Dejanske vrednosti**.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="1f9d8-138">**Predvideni končni datum** na zavihku **Povzetek** se ne ujema z možnostjo **Urnik SČD**.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="1f9d8-139">Možnost **Posodobi dejanske ure** pri primikanju ne deluje pravilno.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="1f9d8-140">Vodja projekta zunaj korenske **poslovne enote** ne more ustvariti projekta.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="1f9d8-141">Spremembe opravila ali kategorije v razdelku **Ocene stroškov** se ne ohranijo.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="1f9d8-142">**Kopija pogodbe** kopira razporede računov in stanje izvajanja.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="1f9d8-143">Gumb **Osveži dejanske podatke** napačno izračuna opravila povzetka.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="1f9d8-144">Dodatek za Microsoft Project: popravek napake s sklicem »null«, če ima kateri koli član ekipe prazno enoto vira.</span><span class="sxs-lookup"><span data-stu-id="1f9d8-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

