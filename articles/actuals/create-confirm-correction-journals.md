---
title: Ustvarjanje in potrjevanje dnevnikov popravkov
description: Ta tema vsebuje informacije o tem, kako ustvariti in potrditi dnevnik popravkov.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896976"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="da609-103">Ustvarjanje in potrjevanje dnevnikov popravkov</span><span class="sxs-lookup"><span data-stu-id="da609-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="da609-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="da609-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="da609-105">Občasno je vnos za čas ali strošek vnesen napačno.</span><span class="sxs-lookup"><span data-stu-id="da609-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="da609-106">Svetovalec lahko na primer pri ustvarjanju časovnega vnosa izbere napačen datum ali pa prenese številke pri vnosu stroška.</span><span class="sxs-lookup"><span data-stu-id="da609-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="da609-107">Če svetovalec ne more posodobiti poslanih vnosov, lahko skrbnik neposredno popravi vnos za projekt.</span><span class="sxs-lookup"><span data-stu-id="da609-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="da609-108">Za dokončanje postopkov v tej temi boste potrebovali skrbniška dovoljenja.</span><span class="sxs-lookup"><span data-stu-id="da609-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="da609-109">Popravek odobrenih časovnih vnosov</span><span class="sxs-lookup"><span data-stu-id="da609-109">Correct approved time entries</span></span>     

<span data-ttu-id="da609-110">Za popravljanje posameznega ali več časovnih vnosov za projekt izvedite naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="da609-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="da609-111">V območju **Prodaja** izberite **Transakcije** in nato izberite **Odobren čas**.</span><span class="sxs-lookup"><span data-stu-id="da609-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="da609-112">Na seznamu **Odobren čas** poiščite in izberite enega ali več odobrenih časovnih vnosov, ki jih želite popraviti.</span><span class="sxs-lookup"><span data-stu-id="da609-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="da609-113">S filtrom lahko poiščete povezane vnose.</span><span class="sxs-lookup"><span data-stu-id="da609-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="da609-114">filtrirate lahko na primer po ID-ju projekta in izberete vse odobrene časovne vnose s tem ID-jem projekta.</span><span class="sxs-lookup"><span data-stu-id="da609-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="da609-115">Izberite **Popravi vnose**.</span><span class="sxs-lookup"><span data-stu-id="da609-115">Select **Correct entries**.</span></span> <span data-ttu-id="da609-116">Samodejno se ustvari nov dnevnik popravkov z dodeljeno vrsto **Popravek časa**.</span><span class="sxs-lookup"><span data-stu-id="da609-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="da609-117">Vnosi, ki ste jih izbrali, so dodani v dnevnik.</span><span class="sxs-lookup"><span data-stu-id="da609-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="da609-118">Na strani **Novi dnevnik** vnesite **Opis** za svoj dnevnik za popravke in nato izberite zavihek **Popravki časovnih vnosov**.</span><span class="sxs-lookup"><span data-stu-id="da609-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="da609-119">V razdelku **Nove vrednosti za časovne vnose** po potrebi posodobite polja s pravilnimi informacijami.</span><span class="sxs-lookup"><span data-stu-id="da609-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="da609-120">Lahko na primer spremenite dodeljeni projekt ali vir, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="da609-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="da609-121">Izberite **Predogled**.</span><span class="sxs-lookup"><span data-stu-id="da609-121">Select **Preview**.</span></span> <span data-ttu-id="da609-122">V pogovornem oknu izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="da609-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="da609-123">Na zavihku **Vrstice dnevnika** si lahko ogledate seznam prvotnih dejanskih vrednosti, povezanih z izbranimi časovnimi vnosi, ki so bili razveljavljani, ter popravljene ustrezne vrstice, ki so bile ustvarjene.</span><span class="sxs-lookup"><span data-stu-id="da609-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="da609-124">Če je treba izvesti dodatne popravke, ponovite 5. in 6. korak.</span><span class="sxs-lookup"><span data-stu-id="da609-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="da609-125">Vse popravljene dejanske vrednosti bodo imele iste vrednosti, kot ste jih izbrali v razdelku **Nove vrednosti za časovne vnose**.</span><span class="sxs-lookup"><span data-stu-id="da609-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="da609-126">Če se popravki prikažejo po pričakovanjih, izberite **Potrdi**.</span><span class="sxs-lookup"><span data-stu-id="da609-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="da609-127">V pogovornem oknu izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="da609-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="da609-128">Vrnite se na območje **Prodaja**, izberite **Projekti** in nato odprite projekt, za katerega ste pravkar posodobili časovne vnose.</span><span class="sxs-lookup"><span data-stu-id="da609-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="da609-129">Na strani **Projekti** v zavihku **Opravljeno delo** si oglejte spremembe, ki ste jih izvedli.</span><span class="sxs-lookup"><span data-stu-id="da609-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="da609-130">Če zavihek **Opravljeno delo** ni viden, izberite **Povezano** > **Opravljeno delo**.</span><span class="sxs-lookup"><span data-stu-id="da609-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="da609-131">Na seznamu **Povezani pogled za opravljeno delo** lahko vidite, da so prvotni časovni vnosi, ki so bili razveljavljeni, še vedno navedeni, navedeni pa so tudi ustrezni popravljeni časovni vnosi.</span><span class="sxs-lookup"><span data-stu-id="da609-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="da609-132">Na naslednji grafiki sta na primer dve vrstični postavki s količino 8,00, ki imata bremena, navedena v stolpcu »Znesek«.</span><span class="sxs-lookup"><span data-stu-id="da609-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="da609-133">Poleg tega sta v stolpcu »Znesek« prikazani dve vrstici s količino –8,00, ki prikazujeta znesek, knjižen v dobro.</span><span class="sxs-lookup"><span data-stu-id="da609-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="da609-134">S temi popravki se količina zmanjša na nič.</span><span class="sxs-lookup"><span data-stu-id="da609-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="da609-135">Popravek odobrenih vnosov stroškov</span><span class="sxs-lookup"><span data-stu-id="da609-135">Correct approved expense entries</span></span>

