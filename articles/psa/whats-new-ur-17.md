---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 17, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 17.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c2b27582a401e41da0a9e60c8f2f32dcdd1944c2
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949249"
---
# <a name="project-service-automation-update-release-17-v3"></a>Izdaja posodobitve 17 za Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.  Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za PSA V3, izdaja posodobitve 17. Ta različica ima številko graditve V3.10.6.34 in je splošno na voljo s samostojno posodobitvijo v marcu 2020.


## <a name="update-release-17"></a>Izdaja posodobitve 17

### <a name="bug-fixes"></a>Popravki napak

**Splošno**

- Popravljeno: Posodobitev aplikacije Project Service Automation za uveljavitev licenc za člane ekipe (središče za projektne vire bo vsebovalo metapodatke 3.x paketa storitve za člane ekipe)
 
**Čas in strošek**

- Popravljeno: Ocene stroškov ni mogoče spremeniti iz ničelne cene v nič (0). Ta sprememba se ne upošteva.

**Vodenje projektov**

- Popravljeno: Kontrola za ničelne vrednosti je bila dodana imenu položaja člana ekipe.
- Popravljeno: Polje **msdyn_userresourceid** v entiteti **msdyn_resourceassignment** je zastarelo.
- Popravljeno: Posodobitev z 2.x na 3.x sedaj obravnava krivulje praznega obsega dela za dodelitev opravil.

**Sales**

- Popravljeno: **Invoice.PreValidateInvoiceUpdate** sedaj obravnava scenarij ustreznega ponovnega dodeljevanja lastnikov zapisov.
- Popravljeno: Če je razred transakcije **Čas**, **UnitGroup** ni mogoče urejati za vse entitete, vključno z: **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** in **ContractLineDetails**. Vendar pa polja **Enota** ni mogoče urejati za **JournalLine** in **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]