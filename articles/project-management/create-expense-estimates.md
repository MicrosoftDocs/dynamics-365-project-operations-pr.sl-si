---
title: Ocena stroškov
description: Ta tema vsebuje informacije o določanju ali oceni stroškov za posamezen projekt.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084678"
---
# <a name="expense-estimates"></a><span data-ttu-id="20923-103">Ocena stroškov</span><span class="sxs-lookup"><span data-stu-id="20923-103">Expense estimates</span></span>
<span data-ttu-id="20923-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="20923-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="20923-105">Aplikacija Dynamics 365 Project Operations poleg definiranja ocen na podlagi virov projektnim vodjem omogoča, da opredelijo projektne stroške za posamezen projekt.</span><span class="sxs-lookup"><span data-stu-id="20923-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="20923-106">Vsako postavko stroškov je mogoče povezati z določeno projektno nalogo ali kategorijo stroškov.</span><span class="sxs-lookup"><span data-stu-id="20923-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="20923-107">Kategorije stroškov so običajno opredeljene na organizacijski ravni.</span><span class="sxs-lookup"><span data-stu-id="20923-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="20923-108">Cene za vsako posamezno kategorijo stroškov so običajno opredeljene v naslednji hierarhiji:</span><span class="sxs-lookup"><span data-stu-id="20923-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="20923-109">Organizacija</span><span class="sxs-lookup"><span data-stu-id="20923-109">Organization</span></span>
- <span data-ttu-id="20923-110">Stranki</span><span class="sxs-lookup"><span data-stu-id="20923-110">Customer</span></span>
- <span data-ttu-id="20923-111">Ponudba/pogodba</span><span class="sxs-lookup"><span data-stu-id="20923-111">Quote/contract</span></span>

<span data-ttu-id="20923-112">Za ogled, dodajanje ali brisanje stroškov projekta izvedite naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="20923-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="20923-113">Na obrazcu **Projekti** izberite projekt, na katerem želite delati.</span><span class="sxs-lookup"><span data-stu-id="20923-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="20923-114">Na zavihku **Ocene projekta** si oglejte seznam stroškov projekta.</span><span class="sxs-lookup"><span data-stu-id="20923-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="20923-115">Izberite možnost **Novi stroški** , da dodate strošek.</span><span class="sxs-lookup"><span data-stu-id="20923-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="20923-116">Ali pa izberite strošek, ki ga želite izbrisati, in nato izberite možnost **Izbriši strošek**.</span><span class="sxs-lookup"><span data-stu-id="20923-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="20923-117">Za vsako postavko stroškov so opredeljeni naslednji atributi:</span><span class="sxs-lookup"><span data-stu-id="20923-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="20923-118">**Kategorija** : običajne združitve, uporabljene za opis vseh stroškov, nastalih pri projektu.</span><span class="sxs-lookup"><span data-stu-id="20923-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="20923-119">**Začetni datum** : predvideni datum nastanka stroškov</span><span class="sxs-lookup"><span data-stu-id="20923-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="20923-120">**Količina** : ocenjeno število postavk odhodkov za posamezno kategorijo</span><span class="sxs-lookup"><span data-stu-id="20923-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="20923-121">**Cena na enoto stroška** : cena na enoto, uporabljena za izračun izdatkov za strošek</span><span class="sxs-lookup"><span data-stu-id="20923-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="20923-122">**Cena na enoto prodaje** : cena na enoto, uporabljena za izračun prodajne cene za strošek</span><span class="sxs-lookup"><span data-stu-id="20923-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

