---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 29, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 29.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010491"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 29. Ta različica ima številko graditve V3.10.47.7 in je splošno na voljo s samoposodobitvijo februarja 2021.

## <a name="update-release-29"></a>Izdaja posodobitve 29

### <a name="bug-fixes"></a>Popravki napak

**Čas in strošek**

Odpravljene so naslednje težave:

- Uporabniki v mreži časovnih vnosov ne vidijo delovnega časa, zabeleženega ob nedelovnih dneh.
- Odobrene vnose stroškov je mogoče urejati v mreži.

**Vodenje projektov**

Odpravljene so naslednje težave:

- Manjka logika preverjanja veljavnosti, ki zagotovi, da ure obsega dela za dodelitev virov ne morejo biti negativne.
- Dejanje po meri **AssignResourcesForTask** posodobi vsa polja namesto samo spremenjenih polj.
- Pri kopiranju projekta v okolju z vtičniki ali poteki dela, ki so registrirani z dogodkom **CreateProject**, se atribut **msdyn_bulkgenerationstatus** ne posodobi, če dejanje kopiranja **CopyWBSToProject** ne uspe.
- Ko razširite koledar projekta, se delovni dnevi ne razvrstijo po naraščajočem vrstnem redu, zaradi česar nekatere posodobitve projektnih opravil ne uspejo.
- Spreminjanje vodje projekta na obstoječem projektu sproži privzeto nastavitev organizacijske enote.

**Prodaja**

Odpravljene so naslednje težave:

- Zavihek **Izvajanje pogodbe** na strani **Pogodba** med inicializacijo tiho odpove, ko ni nobene podrobnosti pogodbe.