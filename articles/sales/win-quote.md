---
title: Zapiranje ponudbe
description: Ta tema vsebuje informacije o zapiranju ponudb v aplikaciji Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f46bf61bc3e492a648d65e86750a25609d5ab7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995956"
---
# <a name="close-a-quote"></a>Zapiranje ponudbe

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ponudbo projekta lahko zaprete kot »Pridobljena« ali »Izgubljena«. Ker funkciji za aktiviranje in pregled ponudb v aplikaciji Microsoft Dynamics 365 Project Operations nista podprti, lahko zaprete osnutek pogodbe.

## <a name="close-a-quote-as-won"></a>Zapiranje ponudbe kot »Pridobljena«

Če zaprete ponudbo za projekt kot »Pridobljena«, bo stanje ponudbe nastavljeno na **Zaprto** in razlog stanja na **Pridobljena**. Ko ponudbo zaprete, je na voljo samo za branje, ustvari pa se osnutek pogodbe o projektu z vsemi informacijami o ponudbah. Ker zaprte ponudbe ni mogoče znova odpreti, bo potrditveno okno potrdilo vaše spremembe, preden ponudbo zaprete.

Pogodba o projektu, izdelana na podlagi ponudbe za projekt, je na voljo tudi v modulu za vodenje projektov in računovodstvo aplikacije Project Operations. Če pogodba o projektu ni preslikana v projekt v nobeni od njegovih vrstic, je ta pogodba o projektu na voljo kot nedejavna pogodba o projektu in začne veljati takoj, ko se projekt preslika v vsaj eno od njegovih podrobnosti pogodbe.

Če je ponudba priložena priložnosti, se vse druge ponudbe projekta za priložnost samodejno zaprejo kot izgubljene.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finančni vpliv zapiranja ponudbe kot pridobljene

Če so bile zabeležene dejanske vrednosti za čas, ko je še bil projekt še vedno priložen osnutku ponudbe, se zabeleži le znesek časa ali stroška. Ko je ponudba zaprta kot »Pridobljena«, bo aplikacija refaktorirala stroške tako, da bo razveljavila starejše dejanske stroške in ponovno ustvarila nove dejanske stroške. Aplikacija bo te dejanske stroške obdelala na podlagi metode obračunavanja v povezani vrstici pogodbe o projektu. Če se dejanski stroški sklicujejo na časovno in materialno vrstico pogodbe, bo sistem samodejno ustvaril ustrezne dejanske nezaračunane zneske prodaje, ko se ponudba zapre in se ustvari pogodba o projektu. Če se dejanski stroški sklicujejo na podrobnost pogodbe s fiksno ceno, bo aplikacija zaustavila ponovno obdelavo dejanskih stroškov na podlagi pravil za izstavitev računa za delitev za stranke v pogodbi o projektu.

Vsi predelani dejanski podatki so na voljo v modulu za vodenje projektov in računovodstvo, ki ga lahko računovodja projekta pregleda, posodobi in objavi v glavni knjigi. 

## <a name="close-a-quote-as-lost"></a>Zapiranje ponudbe kot »Izgubljena«

Če zaprete ponudbo za projekt kot »Izgubljena«, bo stanje nastavljeno na **Zaprto** in razlog stanja na **Izgubljena**. Ko ponudbo zaprete, je na voljo samo za branje. Ker zaprte ponudbe ni mogoče znova odpreti, bo potrditveno okno potrdilo vaše spremembe, preden ponudbo zaprete.

Če se ponudba projekta, ki je zaprta kot »Izgubljena«, v kateri koli vrstici sklicuje na projekt, je tudi ta projekt označen kot zaprt in vse rezervacije virov od tistega dne dalje so preklicane.

> [!NOTE]
> V aplikaciji Project Operations zapiranje ponudbe kot pridobljene ali izgubljene ne bo vplivalo na to stanje priložnosti, ki bo ostalo odprto, dokler se ne zapre ročno.


[!INCLUDE[footer-include](../includes/footer-banner.md)]