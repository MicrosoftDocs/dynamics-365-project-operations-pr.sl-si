---
title: Uspešnost predlogov za račune projekta
description: Ta tema vsebuje informacije o izboljšavah učinkovitosti delovanja predlogov računov za projekte.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269810"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="77539-103">Uspešnost predlogov za račune projekta</span><span class="sxs-lookup"><span data-stu-id="77539-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77539-104">Ko ustvarite nov predlog računa, lahko naletite na težave z učinkovitostjo delovanja, saj se število projektov in podprojektov poveča.</span><span class="sxs-lookup"><span data-stu-id="77539-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="77539-105">Za izboljšanje učinkovitosti delovanja je na voljo funkcija, ki skrajša čas, potreben za izdelavo novega predloga računa za objavljene transakcije projekta.</span><span class="sxs-lookup"><span data-stu-id="77539-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="77539-106">Omogočanje izboljšane učinkovitosti delovanja predlogov za račune projekta</span><span class="sxs-lookup"><span data-stu-id="77539-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="77539-107">Če želite omogočiti funkcijo izboljšanja učinkovitosti delovanja predlogov za račune projekta, izvedite naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="77539-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="77539-108">Pojdite v **Upravljanje funkcij** > **Vse**.</span><span class="sxs-lookup"><span data-stu-id="77539-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="77539-109">Na seznamu funkcij poiščite **Izboljšanje učinkovitosti delovanja predlogov za račune projekta**.</span><span class="sxs-lookup"><span data-stu-id="77539-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="77539-110">Izberite **Omogoči zdaj**.</span><span class="sxs-lookup"><span data-stu-id="77539-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="77539-111">Osvežite brskalnik in ustvarite nov predlog računa.</span><span class="sxs-lookup"><span data-stu-id="77539-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="77539-112">Izklop izboljšane učinkovitosti delovanja predlogov za račune projekta</span><span class="sxs-lookup"><span data-stu-id="77539-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="77539-113">Če želite izklopiti izboljšanje učinkovitosti delovanja predlogov za račune projekta, izvedite naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="77539-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="77539-114">Pojdite v **Upravljanje funkcij** > **Vse**.</span><span class="sxs-lookup"><span data-stu-id="77539-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="77539-115">Na seznamu funkcij poiščite **Izboljšanje učinkovitosti delovanja predlogov za račune projekta**.</span><span class="sxs-lookup"><span data-stu-id="77539-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="77539-116">Izberite **Onemogoči**.</span><span class="sxs-lookup"><span data-stu-id="77539-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="77539-117">Osvežite brskalnik.</span><span class="sxs-lookup"><span data-stu-id="77539-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="77539-118">Uspešnost predloga za račun ne more biti uporabljena, ko so pravila za izstavitev računa onemogočena.</span><span class="sxs-lookup"><span data-stu-id="77539-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="77539-119">Med paketno obdelavo za ustvarjanje predloga za račun bodo številna podopravila, ne glede na to, kaj ste vnesli, na podlagi števila pogodb s transakcijami, ki se zaračunajo, opravila razdelila na največje možno število opravil.</span><span class="sxs-lookup"><span data-stu-id="77539-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="77539-120">Če označite, da serija zajema **3** podopravila za ustvarjanje predloge za račun, obstajata pa samo dve pogodbi s transakcijami, za katere se lahko izda račun, bosta ustvarjeni samo dve podopravili.</span><span class="sxs-lookup"><span data-stu-id="77539-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
