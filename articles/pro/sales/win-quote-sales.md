---
title: Zapiranje ponudbe – poenostavljeno
description: Ta tema vsebuje informacije o zapiranju ponudbe v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272307"
---
# <a name="close-a-quote---lite"></a>Zapiranje ponudbe – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ponudbo projekta lahko zaprete kot »Pridobljena« ali »Izgubljena«. Osnutek ponudbe lahko zaprete, ker postopka za aktiviranje in pregled ponudb nista podprta v aplikaciji Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Zapiranje ponudbe kot »Pridobljena«

Ko projektno ponudbo zaprete kot »Pridobljena«, je stanje nastavljeno na »Zaprto«, razlog stanja pa je »Pridobljena«. Ko ponudbo zaprete, je ponudba projekta na voljo samo za branje, ustvari pa se osnutek pogodbe o projektu, ki vsebuje informacije o ponudbah. Ker zaprte ponudbe ni mogoče znova odpreti, bodo vaše spremembe potrjene s potrditvenim pogovornim oknom.

Če je ponudba priložena priložnosti, se vse druge ponudbe projekta za priložnost samodejno zaprejo kot izgubljene.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finančni vpliv zapiranja ponudbe kot pridobljene

Če obstajajo dejanske vrednosti za čas za projekt, ko je ta še vedno povezan z osnutkom ponudbe, se beleži le strošek časa ali izdatek. Ko je ponudba zaprta kot »Pridobljena«, bo aplikacija refaktorirala stroške tako, da bo razveljavila starejše dejanske stroške in ponovno ustvarila nove dejanske stroške. Aplikacija bo te dejanske stroške obdelala na podlagi metode obračunavanja v povezani vrstici pogodbe o projektu. Če se dejanske vrednosti stroškov sklicujejo na podrobnosti pogodbe za čas in material, so po zapiranju ponudbe in ustvarjanju projektne pogodbe ustvarjene ustrezne neobračunane dejanske vrednosti prodaje. Če se dejanske vrednosti stroškov sklicujejo na podrobnosti pogodbe za fiksno ceno, bo aplikacija prenehala ponovno obdelovati dejanske vrednosti stroškov, ki temeljijo na pravilih za deljeno obračunavanje za stranke projektne pogodbe.

## <a name="closing-a-quote-as-lost"></a>Zapiranje ponudbe kot izgubljene:

Ko projektno ponudbo zaprete kot »Izgubljena«, je stanje nastavljeno na »Zaprto«, razlog stanja pa je »Izgubljena«. Ko ponudbo zaprete, je ponudba projekta na voljo samo za branje. Ker zaprte ponudbe ni mogoče znova odpreti, bo potrditveno okno potrdilo vaše spremembe, preden ponudbo zaprete.

Če se projektna ponudba, ki je zaprta kot »Izgubljena«, v kateri koli podrobnosti sklicuje na projekt, bo tudi ta projekt označen kot »Zaprt«. Vse rezervacije virov od tega dne naprej so preklicane.

> [!NOTE]
> V aplikaciji Project Operations zapiranje ponudbe kot pridobljene ali izgubljene ne bo vplivalo na to stanje priložnosti, ki bo ostalo odprto, dokler se ne zapre ročno.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]