---
title: Prilagajanje tedenskih vnosov
description: Ta tema vsebuje informacije o izvajanju pravil poslovanja po meri, ki sledijo poslovnim praksam organizacije.
author: stsporen
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cc395e77e987dac062251ef87fcf8295305178e2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084843"
---
# <a name="customize-weekly-time-entry"></a>Prilagajanje tedenskih vnosov 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V aplikaciji Microsoft Dynamics 365 Project Service Automation različice 3.3 je Microsoft uvedel moderno mrežo, s katero lahko projektni viri hitro vnesejo čas za en teden naenkrat. Nova tedenska mreža časovnih vnosov lahko prikaže vse vnose, filtrirane po datumu, vrsticah ali tednih. Viri lahko kopirajo časovne vnose znotraj enega tedna in množično kopirajo vnose iz prejšnjih tednov. Prilagojevalci sistema lahko prilagodijo pogled z dodajanjem polj, dodajanjem možnosti iskanja drugim entitetam in izvajanjem pravil poslovanja po meri, ki sledijo poslovni praksi njihove organizacije.

Dostop do mreže časovnih vnosov in nove tedenske časovne mreže je omogočen prek zemljevida mesta. Nerazširljiv časovni vnos po meri, ki je bil vključen v prejšnje različice PSA, je bil nadomeščen z razširljivo tedensko mrežo časovnih vnosov in alternativno izkušnjo v mreži in koledarju, ki sta na voljo samo za branje. Ta sprememba uporabnikom omogoča vnos časa v tednih.

## <a name="page-layout"></a>Postavitev strani
Nova tedenska mreža časovnih vnosov je po meri ustvarjen kontrolnik, ki ima orodno vrstico in dva glavna razdelka – **Razsežnosti** in **Trajanje**. V orodni vrstici je gumb, ki se uporablja samo za ta kontrolnik po meri za mrežo časovnih vnosov. Nasprotno pa se gumbi v podoknu za dejanja na vrhu strani uporabljajo za vse tri vrste kontrolnikov, ki so podprti za časovni vnos: kontrolnik za tedenski časovni vnos, kontrolnik za vnose, ki so na voljo samo za branje, in kontrolnik koledarja.

### <a name="dimensions"></a>Razsežnosti
V razdelku **Razsežnosti** so v obliki naslova stolpca prikazane vse razsežnosti, ki jih je mogoče uporabiti za vnos časa. Vnaprej so podprte spodaj navedene razsežnosti:

- Project
- Projektno opravilo
- Vloga
- Vrsta
- Stanje vnosa

V razdelku **Razsežnosti** urejanje v vrstici ni mogoče. Ta razdelek je podprt s pogledom, ki omogoča dodajanje polj po meri v tedensko mrežo časovnih vnosov. Za več informacij o dodajanju polj po meri si oglejte razdelek »Razširljivost« v nadaljevanju te teme.

### <a name="duration"></a>Trajanje
Razdelek »Trajanje« prikazuje dneve v tednu kot glave stolpcev. Ta razdelek omogoča urejanje v vrstici. Ko je ustvarjena vrstica za časovni vnos z ustreznimi razsežnostmi, lahko uporabniki v vrstico hitro vnesejo količino časa, ki so ga porabili za te razsežnosti.

## <a name="create-a-new-time-entry"></a>Ustvarjanje novega časovnega vnosa
Če želite ustvariti nov časovni vnos v mreži časovnih vnosov, izberite **Novo**. Prikaže se pogovorno okno **Hitro ustvarjanje časovnega vnosa**. V tem pogovornem oknu lahko uporabniki izberejo datum časovnega vnosa in nato vnesejo podatke za **Projekt** , **Projektno opravilo** , **Vlogo** in **Trajanje** razsežnosti v minutah, urah ali dneh, tako da vnesejo vrednosti **h** , **m** ali **d** skupaj s številko. Uporabniki lahko vnesejo tudi opis in komentarje za časovni vnos, ki jih je mogoče dati v skupno javno rabo. Ko uporabniki shranijo spremembe, se njihove vnesene vrednosti za razsežnosti prikažejo v razdelku **Razsežnosti**. Informacije o trajanju, ki so jih vnesli v polje **Trajanje** , se prikažejo v tistem datumu, za katerega je bil ustvarjen časovni vnos.

Polja za iskanje so podprta s sistemskimi pogledi. Ko uporabnik na primer vnese projekt, se polje **Projektno opravilo** privzeto nastavi na pogled **Kopiraj**. Če želite ustvariti časovne vnose za opravila, ki niso dodeljena uporabniku, v pogovornem oknu za iskanje izberite **Spremeni pogled** in nato še pogled **Vsa dejavna projektna opravila**.

