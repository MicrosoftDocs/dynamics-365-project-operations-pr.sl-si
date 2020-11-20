---
title: Poročila o stroških in več odobriteljev
description: Ta tema vsebuje informacije o poročilih o stroških, ki jih mora odobriti več kot ena oseba.
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
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121013"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="d5676-103">Poročila o stroških in več odobriteljev</span><span class="sxs-lookup"><span data-stu-id="d5676-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="d5676-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="d5676-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d5676-105">Glede na pravilnik o odobritvi stroškov vaše organizacije bo morda morala predloženo poročilo o stroških odobriti več kot ena oseba.</span><span class="sxs-lookup"><span data-stu-id="d5676-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="d5676-106">Ko nastavite proces poteka dela za odobritev poročila o stroških, lahko dodate elemente poteka dela, ki vključujejo opravila ali korake za enega ali več odobriteljev poročil o stroških.</span><span class="sxs-lookup"><span data-stu-id="d5676-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="d5676-107">Na primer, morda bo potrebno, da vsa poročila o stroških odobrita dve ločeni osebi, vodja zaposlenega, ki je predložil poročilo, in koordinator za obveznosti.</span><span class="sxs-lookup"><span data-stu-id="d5676-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="d5676-108">Če se odločite za več odobriteljev poročil o stroških, lahko elemente poteka dela dodate na katerega koli od naslednjih načinov:</span><span class="sxs-lookup"><span data-stu-id="d5676-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="d5676-109">Dodajte en element odobritve, ki ima en korak.</span><span class="sxs-lookup"><span data-stu-id="d5676-109">Add one approval element that has one step.</span></span> <span data-ttu-id="d5676-110">Na primer, v koraku je lahko zahtevano, da se poročilo o stroških dodeli uporabniški skupini in da ga odobri 50 odstotkov članov uporabniške skupine.</span><span class="sxs-lookup"><span data-stu-id="d5676-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="d5676-111">Dodajte en element odobritve, ki ima več korakov.</span><span class="sxs-lookup"><span data-stu-id="d5676-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="d5676-112">Na primer, element odobritve ima lahko naslednje korake:</span><span class="sxs-lookup"><span data-stu-id="d5676-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="d5676-113">Vodja zaposlenega, ki je predložil poročilo o stroških, tega odobri.</span><span class="sxs-lookup"><span data-stu-id="d5676-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="d5676-114">Uradnik za obveznosti preveri potrdila in postavke poročila o stroških.</span><span class="sxs-lookup"><span data-stu-id="d5676-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="d5676-115">Lastnik proračuna odobri poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="d5676-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="d5676-116">Dodajte več elementov odobritve, od katerih ima vsak en korak.</span><span class="sxs-lookup"><span data-stu-id="d5676-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="d5676-117">Na primer, lahko dodate ločen element odobritve za vsakega od naslednjih korakov:</span><span class="sxs-lookup"><span data-stu-id="d5676-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="d5676-118">Vodja zaposlenega odobri poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="d5676-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="d5676-119">Lastnik proračuna odobri poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="d5676-119">The budget owner approves the expense report.</span></span>
