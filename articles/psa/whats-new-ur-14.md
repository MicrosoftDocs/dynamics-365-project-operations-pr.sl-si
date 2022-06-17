---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 14, V3
description: Ta članek vsebuje informacije o tem, kaj je novega v posodobitvi Project Service Automation, izdaja 14 V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e8e5132f970e3ec5742842175c118faf98a7b079
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926566"
---
# <a name="project-service-automation-update-release-14-v3"></a>Izdaja posodobitve 14 za Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Dynamics 365 Project Service Automation (PSA). Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tem članku so navedene funkcije in popravki, ki so novi ali spremenjeni za PSA V3, posodobitev izdaje 14. Ta različica ima številko graditve V3.10.4.21 in je na voljo po naslednjem razporedu:

- **Splošna razpoložljivost (samostojna posodobitev):** januar 2020
- **Samodejna posodobitev:** februar 2020

## <a name="update-release-14"></a>Izdaja posodobitve 14

### <a name="enhancements"></a>Izboljšave

- Sales

     - Vrednosti polja po meri iz **Podrobnosti vrstice ponudb** so kopirane v **Podrobnosti vrstice projektne pogodbe**, ko je ponudba posodobljena na **Zaprto kot dobljeno**.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
