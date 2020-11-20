---
title: Pregled sledenja projektom
description: Ta tema vsebuje informacije o spremljanju napredku projekta in porabi stroškov.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f159ecac53b824ef208221bb14958923fb5da63b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127389"
---
# <a name="project-tracking-overview"></a>Pregled sledenja projektom

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Potreba po spremljanju napredka v primerjavi z razporedom se razlikuje glede na panogo. V nekaterih panogah spremljanje poteka na zelo podrobno ravni, v drugih panogah pa na bolj splošni ravni. V tej temi je prikazan način razporejanja, s katerim boste izpolnili zahteve vaše organizacije.

## <a name="effort-tracking-view"></a>Pogled sledenja obsegu dela

Pogled **Sledenje obsegu dela** sledi napredku pri opravil na razporedu tako, da primerja dejanske ure dela, porabljene za opravilo, z načrtovanimi urami dela. Dynamics 365 Project Operations za izračun metrike sledenja uporablja te formule:

- **Odstotek napredka** = dejanski obseg dela do danes ÷ ocena končnih stroškov (EAC) 
- **Predvideni obseg dela do zaključka (ETC)** = načrtovani obseg dela – dejanski obseg dela do danes 
- **Ocena končnih stroškov (EAC)** = preostali obseg dela + dejanski obseg dela do danes 
- **Predvideni odmik od obsega dela** = načrtovan obseg dela – ocena končnih stroškov

Project Operations prikaže projekcijo odmika od obsega dela v opravilu. Če je ocena končnih stroškov večja od načrtovanega obsega dela, bo opravilo predvidoma trajalo dlje časa, kot je bilo prvotno načrtovano, in zamuja načrtovani rok. Če je ocena končnih stroškov manjša od načrtovanega obsega dela, bo opravilo predvidoma trajalo manj časa, kot je bilo prvotno načrtovano, in bo opravljeno pred predvidenim rokom.

## <a name="reprojecting-effort"></a>Vnovična projekcija obsega dela

Vodje projektov pogosto popravijo prvotne ocene v opravilu. Vnovične projekcije projekta so dojemanje ocen vodje projekta glede na trenutno stanje projekta. Vendar odsvetujemo, da vodje projektov spreminjajo osnovne številke. Namreč zato, ker osnova projekta predstavlja zanesljiv vir ocene razporeda in stroškov za projekt, s katerim so se strinjale vse zainteresirane skupine, ki sodelujejo v projektu.

Projektni vodja lahko znova projicira obseg dela v opravilih na dva načina:

- Preglasi lahko privzeti ETC z novo oceno dejanskega preostalega obsega dela v opravilu. 
- Preglasi lahko privzeti odstotek napredka z novo oceno dejanskega napredka v opravilu.

Vsak pristop povzroči ponoven izračun ETC, EAC in odstotka napredka ter predvidenega odmika od obsega dela v opravilu. Ponovno se izračunajo tudi EAC, ETC in odstotek napredka v opravilih povzetkov, kar ustvari novo projekcijo odmika od obsega dela.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Vnovična projekcija obsega dela v opravilih povzetka

Obseg dela v opravilih povzetka ali vsebnika je mogoče znova projicirati. Ne glede na to, ali uporabnik za ponovno projiciranje v opravilih povzetka uporabi preostali obseg dela ali odstotek napredka, se začne naslednji niz izračunov:

- Izračunajo se EAC, ETC in odstotek napredka v opravilu.
- Novi EAC se porazdeli na podrejena opravila v enakem razmerju kot pri prvotnem EAC v opravilu.
- Izračuna se nova ocena končnih stroškov za vsako posamezno opravilo do opravil v listnem vozlišču. 
- Prizadeta podrejena opravila do listnih vozlišč imajo svoj ETC in odstotek napredka, ki je znova izračunan na podlagi vrednosti EAC. Zato pride do nove projekcije odmika od obsega dela za opravilo. 
- Znova se izračunajo vrednosti EAC opravil povzetka vse do korenskega vozlišča.

### <a name="cost-tracking-view"></a>Pogled za sledenje stroškom 

Pogled **Sledenje stroškom** primerja dejanske stroške, ki so bili porabljeni v opravilu, z načrtovanimi stroški opravila. 

> [!NOTE]
> Ta pogled prikazuje samo stroške dela in ne vključuje ocen stroškov. Project Operations za izračun metrike sledenja uporablja te formule:

- **Odstotek porabljenih stroškov** = dejanski stroški, porabljeni do danes ÷ ocena končnih stroškov
- **Stroški do zaključka (CTC)** = načrtovani stroški – dejanski stroški, porabljeni do danes
- **Ocena končnih stroškov (EAC)** = preostali stroški + dejanski stroški, porabljeni do danes
- **Predvideni odmik od stroškov** = načrtovani stroški – ocena končnih stroškov

Projekcija odmika od stroškov je prikazana v opravilu. Če je ocena končnih stroškov večja od načrtovanih stroškov, bo opravilo predvidoma stalo več, kot je bilo prvotno načrtovano. Torej presega proračun. Če je ocena končnih stroškov manjša od načrtovanih stroškov, bo opravilo predvidoma stalo manj, kot je bilo prvotno načrtovano. Torej ni preseglo proračuna.

## <a name="project-managers-reprojection-of-cost"></a>Ponovna projekcija stroškov vodje projekta

Pri ponovni projekciji obsega dela so v pogledu **Sledenje stroškom** znova izračunani CTC, ocena končnih stroškov, odstotek porabljenih stroškov in predvideni odmik od stroškov.

## <a name="project-status-summary"></a>Povzetek stanja projekta

Sledenje podatkom v pogledih **Sledenje obsegu dela** in **Sledenje stroškom** prikaže napredek in porabo stroškov na ravneh korenskega vozlišča, opravil povzetka in opravil v listnem vozlišču. Razdelek **Stanje** na stran **Entiteta projekta** prikazuje povzetek stanja na ravni projekta.

## <a name="status-summary-fields"></a>Polja s povzetkom stanja

Polje **Splošno stanje projekta** je polje, ki ga je mogoče urejati in ki prikazuje splošno stanje projekta. Uporablja barvno kodiranje, na primer zeleno, rumeno in rdečo barvo, za označevanje naraščajočega tveganja. Polje **Komentarji** omogoča vodji projekta, da vnese določene komentarje o stanju. Polja **Stanje posodobljeno dne** ni mogoče urejati, vrednost pa je časovni žig, ki označuje, kdaj je bilo stanje nazadnje posodobljeno.

Polji **Učinkovitost razporeda** in **Stroškovna učinkovitost** sta nastavljeni iz datuma sledenja. Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče v pogledu **Sledenje obsegu dela** pozitivni, lahko polji nastavite na **Pred**. Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče negativni, ju lahko nastavite na **Za**.
