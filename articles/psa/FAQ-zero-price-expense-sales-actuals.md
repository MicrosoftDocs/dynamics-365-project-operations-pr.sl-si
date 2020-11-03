---
title: Zakaj se cena pri dejanski vrednosti »strošek – prodaja« privzeto nastavi na nič?
description: 'Naslednja tri preverjanja vam bodo v pomoč pri odpravljanju naslednje težave: cena pri dejanski vrednosti »strošek – prodaja« se privzeto nastavi na 0.'
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5840bda4f74c720bfcdc7f4e84c8f22e0c6163ec
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084776"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Zakaj se cena pri dejanski vrednosti »strošek – prodaja« privzeto nastavi na nič?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

To pogosto vprašanje se nanaša na dejansko vrednost stroška, kjer je razred transakcije nastavljen na »Strošek«, vrsta transakcije pa je »Neobračunana prodaja«. Naslednja tri preverjanja vam bodo v pomoč pri odpravljanju naslednje težave: cena (obračunska stopnja) pri dejanski vrednosti »strošek – prodaja« se privzeto nastavi na 0.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>1. preverjanje: opredelitev prodajnega cenika za projekt

V polju projekta z dejansko vrednostjo poiščite projekt in pojdite na stran projekta. Nato odprite zavihek »Prodaja«. V mreži z vrsticami projektne pogodbe kliknite povezavo v polju »Projektna pogodba«. Odprla se bo stran projektne pogodbe. Na strani projektne pogodbe odprite zavihek »Projektni ceniki«. Preverite, ali je priložen vsaj en cenik.

Če v mreži projektnih cenikov projektne pogodbe ni priložen noben cenik, naredite naslednje:

- Cenik pripnite v mrežo projektnih cenikov. Ceniki, ki jih je tukaj dovoljeno priložiti, morajo imeti kontekstno polje nastavljeno na »Prodaja«, polje »Valuta« na ceniku pa se mora ujemati s poljem »Valuta« v projektni pogodbi. Ko izvedete potrebne popravke, znova ustvarite vnos stroška, ga odobrite in preverite, ali dejanska vrednost neobračunane prodaje prikazuje veljavno ceno.
- Če je v mreži projektnih cenikov projektne pogodbe priložen en cenik ali več, pojdite na 2. preverjanje.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>2. preverjanje: ali je kateri od cenikov, opredeljenih zgoraj, veljaven za določeni datum dejanske vrednosti stroška?

Da bi storitev Project Service upoštevala cenik za nastavljanje privzete cene, bi moral ta cenik veljati za datum za dejansko vrednost »strošek – prodaja«. Preverite naslednje, da ugotovite, ali so ceniki, opredeljeni zgoraj, veljavni:

- Najprej se prepričajte, da sta začetni in končni datum na zavihku »Splošno« za priložene cenike izpolnjena. Če začetni in končni datum na cenikih, opredeljenih zgoraj, nista izpolnjena, ste osamili težavo. 
- Zabeležite si polje z začetnim datumom za dejansko vrednost »strošek – prodaja« in preverite, ali je kateri od opredeljenih cenikov veljaven za ta datum. Datum dejanske vrednosti stroška bi moral biti na primer med začetnim datumom in končnim datumom na ceniku. 
    - Če ni cenika, ki bi zajemal ta datum za dejansko vrednost »strošek – prodaja«, ste osamili težavo. Spremenite začetni in končni datum na ceniku in s tem zagotovite, da bo cenik zajemal datum za dejansko vrednost stroška. 
    - Če obstaja več kot en cenik, ki zajema datum za dejansko vrednost »strošek – prodaja«, ste osamili težavo. To lahko popravite tako, da uredite začetni in končni datum na cenikih, da bo obstajal samo en cenik, ki bo zajemal datum dejanske vrednosti stroška. 
    - Če obstaja samo en cenik, ki zajema ta datum dejanske vrednosti stroška, se premaknite na 3. preverjanje.
Ko izvedete potrebne popravke, znova ustvarite vnos stroška, ga odobrite in preverite, ali dejanska vrednost neobračunane prodaje prikazuje veljavno ceno.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>3. preverjanje: ali obstaja veljavna cena za kategorijo stroška v veljavnem projektnem ceniku? 

Če ste uspešno zaključili 1. in 2. preverjanje, bi morali zdaj imeti samo en projektni cenik, ki velja za datum dejanske vrednosti »strošek – prodaja«. Odprite ta projektni cenik in pojdite na zavihek »Cene kategorij«. Prepričajte se, da je v mreži vrstica za posebno kategorijo stroška pri dejanski vrednosti stroška.
 
- Če ni nobene vrstice, ste osamili težavo. Ustvarite vrstico v mreži »Cena kategorije« za kategorijo pri dejanski vrednosti stroška. Ko to naredite, znova ustvarite vnos stroška, ga odobrite in preverite, ali dejanska vrednost neobračunane prodaje prikazuje veljavno ceno. 
- Če je v mreži s cenami kategorij prikazana vrstica za kategorijo stroška, preverite, ali ima veljavno ceno.

Da bi razumeli, kaj je veljavna cena, uporabite te načine:

- Če je polje »Način oblikovanja cen« v vrstici »Cena kategorije« nastavljeno na »Nabavna cena«, bo cena enote pri dejanski vrednosti »strošek – prodaja« privzeto nastavljena na vrednost v vnosu stroška.
- Če je polje »Način oblikovanja cen« v vrstici »Cena kategorije« nastavljeno na »Odstotek pribitka«, preverite, ali je polje »Odstotek« nastavljeno na veljavno vrednost. Če uporabite ta odstotek pribitka, se cena enote pri dejanski vrednosti »strošek – prodaja« privzeto nastavi na ceno v vnosu stroška.
- Če je polje »Način oblikovanja cen« v vrstici »Cena kategorije« nastavljeno na »Cena na enoto«, preverite, ali je polje »Cena« nastavljeno na veljavno vrednost. Cena enote pri dejanski vrednosti »strošek – prodaja« bo privzeto nastavljena na znesek valute, določen v polju »Cena«.

Če nastavljena cena za kategorijo stroška ni veljavna, ste osamili težavo. Rešitev je, da uredite vrstico s cenami kategorij z veljavno ceno za kategorijo stroška v skladu z zgornjimi pravili. Ko to naredite, znova ustvarite vnos stroška, ga odobrite in nato preverite, ali ima dejanska vrednost neobračunane prodaje veljavno ceno.

Če po treh opravljenih preverjanjih, opisanih zgoraj, še vedno ne vidite veljavne cene pri dejanski vrednosti »strošek – prodaja«, vložite zahtevo za podporo.


