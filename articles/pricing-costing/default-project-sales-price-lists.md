---
title: Privzeti cenik
description: Ta članek nudi informacije o privzetih prodajah in cenikih stroškov v Project Operations.
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
1. Če zapisu računa ni priloženih cenikov projekta, sistem pogleda prodajne cenike, priložene parametrom projekta, ki se ujemajo z valuto ponudbe projekta.
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

Ceniki z lastnimi cenami niso privzeto nastavljeni za nobeno entiteto v aplikaciji Project Operations. Določanje cenika stroškov, ki se uporablja za stroške projekta, se vedno izvede na podlagi posamezne transakcije. Sistem izvede spodnji postopek, da določi, kateri cenik bo uporabljen za stroške projekta:

1. Sistem pregleduje cenike, ki so vezani na pogodbeno organizacijsko enoto projekta.
1. Nato sistem pogleda datum veljavnosti cenikov, ki se ujemajo z datumom konteksta dohodne ocene ali dejanskega konteksta.

    - *Ocenite kontekst* se nanaša na katerega koli od treh kontekstov ocenjevanja v projektnih operacijah:

        - Vrstica ocene projekta
        - Podrobnosti vrstic ponudbe
        - Podrobnosti pogodb

    - *Dejanski kontekst* se nanaša na katerega koli od treh virov za dejanske podatke v projektnih operacijah:

       - Vrstice dnevnika vnosov, ki so ročno ustvarjene, ali vrstice dnevnika popravkov, ki so ustvarjene v dnevniku popravkov
       - Vrstice dnevnika, ki se ustvarijo med predložitvijo dnevnikov časa, stroškov ali porabe materiala
       - Podrobnosti vrstice računa

    Ko se projektne operacije ujemajo z datumom veljavnosti dohodne vrstice dnevnika ali podrobnosti vrstice računa v *dejanski kontekst*, uporablja **Datum transakcije** polje.

    - Če velja več cenikov za datum vhodnega predračunskega konteksta ali dejanskega konteksta, se izbere nazadnje ustvarjen cenik.
    - Če k pogodbeni organizacijski enoti projekta ni priloženih cenikov, sistem pregleduje stroškovne cenike, ki so pripeti k parametrom projekta, ki ustrezajo valuti projekta.

## <a name="enable-multi-currency-cost-price-list"></a>Omogoči cenike z lastnimi cenami v več valutah

To nastavitev lahko najdete na **nastavitve** \> **Parametri**. Privzeta vrednost je **Ne**.

Ko je ta nastavitev omogočena (to pomeni, da je vrednost nastavljena na **ja**), se sistem obnaša na naslednji način:

- Omogoča povezovanje stroškovnih cenikov v poljubni valuti z organizacijsko enoto. Na primer, stroškovni cenik v valuti EUR je lahko priložen organizacijski enoti v valuti USD. Sistem bo še naprej preverjal, da stroškovni ceniki, ki so vezani na organizacijsko enoto, nimajo prekrivajoče se datumske veljavnosti.
- Potrjuje, da ceniki stroškov, ki so priloženi parametrom projekta, nimajo prekrivajočega se datuma, tudi če imajo različne valute. To vedenje se razlikuje od privzetega vedenja (tj. vedenja, ko je vrednost nastavljena na **št**). V privzetem vedenju so samo cenovni ceniki, ki imajo **enako** valute so potrjene za neprekrivajočo se datumsko veljavnost.
- Za kontekst dohodne transakcije določi cenik stroškov samo na podlagi datuma veljavnosti. To vedenje se razlikuje od privzetega vedenja, kjer sistem izbere cenik stroškov, ki se ujema z valuto projekta in datumom veljavnosti.

Zaradi teh sprememb v obnašanju bodo stranke Project Operations lahko vzdrževale cenik globalnih stroškov, ki bo pomemben za celotno podjetje. Ne bo jim treba imeti cenikov v posamezni valuti poslovanja. Globalni cenik bo veljal datumsko in bo omogočal nastavitev stopenj stroškov v kateri koli valuti za določeno kombinacijo vrednosti dimenzij cen. Valuta cenika stroškov se uporablja samo za vnos privzetih vrednosti, kadar **Cene vlog**, **kategorij**, in **Cenik** ustvarjeni so zapisi postavk. Ne bo uporabljen za določitev cenika.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
