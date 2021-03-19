---
title: Integracija odjemalca Microsoft Project
description: Načrtovanje in vzdrževanje projektnega razporeda je lahko zapleteno, zato morajo vodje projektov uporabljati orodja, ki jim pomagajo pri izpolnjevanju te naloge. Integracija z odjemalcem Microsoft Project Client nudi podporo za odpiranje in upravljanje strukturirane členitve projektnega dela.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289344"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="ecf9d-104">Integracija odjemalca Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="ecf9d-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecf9d-105">Načrtovanje in vzdrževanje projektnega razporeda je lahko zapleteno, zato morajo vodje projektov uporabljati orodja, ki jim pomagajo pri izpolnjevanju te naloge.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="ecf9d-106">Integracija z odjemalcem Microsoft Project Client nudi podporo za odpiranje in upravljanje strukturirane členitve projektnega dela.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="ecf9d-107">Vodja projekta lahko objavi vse spremembe nazaj v strukturirano členitev projektnega dela rešitve Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="ecf9d-108">Če uporabljate julijsko posodobitev (različica 10.0.4), morate namestiti KB 4054797 in 4055884.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="ecf9d-109">Konfiguracija dodatka odjemalca Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="ecf9d-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="ecf9d-110">Če želite omogočiti integracijo z odjemalcem Microsoft Project Client, morate namestiti dodatek Microsoft Dynamics 365 v uporabnikovo odjemalsko aplikacijo Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="ecf9d-111">To naredite tako, da odprete **Delovni prostor za upravljanje projektov**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="ecf9d-112">•   Kliknite **Konfiguriraj dodatek odjemalca projekta** v razdelku **Povezave** > **Nastavitev** delovnega prostora.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="ecf9d-113">•   Kliknite **Odpri** in ob pozivu še **Zaženi**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="ecf9d-114">Odpiranje in urejevanje obstoječega osnutka strukturirane členitve dela v odjemalcu Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="ecf9d-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="ecf9d-115">Če ima projekt v rešitvi Dynamics 365 Finance že ustvarjeno strukturirano členitev dela, lahko strukturirano členitev dela odprete v aplikaciji Microsoft Project Client, kadar je ta v stanju osnutka.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="ecf9d-116">Če želite to možnost odpreti na strani **Projekt**, kliknite povezavo **Odpri v odjemalcu Microsoft Project** na zavihku **Načrt**. To stran lahko odprete tudi v aplikaciji Microsoft Project Client s klikom **Odpri** na zavihku **Microsoft Dynamics 365**. Na seznamu izberite možnost **Pravna oseba** in **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="ecf9d-117">Če uporabljate Internet Explorer za svoj brskalnik, boste morali klikniti **Shrani**, da boste lahko datoteko ročno odprli iz mesta, kamor je prenesena.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="ecf9d-118">Ali pa kliknite **Shrani in odpri**, da odprete datoteko v odjemalcu Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="ecf9d-119">Ne preimenujte datoteke med shranjevanjem.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="ecf9d-120">Pred kakršnim koli urejanjem datoteke s pomočjo odjemalca Microsoft Project Client, jo morate najprej preveriti. Kliknite **Preveri** na zavihku **Microsoft Dynamics 365**. S tem boste drugim uporabnikom preprečili, da bi hkrati urejali strukturirano členitev dela znotraj rešitve Finance.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="ecf9d-121">Če želite po končanih popravkih objaviti strukturirano členitev dela, kliknite **Prijava** na zavihku **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="ecf9d-122">Če je bila projektna skupina že dodana projektu v rešitvi Finance, se seznam virov zapolni s člani skupine.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="ecf9d-123">Če projektna skupina še ni dodana projektu, lahko izberete vire in sestavite skupino znotraj odjemalca Microsoft Project Client, tako da kliknete gumb **Viri** na zavihku **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="ecf9d-124">Spodaj navedeni podatki se bodo v okviru postopka prijave sinhronizirali nazaj v program Finance:</span><span class="sxs-lookup"><span data-stu-id="ecf9d-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="ecf9d-125">•   Naziv opravila</span><span class="sxs-lookup"><span data-stu-id="ecf9d-125">•   Task name</span></span>

