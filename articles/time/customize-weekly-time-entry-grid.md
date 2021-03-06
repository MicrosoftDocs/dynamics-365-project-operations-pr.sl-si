---
title: Razširitev časovnih vnosov
description: Ta tema vsebuje informacije o tem, kako lahko razvijalci razširijo kontrolnik za vnos časa.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930900"
---
# <a name="extending-time-entries"></a>Razširitev časovnih vnosov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Aplikacija Dynamics 365 Project Operations vključuje prilagodljiv in razširljiv kontrolnik za vnos časa. Kontrolnik vključuje naslednje funkcije:

- Vodoravni vnos časa za posamezen teden
- Seštevke po dnevu, vrstici ali tednu
- Kopiranje vrstic ali tednov
- Vnos časa z obliko zapisa HH:mm ali HH.hh (samodejna pretvorba v HH.hh)
- Uvoz iz nalog, rezervacij ali sestankov

Podaljšanje časovnih vnosov je možno na dveh območjih:
- [Dodajanje časovnih vnosov po meri za lastno uporabo](#add)
- [Prilagajanje tedenskega kontrolnika časovnih vnosov](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Dodajanje časovnih vnosov po meri za lastno uporabo

Časovni vnosi so osnovna entiteta, ki je zasnovana za uporabo v več primerih. V 1. aprilskem valu leta 2020 je bila predstavljena osnovna rešitev TESA, ki zagotavlja entiteto **Nastavitve** in novo varnostno vlogo **uporabnika časovnih vnosov**. Vključeni sta tudi novi polji **msdyn_start** in **msdyn_end**, ki imata neposredno povezavo s poljem **msdyn_duration**. Nova entiteta, varnostna vloga in polja v več aplikacijah omogočajo bolj poenoten pristop k upravljanju časa.


### <a name="time-source-entity"></a>Entiteta časovnega vira
| Polje | Opis | 
|-------|------------|
| Imenu  | Ime vnosa časovnega vira, uporabljenega kot vrednost izbire med ustvarjanjem časovnega vnosa. |
| Privzeti časovni vir [Time Source: isdefault] | Privzeto je lahko privzeti časovni vir označen samo en časovni vir. Ta zmožnost omogoča, da se za vnos privzeto določi časovni vir, če ta ni opredeljen. |
|Vrsta časovnega vira [Time Source: sourcetype] | Vrsta vira je možnost (Time Entry Source Type), ki omogoča povezavo časovnega vira z aplikacijo. Temu naboru možnosti bodo dodane dodatne vrednosti, ko bodo dodane dodatne aplikacije. Upoštevajte, da družba Microsoft pridržuje vrednosti, večje od 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Časovni vnosi in entiteta časovnega vira
Vsak časovni vnos je povezan z zapisom časovnega vira. Ta zapis določa, kako in katere aplikacije naj obdelujejo vnos časa.

Časovni vnosi vedno predstavljajo posamezen neprekinjen termin, ki je povezan z začetkom, koncem in trajanjem.

Zapis vnosa časa bo z logiko samodejno posodobljen v naslednjih primerih:

- Če sta priskrbljeni dve od treh naslednjih polj, se tretje izračuna samodejno: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- V poljih **msdyn_start** in **msdyn_end** je upoštevan časovni pas.
- Začetek časovnih vnosov, ustvarjenih samo z določenima poljema **msdyn_date** in **msdyn_duration**, je nastavljen na polnoč. Polji **msdyn_start** in **msdyn_end** bosta ustrezno posodobljeni.

#### <a name="time-entry-types"></a>Vrste časovnih vnosov

Zapisi vnosa časa imajo povezan tip, ki določa vedenje v toku oddaje za povezano aplikacijo.

|Nalepka | Vrednost|
|-----|-----|
|Na odmoru   |192,355,000|
|Potovanja | 192,355,001|
|Nadure   | 192,354,320|
|Delo   | 192,350,000|
|Odsotnost    | 192,350,001|
|Dopust   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Prilagajanje tedenskega kontrolnika časovnih vnosov
Razvijalci lahko drugim entitetam dodajo dodatna polja in poizvedbe ter uvedejo prilagojena poslovna pravila za podporo poslovnih scenarijev.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Dodajanje polj po meri z možnostjo iskanja po drugih entitetah
Za dodajanje polja po meri v tedensko mrežo časovnih vnosov je treba izvesti tri glavne korake.

- Dodajte polje po meri v pogovorno okno za hitro ustvarjanje.
- Konfigurirajte mrežo tako, da prikazuje polja po meri.
- Dodajte polje po meri bodisi na potek opravila za urejanje vrstice ali pa na potek opravila za urejanje celice.

Prav tako morate zagotoviti, da ima novo polje zahtevano preverjanje v poteku opravila za urejanje vrstic ali celic. Del tega koraka je zaklepanje polja na podlagi stanja časovnega vnosa.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodajanje polja po meri v pogovorno okno za hitro ustvarjanje
Polje po meri morate dodati v pogovorno okno **Hitro ustvarjanje časovnega vnosa**. Uporabniki lahko nato vnesejo vrednost pri dodajanju časovnih vnosov z izbiro možnosti **Novo**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfiguriranje mreže za prikaz polja po meri
Za dodajanje polja po meri v tedensko mrežo časovnih vnosov obstajata dva načina:

  - Prilagodite pogled in dodajte polje po meri
  - Ustvarite nov privzeti časovni vnos po meri 


**Prilagajanje pogleda in dodajanje polj po meri**

Prilagodite lahko pogled **Moji tedenski časovni vnosi** in mu dodate polje po meri. Izberete lahko položaj in velikost polja po meri v mreži, tako da uredite te lastnosti v pogledu.

**Ustvarjanje novega privzetega časovnega vnosa po meri** 

Ta pogled mora poleg stolpcev, ki jih želite imeti v mreži, vsebovati še polja **Opis** in **Zunanji komentarji**. 

1. Izberete lahko položaj, velikost in privzeto zaporedje razvrščanja mreže, tako da uredite te lastnosti v pogledu. 
2. Konfigurirajte kontrolnik po meri za ta pogled, da bo nastavljen na kontrolnik **Mreža časovnih vnosov**. 
3. Ta kontrolnik dodajte v pogled in ga izberite za splet, telefon in tablični računalnik. 
4. Konfigurirajte parametre za tedensko mrežo časovnih vnosov. Nastavite polje **Začetni datum** na **msdyn_date**, polje **Trajanje** na **msdyn_duration** in polje **Stanje** na **msdyn_entrystatus**. 
5. V privzetem pogledu je polje **Seznam vnosov s stanjem samo za branje** nastavljeno na **192350002,192350003,192350004**, polje **Potek opravila urejanja vrstice** na **msdyn_timeentryrowedit** in polje **Potek opravila urejanja celice** na **msdyn_timeentryedit**. 
6. Ta polja lahko prilagodite, če želite dodati ali odstraniti stanje samo za branje ali uporabiti drugačno izkušnjo na podlagi opravila (TBX) za urejanje vrstic ali celic. Ta polja morajo biti vezana na statično vrednost.


> [!NOTE] 
> Z obema načinoma boste odstranili nekaj vnaprej nastavljenih filtrirnih možnosti v entitetah **Projekt** in **Projektna opravila**, da bodo vidni vsi pogledi za iskanje po entitetah. Med vnaprej pripravljenimi pogledi so vidni le relevantni pogledi za iskanje.
Določiti morate ustrezen potek opravila za polje po meri. Če ste polje dodali v mrežo, bi se moralo najverjetneje prikazati v poteku opravila za urejanje vrstice, ki se uporablja za polja, ki veljajo za celotno vrstico časovnih vnosov. Če ima polje po meri vsak dan drugačno vrednost, tako kot na primer polje po meri za **Končni čas**, bi moralo iti v potek opravila za urejanje celic.

Če želite dodati polje po meri v potek opravila, povlecite element **Polje** v ustrezen položaj na strani in nato nastavite lastnosti polja. Nastavite lastnost **Vir** na **Časovni vnos** in nato nastavite še lastnost **Podatkovno polje** v polje po meri. Lastnost **Polje** označuje prikazno ime na strani TBX. Izberite možnost **Uporabi**, da shranite spremembe v polju, in nato izberite možnost **Nadgradnja**, da shranite spremembe na strani.

Če želite namesto tega uporabiti novo stran TBX po meri, ustvarite nov proces. Nastavite kategorijo na **Potek poslovnega procesa**, entiteto na **Časovni vnos** in nato še vrsto poslovnega procesa na **Zaženi proces kot potek opravila**. V razdelku **Lastnosti** mora biti lastnost **Ime strani** nastavljena na prikazno ime strani. Dodajte vsa ustrezna polja na stran TBX. Shranite in zaženite proces ter posodobite lastnost kontrolnika po meri za ustrezen potek opravila v vrednost **Ime** za izbrani postopek.

### <a name="add-new-option-set-values"></a>Dodajanje novih vrednosti iz nabora možnosti
Če želite dodati vrednosti iz nabora možnosti v vnaprej nastavljeno polje, odprite stran za urejanje polja in nato pod **Vrsta** ob naboru možnosti izberite **Uredi**. Nato dodajte novo možnost z oznako in barvo po meri. Če želite dodati novo stanje časovnega vnosa, je pravilno ime vnaprej pripravljenega polja **Stanje vnosa** in ne **Stanje**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Določitev novega stanja časovnega vnosa kot »samo za branje«
Če želite določiti novo stanje časovnega vnosa kot »samo za branje«, dodajte novo vrednost časovnega vnosa z lastnostjo **Seznam vnosov, ki so na voljo samo za branje**. Del mreže časovnih vnosov, ki ga je mogoče urejati, bo zaklenjen za vrstice z novim stanjem.
Nato dodajte pravila poslovanja, da zaklenete vsa polja v straneh TBX **Urejanje vrstice časovnega vnosa** in **Urejanje časovnega vnosa**. Do pravil poslovanja za te strani lahko dostopate tako, da odprete urejevalnik poteka poslovnega procesa za to stran in izberete **Pravila poslovanja**. Novo stanje lahko dodate v pogoj obstoječih pravil poslovanja ali pa novemu stanju dodate novo pravilo poslovanja.

### <a name="add-custom-validation-rules"></a>Dodajanje pravil za preverjanje po meri
Za izkušnjo tedenske mreže za vnos časa lahko dodate dve vrsti pravil preverjanja veljavnosti:

- Poslovna pravila na strani odjemalca, ki delujejo v pogovornih oknih za hitro ustvarjanje in na straneh TBX.
- Preverjanja vtičnikov na strani strežnika, ki veljajo za vse posodobitve vnosa časa.

#### <a name="business-rules"></a>Poslovna pravila
Uporabite pravila poslovanja za zaklepanje in odklepanje polj, vnesite privzete vrednosti v polja in določite preverjanja, ki potrebujejo le informacije iz trenutnega zapisa časovnega vnosa. Do pravil poslovanja za stran TBX lahko dostopate tako, da odprete urejevalnik poteka poslovnega procesa za to stran in izberete **Pravila poslovanja**. Nato lahko urejate obstoječa pravila poslovanja ali dodate novo pravilo poslovanja. Za večjo izbiro prilagojenih preverjanj lahko uporabite pravilo poslovanja za zagon JavaScript.

#### <a name="plug-in-validations"></a>Preverjanja vtičnika
Uporabite preverjanje vtičnika za vsa preverjanja, ki zahtevajo več konteksta, kot je na voljo za posamezen zapis časovnega vnosa, ali vsa preverjanja, ki jih želite zagnati v posodobitvah znotraj vrstic v mreži. Če želite dokončati preverjanje, ustvarite vtičnik po meri v entiteti **Časovni vnos**.
