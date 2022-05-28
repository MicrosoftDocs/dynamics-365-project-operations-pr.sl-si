---
title: Sledenje stroškom projekta
description: Ta tema vsebuje informacije o tem, kako aplikacija Project Operations spremlja napredek glede na stroške in porabo pri projektu.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f724ee29728a363c58ed0e69087f4c18be89ea2d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591470"
---
# <a name="labor-cost-tracking-on-projects"></a>Sledenje stroškom dela pri projektih

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dynamics 365 Project Operations sledi ocenam dela in porabi pri najnižji zahtevani granularnosti v načrtu projekta. Finančna ocena stroškov dela temelji na načrtovanem obsegu dela in splošnih ali poimenovanih virih, ki so v načrtu projekta dodeljeni vsakemu opravilu listnega vozlišča. Ko se projekt začne in ljudje začnejo poročati o času za različna projektna opravila, se dejanska poraba pri delu sešteje, kar sproži izračun projekcij.

## <a name="labor-cost-tracking-view"></a>Pogled za sledenje stroškom dela

Na strani **Projekti** v zavihku **Sledenje** lahko izberete možnost **Sledenje** > **Stroški**, da odprete pogled **Sledenje stroškov** in si ogledate napredek porabe pri delu za vsako opravilo v načrtu projekta. Ta pogled tudi primerja dejanske stroške dela za opravilo z načrtovanimi stroški dela. Project Operations uporablja naslednje formule za izračun meritev stroškov dela:

- **Načrtovani stroški**: ocenjeni stroški vseh dodelitev virov za vsako nalogo listnega vozlišča
- **Dejanski stroški**: vsota vseh dejanskih vrednosti za čas, zabeležen pri opravilu
- **Odstotek porabe stroškov**: dejanski stroški ÷ ocena končnih stroškov
- **Preostanek stroškov**: ocena končnih stroškov ÷ dejanski stroški
- **Končni stroški**: preostanek stroškov ÷ dejanski stroški
- **Odmik stroška**: načrtovani stroški ÷ ocena končnih stroškov

Vsako o pravilo prikazuje projekcijo odmika stroškov v opravilu. Če je ocena končnih stroškov večja od načrtovanih stroškov, bo opravilo predvidoma preseglo proračun. Če je ocena končnih stroškov manjša od načrtovanih stroškov, opravilo predvidoma ne bo preseglo proračuna.