<span data-ttu-id="ecf9d-126">•   Datum začetka</span><span class="sxs-lookup"><span data-stu-id="ecf9d-126">•   Start date</span></span>

<span data-ttu-id="ecf9d-127">•   Datum zaključka</span><span class="sxs-lookup"><span data-stu-id="ecf9d-127">•   Finish date</span></span>

<span data-ttu-id="ecf9d-128">•   Predhodniki</span><span class="sxs-lookup"><span data-stu-id="ecf9d-128">•   Predecessors</span></span>

<span data-ttu-id="ecf9d-129">•   Imena virov</span><span class="sxs-lookup"><span data-stu-id="ecf9d-129">•   Resource names</span></span>

<span data-ttu-id="ecf9d-130">•   Kategorija</span><span class="sxs-lookup"><span data-stu-id="ecf9d-130">•   Category</span></span>

<span data-ttu-id="ecf9d-131">•   Kategorija vira</span><span class="sxs-lookup"><span data-stu-id="ecf9d-131">•   Resource category</span></span>

<span data-ttu-id="ecf9d-132">•   Delovni čas</span><span class="sxs-lookup"><span data-stu-id="ecf9d-132">•   Work hours</span></span>

<span data-ttu-id="ecf9d-133">•   Beležke</span><span class="sxs-lookup"><span data-stu-id="ecf9d-133">•   Notes</span></span>

<span data-ttu-id="ecf9d-134">•   Prednost</span><span class="sxs-lookup"><span data-stu-id="ecf9d-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="ecf9d-135">Če v datoteko odjemalca Microsoft Project Client dodate druge stolpce, se ti ne bodo shranili v datoteko in ne bodo prikazani ob ponovnem odpiranju datoteke.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="ecf9d-136">Ustvarjanje strukturirane členitve dela za obstoječi projekt z odjemalcem Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="ecf9d-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="ecf9d-137">Če želite ustvariti novo strukturirano členitev dela z odjemalcem Microsoft Project Client, sledite spodaj navedenim korakom:</span><span class="sxs-lookup"><span data-stu-id="ecf9d-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="ecf9d-138">Odprite odjemalca Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="ecf9d-139">Na zavihku **Microsoft Dynamics 365** kliknite **Odpri**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="ecf9d-140">Izberite možnost **Pravna oseba** za projekt.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="ecf9d-141">Izberite **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="ecf9d-142">Kliknite **Ogled** na zavihku **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="ecf9d-143">Ko ste pripravljeni na objavo v rešitvi Finance, kliknite **Prijava** na zavihku **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="ecf9d-144">Zamenjava obstoječe strukturirane členitve dela za obstoječi projekt z odjemalcem Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="ecf9d-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="ecf9d-145">Če želite ustvariti novo strukturirano členitev dela z odjemalcem Microsoft Project Client in zamenjati obstoječo strukturirano členitev dela za obstoječi projekt, sledite tem korakom:</span><span class="sxs-lookup"><span data-stu-id="ecf9d-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="ecf9d-146">Odprite odjemalca Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="ecf9d-147">Ustvarite razpored v odjemalcu Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="ecf9d-148">Na zavihku **Microsoft Dynamics 365** kliknite **Shrani spremembe** > **Zamenjaj obstoječi projekt**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="ecf9d-149">Izberite možnost **Pravna oseba** za projekt.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="ecf9d-150">Izberite **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="ecf9d-151">Kliknite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="ecf9d-152">Ustvarite nov projekt v odjemalcu Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="ecf9d-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="ecf9d-153">Odprite odjemalca Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="ecf9d-154">Ustvarite razpored v odjemalcu Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="ecf9d-155">Na zavihku **Microsoft Dynamics 365** kliknite **Shrani spremembe** > **Shrani v nov projekt**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="ecf9d-156">Izberite možnost **Pravna oseba** za projekt.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="ecf9d-157">Po potrebi vnesite **ID projekta**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="ecf9d-158">Vnesite **Ime projekta**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="ecf9d-159">Izberite **Vrsto projekta**, **Projektno skupino** in **ID projektne pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="ecf9d-160">Lahko pa kliknete možnost **Novo** in ustvarite novo projektno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="ecf9d-161">Izberite **Koledar**, ki ga želite uporabiti za vire.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="ecf9d-162">Kliknite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="ecf9d-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]