---
title: Zakaj se cena pri dejanski vrednosti »strošek – cena« privzeto nastavi na nič?
description: 'Odpravljanje težav: cena pri dejanski vrednosti »strošek – cena« se privzeto nastavi na 0.'
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146368"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="aeec3-103">Zakaj se cena pri dejanski vrednosti »strošek – cena« privzeto nastavi na nič</span><span class="sxs-lookup"><span data-stu-id="aeec3-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="aeec3-104">To pogosto vprašanje se nanaša na dejansko vrednost stroška, kjer je razred transakcije nastavljen na »Strošek«, vrsta transakcije pa je »Cena«.</span><span class="sxs-lookup"><span data-stu-id="aeec3-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="aeec3-105">Odpravljanje težav v povezavi s cenami pri dejanski vrednosti »strošek – cena«</span><span class="sxs-lookup"><span data-stu-id="aeec3-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="aeec3-106">Odprite povezani vnos stroška in se prepričajte, da je v polju za vnos stroška vnesen znesek.</span><span class="sxs-lookup"><span data-stu-id="aeec3-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="aeec3-107">Če pri izvirnem vnosu stroška polje z zneskom ni bilo izpolnjeno, ste osamili težavo.</span><span class="sxs-lookup"><span data-stu-id="aeec3-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="aeec3-108">Da bi rešili to težavo, znova ustvarite vnos stroška z veljavnim zneskom in ga odobrite.</span><span class="sxs-lookup"><span data-stu-id="aeec3-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
