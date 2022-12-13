---
title: Zapiranje projektnih ponudb
description: Ta članek vsebuje informacije o zapiranju ponudbe v aplikaciji Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4335fa5467640af840c0f68a648c9b8a6864d834
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826196"
---
# <a name="close-project-quotes"></a>Zapiranje projektnih ponudb

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ponudbo projekta lahko zaprete kot »Pridobljena« ali »Izgubljena«. Osnutek ponudbe lahko zaprete, ker postopka za aktiviranje in pregled ponudb nista podprta v aplikaciji Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Zapiranje ponudbe kot »Pridobljena«

Ko projektno ponudbo zaprete kot »Pridobljena«, je stanje nastavljeno na »Zaprto«, razlog stanja pa je »Pridobljena«. Ko ponudbo zaprete, je ponudba projekta na voljo samo za branje, ustvari pa se osnutek pogodbe o projektu, ki vsebuje informacije o ponudbah. Ker zaprte ponudbe ni mogoče znova odpreti, bodo vaše spremembe potrjene s potrditvenim pogovornim oknom.

Če je ponudba priložena priložnosti, se vse druge ponudbe projekta za priložnost samodejno zaprejo kot izgubljene.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finančni vpliv zapiranja ponudbe kot pridobljene

Če obstajajo dejanske vrednosti za čas za projekt, ko je ta še vedno povezan z osnutkom ponudbe, se beleži le strošek časa ali izdatek. Ko je ponudba zaprta kot »Pridobljena«, bo aplikacija refaktorirala stroške tako, da bo razveljavila starejše dejanske stroške in ponovno ustvarila nove dejanske stroške. Aplikacija bo te dejanske stroške obdelala na podlagi metode obračunavanja v povezani vrstici pogodbe o projektu. Če se dejanske vrednosti stroškov sklicujejo na podrobnosti pogodbe za čas in material, so po zapiranju ponudbe in ustvarjanju projektne pogodbe ustvarjene ustrezne neobračunane dejanske vrednosti prodaje. Če se dejanske vrednosti stroškov sklicujejo na podrobnosti pogodbe za fiksno ceno, bo aplikacija prenehala ponovno obdelovati dejanske vrednosti stroškov, ki temeljijo na pravilih za deljeno obračunavanje za stranke projektne pogodbe.

## <a name="closing-a-quote-as-lost"></a>Zapiranje citata kot izgubljenega

Ko projektno ponudbo zaprete kot »Izgubljena«, je stanje nastavljeno na »Zaprto«, razlog stanja pa je »Izgubljena«. Ko ponudbo zaprete, je ponudba projekta na voljo samo za branje. Ker zaprte ponudbe ni mogoče znova odpreti, bo potrditveno okno potrdilo vaše spremembe, preden ponudbo zaprete.

Če se projektna ponudba, ki je zaprta kot »Izgubljena«, v kateri koli podrobnosti sklicuje na projekt, bo tudi ta projekt označen kot »Zaprt«. Vse rezervacije virov od tega dne naprej so preklicane.

> [!NOTE]
> V aplikaciji Project Operations zapiranje ponudbe kot pridobljene ali izgubljene ne bo vplivalo na to stanje priložnosti, ki bo ostalo odprto, dokler se ne zapre ročno.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
