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
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045029"
---
# <a name="develop-project-templates-with-copy-project"></a>Razvoj predlog projekta s funkcijo »Kopiraj projekt«

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations podpira možnost kopiranja projekta in vračanja opravil v splošne vire, ki predstavljajo vlogo. Stranke lahko to funkcijo uporabijo za izdelavo osnovnih predlog projekta.

Ko izberete **Kopiraj projekt**, se posodobi stanje ciljnega projekta. Uporabite **Razlog stanja**, da ugotovite, kdaj je dejanje kopiranja končano. Z izbiro funkcije **Kopiraj projekt** boste tudi posodobili začetni datum projekta na trenutni začetni datum, če v ciljni projektni entiteti ni zaznan noben ciljni datum.

## <a name="copy-project-custom-action"></a>Dejanje po meri »Kopiraj projekt« 

### <a name="name"></a>Imenu 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Parametri vnosa
Na voljo so trije parametri za vnos:

| Parameter          | Vnesi   | Vrednosti                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** ali **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Sklic na entiteto | Izvorni projekt |
| Cilj             | Sklic na entiteto | Ciljni projekt |


- **{"clearTeamsAndAssignments":true}**: privzeto vedenje za spletni projekt, ki odstrani vse naloge in člane ekipe.
- **{"removeNamedResources":true}** Privzeto vedenje za aplikacijo Project Operations, ki povrne naloge nazaj na splošne vire.

Za več informacij o dejanjih glejte [Uporaba dejanj spletnega API-ja](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Določi polja za kopiranje 
Ko je dejanje klicano, si bo dejanje **Kopiraj projekt** v projektnem pogledu ogledalo **Kopiraj projektne stolpce**, da bo določilo, katera polja kopirati pri kopiranju projekta.


### <a name="example"></a>Primer
V spodnjem primeru je prikazano, kako pokličete dejanje po meri **CopyProject** z nastavljenim parametrom **removeNamedResources**.
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
