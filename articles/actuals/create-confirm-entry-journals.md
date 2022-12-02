---
title: Ustvarjanje in potrjevanje dnevnikov vnosov
description: Ta članek vsebuje informacije o tem, kako ustvariti in potrditi dnevnike vnosov v programu Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912352"
---
# <a name="create-and-confirm-entry-journals"></a>Ustvarjanje in potrjevanje dnevnikov vnosov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dnevnike vnosov lahko uporabljate za beleženje dejanskih vrednosti neposredno v programu Microsoft Dynamics 365 Project Operations. Ko uporabljate dnevnike vnosov, vam ni treba vnesti dnevnikov časa, stroškov in porabe materiala v aplikacijo Project Operations.

En dnevnik vnosa vam omogoča ustvarjanje več vrstic dnevnika. Ko je dnevnik potrjen, vrstica dnevnika vnosa zabeleži dejanske vrednosti za naslednje podrobnosti:

- Strošek ali prihodek, odvisno od vrste transakcije, ki je bila izbrana.
- Izbrani razred transakcije. Razpoložljivi razredi so **Čas**, **Stroški**, **Material**, **Honorar**, **Mejnik** in **Davek**.
- Projekt in/ali opravilo, ki je izbrano v vrstici dnevnika.

Sledite tem korakom, da ustvarite dnevnik vnosov v aplikaciji Project Operations.

