---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 25, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 25.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143801"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="212c2-103">Novosti ali spremembe v izdaji posodobitve za Project Service Automation 25, V3</span><span class="sxs-lookup"><span data-stu-id="212c2-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="212c2-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="212c2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="212c2-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="212c2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="212c2-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="212c2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="212c2-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="212c2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="212c2-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="212c2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="212c2-109">Ta tema navaja funkcije in popravke, ki so novi ali spremenjeni za Project Service Automation, različica 3, izdaja posodobitve 25. Ta različica ima številko graditve V 3.10.43.76 in je na splošno na voljo s samoposodobitvijo oktobra 2020.</span><span class="sxs-lookup"><span data-stu-id="212c2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="212c2-110">Izdaja posodobitve 25</span><span class="sxs-lookup"><span data-stu-id="212c2-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="212c2-111">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="212c2-111">Bug fixes</span></span>

<span data-ttu-id="212c2-112">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="212c2-112">**Time and Expense**</span></span>

<span data-ttu-id="212c2-113">Ta težava je odpravljena:</span><span class="sxs-lookup"><span data-stu-id="212c2-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="212c2-114">Grafikon vnosa časa, ki prikazuje dodatne podatke, ki temelji na prevelikem intervalu, ki je pridobljen.</span><span class="sxs-lookup"><span data-stu-id="212c2-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="212c2-115">**Upravljanje virov**</span><span class="sxs-lookup"><span data-stu-id="212c2-115">**Resource Management**</span></span>

<span data-ttu-id="212c2-116">Ta težava je odpravljena:</span><span class="sxs-lookup"><span data-stu-id="212c2-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="212c2-117">Dodana je koda orodja Package Deployer, da lahko preskočite uvoz popravkov rešitve Universal Resource Scheduling , če že obstaja popravek višje različice.</span><span class="sxs-lookup"><span data-stu-id="212c2-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="212c2-118">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="212c2-118">**Project Management**</span></span>

<span data-ttu-id="212c2-119">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="212c2-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="212c2-120">Popravljena neskladja zaokroževanja in neskladja v menjalnem tečaju, kar povzroča nepravilno načrtovane stroške v mreži za sledenje projekta.</span><span class="sxs-lookup"><span data-stu-id="212c2-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="212c2-121">Podpira zmožnost prikaza dveh ali več mrež za odzivanje v obrazcu **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="212c2-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="212c2-122">Zagotovljeno preverjanje veljavnosti za obravnavo zmožnosti dodeljevanja opravila mimo končnega datuma koledarja, kar povzroči neuspešno dodelitev virov.</span><span class="sxs-lookup"><span data-stu-id="212c2-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="212c2-123">Izboljšano obravnavanje napak za obravnavo izjeme sklica »Null«, ustvarjene iz naslednjega:</span><span class="sxs-lookup"><span data-stu-id="212c2-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="212c2-124">Vtičnik **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="212c2-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="212c2-125">**PreValidateProjectTaskCreate** ko se projektno opravilo ustvari brez povezanega projekta</span><span class="sxs-lookup"><span data-stu-id="212c2-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="212c2-126">Vtičnik **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="212c2-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="212c2-127">Vtičnik **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="212c2-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="212c2-128">Vtičnik **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="212c2-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="212c2-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="212c2-129">**Sales**</span></span>

<span data-ttu-id="212c2-130">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="212c2-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="212c2-131">Izboljšano obravnavanje napak za obravnavo izjeme sklica »Null«, ki jo je ustvaril **Kopiraj projekt: ocenjevanje upravljanja virov pomoči**.</span><span class="sxs-lookup"><span data-stu-id="212c2-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="212c2-132">Možnost **Ni pripravljeno za izdajanje računov** v možnosti **Nedokončana opravila obračunavanja časa in materiala** ne izbriše stanja obračunavanja.</span><span class="sxs-lookup"><span data-stu-id="212c2-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="212c2-133">Nepravilno označeni gumbi **Cene** na zavihku **Cena vloge** in **Katalog izdelkov** so popravljeni.</span><span class="sxs-lookup"><span data-stu-id="212c2-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
