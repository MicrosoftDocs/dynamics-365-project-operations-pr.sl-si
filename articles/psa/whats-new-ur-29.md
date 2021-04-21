---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 29, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 29.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664663"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="f459f-103">Novosti ali spremembe v izdaji posodobitve za Project Service Automation 29, V3</span><span class="sxs-lookup"><span data-stu-id="f459f-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f459f-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f459f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f459f-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="f459f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f459f-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f459f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f459f-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="f459f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f459f-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f459f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f459f-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 29.</span><span class="sxs-lookup"><span data-stu-id="f459f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="f459f-110">Ta različica ima številko graditve V3.10.47.7 in je splošno na voljo s samoposodobitvijo februarja 2021.</span><span class="sxs-lookup"><span data-stu-id="f459f-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="f459f-111">Izdaja posodobitve 29</span><span class="sxs-lookup"><span data-stu-id="f459f-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f459f-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="f459f-112">Bug fixes</span></span>

<span data-ttu-id="f459f-113">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="f459f-113">**Time and Expense**</span></span>

<span data-ttu-id="f459f-114">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="f459f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f459f-115">Uporabniki v mreži časovnih vnosov ne vidijo delovnega časa, zabeleženega ob nedelovnih dneh.</span><span class="sxs-lookup"><span data-stu-id="f459f-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="f459f-116">Odobrene vnose stroškov je mogoče urejati v mreži.</span><span class="sxs-lookup"><span data-stu-id="f459f-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="f459f-117">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="f459f-117">**Project Management**</span></span>

<span data-ttu-id="f459f-118">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="f459f-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="f459f-119">Manjka logika preverjanja veljavnosti, ki zagotovi, da ure obsega dela za dodelitev virov ne morejo biti negativne.</span><span class="sxs-lookup"><span data-stu-id="f459f-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="f459f-120">Dejanje po meri **AssignResourcesForTask** posodobi vsa polja namesto samo spremenjenih polj.</span><span class="sxs-lookup"><span data-stu-id="f459f-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="f459f-121">Pri kopiranju projekta v okolju z vtičniki ali poteki dela, ki so registrirani z dogodkom **CreateProject**, se atribut **msdyn_bulkgenerationstatus** ne posodobi, če dejanje kopiranja **CopyWBSToProject** ne uspe.</span><span class="sxs-lookup"><span data-stu-id="f459f-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="f459f-122">Ko razširite koledar projekta, se delovni dnevi ne razvrstijo po naraščajočem vrstnem redu, zaradi česar nekatere posodobitve projektnih opravil ne uspejo.</span><span class="sxs-lookup"><span data-stu-id="f459f-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="f459f-123">Spreminjanje vodje projekta na obstoječem projektu sproži privzeto nastavitev organizacijske enote.</span><span class="sxs-lookup"><span data-stu-id="f459f-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="f459f-124">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="f459f-124">**Sales**</span></span>

<span data-ttu-id="f459f-125">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="f459f-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="f459f-126">Zavihek **Izvajanje pogodbe** na strani **Pogodba** med inicializacijo tiho odpove, ko ni nobene podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="f459f-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
