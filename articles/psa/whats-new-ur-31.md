---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 31, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 31.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945555"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="fbca2-103">Novosti ali spremembe v izdaji posodobitve za Project Service Automation 31, V3</span><span class="sxs-lookup"><span data-stu-id="fbca2-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fbca2-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fbca2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fbca2-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="fbca2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fbca2-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fbca2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fbca2-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="fbca2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fbca2-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fbca2-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fbca2-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 31.</span><span class="sxs-lookup"><span data-stu-id="fbca2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="fbca2-110">Številka graditve te različice je V3.10.52.77 in je na splošno na voljo prek samostojne posodobitve maja 2021.</span><span class="sxs-lookup"><span data-stu-id="fbca2-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="fbca2-111">Izdaja posodobitve 31</span><span class="sxs-lookup"><span data-stu-id="fbca2-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fbca2-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="fbca2-112">Bug fixes</span></span>

<span data-ttu-id="fbca2-113">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="fbca2-113">**Time and Expense**</span></span>

<span data-ttu-id="fbca2-114">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="fbca2-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="fbca2-115">Ukazni gumbi za nadzor vnosa časa na strani **Vir, ki ga je mogoče rezervirati** so povzročali zmedo.</span><span class="sxs-lookup"><span data-stu-id="fbca2-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="fbca2-116">V entiteti **Project.SetTrackingFields** je bila pri potrjevanju časovnega vnosa ustvarjena izjema z referenco z vrednostjo »null«.</span><span class="sxs-lookup"><span data-stu-id="fbca2-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="fbca2-117">**Upravljanje virov**</span><span class="sxs-lookup"><span data-stu-id="fbca2-117">**Resource Management**</span></span>

<span data-ttu-id="fbca2-118">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="fbca2-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="fbca2-119">V možnosti **Ustvari člana ekipe** niso pravilno prikazani metapodatki za nastavitev rezervacije za **Privzeto stanje prevzete rezervacije**.</span><span class="sxs-lookup"><span data-stu-id="fbca2-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="fbca2-120">Pri nadgradnji iz PSA 1.X na 3.X postopek nadgradnje ne uspe pri elementu **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="fbca2-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="fbca2-121">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="fbca2-121">**Sales**</span></span>

<span data-ttu-id="fbca2-122">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="fbca2-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="fbca2-123">Dejanski prihodek v mreži za sledenje pretvori zneske v valuto projekta.</span><span class="sxs-lookup"><span data-stu-id="fbca2-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="fbca2-124">Privzeta valuta ni jasno določena pri ustvarjanju vrstic dnevnika, vrstic ponudb in podrobnosti pogodbe v primerih, kjer se osnovna valuta organizacije razlikuje od valute projekta.</span><span class="sxs-lookup"><span data-stu-id="fbca2-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="fbca2-125">Poizvedba za **Čakanje na potrditev dnevnika popravkov** ne filtrira po projektu.</span><span class="sxs-lookup"><span data-stu-id="fbca2-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="fbca2-126">Preostanek prodaje projekta se napačno izračuna.</span><span class="sxs-lookup"><span data-stu-id="fbca2-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="fbca2-127">Ponudbe na podlagi stika niso uspešne, če so ustvarjene brez cenika.</span><span class="sxs-lookup"><span data-stu-id="fbca2-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="fbca2-128">Ob izbiri možnosti **Potrdi račun** se ne prikaže vrtavka obdelovanja.</span><span class="sxs-lookup"><span data-stu-id="fbca2-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="fbca2-129">Ob izbiri možnosti **Ustvari račun** se ne prikaže vrtavka obdelovanja.</span><span class="sxs-lookup"><span data-stu-id="fbca2-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="fbca2-130">Zapiranje ponudbe s stanjem »izgubljena« ne prekliče rezervacij.</span><span class="sxs-lookup"><span data-stu-id="fbca2-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







