---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 14, V3
description: V tej temi so na voljo informacije o novostih v izdaji posodobitve za Project Service Automation 14, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084714"
---
# <a name="project-service-automation-update-release-14-v3"></a>Izdaja posodobitve 14 za Project Service Automation, V3
Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Dynamics 365 Project Service Automation (PSA). Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za PSA V3, izdaja posodobitve 14. Ta različica ima številko graditve V3.10.4.21 in je na voljo po naslednjem razporedu:

- **Splošna razpoložljivost (samostojna posodobitev):** januar 2020
- **Samodejna posodobitev:** februar 2020

## <a name="update-release-14"></a>Izdaja posodobitve 14

### <a name="enhancements"></a>Izboljšave

- Sales

     - Vrednosti polja po meri iz **Podrobnosti vrstice ponudb** so kopirane v **Podrobnosti vrstice projektne pogodbe** , ko je ponudba posodobljena na **Zaprto kot dobljeno**.
     - Potrjeni projekti so lahko označeni **Zaprto kot izgubljeno**.

- Upravljanje virov

     - Pri podaljšanju rezervacij bodo uporabniki s pogovornim oknom za potrditev pozvani, da povzamejo rezultate rezervacije in zagotovijo povezavo do upravljanja rezervacij.


### <a name="bug-fixes"></a>Popravki napak

- Čas in strošek

     - Popravljeno: izboljšana uporabniška izkušnja, ko uporabnik ne izbere nobenega vnosa za popravilo.

- Upravljanje virov

     - Popravljeno: večkratna rezervacija vira sega čez ime vira, ki ga je mogoče rezervirati.

- Sales

     - Popravljeno: skupna prodajna cena ni izračunana, dokler uporabnik ne vnese tudi lastne cene za ocene stroškov na projektu.
     - Popravljeno: zapiranje ponudbe kot **Pridobljeno** ne uspe, če povezana projektna pogodba ni v stanju **Osnutek**.

