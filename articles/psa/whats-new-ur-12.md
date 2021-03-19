---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 12, V3
description: V tej temi so na voljo informacije o novostih v izdaji posodobitve za Project Service Automation 12, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f1b2fdc37fa2c2e31537b89b7027d2833e905578
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281093"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="e1d89-103">Izdaja posodobitve 12 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="e1d89-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e1d89-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="e1d89-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="e1d89-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="e1d89-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e1d89-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e1d89-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e1d89-107">Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="e1d89-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="e1d89-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e1d89-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e1d89-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 12.</span><span class="sxs-lookup"><span data-stu-id="e1d89-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="e1d89-110">Ta različica ima številko graditve V3.10.2.34 in je splošno na voljo s samostojno posodobitvijo v oktobru 2019.</span><span class="sxs-lookup"><span data-stu-id="e1d89-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="e1d89-111">Izdaja posodobitve 12</span><span class="sxs-lookup"><span data-stu-id="e1d89-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e1d89-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="e1d89-112">Bug fixes</span></span>

- <span data-ttu-id="e1d89-113">Čas in strošek</span><span class="sxs-lookup"><span data-stu-id="e1d89-113">Time and Expense</span></span>

    - <span data-ttu-id="e1d89-114">Popravljeno: sporočila o napakah časovnih vnosov so bila posodobljena z bolj relevantnim kontekstom.</span><span class="sxs-lookup"><span data-stu-id="e1d89-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="e1d89-115">Popravljeno: mreža in razpored časovnih vnosov pravilno prikazujeta navpični drsni trak, ko je potrebno.</span><span class="sxs-lookup"><span data-stu-id="e1d89-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="e1d89-116">Popravljeno: poslani stroškovni in časovni vnosi so lahko odobreni.</span><span class="sxs-lookup"><span data-stu-id="e1d89-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="e1d89-117">Popravljeno: pogovorno okno za potrditev preklica odobritve je bilo popravljeno, da odraža stanje odobritve ob spremembi z **Odobreno** na **Poslano**.</span><span class="sxs-lookup"><span data-stu-id="e1d89-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="e1d89-118">Popravljeno: polja **Cena**, **Enota** in **Količina** so zdaj zaklenjena na zapisu »Strošek«, potem ko je odobren.</span><span class="sxs-lookup"><span data-stu-id="e1d89-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="e1d89-119">Vodenje projektov</span><span class="sxs-lookup"><span data-stu-id="e1d89-119">Project Management</span></span>

    - <span data-ttu-id="e1d89-120">Popravljeno: dejanje **Novo** na glavnem obrazcu **Član ekipe** je bilo odstranjeno.</span><span class="sxs-lookup"><span data-stu-id="e1d89-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="e1d89-121">Popravljeno: dodelitve virov so bile posodobljene, da se upoštevajo napake zaradi netočnega zaokroževanja, zaradi česar se je končni datum opravila prestavil.</span><span class="sxs-lookup"><span data-stu-id="e1d89-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="e1d89-122">Popravljeno: v mreži opravil bodo strežniške napake prikazane uporabniku.</span><span class="sxs-lookup"><span data-stu-id="e1d89-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="e1d89-123">Popravljeno: v izbirniku oseb za opravilo je zdaj upodobljeno ime člana ekipe, namesto imena položaja.</span><span class="sxs-lookup"><span data-stu-id="e1d89-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="e1d89-124">Upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="e1d89-124">Resource Management</span></span>

    - <span data-ttu-id="e1d89-125">Popravljeno: podrobnosti zahtevanega pogoja za vir za projekte, ustvarjene iz predloge, zdaj uporabljajo projektni koledar.</span><span class="sxs-lookup"><span data-stu-id="e1d89-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="e1d89-126">Popravljeno: znanja in sposobnosti so zdaj privzeta iz glavnih podatkov vloge v zahtevan pogoj za vir za to vlogo.</span><span class="sxs-lookup"><span data-stu-id="e1d89-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="e1d89-127">Sales</span><span class="sxs-lookup"><span data-stu-id="e1d89-127">Sales</span></span>

    - <span data-ttu-id="e1d89-128">Popravljeno: podvojeni ID-ji predmetov, najdeni na glavnem obrazcu **Pogodba**.</span><span class="sxs-lookup"><span data-stu-id="e1d89-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="e1d89-129">Popravljeno: logika je bila posodobljena, da je zavihek **Analiza ponudbe** viden, tako da prikazuje nastavitev metapodatkov zavihka.</span><span class="sxs-lookup"><span data-stu-id="e1d89-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="e1d89-130">Popravljeno: datum knjiženja na dejanskem zapisu zdaj prihaja iz datuma časovnega/stroškovnega vnosa in ne datuma odobritve.</span><span class="sxs-lookup"><span data-stu-id="e1d89-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]