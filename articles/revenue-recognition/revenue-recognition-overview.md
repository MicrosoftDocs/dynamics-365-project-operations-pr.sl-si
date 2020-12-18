---
title: Pregled priznavanja prihodkov
description: V tej temi so na voljo informacije o priznavanju prihodkov v storitvi Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531554"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="48a0c-103">Pregled priznavanja prihodkov</span><span class="sxs-lookup"><span data-stu-id="48a0c-103">Revenue recognition overview</span></span>

<span data-ttu-id="48a0c-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="48a0c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="48a0c-105">V storitvi Dynamics 365 Project Operations se načela priznavanja prihodkov razlikujejo glede na izbrani način obračunavanja za projekt ali del projekta.</span><span class="sxs-lookup"><span data-stu-id="48a0c-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="48a0c-106">V tej temi so na voljo informacije o priznavanju prihodkov v storitvi Project Operations.</span><span class="sxs-lookup"><span data-stu-id="48a0c-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="48a0c-107">Knjižene transakcije po načinu obračunavanja časa in materiala</span><span class="sxs-lookup"><span data-stu-id="48a0c-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="48a0c-108">Priznavanje stroškov in prihodkov sta povezana.</span><span class="sxs-lookup"><span data-stu-id="48a0c-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="48a0c-109">Transakcijski stroški in neobračunana prodaja so knjiženi z [dnevnikom integracije za Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="48a0c-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="48a0c-110">Profil projektnih stroškov in prihodkov določa, ali se neobračunane prodajne transakcije knjižijo v glavno knjigo.</span><span class="sxs-lookup"><span data-stu-id="48a0c-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="48a0c-111">Če je izbrana možnost **Fakturiranje prihodkov**, bo sistem med knjiženjem uporabil računa **Vrednost prodaje WIP** in **Vrednost prodaje fakturiranih prihodkov**.</span><span class="sxs-lookup"><span data-stu-id="48a0c-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="48a0c-112">V nadaljevanju je prikazan primer te metode.</span><span class="sxs-lookup"><span data-stu-id="48a0c-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="48a0c-113">Vrsta transakcije</span><span class="sxs-lookup"><span data-stu-id="48a0c-113">Transaction type</span></span> | <span data-ttu-id="48a0c-114">Bremenitev/dobropis</span><span class="sxs-lookup"><span data-stu-id="48a0c-114">Debit/Credit</span></span> | <span data-ttu-id="48a0c-115">Znesek</span><span class="sxs-lookup"><span data-stu-id="48a0c-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="48a0c-116">Vrednost prodaje WIP</span><span class="sxs-lookup"><span data-stu-id="48a0c-116">WIP Sales value</span></span> | <span data-ttu-id="48a0c-117">Bremenitev</span><span class="sxs-lookup"><span data-stu-id="48a0c-117">Debit</span></span> | <span data-ttu-id="48a0c-118">100</span><span class="sxs-lookup"><span data-stu-id="48a0c-118">100</span></span> |
  | <span data-ttu-id="48a0c-119">Vračunana vrednost prihodkov od prodaje</span><span class="sxs-lookup"><span data-stu-id="48a0c-119">Accrued revenue sales value</span></span> | <span data-ttu-id="48a0c-120">Dobropis</span><span class="sxs-lookup"><span data-stu-id="48a0c-120">Credit</span></span> | <span data-ttu-id="48a0c-121">100</span><span class="sxs-lookup"><span data-stu-id="48a0c-121">100</span></span> |

- <span data-ttu-id="48a0c-122">Prihodki so upoštevani pri izdaji računov.</span><span class="sxs-lookup"><span data-stu-id="48a0c-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="48a0c-123">Sistem med knjiženjem uporablja račun **Fakturirani prihodki**.</span><span class="sxs-lookup"><span data-stu-id="48a0c-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="48a0c-124">V nadaljevanju je prikazan primer te metode.</span><span class="sxs-lookup"><span data-stu-id="48a0c-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="48a0c-125">Vrsta transakcije</span><span class="sxs-lookup"><span data-stu-id="48a0c-125">Transaction type</span></span> | <span data-ttu-id="48a0c-126">Bremenitev/dobropis</span><span class="sxs-lookup"><span data-stu-id="48a0c-126">Debit/Credit</span></span> | <span data-ttu-id="48a0c-127">Znesek</span><span class="sxs-lookup"><span data-stu-id="48a0c-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="48a0c-128">Stanje stranke</span><span class="sxs-lookup"><span data-stu-id="48a0c-128">Customer balance</span></span> | <span data-ttu-id="48a0c-129">Bremenitev</span><span class="sxs-lookup"><span data-stu-id="48a0c-129">Debit</span></span> | <span data-ttu-id="48a0c-130">120</span><span class="sxs-lookup"><span data-stu-id="48a0c-130">120</span></span> |
  | <span data-ttu-id="48a0c-131">Prometni davek za plačilo</span><span class="sxs-lookup"><span data-stu-id="48a0c-131">Sales tax payable</span></span> | <span data-ttu-id="48a0c-132">Dobropis</span><span class="sxs-lookup"><span data-stu-id="48a0c-132">Credit</span></span> | <span data-ttu-id="48a0c-133">20</span><span class="sxs-lookup"><span data-stu-id="48a0c-133">20</span></span> |
  | <span data-ttu-id="48a0c-134">Fakturirani prihodek</span><span class="sxs-lookup"><span data-stu-id="48a0c-134">Invoiced Revenue</span></span> | <span data-ttu-id="48a0c-135">Dobropis</span><span class="sxs-lookup"><span data-stu-id="48a0c-135">Credit</span></span> | <span data-ttu-id="48a0c-136">100</span><span class="sxs-lookup"><span data-stu-id="48a0c-136">100</span></span> |

- <span data-ttu-id="48a0c-137">Če so bili prihodki fakturirani ob knjiženju neobračunanih prodaj, bo sistem povrnil obračunane prihodke ob izdaji računa.</span><span class="sxs-lookup"><span data-stu-id="48a0c-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="48a0c-138">Vrsta transakcije</span><span class="sxs-lookup"><span data-stu-id="48a0c-138">Transaction type</span></span> | <span data-ttu-id="48a0c-139">Bremenitev/dobropis</span><span class="sxs-lookup"><span data-stu-id="48a0c-139">Debit/Credit</span></span> | <span data-ttu-id="48a0c-140">Znesek</span><span class="sxs-lookup"><span data-stu-id="48a0c-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="48a0c-141">Vrednost prodaje WIP</span><span class="sxs-lookup"><span data-stu-id="48a0c-141">WIP Sales value</span></span> | <span data-ttu-id="48a0c-142">Dobropis</span><span class="sxs-lookup"><span data-stu-id="48a0c-142">Credit</span></span> | <span data-ttu-id="48a0c-143">100</span><span class="sxs-lookup"><span data-stu-id="48a0c-143">100</span></span> |
  | <span data-ttu-id="48a0c-144">Vračunana vrednost prihodkov od prodaje</span><span class="sxs-lookup"><span data-stu-id="48a0c-144">Accrued revenue sales value</span></span> | <span data-ttu-id="48a0c-145">Bremenitev</span><span class="sxs-lookup"><span data-stu-id="48a0c-145">Debit</span></span> | <span data-ttu-id="48a0c-146">100</span><span class="sxs-lookup"><span data-stu-id="48a0c-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="48a0c-147">Knjižene transakcije z načinom obračunavanja s fiksno ceno</span><span class="sxs-lookup"><span data-stu-id="48a0c-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="48a0c-148">Priznavanje stroškov in prihodkov je ločeno.</span><span class="sxs-lookup"><span data-stu-id="48a0c-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="48a0c-149">Transakcijski stroški so knjiženi z [dnevnikom integracije za Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="48a0c-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="48a0c-150">Neobračunane prodajne transakcije niso ustvarjene.</span><span class="sxs-lookup"><span data-stu-id="48a0c-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="48a0c-151">Prihodke je mogoče upoštevati med izdajanjem računov, če imajo projektni stroški in profil prihodkov atribut **Načelo, uporabljeno za izračune dokončanja projekta** nastavljen na **Brez WIP-a**.</span><span class="sxs-lookup"><span data-stu-id="48a0c-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="48a0c-152">To metodo uporabite samo za kratkoročne in preproste projekte.</span><span class="sxs-lookup"><span data-stu-id="48a0c-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="48a0c-153">Prihodke je mogoče upoštevati z uporabo ocen prihodkov s fiksno ceno, bodisi z metodo **Dokončana pogodba** ali **Priznavanje prihodka glede na odstotek dokončanosti**.</span><span class="sxs-lookup"><span data-stu-id="48a0c-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48a0c-154">Dodatni viri</span><span class="sxs-lookup"><span data-stu-id="48a0c-154">Additional resources</span></span>
[<span data-ttu-id="48a0c-155">Članek Konfiguracija vodenja računov za plačljive projekte</span><span class="sxs-lookup"><span data-stu-id="48a0c-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="48a0c-156">Projekti ocene prihodkov s fiksno ceno</span><span class="sxs-lookup"><span data-stu-id="48a0c-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="48a0c-157">Upravljanje ocen prihodkov</span><span class="sxs-lookup"><span data-stu-id="48a0c-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="48a0c-158">Metode za izračun stroškov za dokončanje</span><span class="sxs-lookup"><span data-stu-id="48a0c-158">Cost to complete methods</span></span>](cost-complete-methods.md)
