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
