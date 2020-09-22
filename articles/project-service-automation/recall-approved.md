---
title: Preklic odobrenih časovnih vnosov ali vnosov stroškov
description: V tej temi najdete informacije o tem, kako prekličete predhodno potrjen čas ali transakcijo stroškov.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755878"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="9cff1-103">Preklic odobrenih časovnih vnosov ali vnosov stroškov</span><span class="sxs-lookup"><span data-stu-id="9cff1-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9cff1-104">Član projektne ekipe ali druga oseba, ki predloži vnos časa ali stroškov, lahko ta vnos po odobritvi prekliče.</span><span class="sxs-lookup"><span data-stu-id="9cff1-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="9cff1-105">Postopek za preklic odobrenega vnosa časa ali stroškov ima dva koraka:</span><span class="sxs-lookup"><span data-stu-id="9cff1-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="9cff1-106">Pošiljatelj zahteva preklic.</span><span class="sxs-lookup"><span data-stu-id="9cff1-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="9cff1-107">Odobritelj odobri preklic.</span><span class="sxs-lookup"><span data-stu-id="9cff1-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="9cff1-108">Zahteva za preklic</span><span class="sxs-lookup"><span data-stu-id="9cff1-108">Request a recall</span></span>

<span data-ttu-id="9cff1-109">Če želite zahtevati preklic odobrenega vnosa časa ali stroškov, sledite spodnjim korakom.</span><span class="sxs-lookup"><span data-stu-id="9cff1-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="9cff1-110">Za časovne vnose odprite **Projekti** \> **Moje delo** \> **Časovni vnos**.</span><span class="sxs-lookup"><span data-stu-id="9cff1-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="9cff1-111">–ali–</span><span class="sxs-lookup"><span data-stu-id="9cff1-111">–or–</span></span>

    <span data-ttu-id="9cff1-112">Za vnose stroškov odprite **Projekti** \> **Moje delo** \> **Stroški**.</span><span class="sxs-lookup"><span data-stu-id="9cff1-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="9cff1-113">Pri časovnih vnosih izberite vse časovne vnose za določeno kombinacijo projekta in opravila.</span><span class="sxs-lookup"><span data-stu-id="9cff1-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="9cff1-114">Druga možnost je, da v mreži izberete posamezne celice za čas na določen datum za določen projekt.</span><span class="sxs-lookup"><span data-stu-id="9cff1-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="9cff1-115">–ali–</span><span class="sxs-lookup"><span data-stu-id="9cff1-115">–or–</span></span>

    <span data-ttu-id="9cff1-116">Pri vnosih stroškov izberite vrstico za vnos stroškov, ki ga želite preklicati.</span><span class="sxs-lookup"><span data-stu-id="9cff1-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="9cff1-117">Izberite **Prekliči**.</span><span class="sxs-lookup"><span data-stu-id="9cff1-117">Select **Recall**.</span></span> <span data-ttu-id="9cff1-118">Prikaže se potrditveno pogovorno okno.</span><span class="sxs-lookup"><span data-stu-id="9cff1-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="9cff1-119">Če so bili izbrani vnosi časa in stroškov že odobreni, morate vnesti razlog za preklic.</span><span class="sxs-lookup"><span data-stu-id="9cff1-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="9cff1-120">Vnesite razlog za preklic in nato izberite **V redu**, da potrdite postopek.</span><span class="sxs-lookup"><span data-stu-id="9cff1-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="9cff1-121">Sistem pošlje osebi, ki je odobrila vnose, zahtevo za odobritev preklica.</span><span class="sxs-lookup"><span data-stu-id="9cff1-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="9cff1-122">Čeprav je odobrene vnose časa in stroškov mogoče preklicati, pa zahteve za preklic ni mogoče ustvariti, če je kupcu že zaračunan odobren čas ali strošek.</span><span class="sxs-lookup"><span data-stu-id="9cff1-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="9cff1-123">Uporabnik, ki poskuša ustvariti zahtevo za preklic, prejme sporočilo, v katerem je navedeno, da časa ali stroškov ni mogoče preklicati, ker je bil vnos že fakturiran.</span><span class="sxs-lookup"><span data-stu-id="9cff1-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="9cff1-124">Odobritev ali zavrnitev zahteve za preklic</span><span class="sxs-lookup"><span data-stu-id="9cff1-124">Approve or reject a recall request</span></span>

<span data-ttu-id="9cff1-125">Če želite odobriti ali zavrniti zahtevo za preklic, sledite spodnjim korakom.</span><span class="sxs-lookup"><span data-stu-id="9cff1-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="9cff1-126">Odprite **Projekti** \> **Moje delo** \> **Odobritve**.</span><span class="sxs-lookup"><span data-stu-id="9cff1-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="9cff1-127">Na strani s seznamom **Odobritve** spremenite pogled na **Zahteva za preklic za odobritev**.</span><span class="sxs-lookup"><span data-stu-id="9cff1-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="9cff1-128">Prikaže se seznam poslanih zahtev za preklic.</span><span class="sxs-lookup"><span data-stu-id="9cff1-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="9cff1-129">Izberite enega ali več vnosov in nato **Odobri** ali **Zavrni**.</span><span class="sxs-lookup"><span data-stu-id="9cff1-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="9cff1-130">Če ste izbrali **Odobri**, prejmete opozoril, ki pojasnjuje učinek odobritve.</span><span class="sxs-lookup"><span data-stu-id="9cff1-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="9cff1-131">Izberite **V redu**, da potrdite postopek.</span><span class="sxs-lookup"><span data-stu-id="9cff1-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="9cff1-132">Zahteva za preklic je odobrena.</span><span class="sxs-lookup"><span data-stu-id="9cff1-132">The recall request is approved.</span></span>

    <span data-ttu-id="9cff1-133">–ali–</span><span class="sxs-lookup"><span data-stu-id="9cff1-133">–or–</span></span>

    <span data-ttu-id="9cff1-134">Če ste izbrali **Zavrni**, je zahteva za preklic zavrnjena.</span><span class="sxs-lookup"><span data-stu-id="9cff1-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="9cff1-135">Tako kot pri zahtevi preklica tudi pri odobritvi preklica sistem v vnosih časa ali stroškov poišče dejavnosti fakturiranja.</span><span class="sxs-lookup"><span data-stu-id="9cff1-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="9cff1-136">Če je bil vnos že fakturiran ali če je v osnutku računa, bo odobritelj prejel sporočilo o napaki, v katerem je navedeno, da časa ali stroškov ni mogoče odobriti za preklic, ker je bil vnos že fakturiran.</span><span class="sxs-lookup"><span data-stu-id="9cff1-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="9cff1-137">Učinek zahteve za preklic</span><span class="sxs-lookup"><span data-stu-id="9cff1-137">Impact of a recall request</span></span>

