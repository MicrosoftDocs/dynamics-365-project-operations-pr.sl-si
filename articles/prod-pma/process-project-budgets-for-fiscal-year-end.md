---
title: Prenos proračunov projektov ob koncu proračunskega leta
description: Ta članek vsebuje informacije o prenosu zneskov preostalega proračuna v prihodnja leta in ustvarjanju podrobnosti registra proračuna.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289749"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="f1dfa-103">Prenos proračunov projektov ob koncu proračunskega leta</span><span class="sxs-lookup"><span data-stu-id="f1dfa-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1dfa-104">Ko delate na večletnem projektu, vam bo morda ob koncu proračunskega leta ostalo nekaj proračunskih sredstev.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="f1dfa-105">Preostala proračunska sredstva lahko prenesete v prihodnje leto in ustvarite podrobnosti registra proračuna za zneske na povezanih računih glavne knjige.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="f1dfa-106">Preden prenesete preostale zneske, preglejte in analizirajte zneske preostalih proračunskih sredstev.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="f1dfa-107">Preglejte in analizirajte preostale zneske proračunskih sredstev</span><span class="sxs-lookup"><span data-stu-id="f1dfa-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="f1dfa-108">Opravite naslednje korake za pregled proračunskih sredstev ob koncu leta za projekte, vendar zneskov ne prenesite naprej.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="f1dfa-109">Odprite **Vodenje projektov in računovodstvo** > **Redno** > **Proračuni** > **Prenos proračunov**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="f1dfa-110">Na strani **Postopek prenosa proračuna projekta** na zavihku **Možnosti ob koncu leta** preverite, ali možnost **Prenesi preostala proračunska sredstva za projekt** ni omogočena.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="f1dfa-111">Na zavihku **Parametri** v polju **Proračunsko leto projekta** izberite proračunsko leto, za katero si želite ogledate znesek preostalih sredstev proračuna.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="f1dfa-112">V polje **Začetno proračunsko leto** izberite proračunsko leto, za katero si želite ogledate znesek preostalih sredstev proračuna.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="f1dfa-113">V polju **Od modela napovedi** izberite **Preostali proračun**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="f1dfa-114">Če želite vključiti projekte, ki ustrezajo izbranim merilom in za katere je bil porabljen ves proračun, izberite **Prikaži porabljene proračune**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="f1dfa-115">Na zavihku za **izbiro proračunov** izberite **Pridobi vse proračune**, da naložite vse proračune, ki ustrezajo izbranim merilom, in nato izberite **Obdelaj**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="f1dfa-116">Če želite oblikovati poizvedbo zbirke podatkov, ki v podokno naloži določen nabor proračunov, izberite **Pridobi izbrane proračune**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="f1dfa-117">Če želite več informacij o določeni vrstici v podoknu, izberite vrstico in nato izberite **Prikaži podrobnosti proračuna** ali **Prikaži račune**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="f1dfa-118">Prenos zneska preostalih proračunskih sredstev</span><span class="sxs-lookup"><span data-stu-id="f1dfa-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="f1dfa-119">Ko obdelate znesek preostalih proračunskih sredstev, lahko ustvarite transakcije v glavni knjigi za zneske, ki jih želite prenesti.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="f1dfa-120">Če želite ustvariti transakcije glavne knjige, opravite korake v razdelku [Prenos zneskov proračuna in ustvarjanje transakcij glavne knjige](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="f1dfa-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="f1dfa-121">Preneseni zneski proračuna se prenesejo v model napovedi, ki je izbran na strani **Modeli napovedi** kot model napovedi za prenos.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="f1dfa-122">Prenos zneskov proračuna in ustvarjanje transakcij glavne knjige</span><span class="sxs-lookup"><span data-stu-id="f1dfa-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="f1dfa-123">Izberite **Vodenje projektov in računovodstvo** > **Redno** > **Proračuni** > **Prenos proračunov**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="f1dfa-124">Na strani **Postopek prenosa proračuna projekta** izberite **Konec leta** in nato omogočite **Prenesi preostala proračunska sredstva za projekt** in **Ustvari vnose v register proračuna v glavni knjigi**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="f1dfa-125">Na zavihku **Parametri** pri skupini polj **Projektni parametri** izberite naslednje:</span><span class="sxs-lookup"><span data-stu-id="f1dfa-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="f1dfa-126">**Proračunsko leto projekta**: izberite začetek proračunskega leta, za katero si želite ogledate znesek preostalih sredstev proračuna.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="f1dfa-127">**Poslovni izid**: ustvarite transakcije poslovnega izida v glavni knjigi.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="f1dfa-128">**Postavka za nedokončano storitev**: ustvarite transakcije za nedokončane storitve (WIP) v glavni knjigi.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="f1dfa-129">**Plačilna lista**: v glavni knjigi ustvarite transakcije za dodelitev plače.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="f1dfa-130">V skupini polj **Glavna knjiga** navedite naslednje podatke:</span><span class="sxs-lookup"><span data-stu-id="f1dfa-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="f1dfa-131">V polje **Začetno proračunsko leto** izberite proračunsko leto, za katero želite prenesti znesek preostalih sredstev proračuna za projekte.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="f1dfa-132">Privzeta vrednost je eno leto po vrednosti v polju **Proračunsko leto projekta**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="f1dfa-133">V polju **Obdobje za prenos** izberite obdobje, za katero želite v glavni knjigi ustvariti podrobnosti registra proračuna.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="f1dfa-134">To je običajno prvo obdobje na začetnem proračunskem letu.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="f1dfa-135">V skupini polj **Kopiraj od/v** navedite naslednje podatke:</span><span class="sxs-lookup"><span data-stu-id="f1dfa-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="f1dfa-136">V polju **Od modela napovedi** izberite model napovedi za proračun projekta, povezan z zneski preostalega proračuna, ki jih želite prenesti za projekte.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="f1dfa-137">V polju **V model za proračun glavne knjige** izberite model za proračun glavne knjige, povezan z zneski proračuna, ki jih želite prenesti v glavno knjigo.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="f1dfa-138">Izberite **Prenesi valuto prodaje**, da prodajno valuto projekta uporabite za transakcije glavne knjige, ki se ustvarijo, ko prenesete zneske proračuna za projekte.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="f1dfa-139">Če možnost ni izbrana, transakcije uporabljajo računovodsko valuto.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="f1dfa-140">Izberite **Prikaži porabljene proračune**, da vključite projekte, za katere je bil porabljen že ves dodeljen proračun, vendar izpolnjujejo druga merila, ki ste jih izbrali pri projektih, prikazanih v spodnjem podoknu.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="f1dfa-141">Na zavihku za **izbiro proračunov** izberite **Pridobi vse proračune**, da naložite vse proračune, ki ustrezajo izbranim merilom.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="f1dfa-142">Če želite oblikovati poizvedbo zbirke podatkov, ki v podokno naloži določen nabor proračunov projektov, izberite **Pridobi izbrane proračune**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="f1dfa-143">Za vsak projekt, ki ga želite obdelati, izberite možnost na začetku vrstice za projekt.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="f1dfa-144">Če želite izbrati vse projekte ali večino od njih, izberite kljukico v zgornjem levem kotu.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="f1dfa-145">Če želite izključiti obdelavo katerega koli projekta, počistite kljukico za ta projekt.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="f1dfa-146">Če želite zneske preostalega proračuna za izbrane projekte prenesti na izbrano proračunsko leto in v glavni knjigi ustvariti podrobnosti registra proračuna, izberite **Obdelaj**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="f1dfa-147">Prenos zneskov proračuna brez ustvarjanja transakcij glavne knjige</span><span class="sxs-lookup"><span data-stu-id="f1dfa-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="f1dfa-148">Odprite **Vodenje projektov in računovodstvo** > **Redno** > **Proračuni** > **Prenos proračunov**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="f1dfa-149">Na strani **Postopek prenosa proračuna projekta** v polju **Možnosti ob koncu leta** izberite možnost **Prenesi preostala proračunska sredstva za projekt**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="f1dfa-150">V skupini **Parametri** v polju **Proračunsko leto projekta** izberite proračunsko leto, za katero si želite ogledate znesek preostalih sredstev proračuna.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="f1dfa-151">V skupini **Kopiraj od/v** navedite naslednje podatke:</span><span class="sxs-lookup"><span data-stu-id="f1dfa-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="f1dfa-152">V polju **Od modela napovedi** izberite model napovedi za proračun projekta, povezan z zneski preostalega proračuna, ki jih želite prenesti za projekte.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="f1dfa-153">Če želite vključiti projekte, za katere je bil porabljen ves proračun, vendar ustrezajo drugim izbranim merilom, izberite **Prikaži porabljene proračune**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="f1dfa-154">V skupini za **izbiro proračunov** izberite **Pridobi vse proračune**, da naložite vse proračune, ki ustrezajo izbranim merilom.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="f1dfa-155">Če želite oblikovati poizvedbo zbirke podatkov, ki v podokno naloži določen nabor proračunov projektov, izberite **Pridobi izbrane proračune**.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="f1dfa-156">Za vsak projekt, ki ga želite obdelati, izberite možnost na začetku vrstice za projekt.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="f1dfa-157">Izberite **Obdelaj** za prenos preostalih zneskov proračuna za izbrane projekte na izbrano proračunsko leto.</span><span class="sxs-lookup"><span data-stu-id="f1dfa-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]