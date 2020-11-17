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
# <a name="develop-project-templates-with-copy-project"></a>Razvoj predlog projekta s funkcijo »Kopiraj projekt«

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dynamics 365 Project Operations podpira zmožnost kopiranja projekta in povrnitve morebitnih nalog nazaj na splošne vire, ki predstavljajo vlogo. Stranke lahko to funkcijo uporabijo za izdelavo osnovnih predlog projekta.

Ko izberete **Kopiraj projekt** , se posodobi stanje ciljnega projekta. Uporabite **Razlog stanja** , da ugotovite, kdaj je dejanje kopiranja končano. Z izbiro funkcije **Kopiraj projekt** boste tudi posodobili začetni datum projekta na trenutni začetni datum, če v ciljni projektni entiteti ni zaznan noben ciljni datum.

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


- **{"clearTeamsAndAssignments":true}** : privzeto vedenje za spletni projekt, ki odstrani vse naloge in člane ekipe.
- **{"removeNamedResources":true}** Privzeto vedenje za aplikacijo Project Operations, ki povrne naloge nazaj na splošne vire.

Za več informacij o dejanjih glejte [Uporaba dejanj spletnega API-ja](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Določi polja za kopiranje 
Ko je dejanje klicano, si bo dejanje **Kopiraj projekt** v projektnem pogledu ogledalo **Kopiraj projektne stolpce** , da bo določilo, katera polja kopirati pri kopiranju projekta.