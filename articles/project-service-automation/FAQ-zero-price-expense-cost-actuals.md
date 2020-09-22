---
title: Zakaj se cena pri dejanski vrednosti »strošek – cena« privzeto nastavi na nič?
description: 'Odpravljanje težav: cena pri dejanski vrednosti »strošek – cena« se privzeto nastavi na 0.'
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755788"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="f16b1-103">Zakaj se cena pri dejanski vrednosti »strošek – cena« privzeto nastavi na nič?</span><span class="sxs-lookup"><span data-stu-id="f16b1-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f16b1-104">To pogosto vprašanje se nanaša na dejansko vrednost stroška, kjer je razred transakcije nastavljen na »Strošek«, vrsta transakcije pa je »Cena«.</span><span class="sxs-lookup"><span data-stu-id="f16b1-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="f16b1-105">Odpravljanje težav v povezavi s cenami pri dejanski vrednosti »strošek – cena«</span><span class="sxs-lookup"><span data-stu-id="f16b1-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="f16b1-106">Odprite povezani vnos stroška in se prepričajte, da je v polju za vnos stroška vnesen znesek.</span><span class="sxs-lookup"><span data-stu-id="f16b1-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="f16b1-107">Če pri izvirnem vnosu stroška polje z zneskom ni bilo izpolnjeno, ste osamili težavo.</span><span class="sxs-lookup"><span data-stu-id="f16b1-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="f16b1-108">Da bi rešili to težavo, znova ustvarite vnos stroška z veljavnim zneskom in ga odobrite.</span><span class="sxs-lookup"><span data-stu-id="f16b1-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
