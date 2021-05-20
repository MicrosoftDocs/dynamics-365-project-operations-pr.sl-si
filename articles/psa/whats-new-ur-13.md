---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 13, V3
description: V tej temi so na voljo informacije o novostih v izdaji posodobitve za Project Service Automation 13, V3.
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
ms.openlocfilehash: a4ebc2e6ca3f6be0a05a7240d762d7a8cf92d81b
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949474"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="7e9e0-103">Izdaja posodobitve 13 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="7e9e0-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7e9e0-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="7e9e0-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="7e9e0-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7e9e0-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7e9e0-107">Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="7e9e0-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7e9e0-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7e9e0-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 13.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="7e9e0-110">Ta različica ima številko graditve V3.10.3.18 in je na voljo po naslednjem razporedu:</span><span class="sxs-lookup"><span data-stu-id="7e9e0-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="7e9e0-111">**Splošna razpoložljivost (samostojna posodobitev):** november 2019</span><span class="sxs-lookup"><span data-stu-id="7e9e0-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="7e9e0-112">**Samodejna posodobitev:** december 2019</span><span class="sxs-lookup"><span data-stu-id="7e9e0-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="7e9e0-113">Izdaja posodobitve 13</span><span class="sxs-lookup"><span data-stu-id="7e9e0-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="7e9e0-114">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="7e9e0-114">Bug fixes</span></span>

- <span data-ttu-id="7e9e0-115">Čas in strošek</span><span class="sxs-lookup"><span data-stu-id="7e9e0-115">Time and Expense</span></span>

     - <span data-ttu-id="7e9e0-116">Popravljeno: funkcionalnost iskanja na strani **Odobritev stroškov** ne deluje pri iskanju po namenu stroška.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="7e9e0-117">Upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="7e9e0-117">Resource Management</span></span>

     - <span data-ttu-id="7e9e0-118">Popravljeno: številke pri usklajevanju so bile posodobljene, da so poravnane desno.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="7e9e0-119">Popravljeno: imena virov ni mogoče dodeliti opravilom prek zavihka **Razpored**.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="7e9e0-120">Vodenje projektov</span><span class="sxs-lookup"><span data-stu-id="7e9e0-120">Project Management</span></span>

     - <span data-ttu-id="7e9e0-121">Popravljeno: ničelna referenčna izjema pri dodeljevanju člana ekipe, ko v **TransactionType** manjkajo informacije za nastavitev za **Enota** in **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="7e9e0-122">Sales</span><span class="sxs-lookup"><span data-stu-id="7e9e0-122">Sales</span></span>

     - <span data-ttu-id="7e9e0-123">Popravljeno: podvojeni zapisi vrste transakcije vrnejo napako, ko so ustvarjeni zapisi cene vloge.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="7e9e0-124">Popravljeno: dodatni gumbi za možnosti **Nova priložnost**, **Ponudba**, **Vrstica naročila** in **Dodajanje izdelka** so vidni v ukazih za »Priložnosti«, »Ponudbe«, »Izdelki iz naročila« in podmrežo »Vrstice«, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="7e9e0-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]