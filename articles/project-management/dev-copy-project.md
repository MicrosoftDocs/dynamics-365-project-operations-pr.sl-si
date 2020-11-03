---
title: Razvoj predlog projekta s funkcijo »Kopiraj projekt«
description: Ta tema vsebuje informacije o tem, kako ustvariti predloge projektov z uporabo dejanja po meri »Kopiraj projekt«.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084696"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="5f604-103">Razvoj predlog projekta s funkcijo »Kopiraj projekt«</span><span class="sxs-lookup"><span data-stu-id="5f604-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="5f604-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="5f604-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5f604-105">Dynamics 365 Project Operations podpira zmožnost kopiranja projekta in povrnitve morebitnih nalog nazaj na splošne vire, ki predstavljajo vlogo.</span><span class="sxs-lookup"><span data-stu-id="5f604-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="5f604-106">Stranke lahko to funkcijo uporabijo za izdelavo osnovnih predlog projekta.</span><span class="sxs-lookup"><span data-stu-id="5f604-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="5f604-107">Ko izberete **Kopiraj projekt** , se posodobi stanje ciljnega projekta.</span><span class="sxs-lookup"><span data-stu-id="5f604-107">When you select **Copy Project** , the status of the target project is updated.</span></span> <span data-ttu-id="5f604-108">Uporabite **Razlog stanja** , da ugotovite, kdaj je dejanje kopiranja končano.</span><span class="sxs-lookup"><span data-stu-id="5f604-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="5f604-109">Z izbiro funkcije **Kopiraj projekt** boste tudi posodobili začetni datum projekta na trenutni začetni datum, če v ciljni projektni entiteti ni zaznan noben ciljni datum.</span><span class="sxs-lookup"><span data-stu-id="5f604-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="5f604-110">Dejanje po meri »Kopiraj projekt«</span><span class="sxs-lookup"><span data-stu-id="5f604-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="5f604-111">Imenu</span><span class="sxs-lookup"><span data-stu-id="5f604-111">Name</span></span> 

<span data-ttu-id="5f604-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="5f604-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="5f604-113">Parametri vnosa</span><span class="sxs-lookup"><span data-stu-id="5f604-113">Input parameters</span></span>
<span data-ttu-id="5f604-114">Na voljo so trije parametri za vnos:</span><span class="sxs-lookup"><span data-stu-id="5f604-114">There are three input parameters:</span></span>

| <span data-ttu-id="5f604-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f604-115">Parameter</span></span>          | <span data-ttu-id="5f604-116">Vnesi</span><span class="sxs-lookup"><span data-stu-id="5f604-116">Type</span></span>   | <span data-ttu-id="5f604-117">Vrednosti</span><span class="sxs-lookup"><span data-stu-id="5f604-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="5f604-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="5f604-118">ProjectCopyOption</span></span>  | <span data-ttu-id="5f604-119">String</span><span class="sxs-lookup"><span data-stu-id="5f604-119">String</span></span> | <span data-ttu-id="5f604-120">**{"removeNamedResources":true}** ali **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="5f604-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="5f604-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="5f604-121">SourceProject</span></span>      | <span data-ttu-id="5f604-122">Sklic na entiteto</span><span class="sxs-lookup"><span data-stu-id="5f604-122">Entity Reference</span></span> | <span data-ttu-id="5f604-123">Izvorni projekt</span><span class="sxs-lookup"><span data-stu-id="5f604-123">Source Project</span></span> |
| <span data-ttu-id="5f604-124">Cilj</span><span class="sxs-lookup"><span data-stu-id="5f604-124">Target</span></span>             | <span data-ttu-id="5f604-125">Sklic na entiteto</span><span class="sxs-lookup"><span data-stu-id="5f604-125">Entity Reference</span></span> | <span data-ttu-id="5f604-126">Ciljni projekt</span><span class="sxs-lookup"><span data-stu-id="5f604-126">Target Project</span></span> |


- <span data-ttu-id="5f604-127">**{"clearTeamsAndAssignments":true}** : privzeto vedenje za spletni projekt, ki odstrani vse naloge in člane ekipe.</span><span class="sxs-lookup"><span data-stu-id="5f604-127">**{"clearTeamsAndAssignments":true}** : Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="5f604-128">**{"removeNamedResources":true}** Privzeto vedenje za aplikacijo Project Operations, ki povrne naloge nazaj na splošne vire.</span><span class="sxs-lookup"><span data-stu-id="5f604-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="5f604-129">Za več informacij o dejanjih glejte [Uporaba dejanj spletnega API-ja](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="5f604-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="5f604-130">Določi polja za kopiranje</span><span class="sxs-lookup"><span data-stu-id="5f604-130">Specify fields to copy</span></span> 
<span data-ttu-id="5f604-131">Ko je dejanje klicano, si bo dejanje **Kopiraj projekt** v projektnem pogledu ogledalo **Kopiraj projektne stolpce** , da bo določilo, katera polja kopirati pri kopiranju projekta.</span><span class="sxs-lookup"><span data-stu-id="5f604-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
