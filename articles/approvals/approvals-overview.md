---
title: Pregled odobritev
description: Ta tema vsebuje informacije o delu z odobritvami v aplikaciji Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 5e30b8a386805faee869f77e695d5ee492d78cdb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996721"
---
# <a name="approvals-overview"></a><span data-ttu-id="ea631-103">Pregled odobritev</span><span class="sxs-lookup"><span data-stu-id="ea631-103">Approvals overview</span></span>

<span data-ttu-id="ea631-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="ea631-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ea631-105">Predlogi za čas, stroške in uporabo materiala grejo skozi potek odobritve.</span><span class="sxs-lookup"><span data-stu-id="ea631-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="ea631-106">Po odobritvi vnosov se transakcije zabeležijo v dejanske vrednosti ali pa se v urnik vpiše čas.</span><span class="sxs-lookup"><span data-stu-id="ea631-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="ea631-107">Potek dela za odobritve</span><span class="sxs-lookup"><span data-stu-id="ea631-107">Approvals workflow</span></span>
<span data-ttu-id="ea631-108">Ko ustvarite in oddate vnos za čas, stroške ali porabo materiala, se ustvari odobritveni zapis.</span><span class="sxs-lookup"><span data-stu-id="ea631-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="ea631-109">Odobritelj ali upravitelj projekta pregleda in odobri vnos.</span><span class="sxs-lookup"><span data-stu-id="ea631-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="ea631-110">Če je vnos povezan s projektom, bodo dejanski podatki ustvarjeni, ko bo ta odobren.</span><span class="sxs-lookup"><span data-stu-id="ea631-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="ea631-111">To omogoča sledenje stroškom in obračunom.</span><span class="sxs-lookup"><span data-stu-id="ea631-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="ea631-112">Odobritev vnosa</span><span class="sxs-lookup"><span data-stu-id="ea631-112">Approve an entry</span></span>
<span data-ttu-id="ea631-113">Stran **Odobritve** vam omogoča preklop med različnimi pogledi, tako da si lahko ogledate različne vrste odobritev.</span><span class="sxs-lookup"><span data-stu-id="ea631-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="ea631-114">Pojdite na stran **Odobritve** in izberite možnost **Stroški**, **Čas**, **Uporaba materiala**, ali **Preklici**.</span><span class="sxs-lookup"><span data-stu-id="ea631-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="ea631-115">Preglejte vsako odobritev in izberite tiste, ki jih želite odobriti.</span><span class="sxs-lookup"><span data-stu-id="ea631-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="ea631-116">Izberite možnost **Odobri** za odobritev izbranih vnosov.</span><span class="sxs-lookup"><span data-stu-id="ea631-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="ea631-117">Sistem te vnose obdela in ustvari dejanske vrednosti.</span><span class="sxs-lookup"><span data-stu-id="ea631-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="ea631-118">Zavrnitev vnosa</span><span class="sxs-lookup"><span data-stu-id="ea631-118">Reject an entry</span></span>
<span data-ttu-id="ea631-119">Kot odobritelj projekta boste morda morali uporabniku poslati vnos v popravek.</span><span class="sxs-lookup"><span data-stu-id="ea631-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="ea631-120">Pojdite na stran **Odobritve** in izberite vnos, ki ga želite zavrniti.</span><span class="sxs-lookup"><span data-stu-id="ea631-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="ea631-121">Izberite možnost **Zavrni**.</span><span class="sxs-lookup"><span data-stu-id="ea631-121">Select **Reject**.</span></span>
3. <span data-ttu-id="ea631-122">Po želji dodajte komentar v pogovornem oknu za **Komentar ob zavrnitvi**, ki uporabnika obvesti, zakaj je vnos zavrnjen.</span><span class="sxs-lookup"><span data-stu-id="ea631-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="ea631-123">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="ea631-123">Select **OK**.</span></span> <span data-ttu-id="ea631-124">Vnos bo vrnjen uporabniku.</span><span class="sxs-lookup"><span data-stu-id="ea631-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="ea631-125">Preklic odobritve</span><span class="sxs-lookup"><span data-stu-id="ea631-125">Cancel approval</span></span>
<span data-ttu-id="ea631-126">V nekaterih primerih boste morda morali preklicati predhodno odobren vnos.</span><span class="sxs-lookup"><span data-stu-id="ea631-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="ea631-127">Preklic predhodno odobrenega vnosa bo imel finančni učinek.</span><span class="sxs-lookup"><span data-stu-id="ea631-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="ea631-128">Odobritev zahtev za preklic</span><span class="sxs-lookup"><span data-stu-id="ea631-128">Approving recall requests</span></span>
<span data-ttu-id="ea631-129">V nekaterih primerih bo svetovalec morda moral preklicati predhodno odobren vnos.</span><span class="sxs-lookup"><span data-stu-id="ea631-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="ea631-130">Preklic predhodno odobrenega vnosa bo imel finančni učinek.</span><span class="sxs-lookup"><span data-stu-id="ea631-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="ea631-131">Odobritelj projekta mora odobriti preklic za razveljavitev transakcije v dejanskih vrednostih.</span><span class="sxs-lookup"><span data-stu-id="ea631-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="ea631-132">Določitev odobriteljev projekta</span><span class="sxs-lookup"><span data-stu-id="ea631-132">Specify Project approvers</span></span>
<span data-ttu-id="ea631-133">Vsak projekt ima več članov projektne skupine.</span><span class="sxs-lookup"><span data-stu-id="ea631-133">Each project has a number of project team members.</span></span> <span data-ttu-id="ea631-134">Določite lahko, kdo od članov ekipe je tudi odobritelj projekta.</span><span class="sxs-lookup"><span data-stu-id="ea631-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="ea631-135">Pojdite na stran **Projekti** in odprite projekt s seznama.</span><span class="sxs-lookup"><span data-stu-id="ea631-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="ea631-136">Na zavihku **Ekipa** izberite člana ekipe, ki bo odobritelj projekta, in nato izberite možnost **Uredi**.</span><span class="sxs-lookup"><span data-stu-id="ea631-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="ea631-137">Polje **Odobritelj projekta** nastavite na možnost **Da**.</span><span class="sxs-lookup"><span data-stu-id="ea631-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="ea631-138">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="ea631-138">Select **Save**.</span></span>
5. <span data-ttu-id="ea631-139">Ponovite drugi, tretji in četrti korak, da dodate dodatne odobritelje projekta.</span><span class="sxs-lookup"><span data-stu-id="ea631-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="ea631-140">Konfiguracija upravitelja izbranega uporabnika</span><span class="sxs-lookup"><span data-stu-id="ea631-140">Configure the user's manager</span></span>

1. <span data-ttu-id="ea631-141">Odprite **Nastavitve** > **Varnost** > **Uporabniki**.</span><span class="sxs-lookup"><span data-stu-id="ea631-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="ea631-142">Izberite uporabnika, ki mu želite dodeliti upravitelja, in v območju **Podatki o organizaciji** s seznama izberite upravitelja.</span><span class="sxs-lookup"><span data-stu-id="ea631-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="ea631-143">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="ea631-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
