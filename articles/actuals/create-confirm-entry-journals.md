---
title: Ustvarite in potrdite dnevnike vnosov
description: Ta tema vsebuje informacije o tem, kako ustvariti in potrditi dnevnike vnosov v Microsoftu Dynamics 365 Project Operations.
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
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584248"
---
# <a name="create-and-confirm-entry-journals"></a>Ustvarite in potrdite dnevnike vnosov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dnevnike vnosov uporabljate za beleženje dejanskega stanja neposredno v Microsoftu Dynamics 365 Project Operations. Ko uporabljate dnevnike vnosov, vam ni treba vnesti dnevnikov časa, stroškov in porabe materiala v Project Operations.

En dnevnik vnosa vam omogoča ustvarjanje več vrstic dnevnika. Ko je dnevnik potrjen, se v vrstico dnevnika vnosa zabeleži dejanski podatki za naslednje podrobnosti:

- Stroški ali prihodki, odvisno od izbrane vrste transakcije.
- Izbrani razred transakcije. Razpoložljivi razredi so **Čas**, **·**, **·**, **·**, **·**, in **davek**.
- Projekt in/ali naloga, ki je izbrana v vrstici dnevnika.

Sledite tem korakom, da ustvarite dnevnik vnosov v Project Operations.

1. Pojdi do **Prodaja** \> **Transakcije** \> **Časopisi**.
2. Na **Vstopni dnevniki** strani s seznamom, v podoknu za dejanja izberite **Novo** ustvariti dnevnik.
3. Na **Nova revija** strani, v **Opis** vnesite opis revije.
4. Prepričajte se, da **Vrsta dnevnika** polje je nastavljeno na **Vstop** in nato izberite **Shrani**. Ko je novi dnevnik vnosov shranjen, a **Dnevniške vrstice** na strani dnevnika se mora pojaviti zavihek.
5. Na **Dnevniške vrstice** zavihku, v orodni vrstici nad mrežo izberite **Novo** da ustvarite vrstico dnevnika vstopa.
6. V **Hitro ustvarjanje** pogovornem oknu za ustvarjanje vrstice dnevnika vnosa, nastavite polja, kot je opisano v naslednji tabeli.

    | Polje | Description | Funkcionalni vpliv |
    | --- | --- | --- |
    | Razred transakcije | Dnevniško vrstico lahko razvrstimo v enega od šestih razredov transakcij: **Čas**, **·**, **·**, **·**, **·**, oz **davek**. | The **davek** transakcijski razred je bil opuščen v Project Operations. <br> Če ustvarite a **davek** transakcijskega razreda, ne bo obdelan z izdajanjem računov ali v izračunih stroškov ali prihodkov. **Mejnik** je transakcijski razred samo za prihodke. <br>The **Zadrževalnik** transakcijski razred predstavlja predujem, ki je bil prejet od stranke. Vedno ga je treba ustvariti kot par zaračunanih prodajnih in neobračunanih vrstic dnevnika prodaje. |
    | Vrsta transakcije | The **Stroški**, **prodaja**, in **Stroški enote virov** vrste transakcij je treba uporabiti za beleženje stroškov.<br> The **Nezaračunana prodaja** in **Zaračunana prodaja** vrste transakcij je treba uporabiti za beleženje prihodkov. | The **Zadrževalnik** transakcijski razred deluje samo z **Nezaračunana prodaja** in **Zaračunana prodaja** vrste transakcij.<br> The **Mejnik** transakcijski razred deluje samo z **Zaračunana prodaja** vrsta transakcije. <br>The **Interorg prodaja** in **Stroški enote virov** vrste transakcij se uporabljajo samo za **Čas** transakcijski razred in so na voljo samo v dnevnikih vnosov v scenariju razmestitve Lite in ne pri uvajanju projektnih operacij v scenarijih Vir/brez zaloge. |
    | Izberite Izdelek | Ko **Material** Če izberete razred transakcije, to polje vam omogoča, da določite, ali je materialna transakcija, za katero ustvarjate vrstico dnevnika, obstoječi izdelek ali vpisani izdelek. | Če izberete **Vpisani izdelek**, lahko vnesete ime za izdelek. |
    | izdelek, | Sklicevanje na izdelek iz kataloga. | |
    | Description | Opis vrstice dnevnika, ki olajša prepoznavanje. | Za neobračunane vrstice dnevnika prodaje bo vrednost uporabljena kot opis, ko bodo ustvarjene podrobnosti vrstice računa. |
    | Zunanji opis | Opis vrstice dnevnika, ki se lahko uporablja za skupno rabo z zunanjimi zainteresiranimi stranmi. | Za neobračunane vrstice dnevnika prodaje bo vrednost uporabljena kot zunanji opis, ko bodo ustvarjene podrobnosti vrstice računa. Lahko se pojavi tudi na računu, ki je poslan stranki. |
    | Vrsta obračunavanja | Vrednost, ki kaže, ali se bo vrstica dnevnika štela kot plačljiva, brezplačna ali neplačljiva komponenta v projektu. | V tipičnem toku je vrsta obračunavanja izpeljana iz dogovorjenih pogojev, ki so določeni v pogodbi. Ko pa beležite vrstico dnevnika, lahko v to polje vnesete vrednost. |
    | Datum dokumenta | Uporabite datum, ko se je transakcija zgodila. | |
    | Datum začetka | Uporabite datum, ko se je transakcija zgodila. | To polje se uporablja za primerjavo z datumom izdelave računa za transakcije **Nezaračunana prodaja** tip. Ta primerjava vam bo pomagala pri odločitvi, ali je transakcija datumsko ali pretekla. Računu bodo dodane samo pretekle transakcije. |
    | Datum konca | Uporabite datum, ko se je transakcija zgodila. | |
    | Datum knjiženja | Uporabite datum, ko bo zabeležen računovodski vpliv. | |
    | Stranka pogodbene linije | Če ima pogodbena vrstica samo eno stranko, je to polje privzeto nastavljeno na stranko v pogodbeni vrstici, ko je vrstica dnevnika shranjena. Če ima pogodbena vrstica več strank, izberite pravilno stranko na pogodbeni vrstici. | Če sistem ne more določiti stranko pogodbene vrstice v dnevniški vrstici in če je na dejanski vrstici prazen **Nezaračunana prodaja** tip, ki je ustvarjen iz vrstice dnevnika, dejanski ne bo zaračunan. |
    | Projekt | Izberite projekt za snemanje dejanskega na. | Na podlagi izbranega projekta, razreda transakcije in naloge bo sistem poskušal določiti stranko pogodbe, pogodbene vrstice in pogodbene vrstice. |
    | opravilo, | Izberite nalogo za snemanje dejanskega na. | Če ste med nastavitvijo pogodbe povezali naloge s pogodbenimi vrsticami, bo sistem uporabil izbrano nalogo, skupaj z razredom projekta in transakcije, da določi stranko pogodbe, pogodbene vrstice in pogodbene vrstice. |
    | Kategorija transakcije | Izberite kategorijo transakcije, da zabeležite dejansko na. | Za odhodke izbrana kategorija transakcije določi privzeto ceno, ki bo vpisana v vrstico dnevnika, ko je shranjena. |
    | Vloga | To polje je pomembno za vrstice časovnega dnevnika. Izberite vlogo vira, ki je porabil čas za projekt in/ali nalogo. | Če za vrstice časovnega dnevnika uporabite konfiguracijo izven škatle za vnos privzetih stroškov virov in obračunskih stopenj, se izbrana vloga uporablja skupaj z enoto virov za določitev privzete cene, ki bo vnesena v vrstico dnevnika, ko je shranjeno. Če za vnos privzetih cen uporabljate konfiguracijo po meri, morate to konfiguracijo pregledati, da ugotovite, ali je **Vloga** polje se uporablja za vnos privzetih vrednosti cene. |
    | Podizvajalska pogodba | Če vrstica dnevnika predstavlja zmogljivost podizvajalcev ali stroške ali material podizvajalcev, izberite ustrezno podizvajalsko pogodbo. | Ko so zapisane vrstice stroškovnega dnevnika, bo izbrana podizvajalska pogodba določila cenik, ki se uporablja za vnos privzete cene na enoto. |
    | Podizvajalska linija | Če vrstica dnevnika predstavlja zmogljivost podizvajalcev ali stroške ali material podizvajalcev, izberite ustrezno vrstico podizvajalcev. | Ko so zapisane vrstice stroškovnega dnevnika, bo izbrana vrstica podizvajalcev zagotovila, da so izračuni razpoložljivih zmogljivosti v vrstici podizvajalcev pravilno izračunani. |
    | Način za izračun zneska | Privzeto je to polje nastavljeno na **Pomnožite količino s ceno**. Ko se uporabi ta metoda, se znesek izračuna kot *Količina* ×*Cena*. Druga podprta metoda je **Fiksna cena**. Pri uporabi te metode bo cena nastavljena na znesek, količina pa ne bo uporabljena pri izračunu. | |
    | Razpored enot in enota | Razpored enot in enota skupaj identificirata enoto količine. | Kombinacija enote in kategorije posla se uporablja za vnos privzetih cen za stroške. V privzeti konfiguraciji Project Operations se kombinacija enote, vloge in enote virov uporablja za vnos privzetih cen za čas. Če imate konfiguracijo po meri za vnos privzetih cen, bo uporabljena skupaj z enoto. Kombinacija izdelka in enote se uporablja za vnos privzetih cen za materiale. |
    | Količina | Vnesite količino. | |
    | Cena | Če cena ostane prazna, ko se ustvari vrstica dnevnika, bodo ustrezne vrednosti uporabljene za vnos privzetih cen, odvisno od razreda posla. Če je cena vnesena, ko je bila ustvarjena vrstica dnevnika, bo ta cena uporabljena. | |
    | Davek | Vnesite poljuben znesek davka. | Glede na vneseni znesek davka bo razširjeni znesek izračunan kot *Znesek* + *davek*. |

