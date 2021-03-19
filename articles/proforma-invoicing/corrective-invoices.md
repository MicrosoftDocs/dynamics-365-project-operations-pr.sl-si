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
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287843"
---
# <a name="corrected-invoices"></a><span data-ttu-id="b2d55-103">Popravljeni računi</span><span class="sxs-lookup"><span data-stu-id="b2d55-103">Corrected invoices</span></span>

<span data-ttu-id="b2d55-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="b2d55-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b2d55-105">Potrjene račune lahko uredite.</span><span class="sxs-lookup"><span data-stu-id="b2d55-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="b2d55-106">Ko uredite potrjeni račun, se ustvari osnutek popravljenega računa.</span><span class="sxs-lookup"><span data-stu-id="b2d55-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="b2d55-107">Ker se predpostavlja, da želite stornirati vse transakcije in količine iz izvirnega računa, popravljeni račun vključuje vse transakcije iz izvirnega računa, vse količine na njem pa imajo vrednost nič (0).</span><span class="sxs-lookup"><span data-stu-id="b2d55-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="b2d55-108">Ko transakcije ne potrebujejo popravka, jih lahko odstranite iz osnutka korektivnega računa.</span><span class="sxs-lookup"><span data-stu-id="b2d55-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="b2d55-109">Za storniranje ali vrnitev le delne količine, lahko uredite polje »Količina« v podrobnosti vrstice.</span><span class="sxs-lookup"><span data-stu-id="b2d55-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="b2d55-110">Če odprete podrobnost vrstice računa, si lahko ogledate količino na izvirnem računu.</span><span class="sxs-lookup"><span data-stu-id="b2d55-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="b2d55-111">Nato lahko uredite količino na trenutnem računu, tako da je manjša ali večja od količine na izvirnem računu.</span><span class="sxs-lookup"><span data-stu-id="b2d55-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="b2d55-112">Ko potrdite korektivni račun, je prvotna obračunana dejanska prodaja stornirana in ustvari se nova obračunana dejanska prodaja.</span><span class="sxs-lookup"><span data-stu-id="b2d55-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="b2d55-113">Če ste zmanjšali količino, se bo zaradi razlike ustvarila tudi nova neobračunana dejanska prodaja.</span><span class="sxs-lookup"><span data-stu-id="b2d55-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="b2d55-114">Če je bila na primer prvotna obračunana prodaja za osem ur, v podrobnosti vrstice popravljenega računa pa je količina zmanjšana na šest ur, se vrstica izvirne obračunane prodaje stornira in ustvarita se dve novi dejanski vrednosti:</span><span class="sxs-lookup"><span data-stu-id="b2d55-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="b2d55-115">Obračunana dejanska prodaja za šest ur.</span><span class="sxs-lookup"><span data-stu-id="b2d55-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="b2d55-116">Neobračunana dejanska prodaja za preostali dve uri.</span><span class="sxs-lookup"><span data-stu-id="b2d55-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="b2d55-117">Ta transakcija je lahko obračunana pozneje ali označena kot transakcija, ki se ne zaračuna, odvisno od pogajanj s stranko.</span><span class="sxs-lookup"><span data-stu-id="b2d55-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]