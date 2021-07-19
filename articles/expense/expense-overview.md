---
title: Pregled stroškov
description: Ta tema vsebuje informacije o funkcijah stroškov v aplikaciji Project Operations.
author: stsporen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 921df6fa8f1eb33bd01792c0b7c787fc74604adf
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368586"
---
# <a name="expense-home-page"></a><span data-ttu-id="21c6a-103">Domača stran stroška</span><span class="sxs-lookup"><span data-stu-id="21c6a-103">Expense home page</span></span>

<span data-ttu-id="21c6a-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="21c6a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="21c6a-105">Dynamics 365 Project Operations podpira možnost obdelave stroškov.</span><span class="sxs-lookup"><span data-stu-id="21c6a-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="21c6a-106">Obdelava stroškov se izvaja s projekti ali brez njih z uporabo prilagodljivega poteka dela pravilnikov, kategorij transakcij in odobritev.</span><span class="sxs-lookup"><span data-stu-id="21c6a-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="21c6a-107">V aplikaciji Project Operations sta podprta dva modela uvajanja za stroške:</span><span class="sxs-lookup"><span data-stu-id="21c6a-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="21c6a-108">**Polni**: na voljo je polno uvajanje za **Project Operations za scenarije na podlagi virov/brez zaloge** ali **Project Operations za scenarije na podlagi proizvodnih naročil**.</span><span class="sxs-lookup"><span data-stu-id="21c6a-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="21c6a-109">**Osnovni**: osnovno uvajanje je na voljo za **projektne postopke za scenarije na podlagi virov/brez zaloge** in **poenostavljeno uvajanje – posel do izstavitve predračuna**.</span><span class="sxs-lookup"><span data-stu-id="21c6a-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="21c6a-110">Celotni</span><span class="sxs-lookup"><span data-stu-id="21c6a-110">Full</span></span> 
<span data-ttu-id="21c6a-111">Polno uvajanje za stroške zagotavlja celovito uvedbo pravilnikov, kar vključuje možnost ustvarjanja pravilnikov, kot so:</span><span class="sxs-lookup"><span data-stu-id="21c6a-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="21c6a-112">Omejitve za kategorijo stroška</span><span class="sxs-lookup"><span data-stu-id="21c6a-112">Expense category limits</span></span>
  - <span data-ttu-id="21c6a-113">Potovanja</span><span class="sxs-lookup"><span data-stu-id="21c6a-113">Travel</span></span>
  - <span data-ttu-id="21c6a-114">Dnevnica</span><span class="sxs-lookup"><span data-stu-id="21c6a-114">Per diem</span></span>
  - <span data-ttu-id="21c6a-115">Uvoz kreditnih kartic</span><span class="sxs-lookup"><span data-stu-id="21c6a-115">Credit card imports</span></span>
  - <span data-ttu-id="21c6a-116">Prepoznavanje računov z optičnim branjem</span><span class="sxs-lookup"><span data-stu-id="21c6a-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="21c6a-117">Osnovno</span><span class="sxs-lookup"><span data-stu-id="21c6a-117">Basic</span></span> 
<span data-ttu-id="21c6a-118">Osnovni scenarij uvajanja stroškov omogoča le beleženje osnovnih stroškov glede na projekt.</span><span class="sxs-lookup"><span data-stu-id="21c6a-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="21c6a-119">Če želite več informacij, glejte razdelek [Vnos stroškov (poenostavljen)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="21c6a-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="21c6a-120">Ugotavljanje vrste uvajanja stroškov</span><span class="sxs-lookup"><span data-stu-id="21c6a-120">Determine your Expense deployment</span></span>
<span data-ttu-id="21c6a-121">Če želite ugotoviti, ali izvajate osnovno upravljanje uvajanja stroškov, preverite, ali se URL konča z **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="21c6a-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]