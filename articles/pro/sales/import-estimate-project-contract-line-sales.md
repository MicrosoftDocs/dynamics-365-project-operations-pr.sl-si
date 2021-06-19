---
title: Uvoz ocene v podrobnosti pogodbe, ki temeljijo na projektu – poenostavljena različica
description: Ta tema vsebuje informacije o uvozu finančnih ocen projekta v podrobnosti pogodbe.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cbd1745f9b6a59a4a03c456cbbc3b7d0b427a2d3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003360"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Uvoz ocene v podrobnosti pogodbe, ki temeljijo na projektu – poenostavljena različica

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V aplikaciji Dynamics 365 Project Operations lahko uvozite ocene iz projekta v podrobnost pogodbe, ki temelji na projektu.

1. Preverite, ali je polje **Projekt** v podrobnostih pogodbe na podlagi projekta izpolnjeno.
2. V zavihku **Podrobnosti pogodb** na podmreži izberite **Uvozi iz ocene projekta**. Odpre se pogovorno okno z možnostmi povzemanja. Razpoložljive možnosti povzemanja so **Razred transakcije**, **Kategorija**, **Vloga** in **Projektno opravilo**.
3. Na podlagi izbranih možnosti za povzemanje je prekopirana ocena iz projekta za vse razrede transakcij in opravil, ki so vključeni v teh podrobnostih pogodb. Če želite preveriti, kateri razredi transakcij so vključeni, izberite zavihek **Splošno** v podrobnostih pogodb na podlagi projekta in preverite vrednosti v poljih **Vključi čas**, **Vključi stroške** in **Vključi dajatve**. 
4. Če si želite ogledati, katera opravila so vključena, izberite zavihek **Plačljiva opravila** v podrobnostih pogodbe. Na podlagi povezanih opravil, ki imajo polje **Vključeni razredi transakcij** nastavljeno na **Da**, se ocene za te kombinacije opravil in razredov transakcij uvozijo v podrobnosti pogodbe.

Pri uvozu ocen sistem privzeto določi cene na podlagi cenikov projekta, priloženih pogodbi, in vrste obračuna, nastavljene v podrobnostih pogodbe. Če je opravilo, vloga ali kategorija v podrobnostih pogodbe nastavljena kot nezaračunljiva, bo uvožena ocenjevalna vrstica nastavljena kot nezaračunljiva in ne bo prispevala k pogodbeni vrednosti podrobnosti pogodbe.

Če imajo podrobnosti pogodbe podrobnosti o vrstici, sta polji **Vrednost pogodbe** in **Ocenjeni davek** v podrobnostih pogodbe povzeti in ju ni mogoče urejati.

Če je izbranih več možnosti povzetka, sistem poskuša povzetek ustvariti po vseh izbranih možnostih. Rezultat povzemanja bo vseboval več uvoženih podrobnosti pogodbe, kot če izberete samo eno možnost povzemanja.

Če ima projekt na primer naslednje vrstice ocen za stroške:

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| Opravilo A | Letalska vozovnica | 10. 1. 2020 | 4 | 400 | 1600 |
| Opravilo B | Hotel | 1. 10. 2020 | 4 | 200 | 800 |
| Opravilo C | Hotel | 1. 11. 2020 | 2 | 200 | 400 |

Če uporabnik izbere povzetek po **Razredu transakcij**, bodo uvoženi naslednji podatki:

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10. 1. 2020 | 3.34 | 840 | 2800 |

Če uporabnik izbere povzetek po **Razredu transakcij** in **Kategoriji**, bodo uvoženi naslednji podatki:

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| Opravilo A | Letalska vozovnica | 1. 10. 2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 1. 10. 2020 | 6 | 200 | 1200 |

Če uporabnik izbere povzetek glede na **Razred transakcij**, **Kategorijo** in **Opravilo listnega vozlišča**, bodo uvoženi naslednji podatki. Upoštevajte, da je ta rezultat enak tistemu na projektu:

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| Opravilo A | Letalska vozovnica | 10. 1. 2020 | 4 | 400 | 1600 |
| Opravilo B | Hotel | 1. 10. 2020 | 4 | 200 | 800 |
| Opravilo C | Hotel | 1. 11. 2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]