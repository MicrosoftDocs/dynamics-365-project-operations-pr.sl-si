---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 33, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 33.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334602"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="39b08-103">Novosti ali spremembe v izdaji posodobitve za Project Service Automation 33, V3</span><span class="sxs-lookup"><span data-stu-id="39b08-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="39b08-104">Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="39b08-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="39b08-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="39b08-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="39b08-106">Združljiva je z s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="39b08-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="39b08-107">Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="39b08-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="39b08-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="39b08-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="39b08-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 33.</span><span class="sxs-lookup"><span data-stu-id="39b08-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="39b08-110">Različica z delovno številko V3.10.54.98 je julija 2021 na voljo s samoposodobitvijo.</span><span class="sxs-lookup"><span data-stu-id="39b08-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="39b08-111">Izdaja posodobitve 33</span><span class="sxs-lookup"><span data-stu-id="39b08-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="39b08-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="39b08-112">Bug fixes</span></span>

<span data-ttu-id="39b08-113">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="39b08-113">**Time and Expense**</span></span>

<span data-ttu-id="39b08-114">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="39b08-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="39b08-115">Zaklenjeni polji **msdyn_description** in **msdyn_externaldescription** je mogoče urediti po oddaji.</span><span class="sxs-lookup"><span data-stu-id="39b08-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="39b08-116">Sporočilo o napaki se pojavi, če je ustvarjen strošek, ki ni povezan s projektom.</span><span class="sxs-lookup"><span data-stu-id="39b08-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="39b08-117">Ko je časovni vnos ustvarjen, se vloga vira privzeto nastavi na nedejavno vlogo.</span><span class="sxs-lookup"><span data-stu-id="39b08-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="39b08-118">Vrstice dnevnika, povezane s preklicanimi in izbrisanimi stroški, se ne odstranijo.</span><span class="sxs-lookup"><span data-stu-id="39b08-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="39b08-119">V obrazcu **Obrazec za hitro ustvarjanje časovnega vnosa** posodobite **Seznam projektnih nalog** in tako datum, ki je prikazan privzeto, zamenjajte z datumom začetka opravila.</span><span class="sxs-lookup"><span data-stu-id="39b08-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="39b08-120">Ko v zavihku **Povezano** za vir, ki ga je mogoče rezervirati, ustvarite časovni vnos, se slednji neustrezno ustvari za vpisane uporabnike namesto za nadrejeni vir, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="39b08-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="39b08-121">V pogovorno okno **MDD za množične odobritve** so dodana nova polja.</span><span class="sxs-lookup"><span data-stu-id="39b08-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="39b08-122">**Načrtovanje projekta**</span><span class="sxs-lookup"><span data-stu-id="39b08-122">**Project planning**</span></span>

<span data-ttu-id="39b08-123">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="39b08-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="39b08-124">Ko so projektne predloge za delovne ure uporabljene v zapletenih koledarjih, se projekt ustvarja počasi.</span><span class="sxs-lookup"><span data-stu-id="39b08-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="39b08-125">Ko je datum začetka poznejši od datuma zaključka, se na predlogi za kopiranje projekta zaradi razlik v časovnih komponentah vsakega polja prikaže napaka.</span><span class="sxs-lookup"><span data-stu-id="39b08-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="39b08-126">**Upravljanje virov**</span><span class="sxs-lookup"><span data-stu-id="39b08-126">**Resource management**</span></span>

<span data-ttu-id="39b08-127">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="39b08-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="39b08-128">V poizvedbi za uporabo virov je uporabljen napačen parameter, XML pa vodi do neustreznega filtriranja rezultatov v mreži **Uporaba virov**.</span><span class="sxs-lookup"><span data-stu-id="39b08-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="39b08-129">Ob potrditvi možnosti **Podaljšanje rezervacij** se prikaže napačen končni datum rezervacije.</span><span class="sxs-lookup"><span data-stu-id="39b08-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="39b08-130">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="39b08-130">**Sales**</span></span>

<span data-ttu-id="39b08-131">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="39b08-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="39b08-132">Sporočilo o napaki se pojavi, če je ustvarjena cena kategorije z manjkajočimi vrednostmi.</span><span class="sxs-lookup"><span data-stu-id="39b08-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="39b08-133">Sporočilo o napaki se pojavi, če je mejnik podrobnosti pogodbe ustvarjen brez vrstice naročila.</span><span class="sxs-lookup"><span data-stu-id="39b08-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
