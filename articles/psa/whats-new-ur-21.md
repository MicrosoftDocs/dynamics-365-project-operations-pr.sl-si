---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 21, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 21.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 69b592db7456bf11c2e933256569d726056d1a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280643"
---
# <a name="project-service-automation-update-release-21-v3"></a>Izdaja posodobitve 21 za Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365. Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti. Ta izdaja je združljiva s storitvijo Dynamics 365 9.x. Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev. Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 21. Številka graditve te različice je V3.10.32.50 in je na splošno na voljo prek samostojne posodobitve junija 2020.

## <a name="update-release-21"></a>Izdaja posodobitve 21

### <a name="bug-fixes"></a>Popravki napak

**Čas in strošek**

Odpravljene so naslednje težave:

- Ko gostite **Nadzor mreže časovnih vnosov** na nadzornih ploščah, mreža ne uporablja celotne širine vsebnika nadzorne plošče.
- Za določene časovne pasove **Nadzor mreže časovnih vnosov** ne prikazuje zapisov.
- Časovni vnosi po 21. uri se prikažejo na napačen dan.
- Če stroškovna kategorija **Zahtevano potrdilo o prejemu stroškov** nima vrednosti, uporabniki ne morejo poslati stroškov.

**Upravljanje virov**

Odpravljene so naslednje težave:

- Neaktivne rezervacije so prikazane v pogledu **Uskladitev**.
- Za dopolnitev splošnega vira je manjkala potrditev, da bi zagotovili veljaven status rezervacije.

**Vodenje projektov**

Odpravljene so naslednje težave:

- Mreže obrazca **Projekt** (**Dodelitev vira**, **Opravilo**, **Pogled** Uskladitev, **Ocene stroškov**) je mogoče urejati, tudi ko projekt ni aktiven.
- Podvojenih strank ni mogoče združiti s strankami, ki so povezane s potrjenimi pogodbami projekta.
- Ko je dodan vir, ki nima veljavnega koledarja, se v sistemu ne prikaže uporabniku prijazno sporočilo o napaki.
- Gumb **Dodaj opravilo** na mreži opravil je omogočen, ko je projekt povezan z dodatkom za **Microsoft Project**.
- Obseg dela raste nenadzorovano, ko je naloga s kategorijo dodeljena viru z vlogo, za katero je določena stroškovna cena.

**Sales**

Uvedene izboljšave:

- Vrstici **Pogostost izdajanja računov** in **Začetni datum obračunavanja** sta bili premaknjeni v zavihek **Razpored izdajanja računov**.

Odpravljene so naslednje težave:

- **Skupna prodajna cena** je enaka nič (0) za **Kategorijo** čeprav ima **Vloga** skupno prodajno ceno, ki ni enaka nič.
- Ko drug prilagojen postopek posodablja dodatno polje, stranke ne morejo spremeniti vrednosti polja **Stanje računa** na polje **Pripravljeno za izdajo računa**.
- Gumb **Osvežitev transakcij vrstice računa** lahko ob večkratni izbiri ustvari več podvojenih vrstic.
- Gumb **Posodobi cene** ne deluje v obrazcu **Hiter pogled** v podmreži **Cene vlog**.
- Logika **Razrešitve prodajnega cenika** nepravilno obdeluje časovne pasove, zaradi česar je izbor cenikov napačen.
- **Skupni dejanski stroški** projekta imajo lahko delno napako po odobritvi enkratnega vnosa.
- Znotraj logike **Razrešitve cen** se ne prikaže uporabniku prijazno sporočilo o napaki, če razdelek **Pridobljena cena vloge** nima vrednosti v poljih **Glavna enota** in **Cena v osnovni enoti**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]