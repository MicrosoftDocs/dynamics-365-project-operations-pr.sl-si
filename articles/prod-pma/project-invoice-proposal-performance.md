---
title: Uspešnost predlogov za račune projekta
description: Ta tema vsebuje informacije o izboljšavah učinkovitosti delovanja predlogov računov za projekte.
author: Yowelle
manager: AnnBe
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 1641d5f731029fdbdc16c4b652cc752a583058c6
ms.sourcegitcommit: 68d52fc983861114e654ffc8d2472b4db9b48981
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920322"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="7b80c-103">Uspešnost predlogov za račune projekta</span><span class="sxs-lookup"><span data-stu-id="7b80c-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b80c-104">Ko ustvarite nov predlog računa, lahko naletite na težave z učinkovitostjo delovanja, saj se število projektov in podprojektov poveča.</span><span class="sxs-lookup"><span data-stu-id="7b80c-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="7b80c-105">Za izboljšanje učinkovitosti delovanja je na voljo funkcija, ki skrajša čas, potreben za izdelavo novega predloga računa za objavljene transakcije projekta.</span><span class="sxs-lookup"><span data-stu-id="7b80c-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="7b80c-106">Omogočanje izboljšane učinkovitosti delovanja predlogov za račune projekta</span><span class="sxs-lookup"><span data-stu-id="7b80c-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="7b80c-107">Če želite omogočiti funkcijo izboljšanja učinkovitosti delovanja predlogov za račune projekta, izvedite naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="7b80c-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="7b80c-108">Pojdite v **Upravljanje funkcij** > **Vse**.</span><span class="sxs-lookup"><span data-stu-id="7b80c-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="7b80c-109">Na seznamu funkcij poiščite **Izboljšanje učinkovitosti delovanja predlogov za račune projekta**.</span><span class="sxs-lookup"><span data-stu-id="7b80c-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="7b80c-110">Izberite **Omogoči zdaj**.</span><span class="sxs-lookup"><span data-stu-id="7b80c-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="7b80c-111">Osvežite brskalnik in ustvarite nov predlog računa.</span><span class="sxs-lookup"><span data-stu-id="7b80c-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="7b80c-112">Izklop izboljšane učinkovitosti delovanja predlogov za račune projekta</span><span class="sxs-lookup"><span data-stu-id="7b80c-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="7b80c-113">Če želite izklopiti izboljšanje učinkovitosti delovanja predlogov za račune projekta, izvedite naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="7b80c-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="7b80c-114">Pojdite v **Upravljanje funkcij** > **Vse**.</span><span class="sxs-lookup"><span data-stu-id="7b80c-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="7b80c-115">Na seznamu funkcij poiščite **Izboljšanje učinkovitosti delovanja predlogov za račune projekta**.</span><span class="sxs-lookup"><span data-stu-id="7b80c-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="7b80c-116">Izberite **Onemogoči**.</span><span class="sxs-lookup"><span data-stu-id="7b80c-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="7b80c-117">Osvežite brskalnik.</span><span class="sxs-lookup"><span data-stu-id="7b80c-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="7b80c-118">Učinkovitosti delovanja predloga za račun ni mogoče uporabiti, če so omogočena pravila za obračun ali se izvajajo paketni procesi.</span><span class="sxs-lookup"><span data-stu-id="7b80c-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
