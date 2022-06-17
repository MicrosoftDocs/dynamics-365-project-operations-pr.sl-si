---
title: Razvoj predlog projekta s funkcijo »Kopiraj projekt«
description: Ta članek vsebuje informacije o tem, kako ustvariti predloge projektov z dejanjem po meri Kopiraj projekt.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923852"
---
# <a name="develop-project-templates-with-copy-project"></a>Razvoj predlog projekta s funkcijo »Kopiraj projekt«

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dynamics 365 Project Operations podpira možnost kopiranja projekta in vračanja opravil v splošne vire, ki predstavljajo vlogo. Stranke lahko to funkcijo uporabijo za izdelavo osnovnih predlog projekta.

Ko izberete **Kopiraj projekt**, se posodobi stanje ciljnega projekta. Uporabite **Razlog stanja**, da ugotovite, kdaj je dejanje kopiranja končano. Z izbiro funkcije **Kopiraj projekt** boste tudi posodobili začetni datum projekta na trenutni začetni datum, če v ciljni projektni entiteti ni zaznan noben ciljni datum.

## <a name="copy-project-custom-action"></a>Dejanje po meri »Kopiraj projekt«

### <a name="name"></a>Imenu 

msdyn\_ CopyProjectV3

### <a name="input-parameters"></a>Parametri vnosa

Na voljo so trije parametri za vnos:

- **ReplaceNamedResources** oz **ClearTeamsAndAssignments** – Nastavite samo eno od možnosti. Ne nastavite obojega.

    - **\{"ReplaceNamedResources":true\}** – Privzeto vedenje za projektne operacije. Vsi poimenovani viri se nadomestijo s splošnimi viri.
    - **\{"ClearTeamsAndAssignments":true\}** – Privzeto vedenje za Project za splet. Vse naloge in člani ekipe so odstranjeni.

- **SourceProject** – Sklic entitete izvornega projekta, iz katerega želite kopirati. Ta parameter ne more biti nič.
- **Tarča** – Referenca entitete ciljnega projekta, na katero se kopira. Ta parameter ne more biti nič.

Naslednja tabela ponuja povzetek treh parametrov.

| Parameter                | Vnesi             | Vrednost                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Logično          | **Prav** oz **Napačno** |
| ClearTeamsAndAssignments | Logično          | **Prav** oz **Napačno** |
| SourceProject            | Sklic na entiteto | Izvorni projekt    |
| Cilj                   | Sklic na entiteto | Ciljni projekt    |

Za več privzetih nastavitev za dejanja glejte [Uporabite dejanja spletnega API-ja](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Validacije

Opravljene so naslednje validacije.

1. Null preveri in pridobi izvorne in ciljne projekte, da potrdi obstoj obeh projektov v organizaciji.
2. Sistem potrdi, da je ciljni projekt veljaven za kopiranje, tako da preveri naslednje pogoje:

    - Na projektu ni nobene prejšnje aktivnosti (vključno z izbiro **Naloge** zavihek), projekt pa je na novo ustvarjen.
    - V tem projektu ni nobene prejšnje kopije, za ta projekt ni bil zahtevan uvoz in projekt nima datoteke **Neuspešno** stanje.

3. Operacija se ne kliče z uporabo HTTP.

## <a name="specify-fields-to-copy"></a>Določi polja za kopiranje

Ko je dejanje klicano, si bo dejanje **Kopiraj projekt** v projektnem pogledu ogledalo **Kopiraj projektne stolpce**, da bo določilo, katera polja kopirati pri kopiranju projekta.

### <a name="example"></a>Primer

Naslednji primer prikazuje, kako poklicati **CopyProjectV3** dejanje po meri z **odstraniNamedResources** nabor parametrov.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
