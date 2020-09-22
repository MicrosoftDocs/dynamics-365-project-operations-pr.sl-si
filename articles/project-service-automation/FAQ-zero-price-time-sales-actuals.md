---
title: Zakaj se cena pri dejanski vrednosti »čas – prodaja« privzeto nastavi na nič?
description: 'Odpravljanje težav: cena pri dejanski vrednosti »čas – prodaja« se privzeto nastavi na 0.'
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 202ee371-2863-4bcf-918c-212d7293faa8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 04ab519955b55088d85bdf36c3a90835f70ea501
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755817"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Zakaj se cena pri dejanski vrednosti »čas – prodaja« privzeto nastavi na nič?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

To pogosto vprašanje se nanaša na dejansko vrednost, kjer je razred transakcije nastavljen na »Čas«, vrsta transakcije pa je »Neobračunana prodaja«. Naslednja tri preverjanja vam bodo v pomoč pri odpravljanju naslednje težave: cena (obračunska stopnja) pri dejanski vrednosti »čas – prodaja« se privzeto nastavi na 0.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>1. preverjanje: opredelitev prodajnega cenika za projekt

V polju projekta z dejansko vrednostjo poiščite projekt in pojdite na stran projekta. Nato odprite zavihek »Prodaja« in v mreži z vrsticami projektne pogodbe kliknite povezavo v polju »Projektna pogodba«. Odprla se bo stran projektne pogodbe. Na strani projektne pogodbe odprite zavihek »Projektni ceniki«. Preverite, ali je priložen vsaj en cenik. Če v mreži projektnih cenikov projektne pogodbe ni priložen noben cenik, ste osamili težavo. Cenik pripnite v mrežo projektnih cenikov. Ceniki, ki jih je tukaj dovoljeno priložiti, morajo imeti kontekstno polje nastavljeno na »Prodaja«, polje »Valuta« na ceniku pa se mora ujemati s poljem »Valuta« v projektni pogodbi. Ko izvedete potrebne popravke, znova ustvarite vnos časa, ga odobrite in preverite, ali dejanska vrednost neobračunane prodaje prikazuje veljavno ceno. 

Če je v mreži projektnih cenikov projektne pogodbe priložen en cenik ali več, pojdite na naslednje preverjanje v dokumentu.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>2. preverjanje: ali je kateri od cenikov, opredeljenih zgoraj, veljaven za določeni datum dejanske vrednosti »čas – prodaja«?

Da bi storitev Project Service upoštevala cenik za nastavljanje privzete cene, bi moral ta cenik veljati za datum za dejansko vrednost »čas – prodaja«. Preverite naslednje, da ugotovite, ali so ceniki, opredeljeni zgoraj, veljavni:
- Prepričajte se, da sta začetni in končni datum na zavihku »Splošno« za priložene cenike izpolnjena. Če začetni in končni datum na cenikih, opredeljenih zgoraj, nista izpolnjena, ste osamili težavo. 
- Zabeležite si polje z začetnim datumom za dejansko vrednost »čas – prodaja« in preverite, ali je kateri od opredeljenih cenikov veljaven za ta datum. Datum dejanske vrednosti »čas – prodaja« bi moral biti na primer med začetnim datumom in končnim datumom na ceniku. 
    - Če ni cenika, ki bi zajemal ta datum za dejansko vrednost »čas – prodaja«, ste osamili težavo. Spremenite začetni in končni datum na ceniku in s tem zagotovite, da bo cenik zajemal datum za dejansko vrednost »čas – prodaja«. 
    - Če obstaja več kot en cenik, ki zajema datum za dejansko vrednost »čas – prodaja«, ste osamili težavo. To lahko popravite tako, da uredite začetni in končni datum na cenikih, da bo obstajal samo en cenik, ki bo zajemal datum dejanske vrednosti »čas – prodaja«. 
    - Če obstaja samo en cenik, ki zajema ta datum dejanske vrednosti »čas – prodaja«, pojdite na 3. preverjanje.
Ko izvedete potrebne popravke, znova ustvarite vnos časa, ga odobrite in preverite, ali dejanska vrednost »čas – prodaja« prikazuje veljavno ceno.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>3. preverjanje: ali obstaja cena v ceniku za cenovne razsežnosti pri dejanski vrednosti »čas – prodaja«?

Če ste uspešno zaključili 1. in 2. preverjanje, bi morali zdaj imeti samo en cenik, ki velja za datum dejanske vrednosti »čas – prodaja«. Odprite ta cenik in se pomaknite na zavihek »Cene vlog«. Prepričajte se, da je v mreži vrstica za cenovne razsežnosti pri dejanski vrednosti »čas – prodaja«.

Če v mreži cen vlog za cenovne razsežnosti pri dejanski vrednosti »čas – prodaja« ni nobene vrstice, ste osamili težavo. Ustvarite vrstico v mreži »Cene vlog« za cenovne razsežnosti pri dejanski vrednosti »čas – prodaja«. Ko to naredite, znova ustvarite vnos časa, ga odobrite in preverite, ali dejanska vrednost »čas – prodaja« prikazuje veljavno ceno.

Če po treh opravljenih preverjanjih, opisanih zgoraj, še vedno ne vidite veljavne cene pri dejanski vrednosti »čas – prodaja«, vložite zahtevo za podporo. 

