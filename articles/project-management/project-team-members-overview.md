---
title: Člani projektne ekipe
description: Ta tema vsebuje informacije o tem, kako delati s podatki, atributi in razporejanjem glede članov projektnih ekip.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f4941803c657fab55ee2702d9f58d6e333592889
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084647"
---
# <a name="project-team-members"></a>Člani projektne ekipe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Člani projektnih ekip so udeleženci projekta, ki zaključijo delo na projektu. Cilj mreže članov ekipe je zagotoviti seznam imenovanih virov, ki so predani interakciji, in splošnih članov ekipe, ki predstavljajo ograde za vire, ki bodo kasneje zaposleni.

Iz mreže članov ekipe lahko vodja projekta in drugi udeleženci projekta vidijo, kdo je zavezan projektu. Ogledajo si lahko tudi povzetek svojih rezervacij, načrtovanega obsega dela in posameznih dodelitev virov. Mreža članov ekipe omogoča vodjem projektov, da opredelijo zahteve za vir za splošne člane ekipe in upravljajo rezervacije obstoječih članov ekipe.

V naslednji tabeli so navedeni ključni atributi člana projektne skupine.

| Ime polje          | Opis                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Način dodelitve        | Način dodelitve, ki se uporablja za rezervacijo virov za projekt.                                                                         |
| Vrsta obračunavanja             | Izberite, ali je član ekipe razvrščen kot plačljiv.                                                                                                                                       |
| Vir, ki ga je mogoče rezervirati        | Vir, ki ga je mogoče rezervirati, izbran, da nadomesti splošni vir                                                                                                                   |
| Stanje izbrisa            | Stanje izbrisa člana skupine za sledenje, ali je bila v PSS poslana zahteva za izbris in ali PSS uspešno in v pričakovanem časovnem obdobju pošlje nazaj odgovor. |
| Skupni obseg dela (ure)     | Količina obsega dela člana ekipe pri njegovih nalogah.                                                                                                                         |
| Končni obseg dela (ure) | Sledenje obsegu dela, ki ga izvede član ekipe pri dodeljenih nalogah.                                                                                           |
| Preostanek dela (ure) | Sledenje obsegu dela, ki ga član ekipe še ni izvedel pri dodeljenih nalogah.                                                                                    |
| Konec                   | Končni datum članstva ekipe virov.                                                                                                                                            |
| Veljavno rezervirane ure        | Veljavno rezervirane ure člana ekipe.                                                                                                                                                                |
| Naziv delovnega mesta            | Ime, ki se uporablja za identifikacijo splošnega vira.                                                                                                                                   |
| Enota vira          | Organizacijska enota vira, ki opravlja delo                                                                                                                      |
| Odobritelj projekta         | Izberite, ali lahko član ekipe odobri čas in stroške.                                                                                                                     |
| Zahtevane ure dela           | Zahtevane ure za člana ekipe iz pogojev za člana ekipe.                                                                                                                       |
| Vloga                     | Vloga, ki jo član ekipe zaseda pri tej ekipi.                                                                                                                                |
| Opis delovnega mesta     | Vnesite opis vloge tega člana ekipe.                                                                                                                             |
| Začasno rezervirane ure        | Začasno rezervirane ure člana ekipe.                                                                                                                                                                 |
| Zaženi                    | Začetni datum članstva ekipe virov.                                                                                                                                          |

Iz mreže članov ekipe lahko izvedete naslednja dejanja:

- **Rezerviraj** : za organizacije, ki uporabljajo metodologijo hibridnih rezervacij, bo dejanje rezervacije uporabnikom omogočilo, da rezervirajo imenovani vir na podlagi zahtev, ki jih ustvari splošni član ekipe.
- **Ustvari zahtevo** : s tem dejanjem se ustvari zahteva.
- **Navedi vzorec** : omogoča vodjem projektov, da natančno prilagodijo krivulje potreb po virih. Vodje projektov se lahko prilagodijo specifičnim potrebam projekta, kadar privzeta porazdelitev ne ustreza.
- **Pošlji zahtevo** : za organizacije, ki uporabljajo centralno metodologijo rezervacij.
- **Uredi** : atribute članov ekipe lahko urejate, vključno z organizacijsko enoto, vlogo in imenom položaja.
- **Upravljaj rezervacije** : ko je treba posodobiti rezervacije virov, upravljanje rezervacij omogoča vodji projekta, da prilagodi:

    - Začetek
    - Konec
    - Dodelitev skupnega obsega dela

- **Novo** : poleg dodajanja virov neposredno iz razporeda lahko vodje projektov iz mreže članov ekipe dodajo nove imenovane ali splošne člane ekipe.
- **Izbriši** : z izbiro enega ali več članov ekipe lahko vodja projekta izbriše vire, ki ne bodo več sodelovali v projektu. Če izbrišete člana ekipe, boste izbrisali tudi vse povezane dodelitve virov in preklicali vse obstoječe rezervacije.
