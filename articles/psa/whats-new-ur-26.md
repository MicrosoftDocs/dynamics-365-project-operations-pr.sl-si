---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 26, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 26.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948844"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="d07ae-103">Izdaja posodobitve 26 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="d07ae-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d07ae-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d07ae-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d07ae-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="d07ae-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d07ae-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d07ae-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d07ae-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="d07ae-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d07ae-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d07ae-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d07ae-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 26, V3.</span><span class="sxs-lookup"><span data-stu-id="d07ae-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="d07ae-110">Ta različica ima številko izdelave V3.10.44.59 in je splošno na voljo s samoposodobitvijo decembra 2020.</span><span class="sxs-lookup"><span data-stu-id="d07ae-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="d07ae-111">Izdaja posodobitve 26</span><span class="sxs-lookup"><span data-stu-id="d07ae-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d07ae-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="d07ae-112">Bug fixes</span></span>

<span data-ttu-id="d07ae-113">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="d07ae-113">**Time and Expense**</span></span>

<span data-ttu-id="d07ae-114">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="d07ae-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="d07ae-115">Uporabniki lahko spremenijo opravilo v časovnem vnosu, ki je bil odobren/poslan.</span><span class="sxs-lookup"><span data-stu-id="d07ae-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="d07ae-116">Pri shranjevanju časovnega vnosa se pojavi napaka »Object Reference Not Set«.</span><span class="sxs-lookup"><span data-stu-id="d07ae-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="d07ae-117">Uvoz časovnega vnosa iz dodelitev virov ustvari časovne vnose z napačnimi vrednostmi DateTime.</span><span class="sxs-lookup"><span data-stu-id="d07ae-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="d07ae-118">Ko sta nameščeni aplikaciji Project Service Automation in Field Service, se gumb **Novo** dvakrat prikaže v ukazni vrstici za časovne vnose v aplikaciji Field Service.</span><span class="sxs-lookup"><span data-stu-id="d07ae-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="d07ae-119">Posodabljanje celic **Dovoli enoto** in **Skupina enot** zdaj ponovno deluje v mreži **Ocene stroškov**.</span><span class="sxs-lookup"><span data-stu-id="d07ae-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="d07ae-120">Oblika **Posodobi urejanje časovnega vnosa** vključuje možnost **Časovnica**.</span><span class="sxs-lookup"><span data-stu-id="d07ae-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="d07ae-121">Odobritev časa za neprojektne časovne vnose blokira sistem pri iskanju vloge odobritelja projekta.</span><span class="sxs-lookup"><span data-stu-id="d07ae-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="d07ae-122">**Upravljanje virov**</span><span class="sxs-lookup"><span data-stu-id="d07ae-122">**Resource Management**</span></span>

<span data-ttu-id="d07ae-123">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="d07ae-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="d07ae-124">V vtičnik **PostProjectCreate** je dodano preverjanje za obstoj primarne zahteve, preden jo ustvarite.</span><span class="sxs-lookup"><span data-stu-id="d07ae-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="d07ae-125">Obrazec za hitro ustvarjanje **Član projektne skupine** vrne izjemo s sklicem »null«, če so polja odstranjena iz obrazca.</span><span class="sxs-lookup"><span data-stu-id="d07ae-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="d07ae-126">Ustvarjanje zahtev za 12 ur v celotnem letu ne bo uspelo.</span><span class="sxs-lookup"><span data-stu-id="d07ae-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="d07ae-127">Izboljšano o napaki za izjemo s sklicem »null« pri ustvarjanju zahteve za vir.</span><span class="sxs-lookup"><span data-stu-id="d07ae-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="d07ae-128">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="d07ae-128">**Project Management**</span></span>

<span data-ttu-id="d07ae-129">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="d07ae-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="d07ae-130">Izboljšana potrditev veljavnosti za obravnavo izjeme s sklicem »null«, ustvarjene v vtičniku **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="d07ae-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="d07ae-131">Projekti, ki jih je objavil namizni vtičnik Microsoft Project, izbrišejo nedodeljene naloge.</span><span class="sxs-lookup"><span data-stu-id="d07ae-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="d07ae-132">Dodano je novo preverjanje veljavnosti, ko je sklic projektnega opravila neveljaven zaradi izjeme s sklicem »null« v vtičniku **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="d07ae-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="d07ae-133">Mreža člana ekipe ne prikazuje posameznih nalog v zapisu člana ekipe.</span><span class="sxs-lookup"><span data-stu-id="d07ae-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="d07ae-134">Dodano je novo preverjanje veljavnosti in sporočila o napakah zaradi izjeme s sklicem »null« v vtičniku **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="d07ae-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="d07ae-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d07ae-135">**Sales**</span></span>

<span data-ttu-id="d07ae-136">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="d07ae-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="d07ae-137">Pri izbiri podrobnosti ponudbe ali pogodbe, ki temelji na projektu, bi moral biti gumb **Predlog** viden samo pri izbiri podrobnosti, ki temeljijo na izdelku in so povezane z obstoječim izdelkom.</span><span class="sxs-lookup"><span data-stu-id="d07ae-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="d07ae-138">Razdelite privilegij **Create_Product** iz privilegija **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="d07ae-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="d07ae-139">Če izbrišete podrobnosti računa, bo prišlo do napake pri sklicu »null« za **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="d07ae-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]