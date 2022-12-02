---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 41, V3
description: Ta članek navaja funkcije in popravke, ki so na voljo v izdaji posodobitve 41, V3 storitve Microsoft Dynamics 365 Project Service Automation.
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930568"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 41, V3. Ta različica ima številko graditve V3.10.62.162 in je splošno na voljo s samostojno posodobitvijo v marcu 2022.

## <a name="update-release-41"></a>Izdaja posodobitve 41

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:

**Vodenje projektov**
- ko poskušate ustvariti projekt iz predloge, ki temelji na projektu, ustvarjenem iz namiznega vtičnika, se pojavi napaka »Preverjanje veljavnosti polja Načrtovano delo za dodelitev virov: datum konca posamezne časovne rezine dodelitve vira ne sme biti pred datumom začetka«.

**Čas in strošek**
- Ko poskušate izbrisati časovni vnos, se prikaže sporočilo o napaki »Prišlo je do nepričakovane napake v kodi ISV«.

**Prodaja**
- Ko ustvarite račun za mejnik s fiksno ceno, polja **Opis** in **Zunanji opis** niso izpolnjena. 
