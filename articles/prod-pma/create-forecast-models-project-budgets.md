---
title: Ustvarjanje modelov napovedi za proračune projektov
description: Ta tema opisuje, kako ustvariti model napovedi za preostale proračune.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006319"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="05fbf-103">Ustvarjanje modelov napovedi za proračune projektov</span><span class="sxs-lookup"><span data-stu-id="05fbf-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05fbf-104">Ta tema opisuje, kako ustvariti model napovedi za preostale proračune.</span><span class="sxs-lookup"><span data-stu-id="05fbf-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="05fbf-105">Projekt, ki je podrejen proračunskemu nadzoru, uporablja dve vrsti proračuna: prvotni in preostali proračun.</span><span class="sxs-lookup"><span data-stu-id="05fbf-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="05fbf-106">Ko ustvarite proračun projekta, morate navesti model napovedi prvotnega in preostalega proračuna, ki sta bila ustvarjena na strani **Modeli napovedi**.</span><span class="sxs-lookup"><span data-stu-id="05fbf-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="05fbf-107">Proračuni projektov, ki temeljijo na določenih modelih, se ustvarijo, ko potrdite proračun projekta.</span><span class="sxs-lookup"><span data-stu-id="05fbf-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="05fbf-108">Model napovedi, ki se uporablja za nadzor proračuna, ne more imeti podmodela ali biti uporabljen kot podmodel.</span><span class="sxs-lookup"><span data-stu-id="05fbf-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="05fbf-109">Izberite **Vodenje projektov in računovodstvo** > **Nastavitev** > **Napovedi**  > **Modeli napovedi**.</span><span class="sxs-lookup"><span data-stu-id="05fbf-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="05fbf-110">Izberite **Novo**, da ustvarite nov model napovedi in nato vnesite ID številko modela in ime novega modela.</span><span class="sxs-lookup"><span data-stu-id="05fbf-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="05fbf-111">Nastavite možnost **Ustavljeno** na **Da**, da preprečite kakršne koli spremembe vrstic napovedi za model napovedi.</span><span class="sxs-lookup"><span data-stu-id="05fbf-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="05fbf-112">Če bi želeli, da vrstice napovedi, s katerimi je povezan model, generirajo napovedi denarnih tokov v glavni knjigi, nastavite **Vključi v napovedi denarnih tokov** na **Da.**</span><span class="sxs-lookup"><span data-stu-id="05fbf-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="05fbf-113">Če želite datum projekta uporabiti kot datum računa, nastavite **Napovedani datum računa** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="05fbf-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="05fbf-114">V polju **Vrsta proračuna** izberite eno od naslednjih vrst modelov:</span><span class="sxs-lookup"><span data-stu-id="05fbf-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="05fbf-115">**Prvotni proračun**: uporabite prvotne zneske proračuna, ki so vneseni, ko je začetni proračun ustvarjen in odobren.</span><span class="sxs-lookup"><span data-stu-id="05fbf-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="05fbf-116">**Preostali proračun**: uporabite preostale proračunske zneske v času trajanja projekta.</span><span class="sxs-lookup"><span data-stu-id="05fbf-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="05fbf-117">Stanja v tem modelu napovedi se zmanjšajo za dejanske transakcije in povečajo ali zmanjšajo s popravki proračuna.</span><span class="sxs-lookup"><span data-stu-id="05fbf-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="05fbf-118">**Prenos naprej**: uporabite zneske prenosa proračuna za projekt.</span><span class="sxs-lookup"><span data-stu-id="05fbf-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="05fbf-119">Prenos naprej je neobvezen postopek, ki ga je mogoče zagnati za prenos neuporabljenih proračunskih zneskov iz enega proračunskega leta v drugega.</span><span class="sxs-lookup"><span data-stu-id="05fbf-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="05fbf-120">Po potrebi nastavite naslednje možnosti:</span><span class="sxs-lookup"><span data-stu-id="05fbf-120">Set the following options as required:</span></span>

   - <span data-ttu-id="05fbf-121">Omogočite **Napovedani datum računa**, če želite datum projekta uporabiti kot datum računa.</span><span class="sxs-lookup"><span data-stu-id="05fbf-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="05fbf-122">Omogočite **Napoved z WIP** za napovedovanje na podlagi dela v teku (WIP) in nato izberite vrsto WIP.</span><span class="sxs-lookup"><span data-stu-id="05fbf-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="05fbf-123">Privzeta možnost **Vrsta proračuna** lahko ostane **Brez**, sicer vnesite novo vrsto.</span><span class="sxs-lookup"><span data-stu-id="05fbf-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="05fbf-124">Po spremembi zapisa ni mogoče spremeniti vrste proračuna.</span><span class="sxs-lookup"><span data-stu-id="05fbf-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="05fbf-125">Če spremenite privzeto vrsto proračuna, druge možnosti ne bodo na voljo za posodobitev in tega modela napovedi ne boste mogli ponovno uporabiti.</span><span class="sxs-lookup"><span data-stu-id="05fbf-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]