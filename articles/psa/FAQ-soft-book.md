---
title: Začasna rezervacija vira
description: V tej temi so na voljo informacije o tem, kako okvirno načrtujete ali začasno rezervirate člane projektne ekipe.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 36246dadb1c4ba0234ae1042ba9e78c96f9d2bd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992937"
---
# <a name="soft-book-a-resource"></a>Začasna rezervacija vira

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Za vir lahko okvirno načrtujete ali začasno rezervirate projektno ekipo in tako nakažete, da boste temu viru dodelili projekt. Začasna rezervacija ne zmanjša razpoložljive zmogljivosti vira, pri čemer lahko začasno rezervirane člane ekipe dodelite projektnim nalogam. Ker začasna rezervacija ne zavzame zmogljivosti vira, lahko ta vir v istem obdobju veljavno rezervirate za druge naloge. Splošnih virov ni mogoče začasno rezervirati, prav tako začasna rezervacija ne more izpolniti zahteve za splošni vir.

Začasno rezervirani člani projektne ekipe so navedeni na zavihku **Ekipa** na strani **Projekt**, pri čemer so začasno rezervirane ure prikazane v stolpcu **Začasno rezervirane ure**, v pogledu **Imenovani člani ekipe**. Začasno rezervirani člani ekipe so navedeni tudi na plošči razporeda. Ker so člani začasno rezervirani, za te vire na plošči razporeda ni prikazana zmanjšana zmogljivost. Začasno rezervirani čas ni prikazan na zavihku **Uskladitev**, niti v polju **Podaljšajte rezervacije** na zavihku **Uskladitev** na plošči razporeda. 

Člana ekipe za projekt lahko začasno rezervirate na dva načina: neposredno na plošči razporeda ali z dodajanjem člana ekipe na zavihku **Ekipa**. 

## <a name="soft-book-from-the-schedule-board"></a>Začasna rezervacija na plošči razporeda
Za začasno rezervacijo vira na plošči razporeda dokončajte spodnje korake. 

1. Odprite ploščo razporeda in nato na plošči **Zahteve za rezervacije** izberite zavihek **Projekt**.
2. Poiščite projekt, za katerega želite začasno rezervirati vir. Če je na seznamu večje število projektov, izberite glavo stolpca **Projekt** in nato uporabite filter za iskanje enega ali več projektov.
3. Izberite projekt ter ga nato povlecite in spustite v časovno mrežo vira.
5. Na plošči **Ustvarjanje rezervacije vira** prilagodite začetni in končni datum, nastavite **Stanje rezervacije** na **Začasno** in nato nastavite še ure. 
6. Kliknite **Rezerviraj**. Vir je zdaj prikazan na zavihku **Ekipa** kot vir za projekt. V pogledu **Poimenovani član ekipe** so začasno rezervirane ure prikazane v stolpcu **Začasno rezervirane ure**.

> [!NOTE]
> Začasno rezervirani vir lahko zdaj dodelite na zavihku **Načrtovanje**. Na zavihku **Uskladitev** je pri viru prikazan primanjkljaj rezervacij glede na dodelitev opravil, ker so na zavihku **Uskladitev** prikazane samo veljavne rezervacije. Funkcijo **Podaljšajte rezervacije** lahko uporabite za veljavno rezervacijo vira, da odpravite primanjkljaj veljavnih rezervacij glede na dodelitve vira. Začasno rezervacijo za vir boste morali preklicati ročno prek možnosti **Upravljaj rezervacije**.

## <a name="soft-book-on-the-team-tab"></a>Začasne rezervacije na zavihku Ekipa

Člane ekipe lahko dodate neposredno na zavihku **Ekipa** in nato v možnosti **Upravljaj rezervacije** spremenite stanje rezervacije z **Veljavna** na **Začasna**. Če člana ekipe dodate na ta način, bo vedno uporabljena veljavna rezervacija, razen če za način dodeljevanja izberete **Brez**.

Če želite uporabiti ta način, dokončajte spodnje korake.

1. Na strani **Projekt** na zavihku **Ekipa** kliknite **Novo**.
2. Izberite vir, ki ga je mogoče rezervirati, vlogo in datumski obseg.
3. Izberite način dodelitve, ki ni **Brez**.
4. Izberite **Shrani**. Vir bo prikazan v mreži, ure pa v stolpcu **Veljavno rezervirane ure**.
5. Rezervacije vira upravljate v možnosti **Upravljanje rezervacij**.
6. Ko se odpre plošča razporeda, razširite vir, da prikažete rezervacije. Rezervacija bo prikazana kot **Veljavna**.
7. Z desno tipko miške kliknite rezervacijo in pod možnostjo **Spremeni stanje** izberite **Začasna rezervacija** \> **Začasna**. Stanje rezervacije je zdaj **Začasna**.
8. Ko zaprete ploščo razporeda, boste videli, da so se v pogledu **Poimenovani člani ekipe** na zavihku **Ekipa** ure za vir premaknile iz stolpca **Veljavno rezervirane ure** v **Začasno rezervirane ure**.

> [!NOTE]
> Če v ekipi veljavno rezervirate vir in temu viru dodelite opravila, nato pa uporabite **Upravljanje rezervacij**, da spremenite stanje iz **Veljavno** v **Začasno**, se dodelitve opravil za vir ohranijo. Vseeno pa bo na zavihku **Uskladitev** pri tem viru prikazan primanjkljaj rezervacij, ker so za uskladitev upoštevane samo veljavne rezervacije, ne pa tudi dodelitve. Uporabite lahko tudi funkcijo **Podaljšaj rezervacije** na zavihku **Uskladitev** in tako veljavno rezervirate vir, pri čemer se odpravi primanjkljaj veljavnih rezervacij glede na dodelitve. V možnosti **Upravljaj rezervacije** morate preklicati začasno rezervacijo za vir.

Ko ste pripravljeni na spremembo začasne rezervacije člana ekipe v veljavno rezervacijo, naredite naslednje:

1. Na plošči razporeda razširite vir, da prikažete rezervacije. Rezervacija bo prikazana kot **Začasna**.
2. Z desno tipko miške kliknite rezervacijo in pod možnostjo **Sprememba stanja** izberite **Veljavna rezervacija** \> **Veljavna**. Stanje rezervacije je zdaj **Veljavna**.
3. Ko zaprete ploščo razporeda, se vrnete na projekt ter odprete zavihek **Ekipa**, vidite, da so ure za vir v pogledu **Poimenovani člani ekipe** na zavihku **Ekipa** premaknjene iz stolpca **Začasno rezervirane ure** v stolpec **Veljavno rezervirane ure**. Če je bil vir dodeljen opravilu, na zavihku **Uskladitev** primanjkljaj rezervacij ni več prikazan, saj je rezervacija zdaj veljavna.



[!INCLUDE[footer-include](../includes/footer-banner.md)]