1. Odprite **Prodaja** \> **Transakcije** \> **Dnevniki**.
2. Na strani s seznamom **Dnevniki vnosov** v podoknu za dejanja izberite **Novo**, da ustvarite dnevnik.
3. Na strani **Novi dnevnik** v polju **Opis** vnesite opis dnevnika.
4. Prepričajte se, da je polje **Vrsta dnevnika** nastavljeno na **Vnos** in nato izberite **Shrani**. Ko je shranjen nov dnevnik vnosa, se bi moral na strani dnevnika pojaviti zavihek **Vrstice dnevnika**.
5. V zavihku **Vrstice dnevnika** v orodni vrstici nad mrežo izberite **Novo** za ustvarjanje vrstice dnevnika vnosov.
6. V pogovornem oknu **Hitro ustvarjanje** za ustvarjanje vrstice dnevnika vnosov, nastavite polja, kot je opisano v naslednji tabeli.

    | Polje | Description | Funkcionalni vpliv |
    | --- | --- | --- |
    | Razred transakcije | Vrstico dnevnika je mogoče razvrstiti v enega od šestih razredov transakcij: **Čas**, **Stroški**, **Material**, **Honorar**, **Mejnik** ali **Davek**. | Razred transakcije **Davek** je bil v aplikaciji Project Operations opuščen. <br> Če ustvarite razred transakcije **Davek**, ne bo obdelan z izdajanjem računov ali v izračunih stroškov ali prihodkov. **Mejnik** je razred transakcije, ki omogoča le zapis prihodkov. <br>**Honorar** je razred transakcije, ki predstavlja predujem, prejet od stranke. Vedno ga je treba ustvariti kot par vrstic dnevnika obračunane prodaje in neobračunane prodaje. |
    | Vrsta transakcije | Vrste transakcij **Stroški**, **Prodaja znotraj organizacije** in **Cena enote vira** je treba uporabiti za beleženje cene.<br> Vrste transakcij **Neobračunana prodaja** in **Obračunana prodaja** je treba uporabiti za beleženje prihodkov. | Razred transakcije **Honorar** deluje samo z vrstama transakcij **Neobračunana prodaja** in **Obračunana prodaja**.<br> Razred transakcije **Mejnik** deluje samo z vrsto transakcije **Obračunana prodaja**. <br>Vrsti transakcij **Prodaja znotraj organizacije** in **Cena enote vira** se uporabljata samo za razred transakcije **Čas** in sta na voljo samo v dnevnikih vnosov v scenariju uvajanja Lite in ne pri uvajanju aplikacije Project Operations v scenarijih z viri/brez zalog. |
    | Izberite Izdelek | Če je izbran razred transakcije **Material**, vam to polje omogoča, da določite, ali je materialna transakcija, za katero ustvarjate vrstico dnevnika, obstoječi izdelek ali izdelek, ki ni v katalogu. | Če izberite možnost **Izdelek, ki ni v katalogu**, lahko vnesite ime izdelka. |
    | izdelek, | Sklic na izdelek iz kataloga. | |
    | Description | Opis vrstice dnevnika za lažje prepoznavanje. | Za neobračunane vrstice dnevnika prodaje bo vrednost uporabljena kot opis, ko bodo ustvarjene podrobnosti vrstice računa. |
    | Zunanji opis | Opis vrstice dnevnika, ki se lahko uporablja za skupno rabo z zunanjimi zainteresiranimi skupinami. | Za neobračunane vrstice dnevnika prodaje bo vrednost uporabljena kot zunanji opis, ko bodo ustvarjene podrobnosti vrstice računa. Lahko se pojavi tudi na računu, ki je poslan stranki. |
    | Vrsta obračunavanja | Vrednost, ki označuje, ali se bo vrstica dnevnika štela kot zaračunljiva, brezplačna ali nezaračunljiva komponenta v projektu. | V običajnem toku je vrsta obračunavanja izpeljana iz dogovorjenih pogojev, ki so določeni v pogodbi. Ko beležite vrstico dnevnika, lahko v to polje vnesete vrednost. |
    | Datum dokumenta | Uporabite datum, ko je prišlo do transakcije. | |
    | Datum začetka | Uporabite datum, ko je prišlo do transakcije. | To polje se uporablja za primerjavo z datumom izdelave računa za transakcije vrste **Neobračunana prodaja**. Ta primerjava vam bo pomagala pri odločitvi, ali ima transakcija prihodnji ali pretekli datum. Na račun bodo dodane samo pretekle transakcije. |
    | Datum konca | Uporabite datum, ko je prišlo do transakcije. | |
    | Datum knjiženja | Uporabite datum, ko bo zabeležen računovodski vpliv. | |
    | Stranka podrobnosti pogodbe | Če ima podrobnost pogodbe samo eno stranko, je to polje privzeto nastavljeno na stranko v podrobnosti pogodbe, ko je vrstica dnevnika shranjena. Če ima podrobnost pogodbe več strank, izberite pravo stranko v podrobnosti pogodbe. | Če sistem ne more določiti stranke podrobnosti pogodbe v vrstici dnevnika in če je polje pod dejansko vrednostjo vrste **Neobračunana prodaja**, ki je ustvarjena iz vrstice dnevnika, prazno, dejanska vrednost ne bo zaračunana. |
    | Projekt | Izberite projekt za beleženje dejanske vrednosti. | Na podlagi izbranega projekta, razreda transakcije in opravila bo sistem poskušal določiti pogodbo, podrobnost pogodbe in podrobnost pogodbe stranke. |
    | opravilo, | Izberite opravilo za beleženje dejanske vrednosti. | Če ste opravila med nastavitvijo pogodbe povezali s podrobnostmi pogodbe, bo sistem uporabil izbrano opravilo, skupaj s projektom in razredom transakcije, da določi pogodbo, podrobnost pogodbe in podrobnost pogodbe stranke. |
    | Kategorija transakcije | Izberite kategorijo transakcij za beleženje dejanske vrednosti. | Kategorija transakcij, izbrana za stroške, določa privzeto ceno, ki bo vnesena v vrstico dnevnika, ko bo shranjena. |
    | Vloga | To polje je pomembno za vrstice dnevnika »Čas«. Izberite vlogo vira, ki je projektu in/ali opravilu posvetil čas. | Če za vnos privzetih stroškov virov in deležev obračunavanja za vrstice dnevnika »Čas« uporabite vnaprej pripravljeno konfiguracijo, se izbrana vloga uporablja skupaj z enoto virov za določitev privzete cene, ki bo vnesena v vrstico dnevnika, ko bo shranjena. Če za vnos privzetih cen uporabljate konfiguracijo po meri, morate to konfiguracijo pregledati, da ugotovite, ali se polje **Vloga** uporablja za vnos privzetih vrednosti cen. |
    | Podizvajalska pogodba | Če vrstica dnevnika predstavlja podizvajalsko zmogljivost ali podizvajalske stroške ali material, izberite ustrezno podizvajalsko pogodbo. | Ko so vrstice dnevnika »Stroški« zabeležene, bo izbrana podizvajalska pogodba določila cenik, ki se uporablja za vnos privzete cene na enoto. |
    | Podrobnosti podizvajalske pogodbe | Če vrstica dnevnika predstavlja podizvajalsko zmogljivost ali podizvajalske stroške ali material, izberite ustrezno podrobnost podizvajalske pogodbe. | Ko so vrstice dnevnika »Stroški« zabeležene, bo izbrana podrobnost podizvajalske pogodbe zagotovila, da so izračuni razpoložljive zmogljivosti v podrobnosti podizvajalske pogodbe pravilno izračunani. |
    | Način za izračun zneska | To polje je privzeto nastavljeno na **Količino pomnoži s ceno**. Pri uporabi tega načina bo znesek izračunan kot *Količina* × *Cena*. Drug podprti način je **Fiksna cena**. Pri uporabi tega načina bo cena nastavljena na znesek, količina pa v izračunu ne bo uporabljena. | |
    | Razpored enote in enota | Razpored enote in enota skupaj določata enoto količine. | Kombinacija enote in kategorije transakcij se uporablja za vnos privzetih cen za stroške. V privzeti konfiguraciji aplikacije Project Operations se kombinacija enote, vloge in enote vira uporablja za vnos privzetih cen za čas. Če imate za vnos privzetih cen konfiguracijo po meri, bo ta uporabljena skupaj z enoto. Kombinacija izdelka in enote se uporablja za vnos privzetih cen za material. |
    | Količina | Vnesite količino. | |
    | Cena | Če je cena ob ustvarjanju vrstice dnevnika prazna, bodo ustrezne vrednosti uporabljene za vnos privzetih cen, odvisno od razreda transakcije. Če je cena vnesena, ko je ustvarjena vrstica dnevnika, bo uporabljena ta cena. | |
    | Davek | Vnesite poljuben znesek davka. | Odvisno od vnesenega zneska davka se skupna vrednost postavk na računu izračuna kot *Znesek* + *Davek*. |

