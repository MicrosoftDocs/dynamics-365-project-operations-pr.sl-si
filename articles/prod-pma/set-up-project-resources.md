---
title: Nastavitev virov projekta
description: Ta tema vsebuje informacije o nastavitvi virov projekta ali pošiljanju zahtev za vire projekta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084928"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="c1fbf-103">Nastavitev virov projekta</span><span class="sxs-lookup"><span data-stu-id="c1fbf-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1fbf-104">Nastaviti morate koledar in ga povezati z zaposlenim ali delavcem.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="c1fbf-105">Koledar se uporablja za načrtovanje projekta in delovnega časa virov, ki so rezervirani za projekt.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="c1fbf-106">Med nastavitvijo koledarja lahko projektni vodje opravijo izravnavo virov kot del optimizacije virov.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="c1fbf-107">Na podlagi razporeda koledarja je mogoče uvesti omejitve za vire.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="c1fbf-108">Koledar lahko nastavite na strani **Koledarji**.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="c1fbf-109">Ko nastavljate delavca kot vir projekta, lahko izbirate med delavci, ki delajo v podjetju, za katero nastavljate vire.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="c1fbf-110">Lahko pa izberete delavce iz drugih podjetij v organizaciji.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="c1fbf-111">Ti delavci so znani kot medpodjetniški viri.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="c1fbf-112">Z naslednjimi postopki je pojasnjeno, kako nastavite delavca kot vir projekta v vašem podjetju in kako nastavite medpodjetniški vir projekta.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="c1fbf-113">Nastavitev delavca kot vir projekta</span><span class="sxs-lookup"><span data-stu-id="c1fbf-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="c1fbf-114">Na strani **Delavci** na seznamu **Delavci** izberite delavca, ki ga dodajate kot vir projekta, in odprite zapis delavca.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="c1fbf-115">V podoknu za dejanja izberite **Projekt** &gt; **Nastavitev** &gt; **Nastavitev projekta**.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="c1fbf-116">Izberite koledar in nato zaprite stran.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="c1fbf-117">Določite lahko tudi privzete projekte za vire kot vrsto preddodelitve.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="c1fbf-118">Preddodelitve je mogoče uporabiti, ko upravitelj virov ali projektni vodja vnaprej ve, na katerih projektih bo delal vir.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="c1fbf-119">Preddodelitve lahko temeljijo tudi na zahtevi sponzorja ali stranke projekta.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="c1fbf-120">Za preddodelitev projekta na strani **Dodelitve projektov** na zavihku **Projekti** v seznamu **Preostali projekti** izberite primeren projekt.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="c1fbf-121">Nastavitev medpodjetniškega vira</span><span class="sxs-lookup"><span data-stu-id="c1fbf-121">Set up an intercompany resource</span></span>

<span data-ttu-id="c1fbf-122">Ko nastavite delavca kot medpodjetniški vir, morate izvesti nastavitev v podjetju posojevalcu in podjetju izposojevalcu.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="c1fbf-123">V podjetju posojevalcu</span><span class="sxs-lookup"><span data-stu-id="c1fbf-123">In the lending company</span></span>

1. <span data-ttu-id="c1fbf-124">V storitvi Finance potrdite, da je izbrano podjetje posojevalec in nato izvedite postopke v prejšnjem razdelku »Nastavitev delavca kot vir projekta«.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="c1fbf-125">Na strani **Medpodjetniško računovodstvo** izberite možnost **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="c1fbf-126">V polju **ID pravne osebe** izberite podjetje posojevalca.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="c1fbf-127">Izpolnite preostala polja, kot je primerno, in nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="c1fbf-128">Na strani **Cena prenosa** izberite možnost **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="c1fbf-129">V polju **Pravna oseba izposojevalka** izberite ustrezno podjetje.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="c1fbf-130">Da bi podjetju izposojevalcu posodili samo vir, ki ste ga ustvarili na začetku tega razdelka, v polju **Vir** izberite ime vira, ki ste ga ustvarili.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="c1fbf-131">Da bi dali vse vire v podjetju posojevalcu na voljo podjetju izposojevalcu, pustite polje **Vir** prazno.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="c1fbf-132">Na strani **Vodenje projektov in računovodski parametri** na zavihku **Medpodjetniško** nastavite možnost **Omogoči medpodjetniško razporejanje virov in časovne liste** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="c1fbf-133">V podjetju izposojevalcu</span><span class="sxs-lookup"><span data-stu-id="c1fbf-133">In the borrowing company</span></span>

- <span data-ttu-id="c1fbf-134">Na strani **Seznam virov** v iskalni filter vnesite ime vira, ki ste ga ustvarili za podjetje posojevalca, da preverite, ali je ime vključeno na seznam virov za podjetje izposojevalca.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="c1fbf-135">Zahteva za vire projekta</span><span class="sxs-lookup"><span data-stu-id="c1fbf-135">Request project resources</span></span>
<span data-ttu-id="c1fbf-136">Funkcionalnost za razporejanje virov projekta samo upraviteljem virov omogoča razporejanje zaposlenih virov angažmajem ali projektom.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="c1fbf-137">Če želite omogočiti to funkcionalnost, dokončajte naslednja opravila ali potrdite, da so bila dokončana:</span><span class="sxs-lookup"><span data-stu-id="c1fbf-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="c1fbf-138">Nastavite zaporedja številk.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-138">Set up number sequences.</span></span>
- <span data-ttu-id="c1fbf-139">Nastavite poteke dela vodenja projektov in računovodstva.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="c1fbf-140">Omogočite poteke dela zahtev za vire.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-140">Enable resource request workflows.</span></span>

<span data-ttu-id="c1fbf-141">Ko so prejšnja opravila dokončana, lahko izvedete naslednja opravila, kot je potrebno:</span><span class="sxs-lookup"><span data-stu-id="c1fbf-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="c1fbf-142">Ustvarite zahtevo za vir iz začasno rezerviranega zaposlenega vira.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="c1fbf-143">Spremljajte zahteve za vire.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-143">Monitor resource requests.</span></span>
- <span data-ttu-id="c1fbf-144">Izpolnite zahteve za vire.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="c1fbf-145">Zahtevajte zaposleni vir iz SČD.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="c1fbf-146">Rezervirajte vire za projekt, ne da bi morali zahtevati zaposleni vir.</span><span class="sxs-lookup"><span data-stu-id="c1fbf-146">Book resources to a project without having a request for a staffed resource.</span></span>
