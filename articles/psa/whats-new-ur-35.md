---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 35, V3
description: V tem članku so navedene funkcije in popravki, ki so na voljo v Microsoft Dynamics 365 Project Service Automation Posodobitev izdaja 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 28b4a5ccbfff83c9b1a18cb0b4062af9cdaf8f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912858"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem objavljamo najnovejšo posodobitev za aplikacijo Microsoft Dynamics 365 Project Service Automation. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Združljiva je z s storitvijo Dynamics 365 9.x. Če želite posodobiti to različico, obiščite spletno stran rešitev za Skrbniško središče za Dynamics 365 in namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za posodobitev Project Service Automation, izdaja 35, V3. Različica z delovno številko V3.10.56.110 je septembra 2021 na voljo s samoposodobitvijo.

## <a name="update-release-35"></a>Izdaja posodobitve 35

### <a name="bug-fixes"></a>Popravki napak

Odpravljene so naslednje težave:

**Čas in strošek**

- Odobritelj projekta prejme napako pravice za branje, ko z vlogo **Odobritelj projekta** odobri vnose stroškov.
- Odobritelj projekta prejme napako pravice za pisanje na **msdyn_projectapproval**, ko z vlogo **Odobritelj projekta** prekliče potrjeni časovni vnos.
- Ko v modulu aplikacije Project Resource Hub v storitvi Dynamics 365 for phone v časovnem vnosu izberete **Kopiraj teden**, se pojavi naslednja napaka: »...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE.«
- Pravilnik **Poskusi znova** samodejno odobri vnose, ki so prej bili zavrnjeni.
- Podmreža **Kompleti odobritve** prikazuje neustrezna dejanja traku.
- Manjkajo ikone za **Projektno opravilo** in **Vloga virov** v entiteti **Vnos časa**.
- Ko uvozite dodelitve virov, uvoženi časovni vnosi nimajo pravilnega trajanja za dodelitve, ki so bile ustvarjene z opravili ročnega ustvarjanja.
- Na strani **Napredno iskanje zapisov vnosa časa** manjka možnost **Izbriši**.
- Na strani **Podatki o vnosu časa** manjka možnost **Shrani**. Ta težava preprečuje shranjevanje sprememb, ko je stran zaprta.

**Načrtovanje projekta**

- Mreži **Dodelitev vira** in **Usklajevanje virov** ne razvrščata združenih atributov po abecedi.
- Opravil ni mogoče ustvariti, če je vedenje datuma prilagojeno za **Samo datum**.

**Upravljanje virov**

- Če sta nameščeni tako storitev Dynamics 365 Field Service kot Project Service Automation, pride do težav s prekrivanjem, ko je **Povezani pogled za zahtevan pogoj za vir** povezan z glavno stranjo.
- Dvoklik možnosti **Shrani** v pogovornem oknu **Hitro ustvarjanje člana ekipe** preprečuje ustvarjanje pogojev za vire.

**Prodaja**

- Če izbrišete opravilo, povezano s citatom, ki ima status **Pridobljen**, se pojavi izjema.
