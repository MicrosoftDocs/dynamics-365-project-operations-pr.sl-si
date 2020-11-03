---
title: Načini za rezervacijo dodelitev v storitvi Project Service Automation
description: V tej temi najdete informacije o različnih načinih za rezervacijo dodelitev.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 295da428ce15e7775450dfa94e96047f200bdede
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084750"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Načini za rezervacijo dodelitev v storitvi Project Service Automation

Če člana ekipe dodate projektu neposredno na zavihku **Ekipa** ali rezervirate vir za projekt oz. zahtevo na plošči razporeda, lahko uporabite več različnih načinov rezervacije dodelitev. V tej temi je pojasnjeno, kako delujejo posamezni načini in kateri načini lahko vodijo v preveliko število rezervacij virov.

## <a name="full-capacity"></a>Polna zmogljivost 
Način »Polna zmogljivost« rezervira polno zmogljivost vira za navedeni datumski obseg. Če je na primer koledar vira nastavljen za delo osem ur na dan in pet dni v tednu, bo vir rezerviran za 40 ur, če nastavite začetni in končni datum, ki zajema pet delovnih dni. Rezervacija je zaključena ne glede na preostalo zmogljivost vira. Če je vir v tem obdobju že rezerviran za druge projekte, je 40 ur rezerviranih kot dodatne ure, kar lahko vodi v preveliko število rezervacij.

## <a name="remaining-capacity"></a>Preostanek zmogljivosti
Način »Preostanek zmogljivosti« je na voljo samo, če projekt rezervirate neposredno prek plošče razporeda. Ta način rezervira razpoložljivo zmogljivost vira v določenem datumskem obsegu. Če ima vir na primer zmogljivost 40 ur na teden in je že rezerviran za 10 ur, rezervacija za isti teden pomeni rezervacijo preostalih 30 ur zmogljivosti za ta teden.

## <a name="percentage-capacity"></a>Odstotek zmogljivosti
Način »Odstotek zmogljivosti« rezervira vir za odstotek zmogljivosti za navedeni datumski obseg. Če je na primer koledar vira nastavljen za delo osem ur na dan in pet dni v tednu ter nastavite začetni in končni datum, ki zajema pet delovnih dni pri 50 % zmogljivosti, bo vir rezerviran za 20 ur. Posamezne rezervacije na dan so enakomerno porazdeljene v obdobju, v tem primeru štiri ure na dan. Rezervacija je zaključena ne glede na preostalo zmogljivost vira. Če je vir v tem obdobju že rezerviran za druge projekte, je 20 ur rezerviranih kot dodatne ure, kar lahko vodi v preveliko število rezervacij.

## <a name="evenly-distribute-hours"></a>Enakomerna porazdelitev ur
Način »Enakomerna porazdelitev ur« rezervira vir za določeno število ur, pri tem pa čas porazdeli enakomerno na dan v določenem datumskem obsegu. Če vir na primer rezervirate za 20 ur v petdnevnem obdobju, ta način enakomerno porazdeli 20 ur na štiri ure na dan. Rezervacija je zaključena ne glede na preostalo zmogljivost vira. Če je vir v tem obdobju že rezerviran za druge projekte, je 20 ur rezerviranih kot dodatne ure, kar lahko vodi v preveliko število rezervacij.

## <a name="front-load-hours"></a>Ure obremenitve na začetku
Način »Ure obremenitve na začetku« rezervira vir za določeno število ur, pri tem pa ure na dan porazdeli na začetek dneva v določenem datumskem obsegu. Obremenitev na začetku porablja razpoložljivo zmogljivost vira v vrstnem redu »prvi rezerviran, prvi porabljen«. Če je na primer razpored dela vira osem ur na dan, pet dni v tednu, vir pa nima trenutnih rezervacij, rezervacija vira za 20 ur v petdnevnem obdobju ustvari ta vzorec dnevnih rezervacij: 

|         Rezervacije          |    1. dan    |    2. dan    |    3. dan    |    4. dan    |    5. dan    |    Skupno    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Obstoječe rezervacije    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Nova rezervacija          |    8        |    8        |    4        |    0        |    0        |    20       |

Način obremenitve na začetku upošteva obstoječe rezervacije in razpoložljivo zmogljivost. Če ima na primer isti vir v delovnem tednu rezerviranih že 20 ur, nove rezervacije porabijo preostalo zmogljivost na naslednji način:

|   Rezervacije          | 1. dan | 2. dan | 3. dan | 4. dan | 5. dan | Skupno |
|---------------------|-------|-------|-------|-------|-------|-------|
| Obstoječe rezervacije | 8     | 8     | 4     | 0     | 0     | 20    |
| Nova rezervacija       | 0     | 0     | 4     | 8     | 8     | 20    |

Ker se upošteva razpoložljiva zmogljivost, lahko prejmete sporočilo o napaki, če vir nima preostale zmogljivosti, ki bi jo rezervacija lahko prevzela. S tem načinom ne morete doseči prevelikega števila rezervacij.

## <a name="none"></a>Ni priprav ali omejitev
Način »Brez« je na voljo samo, če rezervacijo ustvarite na zavihku **Ekipa** znotraj projekta. Ta način projektu doda vir kot člana ekipe, vendar ne ustvari rezervacij, ki bi prevzele zmogljivost vira. Ta način se uporablja, če je privzeti vodja projekta kot član ekipe dodan, ko se ustvari projekt. Vodja projekta kot uporabnik, ki je ustvaril projekt, se projektu privzeto doda, tako da ima zapis entitete projekta lastnika in da obstaja en odobritelj pri projektu. Ker ta uporabnik nima rezervacij, lahko, če želite rezervirati vir, izbrišete vir in ga nato znova dodate ter pri tem uporabite drug način dodeljevanja, ali pa dodate vir opravilom in nato na zavihku **Uskladitev** uporabite možnost **Podaljšanje rezervacij** , s katero ustvarite rezervacije za dodelitve.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Načini dodelitev, ki vodijo v preveliko število rezervacij
Če povzamemo, naslednji načini dodeljevanja vodijo v preveliko število rezervacij, če je vir že dodeljen za druge projekte (ali za druge delovne naloge ali entitete za razporejanje):

- Polna zmogljivost
- Odstotek zmogljivosti
- Enakomerna porazdelitev ur

Če uporabite enega od teh treh načinov dodeljevanja, ne boste obveščeni o tem, da je bilo doseženo preveliko število rezervacij vira. Če želite popraviti preveliko število rezervacij, morate uporabiti ploščo razporeda.
