---
title: Stroški za dnevnice
description: Ta članek vsebuje informacije o tem, kako delati s stroški za dnevnice.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923208"
---
# <a name="per-diem-expenses"></a>Stroški za dnevnice

> [!IMPORTANT] 
> Funkcija, opisana v tem članku, je na voljo ciljnim uporabnikom kot del predogledne različice.

Dnevnica je fiksen, vnaprej določen dnevni dodatek, ki ga podjetje plača svojim zaposlenim za nastanitev (hotele), prehrano in nepredvidene stroške, ki jih imajo ti zaposleni med poslovnim potovanjem. Podjetje ta dodatek zaposlenim izplača namesto dejanskih potnih stroškov. Zaposleni lahko uporabljajo svoje dnevnice **Nepredvideni stroški/drugo** za kritje napitnin, sobne strežbe, storitev pranja perila ali kemičnega čiščenja za pomembne poslovne sestanke. Višina dnevnice se lahko razlikuje glede na to, ali se delodajalec odloči za povračilo skupnih stroškov bivanja in prehrane ali samo stroškov prehrane in nepredvidenih stroškov.

Dnevnice lahko temeljijo na letnem času, kraju potovanja ali obojem. Ko ustvarite pravilo za dnevnice, lahko določite, da se izbrani odstotek od dnevnice zadrži, če zaposleni prejme brezplačne obroke ali storitve. Določite lahko tudi najmanjše in največje število ur, za katera lahko velja dnevnica za potovanje zaposlenega.

Dnevnica se izračuna kot skupni dodatek, ki je ponujen na dan, zmanjšan za znižanje obroka (strošek brezplačne prehrane), ki je zagotovljen zaposlenemu.

## <a name="configure-per-diems"></a>Konfiguracija dnevnice

Če želite konfigurirati stroške za dnevnico, upoštevajte ta navodila:

1. Odprite razdelek **Upravljanje stroškov** \> **Nastavitev** \> **Splošno** \> **Parametri upravljanja stroškov**.
2. V zavihku **Dnevnica** v polju **Izračun znižanja za obrok glede na** izberite način obračuna dnevnic:

    - **Vrsta obroka na potovanje** – izračun dnevnice glede na vrsto vpisanega obroka (zajtrk, kosilo ali večerja) in znižanje obroka, ki je določeno za posamezno vrsto obroka za dnevnico za čas trajanja potovanja.
    - **Vrsta obroka na dan** – izračun dnevnice glede na vrsto vpisanega obroka in znižanje obroka, ki je določeno za posamezno vrsto obroka za dodatek dnevnice na dan.
    - **Število obrokov na dan** – izračun dnevnice glede na število vnesenih obrokov na dan in na znižanje obrokov za število obrokov, ki so dnevno zagotovljeni.

3. Odprite razdelek **Upravljanje stroškov** \> **Nastavitev** \> **Izračuni in kode** \> **Lokacije dnevnic**.
4. Dodajte lokacije, kjer je možno koristiti dnevnice.
5. Za vsako dodano lokacijo v zavihku **Dnevnice** izberite vrednost dnevnice in valuto, ki veljata med izbranim začetnim ter končnim datumom za nastanitev, prehrano in druge stroške. Vrednosti dnevnic in valute konfigurirate tako, da odprete **Upravljanje stroškov** \> **Nastavitev** \> **Izračuni in kode** \> **Dnevnice**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dnevnice v prenovljenem vmesniku stroškov

Funkcija dnevnice je podprta v prenovljenem delovnem prostoru **Upravljanje stroškov** v storitvi Microsoft Dynamics 365 Finance, različica 10.0.25 in novejše.

Če želite omogočiti dnevnice, sledite tem korakom.

1. V delovnem prostoru **Upravljanje funkcij** poiščite in izberite funkcijo **Prenovljena poročila o stroških** na seznamu in nato izberite **Omogoči zdaj**.
2. Poiščite in izberite funkcijo **Dnevnica za prenovljen vmesnik poročila o stroških** na seznamu, nato pa izberite **Omogoči zdaj**.

## <a name="how-the-feature-works"></a>Kako deluje funkcija

V tem razdelku so primeri za tri scenarije konfiguracij. Za vsak primer je polje **Izračun znižanja za obrok glede na** nastavljeno na drugo vrednost. Za vse tri primere je skupni znesek, ki ga je treba plačati, enak do uveljavitve znižanja obroka. Po tej točki se skupni znesek za plačilo razlikuje za vsak primer.

Če želite ustvariti strošek za dnevnico, ki se uporablja za vse tri primere, sledite tem korakom.

1. Odprite zavihek **Delovni prostori** \> **Upravljanje stroškov**.
2. Izberite **Novo poročilo o stroških** ali izberite obstoječe poročilo o stroških na seznamu.
3. Dodajte nov strošek. V polju **Kategorija** izberite **Dnevnica**. Izberite lokacijo ter začetni in končni datum vašega potovanja. Dnevnica za nastanitev, prehrano in nepredvidene stroške (ostali stroški) se izračuna glede na dnevnico, ki je določena za izbrano lokacijo.

    Na primer, kot lokacijo izberete **Redmond (ZDA)**. Dnevni dodatek za to lokacijo je 150 ameriških dolarjev (150 USD) za nastanitev, USD 75 za obroke in USD 5 za nepredvidene stroške. Začetni datum je 10. januar, končni pa 14. januar. Zato je izbrano trajanje pet dni, če je izbrana konfiguracija koledarski dnevi s časom, izbrani čas pa se začne in konča ob 12:00 na začetni in končni datum. Tukaj so izračuni:

    - Skupni znesek za plačilo = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
    - Obrok in dodatni del skupnega zneska = 5 × (75 + 5) = 400 USD

