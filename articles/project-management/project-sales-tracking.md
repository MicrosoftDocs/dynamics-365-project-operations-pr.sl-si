---
title: Sledenje prodaji v projektu
description: Ta tema vsebuje informacije o tem, kako operacije Project Operations spremljajo napredek glede na prihodek od dela na projektu.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 78d7bdaf9f5ca1757273cb81a1303befb0357ba547eb354097786fc3c38962b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995601"
---
# <a name="project-sales-tracking"></a>Sledenje prodaji v projektu

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dynamics 365 Project Operations sledi ocenam dela in prihodkom pri najnižji zahtevani granularnosti v načrtu projekta. Ocena prihodkov od dela temelji na načrtovanem obsegu dela in splošnih ali poimenovanih virih, ki so v načrtu projekta dodeljeni vsakemu opravilu listnega vozlišča. Ko se projekt začne in ljudje začnejo poročati o času za različna projektna opravila, se dejanski prihodek od dela sešteje, kar sproži izračun projekcij.

## <a name="labor-revenue-tracking-view"></a>Pogled sledenja prihodkov od dela

Na strani **Projekti** v zavihku **Sledenje** lahko izberete **Sledenje** > **Stroški**, da odprete pogled **Sledenje stroškov**. Lahko pa izberete možnost **Uporaba** > **Delež obračunavanja**, da odprete pogled **Sledenje prihodkom**, ki prikazuje napredek prihodka od dela za vsako opravilo v načrtu projekta. Ta pogled tudi primerja dejanske porabljene prihodke od dela za opravilo z načrtovanimi prihodki od dela. Project Operations uporablja naslednje formule za izračun meritev prihodkov od dela:

- **Načrtovani prihodki**: ocenjene vrednosti prodaje vseh dodelitev virov za vsako opravilo listnega vozlišča
- **Dejanski prihodki**: vsota vseh dejanskih vrednosti neobračunanih prodaj za čas, zabeležen pri opravilu
- **Obračunani prihodek v %**: dejanski prihodek ÷ ocena končnega prihodka
- **Preostanek prihodka**: ocena končnega prihodka – dejanski prihodek
- **Ocena končnega prihodka**: preostanek prihodka + dejanski prihodek
- **Odmik prihodka**: načrtovan prihodek – ocena končnega prihodka


> [!NOTE]
> Project Operations prikazuje samo prihodke od dela na strani **Projekt** v zavihku **Sledenje**. Čeprav je materiale in stroške mogoče oceniti in slediti njihovi porabi, ti prihodki niso vključeni v prihodke, prikazane v zavihku **Sledenje**. Ta zavihek je zasnovan tako, da deluje samo za vnovično projiciranje prihodkov od dela z vnovičnim projiciranjem obsega dela.  
> Vsi prikazani zneski prihodkov se pretvorijo v valuto stroškov projekta. Valuta stroškov projekta je valuta pogodbene enote za projekt. Za projekte s fiksno ceno številke prihodkov v pogledu **Sledenje prihodkom od dela** niso pomembne, ker dejanske vrednosti neobračunanih prodaj niso zabeležene za odobritev časa.
> Ocenjene prodajne vrednosti za čas, ki so prikazane v zavihku **Ocene** za projekt, morda ne bodo enake načrtovani vrednosti prihodka v zavihku **Sledenje**. Za to neskladje sta možna dva razloga:
><ol>
   ><li> Zavihek <b>Ocene</b> prikazuje predvideni prihodek v prodajni valuti, medtem ko zavihek <b>Sledenje</b> prikazuje načrtovani prihodek, pretvorjen v valuto stroškov. </li>
   ><li> Ko se predvidena prodaja pretvori v valuto pogodbe, kot je prikazano v zavihku <b>Ocene</b>, pretvorba v valuto projekta vključuje korake, ki bi lahko pomenili manjšo natančnost: </li>
><ol>
><li> Znesek predvidene prodaje v valuti pogodbe se najprej pretvori v osnovno valuto (pretvorba 1).</li>
><li> Znesek predvidene prodaje v osnovni valuti se pretvori v valuto stroškov projekta (pretvorba 2). </li>
></ol>
></ol>
> V obeh korakih se uporablja natančnost valute, posledično pa pride do odstopanja načrtovanega prihodka v valuti projekta od načrtovane prodaje v valuti pogodbe.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Vnovično projiciranje prihodkov za opravila listnega vozlišča

