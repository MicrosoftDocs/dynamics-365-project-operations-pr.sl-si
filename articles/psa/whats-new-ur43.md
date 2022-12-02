---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 43, V3
description: Ta članek navaja funkcije in popravke, ki so na voljo v izdaji posodobitve 43, V3 storitve Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/04/2022
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
ms.openlocfilehash: b12cfda08f1ea1fc441782003130be445a437f7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915342"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-43-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 43, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 43, V3. Številka graditve te različice je V3.10.74.200 in je na splošno na voljo prek samostojne posodobitve maja 2022.

## <a name="update-release-43"></a>Izdaja posodobitve 43

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:


**Čas in strošek**

- Pri uvažanju časovnih vnosov iz rezervacij ali dodelitev virov se sklic na povezani vir, ki ga je mogoče rezervirati, ne ohrani.
- Ko je mreža za časovni vnos razširjena na celoten zaslon, krmarjenje po mreži s tabulatorko ne deluje.
- Ko oddate časovni vnos, ki ga ustvari drug uporabnik, se polje **Oddal(-a)** nepravilno izpolni z uporabnikom, ki je ustvaril časovni list.
