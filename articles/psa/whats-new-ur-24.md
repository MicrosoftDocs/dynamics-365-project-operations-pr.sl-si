---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 24, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 24.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c789a65f1996d082410b3d8dd9e76e5065e708a2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280508"
---
# <a name="project-service-automation-update-release-24-v3"></a>Izdaja posodobitve 24 za Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 24. Ta različica ima številko graditve V 3.10.42.43 in je splošno na voljo s samostojno posodobitvijo od oktobra 2020.

## <a name="update-release-24"></a>Izdaja posodobitve 24

### <a name="bug-fixes"></a>Popravki napak

**Sales**

Odpravljene so naslednje težave:

- Težava pri nastavljanju privzetega cenika izdelkov.
- Pridobivanje ponudb je počasno zaradi vdelanega cenika in kopij zapisov o cenah vlog.
- **Projektna pogodba/središče za prodajo** > **Vrstična postavka izdelka/količina vrstice naročila** se samodejno zaokroži na najbližje celo število.
- Povišanje sistemskih pravic pri branju cenikov.
- Kopiranje polj naslova stranke **address1_freighttermscode** in **address1_shippingmethodcode** v ponudbo/naročilo. 


**Čas in strošek**

Odpravljene so naslednje težave:

- **Mreža časovnih vnosov** ne podpira vedenja časa **Samo datum**.
- **Časovni vnos** se ne osvežuje samodejno. Potrebno je ročno osveževanje.
- Časovnih vnosov iz dodelitve ni mogoče uvoziti, ko je v dodelitvah vira premor (0 ur).
- Nastavitev začetka, da bo enak kot **msdyn_date**, pri ustvarjanju časovnega vnosa.
- Ponovno omogočanje množičnega urejanja časovnih vnosov.

**Upravljanje virov**

Odpravljene so naslednje težave:

- Poskus posodobitve stanja dnevne rezervacije brez zahteve povzroči izjemo sklica »null«.
- Pri nalaganju možnosti **Pogled za usklajevanje** se pojavi napaka.


**Vodenje projektov**

Odpravljene so naslednje težave:

- Pri preklopu z možnosti **Ročno** na **Samodejno** v možnosti **Razpored projektov** se samodejno shranjevanje ne dokonča.
- Stroški ne bi smeli biti vračunani v odstopanje v razdelku **Mreža za sledenje projektom**.
- Nedosledno vedenje stolpcev **Oznaka ocene** med obremenitvijo v primerjavi s spremembo vrste **Časovni razpored**.
- Dejanski stroški projekta morda ne odražajo skupnega zneska v razdelku **Dejanske vrednosti**.
- **Predvideni končni datum** na zavihku **Povzetek** se ne ujema z možnostjo **Urnik SČD**.
- Možnost **Posodobi dejanske ure** pri primikanju ne deluje pravilno.
- Vodja projekta zunaj korenske **poslovne enote** ne more ustvariti projekta.
- Spremembe opravila ali kategorije v razdelku **Ocene stroškov** se ne ohranijo.
- **Kopija pogodbe** kopira razporede računov in stanje izvajanja.
- Gumb **Osveži dejanske podatke** napačno izračuna opravila povzetka.
- Dodatek za Microsoft Project: popravek napake s sklicem »null«, če ima kateri koli član ekipe prazno enoto vira.



[!INCLUDE[footer-include](../includes/footer-banner.md)]