Če so bili med potovanjem zagotovljeni zajtrk, kosilo in večerja, je treba te obroke obračunati kot znižanje obroka.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Primer 1: dnevnice, kjer znižanja obrokov temeljijo na vrsti obroka na potovanje

V tem primeru je znižanje obroka 30 odstotkov za zajtrk, 30 odstotkov za kosilo in 40 odstotkov za večerjo. Na strani **Parametri upravljanja stroškov** je polje **Izračun znižanja za obrok glede na** nastavljeno na **Vrsta obroka na potovanje**. Tukaj so izračuni, če so bili zaposlenim zagotovljeni trije zajtrki, dve kosili in nič večerje:

- Zmanjšanje obroka = (3 × \[75 × 30 %\]) + (2 × \[75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Obroki in nepredvideni stroški = 400 – 112,50 = 287,50 USD
- Skupni znesek za plačilo = skupni dodatek – znižanje obroka = 1.150 – 112,50 = 1.037,50 USD

![Strošek za dnevnico, kjer znižanje obrokov temelji na vrsti obroka na potovanje.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Primer 2: dnevnice, kjer znižanja obrokov temeljijo na vrsti obroka na dan

V tem primeru je znižanje obroka 30 odstotkov za zajtrk, 30 odstotkov za kosilo in 40 odstotkov za večerjo. Na strani **Parametri upravljanja stroškov** je polje **Izračun znižanja za obrok glede na** nastavljeno na **Vrsta obroka na dan**. V tem primeru v mreži **Obroki** v pogovornem oknu **Uredi stroške** počistite potrditvena polja, da označite, kateri obroki so vam bili na voljo med potovanjem.

Na primer, tukaj so izračuni, če je bil zajtrk zagotovljen za prve tri dni potovanja:

- Dnevno zmanjšanje obrokov za vsakega od prvih treh dni = 75 × 30 % = 22,50 USD
- Skupno zmanjšanje obroka = 3 × 22,50 = 67,50 USD
- Obroki in nepredvideni stroški za 1.– 3. dan = 75 – 22,50 = 57,50 USD
- Skupni obroki in nepredvideni stroški = vsota obrokov in nepredvidenih stroškov v petih dneh = 400 – 67,50 = 332,50 USD
- Skupni znesek za plačilo = skupni znesek – znižanje obroka = 1.150 – 67,50 = 1.082,50 USD

![Strošek za dnevnico, kjer znižanje obrokov temelji na vrsti obroka na dan.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Primer 3: dnevnice, kjer znižanja obrokov temeljijo na številu obrokov na dan

V tem primeru je zmanjšanje obroka izračunano na podlagi števila obrokov, ki so bili zagotovljeni na dan (tj. polje **Izračun znižanja za obrok glede na** na strani **Parametri upravljanja stroškov** je nastavljeno na **Število obrokov na dan**). V mreži **Obroki** v pogovornem oknu **Uredi stroške** počistite potrditvena polja, da označite, kateri obroki so vam bili zagotovljeni.
V tem primeru znižanje obroka temelji le na št. zagotovljenih obrokov in ne glede na vrsto zagotovljenega obroka (zajtrk/kosilo/večerja).

Tukaj so izračuni za dnevnice, ko je dnevnica 150 USD za nastanitev, 75 USD za prehrano in 5 USD za nepredvidene stroške:

- **Skupni znesek za plačilo** = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
- **En obrok:** Zmanjšanje obroka = 20 % = 15 USD
- **Dva obroka:** Zmanjšanje obroka = 50 % = 37,50 USD
- **Trije obroki:** Zmanjšanje obroka = 100 % = 75 USD

Tukaj so izračuni za **dodatek za prehrano in nepredvidene stroške**, ki vključuje 5 USD za nepredvidene stroške:

- 1. dan – dva zagotovljena obroka = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- 2. dan – dva zagotovljena obroka = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- 3. dan – en zagotovljen obrok = (75 – 15) + 5 = 60 + 5 = 65 USD
- 4. dan – nič zagotovljenih obrokov = (75 – 0) + 5 = 75 + 5 = 80 USD
- 5. dan – trije zagotovljeni obroki = (75 – 75) + 5 = 0 + 5 = 5 USD

- Skupno št. obrokov in nepredvideni stroški = obroki in nepredvideni stroški za 1. dan + 2. dan + 3. dan + 4. dan + 5. dan = 235 USD
- Skupno zmanjšanje obroka = Zmanjšanje obroka za 1. dan + 2. dan + 3. dan + 4. dan + 5. dan = 37,5 + 37,5 + 15 + 0 + 75 = 165 USD
- Skupni znesek za plačilo = skupni dodatek – skupno zmanjšanje obroka = 1.150 USD – 165 USD = 985 USD

![Strošek za dnevnico, kjer znižanje obrokov temelji na številu obrokov na dan.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Od različice aplikacije Finance 10.0.23 dalje, če uporabljate prenovljen vmesnik stroškov, ne morete ustvariti dnevnic s prekrivajočimi se datumi. Če poskusite, boste prejeli sporočilo o napaki.
