---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 28, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 28.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010536"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="41069-103">Novosti ali spremembe v izdaji posodobitve za Project Service Automation 28, V3</span><span class="sxs-lookup"><span data-stu-id="41069-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="41069-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="41069-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="41069-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="41069-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="41069-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="41069-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="41069-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="41069-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="41069-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="41069-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="41069-109">Ta tema navaja funkcije in popravke, ki so novi ali spremenjeni za aplikacijo Project Service Automation V3, izdaja posodobitve 28. Ta različica ima številko graditve V3.10.46.32 in je na splošno na voljo s samoposodobitvijo januarja 2021.</span><span class="sxs-lookup"><span data-stu-id="41069-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="41069-110">Izdaja posodobitve 28</span><span class="sxs-lookup"><span data-stu-id="41069-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="41069-111">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="41069-111">Bug fixes</span></span>

<span data-ttu-id="41069-112">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="41069-112">**Time and Expense**</span></span>

<span data-ttu-id="41069-113">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="41069-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="41069-114">Uporabniki lahko za posodobitev časovnih vnosov, ki do bili odobreni in poslani, uporabijo **Množično urejanje**.</span><span class="sxs-lookup"><span data-stu-id="41069-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="41069-115">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="41069-115">**Project Management**</span></span>

<span data-ttu-id="41069-116">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="41069-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="41069-117">V primerih, ko je GUID opravila interpretiran kot številka, opravil ni mogoče odpreti za urejanje z uporabo možnosti **Uredi opravilo** na traku na strani **Strukturirana členitev dela**.</span><span class="sxs-lookup"><span data-stu-id="41069-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="41069-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="41069-118">**Sales**</span></span>

<span data-ttu-id="41069-119">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="41069-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="41069-120">Ko je priklican vtičnik **GetEstimatesForProject**, je ustvarjena izjema s sklicem »null«.</span><span class="sxs-lookup"><span data-stu-id="41069-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="41069-121">Možnost **Označi kot pripravljeno za izdajanje računov** na mreži mejnika samo delno posodobi atribute, razen atributa **Status računa**, ki je posodobljen.</span><span class="sxs-lookup"><span data-stu-id="41069-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]