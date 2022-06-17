---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 40, V3
description: V tem članku so navedene funkcije in popravki, ki so na voljo v Microsoft Dynamics 365 Project Service Automation Posodobitev izdaja 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912812"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za posodobitev Project Service Automation, izdaja 40, V3. Ta različica ima številko graditve V3.10.61.61 in je splošno na voljo s samoposodobitvijo februarja 2022.

## <a name="update-release-40"></a>Izdaja posodobitve 40

### <a name="features"></a>Funkcije
Prva faza nadgradnje z avtomatizacije Project Service na Project Operations - Lite bo izdana februarja 2022 za vse stranke. Če želite preveriti primernost, glejte [Nadgradite s Project Service Automation na Project Operations](upgrade-project-operations-non-stocked.md). Če se aplikacija ne pojavi v vašem primeru v Power Platform Skrbniški center, se obrnite na podporo in zahtevajte, da se let omogoči za vaša okolja. Vaša zahteva mora vsebovati seznam ID-jev okolja, kjer je treba let omogočiti.

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:

**Čas in strošek**
- Vnos beležke manjka, ko je vnos časa zavrnjen ali preklican. 

**Prodaja**

- Ko posodabljate ocene stroškov ali prodaje z uporabo vtičnikov, ki so že pripravljeni, imate napačno dovoljenje za pošiljanje koristnih podatkov JSON, ki niso veljavni zunaj uporabniškega vmesnika.
- Ko posodobite vrstice ponudb s hitrim pogledom, lahko aktivirate ponudbe.
