---
title: Uvoz ocene v podrobnosti pogodbe, ki temeljijo na projektu
description: Ta tema vsebuje informacije o tem, kako uvoziti ocene projekta v podrobnosti pogodbe.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f2b9cbb4cce1691f262c85d95849e01f1a812d51
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/20/2020
ms.locfileid: "4084991"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Uvoz ocene v podrobnosti pogodbe, ki temeljijo na projektu

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

V storitvi Dynamics 365 Project Operations lahko uvozite ocene iz projekta v podrobnosti pogodbe na podlagi projekta.

1. Preverite, ali je polje **Projekt** v podrobnostih pogodbe na podlagi projekta izpolnjeno.
2. V zavihku **Podrobnosti pogodb** na podmreži izberite **Uvozi iz ocene projekta**. Odpre se pogovorno okno z možnostmi povzemanja. Razpoložljive možnosti povzemanja so **Razred transakcije**, **Kategorija**, **Vloga** in **Projektno opravilo**. Na podlagi izbranih možnosti za povzemanje je prekopirana ocena iz projekta za vse razrede transakcij, ki so vključeni v teh podrobnostih pogodb. 
3. Če želite preveriti, kateri razredi transakcij so vključeni, izberite zavihek **Splošno** v podrobnostih pogodb in preverite vrednosti v poljih **Vključi čas**, **Vključi stroške** in **Vključi dajatve**.

Pri uvozu ocen aplikacija privzeto določi cene na podlagi cenikov projekta, priloženih pogodbi, in vrste obračuna, nastavljene v podrobnostih pogodbe. Če je vloga ali kategorija v podrobnostih pogodbe nastavljena kot nezaračunljiva, bo uvožena ocenjevalna vrstica za to vlogo ali kategorijo nastavljena kot nezaračunljiva in ne bo prispevala k pogodbeni vrednosti podrobnosti pogodbe.

Če imajo podrobnosti pogodbe podrobnosti o vrstici, sta polji **Vrednost pogodbe** in **Ocenjeni davek** v podrobnostih pogodbe povzeti in ju ni mogoče urejati.

Če je izbranih več možnosti povzetka, sistem poskuša povzetek ustvariti po vseh izbranih možnostih. Rezultat povzemanja bo vseboval več uvoženih podrobnosti pogodbe, kot če izberete samo eno možnost povzemanja.

Če je imel projekt na primer naslednje vrstice ocen za stroške:

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| Opravilo A | Letalska vozovnica | 10. 1. 2020 | 4 | 400 | 1600 |
| Opravilo B | Hotel | 1. 10. 2020 | 4 | 200 | 800 |
| Opravilo C | Hotel | 1. 11. 2020 | 2 | 200 | 400 |

Če uporabnik izbere povzetek po **Razredu transakcij**, bodo uvoženi naslednji podatki:

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 10. 1. 2020 | 3.34 | 840 | 2800 |

Če uporabnik izbere povzetek po **Razredu transakcij** in **Kategoriji**, bodo uvoženi naslednji podatki:

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| Opravilo A | Letalska vozovnica | 1. 10. 2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 1. 10. 2020 | 6 | 200 | 1200 |

Če uporabnik izbere povzetek glede na **Razred transakcij**, **Kategorijo** in **Opravilo listnega vozlišča**, bodo uvoženi naslednji podatki. Upoštevajte, da je ta rezultat enak tistemu na projektu:

| Opravilo | Kategoriji | Datum | Količina | Cena enote | Znesek |
| --- | --- | --- | --- | --- | --- |
| Opravilo A | Letalska vozovnica | 10. 1. 2020 | 4 | 400 | 1600 |
| Opravilo B | Hotel | 1. 10. 2020 | 4 | 200 | 800 |
| Opravilo C | Hotel | 1. 11. 2020 | 2 | 200 | 400 |
