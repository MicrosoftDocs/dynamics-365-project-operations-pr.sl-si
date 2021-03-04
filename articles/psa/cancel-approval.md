---
title: Preklic odobrenih časovnih vnosov in vnosov stroškov
description: V tej temi najdete informacije o tem, kako prekličete potrjen čas projekta in transakcijo stroškov.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
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
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150598"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="4b54f-103">Preklic odobrenih časovnih vnosov ali vnosov stroškov</span><span class="sxs-lookup"><span data-stu-id="4b54f-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4b54f-104">V najnovejši različici rešitvi Dynamics 365 Project Service Automation lahko odobritelji prekličejo časovne vnose ali vnose stroškov, ki so jih predhodno odobrili.</span><span class="sxs-lookup"><span data-stu-id="4b54f-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="4b54f-105">Preklic predhodno potrjenega časovnega vnosa ali vnosa stroškov</span><span class="sxs-lookup"><span data-stu-id="4b54f-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="4b54f-106">Če želite preklicati že odobren časovni vnos ali vnos stroškov, sledite spodnjim korakom.</span><span class="sxs-lookup"><span data-stu-id="4b54f-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="4b54f-107">Odprite **Projekti** \> **Moje delo** \> **Odobritve**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="4b54f-108">Na strani s seznamom **Odobritve** spremenite pogled na **Moje pretekle odobritve**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="4b54f-109">Prikaže se seznam časovnih vnosov in vnosov stroškov, ki ste jih odobrili.</span><span class="sxs-lookup"><span data-stu-id="4b54f-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="4b54f-110">Izberite enega ali več vnosov in nato **Prekliči odobritev**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="4b54f-111">Prikaže se opozorilo.</span><span class="sxs-lookup"><span data-stu-id="4b54f-111">You receive a warning message.</span></span>
4. <span data-ttu-id="4b54f-112">Če želite preklicati odobritev, izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="4b54f-113">Razumevanje vpliva preklica odobritve časovnega vnosa ali vnosa stroškov</span><span class="sxs-lookup"><span data-stu-id="4b54f-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="4b54f-114">Preklic odobritve ima operativni in finančni učinek.</span><span class="sxs-lookup"><span data-stu-id="4b54f-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="4b54f-115">Operativni učinek</span><span class="sxs-lookup"><span data-stu-id="4b54f-115">Operational impact</span></span>

<span data-ttu-id="4b54f-116">Ko je odobritev preklicana, se stanje zapisa ponastavi na **Osnutek** in odobritev ni več prikazana v pogledu **Moje pretekle odobritve**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="4b54f-117">Namesto tega je preklicana odobritev prikazana v pogledu **Časovni vnosi za odobritev** ali **Vnosi stroškov za odobritev**, odvisno od tega, ali je šlo za časovni vnos ali vnos stroškov.</span><span class="sxs-lookup"><span data-stu-id="4b54f-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="4b54f-118">Poleg tega se stanje povezanega vnosa časa ali stroškov spremeni v **Poslano**, tako da je povezan vnos skladen z odobritvami, ki imajo stanje **Osnutek**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="4b54f-119">Kot odobritelj lahko urejate nekatera polja odobritve s stanjem **Osnutek**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="4b54f-120">Med ta polja spadata **Vrsta obračunavanja** in **Ure za obračunavanje za vnose časa**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="4b54f-121">Ko naredite spremembe, lahko zapis znova odobrite.</span><span class="sxs-lookup"><span data-stu-id="4b54f-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="4b54f-122">Lahko pa tudi zavrnete vnos.</span><span class="sxs-lookup"><span data-stu-id="4b54f-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="4b54f-123">Če zavrnete odobritev časovnega vnosa, se stanje postavke spremeni v **Vrnjeno**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="4b54f-124">Če zavrnete odobritev vnosa stroškov, se stanje spremeni v **Zavrnjeno**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="4b54f-125">Vrnjeni in zavrnjeni vnosi delujejo enako kot vnos s stanjem **Osnutek**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="4b54f-126">Član projektne ekipe lahko naredi vse potrebne spremembe vnosa in ga nato znova predloži v odobritev ali v celoti izbriše vnos.</span><span class="sxs-lookup"><span data-stu-id="4b54f-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="4b54f-127">Finančni učinek</span><span class="sxs-lookup"><span data-stu-id="4b54f-127">Financial impact</span></span>

<span data-ttu-id="4b54f-128">Ko je odobritev preklicana, to tudi finančno vpliva na projekt.</span><span class="sxs-lookup"><span data-stu-id="4b54f-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="4b54f-129">Ustrezne dejanske vrednosti za stroške in prodajne cene se posodobijo tako:</span><span class="sxs-lookup"><span data-stu-id="4b54f-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="4b54f-130">Stanje prilagoditve je nastavljeno na **Prilagojeno**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="4b54f-131">Stanje obračunavanja je nastavljeno na **Preklicano**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="4b54f-132">Nato se v tabeli »Dejanske vrednosti« ustvarijo postavke storniranja.</span><span class="sxs-lookup"><span data-stu-id="4b54f-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="4b54f-133">Če želite ustvariti postavke storniranja, sistem prekopira vrednosti polj iz prvotnih dejanskih vrednosti.</span><span class="sxs-lookup"><span data-stu-id="4b54f-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="4b54f-134">Edine vrednosti, ki niso prekopirane, so vrednosti količin.</span><span class="sxs-lookup"><span data-stu-id="4b54f-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="4b54f-135">Te vrednosti se stornirajo.</span><span class="sxs-lookup"><span data-stu-id="4b54f-135">These values are reversed instead.</span></span> <span data-ttu-id="4b54f-136">Stornirane dejanske vrednosti se ustvarijo za dejanske vrednosti **Stroški** in **Neobračunana prodaja**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="4b54f-137">Polje **Stanje prilagoditve** za stornirane dejanske vrednosti je nastavljeno na **Ni mogoče prilagoditi**, stanje obračunavanja pa je nastavljeno na **Preklicano**.</span><span class="sxs-lookup"><span data-stu-id="4b54f-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="4b54f-138">Po teh spremembah se znesek, ki je zabeležen kot porabljen za projekt, in zaostali prihodki v projektu ne bodo več upoštevali pri zneskih, ki jih predstavljajo te dejanske vrednosti.</span><span class="sxs-lookup"><span data-stu-id="4b54f-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
