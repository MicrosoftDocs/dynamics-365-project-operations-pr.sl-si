---
title: Privzeti cenik
description: Ta tema vsebuje informacije o privzetih cenikih s prodajno in lastno ceno v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 275ef9b9706d212a6da0dc7c060081c3226572f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084635"
---
# <a name="default-price-lists"></a>Privzeti cenik

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

## <a name="sales-price-lists"></a>Prodajni ceniki

Vsaka projektna ponudba in pogodba v aplikaciji Dynamics 365 Project Operations vsebuje privzeti prodajni cenik. 

### <a name="price-list-default-on-project-quotes"></a>Privzeti cenik za projektne ponudbe
Sistem izvede spodnji postopek, da določi, kateri cenik bo privzeto uporabljen za projektno ponudbo:

1. Sistem preuči cenike, ki so priloženi projektnim cenikom računa. 
2. Če so zapisu o računu priloženi projektni ceniki, sistem pregleda prodajne cenike, priložene projektnim parametrom, ki ustrezajo valuti projektne ponudbe.
3. Nato sistem preveri veljavnost datumov cenikov, ki ustrezajo časovnemu obdobju projektne ponudbe. Še posebno datum, ko je bila ponudba ustvarjena.
4. Če je na datum projektne ponudbe v veljavi več cenikov, se vsi ceniki privzeto nastavijo za projektno ponudbo.
5. Če na datum projektne ponudbe ni v veljavi noben cenik, na projektni ponudbi ne bo privzetega projektnega cenika. Na projektni ponudbi se bo pojavilo opozorilno sporočilo. V sporočilu je zapisano, da dejanske vrednosti in ocene projekta ne bodo podane, ker niste priložili nobenega cenika.

### <a name="price-list-default-on-project-contracts"></a>Privzeti cenik za projektne pogodbe 
Sistem izvede spodnji postopek, da določi, kateri cenik bo privzeto uporabljen za projektno pogodbo:

1. Če je pogodba ustvarjena iz ponudbe, se projektni ceniki na ponudbi kopirajo ločeno in se priložijo projektni pogodbi.
2. Če je pogodba ustvarjena na novo, sistem pregleda cenike, ki so priloženi projektnim cenikom računa. Če zapisu o računu niso priloženi projektni ceniki, sistem poišče prodajne cenike, priložene projektnim parametrom, ki ustrezajo valuti projektne pogodbe.
4. Nato sistem preveri veljavnost datumov cenikov, ki ustrezajo časovnemu obdobju projektne pogodbe. Še posebno datum, ko je bila pogodba ustvarjena.
5. Če je na datum projektne pogodbe v veljavi več cenikov, se vsi ceniki privzeto nastavijo za projektno pogodbo.
6. Če na datum projektne pogodbe ni v veljavi noben cenik, na projektni pogodbi ne bo privzetega projektnega cenika. Na projektni pogodbi se bo pojavilo opozorilno sporočilo. V sporočilu je zapisano, da dejanske vrednosti in ocene projekta ne bodo podane, ker niste priložili nobenega cenika.

## <a name="cost-price-lists"></a>Cenik z lastnimi cenami

Ceniki z lastnimi cenami niso privzeto nastavljeni za nobeno entiteto v aplikaciji Project Operations. Določitev cenika z lastnimi cenami, ki se bo uporabil za stroške projekta, se vedno izvede na mestu uporabe. Sistem izvede spodnji postopek, da določi, kateri cenik bo uporabljen za stroške projekta:

1. Sistem najprej preuči cenike, ki so priloženi pogodbeni organizacijski enoti projekta.
2. Nato sistem preveri veljavnost datumov cenikov, ki se ujemajo z datumom dohodne vrstice ocene ali dejanske vrednosti. V tem primeru se *vrstica ocene* nanaša na vse tri kontekste ocenjevanja v aplikaciji Project Operations:

    - Vrstica ocene projekta
    - Podrobnosti vrstic ponudbe
    - Podrobnosti pogodb
  
3. Če obstaja več cenikov, ki so v veljavi na datum dohodne ocene ali dejanske vrednosti, bo izbran nazadnje ustvarjen cenik.
4. Če pogodbeni organizacijski enoti projekta ni priložen noben projektni cenik, sistem pregleda prodajne cenike, priložene projektnim parametrom, ki ustrezajo valuti projektne ponudbe.
5. Nato sistem preveri veljavnost datumov cenikov, ki se ujemajo z datumom dohodne vrstice ocene ali dejanske vrednosti. 
6. Če obstaja več cenikov, ki so v veljavi na datum dohodne ocene ali dejanske vrednosti, bo izbran nazadnje ustvarjen cenik.
7. Če projektnim parametrom, ki se ujemajo z valuto in datumom začetka veljavnosti, ni priložen noben prodajni cenik, sistem privzeto nastavi stopnjo stroškov na nič (0) za dohodne vrstice ocene ali dejanskih vrednosti.
