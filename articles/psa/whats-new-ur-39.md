---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 39, V3
description: Ta članek navaja funkcije in popravke, ki so na voljo v izdaji posodobitve 39, V3 storitve Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922472"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 39, V3. Ta različica ima številko graditve V3.10.60.170 in je splošno na voljo s samostojno posodobitvijo v januarju 2022.

## <a name="update-release-39"></a>Izdaja posodobitve 39

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:

**Splošno**

- Na zemljevidu mesta je bilo za prevod v arabščino narejenih več izboljšav.

**Vodenje projektov**

- Napaka se pojavi, ko spremenite vodjo projekta na uporabnika, ki je že član ekipe v projektu.

**Prodaja**

- Lastnik **Cenika projektne pogodbe** je napačen, ko se cenik ustvari samodejno. 
- Datum veljavnosti cenika ni upoštevan, ko je cenik uporabljen za parameter projekta.
- Pri urejanju dveh ločenih ponudb pogodbena enota morda nima pravilne privzete vrednosti.
