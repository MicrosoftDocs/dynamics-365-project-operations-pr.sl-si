---
title: Razširitev časovnih vnosov
description: Ta tema vsebuje informacije o tem, kako lahko razvijalci razširijo kontrolnik za vnos časa.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583006"
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
Vsak časovni vnos je povezan z zapisom časovnega vira. Ta zapis določa, katere aplikacije naj obdelajo vnos časa in kako.

Časovni vnosi vedno predstavljajo posamezen neprekinjen termin, ki je povezan z začetkom, koncem in trajanjem.

Zapis vnosa časa bo z logiko samodejno posodobljen v naslednjih primerih:

- Če sta priskrbljeni dve od treh naslednjih polj, se tretje izračuna samodejno: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- The **msdyn_start** in **msdyn_end** polja se zavedajo časovnega pasu.
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

1. Dodajte polje po meri v **Hitro ustvarjanje** pogovorno okno.
2. Konfigurirajte mrežo tako, da prikazuje polja po meri.
3. Dodajte polje po meri v **Urejanje vrstice** oz **Urejanje časovnega vnosa** stran, kot je primerno.

Prepričajte se, da ima novo polje zahtevane potrditve na **Urejanje vrstice** oz **Urejanje časovnega vnosa** stran. Kot del te naloge zaklenite polje glede na stanje vnosa časa.

Ko dodate polje po meri v **Vnos časa** mrežo in nato ustvarite časovne vnose neposredno v mreži, se polje po meri za te vnose samodejno nastavi tako, da se ujema z vrstico. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodajte polje po meri v pogovorno okno Hitro ustvarjanje
Dodajte polje po meri v **Hitro ustvarjanje: Ustvari vnos časa** pogovorno okno. Uporabniki lahko nato vnesejo vrednost pri dodajanju časovnih vnosov z izbiro možnosti **Novo**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfiguriranje mreže za prikaz polja po meri
Polje po meri lahko dodate na dva načina **Tedenski vnos časa** mreža.

- Prilagodite **Moji tedenski vnosi časa** pogled in mu dodajte polje po meri. Določite lahko položaj in velikost polja po meri v mreži z urejanjem lastnosti v pogledu.
- Ustvarite nov pogled vnosa časa po meri in ga nastavite kot privzeti pogled. Ta pogled bi moral vsebovati **Opis** in **Zunanji komentarji** polja poleg stolpcev, ki jih želite vključiti v mrežo. Določite lahko položaj, velikost in privzeti vrstni red mreže z urejanjem lastnosti v pogledu. Nato konfigurirajte kontrolnik po meri za ta pogled, da bo nastavljen na **Mreža časovnih vnosov**. Dodajte kontrolnik v pogled in ga izberite za **spletu**, **·**, in **tablica**. Nato konfigurirajte parametre za **Tedenski vnos časa** mreža. Nastavite **Začetni datum** polje do **msdyn\_ datum**, nastavite **Trajanje** polje do **msdyn\_ trajanje**, in nastavite **Stanje** polje do **msdyn\_ vstopni status**. The **Seznam statusov samo za branje** polje je nastavljeno na **192350002 (odobreno)**, **(Oddano)**, oz **192350004 (zahtevan odpoklic)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Dodajte polje po meri na ustrezno stran za urejanje
Strani, ki se uporabljajo za urejanje časovnega vnosa ali vrstice časovnih vnosov, najdete pod **Obrazci**. The **Uredi vnos** gumb v mreži odpre **Uredi vnos** stran in **Uredi vrstico** gumb odpre **Urejanje vrstice** stran. Te strani lahko uredite tako, da vključujejo polja po meri.

Obe možnosti odstranita vklopljeno filtriranje izven škatle **Projekt** in **Projektna naloga** entitete, tako da so vidni vsi pogledi iskanja za entitete. Med vnaprej pripravljenimi pogledi so vidni le ustrezni pogledi za iskanje.

