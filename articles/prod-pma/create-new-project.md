---
title: Ustvarite nov projekt
description: Ta tema vsebuje informacije o ustvarjanju novega projekta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084891"
---
# <a name="create-a-new-project"></a><span data-ttu-id="92ab1-103">Ustvarite nov projekt</span><span class="sxs-lookup"><span data-stu-id="92ab1-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92ab1-104">Dokončajte naslednje korake, da ustvarite nov projekt.</span><span class="sxs-lookup"><span data-stu-id="92ab1-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="92ab1-105">Na strani **Vodenje projektov** izberite **Nov projekt** , nato pa vnesite naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="92ab1-105">On the **Project management** page, select **New project** , and enter the following values:</span></span>

    - <span data-ttu-id="92ab1-106">**Vrsta projekta:** Čas in material</span><span class="sxs-lookup"><span data-stu-id="92ab1-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="92ab1-107">**Ime projekta:** 2. faza nadgradnje XYZ</span><span class="sxs-lookup"><span data-stu-id="92ab1-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="92ab1-108">**Projektna skupina:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="92ab1-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="92ab1-109">**ID projektne pogodbe:** 00000002</span><span class="sxs-lookup"><span data-stu-id="92ab1-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="92ab1-110">Izberite **Ustvarjanje projekta**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="92ab1-111">Dodeljevanje vira projektu</span><span class="sxs-lookup"><span data-stu-id="92ab1-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="92ab1-112">Na strani **Delavci** na seznamu **Delavci** izberite zapis za delavca, za katerega ste prej nastavili spodobnosti, in odprite zapis delavca.</span><span class="sxs-lookup"><span data-stu-id="92ab1-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="92ab1-113">V podoknu za dejanja na zavihku **Projekt** v skupini **Nastavitev** izberite **Dodelitve projektov**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="92ab1-114">Na strani **Dodelitve projekta potrjevanja vira** na zavihku **Projekti** v polju **Dodaj projekt v izbrane projekte** filtrirajte na projekt **2. faza nadgradnje XYZ**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="92ab1-115">V podoknu **Preostali projekti** izberite projekt in nato izberite gumb puščice, da ga dodate v podokno **Izbrani projekti**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="92ab1-116">Prav tako lahko dodelite kategorije za vir, kot je potrebno.</span><span class="sxs-lookup"><span data-stu-id="92ab1-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="92ab1-117">Vrsta kategorije je bodisi **Stroški** ali **Prihodki**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="92ab1-118">Vrsto kategorije določa vaša organizacija.</span><span class="sxs-lookup"><span data-stu-id="92ab1-118">The category type is determined by your organization.</span></span> <span data-ttu-id="92ab1-119">Če za vir ni dodeljene nobene kategorije, storitev Finance poišče privzeto kategorijo urnih cen stroškov in prihodkov.</span><span class="sxs-lookup"><span data-stu-id="92ab1-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="92ab1-120">Nastavitev vira projekta in značilnosti vloge</span><span class="sxs-lookup"><span data-stu-id="92ab1-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="92ab1-121">Projektni vodja lahko uporabi funkcionalnost iskanja virov za projekt, da ustvari vloge, ki so potrebne za projekt.</span><span class="sxs-lookup"><span data-stu-id="92ab1-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="92ab1-122">Vloge se lahko uporabijo, če so potrjeni viri še vedno neznani, ko se viri rezervirajo.</span><span class="sxs-lookup"><span data-stu-id="92ab1-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="92ab1-123">Vloge so lahko začasno rezervirane kot načrtovani viri, da lahko nadaljujete faze načrtovanja projekta.</span><span class="sxs-lookup"><span data-stu-id="92ab1-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="92ab1-124">[![Primer vloge](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="92ab1-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="92ab1-125">**Scenarij:** Podjetje Contoso je prejelo naročilo za izpolnitev časovnega in materialnega projekta, ki ima odobreno projektno listino.</span><span class="sxs-lookup"><span data-stu-id="92ab1-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="92ab1-126">Mlajši projektni vodja še vedno izpolnjuje obseg projekta.</span><span class="sxs-lookup"><span data-stu-id="92ab1-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="92ab1-127">Upravitelj virov trenutno prepoznava specifične vire, ki bodo rezervirani za delo na novem projektu.</span><span class="sxs-lookup"><span data-stu-id="92ab1-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="92ab1-128">Zaradi kritične narave projekta je sponzor projekta za eno od vlog zahteval višjega projektnega vodjo.</span><span class="sxs-lookup"><span data-stu-id="92ab1-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="92ab1-129">Upravitelj virov mora pridobiti nov vir in določiti vlogo v sistemu, če mlajši projektni vodja med načrtovanjem projekta zahteva informacije o viru.</span><span class="sxs-lookup"><span data-stu-id="92ab1-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="92ab1-130">Naslednji koraki prikazujejo, kako lahko upravitelj virov nastavi vlogo višjega projektnega vodje in z njo poveže značilnosti vira.</span><span class="sxs-lookup"><span data-stu-id="92ab1-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="92ab1-131">Pozneje lahko vlogo uporabimo za iskanje razpoložljivih virov, ki se ujemajo z zahtevanimi sposobnostmi virov.</span><span class="sxs-lookup"><span data-stu-id="92ab1-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="92ab1-132">Na strani **Nastavitev vlog** izberite **Novo** , nato pa vnesite naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="92ab1-132">On the **Setup roles** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="92ab1-133">**ID vloge:** Višji projektni vodja</span><span class="sxs-lookup"><span data-stu-id="92ab1-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="92ab1-134">**Opis:** Višji projektni vodja</span><span class="sxs-lookup"><span data-stu-id="92ab1-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="92ab1-135">Izberite **Ustvari**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-135">Select **Create**.</span></span>
3. <span data-ttu-id="92ab1-136">Izberite vlogo **Višji projektni vodja** in nato izberite **Konfiguracija značilnosti**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="92ab1-137">V polju **Vrsta značilnosti** izberite **Znanje**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="92ab1-138">V polju **Razpoložljive značilnosti** vnesite znanje, po katerem se išče.</span><span class="sxs-lookup"><span data-stu-id="92ab1-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="92ab1-139">V polju **Vrsta značilnosti** izberite **Potrdilo**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="92ab1-140">V polju **Razpoložljive značilnosti** vnesite vrsto potrdila, po katerem se išče.</span><span class="sxs-lookup"><span data-stu-id="92ab1-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="92ab1-141">Dodeljevanje vira projekta projektu</span><span class="sxs-lookup"><span data-stu-id="92ab1-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="92ab1-142">Na strani **Vsi projekti** izberite projekt **2. faza nadgradnje XYZ**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="92ab1-143">Na zavihku **Projektna ekipa in načrtovanje** izberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="92ab1-144">V polju **Vloga** izberite **Član ekipe**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="92ab1-145">Izberite **Rezervacija iz koledarja**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="92ab1-146">Na strani **Razpoložljivost vira** izberite **Nastavitve pogleda**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="92ab1-147">Na strani **Prilagajanje nastavitev pogleda** vnesite naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="92ab1-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="92ab1-148">**Oblika za pogled datumskega obsega:** Dan</span><span class="sxs-lookup"><span data-stu-id="92ab1-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="92ab1-149">**Prikaz opisov razpoložljivosti:** Da</span><span class="sxs-lookup"><span data-stu-id="92ab1-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="92ab1-150">**Prikaz preostale zmogljivosti:** Da</span><span class="sxs-lookup"><span data-stu-id="92ab1-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="92ab1-151">Na seznamu virov izberite vir.</span><span class="sxs-lookup"><span data-stu-id="92ab1-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="92ab1-152">Izberite **Veljavna rezervacija** in **Polna zmogljivost**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="92ab1-153">Dodeljevanje vira privzeti vlogi</span><span class="sxs-lookup"><span data-stu-id="92ab1-153">Assign a resource to a default role</span></span>

<span data-ttu-id="92ab1-154">Kot pomoč lahko projektni vodje ali upravitelji virov prikažejo vire, ki jih je mogoče rezervirati za projekt, na ravni z več podrobnostmi.</span><span class="sxs-lookup"><span data-stu-id="92ab1-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="92ab1-155">Privzeto vlogo lahko povežete z obstoječim virom ali novo pridobljenim virom.</span><span class="sxs-lookup"><span data-stu-id="92ab1-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="92ab1-156">Na primer, Daniel je imel ob začetku sodelovanja izkušnje in znanja za zapolnitev vloge poslovnega analitika.</span><span class="sxs-lookup"><span data-stu-id="92ab1-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="92ab1-157">Upravitelj virov je to vlogo določil kot privzeto vlogo za Daniela.</span><span class="sxs-lookup"><span data-stu-id="92ab1-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="92ab1-158">Zato je upravitelj virov Daniela dodal v skupino poslovnih analitikov, ki so na voljo za delo na projektih.</span><span class="sxs-lookup"><span data-stu-id="92ab1-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="92ab1-159">Med rezervacijo virov lahko projektni vodje filtrirajo vire z vlogo, ki so na voljo za delo na projektih.</span><span class="sxs-lookup"><span data-stu-id="92ab1-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="92ab1-160">Te informacije lahko uporabijo kot eno merilo, kadar med zapolnitvijo virov izvajajo analizo odločitev z več merili.</span><span class="sxs-lookup"><span data-stu-id="92ab1-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="92ab1-161">V filter lahko dodajo tudi druge značilnosti virov za iskanje virov s posebnimi znanji, izobrazbo in izkušnjami za določen projekt.</span><span class="sxs-lookup"><span data-stu-id="92ab1-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="92ab1-162">**Scenarij:** Odobren projekt se je začel in vloga višjega projektnega vodje je bila rezervirana kot načrtovani vir v fazi načrtovanja projekta.</span><span class="sxs-lookup"><span data-stu-id="92ab1-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="92ab1-163">Upravitelj virov je zdaj pridobil vir za zapolnitev vloge višjega projektnega vodje.</span><span class="sxs-lookup"><span data-stu-id="92ab1-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="92ab1-164">Na strani **Seznam virov** izberite **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="92ab1-165">Na strani **Vloga vira** izberite **Novo** , nato pa vnesite naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="92ab1-165">On the **Resource role** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="92ab1-166">**Datum začetka veljavnosti:** Vnesite trenutni datum.</span><span class="sxs-lookup"><span data-stu-id="92ab1-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="92ab1-167">**Datum poteka:** Vnesite **Nikoli**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="92ab1-168">**Vloga:** Vnesite **Višji projektni vodja**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="92ab1-169">Izberite **Shrani** in nato zaprite stran.</span><span class="sxs-lookup"><span data-stu-id="92ab1-169">Select **Save** , and then close the page.</span></span>
4. <span data-ttu-id="92ab1-170">Na zavihku **Sposobnosti** dodajte znanje **Vodenje projektov** in potrdilo **PMP**.</span><span class="sxs-lookup"><span data-stu-id="92ab1-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
