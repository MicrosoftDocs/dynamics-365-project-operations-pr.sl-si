---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 19, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 19.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 7812bc41f32f9d4116c63990059f7dbc0351cf9e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006621"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="8ae3d-103">Izdaja posodobitve 19 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="8ae3d-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8ae3d-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8ae3d-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8ae3d-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8ae3d-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8ae3d-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8ae3d-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8ae3d-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za PSA V3, izdaja posodobitve 19.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="8ae3d-110">Številka graditve te različice je V3.10.30.41 in je na splošno na voljo prek samostojne posodobitve maja 2020.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="8ae3d-111">Izdaja posodobitve 19</span><span class="sxs-lookup"><span data-stu-id="8ae3d-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8ae3d-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="8ae3d-112">Bug fixes</span></span>

<span data-ttu-id="8ae3d-113">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-113">**Time and Expense**</span></span>

<span data-ttu-id="8ae3d-114">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="8ae3d-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="8ae3d-115">Napake zaradi uvoza časovnih vnosov niso prikazane pravilno.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="8ae3d-116">Mreža časovnega vnosa ne podpira vedenja polja **Samo datum**.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="8ae3d-117">Viri projekta ne morejo ustvariti stroška s projektom.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="8ae3d-118">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-118">**Project Management**</span></span>

<span data-ttu-id="8ae3d-119">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="8ae3d-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="8ae3d-120">Podrejeno opravilo podrejenega opravila ustvari nepravilno oceno obsega dela med izračunom ocene končnih stroškov.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="8ae3d-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8ae3d-121">**Sales**</span></span>

<span data-ttu-id="8ae3d-122">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="8ae3d-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="8ae3d-123">Dejanje **Preračunaj** ne deluje s podrobnostmi vrstice pogodbe o stroških ali podrobnostmi vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="8ae3d-124">V ocenah stroškov manjka možnost **Posodobi cene**.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="8ae3d-125">Stranke na strani **Projektna pogodba** ne morejo izbrati razlogov stanja pogodb po meri.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="8ae3d-126">Stranke pri ustvarjanju cenika po meri iz ponudbe opažajo slabše delovanje.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="8ae3d-127">Stranke opažajo neskladnost s privzetimi vrednostmi **enot** na straneh **Podrobnosti vrstice ponudbe** in **Podrobnosti vrstice pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="8ae3d-128">Če so v vrstico pogodbe, ki se zaračunava, dodani elementi kategorije transakcije, ki se ne zaračunava, vrsta obračunavanja **Se ne zaračuna** kategorije transakcije ne bo upoštevana.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="8ae3d-129">Stranke novo dodanih vlog in kategorij ne morejo uporabiti za predhodno ustvarjene pogodbe.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="8ae3d-130">Stranke opažajo slabše delovanje funkcije »Nepotrebno pridobivanje« v datoteki PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="8ae3d-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="8ae3d-131">Vloge, ki so na seznamu **Kategorije virov** določene, da se ne zaračunavajo, morajo biti v vrstici pogodbe za projekt na zavihek **Vloge, ki se zaračunajo** dodane z opisom **Se ne zaračuna**.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="8ae3d-132">Stranke lahko pri ustvarjanju projekta opazijo slabše delovanje, ker **GetBookableResourceIdFromUser** pridobi vse stolpce virov, ki jih je mogoče rezervirati, ne le primarnega ID-ja.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="8ae3d-133">Entiteta **TransactionType** manjka v vtičniku posodobitve pred preverjanjem pristnosti, da uporabnikom prepreči vnos elementov **Enote** in **Skupine enot**, ki niso veljavne za vrste transakcij.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="8ae3d-134">Korak **Odstrani** ne deluje pri uvozu časovnega vnosa.</span><span class="sxs-lookup"><span data-stu-id="8ae3d-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]