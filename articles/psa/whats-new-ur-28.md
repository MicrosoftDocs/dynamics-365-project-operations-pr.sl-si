---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 28, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 28.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b06a5ee6d0e2da76801a36701f38f1885d6c7562
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010536"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

Ta tema navaja funkcije in popravke, ki so novi ali spremenjeni za aplikacijo Project Service Automation V3, izdaja posodobitve 28. Ta različica ima številko graditve V3.10.46.32 in je na splošno na voljo s samoposodobitvijo januarja 2021.

## <a name="update-release-28"></a>Izdaja posodobitve 28

### <a name="bug-fixes"></a>Popravki napak

**Čas in strošek**

Odpravljene so naslednje težave:

- Uporabniki lahko za posodobitev časovnih vnosov, ki do bili odobreni in poslani, uporabijo **Množično urejanje**.

**Vodenje projektov**

Odpravljene so naslednje težave:

- V primerih, ko je GUID opravila interpretiran kot številka, opravil ni mogoče odpreti za urejanje z uporabo možnosti **Uredi opravilo** na traku na strani **Strukturirana členitev dela**.

**Sales**

Odpravljene so naslednje težave:

- Ko je priklican vtičnik **GetEstimatesForProject**, je ustvarjena izjema s sklicem »null«.
- Možnost **Označi kot pripravljeno za izdajanje računov** na mreži mejnika samo delno posodobi atribute, razen atributa **Status računa**, ki je posodobljen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]