Prihodkov od dela za opravila listnega vozlišča ni mogoče vnovično projicirati neposredno v zavihku **Sledenje** na strani **Projekt**. Lahko pa uporabite pogled **Sledenje obsegu dela**, da znova projicirate preostanek obsega dela za opravilo. To povzroči vnovični izračun preostanka prihodkov za opravilo. Sledi opis postopka.

1. Vodja projekta lahko obseg dela za opravila povzetka vnovično projicira tako, da posodobi privzeto vrednost v polju **Preostanek obsega dela** z novo oceno preostanka obsega dela za opravilo. Vnovično projiciranje povzroči vnovičen izračun ocene končnih stroškov (EAC), odstotka napredka in predvidenega odmika od obsega dela v opravilu. Ponovno se izračunajo tudi EAC, predviden obseg dela do zaključka (ETC) in odstotek napredka v opravilih povzetkov, kar ustvari novo projekcijo odmika od obsega dela.
2. Na podlagi nove vrednosti za preostanek obsega dela za opravilo sistem izračuna preostanek prihodkov v pogledu **Sledenje prihodkov**. Za izračun preostanka prihodkov na podlagi preostanka obsega dela sistem najprej kot načrtovane prihodke ali načrtovani obseg dela izračuna povprečne prihodke ene ure dela za opravilo povzetka. Načrtovani prihodki so vsota prihodkov vseh dodelitev virov za opravilo. Povprečni prihodki na uro se uporabljajo za izračun preostanka prihodkov za novo projiciran preostanek obsega dela za nalogo.
3. Znova se izračunajo predvideni končni prihodki in odstotek porabe prihodkov za opravilo listnega vozlišča.
4. Znova se izračunajo vrednosti končnih prihodkov opravil povzetka vse do korenskega vozlišča.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Vnovično projiciranje prihodkov za opravila povzetkov

Prihodke od dela lahko znova načrtujete za opravila povzetkov ali opravila vsebnika. Vendar prihodkov od dela za opravila povzetkov projekta ne morete znova projicirati neposredno v zavihku **Sledenje** na strani **Projekt**. Podobno kot pri opravilih listnega vozlišča lahko znova projicirate tudi opravila povzetka in vsebnika s pomočjo pogleda **Sledenje obsegu dela**. V tem pogledu lahko znova projicirate preostanek obsega dela za opravilo povzetka, kar povzroči vnovični izračun preostanka prihodkov za opravilo povzetka. Sledi opis postopka.

1. Vodja projekta lahko obseg dela za opravila povzetka vnovično projicira tako, da posodobi privzeto vrednost v polju **Preostanek obsega dela** z novo oceno **preostanka obsega dela** za opravilo. Vnovično projiciranje povzroči vnovičen izračun ocene končnih stroškov (EAC), odstotka napredka in predvidenega odmika od obsega dela v opravilu. Ponovno se izračunajo tudi EAC, ETC in odstotek napredka v opravilih povzetkov, kar ustvari novo projekcijo odmika od obsega dela.
2. Na podlagi nove vrednosti v polju **Preostanek obsega dela** za opravilo sistem izračuna preostanek prihodkov v pogledu **Sledenje prihodkov**. Za izračun preostanka prihodkov na podlagi preostanka obsega dela sistem najprej kot načrtovane prihodke ali načrtovani obseg dela izračuna povprečne prihodke ene ure dela za opravilo povzetka. Načrtovani prihodki so vsota prihodkov vseh dodelitev virov za opravilo. Povprečni prihodki na uro se nato uporabijo za izračun prihodkov za novo projiciran preostanek obsega dela za nalogo.
3. Znova se izračunajo predvideni končni prihodki in odstotek porabe prihodkov za opravilo povzetka.
4. Nova vrednost za oceno končnih prihodkov se porazdeli na podrejena opravila v enakem razmerju kot pri prvotnih predvidenih prihodkih v opravilu.
5. Izračuna se nova ocena končnih prihodkov za vsako posamezno opravilo do opravil v listnem vozlišču. Na podlagi te vrednosti bo na podlagi vrednosti končnih prihodkov znova izračunan odstotek preostanka in porabe prihodkov za prizadeta podrejena opravila do listnih vozlišč. Zato pride do nove projekcije odmika prihodka za opravilo. 
6. Znova se izračunajo vrednosti končnih prihodkov opravil povzetka vse do korenskega vozlišča.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