## <a name="confirm-an-entry-journal"></a>Potrditev dnevnika vnosov

Ko vnesete vse vrstice dnevnika v dnevnik vnosov, lahko dnevnik potrdite. Ta postopek bo zabeležil vsako vrstico dnevnika kot dejansko stanje v ustreznih projektih.

Ko je dnevnik potrjen, ne morete več urejati dnevnika ali njegovih vrstic.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Dejanske vrednosti, ustvarjene s potrditvijo dnevnika vnosov

Obstaja nekaj ključnih razlik med dejanskimi vrednostmi, ki so ustvarjene s potrditvijo dnevnika vnosov, in dejanskimi vrednostmi, ki so ustvarjene med odobritvijo dnevnikov porabe časa, stroškov in materiala ter potrditvijo računa v aplikaciji Project Operations:

- Dnevniki vnosov ne uporabljajo povezav transakcij za povezavo dejanskih stroškov z neobračunano dejansko prodajo. Dejanske vrednosti, ki so ustvarjene, ko so odobreni dnevniki porabe časa, stroškov in materiala, vedno uporabljajo povezave transakcij za povezovanje stroškov in neobračunane dejanske prodaje.
- Dnevniki vnosov ne uporabljajo izvorov transakcij za povezavo dejanskih stroškov in neobračunane dejanske prodaje s katerimkoli izvornim zapisom. Dejanske vrednosti, ki so ustvarjene, ko so odobreni dnevniki porabe časa, stroškov in materiala, vedno uporabljajo izvore transakcij za povezovanje stroškov in neobračunane dejanske prodaje z izvornim časovnim vnosom.
- Ko se zaračunajo neobračunane dejanske vrednosti prodaje, ustvarjene s potrditvijo dnevnika vnosov, so obračunane dejanske vrednosti prodaje, ki so ustvarjene med potrditvijo računa, povezane z neobračunanimi dejanskimi vrednostmi prodaje, na podoben način kot neobračunane dejanske vrednosti prodaje, ki so ustvarjene, ko so odobreni dnevniki porabe časa, stroškov in materiala.
- Vrstice dnevnika vnosov, ustvarjene za čas, ki ga vnesejo medorganizacijski viri, ne povzročijo, da se dejanske vrednosti vrst **Cena enote vira** in **Prodaja znotraj organizacije** ustvarijo samodejno. Te dejanske vrednosti morate ustvariti ročno. To vedenje se razlikuje od vedenja za časovne vnose, ki jih zabeležijo medorganizacijski viri. V tem primeru, ko je čas odobren, aplikacija samodejno ustvari dejanske vrednosti vrste **Stroški** za projekt in dejanske vrednosti vrst **Cena enote vira** in **Prodaja znotraj organizacije** za lastniški oddelek zaposlenega. Nato uporabi povezave transakcij, da te dejanske vrednosti poveže skupaj, in izvore transakcij, da jih poveže z izvornim časovnim vnosom.
- Ko so dnevniki vnosov potrjeni, ustvarijo dejanske vrednosti. Vendar dnevnikov popravkov ni mogoče uporabiti za popravljanje teh dejanskih vrednosti. To vedenje se razlikuje od vedenja dejanskih vrednosti, ki so ustvarjene, ko so odobreni dnevniki porabe časa, stroškov in materiala. V tem primeru vam aplikacija omogoča uporabo dnevnikov popravkov za popravljanje dejanskih vrednosti za odpravo morebitnih napak, pod pogojem, da te dejanske vrednosti še niso bile zaračunane. Če so že bile zaračunane, lahko še vedno popravite dejansko vrednost, če stranki izdate račun za celotno dobroimetje te dejanske vrednosti.

> [!NOTE]
> Dnevniki vnosov ne uveljavljajo strogih pravil o privzetem nastavljanju. Zato te dnevnike vnosov uporabljajte čim manj ter bodite previdni in pazljivi, da zagotovite, da v svojem sistemu ne ustvarite poškodovanih finančnih podatkov. Če je mogoče, za ustvarjanje dejanskih vrednosti uporabite dnevnike časa, stroškov in porabe materiala, nastavitev mejnika in honorarja v projektnih pogodbah ter postopek potrditve računov za projekt namesto dnevnikov vnosov.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
