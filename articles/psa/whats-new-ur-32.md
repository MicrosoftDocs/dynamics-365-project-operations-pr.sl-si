---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 32, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 32.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129686"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="7dd68-103">Novosti ali spremembe v izdaji posodobitve za Project Service Automation 32, V3</span><span class="sxs-lookup"><span data-stu-id="7dd68-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7dd68-104">Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7dd68-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="7dd68-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="7dd68-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7dd68-106">Združljiva je z s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="7dd68-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7dd68-107">Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="7dd68-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="7dd68-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7dd68-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7dd68-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 32.</span><span class="sxs-lookup"><span data-stu-id="7dd68-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="7dd68-110">Ta različica ima številko gradnje V3.10.53.108 in je na splošno na voljo s samoposodobitvijo junija 2021.</span><span class="sxs-lookup"><span data-stu-id="7dd68-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="7dd68-111">Izdaja posodobitve 32</span><span class="sxs-lookup"><span data-stu-id="7dd68-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7dd68-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="7dd68-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="7dd68-113">Splošno</span><span class="sxs-lookup"><span data-stu-id="7dd68-113">General</span></span>

- <span data-ttu-id="7dd68-114">Če večja nadgradnja ne uspe, je treba blokirati samo glavne vstopne točke aplikacije, da se zagotovi, da so entitete v skupni rabi še vedno dostopne.</span><span class="sxs-lookup"><span data-stu-id="7dd68-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="7dd68-115">Čas in strošek</span><span class="sxs-lookup"><span data-stu-id="7dd68-115">Time and Expense</span></span>

<span data-ttu-id="7dd68-116">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="7dd68-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="7dd68-117">**TimeEntriesImportFromResourceAssignment** ne vzdržuje začetnega in končnega časa rezine krivulje za dodelitev vira.</span><span class="sxs-lookup"><span data-stu-id="7dd68-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="7dd68-118">Ko izberete možnost **Odpri vnos** v mreži **Vnos časa**, morda ne boste mogli izbirati drugih obrazcev.</span><span class="sxs-lookup"><span data-stu-id="7dd68-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="7dd68-119">Medtem ko uvažate dodelitve v časovne vnose, lahko poizvedba odjemalske kode ustvari dolg URL, zaradi katerega poizvedba ne uspe.</span><span class="sxs-lookup"><span data-stu-id="7dd68-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="7dd68-120">Ko je vrednost izbrisana iz celice v mreži **Vnos časa**, fokus ne ostane v mreži.</span><span class="sxs-lookup"><span data-stu-id="7dd68-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="7dd68-121">Gumb **Zavrni** je odstranjen iz pogleda **Obdelava odobritev** za sodobne odobritve.</span><span class="sxs-lookup"><span data-stu-id="7dd68-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="7dd68-122">Na stabilnost in zmogljivost množične odobritve vnosa časa vplivajo zastoji in neuspelo ravnanje s prilagajanji, povezanimi z entiteto **Vnos časa**.</span><span class="sxs-lookup"><span data-stu-id="7dd68-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="7dd68-123">Načrtovanje projekta</span><span class="sxs-lookup"><span data-stu-id="7dd68-123">Project Planning</span></span>

- <span data-ttu-id="7dd68-124">Izjema z referenco z vrednostjo »null« se ustvari, ko posodobite projekt, ki ima v polju **Pogodbena enota** vrednost »null«.</span><span class="sxs-lookup"><span data-stu-id="7dd68-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="7dd68-125">Funkcija **osvežitev skupnih vrednosti za projekt** napačno izračuna preostali strošek in preostale prodaje za projekt.</span><span class="sxs-lookup"><span data-stu-id="7dd68-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="7dd68-126">Odvečni izračuni cen vplivajo na učinkovitost delovanja, ki je povezana s posodobitvami na krivuljah dodelitve virov.</span><span class="sxs-lookup"><span data-stu-id="7dd68-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="7dd68-127">Upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="7dd68-127">Resource Management</span></span>

<span data-ttu-id="7dd68-128">Ta težava je odpravljena:</span><span class="sxs-lookup"><span data-stu-id="7dd68-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="7dd68-129">Ko je zmogljivost koledarja vira, ki ga je mogoče rezervirati, večja od 1, rešitev Project Service Automation napačno prepozna zmogljivost kot 0 (nič).</span><span class="sxs-lookup"><span data-stu-id="7dd68-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="7dd68-130">Zato se v pogledu razporeda pojavi neskončna zanka.</span><span class="sxs-lookup"><span data-stu-id="7dd68-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="7dd68-131">Prodaja</span><span class="sxs-lookup"><span data-stu-id="7dd68-131">Sales</span></span>

<span data-ttu-id="7dd68-132">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="7dd68-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="7dd68-133">Ko se ustvari vrstica dnevnika, ki ima vrsto transakcije po meri, pride do naslednje izjeme z referenco z vrednostjo »null«: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="7dd68-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="7dd68-134">Vlog in kategorij, ki so deaktivirane pred kopiranjem ponudbe, ne smete dodajati plačljivim vlogam in kategorijam na novo kopirane ponudbe.</span><span class="sxs-lookup"><span data-stu-id="7dd68-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="7dd68-135">Datum dokumenta in datum knjiženja računov nista usklajena z začetnim datumom, ki je naveden v podrobnosti vrstice računa, ustvarjene neposredno v osnutku računa.</span><span class="sxs-lookup"><span data-stu-id="7dd68-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="7dd68-136">Izjeme z referenco z vrednostjo »null« se ustvarijo v scenarijih, ki so povezani z deaktivacijo vlog in kategorij pred kopiranjem ponudbe.</span><span class="sxs-lookup"><span data-stu-id="7dd68-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="7dd68-137">Dejanje **Posodobi cene** na strani **Projekti** ne posodobi ocen stroškov in ocen materiala.</span><span class="sxs-lookup"><span data-stu-id="7dd68-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
