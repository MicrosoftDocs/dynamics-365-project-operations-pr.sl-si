---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 31, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 31.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945555"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Novosti ali spremembe v izdaji posodobitve za Project Service Automation 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 31. Številka graditve te različice je V3.10.52.77 in je na splošno na voljo prek samostojne posodobitve maja 2021.

## <a name="update-release-31"></a>Izdaja posodobitve 31

### <a name="bug-fixes"></a>Popravki napak

**Čas in strošek**

Odpravljene so naslednje težave:

- Ukazni gumbi za nadzor vnosa časa na strani **Vir, ki ga je mogoče rezervirati** so povzročali zmedo.
- V entiteti **Project.SetTrackingFields** je bila pri potrjevanju časovnega vnosa ustvarjena izjema z referenco z vrednostjo »null«.

**Upravljanje virov**

Odpravljene so naslednje težave:

- V možnosti **Ustvari člana ekipe** niso pravilno prikazani metapodatki za nastavitev rezervacije za **Privzeto stanje prevzete rezervacije**.
- Pri nadgradnji iz PSA 1.X na 3.X postopek nadgradnje ne uspe pri elementu **UpgradeResourceRequirements**.


**Prodaja**

Odpravljene so naslednje težave:

- Dejanski prihodek v mreži za sledenje pretvori zneske v valuto projekta.
- Privzeta valuta ni jasno določena pri ustvarjanju vrstic dnevnika, vrstic ponudb in podrobnosti pogodbe v primerih, kjer se osnovna valuta organizacije razlikuje od valute projekta.
- Poizvedba za **Čakanje na potrditev dnevnika popravkov** ne filtrira po projektu.
- Preostanek prodaje projekta se napačno izračuna.
- Ponudbe na podlagi stika niso uspešne, če so ustvarjene brez cenika.
- Ob izbiri možnosti **Potrdi račun** se ne prikaže vrtavka obdelovanja.
- Ob izbiri možnosti **Ustvari račun** se ne prikaže vrtavka obdelovanja.
- Zapiranje ponudbe s stanjem »izgubljena« ne prekliče rezervacij.






