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
ms.openlocfilehash: dbdcb811bfeacf17e841d679f097c591c16cd4c0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281048"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="a69f2-103">Izdaja posodobitve 13 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="a69f2-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a69f2-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="a69f2-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="a69f2-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="a69f2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a69f2-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a69f2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a69f2-107">Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="a69f2-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="a69f2-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a69f2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a69f2-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 13.</span><span class="sxs-lookup"><span data-stu-id="a69f2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="a69f2-110">Ta različica ima številko graditve V3.10.3.18 in je na voljo po naslednjem razporedu:</span><span class="sxs-lookup"><span data-stu-id="a69f2-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="a69f2-111">**Splošna razpoložljivost (samostojna posodobitev):** november 2019</span><span class="sxs-lookup"><span data-stu-id="a69f2-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="a69f2-112">**Samodejna posodobitev:** december 2019</span><span class="sxs-lookup"><span data-stu-id="a69f2-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="a69f2-113">Izdaja posodobitve 13</span><span class="sxs-lookup"><span data-stu-id="a69f2-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="a69f2-114">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="a69f2-114">Bug fixes</span></span>

- <span data-ttu-id="a69f2-115">Čas in strošek</span><span class="sxs-lookup"><span data-stu-id="a69f2-115">Time and Expense</span></span>

     - <span data-ttu-id="a69f2-116">Popravljeno: funkcionalnost iskanja na strani **Odobritev stroškov** ne deluje pri iskanju po namenu stroška.</span><span class="sxs-lookup"><span data-stu-id="a69f2-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="a69f2-117">Upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="a69f2-117">Resource Management</span></span>

     - <span data-ttu-id="a69f2-118">Popravljeno: številke pri usklajevanju so bile posodobljene, da so poravnane desno.</span><span class="sxs-lookup"><span data-stu-id="a69f2-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="a69f2-119">Popravljeno: imena virov ni mogoče dodeliti opravilom prek zavihka **Razpored**.</span><span class="sxs-lookup"><span data-stu-id="a69f2-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="a69f2-120">Vodenje projektov</span><span class="sxs-lookup"><span data-stu-id="a69f2-120">Project Management</span></span>

     - <span data-ttu-id="a69f2-121">Popravljeno: ničelna referenčna izjema pri dodeljevanju člana ekipe, ko v **TransactionType** manjkajo informacije za nastavitev za **Enota** in **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="a69f2-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="a69f2-122">Sales</span><span class="sxs-lookup"><span data-stu-id="a69f2-122">Sales</span></span>

     - <span data-ttu-id="a69f2-123">Popravljeno: podvojeni zapisi vrste transakcije vrnejo napako, ko so ustvarjeni zapisi cene vloge.</span><span class="sxs-lookup"><span data-stu-id="a69f2-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="a69f2-124">Popravljeno: dodatni gumbi za možnosti **Nova priložnost**, **Ponudba**, **Vrstica naročila** in **Dodajanje izdelka** so vidni v ukazih za »Priložnosti«, »Ponudbe«, »Izdelki iz naročila« in podmrežo »Vrstice«, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="a69f2-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]