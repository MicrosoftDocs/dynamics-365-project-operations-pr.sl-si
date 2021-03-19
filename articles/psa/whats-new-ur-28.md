---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 28, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 28.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 079679302b2d8dac3074732b2392a7b811ac9711
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280238"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="46e28-103">Novosti ali spremembe v izdaji posodobitve za Project Service Automation 28, V3</span><span class="sxs-lookup"><span data-stu-id="46e28-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="46e28-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="46e28-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="46e28-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="46e28-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="46e28-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="46e28-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="46e28-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="46e28-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="46e28-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="46e28-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="46e28-109">Ta tema navaja funkcije in popravke, ki so novi ali spremenjeni za aplikacijo Project Service Automation V3, izdaja posodobitve 28. Ta različica ima številko graditve V3.10.46.32 in je na splošno na voljo s samoposodobitvijo januarja 2021.</span><span class="sxs-lookup"><span data-stu-id="46e28-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="46e28-110">Izdaja posodobitve 28</span><span class="sxs-lookup"><span data-stu-id="46e28-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="46e28-111">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="46e28-111">Bug fixes</span></span>

<span data-ttu-id="46e28-112">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="46e28-112">**Time and Expense**</span></span>

<span data-ttu-id="46e28-113">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="46e28-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="46e28-114">Uporabniki lahko za posodobitev časovnih vnosov, ki do bili odobreni in poslani, uporabijo **Množično urejanje**.</span><span class="sxs-lookup"><span data-stu-id="46e28-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="46e28-115">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="46e28-115">**Project Management**</span></span>

<span data-ttu-id="46e28-116">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="46e28-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="46e28-117">V primerih, ko je GUID opravila interpretiran kot številka, opravil ni mogoče odpreti za urejanje z uporabo možnosti **Uredi opravilo** na traku na strani **Strukturirana členitev dela**.</span><span class="sxs-lookup"><span data-stu-id="46e28-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="46e28-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="46e28-118">**Sales**</span></span>

<span data-ttu-id="46e28-119">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="46e28-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="46e28-120">Ko je priklican vtičnik **GetEstimatesForProject**, je ustvarjena izjema s sklicem »null«.</span><span class="sxs-lookup"><span data-stu-id="46e28-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="46e28-121">Možnost **Označi kot pripravljeno za izdajanje računov** na mreži mejnika samo delno posodobi atribute, razen atributa **Status računa**, ki je posodobljen.</span><span class="sxs-lookup"><span data-stu-id="46e28-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]