Določiti morate ustrezno stran za polje po meri. Najverjetneje, če ste polje dodali v mrežo, bi moralo iti na **Urejanje vrstice** stran, ki se uporablja za polja, ki veljajo za celotno vrstico časovnih vnosov. Če ima polje po meri vsakodnevno edinstveno vrednost v vrstici (na primer, če je to polje po meri za končni čas), bi moralo iti na **Urejanje časovnega vnosa** stran.

Če želite na stran dodati polje po meri, povlecite a **Polje** element na ustrezen položaj na strani in nato nastavite njegove lastnosti.

### <a name="add-new-option-set-values"></a>Dodajanje novih vrednosti iz nabora možnosti
Če želite dodati vrednosti nabor možnosti v polje izven škatle, sledite tem korakom.

1. Odprite stran za urejanje polja in nato pod **Vrsta**, izberite **Uredi** poleg nabor možnosti.
2. Dodajte novo možnost z oznako in barvo po meri. Če želite dodati nov status časovnega vnosa, se poimenuje polje izven škatle **Status vstopa**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Določitev novega stanja časovnega vnosa kot »samo za branje«
Če želite določiti novo stanje časovnega vnosa kot »samo za branje«, dodajte novo vrednost časovnega vnosa z lastnostjo **Seznam vnosov, ki so na voljo samo za branje**. Ne pozabite dodati številke, ne oznake. Del mreže za vnos časa, ki ga je mogoče urejati, bo zdaj zaklenjen za vrstice, ki imajo nov status. Za nastavitev **Seznam statusov samo za branje** lastnine različno za različne **Vnos časa** ogledov, dodajte **Vnos časa** mreža v pogledu **Kontrole po meri** razdelku in ustrezno konfigurirajte parametre.

Nato dodajte poslovna pravila, da zaklenete vsa polja na **Urejanje vrstice** in **Urejanje časovnega vnosa** strani. Za dostop do poslovnih pravil za te strani odprite urejevalnik obrazcev za vsako stran in nato izberite **Poslovna pravila**. Novo stanje lahko dodate v pogoj obstoječih pravil poslovanja ali pa novemu stanju dodate novo pravilo poslovanja.

### <a name="add-custom-validation-rules"></a>Dodajanje pravil za preverjanje po meri
Dodate lahko dve vrsti pravil za preverjanje veljavnosti za **Tedenski vnos časa** izkušnja mreže:

- Poslovna pravila na strani odjemalca, ki delujejo na straneh
- Preverjanja vtičnikov na strani strežnika, ki veljajo za vse posodobitve časovnih vnosov

#### <a name="client-side-business-rules"></a>Poslovna pravila na strani odjemalca
Uporabite pravila poslovanja za zaklepanje in odklepanje polj, vnesite privzete vrednosti v polja in določite preverjanja, ki potrebujejo le informacije iz trenutnega zapisa časovnega vnosa. Za dostop do poslovnih pravil za stran odprite urejevalnik obrazcev in nato izberite **Poslovna pravila**. Nato lahko urejate obstoječa pravila poslovanja ali dodate novo pravilo poslovanja.

#### <a name="server-side-plug-in-validations"></a>Preverjanja vtičnikov na strani strežnika
Uporabite validacije vtičnikov za vse validacije, ki zahtevajo več konteksta, kot je na voljo v enem zapisu časovnega vnosa. Uporabite jih tudi za morebitne validacije, ki jih želite zagnati pri vgrajenih posodobitvah v mreži. Če želite dokončati preverjanja, ustvarite vtičnik po meri na **Vnos časa** entiteta.

### <a name="limits"></a>Omejitve
Trenutno je **Vnos časa** mreža ima omejitev velikosti 500 vrstic. Če je več kot 500 vrstic, odvečne vrstice ne bodo prikazane. Te omejitve velikosti ni mogoče povečati.

### <a name="copying-time-entries"></a>Kopiranje časovnih vnosov
Uporabite pogled **Kopiraj stolpce časovnih vnosov**, da določite seznam polj, ki jih želite kopirati med vnosom časa. **Datum** in **Trajanje** sta obvezni polji, ki jih ne smete odstraniti iz pogleda.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
