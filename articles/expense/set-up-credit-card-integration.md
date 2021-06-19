---
title: Nastavitev integracije kreditne kartice
description: Ta tema razlaga, kako delati s transakcijami s kreditnimi karticami, povezanimi s stroški.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001850"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="1292c-103">Nastavitev integracije kreditne kartice</span><span class="sxs-lookup"><span data-stu-id="1292c-103">Set up credit card integration</span></span>

<span data-ttu-id="1292c-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="1292c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1292c-105">Transakcije s kreditnimi karticami, povezane s stroški, lahko nastavite tako, da se samodejno uvozijo po ponavljajočem se urniku.</span><span class="sxs-lookup"><span data-stu-id="1292c-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="1292c-106">Lahko pa transakcije uvozite tudi ročno, kot so potrebne.</span><span class="sxs-lookup"><span data-stu-id="1292c-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="1292c-107">Transakcije s kreditnimi karticami se uvažajo prek podatkovne entitete za transakcije s kreditnimi karticami.</span><span class="sxs-lookup"><span data-stu-id="1292c-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="1292c-108">Uvoz transakcij s kreditnimi karticami</span><span class="sxs-lookup"><span data-stu-id="1292c-108">Import credit card transactions</span></span>

<span data-ttu-id="1292c-109">Če želite uvoziti transakcije s kreditno kartico, sledite tem korakom:</span><span class="sxs-lookup"><span data-stu-id="1292c-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="1292c-110">Na strani **Transakcije s kreditnimi karticami** izberite **Uvoz transakcij**.</span><span class="sxs-lookup"><span data-stu-id="1292c-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="1292c-111">Če prvič odpirate upravljanje podatkov, mora sistem posodobiti seznam podatkovnih entitet, preden lahko nadaljujete.</span><span class="sxs-lookup"><span data-stu-id="1292c-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="1292c-112">V polje **Ime** vnesite edinstven opis za uvozno opravilo.</span><span class="sxs-lookup"><span data-stu-id="1292c-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="1292c-113">V polju **Izvorna oblika zapisa podatkov** izberite obliko zapisa datoteke, ki vsebuje transakcije s kreditno kartico za uvoz.</span><span class="sxs-lookup"><span data-stu-id="1292c-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="1292c-114">Izberite **Naloži**, nato pa poiščite in izberite datoteko za uvoz.</span><span class="sxs-lookup"><span data-stu-id="1292c-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="1292c-115">Ko je datoteka naložena, preverite preslikavo datoteke transakcij s kreditnimi karticami in stolpce podatkovne entitete transakcij s kreditnimi karticami, tako da izberete povezavo **Prikaz zemljevida** na ploščici.</span><span class="sxs-lookup"><span data-stu-id="1292c-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="1292c-116">Če obstajajo napake pri preslikavi ali če morate spremeniti preslikavo, naredite spremembe preslikave bodisi iz zavihka **Upodobitev preslikave** ali zavihka **Podrobnosti preslikave**.</span><span class="sxs-lookup"><span data-stu-id="1292c-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="1292c-117">Za avtomatizacijo transakcij s kreditnimi karticami izberite **Ustvari ponavljajoči se podatkovni posel**.</span><span class="sxs-lookup"><span data-stu-id="1292c-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="1292c-118">Nato lahko nastavite ponavljanje, ki opredeljuje, kako pogosto naj se transakcije s kreditnimi karticami uvozijo.</span><span class="sxs-lookup"><span data-stu-id="1292c-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="1292c-119">Ko končate, izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="1292c-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="1292c-120">Če želite izbrano datoteko uvoziti zdaj, izberite **Uvozi**.</span><span class="sxs-lookup"><span data-stu-id="1292c-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="1292c-121">Če med uvozom pride do napak, si lahko ogledate dnevnik izvajanja ali podatke za pripravljanje, da vidite napake, ki jih morate popraviti, da zagotovite uspešen uvoz.</span><span class="sxs-lookup"><span data-stu-id="1292c-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="1292c-122">Če morate uvoziti več oblik zapisa datotek, morate za vsako vrsto zapisa ustvariti ločena opravila za uvoz.</span><span class="sxs-lookup"><span data-stu-id="1292c-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="1292c-123">Prerazporeditev transakcij s kreditnimi karticami za zaposlene, katerih zaposlitev se je končala</span><span class="sxs-lookup"><span data-stu-id="1292c-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="1292c-124">Ko je zapis zaposlenega ukinjen, je zaposlenčev račun za domenske storitve Active Directory (AD DS) onemogočen.</span><span class="sxs-lookup"><span data-stu-id="1292c-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="1292c-125">Vendar pa lahko še obstajajo aktivne transakcije s kreditnimi karticami, ki jih je treba predložiti kot stroške in povrniti.</span><span class="sxs-lookup"><span data-stu-id="1292c-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="1292c-126">Na strani **Transakcije s kreditnimi karticami** lahko zaposlenemu dodelite katero koli transakcijo s kreditno kartico, pri kateri je bila možnost povezanega zaposlenega prekinjena.</span><span class="sxs-lookup"><span data-stu-id="1292c-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="1292c-127">Izberite eno ali več transakcij s kreditnimi karticami in nato izberite **Prerazporeditev transakcij**.</span><span class="sxs-lookup"><span data-stu-id="1292c-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="1292c-128">Nato lahko izberete drugega zaposlenega, ki mu dodelite transakcije s kreditnimi karticami.</span><span class="sxs-lookup"><span data-stu-id="1292c-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="1292c-129">Ko so transakcije s kreditnimi karticami prerazporejene, jih lahko izberete za poročilo o stroških in plačate prek običajnega procesa za povračilo po poročilu o stroških.</span><span class="sxs-lookup"><span data-stu-id="1292c-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="1292c-130">Izbrišite transakcije s kreditnimi karticami</span><span class="sxs-lookup"><span data-stu-id="1292c-130">Delete credit card transactions</span></span> 

<span data-ttu-id="1292c-131">Včasih je po uvozu transakcij s kreditno kartico morda treba nekatere transakcije izbrisati.</span><span class="sxs-lookup"><span data-stu-id="1292c-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="1292c-132">To je lahko zato, ker so transakcije podvojene ali ker podatki morda niso točni.</span><span class="sxs-lookup"><span data-stu-id="1292c-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="1292c-133">Skrbniki lahko uporabljajo funkcijo **»Izbriši transakcije s kreditno kartico«** za izbiro in brisanje transakcij s kreditnimi karticami, ki **niso priložene** poročilu o odhodkih.</span><span class="sxs-lookup"><span data-stu-id="1292c-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="1292c-134">Odprite **Redna opravila** > **Izbriši transakcije s kreditnimi karticami**.</span><span class="sxs-lookup"><span data-stu-id="1292c-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="1292c-135">Izberite **Filter** in zagotovite informacije za identifikacijo zapisov, ki jih je treba vključiti.</span><span class="sxs-lookup"><span data-stu-id="1292c-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="1292c-136">Če želite izbrisati zapise, izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="1292c-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
