---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 41, V3
description: Ta tema navaja funkcije in popravke, ki so na voljo v izdaji posodobitve 41, V3 storitve Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580982"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 41, V3. Ta različica ima številko graditve V3.10.62.162 in je splošno na voljo s samostojno posodobitvijo v marcu 2022.

## <a name="update-release-41"></a>Izdaja posodobitve 41

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:

**Vodenje projektov**
- Ko poskušate ustvariti projekt iz predloge, ki temelji na projektu, ustvarjenem z namizni dodatki, se prikaže naslednja napaka: »Preverjanje polja načrtovanega dela za dodelitev sredstev: Končni datum vsake časovne rezine dodelitve vira ne sme biti prej kot njen začetni datum Datum".

**Čas in strošek**
- Ko poskušate izbrisati časovni vnos, se prikaže naslednje sporočilo o napaki: »Prišlo je do nepričakovane napake iz kode ISV«.

**Prodaja**
- Ko ustvarite račun za mejnik s fiksno ceno, **Opis** in **Zunanji opis** polja niso zapolnjena. 
