---
title: Kako začasno rezerviram vire v aplikaciji različice 2.x?
description: V tem članku je opisano, kako začasno rezervirate člane projektne ekipe v storitvi Project Service.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: a35799b422fa338c2666e1b2aa11bc2a54f5cce3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122273"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Kako začasno rezerviram vire v spletni aplikaciji (aplikacija Project Service različice 2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Za vir lahko okvirno načrtujete ali začasno rezervirate projektno ekipo in tako nakažete, da boste temu viru dodelili projekt. Začasne rezervacije ne porabijo razpoložljive zmogljivosti vira. Začasno rezerviranih članov ekipe ni mogoče dodeliti projektnim nalogam. Nalogam je mogoče dodeliti samo vire s stanjem veljavne rezervacije in vrsto obveznosti Potrjeno (ob upoštevanju, da imajo dovolj ur veljavnih rezervacij, ki jih potrebujejo za dodelitev).

Člani projektne ekipe, ki so začasno rezervirani, so prikazani na mreži članov ekipe, pri čemer so začasno rezervirane ure prikazane v stolpcu Začasno rezervirano. Prikazani so tudi na plošči razporeda. Vseeno pa porabljena zmogljivost ni navedena, ker začasne rezervacije ne vplivajo na zmogljivost vira.

Obstajajo trije načini za začasno rezervacijo člana skupine v projektu prek aplikacije Project Service različice 2.x. Začasno lahko rezervirate prek plošče razporeda, uporabite funkcijo Upravljanje rezervacij ali ustvarite splošen vir. Ti načini so opisani spodaj.

## <a name="soft-book-with-the-schedule-board"></a>Začasna rezervacija prek plošče razporeda

Za začasno rezervacijo prek plošče razporeda upoštevajte ta postopek: 
1. Odpiranje plošče razporeda.
2. Na dnu plošče Zahteve za rezervacije na plošči razporeda izberite zavihek Projekt.
3. Poiščite projekt, za katerega želite začasno rezervirati vir. Če imate več projektov, kliknite glavo stolpca Projekt in prek filtrov poiščite svoj projekt.
4. Kliknite projekt, nato ga povlecite in spustite na časovno mrežo vira.
5. Na desni se odpre plošča Ustvarjanje rezervacije vira. Nastavite začetni in končni datum, izberite stanje rezervacije Začasno in določite ure. 
6. Kliknite Rezerviraj.
7. V projektu bo vir zdaj prikazan kot član ekipe, začasno rezervirane ure pa bodo prikazane v stolpcu Začasno rezervirano.

Upoštevajte, da virov v strukturirani členitvi dela (SČD) ne morete dodeliti opravilom, ker morajo biti veljavno rezervirani v ekipi, da jih lahko dodelite.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Začasna rezervacija prek funkcije Upravljanje rezervacij

Za začasno rezervacijo prek funkcije Upravljanje rezervacij upoštevajte ta postopek:
1. Na mreži člana ekipe kliknite Novo.
2. Izberite vire, ki jih je mogoče rezervirati, vloge ter časovno obdobje.
3. Izberite način dodelitve, ki je različen od Brez:
- Polna zmogljivost
- Odstotek zmogljivosti
- Po urah, enakomerno
- Po urah, obremenitev na začetku
4. Kliknite Shrani. Vir bo prikazan na mreži ekipe, ure pa kot Veljavno rezervirane ure.
5. Ohranjanje rezervacije vira s klikom na Upravljanje rezervacij.
6. Ko se odpre plošča razporeda, razširite vir, da prikažete rezervacije. Rezervacija bo navedena kot Veljavna.
7. Z desno tipko miške kliknite rezervacijo, pod možnostjo Sprememba stanja izberite Začasna rezervacija in nato Začasna. Stanje rezervacije je Začasna.
8. Ko zaprete ploščo razporeda boste videli, da so se ure za vir na mreži ekipe spremenile iz Veljavno v Začasno.
Upoštevajte, da če veljavno rezervirate vir v ekipi in nato viru dodelite opravila v SČD, bodo, ko prek upravljanja rezervacij stanje spremenite iz veljavnega v začasno, dodelitve odstranjene iz opravil za ta vir, saj je samo veljavno rezerviranim virom mogoče dodeliti opravila.

## <a name="soft-book-by-creating-a-generic-resource"></a>Začasna rezervacija prek ustvarjanja splošnega vira

Začasno rezervacijo lahko ustvarite tudi tako, da ustvarite splošen vir v skupini članov, izpolnite ploščo razporeda ali zahtevo za vir in med postopkom rezervacije spremenite vrsto.
Upoštevajte spodnji postopek:

1. V SČD projekta dodelite vloge opravilom, za katera želite ustvariti splošnega člana ekipe.
2. Kliknite Ustvari projektno ekipo.
3. Na mreži člana ekipe izberite splošen vir in kliknite Rezerviraj.
4. Na plošči razporeda izberite vir, ki ga želite rezervirati.
5. Na plošči razporeda, v razdelku Ustvarjanje rezervacije vira, spremenite stanje rezervacije v Začasno.
6. Kliknite Rezerviraj ali Rezerviraj in zapri.

Ko zaprete ploščo razporeda boste izbrani vir videli v skupini, pri čemer so prikazane začasno rezervirane ure in dodeljene ure. Prav tako bo splošni vir ostal v ekipi kot indikator, da so opravila dodeljena začasno dodeljenemu članu ekipe.

Ko ste pripravljeni na spremembo začasne rezervacije člana ekipe v veljavno rezervacijo, da mu lahko dodelite opravila, naredite naslednje:

1. Izberite vir in kliknite Upravljanje rezervacij.
2. Ko se odpre plošča razporeda, razširite vir, da prikažete rezervacije. Rezervacija bo označena kot Začasna.
3. Z desno tipko miške kliknite rezervacijo, pod možnostjo Sprememba stanja izberite Veljavna rezervacija in nato Veljavna. Stanje rezervacije je Veljavna.
4. Ko zaprete ploščo razporeda boste videli, da so se ure za vir na mreži ekipe spremenile iz Začasno v Veljavno. Zdaj lahko viru dodelite opravila (ob upoštevanju, da so veljavno rezervirane ure usklajene s predvidenimi urami za opravilo). Če ste upoštevali korake za izpolnitev splošnega vira iz točke 3 zgoraj, bo, ko stanje začasno rezerviranega vira spremenite v veljavno rezerviranega, splošni član ekipe odstranjen iz ekipe.
