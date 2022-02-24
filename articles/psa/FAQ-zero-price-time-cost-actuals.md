---
title: Zakaj se cena pri dejanski vrednosti »čas – cena« privzeto nastavi na nič?
description: 'Odpravljanje težav: cena pri dejanski vrednosti »čas – cena« se privzeto nastavi na 0.'
author: rumant
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
ms.openlocfilehash: ffe915a48f088bde457121a323325ba490c24e45
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993076"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Zakaj se cena pri dejanski vrednosti »čas – cena« privzeto nastavi na nič?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

To pogosto vprašanje se nanaša na dejansko vrednost, kjer je razred transakcije nastavljen na »Čas«, vrsta transakcije pa je »Cena«. Naslednja tri preverjanja vam bodo v pomoč pri odpravljanju naslednje težave: cena pri dejanski vrednosti »čas – cena« se privzeto nastavi na 0.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>1. preverjanje: opredelitev cenika z lastnimi cenami za projekt

V polju projekta z dejansko vrednostjo poiščite projekt in nato pojdite na stran projekta. V polju kliknite povezavo do pogodbene enote. Na strani pogodbene enote preverite, ali je v mreži cenikov z lastnimi cenami na voljo cenik za pogodbeno enoto.

Če obstaja več kot en cenik, ste osamili težavo. Storitev Project Service podpira samo en cenik na organizacijsko enoto. Odstranite vse cenike pri tej entiteti, dokler v mreži organizacijske enote s ceniki z lastnimi cenami ne bo priložen samo en cenik.

Če v organizacijski enoti ni priloženega cenika, si zabeležite valuto organizacijske enote. Odprite Project Service in nato možnost »Parametri« ter odprite zavihek »Ceniki«. Preverite, ali so na voljo ceniki, pri katerih je kontekst nastavljen na »Cena« in kjer se valuta ujema z valuto organizacijske enote.
 
Če ni cenikov, ki bi ustrezali tem merilom, ste osamili težavo. Prepričajte se, da imate vsaj en cenik, pri katerem je kontekst nastavljen na »Cena« in kjer se valuta ujema z valuto organizacijske enote.

Če obstaja več kot en cenik, ki ustreza tem merilom, dalje berite ta dokument, da izvedete več preverjanj.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>2. preverjanje: ali je kateri od cenikov, opredeljenih zgoraj, veljaven za določeni datum dejanske vrednosti »čas – cena«?

Da bi storitev Project Service upoštevala cenik za nastavljanje privzete cene, bi moral ta cenik veljati za datum za dejansko vrednost »čas – cena«. Preverite naslednje, da ugotovite, ali so ceniki, opredeljeni zgoraj, veljavni:

- Prepričajte se, da sta začetni in končni datum na zavihku »Splošno« za priložene cenike izpolnjena. Če začetni in končni datum na cenikih, opredeljenih zgoraj, nista izpolnjena, ste osamili težavo. 
- Zabeležite si polje z začetnim datumom za dejansko vrednost »čas – cena« in preverite, ali je kateri od opredeljenih cenikov veljaven za ta datum. Datum dejanske vrednosti »čas – cena« bi moral biti na primer med začetnim datumom in končnim datumom na ceniku. 
    - Če ni cenika, ki bi zajemal ta datum za dejansko vrednost »čas – cena«, ste osamili težavo. Spremenite začetni in končni datum na ceniku in s tem zagotovite, da bo cenik zajemal datum za dejansko vrednost »čas – cena«. 
    - Če obstaja več kot en cenik, ki zajema datum za dejansko vrednost »čas – cena«, ste osamili težavo. To lahko popravite tako, da uredite začetni in končni datum na cenikih, da bo obstajal samo en cenik, ki bo zajemal datum dejanske vrednosti »čas – cena«. 
    - Če obstaja samo en cenik, ki zajema ta datum dejanske vrednosti »čas – cena«, se premaknite na naslednje preverjanje v dokumentu.
Ko izvedete potrebne popravke, znova ustvarite vnos časa, ga odobrite in preverite, ali dejanska vrednost »čas – cena« prikazuje veljavno ceno.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>3. preverjanje: ali obstaja cena v ceniku za cenovne razsežnosti pri dejanski vrednosti »čas – cena«?

Če ste uspešno zaključili 1. in 2. preverjanje, bi morali zdaj imeti samo en cenik, ki velja za datum dejanske vrednosti »čas – cena«. Odprite ta cenik in pojdite na zavihek »Cene vlog«. Prepričajte se, da je v mreži vrstica za cenovne razsežnosti pri dejanski vrednosti »čas – cena«.

Če v mreži cen vlog za cenovne razsežnosti pri dejanski vrednosti »čas – cena« ni nobene vrstice, ste osamili težavo. Ustvarite vrstico v mreži »Cene vlog« za cenovne razsežnosti pri dejanski vrednosti »čas – cena«. Ko to naredite, znova ustvarite vnos časa, ga odobrite in preverite, ali dejanska vrednost »čas – cena« prikazuje veljavno ceno.
 
Če po treh opravljenih preverjanjih, opisanih zgoraj, še vedno ne vidite veljavne cene pri dejanski vrednosti »čas – cena«, vložite zahtevo za podporo.





[!INCLUDE[footer-include](../includes/footer-banner.md)]