<span data-ttu-id="da609-136">Za popravljanje enega ali več vnosov stroškov opravite naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="da609-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="da609-137">V območju **Prodaja** v levem podoknu za krmarjenje pri možnosti **Transakcije** izberite **Odobreni stroški**.</span><span class="sxs-lookup"><span data-stu-id="da609-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="da609-138">Na seznamu **Odobreni stroški** izberite projekt, ki ga želite popraviti, nato pa izberite **Popravi vnose**.</span><span class="sxs-lookup"><span data-stu-id="da609-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="da609-139">Novi dnevnik popravkov bo ustvarjen samodejno z dodeljeno vrsto **Popravek stroška**.</span><span class="sxs-lookup"><span data-stu-id="da609-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="da609-140">Na strani **Novi dnevnik** vnesite **Opis** za popravek in na zavihku **Popravek stroška** v razdelku **Nove vrednosti za stroške** izberite podatkovna polja, ki jih želite popraviti za izbrane vrstice stroškov.</span><span class="sxs-lookup"><span data-stu-id="da609-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="da609-141">Strošek lahko na primer dodelite za drug **Projekt** ali popravite možnosti **Kategorija stroška**, **Datum stroška** ali **Vir, ki ga je mogoče rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="da609-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="da609-142">Izberite **Predogled**.</span><span class="sxs-lookup"><span data-stu-id="da609-142">Select **Preview**.</span></span> <span data-ttu-id="da609-143">V pogovornem oknu izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="da609-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="da609-144">Na zavihku **Vrstice dnevnika** preverite popravke. Lahko si ogledate seznam prvotnih dejanskih vrednosti, povezanih z izbranimi vnosi stroškov, ki so bili razveljavljani, ter popravljene ustrezne vrstice, ki so bile ustvarjene.</span><span class="sxs-lookup"><span data-stu-id="da609-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="da609-145">Če so popravljene vrednosti v skladu s pričakovanji, izberite **Potrdi**.</span><span class="sxs-lookup"><span data-stu-id="da609-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="da609-146">V pogovornem oknu izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="da609-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="da609-147">Če vrednosti niso prikazane v skladu s pričakovanji, izberite **Prekliči**, da se vrnete na seznam **Odobreni stroški**.</span><span class="sxs-lookup"><span data-stu-id="da609-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="da609-148">Ponovite korake od 2. do 5.</span><span class="sxs-lookup"><span data-stu-id="da609-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="da609-149">Popravljene dejanske vrednosti bodo imele iste vrednosti, kot ste jih izbrali v razdelku **Nove vrednosti za stroške**.</span><span class="sxs-lookup"><span data-stu-id="da609-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="da609-150">Ko potrdite dnevnik za popravke, se pomaknite nazaj do projekta ali projektov, ki ste jih posodobili, da si ogledate spremembe.</span><span class="sxs-lookup"><span data-stu-id="da609-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="da609-151">Na strani projekta, na zavihku **Opravljeno delo** preglejte **Povezani pogled za opravljeno delo**.</span><span class="sxs-lookup"><span data-stu-id="da609-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="da609-152">Izvirni vnosi in popravljeni vnosi so navedeni.</span><span class="sxs-lookup"><span data-stu-id="da609-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="da609-153">Naslednji grafični prikaz prikazuje izvirne zneske za vnos stroška in ustrezne popravljene zneske za vnos stroška.</span><span class="sxs-lookup"><span data-stu-id="da609-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


