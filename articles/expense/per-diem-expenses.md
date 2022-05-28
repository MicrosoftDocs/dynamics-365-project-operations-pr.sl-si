---
title: Dnevnice
description: Ta tema ponuja informacije o tem, kako delati z dnevnimi stroški.
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
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596070"
---
# <a name="per-diem-expenses"></a>Dnevnice

> [!IMPORTANT] 
> Funkcionalnost, ki je opisana v tem tema, je na voljo ciljnim uporabnikom kot del izdaje za predogled.

Dnevnica je fiksna, vnaprej določena dnevnica, ki jo podjetje plača svojim zaposlenim za prenočišče (hotele), prehrano in nepredvidene stroške, ki jih imajo ti zaposleni med potovanjem na delo. Podjetje zaposlenim izplačuje ta dodatek namesto dejanskih potnih stroškov. Zaposleni lahko uporabljajo svoje **Slučaji/drugo** dnevnice za kritje napitnine, sobne strežbe, pranja perila ali kemičnega čiščenja za pomembna poslovna srečanja. Dnevnica se lahko razlikuje, odvisno od tega, ali se delodajalec odloči, da bo povrnil skupne stroške nastanitve in obrokov ali samo stroške obrokov in nepredvidenih stroškov.

Dnevnice lahko temeljijo na letnem času, kraju potovanja ali obojem. Ko ustvarite pravilo za dnevnice, lahko določite, da bo odstotek dnevnic zadržan, če zaposleni prejme brezplačne obroke ali storitve. Nastavite lahko tudi najmanjše in največje število ur, za katere se dnevnica lahko uporabi za potovanja zaposlenega.

Dnevnica se izračuna kot skupni dodatek, ki je ponujen na dan, zmanjšan za znižanje obrokov (stroški brezplačnih obrokov), ki je zagotovljeno zaposlenemu.

## <a name="configure-per-diems"></a>Konfigurirajte dnevnice

Če želite konfigurirati dnevnice, sledite tem korakom.

1. Pojdi do **Upravljanje odhodkov** \> **Nastaviti** \> **General** \> **Parametri upravljanja odhodkov**.
2. Na **Dnevnice** zavihek, v **Izračunajte zmanjšanje obroka za** polje, izberite, kako naj se izračunajo dnevnice:

    - **Vrsta obroka na potovanje** – Izračunajte dnevnico glede na vrsto vnesenega obroka (zajtrk, kosilo ali večerja) in na podlagi znižanja obrokov, ki je določeno za vsako vrsto obroka za dnevnico za čas potovanja.
    - **Vrsta obroka na dan** – Izračunajte dnevnico glede na vrsto vnesenega obroka in na znižanje obrokov, ki je določeno za vsako vrsto obroka za dnevnico na dan.
    - **Število obrokov na dan** – Izračunajte dnevnico glede na število vnesenih obrokov na dan in na znižanje obrokov za število obrokov, ki so zagotovljeni vsak dan.

3. Pojdi do **Upravljanje odhodkov** \> **Nastaviti** \> **Izračuni in kode** \> **Lokacije dnevnic**.
4. Dodajte lokacije, kjer se lahko porabijo dnevnice.
5. Za vsako lokacijo, ki jo dodate, na **Dnevnice** izberite dnevnico in valuto, ki veljata med določenim začetnim in končnim datumom za nastanitev, obroke in druge stroške. Če želite konfigurirati dnevnice in valute, pojdite na **Upravljanje odhodkov** \> **Nastaviti** \> **Izračuni in kode** \> **Dnevnice**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dnevnice v prenovljenem vmesniku stroškov

Funkcija dnevnice je podprta v prenovljenem **Upravljanje odhodkov** delovni prostor v Microsoft Dynamics 365 Finance različica 10.0.25 in novejše.

Če želite omogočiti dnevnice, sledite tem korakom.

1. V **Upravljanje funkcij** delovni prostor, poiščite in izberite **Prenovljena poročila o stroških** funkcijo na seznamu in nato izberite **Omogoči zdaj**.
2. Poiščite in izberite **Dnevnica za poročilo o stroških na novo zasnovan vmesnik** funkcijo na seznamu in nato izberite **Omogoči zdaj**.

## <a name="how-the-feature-works"></a>Kako deluje funkcija

V tem razdelku so primeri za tri konfiguracijske scenarije. Za vsak primer, **Izračunajte zmanjšanje obroka za** polje je nastavljeno na drugo vrednost. Za vse tri primere je skupni znesek, ki ga je treba plačati, enak, dokler se ne uporabi znižanje obrokov. Po tej točki se skupni znesek, ki ga je treba plačati, razlikuje za vsak primer.

Če želite ustvariti dnevnice, ki se uporabljajo za vse tri primere, sledite tem korakom.

1. Pojdi do **Delovni prostori** \> **Upravljanje odhodkov**.
2. Izberite **Novo poročilo o stroških** ali izberite obstoječe poročilo o stroških.
3. Dodajte nov strošek. V **Kategorija** polje, izberite **Dnevnice**. Izberite lokacijo ter datum začetka in konca potovanja. Dnevnica za bivanje, prehrano in nepredvidene stroške (druge stroške) se izračuna glede na dnevnico, ki je določena za izbrano lokacijo.

    Na primer, izberete **Redmond (ZDA)** kot lokacija. Dnevni dodatek za to lokacijo je 150 ameriških dolarjev (150 USD) za prenočišče, USD 75 za obroke in USD 5 za nepredvidene stroške. Začetni datum je 10. januar, končni datum pa 14. januar. Zato je izbrano trajanje pet dni, ko je izbrana konfiguracija koledarski dnevi s časom, izbrani čas pa se začne in konča ob 12:00 na začetni in končni datum. Tukaj so izračuni:

    - Skupni znesek za plačilo = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Obrok in naključni del celotne količine = 5 × (75 + 5) = USD 400

