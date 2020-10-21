---
title: Uvoz ocene projekta v vrstico ponudbe, ki temelji na projektu
description: Ta tema vsebuje informacije o tem, kako uvoziti ocene projekta v vrstico ponudbe.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908601"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Uvoz ocene projekta v vrstico ponudbe, ki temelji na projektu

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


Če je projekt ustvarjen v predprodajni fazi, lahko izberete uvoz finančne ocene iz projekta v vrstico ponudbe, ki temelji na projektu.

1. Prepričajte se, da so v vrstici ponudbe, ki temelji na projektu, podatki vneseni v polje **Projekt**.
2. Na zavihku **Podrobnosti vrstice ponudbe** izberite možnost **Uvozi iz ocene projekta**.
3. V pogovornem oknu izberite eno od naslednjih možnosti povzemanja.

  - **Razred transakcije**
  - **Kategorija**
  - **Vloga** 
  - **Projektno opravilo**

Na podlagi vaše izbire je prekopirana ocena iz projekta za vse razrede transakcij, ki so vključeni v tej vrstici ponudbe. Če želite preveriti, kateri razredi transakcij so vključeni, izberite zavihek **Splošno** v vrstici ponudbe, ki temelji na projektu, in preverite vrednosti za polja **Vključi čas**, **Vključi stroške** in **Vključi dajatve**.

Pri uvozu ocen sistem privzeto določi cene na podlagi cenikov projekta, priloženih ponudbi, in vrste obračuna, nastavljene v vrstici ponudbe, ki temelji na projektu. Če je vloga ali kategorija v vrstici ponudbe, ki temelji na projektu, nastavljena kot nezaračunljiva, bo uvožena ocenjevalna vrstica nastavljena kot nezaračunljiva in ne bo prispevala k ponudbeni vrednosti ponudbene vrstice.

Če ima vrstica ponudbe podrobnosti o vrstici, sta polji **Vrednost ponudbe** in **Ocenjeni davek** v vrstici ponudbe povzeti in ju ni mogoče urejati.

Če je izbranih več možnosti povzetka, se poskuša povzetek ustvariti po vseh izbranih možnostih. To pomeni, da bo izhodnih podatkov iz uvoženih ponudb več, kot če bi izbrali samo eno možnost povzetka.

Če ima projekt na primer naslednje vrstice ocen za stroške.

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| Opravilo A | Letalska vozovnica | 10. 1. 2020 | 4 | 400 | 1600 |
| Opravilo B | Hotel | 1. 10. 2020 | 4 | 200 | 800 |
| Opravilo C | Hotel | 1. 11. 2020 | 2 | 200 | 400 |

Če uporabnik izbere povzetek po razredu transakcij, bodo uvoženi naslednji podatki.

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| | | 1. 10. 2020 | 3.34 | 840 | 2800 |

Če uporabnik izbere povzetek po razredu transakcij in kategorij, bodo uvoženi naslednji podatki.

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| Opravilo A | Letalska vozovnica | 1. 10. 2020 | 4 | 400 | 1600 |
| | Hotel | 1. 10. 2020 | 6 | 200 | 1200 |

Če uporabnik izbere povzetek po razredu transakcij, kategorij in opravilu listnega vozlišča, bodo uvoženi naslednji podatki. Upoštevajte, da je ta rezultat enak tistemu na projektu.

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| Opravilo A | Letalska vozovnica | 10. 1. 2020 | 4 | 400 | 1600 |
| Opravilo B | Hotel | 1. 10. 2020 | 4 | 200 | 800 |
| Opravilo C | Hotel | 1. 11. 2020 | 2 | 200 | 400 |