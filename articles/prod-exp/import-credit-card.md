---
title: Uvoz in vzdrževanje transakcij s kreditnimi karticami
description: V tej temi je pojasnjeno, kako uvoziti in vzdrževati transakcije s kreditnimi karticami, povezane s stroški. Te transakcije lahko nastavite tako, da se samodejno uvozijo v rednem intervalu, ali pa jih po potrebi ročno uvozite.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084909"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="78349-104">Uvoz in vzdrževanje transakcij s kreditnimi karticami</span><span class="sxs-lookup"><span data-stu-id="78349-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78349-105">Transakcije s kreditnimi karticami, povezane s stroški, lahko nastavite tako, da se samodejno uvozijo po ponavljajočem se urniku.</span><span class="sxs-lookup"><span data-stu-id="78349-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="78349-106">Lahko pa transakcije uvozite tudi ročno, kot so potrebne.</span><span class="sxs-lookup"><span data-stu-id="78349-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="78349-107">Transakcije s kreditnimi karticami se uvažajo prek podatkovne entitete za transakcije s kreditnimi karticami.</span><span class="sxs-lookup"><span data-stu-id="78349-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="78349-108">Za več informacij o podatkovnih entitetah glejte [Podatkovne entitete](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="78349-108">For more information about data entities, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="78349-109">Uvoz transakcij s kreditnimi karticami</span><span class="sxs-lookup"><span data-stu-id="78349-109">Import credit card transactions</span></span>

1. <span data-ttu-id="78349-110">Na strani **Transakcije s kreditnimi karticami** izberite **Uvoz transakcij**.</span><span class="sxs-lookup"><span data-stu-id="78349-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="78349-111">Če prvič odpirate upravljanje podatkov, mora sistem posodobiti seznam podatkovnih entitet, preden lahko nadaljujete.</span><span class="sxs-lookup"><span data-stu-id="78349-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="78349-112">V polje **Ime** vnesite enolični opis opravila uvoza.</span><span class="sxs-lookup"><span data-stu-id="78349-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="78349-113">V polju **Izvorna oblika zapisa podatkov** izberite obliko zapisa datoteke, ki vsebuje transakcije s kreditno kartico za uvoz.</span><span class="sxs-lookup"><span data-stu-id="78349-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="78349-114">Izberite **Naloži** , nato pa poiščite in izberite datoteko za uvoz.</span><span class="sxs-lookup"><span data-stu-id="78349-114">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="78349-115">Ko je datoteka naložena, preverite preslikavo datoteke transakcij s kreditnimi karticami in stolpce podatkovne entitete transakcij s kreditnimi karticami, tako da izberete povezavo **Prikaz zemljevida** na ploščici.</span><span class="sxs-lookup"><span data-stu-id="78349-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="78349-116">Če obstajajo napake pri preslikavi ali če morate spremeniti preslikavo, naredite spremembe preslikave bodisi iz zavihka **Upodobitev preslikave** ali zavihka **Podrobnosti preslikave**.</span><span class="sxs-lookup"><span data-stu-id="78349-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="78349-117">Za avtomatizacijo transakcij s kreditnimi karticami izberite **Ustvari ponavljajoči se podatkovni posel**.</span><span class="sxs-lookup"><span data-stu-id="78349-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="78349-118">Nato lahko nastavite ponavljanje, ki opredeljuje, kako pogosto naj se transakcije s kreditnimi karticami uvozijo.</span><span class="sxs-lookup"><span data-stu-id="78349-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="78349-119">Ko končate, izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="78349-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="78349-120">Če želite izbrano datoteko uvoziti zdaj, izberite **Uvozi**.</span><span class="sxs-lookup"><span data-stu-id="78349-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="78349-121">Če med uvozom pride do napak, si lahko ogledate dnevnik izvajanja ali podatke o pripravi, da vidite napake, ki jih morate odpraviti, da zagotovite uspešen uvoz.</span><span class="sxs-lookup"><span data-stu-id="78349-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="78349-122">Če morate uvoziti več oblik zapisov datotek, morate za vsako vrsto oblike zapisa ustvariti ločen posel za uvoz.</span><span class="sxs-lookup"><span data-stu-id="78349-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="78349-123">Prerazporeditev transakcij s kreditnimi karticami za zaposlene, katerih zaposlitev se je končala</span><span class="sxs-lookup"><span data-stu-id="78349-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="78349-124">Ko je zapis zaposlenega ukinjen, je zaposlenčev račun za domenske storitve Active Directory (AD DS) onemogočen.</span><span class="sxs-lookup"><span data-stu-id="78349-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="78349-125">Vendar pa lahko še obstajajo aktivne transakcije s kreditnimi karticami, ki jih je treba predložiti kot stroške in povrniti.</span><span class="sxs-lookup"><span data-stu-id="78349-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="78349-126">Na strani **Transakcije s kreditnimi karticami** lahko prerazporedite zaposlenega za katero koli transakcijo s kreditno kartico, kjer se je zaposlitev povezanega zaposlenega končala.</span><span class="sxs-lookup"><span data-stu-id="78349-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="78349-127">Izberite eno ali več transakcij s kreditnimi karticami in nato izberite **Prerazporeditev transakcij**.</span><span class="sxs-lookup"><span data-stu-id="78349-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="78349-128">Nato lahko izberete drugega zaposlenega, ki mu dodelite transakcije s kreditnimi karticami.</span><span class="sxs-lookup"><span data-stu-id="78349-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="78349-129">Ko so transakcije s kreditnimi karticami prerazporejene, jih lahko izberete za poročilo o stroških in plačate prek običajnega procesa za povračilo po poročilu o stroških.</span><span class="sxs-lookup"><span data-stu-id="78349-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