## <a name="edit-a-time-entry"></a>Urejanje časovnega vnosa
Podrobnosti iz nekaterih polj na strani časovnega vnosa, kot so **Opis** in **Zunanji komentarji** , niso prikazane v tedenski mreži časovnih vnosov. Namesto tega se v celicah za trajanje, ki imajo te dodatne podrobnosti, pojavi majhen trikotni kazalnik. Izberite celico in nato še možnost **Uredi podrobnosti** , da si ogledate podatke v podoknu **Hitro urejanje**. Če želite urediti ali posodobiti podrobnosti določenega časovnega vnosa, ki ni del tedenske mreže časovnih vnosov, morajo uporabniki odpreti podokno **Hitro urejanje**.

## <a name="copy-a-time-entry-row"></a>Kopiranje vrstice časovnega vnosa
Po tem, ko je ustvarjena prva vrstica časovnega vnosa, lahko uporabniki izberejo možnost **Kopiraj vrstico** , če želijo kopirati celotno vrstico v novo vrstico. Ko vrstico kopirate na ta način, se pri tem kopirajo tudi razsežnosti in trajanje. Uporabniki lahko izberejo tudi možnost **Uredi vrstico** , da posodobijo vrednosti razsežnosti in trajanja v vrstici razdelka **Trajanje**.

## <a name="open-a-time-entry"></a>Odpiranje časovnega vnosa
Za podporo optimalnega in hitrega vnašanja v najbolj uporabljenih poljih je v tedenski mreži časovnih vnosov prikazana podmnožica izbranih razsežnosti in časovnih obdobij. Če si želite ogledati vse podrobnosti posameznega časovnega vnosa, v razdelku **Urejanje vnosa** izberite **Odpri**.

## <a name="submit-a-time-entry"></a>Pošiljanje časovnega vnosa
Uporabniki lahko pošljejo en sam časovni vnos ali skupino časovnih vnosov, tako da izberejo blok celic ali celotno vrstico časovnega vnosa in nato izberejo **Pošlji**. Poslani časovni vnosi se prikažejo kot vnosi, ki čakajo na odobritev na strani potrjevalcev za **Odobritev**. Ko so časovni vnosi uspešno poslani, jih ni več mogoče urejati.

## <a name="recall-a-time-entry"></a>Preklic časovnega vnosa
Poslane časovne vnose lahko tudi prekličete. Prekličete lahko posamezen časovni vnos, blok časovnih vnosov ali celotno vrstico časovnih vnosov. Viri lahko urejajo preklicane časovne vnose.

## <a name="time-entry-status"></a>Stanje časovnega vnosa
Novim časovnim vnosom je samodejno dodeljeno stanje **Osnutek**. Ko je časovni vnos poslan, se stanje posodobi na **Poslano**. Ko je poslan časovni vnos odobren, se stanje posodobi na **Odobreno**. Če je časovni vnos zavrnjen, se stanje posodobi na **Vrnjeno** , vnos pa je nato mogoče popraviti in ponovno poslati. Izbrisati je mogoče le časovne vnose s stanjem **Osnutek**.

## <a name="view-rejection-comments"></a>Ogled komentarjev ob zavrnitvi
Ko potrditelj zavrne časovni vnos, lahko potrditelj komentira zavrnitev, da bi vir lažje razumel njen razlog. Če si želite ogledati komentar zavrnitve časovnega vnosa, izberite **Odpri vnos**. Komentarji zavrnitve bodo prikazani na časovnici. Na časovnici se lahko vir odzove na komentarje o zavrnitvi, preden ponovno pošlje vnos.

## <a name="copy-week"></a>Kopiraj teden
Ko ustvarijo nekaj časovnih vnosov, lahko uporabniki izberejo funkcijo **Kopiraj teden** za množično ustvarjanje dodatnih časovnih vnosov. Prikaže se pogovorno okno **Kopiraj**. V razdelku **Od obdobja** uporabite polji **Začetni datum** in **Končni datum** , da določite datumski obseg za kopiranje časovnih vnosov. V razdelku **Do obdobja** v polju **Začetni datum** določite datum, za katerega želite ustvariti časovne vnose. Nato izberite **Kopiraj**. V razdelku »Do obdobja« se za izbran datum ustvari kopija časovnih vnosov za ustrezen dan v tednu v razdelku »Od obdobja«. Ponedeljkov časovni vnos iz prejšnjega tedna bo kopiran v ponedeljek za teden, ki je označen kot možnost »Do obdobja«.

