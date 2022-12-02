---
title: Razširitev časovnih vnosov
description: Ta članek vsebuje informacije o tem, kako lahko razvijalci razširijo kontrolnik za vnos časa.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914790"
---
# <a name="extending-time-entries"></a>Razširitev časovnih vnosov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Aplikacija Dynamics 365 Project Operations vključuje kontrolnik po meri razširljivega časovnega vnosa. Kontrolnik vključuje naslednje funkcije:

- Vodoravni vnos časa za posamezen teden
- Seštevke po dnevu, vrstici ali tednu
- Kopiranje vrstic ali tednov
- Vnos časa z obliko zapisa HH:mm ali HH.hh (samodejna pretvorba v HH.hh)
- Uvoz iz nalog, rezervacij ali sestankov

Podaljšanje časovnih vnosov je možno na dveh območjih:
- [Dodajanje časovnih vnosov po meri za lastno uporabo](#add)
- [Prilagajanje tedenskega kontrolnika časovnih vnosov](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Dodajanje časovnih vnosov po meri za lastno uporabo

Časovni vnosi so osnovna entiteta, ki se uporablja v več scenarijih. V 1. aprilskem valu leta 2020 je bila predstavljena osnovna rešitev TESA. TESA zagotavlja entiteto **Nastavitve** in novo varnostno vlogo **Uporabnik časovnega vnosa**. Vključeni sta tudi novi polji **msdyn_start** in **msdyn_end**, ki imata neposredno povezavo s poljem **msdyn_duration**. Nova entiteta, varnostna vloga in polja v več aplikacijah omogočajo bolj poenoten pristop k upravljanju časa.


### <a name="time-source-entity"></a>Entiteta časovnega vira
| Polje | Opis | 
|-------|------------|
| Imenu  | Ime vnosa časovnega vira, uporabljenega kot vrednost izbire med ustvarjanjem časovnega vnosa. |
| Privzeti časovni vir [Time Source: isdefault] | Privzeto je lahko nastavljen samo en časovni vir. To omogoča, da se za vnos privzeto določi časovni vir, če ta ni opredeljen. |
|Vrsta časovnega vira [Time Source: sourcetype] | Vrsta vira je možnost (Time Entry Source Type), ki omogoča povezavo časovnega vira z aplikacijo. Družba Microsoft pridržuje vrednosti, večje od 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Časovni vnosi in entiteta časovnega vira
Vsak časovni vnos je povezan z zapisom časovnega vira. Ta zapis določa, kako in katere aplikacije naj obdelujejo vnos časa.

Časovni vnosi vedno predstavljajo posamezen neprekinjen termin, ki je povezan z začetkom, koncem in trajanjem.

Zapis vnosa časa bo z logiko samodejno posodobljen v naslednjih primerih:

- Če sta priskrbljeni dve od treh naslednjih polj, se tretje izračuna samodejno: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- V poljih **msdyn_start** in **msdyn_end** je upoštevan časovni pas.
- Časovni vnosi, ki so ustvarjeni samo z določenima entitetama **msdyn_date** in **msdyn_duration**, se bodo zagnali ob polnoči. Polji **msdyn_start** in **msdyn_end** se bosta ustrezno posodobili.

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

1. Dodajte polje po meri v pogovorno okno **Hitro ustvarjanje**.
2. Konfigurirajte mrežo tako, da prikazuje polja po meri.
3. Po potrebi dodajte polje po meri na strani **Urejanje vrstice** ali **Urejanje časovnega vnosa**.

Prepričajte se, da ima novo polje zahtevano preverjanje na strani **Urejanje vrstice** ali **Urejanje časovnega vnosa**. Del tega opravila je zaklepanje polja na podlagi stanja časovnega vnosa.

Ko dodate polje po meri v mrežo **Časovni vnos** in nato ustvarite časovne vnose neposredno v mreži, se polje po meri za te vnose samodejno nastavi tako, da se ujema z vrstico. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodajanje polja po meri v pogovorno okno »Hitro ustvarjanje«
Polje po meri dodajte v pogovorno okno **Hitro ustvarjanje: ustvarjanje časovnega vnosa**. Uporabniki lahko nato vnesejo vrednost pri dodajanju časovnih vnosov z izbiro možnosti **Novo**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfiguriranje mreže za prikaz polja po meri
Za dodajanje polja po meri v mrežo **Tedenski časovni vnosi** obstajata dva načina.

- Prilagodite lahko pogled **Moji tedenski časovni vnosi** in mu dodate polje po meri. Določite lahko položaj in velikost polja po meri v mreži, tako da uredite te lastnosti v pogledu.
- Ustvarite nov pogled časovnih vnosov po meri in ga nastavite kot privzeti pogled. Ta pogled mora poleg stolpcev, ki jih želite imeti v mreži, vsebovati še polja **Opis** in **Zunanji komentarji**. Določite lahko položaj, velikost in privzeto zaporedje razvrščanja mreže, tako da uredite lastnosti v pogledu. Nato konfigurirajte kontrolnik po meri za ta pogled, da bo nastavljen na **Mreža časovnih vnosov**. Kontrolnik dodajte v pogled in ga izberite za **Splet**, **Telefon** in **Tablični računalnik**. Nato konfigurirajte parametre za mrežo **Tedenski časovni vnosi**. Nastavite polje **Začetni datum** na **msdyn\_date**, polje **Trajanje** na **msdyn\_duration** in polje **Stanje** na **msdyn\_entrystatus**. Polje **Seznam stanj samo za branje** je nastavljeno na **192350002 (Odobreno)**, **192350003 (Poslano)** ali **192350004 (Zahteva za preklic)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Dodajanje polja po meri ustrezni strani za urejanje
Strani, ki se uporabljajo za urejanje časovnega vnosa ali vrstice časovnih vnosov, najdete pod možnostjo **Obrazci**. Gumb **Uredi vnos** v mreži odpre stran **Uredi vnos** in gumb **Uredi vrstico** odpre stran **Urejanje vrstice**. Te strani lahko uredite tako, da vključujejo polja po meri.

Z obema načinoma boste odstranili nekaj vnaprej nastavljenih filtrirnih možnosti v entitetah **Projekt** in **Projektna opravila**, da bodo vidni vsi pogledi za iskanje po entitetah. Med vnaprej pripravljenimi pogledi so vidni le ustrezni pogledi za iskanje.

Določiti morate ustrezno stran za polje po meri. Če ste polje dodali v mrežo, bi se moralo najverjetneje prikazati na strani **Urejanje vrstice**, ki se uporablja za polja, ki veljajo za celotno vrstico časovnih vnosov. Če ima polje po meri v vrstici vsak dan drugačno vrednost (če je na primer polje po meri za končni čas), bi moralo iti na stran **Urejanje časovnega vnosa**.

Če želite dodati polje po meri na stran, povlecite element **Polje** v ustrezen položaj na strani in nato nastavite njegove lastnosti.

### <a name="add-new-option-set-values"></a>Dodajanje novih vrednosti iz nabora možnosti
Če želite vrednosti nabora možnosti dodati v vnaprej pripravljeno polje, sledite tem korakom.

1. Odprite stran za urejanje polja in nato pod **Vrsta** ob naboru možnosti izberite **Uredi**.
2. Dodajte novo možnost z oznako in barvo po meri. Če želite dodati novo stanje časovnega vnosa, je pravilno ime vnaprej pripravljenega polja **Stanje vnosa**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Določitev novega stanja časovnega vnosa kot »samo za branje«
Če želite določiti novo stanje časovnega vnosa kot »samo za branje«, dodajte novo vrednost časovnega vnosa z lastnostjo **Seznam vnosov, ki so na voljo samo za branje**. Dodajte številko, ne oznake. Del mreže časovnih vnosov, ki ga je mogoče urejati, bo zdaj zaklenjen za vrstice z novim stanjem. Za različno nastavitev lastnosti **Seznam stanj samo za branje** za različne poglede **Časovni vnos** dodajte mrežo **Časovni vnos** v razdelek za pogled **Kontrolniki po meri** in ustrezno konfigurirajte parametre.

Nato dodajte pravila poslovanja, da zaklenete vsa polja na straneh **Urejanje vrstice** in **Urejanje časovnega vnosa**. Do pravil poslovanja za te strani lahko dostopate tako, da odprete urejevalnik obrazcev za vsako stran in izberete **Pravila poslovanja**. Novo stanje lahko dodate v pogoj obstoječih pravil poslovanja ali pa novemu stanju dodate novo pravilo poslovanja.

### <a name="add-custom-validation-rules"></a>Dodajanje pravil za preverjanje po meri
Za izkušnjo mreže **Tedenski časovni vnosi** lahko dodate dve vrsti pravil preverjanja veljavnosti:

- Pravila poslovanja na strani odjemalca, ki delujejo na straneh
- Preverjanja vtičnikov na strani strežnika, ki veljajo za vse posodobitve vnosa časa

#### <a name="client-side-business-rules"></a>Pravila poslovanja na strani odjemalca
Uporabite pravila poslovanja za zaklepanje in odklepanje polj, vnesite privzete vrednosti v polja in določite preverjanja, ki potrebujejo le informacije iz trenutnega zapisa časovnega vnosa. Do pravil poslovanja za stran lahko dostopate tako, da odprete urejevalnik obrazcev in izberete **Pravila poslovanja**. Nato lahko urejate obstoječa pravila poslovanja ali dodate novo pravilo poslovanja.

#### <a name="server-side-plug-in-validations"></a>Preverjanja veljavnosti strežniških vtičnikov
Uporabite preverjanje veljavnosti vtičnika za vsa preverjanja, ki zahtevajo več konteksta, kot je na voljo za posamezen zapis časovnega vnosa. Uporabite jo tudi za vsa preverjanja veljavnosti, ki jih želite zagnati v posodobitvah znotraj vrstic v mreži. Če želite dokončati preverjanje veljavnosti, ustvarite vtičnik po meri v entiteti **Časovni vnos**.

### <a name="limits"></a>Omejitve
Trenutno ima mreža **Časovni vnos** omejitev velikosti 500 vrstic. Če je več kot 500 vrstic, odvečne vrstice ne bodo prikazane. Te omejitve velikosti ni mogoče povečati.

### <a name="copying-time-entries"></a>Kopiranje časovnih vnosov
Uporabite pogled **Kopiraj stolpce časovnih vnosov**, da določite seznam polj, ki jih želite kopirati med vnosom časa. **Datum** in **Trajanje** sta obvezni polji, ki jih ne smete odstraniti iz pogleda.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
