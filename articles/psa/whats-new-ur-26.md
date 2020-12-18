---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643283"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="bf453-102">Izdaja posodobitve 26 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="bf453-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="bf453-103">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bf453-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bf453-104">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="bf453-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bf453-105">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="bf453-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bf453-106">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="bf453-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="bf453-107">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="bf453-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bf453-108">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 26, V3.</span><span class="sxs-lookup"><span data-stu-id="bf453-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="bf453-109">Ta različica ima številko izdelave V3.10.44.59 in je splošno na voljo s samoposodobitvijo decembra 2020.</span><span class="sxs-lookup"><span data-stu-id="bf453-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="bf453-110">Izdaja posodobitve 26</span><span class="sxs-lookup"><span data-stu-id="bf453-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="bf453-111">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="bf453-111">Bug fixes</span></span>

<span data-ttu-id="bf453-112">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="bf453-112">**Time and Expense**</span></span>

<span data-ttu-id="bf453-113">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="bf453-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="bf453-114">Uporabniki lahko spremenijo opravilo v časovnem vnosu, ki je bil odobren/poslan.</span><span class="sxs-lookup"><span data-stu-id="bf453-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="bf453-115">Pri shranjevanju časovnega vnosa se pojavi napaka »Object Reference Not Set«.</span><span class="sxs-lookup"><span data-stu-id="bf453-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="bf453-116">Uvoz časovnega vnosa iz dodelitev virov ustvari časovne vnose z napačnimi vrednostmi DateTime.</span><span class="sxs-lookup"><span data-stu-id="bf453-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="bf453-117">Ko sta nameščeni aplikaciji Project Service Automation in Field Service, se gumb **Novo** dvakrat prikaže v ukazni vrstici za časovne vnose v aplikaciji Field Service.</span><span class="sxs-lookup"><span data-stu-id="bf453-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="bf453-118">Posodabljanje celic **Dovoli enoto** in **Skupina enot** zdaj ponovno deluje v mreži **Ocene stroškov**.</span><span class="sxs-lookup"><span data-stu-id="bf453-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="bf453-119">Oblika **Posodobi urejanje časovnega vnosa** vključuje možnost **Časovnica**.</span><span class="sxs-lookup"><span data-stu-id="bf453-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="bf453-120">Odobritev časa za neprojektne časovne vnose blokira sistem pri iskanju vloge odobritelja projekta.</span><span class="sxs-lookup"><span data-stu-id="bf453-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="bf453-121">**Upravljanje virov**</span><span class="sxs-lookup"><span data-stu-id="bf453-121">**Resource Management**</span></span>

<span data-ttu-id="bf453-122">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="bf453-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="bf453-123">V vtičnik **PostProjectCreate** je dodano preverjanje za obstoj primarne zahteve, preden jo ustvarite.</span><span class="sxs-lookup"><span data-stu-id="bf453-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="bf453-124">Obrazec za hitro ustvarjanje **Član projektne skupine** vrne izjemo s sklicem »null«, če so polja odstranjena iz obrazca.</span><span class="sxs-lookup"><span data-stu-id="bf453-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="bf453-125">Ustvarjanje zahtev za 12 ur v celotnem letu ne bo uspelo.</span><span class="sxs-lookup"><span data-stu-id="bf453-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="bf453-126">Izboljšano o napaki za izjemo s sklicem »null« pri ustvarjanju zahteve za vir.</span><span class="sxs-lookup"><span data-stu-id="bf453-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="bf453-127">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="bf453-127">**Project Management**</span></span>

<span data-ttu-id="bf453-128">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="bf453-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="bf453-129">Izboljšana potrditev veljavnosti za obravnavo izjeme s sklicem »null«, ustvarjene v vtičniku **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="bf453-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="bf453-130">Projekti, ki jih je objavil namizni vtičnik Microsoft Project, izbrišejo nedodeljene naloge.</span><span class="sxs-lookup"><span data-stu-id="bf453-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="bf453-131">Dodano je novo preverjanje veljavnosti, ko je sklic projektnega opravila neveljaven zaradi izjeme s sklicem »null« v vtičniku **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="bf453-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="bf453-132">Mreža člana ekipe ne prikazuje posameznih nalog v zapisu člana ekipe.</span><span class="sxs-lookup"><span data-stu-id="bf453-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="bf453-133">Dodano je novo preverjanje veljavnosti in sporočila o napakah zaradi izjeme s sklicem »null« v vtičniku **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="bf453-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="bf453-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="bf453-134">**Sales**</span></span>

<span data-ttu-id="bf453-135">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="bf453-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="bf453-136">Pri izbiri podrobnosti ponudbe ali pogodbe, ki temelji na projektu, bi moral biti gumb **Predlog** viden samo pri izbiri podrobnosti, ki temeljijo na izdelku in so povezane z obstoječim izdelkom.</span><span class="sxs-lookup"><span data-stu-id="bf453-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="bf453-137">Razdelite privilegij **Create_Product** iz privilegija **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="bf453-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="bf453-138">Če izbrišete podrobnosti računa, bo prišlo do napake pri sklicu »null« za **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="bf453-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
