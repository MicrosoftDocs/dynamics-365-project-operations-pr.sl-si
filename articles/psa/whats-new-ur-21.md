---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 21, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 21.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: ad44f6747486222cc1f48c7b645f2525d382dca3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949069"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="c257b-103">Izdaja posodobitve 21 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="c257b-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c257b-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c257b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c257b-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="c257b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c257b-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c257b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c257b-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="c257b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c257b-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c257b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c257b-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 21.</span><span class="sxs-lookup"><span data-stu-id="c257b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="c257b-110">Številka graditve te različice je V3.10.32.50 in je na splošno na voljo prek samostojne posodobitve junija 2020.</span><span class="sxs-lookup"><span data-stu-id="c257b-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="c257b-111">Izdaja posodobitve 21</span><span class="sxs-lookup"><span data-stu-id="c257b-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c257b-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="c257b-112">Bug fixes</span></span>

<span data-ttu-id="c257b-113">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="c257b-113">**Time and Expense**</span></span>

<span data-ttu-id="c257b-114">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="c257b-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c257b-115">Ko gostite **Nadzor mreže časovnih vnosov** na nadzornih ploščah, mreža ne uporablja celotne širine vsebnika nadzorne plošče.</span><span class="sxs-lookup"><span data-stu-id="c257b-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="c257b-116">Za določene časovne pasove **Nadzor mreže časovnih vnosov** ne prikazuje zapisov.</span><span class="sxs-lookup"><span data-stu-id="c257b-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="c257b-117">Časovni vnosi po 21. uri se prikažejo na napačen dan.</span><span class="sxs-lookup"><span data-stu-id="c257b-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="c257b-118">Če stroškovna kategorija **Zahtevano potrdilo o prejemu stroškov** nima vrednosti, uporabniki ne morejo poslati stroškov.</span><span class="sxs-lookup"><span data-stu-id="c257b-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="c257b-119">**Upravljanje virov**</span><span class="sxs-lookup"><span data-stu-id="c257b-119">**Resource Management**</span></span>

<span data-ttu-id="c257b-120">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="c257b-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="c257b-121">Neaktivne rezervacije so prikazane v pogledu **Uskladitev**.</span><span class="sxs-lookup"><span data-stu-id="c257b-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="c257b-122">Za dopolnitev splošnega vira je manjkala potrditev, da bi zagotovili veljaven status rezervacije.</span><span class="sxs-lookup"><span data-stu-id="c257b-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="c257b-123">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="c257b-123">**Project Management**</span></span>

<span data-ttu-id="c257b-124">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="c257b-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="c257b-125">Mreže obrazca **Projekt** (**Dodelitev vira**, **Opravilo**, **Pogled** Uskladitev, **Ocene stroškov**) je mogoče urejati, tudi ko projekt ni aktiven.</span><span class="sxs-lookup"><span data-stu-id="c257b-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="c257b-126">Podvojenih strank ni mogoče združiti s strankami, ki so povezane s potrjenimi pogodbami projekta.</span><span class="sxs-lookup"><span data-stu-id="c257b-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="c257b-127">Ko je dodan vir, ki nima veljavnega koledarja, se v sistemu ne prikaže uporabniku prijazno sporočilo o napaki.</span><span class="sxs-lookup"><span data-stu-id="c257b-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="c257b-128">Gumb **Dodaj opravilo** na mreži opravil je omogočen, ko je projekt povezan z dodatkom za **Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="c257b-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="c257b-129">Obseg dela raste nenadzorovano, ko je naloga s kategorijo dodeljena viru z vlogo, za katero je določena stroškovna cena.</span><span class="sxs-lookup"><span data-stu-id="c257b-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="c257b-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="c257b-130">**Sales**</span></span>

<span data-ttu-id="c257b-131">Uvedene izboljšave:</span><span class="sxs-lookup"><span data-stu-id="c257b-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="c257b-132">Vrstici **Pogostost izdajanja računov** in **Začetni datum obračunavanja** sta bili premaknjeni v zavihek **Razpored izdajanja računov**.</span><span class="sxs-lookup"><span data-stu-id="c257b-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="c257b-133">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="c257b-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="c257b-134">**Skupna prodajna cena** je enaka nič (0) za **Kategorijo** čeprav ima **Vloga** skupno prodajno ceno, ki ni enaka nič.</span><span class="sxs-lookup"><span data-stu-id="c257b-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="c257b-135">Ko drug prilagojen postopek posodablja dodatno polje, stranke ne morejo spremeniti vrednosti polja **Stanje računa** na polje **Pripravljeno za izdajo računa**.</span><span class="sxs-lookup"><span data-stu-id="c257b-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="c257b-136">Gumb **Osvežitev transakcij vrstice računa** lahko ob večkratni izbiri ustvari več podvojenih vrstic.</span><span class="sxs-lookup"><span data-stu-id="c257b-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="c257b-137">Gumb **Posodobi cene** ne deluje v obrazcu **Hiter pogled** v podmreži **Cene vlog**.</span><span class="sxs-lookup"><span data-stu-id="c257b-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="c257b-138">Logika **Razrešitve prodajnega cenika** nepravilno obdeluje časovne pasove, zaradi česar je izbor cenikov napačen.</span><span class="sxs-lookup"><span data-stu-id="c257b-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="c257b-139">**Skupni dejanski stroški** projekta imajo lahko delno napako po odobritvi enkratnega vnosa.</span><span class="sxs-lookup"><span data-stu-id="c257b-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="c257b-140">Znotraj logike **Razrešitve cen** se ne prikaže uporabniku prijazno sporočilo o napaki, če razdelek **Pridobljena cena vloge** nima vrednosti v poljih **Glavna enota** in **Cena v osnovni enoti**.</span><span class="sxs-lookup"><span data-stu-id="c257b-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]