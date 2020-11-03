---
title: Ceniki za projekte
description: Ta tema vsebuje informacije o entiteti cenika projekta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1a69cf51ca8cde8260f4136cf1b2e936f99b112a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084982"
---
# <a name="project-price-lists"></a>Ceniki za projekte

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Storitev Dynamics 365 Project Operations razširja entiteto cenika v storitvi Dynamics 365 Sales. 

## <a name="key-entities"></a>Ključne entitete

Cenik vsebuje informacije, ki jih določajo štiri različne entitete:

- **Cenik** : ta entiteta shranjuje informacije o kontekstu, valuti, datumski veljavnosti in časovni enoti za čas določanja cen. Kontekst pokaže, ali cenik določa stroškovne ali prodajne zneske. 
- **Valuta** : v tej entiteti je shranjena valuta cen, navedenih na ceniku. 
- **Datum** : ta entiteta se uporablja, ko sistem poskuša vnesti privzeto ceno za transakcijo. Izbran je cenik, katerega datumska veljavnost vključuje datum transakcije. Če je najden več kot en cenik, ki je veljaven za datum transakcije in priložen povezani ponudbi, pogodbi ali organizacijski enoti, se cena privzeto ne določi. 
- **Čas** : v tej entiteti je shranjena časovno enoto, za katero so izražene cene, na primer dnevne ali urne postavke. 

Entiteta »Cenik« ima tri sorodne tabele, v katerih so shranjene cene:

  - **Cena vloge** : v tej tabeli so shranjene vrednosti za kombinacijo vloge in organizacijske enote, uporablja pa se za nastavitev na podlagi vlog za človeške vire.
  - **Cena kategorije transakcije** : v tej tabeli so shranjene cene glede na kategorijo transakcij, uporablja pa se za določanje cen kategorij stroškov.
  - **Elementi cenika** : v tej tabeli so shranjene cene kataloških izdelkov.
 
Cenik je kartica s cenami. Kartica s cenami je kombinacija entitete »Cenik« in povezanih vrstic v tabelah »Cena vloge«, »Cena kategorije transakcije« in »Elementi cenika«.

## <a name="resource-roles"></a>Vloge virov

Izraz *vloga vira* se nanaša na nabor znanja, sposobnosti in potrdil, ki jih mora imeti oseba, da lahko izvaja določeno skupino opravil v okviru projekta.

Čas človeških virov je v ponudbi naveden na podlagi vloge, ki jo vir izpolni pri določenem projektu. Za čas človeških virov izračun stroškov in zneskov za obračunavanje temelji na vlogi vira. Ceno za čas je mogoče določiti v kateri koli enoti v skupini enot **Čas**.

Skupina enot **Čas** je ustvarjena, ko namestite storitev Project Operations. Privzeto ima nastavljeno enoto **Ura**. Atributov skupine enot **Čas** enote **Ura** ni mogoče izbrisati, preimenovati ali urejati. Vendar pa lahko v skupino enot **Čas** dodate druge enote. Če poskušate izbrisati skupino enot **Čas** ali **Ura** , lahko povzročite napake v poslovni logiki.
 
## <a name="transaction-categories-and-expense-categories"></a>Kategorije transakcij in kategorije stroškov

Potni in drugi stroški, ki nastanejo pri delu projektnih svetovalcev, so zaračunani stranki. Določanje cen kategorij stroškov se izvede z uporabo cenikov. Primeri kategorij stroškov so letalske karte, nočitve v hotelih in najem vozila. Vsaka vrstica cenika za stroške določa ceno za določeno kategorijo stroškov. Za določanje cen kategorij stroškov se uporabljajo naslednji trije načini:

- **Nabavna cena** : cena stroška, ki se zaračuna stranki brez pribitka,
- **Odstotek pribitka** : odstotek dejanske cene, ki se prišteje nabavni ceni in zaračuna stranki. 
- **Cena na enoto** : cena za obračunavanje, ki je nastavljena za vsako enoto v kategoriji stroškov. Znesek, ki je zaračunan stranki, se izračuna na podlagi števila stroškovnih enot stroškov, ki ga vnese svetovalec. Za izračun kilometrine se uporablja metoda cene na enoto. Primer: kategorija stroška kilometrine je lahko nastavljena na 30 ameriških dolarjev (USD) na dan ali 2 USD na miljo. Ko svetovalec vnese kilometrino za projekt, se znesek za obračun izračuna na podlagi števila milj, ki jih svetovalec vnese.
 
## <a name="project-sales-pricing-and-overrides"></a>Prodajne cene za projekt in preglasitve

Za projektne ponudbe in pogodbe ima cenik projekta drugačen vzorec preglasitve cen kot cenik izdelkov. V vrstici ponudbe, ki temelji na katalogu izdelkov, lahko preglasite ceno za vloge in kategorije neposredno v vrstici ponudbe, saj vsaka vrstica ponudbe predstavlja natanko en kataloški izdelek. V vrstici ponudbe, ki temelji na projektu, pa ni mogoče preglasiti cene za vloge in kategorije neposredno v vrstici ponudbe. S cenikom projekta podprite dva različna vzorca preglasitve.

