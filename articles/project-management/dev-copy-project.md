---
title: Razvoj predlog projekta s funkcijo »Kopiraj projekt«
description: Ta tema vsebuje informacije o tem, kako ustvariti predloge projektov z uporabo dejanja po meri »Kopiraj projekt«.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949834"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="216ad-103">Razvoj predlog projekta s funkcijo »Kopiraj projekt«</span><span class="sxs-lookup"><span data-stu-id="216ad-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="216ad-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="216ad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="216ad-105">Dynamics 365 Project Operations podpira možnost kopiranja projekta in vračanja opravil v splošne vire, ki predstavljajo vlogo.</span><span class="sxs-lookup"><span data-stu-id="216ad-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="216ad-106">Stranke lahko to funkcijo uporabijo za izdelavo osnovnih predlog projekta.</span><span class="sxs-lookup"><span data-stu-id="216ad-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="216ad-107">Ko izberete **Kopiraj projekt**, se posodobi stanje ciljnega projekta.</span><span class="sxs-lookup"><span data-stu-id="216ad-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="216ad-108">Uporabite **Razlog stanja**, da ugotovite, kdaj je dejanje kopiranja končano.</span><span class="sxs-lookup"><span data-stu-id="216ad-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="216ad-109">Z izbiro funkcije **Kopiraj projekt** boste tudi posodobili začetni datum projekta na trenutni začetni datum, če v ciljni projektni entiteti ni zaznan noben ciljni datum.</span><span class="sxs-lookup"><span data-stu-id="216ad-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="216ad-110">Dejanje po meri »Kopiraj projekt«</span><span class="sxs-lookup"><span data-stu-id="216ad-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="216ad-111">Imenu</span><span class="sxs-lookup"><span data-stu-id="216ad-111">Name</span></span> 

<span data-ttu-id="216ad-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="216ad-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="216ad-113">Parametri vnosa</span><span class="sxs-lookup"><span data-stu-id="216ad-113">Input parameters</span></span>
<span data-ttu-id="216ad-114">Na voljo so trije parametri za vnos:</span><span class="sxs-lookup"><span data-stu-id="216ad-114">There are three input parameters:</span></span>

| <span data-ttu-id="216ad-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="216ad-115">Parameter</span></span>          | <span data-ttu-id="216ad-116">Vnesi</span><span class="sxs-lookup"><span data-stu-id="216ad-116">Type</span></span>   | <span data-ttu-id="216ad-117">Vrednosti</span><span class="sxs-lookup"><span data-stu-id="216ad-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="216ad-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="216ad-118">ProjectCopyOption</span></span>  | <span data-ttu-id="216ad-119">String</span><span class="sxs-lookup"><span data-stu-id="216ad-119">String</span></span> | <span data-ttu-id="216ad-120">**{"removeNamedResources":true}** ali **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="216ad-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="216ad-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="216ad-121">SourceProject</span></span>      | <span data-ttu-id="216ad-122">Sklic na entiteto</span><span class="sxs-lookup"><span data-stu-id="216ad-122">Entity Reference</span></span> | <span data-ttu-id="216ad-123">Izvorni projekt</span><span class="sxs-lookup"><span data-stu-id="216ad-123">Source Project</span></span> |
| <span data-ttu-id="216ad-124">Cilj</span><span class="sxs-lookup"><span data-stu-id="216ad-124">Target</span></span>             | <span data-ttu-id="216ad-125">Sklic na entiteto</span><span class="sxs-lookup"><span data-stu-id="216ad-125">Entity Reference</span></span> | <span data-ttu-id="216ad-126">Ciljni projekt</span><span class="sxs-lookup"><span data-stu-id="216ad-126">Target Project</span></span> |


- <span data-ttu-id="216ad-127">**{"clearTeamsAndAssignments":true}**: privzeto vedenje za spletni projekt, ki odstrani vse naloge in člane ekipe.</span><span class="sxs-lookup"><span data-stu-id="216ad-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="216ad-128">**{"removeNamedResources":true}** Privzeto vedenje za aplikacijo Project Operations, ki povrne naloge nazaj na splošne vire.</span><span class="sxs-lookup"><span data-stu-id="216ad-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="216ad-129">Za več informacij o dejanjih glejte [Uporaba dejanj spletnega API-ja](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="216ad-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="216ad-130">Določi polja za kopiranje</span><span class="sxs-lookup"><span data-stu-id="216ad-130">Specify fields to copy</span></span> 
<span data-ttu-id="216ad-131">Ko je dejanje klicano, si bo dejanje **Kopiraj projekt** v projektnem pogledu ogledalo **Kopiraj projektne stolpce**, da bo določilo, katera polja kopirati pri kopiranju projekta.</span><span class="sxs-lookup"><span data-stu-id="216ad-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="216ad-132">Primer</span><span class="sxs-lookup"><span data-stu-id="216ad-132">Example</span></span>
<span data-ttu-id="216ad-133">V spodnjem primeru je prikazano, kako pokličete dejanje po meri **CopyProject** z nastavljenim parametrom **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="216ad-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]