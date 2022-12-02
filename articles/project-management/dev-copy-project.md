---
title: Razvoj predlog projekta s funkcijo »Kopiraj projekt«
description: Ta članek vsebuje informacije o tem, kako ustvariti predloge projektov z uporabo dejanja po meri »Kopiraj projekt«.
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

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Parametri vnosa

Na voljo so trije parametri za vnos:

- **ReplaceNamedResources** ali **ClearTeamsAndAssignments** – Nastavite samo eno od teh možnosti. Ne nastavite obeh.

    - **\{"ReplaceNamedResources":true\}** – Privzeto vedenje za aplikacijo Project Operations. Poimenovani viri so zamenjani s splošnimi viri.
    - **\{"ClearTeamsAndAssignments":true\}** – Privzeto vedenje za storitev Project for the Web. Vsa opravila in člani ekipe so odstranjeni.

- **SourceProject** – Sklic entitete izvornega projekta, v katerega se kopira. Ta parameter ne sme imeti vrednosti »null«.
- **Target** – Sklic entitete ciljnega projekta, v katerega se kopira. Ta parameter ne sme imeti vrednosti »null«.

Naslednja tabela prikazuje povzetek treh parametrov.

| Parameter                | Vnesi             | Vrednost                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Logično          | **True** ali **False** |
| ClearTeamsAndAssignments | Logično          | **True** ali **False** |
| SourceProject            | Sklic na entiteto | Izvorni projekt    |
| Cilj                   | Sklic na entiteto | Ciljni projekt    |

Za več informacij o dejanjih glejte [Uporaba dejanj spletnega API-ja](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Preverjanje veljavnosti

Opravijo se naslednja preverjanja veljavnosti.

1. »Null« preveri in pridobi izvorni in ciljni projekt, da potrdi obstoj obeh projektov v organizaciji.
2. Sistem preveri, ali je ciljni projekt veljaven za kopiranje, tako da preveri naslednje pogoje:

    - Na projektu ni predhodnih dejavnosti (vključno z izborom zavihka **Opravila**) in projekt je na novo ustvarjen.
    - Ni prejšnjih kopij, za ta projekt ni bil zahtevan noben uvoz in projekt nima stanja **Ni uspelo**.

3. Postopek se ne kliče z uporabo HTTP.

## <a name="specify-fields-to-copy"></a>Določi polja za kopiranje

Ko je dejanje klicano, si bo dejanje **Kopiraj projekt** v projektnem pogledu ogledalo **Kopiraj projektne stolpce**, da bo določilo, katera polja kopirati pri kopiranju projekta.

### <a name="example"></a>Primer

V spodnjem primeru je prikazano, kako prikličete dejanje po meri **CopyProjectV3** z nastavljenim parametrom **removeNamedResources**.

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
