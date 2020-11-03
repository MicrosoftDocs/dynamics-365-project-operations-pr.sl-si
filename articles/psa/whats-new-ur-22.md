---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 22, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 22.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084704"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="4c085-103">Izdaja posodobitve 22 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="4c085-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="4c085-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4c085-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4c085-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="4c085-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4c085-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4c085-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4c085-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="4c085-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4c085-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4c085-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4c085-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 22.</span><span class="sxs-lookup"><span data-stu-id="4c085-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="4c085-110">Številka graditve te različice je V3.10.33.48 in je na splošno na voljo prek samostojne posodobitve junija 2020.</span><span class="sxs-lookup"><span data-stu-id="4c085-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="4c085-111">Izdaja posodobitve 22</span><span class="sxs-lookup"><span data-stu-id="4c085-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4c085-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="4c085-112">Bug fixes</span></span>



<span data-ttu-id="4c085-113">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="4c085-113">**Time and Expense**</span></span>

<span data-ttu-id="4c085-114">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="4c085-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="4c085-115">**Časovni vnosi** po uvozu niso samodejno dodani v urnik časovnih vnosov.</span><span class="sxs-lookup"><span data-stu-id="4c085-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="4c085-116">Mrežni izbirnik datuma **Časovni vnos** ne prepozna uporabnikovih področnih nastavitev.</span><span class="sxs-lookup"><span data-stu-id="4c085-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="4c085-117">**Upravljanje virov**</span><span class="sxs-lookup"><span data-stu-id="4c085-117">**Resource Management**</span></span>

<span data-ttu-id="4c085-118">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="4c085-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="4c085-119">V ročnem načinu se spremembe obrisov v razdelku **Dodelitev vira** ne prepoznajo, ko gre za ustvarjanje zahtev v razdelku **Zahteve za vir**.</span><span class="sxs-lookup"><span data-stu-id="4c085-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="4c085-120">V razdelku **Zahteve za vir** statusi zahtev po meri niso podprti.</span><span class="sxs-lookup"><span data-stu-id="4c085-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="4c085-121">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="4c085-121">**Project Management**</span></span>

<span data-ttu-id="4c085-122">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="4c085-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="4c085-123">Z dvoklikom možnosti EstimateGridControl ne dobite pravilne razčlembe številk nizozemskega zapisa.</span><span class="sxs-lookup"><span data-stu-id="4c085-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="4c085-124">Dodeljene ure se ne posodabljajo pravilno, ko se dodeljena opravila spreminja z dodatkom za namizni odjemalec Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="4c085-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="4c085-125">V omrežjih za sledenje in ocene projektov je prikazana napačna koda prodajne valute, kadar je pogodbena valuta drugačna od valute stranke in če je organizacija nameščena za prikaz valutnih kod namesto simbolov valut.</span><span class="sxs-lookup"><span data-stu-id="4c085-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="4c085-126">Končnemu datumu člana ekipe je dodan en dan, če delovni urnik traja 24 ur na dan.</span><span class="sxs-lookup"><span data-stu-id="4c085-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="4c085-127">V časovnici projektov dodajanje kategorije transakcije v opravilo ne sproži samodejnega shranjevanja.</span><span class="sxs-lookup"><span data-stu-id="4c085-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="4c085-128">Pri dodajanju člana ekipe v predlogo projekta se prikaže naslednja napaka: »Zahteve po virih je nemogoče povezati s predlogami projekta«.</span><span class="sxs-lookup"><span data-stu-id="4c085-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="4c085-129">Skript pravilnika traku "msdyn.Approval.CanApproveOrReject" prikaže napako časovne omejitve.</span><span class="sxs-lookup"><span data-stu-id="4c085-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="4c085-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="4c085-130">**Sales**</span></span>

<span data-ttu-id="4c085-131">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="4c085-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="4c085-132">Sporočilo o napaki se ne prikaže, ko je v iskalnem polju cenika izbran stroškovni cenik v razdelku »Cenik nove ponudbe projekta«.</span><span class="sxs-lookup"><span data-stu-id="4c085-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="4c085-133">Zapiranje ponudbe, kot da je pridobljena, ne povzroči premika do ustvarjene pogodbe, če je BPF, priložen ponudbi, v zaključni fazi.</span><span class="sxs-lookup"><span data-stu-id="4c085-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="4c085-134">Storniranje vnosov v razdelku **Neobračunana prodaja** je povezano z izvirnimi stroški ob odpoklicu časovnega vnosa.</span><span class="sxs-lookup"><span data-stu-id="4c085-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="4c085-135">Po izbiri gumba **Potrdi** se stanje računa ne spremeni v **Potrjeno** , razen če je račun osvežen.</span><span class="sxs-lookup"><span data-stu-id="4c085-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
