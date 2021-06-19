---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 30, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 30.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010446"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="259fc-103">Novosti ali spremembe v izdaji posodobitve za Project Service Automation 30, V3</span><span class="sxs-lookup"><span data-stu-id="259fc-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="259fc-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="259fc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="259fc-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="259fc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="259fc-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="259fc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="259fc-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="259fc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="259fc-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="259fc-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="259fc-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 30.</span><span class="sxs-lookup"><span data-stu-id="259fc-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="259fc-110">Številka graditve te različice je V3.10.51.61 in je na splošno na voljo prek samostojne posodobitve v aprilu 2021.</span><span class="sxs-lookup"><span data-stu-id="259fc-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="259fc-111">Izdaja posodobitve 30</span><span class="sxs-lookup"><span data-stu-id="259fc-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="259fc-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="259fc-112">Bug fixes</span></span>

<span data-ttu-id="259fc-113">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="259fc-113">**Time and Expense**</span></span>

<span data-ttu-id="259fc-114">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="259fc-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="259fc-115">Napaka se pojavi, ko ustvarite in shranite vnos časa na strani **Hitro ustvarjanje**, če je polje **Vloga** odstranjeno.</span><span class="sxs-lookup"><span data-stu-id="259fc-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="259fc-116">Filter za vnos časa uporablja napačen operator filtra.</span><span class="sxs-lookup"><span data-stu-id="259fc-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="259fc-117">Kopirani časovni listi niso samodejno prikazani, ko izberete **Kopiraj teden** pri kontrolniku za vnos časa.</span><span class="sxs-lookup"><span data-stu-id="259fc-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="259fc-118">**Upravljanje virov**</span><span class="sxs-lookup"><span data-stu-id="259fc-118">**Resource Management**</span></span>

<span data-ttu-id="259fc-119">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="259fc-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="259fc-120">Ko podaljšate rezervacijo, je stanje rezervacije, dodeljeno veljavni rezervacije, napačno.</span><span class="sxs-lookup"><span data-stu-id="259fc-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="259fc-121">Podaljšanje rezervacije upošteva stanje rezervacije, opredeljeno kot **Potrjeno** v metapodatkih o nastavitvi rezervacije.</span><span class="sxs-lookup"><span data-stu-id="259fc-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="259fc-122">Če veljavno stanje rezervacije ni določeno, sporočilo o napaki ni pravilno lokalizirano.</span><span class="sxs-lookup"><span data-stu-id="259fc-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="259fc-123">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="259fc-123">**Project Management**</span></span>

<span data-ttu-id="259fc-124">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="259fc-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="259fc-125">Projektov ni mogoče ustvariti v eni valuti in vključujejo povezane naloge v drugi valuti.</span><span class="sxs-lookup"><span data-stu-id="259fc-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="259fc-126">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="259fc-126">**Sales**</span></span>

<span data-ttu-id="259fc-127">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="259fc-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="259fc-128">Ko se cenik kopira, se cene ne posodabljajo.</span><span class="sxs-lookup"><span data-stu-id="259fc-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="259fc-129">Zaključevanje ponudbe kot neuspešne ne uspe, če ima podrobnost o ceni vrednost za izvor.</span><span class="sxs-lookup"><span data-stu-id="259fc-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="259fc-130">Pri entiteti **Projektno opravilo** so bili **Ocenjeni stroški** preimenovani v možnost **Načrtovani stroški (osnova)**.</span><span class="sxs-lookup"><span data-stu-id="259fc-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="259fc-131">Izjema z referenco z vrednostjo »null« se ustvari, ko se računi ustvarijo ali izbrišejo.</span><span class="sxs-lookup"><span data-stu-id="259fc-131">A null reference exception is generated when invoices are created or deleted.</span></span>
