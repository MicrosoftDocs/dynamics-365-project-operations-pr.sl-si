---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 25, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 25.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 30822ec64b31e110202a587dd941bdff60116712
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280463"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Ta tema navaja funkcije in popravke, ki so novi ali spremenjeni za Project Service Automation, različica 3, izdaja posodobitve 25. Ta različica ima številko graditve V 3.10.43.76 in je na splošno na voljo s samoposodobitvijo oktobra 2020.

## <a name="update-release-25"></a>Izdaja posodobitve 25

### <a name="bug-fixes"></a>Popravki napak

**Čas in strošek**

Ta težava je odpravljena:

- Grafikon vnosa časa, ki prikazuje dodatne podatke, ki temelji na prevelikem intervalu, ki je pridobljen.

**Upravljanje virov**

Ta težava je odpravljena:

- Dodana je koda orodja Package Deployer, da lahko preskočite uvoz popravkov rešitve Universal Resource Scheduling , če že obstaja popravek višje različice.

**Vodenje projektov**

Odpravljene so naslednje težave:

- Popravljena neskladja zaokroževanja in neskladja v menjalnem tečaju, kar povzroča nepravilno načrtovane stroške v mreži za sledenje projekta.
- Podpira zmožnost prikaza dveh ali več mrež za odzivanje v obrazcu **Projekt**.
- Zagotovljeno preverjanje veljavnosti za obravnavo zmožnosti dodeljevanja opravila mimo končnega datuma koledarja, kar povzroči neuspešno dodelitev virov.
- Izboljšano obravnavanje napak za obravnavo izjeme sklica »Null«, ustvarjene iz naslednjega:

    - Vtičnik **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** ko se projektno opravilo ustvari brez povezanega projekta
    - Vtičnik **PreProjectTeamMemberCreate**
    - Vtičnik **PostProjectTeamMemberDelete**
    - Vtičnik **PreValidateProjectTaskDelete**

**Sales**

Odpravljene so naslednje težave:

- Izboljšano obravnavanje napak za obravnavo izjeme sklica »Null«, ki jo je ustvaril **Kopiraj projekt: ocenjevanje upravljanja virov pomoči**.
- Možnost **Ni pripravljeno za izdajanje računov** v možnosti **Nedokončana opravila obračunavanja časa in materiala** ne izbriše stanja obračunavanja.
- Nepravilno označeni gumbi **Cene** na zavihku **Cena vloge** in **Katalog izdelkov** so popravljeni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]