>[!NOTE]
> Project Operations prikazuje samo stroške dela na strani **Projekt** v zavihku **Sledenje**. Čeprav je materiale in stroške mogoče oceniti in slediti njihovi porabi, ti stroški niso vključeni v stroške, prikazane v zavihku **Sledenje**. Ta zavihek je zasnovan tako, da deluje samo za vnovično projiciranje stroškov dela z vnovičnim projiciranjem obsega dela.
Vsi prikazani zneski stroškov se v valuto stroškov projekta pretvorijo iz valute lastne cene projekta, s katero je določena mera stroškov. Valuta stroškov projekta je valuta pogodbene enote za projekt. Ocenjene vrednosti stroškov za čas, ki so prikazane v zavihku **Ocene** na strani **Projekt**, morda ne bodo enake načrtovanim stroškom v zavihku **Sledenje**. Razlog za to neskladje so razlikah v načinu povzemanja ocenjenih stroškov na mreži **Ocene** in izračunavanja načrtovanih stroškov na mreži **Sledenje**. 
>
> - Zavihek **Ocene** izračuna predvidene stroške tako, da uporabi isto valuto mere stroškov v ceniku. Nato se ocenjeni stroški v valuti cenika pretvorijo v predvidene stroške v valuti stroškov projekta. Ocenjeni stroški v valuti projekta so zaokroženi na 2 decimalni mesti. Med to pretvorbo se na nobeni točki ne uporabi natančnost valute. 
> - V zavihku **Sledenje** izračun načrtovanih stroškov sledi nekoliko drugačnemu vrstnemu redu izračuna, ki v dveh stopnjah vključuje uporabo natančnosti valute: 
   ><ol>
   ><li>Znesek predvidenih stroškov v valuti cenika se pretvori v osnovno valuto (pretvorba 1).</li>
   ><li>Znesek predvidenih stroškov v osnovni valuti se pretvori v valuto stroškov projekta (pretvorba 2). </li>
   ></ol>
   >V obeh korakih se uporabi natančnost valute za načrtovane stroške (v zavihku **Sledenje**), ki nekoliko odstopajo od predvidenih stroškov (v pogledu **Časovno razporejeno** v zavihku **Ocene**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Vnovično projiciranje stroškov za opravila listnega vozlišča

Stroškov dela za opravila listnega vozlišča ni mogoče vnovično projicirati neposredno v zavihku **Sledenje** na strani **Projekt**. Lahko pa uporabite pogled **Sledenje obsegu dela**, da znova projicirate preostanek obsega dela za opravilo. To povzroči vnovični izračun preostanka stroškov za opravilo. Sledi opis postopka.

1. Vodja projekta lahko obseg dela za opravila povzetka vnovično projicira tako, da posodobi privzeto vrednost v polju **Preostanek obsega dela** z novo oceno preostanka obsega dela za opravilo. Vnovično projiciranje povzroči vnovičen izračun ocene končnih stroškov (EAC), odstotka napredka in predvidenega odmika od obsega dela v opravilu. Ponovno se izračunajo tudi EAC, predviden obseg dela do zaključka (ETC) in odstotek napredka v opravilih povzetkov, kar ustvari novo projekcijo odmika od obsega dela.
2. Na podlagi nove vrednosti za preostanek obsega dela za opravilo sistem izračuna preostanek stroškov v pogledu **Sledenje stroškov**. Za izračun preostanka stroškov na podlagi preostanka obsega dela sistem najprej kot načrtovane stroške ali načrtovani obseg dela izračuna povprečne stroške ene ure dela za opravilo. Načrtovani stroški so vsota stroškov vseh dodelitev virov za opravilo. Povprečni stroški na uro se uporabljajo za izračun preostanka stroškov za novo projiciran preostanek obsega dela za nalogo.
3. Znova se izračunajo končni stroški in odstotek porabe stroškov za opravilo listnega vozlišča.
4. Znova se izračunajo vrednosti končnih stroškov opravil povzetka vse do korenskega vozlišča.

## <a name="reprojecting-costs-on-summary-tasks"></a>Vnovično projiciranje stroškov za opravila povzetkov

Stroške dela lahko znova načrtujete za opravila povzetkov ali opravila vsebnika. Vendar stroškov dela za opravila povzetkov projekta ne morete znova projicirati neposredno v zavihku **Sledenje** na strani **Projekt**. Podobno kot pri opravilih listnega vozlišča lahko znova projicirate tudi opravila povzetka in vsebnika s pomočjo pogleda **Sledenje obsegu dela**. V tem pogledu lahko znova projicirate preostanek obsega dela za opravilo povzetka, kar povzroči vnovični izračun preostanka stroškov za opravilo povzetka. Sledi opis postopka.

1. Vodja projekta lahko obseg dela za opravila povzetka vnovično projicira tako, da posodobi privzeto vrednost preostanka obsega dela z novo oceno opravila. Ta posodobitev povzroči ponoven izračun ocene končnih stroškov (EAC) povzetka, odstotka napredka in predvidenega odmika od obsega dela v opravilu. Ponovno se izračunajo tudi EAC, ETC in odstotek napredka v opravilih povzetkov, kar ustvari novo projekcijo odmika od obsega dela.
2. Na podlagi nove vrednosti za preostanek obsega dela za opravilo povzetka sistem izračuna preostanek stroškov v pogledu **Sledenje stroškov**. Za izračun preostanka stroškov na podlagi preostanka obsega dela sistem najprej kot načrtovane stroške ali načrtovani obseg dela izračuna povprečne stroške ene ure dela za opravilo povzetka. Povprečni stroški na uro se uporabljajo za izračun stroškov novo projiciranega preostanka obsega dela za opravilo povzetka.
3. Znova se izračunajo končni stroški in odstotek porabe stroškov za opravilo povzetka.
4. Novi končni stroški se porazdelijo na podrejena opravila v enakem razmerju kot pri prvotnih predvidenih stroških v opravilu.
5. Izračuna se nova vrednost končnih stroškov za vsako posamezno opravilo do opravil v listnem vozlišču. Na podlagi te vrednosti bo na podlagi vrednosti končnih stroškov znova izračunan odstotek preostanka in porabe stroškov za prizadeta podrejena opravila do listnih vozlišč. Rezultat te vrednosti je nova projekcija odmika stroškov za opravilo. 


Polje **Stroškovna učinkovitost** lahko nastavite iz podatkov o sledenju. Ko je odmik stroškov za korensko vozlišče v pogledu **Sledenje stroškov** negativen, lahko to polje nastavite na **pod proračunom**. Ko je odmik stroškov za korensko vozlišče pozitivno, lahko vrednost nastavite na **čez proračun**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
