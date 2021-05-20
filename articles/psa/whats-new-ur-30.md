---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 30, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 30.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852895"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 30. Številka graditve te različice je V3.10.51.61 in je na splošno na voljo prek samostojne posodobitve v aprilu 2021.

## <a name="update-release-30"></a>Izdaja posodobitve 30

### <a name="bug-fixes"></a>Popravki napak

**Čas in strošek**

Odpravljene so naslednje težave:

- Napaka se pojavi, ko ustvarite in shranite vnos časa na strani **Hitro ustvarjanje**, če je polje **Vloga** odstranjeno.
- Filter za vnos časa uporablja napačen operator filtra.
- Kopirani časovni listi niso samodejno prikazani, ko izberete **Kopiraj teden** pri kontrolniku za vnos časa.

**Upravljanje virov**

Odpravljene so naslednje težave:

- Ko podaljšate rezervacijo, je stanje rezervacije, dodeljeno veljavni rezervacije, napačno. Podaljšanje rezervacije upošteva stanje rezervacije, opredeljeno kot **Potrjeno** v metapodatkih o nastavitvi rezervacije.
- Če veljavno stanje rezervacije ni določeno, sporočilo o napaki ni pravilno lokalizirano.

**Vodenje projektov**

Odpravljene so naslednje težave:

- Projektov ni mogoče ustvariti v eni valuti in vključujejo povezane naloge v drugi valuti.

**Prodaja**

Odpravljene so naslednje težave:

- Ko se cenik kopira, se cene ne posodabljajo.
- Zaključevanje ponudbe kot neuspešne ne uspe, če ima podrobnost o ceni vrednost za izvor.
- Pri entiteti **Projektno opravilo** so bili **Ocenjeni stroški** preimenovani v možnost **Načrtovani stroški (osnova)**.
- Izjema z referenco z vrednostjo »null« se ustvari, ko se računi ustvarijo ali izbrišejo.