Če so bili med potovanjem zagotovljeni zajtrk, kosilo in večerja, je treba te obroke upoštevati kot znižanje obrokov.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Primer 1: Dnevnica, kjer znižanja obrokov temeljijo na vrsti obroka na potovanje

V tem primeru je zmanjšanje obroka 30 odstotkov za zajtrk, 30 odstotkov za kosilo in 40 odstotkov za večerjo. Na **Parametri upravljanja odhodkov** stran, **Izračunajte zmanjšanje obroka za** polje je nastavljeno na **Vrsta obroka na potovanje**. Tukaj so izračuni, če so bili zaposlenemu zagotovljeni trije zajtrki, dve kosili in nič večerje:

- Zmanjšanje obroka = (3 ×\[ 75 × 30 %\]) + (2 ×\[ 75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Obroki in pomožni stroški = 400 – 112,50 = USD 287.50
- Skupni znesek, ki ga je treba plačati = Skupni dodatek – Zmanjšanje obrokov = 1.150 – 112,50 = USD 1,037.50

![Odhodki za dnevnice, kjer znižanje obroka temelji na vrsti obroka na potovanje.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Primer 2: Dnevnica, kjer znižanje obrokov temelji na vrsti obroka na dan

V tem primeru je zmanjšanje obroka 30 odstotkov za zajtrk, 30 odstotkov za kosilo in 40 odstotkov za večerjo. Na **Parametri upravljanja odhodkov** stran, **Izračunajte zmanjšanje obroka za** polje je nastavljeno na **Vrsta obroka na dan**. V tem primeru v **Obroki** mrežo v **Uredi stroške** v pogovornem oknu počistite potrditvena polja, da označite, kateri obroki so vam bili na voljo med potovanjem.

Tukaj so na primer izračuni, če je bil zajtrk zagotovljen za prve tri dni potovanja:

- Zmanjšanje dnevnega obroka za vsak od prvih treh dni = 75 × 30 % = USD 22.50
- Skupno zmanjšanje obrokov = 3 × 22,50 = USD 67.50
- Obroki in dodatni stroški za dneve od 1. do 3. = 75 – 22.50 = USD 57.50
- Skupni obroki in nepredvideni stroški = Vsota obrokov in nepredvidenih stroškov v petih dneh = 400 – 67,50 = USD 332.50
- Skupni znesek, ki ga je treba plačati = Skupni znesek – Zmanjšanje obrokov = 1.150 – 67,50 = USD 1,082.50

![Dnevnice, kjer znižanje obroka temelji na vrsti obroka na dan.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Primer 3: Dnevnica, kjer znižanje obrokov temelji na številu obrokov na dan

V tem primeru se zmanjšanje obroka izračuna na podlagi števila obrokov, ki so bili zagotovljeni na dan (tj.**Izračunajte zmanjšanje obroka za** polje na **Parametri upravljanja odhodkov** stran je nastavljena na **Število obrokov na dan**). V **Obroki** mrežo v **Uredi stroške** pogovornem oknu počistite potrditvena polja, da označite, kateri obroki so bili zagotovljeni.
V tem primeru znižanje obroka temelji samo na # zagotovljenih obrokih in ne na vrsti obroka (zajtrk/kosilo/večerja).

Tukaj so izračuni za dnevnice, ko je dnevnica USD 150 za bivanje, USD 75 za obroke in USD 5 za nepredvidene stroške:

- **Skupni znesek za plačilo** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **En obrok:** Znižanje obrokov = 20 % = USD 15
- **dva obroka:** Znižanje obrokov = 50 % = USD 37.50
- **trije obroki:** Znižanje obrokov = 100 % = USD 75

Tukaj so izračuni za **obroki in nepredvideni stroški**, ki vključuje USD 5 za nepredvidene stroške:

- 1. dan - zagotovljena dva obroka = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 2. dan - zagotovljena dva obroka = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 3. dan - En obrok zagotovljen = (75 – 15) + 5 = 60 + 5 = USD 65
- 4. dan - Nič obrokov = (75-0) + 5 = 75 + 5 = USD 80
- 5. dan - zagotovljeni trije obroki = (75 – 75) + 5 = 0 + 5 = USD 5

- Skupno število obrokov in nepredvidenih stroškov = Obroki in dogodki za 1. dan + 2. dan + 3. dan + 4. dan + 5. dan = USD 235
- Skupno zmanjšanje obroka = zmanjšanje obroka za 1. dan+ 2. dan + 3. dan+ 4. dan+ 5. dan= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Skupni znesek, ki ga je treba plačati = Skupni dodatek – Skupno zmanjšanje obrokov = USD 1,150 - USD 165 = USD 985

![Dnevnice, kjer znižanje obrokov temelji na številu obrokov na dan.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Od različice Finance 10.0.23, če uporabljate prenovljeni vmesnik za stroške, ne morete ustvariti dnevnic, ki imajo prekrivajoče se datume. Če poskusite, boste prejeli sporočilo o napaki.
