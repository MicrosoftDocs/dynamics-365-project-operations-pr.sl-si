---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 42, V3
description: Ta tema navaja funkcije in popravke, ki so na voljo v izdaji posodobitve 42, V3 storitve Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589216"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation 42, V3. Številka graditve te različice je V3.10.73.61 in je na splošno na voljo prek samostojne posodobitve v aprilu 2022.

## <a name="update-release-42"></a>Izdaja posodobitve 42

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:

**Čas in strošek**

- Ko je časovni list zavrnjen, je uporabnik, ki ga je zavrnil, napačno identificiran kot **sistem**.
- Ko so uvoženi časovni vnosi, se **Kategorija vira** manjka vrednost.
- Odobritelji projektov lahko odobrijo predložene projekte, če njihova dovoljenja niso posebej nastavljena **Lahko odobri**.

**Prodaja**

- Ko so dejanski podatki prijavljeni za naloge na nekorenski ravni, so dejanski stroški napačno združeni.
