---
title: Privzeti cenik
description: Ta članek vsebuje informacije o privzetih cenikih s prodajno in lastno ceno v aplikaciji Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410283"
---
# <a name="default-price-lists"></a>Privzeti cenik

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

## <a name="sales-price-lists"></a>Prodajni ceniki

Vse ponudbe in pogodbe za projekt v aplikaciji Dynamics 365 Project Operations vsebujejo privzeti prodajni cenik. 

### <a name="price-list-default-on-project-quotes"></a>Privzeti cenik za projektne ponudbe
Sistem izvede spodnji postopek, da določi, kateri cenik bo privzeto uporabljen za projektno ponudbo:

1. Sistem preuči cenike, ki so priloženi projektnim cenikom računa. 
1. Če zapisu o računu ni priloženih projektnih cenikov, sistem pregleda prodajne cenike, priložene projektnim parametrom, ki ustrezajo valuti projektne ponudbe.
1. Nato sistem preveri veljavnost datumov cenikov, ki ustrezajo časovnemu obdobju projektne ponudbe. Še posebno datum, ko je bila ponudba ustvarjena.
1. Če je na datum projektne ponudbe v veljavi več cenikov, se vsi ceniki privzeto nastavijo za projektno ponudbo.
1. Če na datum projektne ponudbe ni v veljavi noben cenik, na projektni ponudbi ne bo privzetega projektnega cenika. Na projektni ponudbi se bo pojavilo opozorilno sporočilo. V sporočilu je zapisano, da dejanske vrednosti in ocene projekta ne bodo podane, ker niste priložili nobenega cenika.

### <a name="price-list-default-on-project-contracts"></a>Privzeti cenik za projektne pogodbe 
Sistem izvede spodnji postopek, da določi, kateri cenik bo privzeto uporabljen za projektno pogodbo:

1. Če je pogodba ustvarjena iz ponudbe, se projektni ceniki na ponudbi kopirajo ločeno in se priložijo projektni pogodbi.
1. Če je pogodba ustvarjena na novo, sistem pregleda cenike, ki so priloženi projektnim cenikom računa. Če zapisu o računu niso priloženi projektni ceniki, sistem poišče prodajne cenike, priložene projektnim parametrom, ki ustrezajo valuti projektne pogodbe.
1. Nato sistem preveri veljavnost datumov cenikov, ki ustrezajo časovnemu obdobju projektne pogodbe. Še posebno datum, ko je bila pogodba ustvarjena.
1. Če je na datum projektne pogodbe v veljavi več cenikov, se vsi ceniki privzeto nastavijo za projektno pogodbo.
1. Če na datum projektne pogodbe ni v veljavi noben cenik, na projektni pogodbi ne bo privzetega projektnega cenika. Na projektni pogodbi se bo pojavilo opozorilno sporočilo. V sporočilu je zapisano, da dejanske vrednosti in ocene projekta ne bodo podane, ker niste priložili nobenega cenika.

## <a name="cost-price-lists"></a>Cenik z lastnimi cenami

Ceniki z lastnimi cenami niso privzeto nastavljeni za nobeno entiteto v aplikaciji Project Operations. Določitev cenika z lastnimi cenami, ki se bo uporabil za stroške projekta, se vedno izvede za vsako transakcijo posebej. Sistem izvede spodnji postopek, da določi, kateri cenik bo uporabljen za stroške projekta:

1. Sistem preuči cenike, ki so priloženi pogodbeni organizacijski enoti projekta.
1. Nato sistem preveri veljavnost datumov cenikov, ki se ujemajo z datumom dohodnega konteksta ocenjevanja ali dejanskega konteksta.

    - *Kontekst ocenjevanja* se nanaša na kateregakoli od treh kontekstov ocenjevanja v aplikaciji Project Operations:

        - Vrstica ocene projekta
        - Podrobnosti vrstic ponudbe
        - Podrobnosti pogodb

    - *Dejanski kontekst* se nanaša na kateregakoli od treh virov za dejanske vrednosti v aplikaciji Project Operations:

       - Vrstice dnevnika vnosov, ki so ročno ustvarjene, ali vrstice dnevnika popravkov, ki so ustvarjene v dnevniku popravkov
       - Vrstice dnevnika, ki se ustvarijo med predložitvijo dnevnikov časa, stroškov ali porabe materiala
       - Podrobnosti vrstice računa

    Ko se aplikacija Project Operations ujema z datumom veljavnosti dohodne vrstice dnevnika ali podrobnosti vrstice računa v *dejanskem kontekstu*, uporablja polje **Datum transakcije**.

    - Če obstaja več cenikov, ki so v veljavi na datum dohodnega konteksta ocenjevanja ali dejanskega konteksta, bo izbran nazadnje ustvarjen cenik.
    - Če pogodbeni organizacijski enoti projekta ni priložen noben projektni cenik, sistem pregleda prodajne cenike, priložene projektnim parametrom, ki ustrezajo valuti projektne ponudbe.

## <a name="enable-multi-currency-cost-price-list"></a>Omogoči cenike z lastnimi cenami v več valutah

To nastavitev lahko najdete v razdelku **Nastavitve** \> **Parametri**. Privzeta vrednost je **Ne**.

Ko je ta nastavitev omogočena (to pomeni, da je vrednost nastavljena na **Da**), se sistem obnaša na naslednji način:

- Omogoča povezovanje cenikov z lastnimi cenami v katerikoli valuti z organizacijsko enoto. Na primer, cenik z lastnimi cenami v valuti EUR je lahko priložen organizacijski enoti v valuti USD. Sistem bo še naprej preverjal, ali ceniki z lastnimi cenami, ki so vezani na organizacijsko enoto, nimajo prekrivajoče se datumske veljavnosti.
- Preverja, ali ceniki z lastnimi cenami, ki so priloženi parametrom projekta, nimajo prekrivajoče se datumske veljavnosti, tudi če imajo različne valute. To vedenje se razlikuje od privzetega vedenja (tj. vedenja, ko je vrednost nastavljena na **Ne**). V privzetem vedenju se preverjajo samo ceniki z lastnimi cenami, ki imajo **enako** valuto, za neprekrivajočo se datumsko veljavnostjo.
- Za kontekst dohodne transakcije določi cenik z lastnimi cenami samo na podlagi datuma veljavnosti. To vedenje se razlikuje od privzetega vedenja, kjer sistem izbere cenik z lastnimi cenami, ki se ujema z valuto projekta in datumom veljavnosti.

Zaradi teh sprememb v vedenju bodo lahko stranke aplikacije Project Operations vzdrževale globalni cenik z lastnimi cenami, ki bo pomemben za celotno podjetje. Ne bo jim treba imeti cenikov v vsaki valuti poslovanja. Globalni cenik bo imel datumsko veljavnost in bo omogočal nastavitev mere stroškov v katerikoli valuti za določeno kombinacijo vrednosti cenovnih razsežnosti. Valuta cenika z lastnimi stroški se uporablja samo za vnos privzetih vrednosti, če so ustvarjeni zapisi elementov **Cene vlog**, **Cene kategorij** in **Cenik**. Valuta ne bo uporabljena za določitev cenika.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
