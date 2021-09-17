---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 34, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 34.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: 528d4f8d108720cb9c912cea1c0d5f37e3716eec
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323301"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 34. Različica z delovno številko V3.10.55.38 je julija 2021 na voljo s samoposodobitvijo.

## <a name="update-release-34"></a>Izdaja posodobitve 34

### <a name="bug-fixes"></a>Popravki napak
Odpravljene so naslednje težave:

**Splošno**

- Posodobitve, ki jih vodi izdajatelj, ne aktivirajo novega sodobnega poteka dela odobritve.
- Atributi **Stanje cilja** in **Vrsta dejanja** manjkajo na glavni strani **Nabor odobritev**.

**Čas in strošek**

- Zahteve za vpoklic ni mogoče odobriti s sodobnim tokom odobritve.
- Kopiranje tedenskih časovnih vnosov ne deluje, če kopirate vnose, ki niso povezani s prijavljenim uporabnikom.

**Načrtovanje projekta**

- Pri uvozu iz dodatka na namizju Microsoft Project so krivulje dodelitve virov poškodovane.

**Upravljanje virov**

- Ko objavite projekt iz dodatka na namizne odjemalca Microsoft Project, se končni datum obstoječih zahtev spremeni.
- Decimalna natančnost presega dve decimalni mesti v pogovornem oknu za potrditev rezervacije.

**Prodaja**

- Ko pogodbi o projektu dodate vrstico, ki temelji na izdelku, z obstoječim izdelkom, se prikaže zapis **ključa ni mogoče najti v slovarju**.
- Potencialnih strank ni mogoče določiti, če je vrsta naročila preslikana iz potencialne stranke v priložnost.
