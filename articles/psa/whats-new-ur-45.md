---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 45, V3
description: Ta članek navaja funkcije in popravke, ki so na voljo v izdaji posodobitve 45, V3 storitve Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169189"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 45, V3. Različica z delovno številko V3.10.76.168 je julija 2022 na voljo s samoposodobitvijo.

## <a name="update-release-45"></a>Izdaja posodobitve 45

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:

**Prodaja**

- Uporabniki ne morejo uspešno ustvariti računov, potem ko so poskusili ustvariti račun brez neobračunane prodaje, če si hkrati ogledujejo isti primerek strani in ne osvežijo.

**Čas in strošek**

- Ko so omogočene sodobne odobritve in je odobrena preklicana odobritev projekta, se stopnja zapisa nepravilno posodobi na **Zahteva za preklic odobrena**.
- Ko so sodobne odobritve omogočene in so Tokovi za oblak neaktivni, postopek odobritve ni uspešen, uporabniki, ki predložijo ali odobrijo, pa niso obveščeni.