## <a name="confirm-an-entry-journal"></a>Potrdite dnevnik vstopa

Ko vnesete vse vrstice dnevnika v dnevnik vnosa, lahko dnevnik potrdite. Ta postopek bo zabeležil vsako vrstico dnevnika kot dejansko stanje na ustreznih projektih.

Ko je dnevnik potrjen, ne morete več urejati njega ali katere koli njegove vrstice.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Dejanski podatki, ustvarjeni s potrditvijo dnevnika vnosov

Obstaja nekaj ključnih razlik med dejanskim stanjem, ki je ustvarjeno s potrditvijo dnevnika vnosa, in dejanskim stanjem, ki se ustvari med odobritvijo dnevnikov porabe časa, stroškov in materiala ter potrditvijo računa v Project Operations:

- Dnevniki vnosov ne uporabljajo transakcijskih povezav, da bi povezali dejanski strošek z dejansko nezaračunano prodajo. Dejanski podatki, ki so ustvarjeni, ko so dnevniki porabe časa, stroškov in materiala odobreni, vedno uporabljajo transakcijske povezave za povezavo dejanskih stroškov in nezaračunane prodaje.
- Dnevniki vnosov ne uporabljajo izvora transakcije za povezavo dejanskih stroškov in dejanskih prodaj brez obračuna s katerim koli izvirnim zapisom. Dejanski podatki, ki so ustvarjeni, ko so dnevniki porabe časa, stroškov in materiala odobreni, vedno uporabljajo izvor transakcije, da povežejo dejanske stroške in nezaračunane prodaje z izvirnim vnosom časa.
- Ko se zaračunajo dejanski podatki o neobračunani prodaji, ki so ustvarjeni s potrditvijo dnevnika vnosa, so zaračunane dejanske prodajne vrednosti, ki so ustvarjene med potrditvijo računa, povezane z neobračunanimi dejanskimi prodajnimi dejstvi na podoben način kot neobračunane dejanske prodaje, ki so ustvarjene, ko so čas, stroški in Dnevniki porabe materiala so odobreni.
- Vrstice dnevnika vnosov, ki so ustvarjene za čas, ki ga vnesejo medorganizacijski viri, ne povzročajo dejanskega stanja **Stroški enote virov** in **Interorg prodaja** vrste, ki se samodejno ustvarijo. Te dejanske podatke je treba ustvariti ročno. To vedenje se razlikuje od vedenja za časovne vnose, ki jih beležijo medorganizacijski viri. V tem primeru, ko je čas odobren, aplikacija samodejno ustvari dejanske podatke **Stroški** tip na projektu in dejanskem stanju **Stroški enote virov** in **Interorg prodaja** vrste na lastniškem oddelku zaposlenega. Nato uporablja transakcijske povezave, da poveže te dejanske podatke skupaj, in izvor transakcije, da jih poveže z izvornim časovnim vnosom.
- Ko so dnevniki vnosov potrjeni, ustvarijo dejanske podatke. Vendar dnevnikov popravkov ni mogoče uporabiti za popravljanje teh dejanskih podatkov. To vedenje se razlikuje od vedenja za dejanske vrednosti, ki so ustvarjene, ko so odobreni dnevniki porabe časa, stroškov in materiala. V tem primeru vam aplikacija omogoča uporabo dnevnikov popravkov, da popravite dejanske podatke in odpravite morebitne napake, pod pogojem, da ti dejanski podatki še niso bili zaračunani. Če so že bili zaračunani, lahko še vedno popravite dejansko stanje, če stranki obdelate celotno dobroimetje tega dejanskega zneska.

> [!NOTE]
> Dnevniki vnosov ne uveljavljajo strogih pravil o neplačilu. Zato čim manj uporabljajte te dnevnike vnosov ter bodite previdni in previdni, da ne boste ustvarili poškodovanih finančnih podatkov v vašem sistemu. Kadar koli lahko, namesto dnevnikov vnosov uporabite dnevnike porabe časa, stroškov in materiala, nastavitev mejnikov in zadrževalnikov v projektnih pogodbah ter postopek potrditve računa projekta.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
