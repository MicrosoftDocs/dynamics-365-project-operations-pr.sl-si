---
title: Razvoj predlog projekta s funkcijo »Kopiraj projekt«
description: Ta tema vsebuje informacije o tem, kako ustvariti predloge projektov z uporabo dejanja po meri »Kopiraj projekt«.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642428"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="e306a-103">Razvoj predlog projekta s funkcijo »Kopiraj projekt«</span><span class="sxs-lookup"><span data-stu-id="e306a-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="e306a-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="e306a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e306a-105">Dynamics 365 Project Operations podpira možnost kopiranja projekta in vračanja opravil v splošne vire, ki predstavljajo vlogo.</span><span class="sxs-lookup"><span data-stu-id="e306a-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="e306a-106">Stranke lahko to funkcijo uporabijo za izdelavo osnovnih predlog projekta.</span><span class="sxs-lookup"><span data-stu-id="e306a-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="e306a-107">Ko izberete **Kopiraj projekt**, se posodobi stanje ciljnega projekta.</span><span class="sxs-lookup"><span data-stu-id="e306a-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="e306a-108">Uporabite **Razlog stanja**, da ugotovite, kdaj je dejanje kopiranja končano.</span><span class="sxs-lookup"><span data-stu-id="e306a-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="e306a-109">Z izbiro funkcije **Kopiraj projekt** boste tudi posodobili začetni datum projekta na trenutni začetni datum, če v ciljni projektni entiteti ni zaznan noben ciljni datum.</span><span class="sxs-lookup"><span data-stu-id="e306a-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="e306a-110">Dejanje po meri »Kopiraj projekt«</span><span class="sxs-lookup"><span data-stu-id="e306a-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="e306a-111">Imenu</span><span class="sxs-lookup"><span data-stu-id="e306a-111">Name</span></span> 

<span data-ttu-id="e306a-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="e306a-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="e306a-113">Parametri vnosa</span><span class="sxs-lookup"><span data-stu-id="e306a-113">Input parameters</span></span>
<span data-ttu-id="e306a-114">Na voljo so trije parametri za vnos:</span><span class="sxs-lookup"><span data-stu-id="e306a-114">There are three input parameters:</span></span>

| <span data-ttu-id="e306a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e306a-115">Parameter</span></span>          | <span data-ttu-id="e306a-116">Vnesi</span><span class="sxs-lookup"><span data-stu-id="e306a-116">Type</span></span>   | <span data-ttu-id="e306a-117">Vrednosti</span><span class="sxs-lookup"><span data-stu-id="e306a-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="e306a-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="e306a-118">ProjectCopyOption</span></span>  | <span data-ttu-id="e306a-119">String</span><span class="sxs-lookup"><span data-stu-id="e306a-119">String</span></span> | <span data-ttu-id="e306a-120">**{"removeNamedResources":true}** ali **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="e306a-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="e306a-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="e306a-121">SourceProject</span></span>      | <span data-ttu-id="e306a-122">Sklic na entiteto</span><span class="sxs-lookup"><span data-stu-id="e306a-122">Entity Reference</span></span> | <span data-ttu-id="e306a-123">Izvorni projekt</span><span class="sxs-lookup"><span data-stu-id="e306a-123">Source Project</span></span> |
| <span data-ttu-id="e306a-124">Cilj</span><span class="sxs-lookup"><span data-stu-id="e306a-124">Target</span></span>             | <span data-ttu-id="e306a-125">Sklic na entiteto</span><span class="sxs-lookup"><span data-stu-id="e306a-125">Entity Reference</span></span> | <span data-ttu-id="e306a-126">Ciljni projekt</span><span class="sxs-lookup"><span data-stu-id="e306a-126">Target Project</span></span> |


- <span data-ttu-id="e306a-127">**{"clearTeamsAndAssignments":true}**: privzeto vedenje za spletni projekt, ki odstrani vse naloge in člane ekipe.</span><span class="sxs-lookup"><span data-stu-id="e306a-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="e306a-128">**{"removeNamedResources":true}** Privzeto vedenje za aplikacijo Project Operations, ki povrne naloge nazaj na splošne vire.</span><span class="sxs-lookup"><span data-stu-id="e306a-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="e306a-129">Za več informacij o dejanjih glejte [Uporaba dejanj spletnega API-ja](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="e306a-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="e306a-130">Določi polja za kopiranje</span><span class="sxs-lookup"><span data-stu-id="e306a-130">Specify fields to copy</span></span> 
<span data-ttu-id="e306a-131">Ko je dejanje klicano, si bo dejanje **Kopiraj projekt** v projektnem pogledu ogledalo **Kopiraj projektne stolpce**, da bo določilo, katera polja kopirati pri kopiranju projekta.</span><span class="sxs-lookup"><span data-stu-id="e306a-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