## <a name="import"></a>Uvoz
Isti osnovni postopek se uporablja za uvoz iz rezervacij, dodelitev in izmenjav. Uporabniki lahko določijo datumski obseg, iz katerega so uvožene rezervacije. Nato morajo posebej izbrati rezervacije, ki jih želijo kopirati v osnutke časovnih vnosov. V prejšnji izdaji so se časovni vnosi prikazali v mreži in koledarju in se nato po osveževanju seje izgubili.

## <a name="extensibility"></a>Razširljivost
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Dodajanje polj po meri, ki imajo možnost iskanja po drugih entitetah
Za dodajanje polja po meri v tedensko mrežo časovnih vnosov je treba izvesti tri glavne korake.

1.  Dodajte polje po meri v pogovorno okno za hitro ustvarjanje.
2.  Konfigurirajte mrežo tako, da prikazuje polja po meri.
3.  Dodajte polje po meri bodisi na potek opravila za urejanje vrstice bodisi na potek opravila za urejanje celice, kar je ustrezneje.

Prav tako morate zagotoviti, da ima novo polje zahtevano preverjanje v poteku opravila za urejanje vrstic ali celic. Kot del tega koraka morate zakleniti polje na podlagi stanja časovnega vnosa.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodajanje polja po meri v pogovorno okno za hitro ustvarjanje
Polje po meri morate dodati v pogovorno okno Hitro ustvarjanje, Ustvari časovni vnos. To storite zato, da lahko uporabniki vnesejo vrednosti, ko dodajajo časovne vnose z gumbom **Novo**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfiguriranje mreže za prikaz polja po meri
Za dodajanje polja po meri v tedensko mrežo časovnih vnosov obstajata dva načina. Prvi način je tak, da prilagodite pogled **Moji tedenski časovni vnosi** in mu dodate polje po meri. Izberete lahko položaj in velikost polja po meri v mreži, tako da uredite te lastnosti v pogledu.

Druga možnost je ta, da ustvarite nov pogled časovnih vnosov po meri in ga nastavite kot privzeti pogled. Ta pogled mora poleg stolpcev, ki jih želite imeti v mreži, vsebovati še polja **Opis** in **Zunanji komentarji**. Izberete lahko položaj, velikost in privzeto zaporedje razvrščanja mreže, tako da uredite te lastnosti v pogledu. Nato konfigurirajte kontrolnik po meri za ta pogled, da bo nastavljen na **Mreža časovnih vnosov**. Ta kontrolnik dodajte v pogled in ga izberite za splet, telefon in tablični računalnik. Nato konfigurirajte parametre za tedensko mrežo časovnih vnosov. Nastavite polje **Začetni datum** na **msdyn_date** , polje **Trajanje** na **msdyn_duration** in polje **Stanje** na **msdyn_entrystatus**. V privzetem pogledu je polje **Seznam vnosov s stanjem samo za branje** nastavljeno na **192350002,192350003,192350004** , polje **Potek opravila urejanja vrstice** na **msdyn_timeentryrowedit** in polje **Potek opravila urejanja celice** na **msdyn_timeentryedit**. Ta polja lahko prilagodite, če želite dodati ali odstraniti stanje samo za branje ali uporabiti drugačno izkušnjo na podlagi opravila (TBX) za urejanje vrstic ali celic. Ta polja morajo biti vezana na statično vrednost.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Dodajanje polja po meri ustreznemu poteku opravila za urejanje
Strani TBX, ki se uporabljajo za urejanje, je mogoče najti v razdelku **Procesi**. Privzete strani so **Project Service – Urejanje vrstice časovnega vnosa** in **Project Service – Urejanje časovnega vnosa**. Te privzete strani lahko ali urejate ali ustvarite nove strani TBX po meri.

> [!NOTE] 
> Z obema načinoma boste odstranili nekaj vnaprej nastavljenih filtrirnih možnosti v entitetah **Projekt** in **Projektna opravila** , da bodo vidni vsi pogledi za iskanje po entitetah. Med vnaprej pripravljenimi pogledi so vidni le ustrezni pogledi za iskanje.

Določiti morate ustrezen potek opravila za polje po meri. Če ste polje dodali v mrežo, bi se moralo najverjetneje prikazati v poteku opravila za urejanje vrstice, ki se uporablja za polja, ki veljajo za celotno vrstico časovnih vnosov. Če ima polje po meri vsak dan drugačno vrednost, tako kot na primer polje po meri za **Končni čas** , bi moralo iti v potek opravila za urejanje celic.

