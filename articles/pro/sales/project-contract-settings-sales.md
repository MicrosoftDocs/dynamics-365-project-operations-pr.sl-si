---
title: Polja in podatki o projektni pogodbi
description: Ta tema vsebuje informacije o poljih, ki vplivajo na podrobnosti pogodbe, in informacije o pogodbi, ki so povzete v vrstičnih postavkah.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 082292c54682022933a4b46b856f9241078a9067
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088107"
---
# <a name="project-contract-fields-and-information"></a>Polja in podatki o projektni pogodbi 

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta tema vsebuje informacije o poljih, ki veljajo za celotno projektno pogodbo, vključno z nastavitvami, ki vplivajo na vse podrobnosti pogodbe. Vključene so tudi informacije o pogodbi, ki so povzete po vrstičnih postavkah za vodenje KPI-jev projektne pogodbe.

V spodnji tabeli so navedena polja v projektni pogodbi, ki so na voljo le v storitvi Dynamics 365 Project Operations ali pa imajo nekatere pomembne spremembe v delovanju prodajnih naročil v storitvi Dynamics 365 Sales.

| Polje | LOkacija | Ustreznost, namen in smernice | Nadaljnji vpliv |
| --- | --- | --- | --- |
| Vnesi | Zavihek **Povzetek** (skrito) | To je polje z naborom možnosti in naslednjimi možnostmi:</br>- **temelji na delu** (na voljo samo, če je nameščena storitev Project Operations)</br>- **temelji na elementu** (na voljo samo, če sta nameščeni storitvi Project Operations in Sales)</br>- **temelji na vzdrževanju storitev** (na voljo, ko je nameščena storitev Dynamics 365 Field Service) | V storitvi Project Operations je privzeta vrednost tega polja **Temelji na delu** in razvršča pogodbo kot pogodbo, ki temelji na projektu. Pogodba mora temeljiti na projektu, da lahko omogoča vse razširitve in funkcije, specifične za projekt. |
| Možna stranka | Zavihek **Povzetek** | Sklic na zapis strankinega podjetja ali kupca. V pogodbi, ustvarjeni iz ponudbe, se ta vrednost kopira iz ustreznega polja pri zapisu ponudbe. | Valuta na projektni pogodbi je privzeto nastavljena glede na valuto stranke. To je mogoče spremeniti, preden shranite pogodbo. |
| Vodja za upravljanje kupcev | Zavihek **Povzetek** | Ime upravitelja kupcev za ta posel. V pogodbi, ustvarjeni iz ponudbe, se ta vrednost kopira iz ustreznega polja pri zapisu ponudbe. | Upravitelj kupcev je odgovoren za upravljanje odnosa s stranko do zaključka tega projekta. Na podlagi zapisa vira, ki ga je mogoče rezervirati in je povezan z upraviteljem kupcev, je privzeto nastavljena pogodbena enota na projektni pogodbi. |
| Pogodbena enota | Zavihek **Povzetek** | Organizacijska enota, ki je odgovorna za izvedbo projektov, povezanih s to pogodbo. V pogodbi, ustvarjeni iz ponudbe, se ta vrednost kopira iz ustreznega polja pri zapisu ponudbe. | Pogodbena enota je oddelek podjetja, ki izvaja projekte. Vsaka pogodbena enota ima valuto in ta valuta se uporablja za poročanje o ocenjenih in dejanskih stroških, nastalih med projektom. |
| Cenik izdelkov | Zavihek **Povzetek** | Ta cenik se uporablja za privzeto nastavitev cen v podrobnostih pogodbe, ki temeljijo na izdelkih. Seznam spustnih možnosti za to polje prikazuje seznam cenikov, kjer se valuta cenika ujema z valuto na pogodbi. V pogodbi, ustvarjeni iz ponudbe, se ta vrednost kopira iz ustreznega polja pri zapisu ponudbe. V projektni pogodbi je to polje privzeto nastavljeno iz zapisa kupca, vendar ga je mogoče spremeniti. | Za to polje ni odvisnih ustreznosti. |
| Valuta | Zavihek **Povzetek** | Valuta, uporabljena za poročanje o vrednosti tega posla, in valuta, v kateri bo stranki izdan račun. V pogodbi, ustvarjeni iz ponudbe, se ta vrednost kopira iz ustreznega polja pri zapisu ponudbe. V projektni pogodbi je to polje privzeto nastavljeno iz zapisa kupca, vendar ga je mogoče spremeniti. | Ko je pogodba shranjena, tega polja ni več mogoče urejati. To polje se uporablja za privzeto nastavitev cenikov izdelkov in projektov na pogodbi. Valuta na pogodbi se uporablja za ujemanje valute na ceniku. |
| Omejitev »Ni dovoljeno preseči« | Zavihek **Povzetek** | To polje pomeni dogovorjeno zgornjo mejo končne vrednosti, s katero se stranka strinja za ta posel. | Zgornja meja se oceni med izvajanjem ter velja za vse vrstične postavke in projekte, povezane s tem poslom. |
| Zahtevani datum dostave | Zavihek **Povzetek** | V pogodbi, ustvarjeni iz projektne ponudbe, se ta vrednost kopira iz ustreznega polja pri projektni ponudbi. | Ta datum se uporablja kot končni datum za ustvarjanje razporedov za izdajanje računov. |

