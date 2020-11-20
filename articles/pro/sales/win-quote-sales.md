---
title: Zapiranje ponudbe – poenostavljeno
description: Ta tema vsebuje informacije o zapiranju ponudbe v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175731"
---
# <a name="close-a-quote---lite"></a>Zapiranje ponudbe – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ponudbo projekta lahko zaprete kot »Pridobljena« ali »Izgubljena«. Ker postopka za aktiviranje in pregledovanje nista na voljo v storitvi Microsoft Dynamics 365 Project Operations, lahko zaprete osnutek ponudbe.

## <a name="close-a-quote-as-won"></a>Zapiranje ponudbe kot »Pridobljena«

Če zaprete ponudbo za projekt kot »Pridobljena«, bo stanje ponudbe nastavljeno na »Zaprto« in razlog stanja na »Pridobljena«. Ko ponudbo zaprete, je ponudba projekta na voljo samo za branje, ustvari pa se osnutek pogodbe o projektu, ki vsebuje informacije o ponudbah. Ker zaprte ponudbe ni mogoče znova odpreti, se pred potrditvijo sprememb pojavi potrditveno pogovorno okno, saj zaprte ponudbe ni mogoče znova odpreti in sprememb ni mogoče razveljaviti.

Če je ponudba priložena priložnosti, se vse druge ponudbe projekta za priložnost samodejno zaprejo kot izgubljene.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finančni vpliv zapiranja ponudbe kot pridobljene

Če so bile zabeležene dejanske vrednosti za čas, ko je še bil projekt še vedno priložen osnutku ponudbe, se zabeleži le znesek časa ali stroška. Ko je ponudba zaprta kot »Pridobljena«, bo aplikacija refaktorirala stroške tako, da bo razveljavila starejše dejanske stroške in ponovno ustvarila nove dejanske stroške. Aplikacija bo te dejanske stroške obdelala na podlagi metode obračunavanja v povezani vrstici pogodbe o projektu. Če se dejanski stroški sklicujejo na časovno in materialno vrstico pogodbe, bo sistem samodejno ustvaril ustrezne dejanske nezaračunane zneske prodaje, ko se ponudba zapre in se ustvari pogodba o projektu. Če se dejanski stroški sklicujejo na podrobnost pogodbe s fiksno ceno, bo aplikacija zaustavila ponovno obdelavo dejanskih stroškov na podlagi pravil za izstavitev računa za delitev za stranke v pogodbi o projektu.

## <a name="closing-a-quote-as-lost"></a>Zapiranje ponudbe kot izgubljene:

Če zaprete ponudbo za projekt kot »Izgubljena«, bo stanje nastavljeno na »Zaprto« in razlog stanja na »Izgubljena«. Ko ponudbo zaprete, je ponudba projekta na voljo samo za branje. Ker zaprte ponudbe ni mogoče znova odpreti, bo potrditveno okno potrdilo vaše spremembe, preden ponudbo zaprete.

Če se ponudba projekta, ki je zaprta kot »Izgubljena«, v kateri koli vrstici sklicuje na projekt, je tudi ta projekt označen kot zaprt in vse rezervacije virov od tistega dne dalje so preklicane.

> [!NOTE]
> V aplikaciji Project Operations zapiranje ponudbe kot pridobljene ali izgubljene ne bo vplivalo na to stanje priložnosti, ki bo ostalo odprto, dokler se ne zapre ročno.