Če želite dodati polje po meri v potek opravila, povlecite element **Polje** v ustrezen položaj na strani in nato nastavite njegove lastnosti. Nastavite lastnost **Vir** na **Časovni vnos** in nato nastavite še lastnost **Podatkovno polje** v polje po meri. Lastnost **Polje** označuje prikazno ime na strani TBX. Izberite možnost **Uporabi** , da shranite spremembe v polju. Nato izberite možnost **Posodobi** , da shranite spremembe na strani.

Če želite namesto tega uporabiti novo stran TBX po meri, ustvarite nov proces. Nastavite kategorijo na **Potek poslovnega procesa** , entiteto na **Časovni vnos** in nato še vrsto poslovnega procesa na **Zaženi proces kot potek opravila**. V razdelku **Lastnosti** mora biti lastnost **Ime strani** nastavljena na prikazno ime strani. Dodajte vsa ustrezna polja na stran TBX. Shranite in zaženite proces ter posodobite lastnost kontrolnika po meri za ustrezen potek opravila v vrednost **Ime** za izbrani postopek.

### <a name="add-new-option-set-values"></a>Dodajanje novih vrednosti iz nabora možnosti
Če želite dodati vrednosti iz nabora možnosti v vnaprej nastavljeno polje, odprite stran za urejanje polja in nato pod **Vrsta** ob naboru možnosti izberite **Uredi**. Nato dodajte novo možnost z oznako in barvo po meri. Če želite dodati novo stanje časovnega vnosa, je pravilno ime vnaprej pripravljenega polja **Stanje vnosa** in ne **Stanje**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Določitev novega stanja časovnega vnosa kot »samo za branje«
Če želite določiti novo stanje časovnega vnosa kot »samo za branje«, dodajte novo vrednost časovnega vnosa (številko, ne oznako) v lastnost **Seznam vnosov, ki so na voljo samo za branje**. Del mreže časovnih vnosov, ki ga je mogoče urejati, bo zaklenjen za vrstice z novim stanjem.
Nato dodajte pravila poslovanja, da zaklenete vsa polja v straneh TBX **Urejanje vrstice časovnega vnosa** in **Urejanje časovnega vnosa**. Do pravil poslovanja za te strani lahko dostopate tako, da odprete urejevalnik poteka poslovnega procesa za to stran in izberete **Pravila poslovanja**. Novo stanje lahko dodate v pogoj obstoječih pravil poslovanja ali pa novemu stanju dodate novo pravilo poslovanja.

### <a name="add-custom-validation-rules"></a>Dodajanje pravil za preverjanje po meri
Obstajata dve vrsti pravil za preverjanje, ki jih lahko dodate izkušnji tedenske mreže časovnih vnosov: •   pravila poslovanja v odjemalcu, ki delujejo v pogovornih oknih za hitro ustvarjanje in na straneh TBX •   preverjanja vtičnika v strežniku, ki veljajo za vse posodobitve časovnih vnosov

#### <a name="business-rules"></a>Pravila poslovanja
Uporabite pravila poslovanja za zaklepanje in odklepanje polj, vnesite privzete vrednosti v polja in določite preverjanja, ki potrebujejo le informacije iz trenutnega zapisa časovnega vnosa. Do pravil poslovanja za stran TBX lahko dostopate tako, da odprete urejevalnik poteka poslovnega procesa za to stran in izberete **Pravila poslovanja**. Nato lahko urejate obstoječa pravila poslovanja ali dodate novo pravilo poslovanja. Za večjo izbiro prilagojenih preverjanj lahko uporabite pravilo poslovanja za zagon JavaScript.

#### <a name="plug-in-validations"></a>Preverjanja vtičnika
Uporabite preverjanje vtičnika za vsa preverjanja, ki zahtevajo več konteksta, kot je na voljo za posamezen zapis časovnega vnosa, ali vsa preverjanja, ki jih želite zagnati v posodobitvah znotraj vrstic v mreži. Če želite dokončati preverjanje, ustvarite vtičnik po meri v entiteti **Časovni vnos**.

> [!IMPORTANT] 
> Trenutno je na straneh TBX znana težava, ki uporabnikom preprečuje popravljanje informacij in ponovno izbiranje možnosti »Opravljeno«, ko posodobitev ne izvede preverjanja vtičnika. Kot rešitev lahko nastavite preverjanja pravil poslovanja, da to preprečite v čim večji meri.
