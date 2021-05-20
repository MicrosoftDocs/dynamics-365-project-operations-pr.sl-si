---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 23, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 23.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: f90c0d2168b261cf1b6ef10374f282274ea61af5
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948979"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="13342-103">Izdaja posodobitve 23 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="13342-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="13342-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="13342-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="13342-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="13342-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="13342-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="13342-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="13342-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="13342-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="13342-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="13342-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="13342-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 23.</span><span class="sxs-lookup"><span data-stu-id="13342-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="13342-110">Ta različica ima številko graditve V 3.10.34.30 in je splošno na voljo s samostojno posodobitvijo od avgusta 2020.</span><span class="sxs-lookup"><span data-stu-id="13342-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="13342-111">Izdaja posodobitve 23</span><span class="sxs-lookup"><span data-stu-id="13342-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="13342-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="13342-112">Bug fixes</span></span>

<span data-ttu-id="13342-113">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="13342-113">**Time and Expense**</span></span>

<span data-ttu-id="13342-114">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="13342-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="13342-115">Obravnavanje mejnega primera v razdelku **Brisanje člana projektne ekipe** za zagotavljanje smiselne izjeme.</span><span class="sxs-lookup"><span data-stu-id="13342-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="13342-116">Pri uvozu dodelitve se prikaže prazen zaslon za odstranjevanje.</span><span class="sxs-lookup"><span data-stu-id="13342-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="13342-117">**Upravljanje virov**</span><span class="sxs-lookup"><span data-stu-id="13342-117">**Resource Management**</span></span>

<span data-ttu-id="13342-118">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="13342-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="13342-119">**Kartica virov v mreži za uporabo virov** prikazuje napačne podatke, če je časovno merilo več kot pet dni.</span><span class="sxs-lookup"><span data-stu-id="13342-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="13342-120">Ko stranke ustvarijo vir, ki ga je mogoče rezervirati, vtičnik občasno ne uspe samodejno dodati vira v skupino Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="13342-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="13342-121">Pogled **Uskladitev** napačno prikazuje ročne obrise v pogledu **Teden** ali **Mesec**.</span><span class="sxs-lookup"><span data-stu-id="13342-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="13342-122">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="13342-122">**Project Management**</span></span>

<span data-ttu-id="13342-123">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="13342-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="13342-124">Zaradi prekomernega števila entitet **RetrieveMultiple za uporabniške nastavitve** je delovanje odobritev projektov in drugih postopkov poslabšano.</span><span class="sxs-lookup"><span data-stu-id="13342-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="13342-125">Iskanje virov v mreži **Načrtovanje opravil** je omejeno na prikaz največ pet članov projektne ekipe.</span><span class="sxs-lookup"><span data-stu-id="13342-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="13342-126">Iskanje virov v mreži **Načrtovanje opravil** ne filtrira nedejavnih virov.</span><span class="sxs-lookup"><span data-stu-id="13342-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="13342-127">Ročni način ne deluje po pričakovanjih v strukturirani členitvi dela pri načrtovanju projekta.</span><span class="sxs-lookup"><span data-stu-id="13342-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="13342-128">Mreža **Načrtovanje opravil** prikazuje **Nedejavne kategorije transakcij**.</span><span class="sxs-lookup"><span data-stu-id="13342-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="13342-129">Mreža **Dodelitev virov** napačno zaokroži, če ima opravilo več dodelitev.</span><span class="sxs-lookup"><span data-stu-id="13342-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="13342-130">Vrednosti zaokroževanja se razlikujejo med načrtovanimi in dejanskimi stroški za eno opravilo.</span><span class="sxs-lookup"><span data-stu-id="13342-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="13342-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="13342-131">**Sales**</span></span>

<span data-ttu-id="13342-132">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="13342-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="13342-133">Z dvoklikom možnosti **Pridobi vse kategorije transakcij** se ustvari več vrstic.</span><span class="sxs-lookup"><span data-stu-id="13342-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]