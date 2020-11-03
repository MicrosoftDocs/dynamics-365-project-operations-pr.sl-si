---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 14, V3
description: V tej temi so na voljo informacije o novostih v izdaji posodobitve za Project Service Automation 14, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084714"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="b36d0-103">Izdaja posodobitve 14 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="b36d0-103">Project Service Automation Update Release 14, V3</span></span>
<span data-ttu-id="b36d0-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="b36d0-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="b36d0-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="b36d0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b36d0-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b36d0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b36d0-107">Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="b36d0-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="b36d0-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b36d0-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b36d0-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za PSA V3, izdaja posodobitve 14.</span><span class="sxs-lookup"><span data-stu-id="b36d0-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="b36d0-110">Ta različica ima številko graditve V3.10.4.21 in je na voljo po naslednjem razporedu:</span><span class="sxs-lookup"><span data-stu-id="b36d0-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="b36d0-111">**Splošna razpoložljivost (samostojna posodobitev):** januar 2020</span><span class="sxs-lookup"><span data-stu-id="b36d0-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="b36d0-112">**Samodejna posodobitev:** februar 2020</span><span class="sxs-lookup"><span data-stu-id="b36d0-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="b36d0-113">Izdaja posodobitve 14</span><span class="sxs-lookup"><span data-stu-id="b36d0-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="b36d0-114">Izboljšave</span><span class="sxs-lookup"><span data-stu-id="b36d0-114">Enhancements</span></span>

- <span data-ttu-id="b36d0-115">Sales</span><span class="sxs-lookup"><span data-stu-id="b36d0-115">Sales</span></span>

     - <span data-ttu-id="b36d0-116">Vrednosti polja po meri iz **Podrobnosti vrstice ponudb** so kopirane v **Podrobnosti vrstice projektne pogodbe** , ko je ponudba posodobljena na **Zaprto kot dobljeno**.</span><span class="sxs-lookup"><span data-stu-id="b36d0-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="b36d0-117">Potrjeni projekti so lahko označeni **Zaprto kot izgubljeno**.</span><span class="sxs-lookup"><span data-stu-id="b36d0-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="b36d0-118">Upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="b36d0-118">Resource Management</span></span>

     - <span data-ttu-id="b36d0-119">Pri podaljšanju rezervacij bodo uporabniki s pogovornim oknom za potrditev pozvani, da povzamejo rezultate rezervacije in zagotovijo povezavo do upravljanja rezervacij.</span><span class="sxs-lookup"><span data-stu-id="b36d0-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="b36d0-120">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="b36d0-120">Bug fixes</span></span>

- <span data-ttu-id="b36d0-121">Čas in strošek</span><span class="sxs-lookup"><span data-stu-id="b36d0-121">Time and Expense</span></span>

     - <span data-ttu-id="b36d0-122">Popravljeno: izboljšana uporabniška izkušnja, ko uporabnik ne izbere nobenega vnosa za popravilo.</span><span class="sxs-lookup"><span data-stu-id="b36d0-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="b36d0-123">Upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="b36d0-123">Resource Management</span></span>

     - <span data-ttu-id="b36d0-124">Popravljeno: večkratna rezervacija vira sega čez ime vira, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="b36d0-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="b36d0-125">Sales</span><span class="sxs-lookup"><span data-stu-id="b36d0-125">Sales</span></span>

     - <span data-ttu-id="b36d0-126">Popravljeno: skupna prodajna cena ni izračunana, dokler uporabnik ne vnese tudi lastne cene za ocene stroškov na projektu.</span><span class="sxs-lookup"><span data-stu-id="b36d0-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="b36d0-127">Popravljeno: zapiranje ponudbe kot **Pridobljeno** ne uspe, če povezana projektna pogodba ni v stanju **Osnutek**.</span><span class="sxs-lookup"><span data-stu-id="b36d0-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

