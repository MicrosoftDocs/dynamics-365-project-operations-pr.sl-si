---
title: Več odobriteljev za poročilo o stroških
description: Ta tema vsebuje informacije o poročilih o stroških, ki jih mora odobriti več oseb.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745dda957fab5acc464b9d1c774fcdc783cde40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005271"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="dd49c-103">Več odobriteljev za poročilo o stroških</span><span class="sxs-lookup"><span data-stu-id="dd49c-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="dd49c-104">Glede na pravilnik o odobritvi stroškov vaše organizacije bo morda morala poročilo o stroških, ki ga predloži zaposleni, odobriti več kot ena oseba.</span><span class="sxs-lookup"><span data-stu-id="dd49c-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="dd49c-105">Ko nastavite proces poteka dela za odobritev poročila o stroških, lahko dodate elemente poteka dela, ki vključujejo opravila ali korake za enega ali več odobriteljev poročil o stroških.</span><span class="sxs-lookup"><span data-stu-id="dd49c-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="dd49c-106">Na primer, morda bo potrebno, da vsa poročila o stroških najprej odobrita vodja zaposlenega, ki je predložil poročilo, in nato še koordinator za obveznosti.</span><span class="sxs-lookup"><span data-stu-id="dd49c-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="dd49c-107">Če se odločite za več odobriteljev poročil o stroških, lahko elemente poteka dela dodate na katerega koli od naslednjih načinov:</span><span class="sxs-lookup"><span data-stu-id="dd49c-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="dd49c-108">Dodajte en element odobritve, ki ima en korak.</span><span class="sxs-lookup"><span data-stu-id="dd49c-108">Add one approval element that has one step.</span></span> <span data-ttu-id="dd49c-109">Na primer, v koraku je lahko zahtevano, da se poročilo o stroških dodeli uporabniški skupini in da ga odobri 50 odstotkov članov uporabniške skupine.</span><span class="sxs-lookup"><span data-stu-id="dd49c-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="dd49c-110">Dodajte en element odobritve, ki ima več korakov.</span><span class="sxs-lookup"><span data-stu-id="dd49c-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="dd49c-111">Na primer, element odobritve ima lahko naslednje korake:</span><span class="sxs-lookup"><span data-stu-id="dd49c-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="dd49c-112">Vodja zaposlenega, ki je predložil poročilo o stroških, tega odobri.</span><span class="sxs-lookup"><span data-stu-id="dd49c-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="dd49c-113">Uradnik za obveznosti preveri potrdila in postavke poročila o stroških.</span><span class="sxs-lookup"><span data-stu-id="dd49c-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="dd49c-114">Lastnik proračuna odobri poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="dd49c-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="dd49c-115">Dodajte več elementov odobritve, od katerih ima vsak en korak.</span><span class="sxs-lookup"><span data-stu-id="dd49c-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="dd49c-116">Na primer, lahko dodate ločen element odobritve za vsakega od naslednjih korakov:</span><span class="sxs-lookup"><span data-stu-id="dd49c-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="dd49c-117">Vodja zaposlenega odobri poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="dd49c-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="dd49c-118">Lastnik proračuna odobri poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="dd49c-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]