<span data-ttu-id="9cff1-138">Preklic odobritve ima operativni in finančni učinek.</span><span class="sxs-lookup"><span data-stu-id="9cff1-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="9cff1-139">Operativni učinek</span><span class="sxs-lookup"><span data-stu-id="9cff1-139">Operational impact</span></span>

<span data-ttu-id="9cff1-140">Če je zahteva za preklic odobrena, je zapis odobritve označen kot **Zavrnjeno**.</span><span class="sxs-lookup"><span data-stu-id="9cff1-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="9cff1-141">Stanje vnosa se spremeni na **Vrnjeno** ali **Zavrnjeno**, odvisno od tega, ali gre za časovni vnos ali vnos stroškov.</span><span class="sxs-lookup"><span data-stu-id="9cff1-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="9cff1-142">Član projektne ekipe si lahko ogleda vnose, jih uredi in nato znova pošlje ali pa jih v celoti izbriše.</span><span class="sxs-lookup"><span data-stu-id="9cff1-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="9cff1-143">Če je zahteva za preklic zavrnjena, stanje vnosa ostane **Odobreno**, vnosa pa član projektne ekipe ali odobritelj v projektu ne more urejati.</span><span class="sxs-lookup"><span data-stu-id="9cff1-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="9cff1-144">Finančni učinek</span><span class="sxs-lookup"><span data-stu-id="9cff1-144">Financial impact</span></span>

<span data-ttu-id="9cff1-145">Če je zahteva za preklic odobrena, se ustrezne dejanske vrednosti za stroške in prodajne cene posodobijo tako:</span><span class="sxs-lookup"><span data-stu-id="9cff1-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="9cff1-146">Polje **Stanje prilagoditve** je posodobljeno na **Prilagojeno**.</span><span class="sxs-lookup"><span data-stu-id="9cff1-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="9cff1-147">Polje **Stanje obračunavanja** je posodobljeno na **Preklicano**.</span><span class="sxs-lookup"><span data-stu-id="9cff1-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="9cff1-148">Nato se v tabeli »Dejanske vrednosti« ustvarijo postavke storniranja.</span><span class="sxs-lookup"><span data-stu-id="9cff1-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="9cff1-149">Če želite ustvariti postavke storniranja, sistem prekopira vrednosti polj iz prvotnih dejanskih vrednosti.</span><span class="sxs-lookup"><span data-stu-id="9cff1-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="9cff1-150">Edine vrednosti, ki niso prekopirane, so vrednosti količin.</span><span class="sxs-lookup"><span data-stu-id="9cff1-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="9cff1-151">Te vrednosti se stornirajo.</span><span class="sxs-lookup"><span data-stu-id="9cff1-151">These values are reversed instead.</span></span> <span data-ttu-id="9cff1-152">Stornirane dejanske vrednosti se ustvarijo za dejanske vrednosti **Stroški** in **Neobračunana prodaja**.</span><span class="sxs-lookup"><span data-stu-id="9cff1-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="9cff1-153">Polje **Stanje prilagoditve** za stornirane dejanske vrednosti je nastavljeno na **Ni mogoče prilagoditi**, polje **Stanje obračunavanja** pa na **Preklicano**.</span><span class="sxs-lookup"><span data-stu-id="9cff1-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="9cff1-154">Zaradi teh sprememb se zabeleženi stroški in zaostali prihodki v projektu ne bodo več upoštevali pri zneskih, ki jih predstavljajo te dejanske vrednosti.</span><span class="sxs-lookup"><span data-stu-id="9cff1-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="9cff1-155">Če je zahteva za preklic zavrnjena, ni finančnega vpliva na projekt.</span><span class="sxs-lookup"><span data-stu-id="9cff1-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="9cff1-156">Spremembe zapisov časovnega vnosa</span><span class="sxs-lookup"><span data-stu-id="9cff1-156">Changes to time entry records</span></span>

<span data-ttu-id="9cff1-157">Spodnja slika prikazuje spremembe, do katerih pride pri odobrenih časovnih vnosih, ko so ti preklicani.</span><span class="sxs-lookup"><span data-stu-id="9cff1-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Prehodi stanja časovnega vnosa](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="9cff1-159">Spremembe zapisov vnosa stroškov</span><span class="sxs-lookup"><span data-stu-id="9cff1-159">Changes to expense entry records</span></span>

<span data-ttu-id="9cff1-160">Spodnja slika prikazuje spremembe, do katerih pride pri odobrenih vnosih stroškov, ko so ti preklicani.</span><span class="sxs-lookup"><span data-stu-id="9cff1-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Prehodi stanja vnosa stroškov](media/ExpenseEntryStateTransitions.png)