> [!NOTE]
> Priporočamo, da zaradi razlik v delovanju obeh pri preglasitvi cen uporabljate ločen cenik za svoje projektne vire in za katalog izdelkov.

Vsaka od naslednjih entitet ima lahko enega ali več povezanih prodajnih cenikov za cene v okviru projekta:

- Stranka (račun) 
- Priložnost 
- Ponudba 
- Projektna pogodba

Povezovanje teh entitet s cenikom določajo ceniki projektov. S prodajnimi entitetami »Stranka«, »Priložnost«, »Ponudba«, »Projektna pogodba« lahko povežete enega ali več cenikov.

Privzeti cenik projekta ni samodejno vnesen v zapisu stranke. Vendar pa lahko cenik projekta zapisu stranke ročno priložite. Kljub temu cenik projekta ročno priložite samo, če imate s stranko dogovorjene posebne cene. 

Ko je prodajni entiteti priloži cenik projekta, se preverijo naslednje informacije:

- Kontekst cenika je **Prodaja**. 
- Valuta cenika se ujema z valuto stranke. 

V projektni pogodbi se za samodejno nastavitev povezanih cenikov projekta uporablja naslednji vrstni red:

1. Citat
2. Priložnost
3. Stranki 
4. Globalne nastavitve 

Ko je cenik projekta privzeto vnesen, sistem preveri, ali se valuta ujema z valuto stranke in ali so privzeti ceniki bili vneseni s kontekstom **Prodaja**.

Z entitetami »Stranka«, »Priložnost«, »Ponudba«, »Projektna pogodba« lahko povežete več cenikov projekta. Ta zmožnost podpira datumsko določene privzete cene za dolgoročne projektne pogodbe, kjer boste morda potrebovali več kot en cenik, da se upošteva posodobitev cen, do katere pride zaradi inflacije. Če pa imajo ceniki, ki jih povežete z entiteto »Stranka«, »Priložnost«, »Ponudba«, »Projektna pogodba«, prekrivajočo datumsko veljavnost, so lahko privzete cene napačne. Zato se prepričajte, da ceniki projektov, ki imajo prekrivajočo datumsko veljavnost, niso povezani s temi entitetami.

### <a name="deal-specific-price-overrides"></a>Preglasitve cen za posamezne projekte

Ustvarite lahko projektne preglasitve za izbrane cenike projekta, ki se privzeto vnesejo za ponudbo ali projektno pogodbo.

Projektna pogodba privzeto dobi kopijo glavnega prodajnega cenika namesto neposredne povezave z njim. Tako se zagotovi, da se dogovori o cenah, sklenjeni s strankami za izjave o delu, ne spremenijo, ko pride do sprememb glavnega cenika.

V ponudbi pa lahko uporabite glavni cenik. Lahko pa tudi kopirate glavni cenik in ga uredite, da ustvarite cenik po meri, ki velja samo za to določeno ponudbo. Če želite ustvariti nov cenik, ki je specifičen za ponudbo, na strani **Ponudba** izberite možnost **Ustvarjanje cen po meri**. Do cenika projekta, ki je posebej določen za projekt, lahko dostopate samo iz ponudbe. 

Ko ustvarite cenik projekta po meri, se kopirajo samo projektne komponente cenika. Povedano drugače, nov cenik je ustvarjen kot kopija obstoječega cenika projekta, ki je priložen ponudbi, in ta novi cenik vsebuje le povezane cene vlog in cene kategorij transakcij.
  
## <a name="tracking-costs"></a>Sledenje stroškom

Project Operations sledi stroškom porabe časa človeških virov na projektih. Sledi tudi drugim stroškom, ki so nastali med projektom, npr. potnim stroškom.

Tako kot zneski za obračunavanje se tudi stroški za človeške vire izračunajo z uporabo cenikov. Tukaj so glavne razlike v delovanju cenika z lastnimi cenami in prodajnega cenika:

- Mere stroškov določenega vira ni mogoče preglasiti za posamezen projekt, pogodbo ali ponudbo. Vendar pa se stroške za obračunavanje preglasi za posamezne projekte, če je so bile narejene spremembe zaradi narave projekta. 

- Za razrešitev cenika z lastnimi cenami se uporabi ta vrstni red:

    1. Cenik z lastnimi cenami, ki je priložen organizacijski enoti
    2. Cenik z lastnimi cenami, ki je priložen parametrom aplikacije Project Operations. Ker so lahko parametrom priloženi ceniki z lastnimi cenami v različnih valutah, se izvede uskladitev valut med valuto pogodbene organizacijske enote projekta, pogodbo ali ponudbe in valuto cenika z lastnimi cenami.
    3. Pri stroških se metodi nabavne cene in pribitka na ceno ne uporabljata za cenike z lastnimi cenami. Če se ti metodi določanja cen uporabljata v vrsticah cenika z lastnimi cenami za nastavitev stroškovnih kategorij transakcij, jih sistem prezre in ne vnese nobene privzete lastne cene.
