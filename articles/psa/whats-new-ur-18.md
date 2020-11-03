---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 18, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 18.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084710"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="bec8b-103">Izdaja posodobitve 18 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="bec8b-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="bec8b-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bec8b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="bec8b-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="bec8b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="bec8b-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="bec8b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="bec8b-107">Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="bec8b-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="bec8b-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="bec8b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="bec8b-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 18.</span><span class="sxs-lookup"><span data-stu-id="bec8b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="bec8b-110">Številka graditve te različice je V3.10.8.12 in je na splošno na voljo prek samostojne posodobitve v aprilu 2020.</span><span class="sxs-lookup"><span data-stu-id="bec8b-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="bec8b-111">Izdaja posodobitve 18</span><span class="sxs-lookup"><span data-stu-id="bec8b-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="bec8b-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="bec8b-112">Bug fixes</span></span>

<span data-ttu-id="bec8b-113">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="bec8b-113">**Time and Expense**</span></span>

- <span data-ttu-id="bec8b-114">Popravljeno: postopki **Preklic** , **Zahteva** in **Preklic odobritve** naletijo na izjeme z nejasnimi sporočili o napakah.</span><span class="sxs-lookup"><span data-stu-id="bec8b-114">Fixed: **Recall** , **Request** , and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="bec8b-115">Popravljeno: ko za določen strošek postopek **Preklic odobritve** ne uspe, ne pride do napake ustrezne izjeme.</span><span class="sxs-lookup"><span data-stu-id="bec8b-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="bec8b-116">Popravljeno: mreža časovnih vnosov nepravilno obravnava dela proste dneve v Avstraliji po oktobrskem preklopu na poletni čas.</span><span class="sxs-lookup"><span data-stu-id="bec8b-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="bec8b-117">Popravljeno: nepravilna logika privzetih nastavitev preprečuje oddajo stroškov.</span><span class="sxs-lookup"><span data-stu-id="bec8b-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="bec8b-118">Popravljeno: če odobritev časovnega vnosa ne uspe, odobritev ostane v stanju **V teku**.</span><span class="sxs-lookup"><span data-stu-id="bec8b-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="bec8b-119">Popravljeno: napake strežnika SQL pri množičnih odobritvah (zamuda/časovna omejitev).</span><span class="sxs-lookup"><span data-stu-id="bec8b-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="bec8b-120">Popravljeno: večje težave z uporabniško izkušnjo, ki jih povzroči posodabljanje članov ekipe pri odobravanju časovnih vnosov.</span><span class="sxs-lookup"><span data-stu-id="bec8b-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="bec8b-121">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="bec8b-121">**Project Management**</span></span>

- <span data-ttu-id="bec8b-122">Popravljeno: obvestilo o časovnem pasu se je premaknilo s pogleda **Uskladitev** na glavni obrazec **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="bec8b-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="bec8b-123">Popravljeno: predloga koledarja nima pravilnih privzetih nastavitev, ko se odpre nov obrazec projekta.</span><span class="sxs-lookup"><span data-stu-id="bec8b-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="bec8b-124">Popravljeno: uporabniki brskalnikov, ki temeljijo na programski opremi Chromium, ne morejo preprosto izbrati predhodnih opravil za izbris.</span><span class="sxs-lookup"><span data-stu-id="bec8b-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="bec8b-125">Popravljeno: ustvarjanje ali kopiranje **projekta iz prazne predloge** pridobi nepovezane dodelitve.</span><span class="sxs-lookup"><span data-stu-id="bec8b-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="bec8b-126">Popravljeno: v določenih robnih primerih se pri ustvarjanju nove naloge iz mreže opravil ustvarijo podvojeni zapisi.</span><span class="sxs-lookup"><span data-stu-id="bec8b-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="bec8b-127">Popravljeno: v ročnem načinu uporabniki ne morejo spremeniti začetnih datumov opravil na poznejše od trenutno shranjenega datuma.</span><span class="sxs-lookup"><span data-stu-id="bec8b-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="bec8b-128">**Upravljanje virov**</span><span class="sxs-lookup"><span data-stu-id="bec8b-128">**Resource Management**</span></span>

- <span data-ttu-id="bec8b-129">Popravljeno: v pogled **Uskladitev** vrstica delne vsote napačno izračuna razlike pri rezervacijah po podaljšanju rezervacij.</span><span class="sxs-lookup"><span data-stu-id="bec8b-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="bec8b-130">Popravljeno: pogled **Uskladitev** napačno prikaže dodelitve virov, ko ima vir, ki ga je mogoče rezervirati, koledar, ki se ne ujema s koledarjem projekta.</span><span class="sxs-lookup"><span data-stu-id="bec8b-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="bec8b-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="bec8b-131">**Sales**</span></span>

- <span data-ttu-id="bec8b-132">Opravljeno: ko so časovni vnosi ponovno odobreni ( **Odobri > Prekliči >** ponovno odobri), se ustvari podvojeni dejanski znesek, ki se ne zaračuna.</span><span class="sxs-lookup"><span data-stu-id="bec8b-132">Fixed: When time entries are re-approved ( **Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
