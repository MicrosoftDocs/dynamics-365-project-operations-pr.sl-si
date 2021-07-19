---
title: Ročna uvedba aplikacije Project Operations Dataverse s podporo za dvojno zapisovanje
description: Ta tema vsebuje informacije o tem, kako ročno uvesti aplikacijo Project Operations Dataverse tako, da bo podpirala dvojno zapisovanje.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274028"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="e71bd-103">Ročna uvedba aplikacije Project Operations Dataverse s podporo za dvojno zapisovanje</span><span class="sxs-lookup"><span data-stu-id="e71bd-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="e71bd-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_</span><span class="sxs-lookup"><span data-stu-id="e71bd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e71bd-105">Ta tema vsebuje informacije o tem, kako aplikacijo Microsoft Dynamics 365 Project Operations ročno uvesti v storitev Microsoft Dataverse tako, da bo podpirala dvojno zapisovanje.</span><span class="sxs-lookup"><span data-stu-id="e71bd-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="e71bd-106">Če so izpolnjene določene zahteve, Aplikacija Project Operations zazna konfiguracijo okolja in nudi dodatno podporo za dvojno zapisovanje.</span><span class="sxs-lookup"><span data-stu-id="e71bd-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="e71bd-107">Če ste sledili navodilom v tej temi, lahko med uvajanjem prek Microsoft Dynamics Lifecycle Services (LCS) preskočite uvajanje integracije Microsoft Power Platform (pred tem poznane kot okolje storitve Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="e71bd-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="e71bd-108">Postopek uvajanja aplikacije Project Operations v Dataverse z omogočeno podporo za dvojno zapisovanje je sestavljen iz štirih korakov:</span><span class="sxs-lookup"><span data-stu-id="e71bd-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="e71bd-109">[Ustvarjenje novega okolja v storitvi Dataverse s podporo za dvojno zapisovanje](#create).</span><span class="sxs-lookup"><span data-stu-id="e71bd-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="e71bd-110">[Dodajanje pogojev za dvojno zapisovanje v okolje](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="e71bd-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="e71bd-111">[Dodajanje aplikacije Project Operations v storitvi Dataverse](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="e71bd-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="e71bd-112">[Povezava okolij](#link).</span><span class="sxs-lookup"><span data-stu-id="e71bd-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="e71bd-113">Ustvarjenje novega okolja v storitvi Dataverse s podporo za dvojno zapisovanje</span><span class="sxs-lookup"><span data-stu-id="e71bd-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="e71bd-114">Če želite zaključiti postopek, se morate vpisati kot skrbnik.</span><span class="sxs-lookup"><span data-stu-id="e71bd-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="e71bd-115">Odprite [skrbniško središče Power Platform](https://admin.powerplatform.com) in se vpišite kot skrbnik.</span><span class="sxs-lookup"><span data-stu-id="e71bd-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="e71bd-116">Ustvarite novo okolje in ga poimenujte.</span><span class="sxs-lookup"><span data-stu-id="e71bd-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="e71bd-117">Izberite vrsto okolja.</span><span class="sxs-lookup"><span data-stu-id="e71bd-117">Select the environment type.</span></span> <span data-ttu-id="e71bd-118">Če ste se prijavili za preskusno različico, izberite **Preskusna različica (na podlagi naročnine)**.</span><span class="sxs-lookup"><span data-stu-id="e71bd-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="e71bd-119">Potrdite območje uvajanja.</span><span class="sxs-lookup"><span data-stu-id="e71bd-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="e71bd-120">Omogočite možnost **Ustvarjenje zbirke podatkov za to okolje**.</span><span class="sxs-lookup"><span data-stu-id="e71bd-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="e71bd-121">Potrdite jezik ter potrdite, da se valuta ujema z valuto aplikacije Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e71bd-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="e71bd-122">Omogočite možnost **Aplikacije Dynamics 365** in potrdite, da je polje **Samodejno uvedi te aplikacije** nastavljeno na **Brez**.</span><span class="sxs-lookup"><span data-stu-id="e71bd-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="e71bd-123">Dodajte varnostno skupino, če je to zahtevano.</span><span class="sxs-lookup"><span data-stu-id="e71bd-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="e71bd-124">Izberite **Shrani**, da ustvarite okolje.</span><span class="sxs-lookup"><span data-stu-id="e71bd-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="e71bd-125">Počakajte, da se uvajanje zaključi in da okolje vstopi v stanje **Pripravljeno**.</span><span class="sxs-lookup"><span data-stu-id="e71bd-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="e71bd-126">Dodajanje pogojev za dvojno zapisovanje v okolje</span><span class="sxs-lookup"><span data-stu-id="e71bd-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="e71bd-127">Podpora za dvojno zapisovanje vsebuje dodatna polja, dodana ključnim entitetam, kot je entiteta **Podjetje**.</span><span class="sxs-lookup"><span data-stu-id="e71bd-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="e71bd-128">Če podporo za dvojno zapisovanje vključujete v obstoječe okolje, bo za to, da jo omogočite, morda potrebna posodobitev podatkov.</span><span class="sxs-lookup"><span data-stu-id="e71bd-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="e71bd-129">Za informacije o tem, kako uporabiti metodo ponovnega vzorčenja podatkov, si oglejte možnost [Uporaba metode ponovnega vzorčenja podatkov podjetja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="e71bd-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="e71bd-130">Za več informacij o dvojnem zapisovanju si oglejte [Sistemske zahteve za dvojno zapisovanje](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="e71bd-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="e71bd-131">Zaključite postopek dodajanja pogojev za dvojno zapisovanje v okolje.</span><span class="sxs-lookup"><span data-stu-id="e71bd-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="e71bd-132">Odprite okolje, ki ste ga ustvarili, in pojdite v razdelek **Viri** \> **Aplikacija Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="e71bd-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="e71bd-133">Na seznamu aplikacije izberite možnost **Osnovna rešitev za dvojno zapisovanje** in jo namestite.</span><span class="sxs-lookup"><span data-stu-id="e71bd-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="e71bd-134">Počakajte, da se namestitev zaključi.</span><span class="sxs-lookup"><span data-stu-id="e71bd-134">Wait until the installation is completed.</span></span> <span data-ttu-id="e71bd-135">Nato na seznamu aplikacije izberite možnost **Rešitev za organiziranje aplikacije za dvojno zapisovanje** in jo namestite.</span><span class="sxs-lookup"><span data-stu-id="e71bd-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="e71bd-136">Dodajanje aplikacije Project Operations v storitvi Dataverse</span><span class="sxs-lookup"><span data-stu-id="e71bd-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="e71bd-137">Ta postopek lahko zaključite samo, če ste zaključili prejšnje postopke, še preden ste namestili aplikacijo Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e71bd-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="e71bd-138">Med namestitvijo sistem analizira konfiguracijo okolja in doda podporo za dvojno zapisovanje, če je to zahtevano.</span><span class="sxs-lookup"><span data-stu-id="e71bd-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="e71bd-139">Odprite okolje, ki ste ga ustvarili, in pojdite v razdelek **Viri** \> **Aplikacija Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="e71bd-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="e71bd-140">Na seznamu aplikacije izberite **Microsoft Dynamics 365 Project Operations** in ga namestite.</span><span class="sxs-lookup"><span data-stu-id="e71bd-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="e71bd-141">Povezava okolij</span><span class="sxs-lookup"><span data-stu-id="e71bd-141">Link your environments</span></span>

<span data-ttu-id="e71bd-142">Ko je okolje Dataverse uvedeno, lahko v aplikaciji Finance and Operations nastavite povezavo.</span><span class="sxs-lookup"><span data-stu-id="e71bd-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="e71bd-143">Upoštevajte korake v razdelku [Uporaba čarovnika za dvojno zapisovanje z namenom povezave okolij](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="e71bd-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
