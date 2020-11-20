---
title: Pregled stroškov
description: Ta tema vsebuje informacije o funkcijah stroškov v aplikaciji Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6c5ef2a45e8141bda38baf3eaf0a403d6db95e48
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122858"
---
# <a name="expense-home-page"></a><span data-ttu-id="16d42-103">Domača stran stroška</span><span class="sxs-lookup"><span data-stu-id="16d42-103">Expense home page</span></span>

<span data-ttu-id="16d42-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="16d42-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="16d42-105">Aplikacija Dynamics 365 Project Operations podpira zmožnost obdelave stroškov.</span><span class="sxs-lookup"><span data-stu-id="16d42-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="16d42-106">Obdelava stroškov se izvaja s projekti ali brez njih z uporabo prilagodljivega poteka dela pravilnikov, kategorij transakcij in odobritev.</span><span class="sxs-lookup"><span data-stu-id="16d42-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="16d42-107">V aplikaciji Project Operations sta podprta dva modela uvajanja za stroške:</span><span class="sxs-lookup"><span data-stu-id="16d42-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="16d42-108">**Polni**: na voljo je polno uvajanje za **projektne postopke za scenarije na podlagi virov/brez zaloge** ali **projektne postopke za scenarije na podlagi proizvodnih naročil**.</span><span class="sxs-lookup"><span data-stu-id="16d42-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="16d42-109">**Osnovni**: osnovno uvajanje je na voljo za **projektne postopke za scenarije na podlagi virov/brez zaloge** in **poenostavljeno uvajanje – posel do izstavitve predračuna**.</span><span class="sxs-lookup"><span data-stu-id="16d42-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="16d42-110">Celotni</span><span class="sxs-lookup"><span data-stu-id="16d42-110">Full</span></span> 
<span data-ttu-id="16d42-111">Polno uvajanje stroškov zagotavlja popolno uveljavljanje pravilnikov, kar vključuje možnost ustvarjanja elementov pravilnikov, kot so:</span><span class="sxs-lookup"><span data-stu-id="16d42-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="16d42-112">Omejitve za kategorijo stroška</span><span class="sxs-lookup"><span data-stu-id="16d42-112">Expense category limits</span></span>
  - <span data-ttu-id="16d42-113">Potovanja</span><span class="sxs-lookup"><span data-stu-id="16d42-113">Travel</span></span>
  - <span data-ttu-id="16d42-114">Dnevnica</span><span class="sxs-lookup"><span data-stu-id="16d42-114">Per diem</span></span>
  - <span data-ttu-id="16d42-115">Uvoz kreditnih kartic</span><span class="sxs-lookup"><span data-stu-id="16d42-115">Credit card imports</span></span>
  - <span data-ttu-id="16d42-116">Prepoznavanje računov z optičnim branjem</span><span class="sxs-lookup"><span data-stu-id="16d42-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="16d42-117">Osnovno</span><span class="sxs-lookup"><span data-stu-id="16d42-117">Basic</span></span> 
<span data-ttu-id="16d42-118">Osnovni scenarij uvajanja stroškov omogoča le beleženje osnovnih stroškov glede na projekt.</span><span class="sxs-lookup"><span data-stu-id="16d42-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="16d42-119">Če želite več informacij, glejte razdelek [Vnos stroškov (poenostavljen)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="16d42-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="16d42-120">Ugotavljanje vrste uvajanja stroškov</span><span class="sxs-lookup"><span data-stu-id="16d42-120">Determine your Expense deployment</span></span>
<span data-ttu-id="16d42-121">Če želite ugotoviti, ali izvajate osnovno upravljanje uvajanja stroškov, preverite, ali se URL konča z **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="16d42-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
