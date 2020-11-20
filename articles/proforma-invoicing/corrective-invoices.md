---
title: Popravljeni računi
description: Ta tema vsebuje informacije o popravljenih računih.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122408"
---
# <a name="corrected-invoices"></a><span data-ttu-id="182c6-103">Popravljeni računi</span><span class="sxs-lookup"><span data-stu-id="182c6-103">Corrected invoices</span></span>

<span data-ttu-id="182c6-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="182c6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="182c6-105">Potrjene račune lahko uredite.</span><span class="sxs-lookup"><span data-stu-id="182c6-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="182c6-106">Ko uredite potrjeni račun, se ustvari osnutek popravljenega računa.</span><span class="sxs-lookup"><span data-stu-id="182c6-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="182c6-107">Ker se predpostavlja, da želite stornirati vse transakcije in količine iz izvirnega računa, popravljeni račun vključuje vse transakcije iz izvirnega računa, vse količine na njem pa imajo vrednost nič (0).</span><span class="sxs-lookup"><span data-stu-id="182c6-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="182c6-108">Ko transakcije ne potrebujejo popravka, jih lahko odstranite iz osnutka korektivnega računa.</span><span class="sxs-lookup"><span data-stu-id="182c6-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="182c6-109">Za storniranje ali vrnitev le delne količine, lahko uredite polje »Količina« v podrobnosti vrstice.</span><span class="sxs-lookup"><span data-stu-id="182c6-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="182c6-110">Če odprete podrobnost vrstice računa, si lahko ogledate količino na izvirnem računu.</span><span class="sxs-lookup"><span data-stu-id="182c6-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="182c6-111">Nato lahko uredite količino na trenutnem računu, tako da je manjša ali večja od količine na izvirnem računu.</span><span class="sxs-lookup"><span data-stu-id="182c6-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="182c6-112">Ko potrdite korektivni račun, je prvotna obračunana dejanska prodaja stornirana in ustvari se nova obračunana dejanska prodaja.</span><span class="sxs-lookup"><span data-stu-id="182c6-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="182c6-113">Če ste zmanjšali količino, se bo zaradi razlike ustvarila tudi nova neobračunana dejanska prodaja.</span><span class="sxs-lookup"><span data-stu-id="182c6-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="182c6-114">Če je bila na primer prvotna obračunana prodaja za osem ur, v podrobnosti vrstice popravljenega računa pa je količina zmanjšana na šest ur, se vrstica izvirne obračunane prodaje stornira in ustvarita se dve novi dejanski vrednosti:</span><span class="sxs-lookup"><span data-stu-id="182c6-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="182c6-115">Obračunana dejanska prodaja za šest ur.</span><span class="sxs-lookup"><span data-stu-id="182c6-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="182c6-116">Neobračunana dejanska prodaja za preostali dve uri.</span><span class="sxs-lookup"><span data-stu-id="182c6-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="182c6-117">Ta transakcija je lahko obračunana pozneje ali označena kot transakcija, ki se ne zaračuna, odvisno od pogajanj s stranko.</span><span class="sxs-lookup"><span data-stu-id="182c6-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
