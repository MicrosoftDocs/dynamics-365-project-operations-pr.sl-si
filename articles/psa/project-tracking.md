---
title: Napredek projekta in poraba stroškov
description: Ta tema vsebuje informacije o spremljanju napredka projekta in porabi stroškov.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 8bde19fbf1dd9f0c760455ecb7f7f2bd14a358d441bf024ec0cdefa42866f53e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987186"
---
# <a name="project-progress-and-cost-consumption"></a>Napredek projekta in poraba stroškov

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Potreba po spremljanju napredka v primerjavi z razporedom se razlikuje glede na panogo. V nekaterih panogah spremljanje poteka na zrnati ravni, v drugih panogah pa na višji ravni. V tej temi je prikazan način razporejanja, s katerim boste izpolnili zahteve vaše organizacije.

## <a name="effort-tracking-view"></a>Pogled sledenja obsegu dela

Pogled **Sledenje obsegu dela** spremlja napredek opravila v razporedu. Primerja dejanske ure obsega dela, ki so bile porabljene za opravilo, z načrtovanimi urami obsega dela za opravilo. Project Service Automation za izračun metrike sledenja uporablja te formule:

Najprej pri ustvarjanju opravila: načrtovani stroški bodo nastavljeni na oceno končnih stroškov. Ko so za opravilo zabeležene dejanske vrednosti, se v pogledu Sledenje za obseg dela izračuna naslednje:

- Odstotek napredka = dejanski obseg dela do danes ÷ ocena končnih stroškov (EAC) 
- Predvideni obseg dela do zaključka (ETC) = ocena končnih stroškov (EAC) – dejanski obseg dela do danes 
- Ocena končnih stroškov (EAC) = preostali obseg dela + dejanski obseg dela do danes 
- Predvideni odmik od obsega dela = načrtovan obseg dela – ocena končnih stroškov

Project Service Automation prikaže projekcijo odmika od obsega dela v opravilu. Če je EAC večji od načrtovanega obsega dela, bo opravilo predvidoma trajalo dlje časa, kot je bilo prvotno načrtovano. Torej je v zaostanku. Če je EAC manjši od načrtovanega obsega dela, bo opravilo predvidoma trajalo manj časa, kot je bilo prvotno načrtovano. Torej prehiteva urnik.

## <a name="reprojecting-effort"></a>Vnovična projekcija obsega dela

Vodja projekta pogosto popravi prvotne ocene v opravilu. Vnovične projekcije projekta so dojemanje ocen vodje projekta glede na trenutno stanje projekta. Vendar pa ne priporočamo, da vodje projektov spreminjajo osnovne številke, saj osnova projekta predstavlja zanesljiv vir ocene razporeda in stroškov za projekt, s katerim so se strinjale vse zainteresirane skupine, ki sodelujejo v projektu.

Projektni vodja lahko znova projicira obseg dela v opravilih na dva načina:

- Preglasi lahko privzeti ETC z novo oceno dejanskega preostalega obsega dela v opravilu. 
- Preglasi lahko privzeti odstotek napredka z novo oceno dejanskega napredka v opravilu.

Oba pristopa povzročita ponoven izračun ETC, EAC in odstotka napredka ter predvidenega odmika od obsega dela v opravilu. Ponovno se izračunajo tudi EAC, ETC in odstotek napredka v opravilih povzetkov, kar ustvari novo projekcijo odmika od obsega dela.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Vnovična projekcija obsega dela v opravilih povzetka

Obseg dela v opravilih povzetka ali vsebnika je mogoče znova projicirati. Ne glede na to, ali uporabnik za ponovno projiciranje v opravilih povzetka uporabi preostali obseg dela ali odstotek napredka, se začne naslednji niz izračunov:

- Izračunajo se EAC, ETC in odstotek napredka v opravilu.
- Novi EAC se porazdeli na podrejena opravila v enakem razmerju kot pri prvotnem EAC v opravilu.
- Izračuna se nova ocena končnih stroškov za vsako posamezno opravilo do opravil v listnem vozlišču. 
- Prizadeta podrejena opravila do listnih vozlišč imajo svoj ETC in odstotek napredka, ki je znova izračunan na podlagi vrednosti EAC. Zato pride do nove projekcije odmika od obsega dela za opravilo. 
- Znova se izračunajo vrednosti EAC opravil povzetka vse do korenskega vozlišča.

### <a name="cost-tracking-view"></a>Pogled za sledenje stroškom 

Pogled **Sledenje stroškom** primerja dejanske stroške, ki so bili porabljeni v opravilu, z načrtovanimi stroški. 

> [!NOTE]
> Ta pogled prikazuje samo stroške dela in ne vključuje ocen stroškov. 

Project Service Automation za izračun metrike sledenja uporablja te formule:

Ko je opravilo ustvarjeno, so načrtovani stroški enaki oceni končnih stroškov. Ko so za opravilo zabeležene dejanske vrednosti, se v pogledu **Sledenje** za stroške izračuna naslednje:

 - Odstotek porabljenih stroškov = dejanski stroški, porabljeni do danes ÷ ocena končnih stroškov za opravilo
 - Stroški do zaključka (CTC) = ocena končnih stroškov – dejanski stroški, porabljeni do danes
 - Ocena končnih stroškov = stroški do zaključka (CTC) – dejanski stroški, porabljeni do danes
 - Predvideni odmik od stroškov = načrtovani stroški – ocena končnih stroškov

Projekcija odmika od stroškov je prikazana v opravilu. Če je ocena končnih stroškov večja od načrtovanih stroškov, bo opravilo predvidoma stalo več, kot je bilo prvotno načrtovano. Torej presega proračun. Če je ocena končnih stroškov manjša od načrtovanih stroškov, bo opravilo predvidoma stalo manj, kot je bilo prvotno načrtovano.

## <a name="project-managers-reprojection-of-cost"></a>Ponovna projekcija stroškov vodje projekta

Pri ponovni projekciji obsega dela so v pogledu **Sledenje stroškom** znova izračunani stroški do zaključka (CTC), ocena končnih stroškov, odstotek porabljenih stroškov in predvideni odmik od stroškov.

## <a name="project-status-summary"></a>Povzetek stanja projekta

Sledenje podatkom v pogledih **Sledenje obsegu dela** in **Sledenje stroškom** prikaže napredek in porabo stroškov na ravneh korenskega vozlišča, opravil povzetka in opravil v listnem vozlišču. Razdelek **Stanje** na stran **Entiteta projekta** prikazuje povzetek stanja na ravni projekta.

## <a name="status-summary-fields"></a>Polja s povzetkom stanja

Polje **Splošno stanje projekta** je polje, ki ga je mogoče urejati in ki prikazuje splošno stanje projekta. Uporablja barvno kodiranje, na primer zeleno, rumeno in rdečo barvo, za označevanje naraščajočega tveganja. Polje **Komentarji** omogoča vodji projekta, da vnese določene komentarje o stanju. Polja **Stanje posodobljeno dne** ni mogoče urejati, vrednost pa je časovni žig, ki označuje, kdaj je bilo stanje nazadnje posodobljeno.

Polji **Učinkovitost razporeda** in **Stroškovna učinkovitost** sta nastavljeni iz datuma sledenja. Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče v pogledu **Sledenje obsegu dela** pozitivni, lahko polji nastavite na **Pred**. Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče negativni, ju lahko nastavite na **Za**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]