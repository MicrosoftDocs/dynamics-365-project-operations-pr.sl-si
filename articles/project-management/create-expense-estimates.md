---
title: Ocena stroškov
description: Ta tema vsebuje informacije o določanju ali oceni stroškov za posamezen projekt.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287078"
---
# <a name="expense-estimates"></a><span data-ttu-id="23f9e-103">Ocena stroškov</span><span class="sxs-lookup"><span data-stu-id="23f9e-103">Expense estimates</span></span>
<span data-ttu-id="23f9e-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="23f9e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="23f9e-105">Poleg opredelitve ocen, ki temeljijo na virih, aplikacija Dynamics 365 Project Operations projektnim vodjem omogoča, da za vsak projekt opredelijo stroške, ki temeljijo na projektu.</span><span class="sxs-lookup"><span data-stu-id="23f9e-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="23f9e-106">Vsako postavko stroškov je mogoče povezati z določeno projektno nalogo ali kategorijo stroškov.</span><span class="sxs-lookup"><span data-stu-id="23f9e-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="23f9e-107">Kategorije stroškov so običajno opredeljene na organizacijski ravni.</span><span class="sxs-lookup"><span data-stu-id="23f9e-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="23f9e-108">Cene za vsako posamezno kategorijo stroškov so običajno opredeljene v naslednji hierarhiji:</span><span class="sxs-lookup"><span data-stu-id="23f9e-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="23f9e-109">Organizacija</span><span class="sxs-lookup"><span data-stu-id="23f9e-109">Organization</span></span>
- <span data-ttu-id="23f9e-110">Stranki</span><span class="sxs-lookup"><span data-stu-id="23f9e-110">Customer</span></span>
- <span data-ttu-id="23f9e-111">Ponudba/pogodba</span><span class="sxs-lookup"><span data-stu-id="23f9e-111">Quote/contract</span></span>

<span data-ttu-id="23f9e-112">Za ogled, dodajanje ali brisanje stroškov projekta izvedite naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="23f9e-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="23f9e-113">Na obrazcu **Projekti** izberite projekt, na katerem želite delati.</span><span class="sxs-lookup"><span data-stu-id="23f9e-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="23f9e-114">Na zavihku **Ocene projekta** si oglejte seznam stroškov projekta.</span><span class="sxs-lookup"><span data-stu-id="23f9e-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="23f9e-115">Izberite možnost **Novi stroški**, da dodate strošek.</span><span class="sxs-lookup"><span data-stu-id="23f9e-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="23f9e-116">Ali pa izberite strošek, ki ga želite izbrisati, in nato izberite možnost **Izbriši strošek**.</span><span class="sxs-lookup"><span data-stu-id="23f9e-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="23f9e-117">Za vsako postavko stroškov so opredeljeni naslednji atributi:</span><span class="sxs-lookup"><span data-stu-id="23f9e-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="23f9e-118">**Kategorija**: običajne združitve, uporabljene za opis vseh stroškov, nastalih pri projektu.</span><span class="sxs-lookup"><span data-stu-id="23f9e-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="23f9e-119">**Začetni datum**: predvideni datum nastanka stroškov</span><span class="sxs-lookup"><span data-stu-id="23f9e-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="23f9e-120">**Količina**: ocenjeno število postavk odhodkov za posamezno kategorijo</span><span class="sxs-lookup"><span data-stu-id="23f9e-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="23f9e-121">**Cena na enoto stroška** : cena na enoto, uporabljena za izračun izdatkov za strošek</span><span class="sxs-lookup"><span data-stu-id="23f9e-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="23f9e-122">**Cena na enoto prodaje** : cena na enoto, uporabljena za izračun prodajne cene za strošek</span><span class="sxs-lookup"><span data-stu-id="23f9e-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]