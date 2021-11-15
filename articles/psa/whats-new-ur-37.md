---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 37, V3
description: Ta tema navaja funkcije in popravke, ki so na voljo v izdaji posodobitve 37, V3 storitve Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727625"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 37, V3. Ta različica ima številko izdelave V3.10.58.120 in je na splošno na voljo prek samodejne posodobitve novembra 2021.

## <a name="update-release-37"></a>Izdaja posodobitve 37

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:

**Čas in strošek**
- Uporabniki ne morejo izbrisati časovnega vnosa tako, da počistijo celico.
- Pogled **Moja neuspešna odobritev** vsebuje samo odobritve projektov s statusom **Poslano**.

**Upravljanje projektov**
- Uporabniki prejmejo napako izjeme ničelnega sklica, ko odprejo projekt v namiznem dodatku Microsoft, če je ime položaja člana projektne skupine prazno.
- Na strani **Projektno opravilo** ni gumba **Shrani**, tako da uporabniki ne morejo shraniti sprememb v zapise opravil.
- Uporabniki ne morejo izbrisati projekta, ki ima opravilo, povezano s ponudbo s stanjem **Pridobljeno**.

**Prodaja**
- Polje **Valuta** na strani **Projekt** je posodobljena, da se ujema z valuto uporabljene predloge.
- Stroški so napačno izračunani za opravila, ki imajo več valut.
