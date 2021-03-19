---
title: Nastavitev integracije kreditne kartice
description: V tej temi je pojasnjeno, kako uvoziti in vzdrževati transakcije s kreditnimi karticami, povezane s stroški.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276188"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="c6b26-103">Nastavitev integracije kreditne kartice</span><span class="sxs-lookup"><span data-stu-id="c6b26-103">Set up credit card integration</span></span>

<span data-ttu-id="c6b26-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="c6b26-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c6b26-105">Transakcije s kreditnimi karticami, povezane s stroški, lahko nastavite tako, da se samodejno uvozijo po ponavljajočem se urniku.</span><span class="sxs-lookup"><span data-stu-id="c6b26-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="c6b26-106">Lahko pa transakcije uvozite tudi ročno, kot so potrebne.</span><span class="sxs-lookup"><span data-stu-id="c6b26-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="c6b26-107">Transakcije s kreditnimi karticami se uvažajo prek podatkovne entitete za transakcije s kreditnimi karticami.</span><span class="sxs-lookup"><span data-stu-id="c6b26-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="c6b26-108">Uvoz transakcij s kreditnimi karticami</span><span class="sxs-lookup"><span data-stu-id="c6b26-108">Import credit card transactions</span></span>

1. <span data-ttu-id="c6b26-109">Na strani **Transakcije s kreditnimi karticami** izberite **Uvoz transakcij**.</span><span class="sxs-lookup"><span data-stu-id="c6b26-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="c6b26-110">Če prvič odpirate upravljanje podatkov, mora sistem posodobiti seznam podatkovnih entitet, preden lahko nadaljujete.</span><span class="sxs-lookup"><span data-stu-id="c6b26-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="c6b26-111">V polje **Ime** vnesite enolični opis opravila uvoza.</span><span class="sxs-lookup"><span data-stu-id="c6b26-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="c6b26-112">V polju **Izvorna oblika zapisa podatkov** izberite obliko zapisa datoteke, ki vsebuje transakcije s kreditno kartico za uvoz.</span><span class="sxs-lookup"><span data-stu-id="c6b26-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="c6b26-113">Izberite **Naloži**, nato pa poiščite in izberite datoteko za uvoz.</span><span class="sxs-lookup"><span data-stu-id="c6b26-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="c6b26-114">Ko je datoteka naložena, preverite preslikavo datoteke transakcij s kreditnimi karticami in stolpce podatkovne entitete transakcij s kreditnimi karticami, tako da izberete povezavo **Prikaz zemljevida** na ploščici.</span><span class="sxs-lookup"><span data-stu-id="c6b26-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="c6b26-115">Če obstajajo napake pri preslikavi ali če morate spremeniti preslikavo, naredite spremembe preslikave bodisi iz zavihka **Upodobitev preslikave** ali zavihka **Podrobnosti preslikave**.</span><span class="sxs-lookup"><span data-stu-id="c6b26-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="c6b26-116">Za avtomatizacijo transakcij s kreditnimi karticami izberite **Ustvari ponavljajoči se podatkovni posel**.</span><span class="sxs-lookup"><span data-stu-id="c6b26-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="c6b26-117">Nato lahko nastavite ponavljanje, ki opredeljuje, kako pogosto naj se transakcije s kreditnimi karticami uvozijo.</span><span class="sxs-lookup"><span data-stu-id="c6b26-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="c6b26-118">Ko končate, izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="c6b26-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="c6b26-119">Če želite izbrano datoteko uvoziti zdaj, izberite **Uvozi**.</span><span class="sxs-lookup"><span data-stu-id="c6b26-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="c6b26-120">Če med uvozom pride do napak, si lahko ogledate dnevnik izvajanja ali podatke o pripravi, da vidite napake, ki jih morate odpraviti, da zagotovite uspešen uvoz.</span><span class="sxs-lookup"><span data-stu-id="c6b26-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="c6b26-121">Če morate uvoziti več oblik zapisov datotek, morate za vsako vrsto oblike zapisa ustvariti ločen posel za uvoz.</span><span class="sxs-lookup"><span data-stu-id="c6b26-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="c6b26-122">Prerazporeditev transakcij s kreditnimi karticami za zaposlene, katerih zaposlitev se je končala</span><span class="sxs-lookup"><span data-stu-id="c6b26-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="c6b26-123">Ko je zapis zaposlenega ukinjen, je zaposlenčev račun za domenske storitve Active Directory (AD DS) onemogočen.</span><span class="sxs-lookup"><span data-stu-id="c6b26-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="c6b26-124">Vendar pa lahko še obstajajo aktivne transakcije s kreditnimi karticami, ki jih je treba predložiti kot stroške in povrniti.</span><span class="sxs-lookup"><span data-stu-id="c6b26-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="c6b26-125">Na strani **Transakcije s kreditnimi karticami** lahko prerazporedite zaposlenega za katero koli transakcijo s kreditno kartico, kjer se je zaposlitev povezanega zaposlenega končala.</span><span class="sxs-lookup"><span data-stu-id="c6b26-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="c6b26-126">Izberite eno ali več transakcij s kreditnimi karticami in nato izberite **Prerazporeditev transakcij**.</span><span class="sxs-lookup"><span data-stu-id="c6b26-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="c6b26-127">Nato lahko izberete drugega zaposlenega, ki mu dodelite transakcije s kreditnimi karticami.</span><span class="sxs-lookup"><span data-stu-id="c6b26-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="c6b26-128">Ko so transakcije s kreditnimi karticami prerazporejene, jih lahko izberete za poročilo o stroških in plačate prek običajnega procesa za povračilo po poročilu o stroških.</span><span class="sxs-lookup"><span data-stu-id="c6b26-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]