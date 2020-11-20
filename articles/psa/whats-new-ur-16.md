---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 16, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 16.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 2c93d34b61001b7755d426539ac384641a7bc9da
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121598"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="d83a4-103">Izdaja posodobitve 16 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="d83a4-103">Project Service Automation Update Release 16, V3</span></span>

<span data-ttu-id="d83a4-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d83a4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d83a4-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="d83a4-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="d83a4-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d83a4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d83a4-107">Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="d83a4-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="d83a4-108">Za več informacij glejte [Namestitev, posodobitev prednostne rešitve](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="d83a4-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="d83a4-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za PSA V3, izdaja posodobitve 16.</span><span class="sxs-lookup"><span data-stu-id="d83a4-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="d83a4-110">Ta različica ima številko graditve V3.10.6.34 in je splošno na voljo s samostojno posodobitvijo v januarju 2020.</span><span class="sxs-lookup"><span data-stu-id="d83a4-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="d83a4-111">Izdaja posodobitve 16</span><span class="sxs-lookup"><span data-stu-id="d83a4-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d83a4-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="d83a4-112">Bug fixes</span></span>

-   <span data-ttu-id="d83a4-113">Čas in strošek</span><span class="sxs-lookup"><span data-stu-id="d83a4-113">Time and Expense</span></span>

    -   <span data-ttu-id="d83a4-114">Popravljeno: Uporabniki, ki poskušajo predložiti izbrisane vnose za čas in stroške za odobritve, bodo zdaj prejeli ustrezna sporočila o napaki.</span><span class="sxs-lookup"><span data-stu-id="d83a4-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="d83a4-115">Vodenje projektov</span><span class="sxs-lookup"><span data-stu-id="d83a4-115">Project Management</span></span>

    -   <span data-ttu-id="d83a4-116">Popravljeno: Enote vira, ki so v predlogah določene za člane skupine, se spoštujejo, predloge pa se uporabijo za nov projekt.</span><span class="sxs-lookup"><span data-stu-id="d83a4-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="d83a4-117">Popravljeno: Izboljšano upravljanje ponovne dodelitve lastništva zapisov.</span><span class="sxs-lookup"><span data-stu-id="d83a4-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="d83a4-118">Popravljeno: Projektov, ki so v postopku kopiranja, ne bo dovoljeno kopirati, dokler se ne končajo vse operacije kopiranja.</span><span class="sxs-lookup"><span data-stu-id="d83a4-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="d83a4-119">Upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="d83a4-119">Resource Management</span></span>

    -   <span data-ttu-id="d83a4-120">Popravljeno: Podaljšanje rezervacij zdaj pravilno upravlja s kratkimi obdobji in za podaljšane rezervacije ne ustvarja več nič ur.</span><span class="sxs-lookup"><span data-stu-id="d83a4-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="d83a4-121">Popravljeno: Pogled usklajevanja je zdaj ustvarjen, ko je časovni pas projekta +5.30 GMT in čas uporabnika drugačen.</span><span class="sxs-lookup"><span data-stu-id="d83a4-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="d83a4-122">Sales</span><span class="sxs-lookup"><span data-stu-id="d83a4-122">Sales</span></span>

    -   <span data-ttu-id="d83a4-123">Popravljeno: Ko je projekt, preslikan na podrobnosti pogodbe, odstranjen in nov projekt preslikan, dejanski zapisi o novem projektu niso bili ponovno ocenjeni na podlagi pravil za obračunavanje in določanje cen, določenih v podrobnostih pogodbe.</span><span class="sxs-lookup"><span data-stu-id="d83a4-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="d83a4-124">To je bilo v tej izdaji popravljeno.</span><span class="sxs-lookup"><span data-stu-id="d83a4-124">This has been fixed in this release.</span></span> <span data-ttu-id="d83a4-125">Cene in dejanski zapisi glede na novo preslikanega projekta bodo razveljavljeni in ponovno pravilno ustvarjeni na podlagi pravil za določanje cen in obračunavanje iz podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="d83a4-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="d83a4-126">Tudi dejanski zapisi nepreslikanega projekta bodo posledično ponovno ovrednoteni in na novo ustvarjeni.</span><span class="sxs-lookup"><span data-stu-id="d83a4-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="d83a4-127">Popravljeno: V polje **Znesek** vrstice ocene je bila dodana dodatna potrditev za zagotovitev, da se ničelne vrednosti ne ohranijo.</span><span class="sxs-lookup"><span data-stu-id="d83a4-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="d83a4-128">Popravljeno: Ko so bile posodobljene dejanske vrednosti o projektu, je bil v glavni obrazec projekta dodan gumb za osvežitev, ki uporabnikom omogoča ponovno sinhronizacijo dejanskih vrednosti.</span><span class="sxs-lookup"><span data-stu-id="d83a4-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="d83a4-129">Popravljeno: Ko uporabniki nadgradijo z 2.X na 3.X, bodo dovoljeni projekti z vrednostjo NULL za ime projekta.</span><span class="sxs-lookup"><span data-stu-id="d83a4-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