Naslednji KPI-ji so na voljo na zavihku **Izvedba pogodbe** projektne pogodbe.

| Polje | LOkacija | Ustreznost, namen in smernice |
| --- | --- | --- |
| Vrednost pogodbe | Splošna pogodba | Skupna vrednost projektne pogodbe. |
| Obračunani znesek | Splošna pogodba | Vsota zneskov na vseh računih za to pogodbo. |
| Nastali stroški | Splošna pogodba | Vsota vseh dejanskih stroškov, zabeleženih za vse projekte, ki so preslikani v pogodbo. |
| Stopnja bruto dobička | Splošna pogodba | Obračunani znesek – strošek, nastal do datuma/obračunani znesek |
| Pričakovana marža | Splošna pogodba | (vrednost naročila – ocenjeni stroški)/vrednost pogodbe; ocenjeni stroški = vsota vseh ocenjenih stroškov za vse projekte, preslikane v pogodbo.|
| Vrednost pogodbe | Podrobnosti, ki temeljijo na projektih | Vrednost podrobnosti pogodbe. |
| Obračunani znesek | Podrobnosti, ki temeljijo na projektih | Za podrobnosti pogodbe s fiksno ceno: vsota vseh dejansko obračunanih prodajnih mejnikov glede na to podrobnost pogodbe na različnih računih, ustvarjenih za to pogodbo. Za podrobnosti pogodbe glede časa in materialov: vsota vseh dejansko obračunanih prodajnih mejnikov od tistih, ki se lahko obračunajo, glede na to podrobnost pogodbe na različnih računih, ustvarjenih za to pogodbo. |
| Nastali stroški | Podrobnosti, ki temeljijo na projektih | Vsota vseh dejanskih stroškov, zabeleženih za vse projekte, ki so preslikani v podrobnost pogodbe. |
| Stopnja bruto dobička | Podrobnosti, ki temeljijo na projektih | (obračunani znesek – strošek, nastal do datuma)/obračunani znesek |
| Pričakovana marža | Podrobnosti, ki temeljijo na projektih | (znesek podrobnosti pogodbe v osnovni valuti – ocenjeni stroški podrobnosti pogodbe v osnovni valuti)/znesek podrobnosti pogodbe v osnovni valuti |
| Nastali stroški | Podrobnost vrstice, ki temelji na projektu | Čas: vsota dejanskih vrednosti »čas – cena«, zabeleženih za to vlogo pri projektu, preslikanem v podrobnost pogodbe. Stroški: vsota dejanskih vrednosti »strošek – cena«, zabeleženih za to kategorijo pri projektu, preslikanem v podrobnost pogodbe. |
| Zabeležena količina | Podrobnost vrstice, ki temelji na projektu | Čas: skupna količina dejanskih vrednosti »čas – cena« za vlogo pri projektu, preslikanem v to podrobnost pogodbe. Stroški: skupna količina za to kategorijo stroškov pri dejanskih vrednostih »strošek – cena« pri projektu je preslikana v to podrobnost pogodbe. |
| Obračunani znesek | Podrobnost vrstice, ki temelji na projektu | Za podrobnost pogodbe s fiksno ceno je to polje prazno na ravni podrobnosti in je prikazano samo na ravni podrobnosti pogodbe. Za podrobnosti pogodbe glede časa in materialov se izračuni zaključijo na ravni podrobnosti. Podrobnosti prikazujejo vsoto zneska pri vseh obračunanih podrobnostih prihodkov v primerjavi s to podrobnostjo pogodbe, ki se zaračunavajo. |
| Obračunana količina | Podrobnost vrstice, ki temelji na projektu | Za podrobnost pogodbe s fiksno ceno je to polje prazno na ravni podrobnosti in je prikazano samo na ravni podrobnosti pogodbe. Za podrobnosti pogodbe glede časa in materialov se izračuni zaključijo na ravni podrobnosti za čas in stroške. Čas: vsota ur pri vseh obračunanih podrobnostih prihodkov za to vlogo v primerjavi s to podrobnostjo pogodbe, ki se zaračunavajo. Stroški: skupna količina za to kategorijo stroškov pri dejanskih vrednostih »strošek – cena« pri projektu je preslikana v to podrobnost pogodbe. |
| Vrednost pogodbe | Podrobnosti, ki temeljijo na izdelkih | Vrednost podrobnosti pogodbe za to podrobnost pogodbe, ki temelji na izdelku. |
| Obračunani znesek | Podrobnosti, ki temeljijo na izdelkih | Vsota zneskov pri vseh podrobnostih računov na podlagi te podrobnosti pogodbe, ki temelji na izdelku, na različnih računih, ustvarjenih za to pogodbo. |
| Nastali stroški | Podrobnosti, ki temeljijo na izdelkih | Vsota vseh dejanskih stroškov, zabeleženih za podrobnost pogodbe, ki temelji na izdelku. |
| Stopnja bruto dobička | Podrobnosti, ki temeljijo na projektih | Obračunani znesek – strošek, nastal do datuma/obračunani znesek |
| Pričakovana marža | Podrobnosti, ki temeljijo na izdelkih | (vrednost podrobnosti pogodbe – ocenjeni stroški za podrobnost pogodbe)/vrednost podrobnosti pogodbe |