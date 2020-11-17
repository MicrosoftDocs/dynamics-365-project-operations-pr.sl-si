---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 16, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 16.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f277d23e3fb0517f072e51f6f80f855479ab8189
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084715"
---
# <a name="project-service-automation-update-release-16-v3"></a>Izdaja posodobitve 16 za Project Service Automation, V3

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.  Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev prednostne rešitve](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za PSA V3, izdaja posodobitve 16. Ta različica ima številko graditve V3.10.6.34 in je splošno na voljo s samostojno posodobitvijo v januarju 2020.


## <a name="update-release-16"></a>Izdaja posodobitve 16

### <a name="bug-fixes"></a>Popravki napak

-   Čas in strošek

    -   Popravljeno: Uporabniki, ki poskušajo predložiti izbrisane vnose za čas in stroške za odobritve, bodo zdaj prejeli ustrezna sporočila o napaki.

-   Vodenje projektov

    -   Popravljeno: Enote vira, ki so v predlogah določene za člane skupine, se spoštujejo, predloge pa se uporabijo za nov projekt.

    -   Popravljeno: Izboljšano upravljanje ponovne dodelitve lastništva zapisov.

    -   Popravljeno: Projektov, ki so v postopku kopiranja, ne bo dovoljeno kopirati, dokler se ne končajo vse operacije kopiranja.

-   Upravljanje virov

    -   Popravljeno: Podaljšanje rezervacij zdaj pravilno upravlja s kratkimi obdobji in za podaljšane rezervacije ne ustvarja več nič ur.

    -   Popravljeno: Pogled usklajevanja je zdaj ustvarjen, ko je časovni pas projekta +5.30 GMT in čas uporabnika drugačen.

-   Sales

    -   Popravljeno: Ko je projekt, preslikan na podrobnosti pogodbe, odstranjen in nov projekt preslikan, dejanski zapisi o novem projektu niso bili ponovno ocenjeni na podlagi pravil za obračunavanje in določanje cen, določenih v podrobnostih pogodbe. To je bilo v tej izdaji popravljeno. Cene in dejanski zapisi glede na novo preslikanega projekta bodo razveljavljeni in ponovno pravilno ustvarjeni na podlagi pravil za določanje cen in obračunavanje iz podrobnosti pogodbe. Tudi dejanski zapisi nepreslikanega projekta bodo posledično ponovno ovrednoteni in na novo ustvarjeni.

    -   Popravljeno: V polje **Znesek** vrstice ocene je bila dodana dodatna potrditev za zagotovitev, da se ničelne vrednosti ne ohranijo.

    -   Popravljeno: Ko so bile posodobljene dejanske vrednosti o projektu, je bil v glavni obrazec projekta dodan gumb za osvežitev, ki uporabnikom omogoča ponovno sinhronizacijo dejanskih vrednosti.

    -   Popravljeno: Ko uporabniki nadgradijo z 2.X na 3.X, bodo dovoljeni projekti z vrednostjo NULL za ime projekta.
