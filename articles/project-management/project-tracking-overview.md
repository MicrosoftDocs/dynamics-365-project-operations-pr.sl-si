---
title: Sledenje obsegu projektov
description: Ta tema vsebuje informacije o spremljanju obsega projekta in napredka dela.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 037118714cf01ba2fb91cdd94345495d12ccb645
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593816"
---
# <a name="project-effort-tracking"></a>Sledenje obsegu projektov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Potreba po spremljanju napredka v primerjavi z razporedom se razlikuje glede na panogo. V nekaterih panogah spremljanje poteka na zelo podrobno ravni, v drugih panogah pa na bolj splošni ravni. V tej temi je prikazan način razporejanja, s katerim boste izpolnili zahteve vaše organizacije.

## <a name="effort-tracking-view"></a>Pogled sledenja obsegu dela

Pogled **Sledenje obsegu dela** sledi napredku pri opravil na razporedu tako, da primerja dejanske ure dela, porabljene za opravilo, z načrtovanimi urami dela. Aplikacija Dynamics 365 Project Operations za izračun metrike sledenja uporablja te formule:

- **Odstotek napredka** = dejanski obseg dela do danes ÷ ocena končnih stroškov (EAC) 
- **Preostali obseg dela** = ocena obsega končnih stroškov – dejanski obseg dela do danes 
- **Ocena končnih stroškov (EAC)** = preostali obseg dela + dejanski obseg dela do danes 
- **Predvideni odmik od obsega dela** = načrtovan obseg dela – ocena končnih stroškov

Project Operations prikaže projekcijo odmika od obsega dela v opravilu. Če je ocena končnih stroškov večja od načrtovanega obsega dela, bo opravilo predvidoma trajalo dlje časa, kot je bilo prvotno načrtovano, in zamuja načrtovani rok. Če je ocena končnih stroškov manjša od načrtovanega obsega dela, bo opravilo predvidoma trajalo manj časa, kot je bilo prvotno načrtovano, in bo opravljeno pred predvidenim rokom.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Vnovično projiciranje obsega dela za opravila listnega vozlišča

Vodje projektov pogosto popravijo prvotne ocene v opravilu. Vnovične projekcije projekta so dojemanje ocen vodje projekta glede na trenutno stanje projekta. Vendar svetujemo, da vodje projektov ne spreminjajo načrtovanih številk obsega dela. To je zato, ker projektno načrtovani obseg dela predstavlja uveljavljeni vir zanesljivih podatkov za načrt projekta in oceno stroškov ter so se s tem strinjale vse zainteresirane skupine.

Vodja projekta lahko obseg dela vnovično projicira za opravila tako, da posodobi privzet **preostali obseg dela** z novo oceno opravila. Ta posodobitev povzroči ponoven izračun ocene končnih stroškov (EAC), odstotka napredka in predvidenega odmika od obsega dela v opravilu. Ponovno se izračunajo tudi EAC, ETC in odstotek napredka v opravilih povzetkov, kar ustvari novo projekcijo odmika od obsega dela.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Vnovična projekcija obsega dela v opravilih povzetka

Obseg dela v opravilih povzetka ali vsebnika je mogoče znova projicirati. Vodje projektov lahko posodobijo preostali obseg dela za povzetke opravil. Posodobitev preostalega obsega dela v aplikaciji sproži naslednji niz izračunov:

- Izračunata se ocena končnih stroškov in odstotek napredka v opravilu.
- Novi EAC se porazdeli na podrejena opravila v enakem razmerju kot pri prvotnem EAC v opravilu.
- Izračuna se nova ocena končnih stroškov za vsako posamezno opravilo do opravil v listnem vozlišču. 
- Prizadeta podrejena opravila do listnih vozlišč imajo svoj preostali obseg dela in odstotek napredka, ki je znova izračunan na podlagi vrednosti ocene končnih stroškov. Zato pride do nove projekcije odmika od obsega dela za opravilo. 
- Znova se izračunajo vrednosti EAC opravil povzetka vse do korenskega vozlišča.
- Odobreni napor za povzetek naloge je vsota odobrenega napora za vse otroške naloge in odobrenega napora za povzetek naloge.
- Preostali napor pri povzetku naloge je vsota preostalega napora pri vseh podrejenih opravilih minus odobreni napor pri povzetku nalogi.

## <a name="project-status-summary"></a>Povzetek stanja projekta

Sledenje podatkom v pogledih **Sledenje obsegu dela** in **Sledenje stroškom** prikaže napredek in porabo stroškov na ravneh korenskega vozlišča, opravil povzetka in opravil v listnem vozlišču. Razdelek **Stanje** na stran **Entiteta projekta** prikazuje povzetek stanja na ravni projekta.

## <a name="status-summary-fields"></a>Polja s povzetkom stanja

Polje **Splošno stanje projekta** je polje, ki ga je mogoče urejati in ki prikazuje splošno stanje projekta. Uporablja barvno kodiranje, na primer zeleno, rumeno in rdečo barvo, za označevanje naraščajočega tveganja. Polje **Komentarji** omogoča vodji projekta, da vnese določene komentarje o stanju. Polja **Stanje posodobljeno dne** ni mogoče urejati, vrednost pa je časovni žig, ki označuje, kdaj je bilo stanje nazadnje posodobljeno.

Polji **Učinkovitost razporeda** in **Stroškovna učinkovitost** sta nastavljeni iz datuma sledenja. Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče v pogledu **Sledenje obsegu dela** pozitivni, lahko polji nastavite na **Pred**. Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče negativni, ju lahko nastavite na **Za**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
