---
title: Nadgradnja domače strani
description: Ta tema vsebuje informacije o tem, kje najdete pomembne informacije o novih in spremenjenih funkcijah aplikacije Dynamics 365 Project Service Automation, in o postopku za nadgradnjo na najnovejšo različico.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fa25d069de8098c0e8788c9ebb8aa3426eec5db9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121778"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="99e31-103">Nadgradnja domače strani</span><span class="sxs-lookup"><span data-stu-id="99e31-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="99e31-104">Nadgradnja storitve PSA, različice 2.x ali 1.x, na različico 3.x</span><span class="sxs-lookup"><span data-stu-id="99e31-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="99e31-105">Novi primerki</span><span class="sxs-lookup"><span data-stu-id="99e31-105">New instances</span></span>

<span data-ttu-id="99e31-106">Od 17. maja 2019, ko je bila rešitev Project Service Automation izbrana med pripravo novega primerka, se različica 3.x privzeto namesti.</span><span class="sxs-lookup"><span data-stu-id="99e31-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="99e31-107">Obstoječi primerki</span><span class="sxs-lookup"><span data-stu-id="99e31-107">Existing instances</span></span>

<span data-ttu-id="99e31-108">V prejšnjih različicah so se morale stranke, ki imajo primerek PSA različice 2.x in ga morajo nadgraditi na različico 3.x, tj. različica PSA na podlagi poenotenega vmesnika odjemalca (UCI), obrniti na Microsoftovo podporo in podati podrobnosti o njihovem primerku, da lahko podpora omogoči primerek za nadgradnjo na različico 3.x.</span><span class="sxs-lookup"><span data-stu-id="99e31-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="99e31-109">Od 1. marca 2020 bodo stranke, ki imajo primerek PSA različice 2.x in ga morajo nadgraditi na različico 3.x, lahko svoje primerke nadgradile neposredno s skrbniškega portala, ne da bi se morale obrniti na Microsoftovo podporo.</span><span class="sxs-lookup"><span data-stu-id="99e31-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="99e31-110">PSA različice 3.x vključuje pomembne spremembe.</span><span class="sxs-lookup"><span data-stu-id="99e31-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="99e31-111">Zgrajen je bil na osnovi ogrodja poenotenega vmesnika, da bi pomagal zagotoviti izboljšano uporabniško izkušnjo.</span><span class="sxs-lookup"><span data-stu-id="99e31-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="99e31-112">Na novo zasnovana aplikacija zagotavlja skladen in enoten uporabniški vmesnik (UI), ki sledi odzivnim načelom oblikovanja za optimalen prikaz na zaslonu poljubne velikosti ali kateri koli napravi.</span><span class="sxs-lookup"><span data-stu-id="99e31-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="99e31-113">V aplikaciji se je izvedlo še veliko drugih sprememb.</span><span class="sxs-lookup"><span data-stu-id="99e31-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="99e31-114">Spremenila so se nekatera področja, na primer za oblikovanje cen, opravljanje rezervacij ter dodeljevanje virov, časa, stroškov in odobritev.</span><span class="sxs-lookup"><span data-stu-id="99e31-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="99e31-115">Priporočamo vam, da pred izvedbo postopka za nadgradnjo izvedete naslednja opravila:</span><span class="sxs-lookup"><span data-stu-id="99e31-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="99e31-116">Preverite, ali sta v identificiranem primerku nameščeni tako Dynamics 365 Field Service kot Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="99e31-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="99e31-117">Če sta nameščeni obe rešitvi, ju najprej nadgradite in šele nato nadaljujete z običajno uporabo primerka.</span><span class="sxs-lookup"><span data-stu-id="99e31-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="99e31-118">Pozorno preglejte naslednje teme.</span><span class="sxs-lookup"><span data-stu-id="99e31-118">Carefully review the following topics.</span></span> <span data-ttu-id="99e31-119">Seznanjenje in razumevanje sprememb med različicami vam bo pomagalo pri postopku nadgradnje.</span><span class="sxs-lookup"><span data-stu-id="99e31-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="99e31-120">Te teme zagotavljajo informacije o večjih spremembah v PSA, skupaj z nasveti in priporočili za načrtovanje nadgradnje na različico 3.x.</span><span class="sxs-lookup"><span data-stu-id="99e31-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="99e31-121">Novosti ali spremembe v storitvi Project Service Automation različice 3</span><span class="sxs-lookup"><span data-stu-id="99e31-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="99e31-122">Vidiki nadgradnje – nadgradnja storitve Project Service Automation različice 2.x ali 1.x na različico 3</span><span class="sxs-lookup"><span data-stu-id="99e31-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="99e31-123">Nadgradite različico za preizkusno okolje, da ocenite spremembe v uvedbi, preden nadgradite produkcijski primerek.</span><span class="sxs-lookup"><span data-stu-id="99e31-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="99e31-124">Ko boste pregledali zgoraj omenjene teme in boste pripravljeni na nadgradnjo na PSA različice 3.x ali različico na podlagi UCI, pošljite zahtevo Microsoftovi podpori, da bo ta omogočila nadgradnjo v skrbniškem središču.</span><span class="sxs-lookup"><span data-stu-id="99e31-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="99e31-125">Vaša zahteva naj vsebuje tudi podrobnosti vašega primerka.</span><span class="sxs-lookup"><span data-stu-id="99e31-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="99e31-126">Starejše različice PSA (PSA različice 2.x) v novo ustvarjenem primerku</span><span class="sxs-lookup"><span data-stu-id="99e31-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="99e31-127">Od 17. maja 2019 bodo imeli vsi novi primerki privzetega odjemalca v obliki UCI.</span><span class="sxs-lookup"><span data-stu-id="99e31-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="99e31-128">Za prilagoditev na to spremembo bosta privzeto omogočeni PSA različice 3.x in Field Service različice 8.x, saj sta ti različici zasnovani za delo z odjemalcem UCI.</span><span class="sxs-lookup"><span data-stu-id="99e31-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="99e31-129">Od 1. marca 2020 stranke, ki uporabljajo Dynamics PSA, ne bodo več mogle ustvarjati novih okolij s starejšimi različicami PSA, na primer PSA različice 2.x ali starejšimi.</span><span class="sxs-lookup"><span data-stu-id="99e31-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="99e31-130">Vsako novo okolje bo razpoložljivo samo v različici PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="99e31-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="99e31-131">Za najboljšo izkušnjo pri uporabi starejših različic storitev Field Service in PSA, pojdite na stran **Sistemske nastavitve** in v polju **Uporabi samo nov poenoteni vmesnik (priporočeno)** izberite **Ne**, saj te različice niso zasnovane tako, da bi jih lahko pravilno naložili v UCI.</span><span class="sxs-lookup"><span data-stu-id="99e31-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="99e31-132">Po izklopu UCI lahko odprete in zaženete te različice rešitev Field Service in PSA prek starega spletnega odjemalca.</span><span class="sxs-lookup"><span data-stu-id="99e31-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
