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
ms.openlocfilehash: 87f10d793f9edc055444a3cecea9ea709c1fd7ff7213d6cfaf6b3cbe83a6a5a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985116"
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