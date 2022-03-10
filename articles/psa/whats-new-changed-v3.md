---
title: Novosti ali spremembe v storitvi Project Service Automation različice 3
description: V tej temi so na voljo informacije o novostih in spremembah v storitvi Project Service Automation različice 3.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: afce9cd2d4b3920dc5de5d3deab8920a7f51f275a73918a84db300739b1b4feb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987096"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Novosti ali spremembe v storitvi Project Service Automation različice 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

V tej temi so na voljo informacije o spremembah uporabniškega vmesnika, funkcij in terminologije v storitvi Project Service Automation med različico 2 ali 1 in različico 3.

## <a name="project-scheduling"></a>Razporejanje projektov
Razpored projektov, ki je v prejšnjih različicah bil znan kot strukturirana členitev dela (SČD), je preimenovan v razpored in do njega lahko dostopate s klikom zavihka **Razpored**. 

![Razpored projektov.](media/psa-schedule-01.png)

Zdaj ima razpored novo središče za interakcijo, ki je tako moderno kot dostopno. Toda temeljni mehanizem za razporejanje storitve Project Service Automation je ostal enak. Krmilni gumbi v traku mreže razporeda omogočajo interakcijo z razporedom, kar je podobno kot v prejšnji različici storitve Project Service Automation. Dodatne spremembe razporeda vključujejo:

- **Ganttov grafikon** – ni več na voljo. Nova Ganttova upodobitev bo na voljo v prihodnji posodobitvi.
- **Glave stolpcev** – glave stolpcev v mreži lahko skrijete tako, da kliknete navzdol usmerjen indikator poleg naslova stolpca. 
- **Stolpci** – skrite stolpce lahko prikažete tako, da kliknete možnost **Dodaj stolpec**. 
- **Kategorija transakcije** – polje za iskanje **Kategorija transakcije** je bilo dodano v mrežo razporeda in je privzeto prikazano. 
 
## <a name="project-templates"></a>Projektne predloge
Pri funkciji projektnih predlog so bile izvedene naslednje spremembe:

### <a name="create-a-project-template"></a>Ustvarjanje projektne predloge 
V različici 3 lahko ustvarite projektno predlogo, kar je podobno kot v prejšnjih različicah storitve Project Service Automation. Predloga lahko vsebuje samo razpored, razpored pa lahko vključuje dodelitve, vendar njihovo vključevanje ni obvezno. Če ima razpored dodelitve, so lahko namenjene samo splošnim virom. Za splošne vire lahko ustvarite zahteve za vire, vendar jih v predlogi ni mogoče rezervirati s pravimi viri. V predlogi ne morete rezervirati pravega vira za ekipo. 

### <a name="create-a-template-from-an-existing-template"></a>Ustvarjanje predloge iz obstoječe predloge
Ko ustvarite novo projektno predlogo iz obstoječe predloge v storitvi Project Service Automation različice 3, se zgodi naslednje: 

- Razpored izvornega projekta se kopira v predlogo. 
- Splošni viri se kopirajo v ekipo in vse dodelitve splošnih virov se prekopirajo. Zahteve za splošne vire niso kopirane. 

### <a name="create-a-template-from-an-existing-project"></a>Ustvarjanje predloge iz obstoječega projekta
Ko ustvarite novo projektno predlogo iz obstoječega projekta, se zgodi naslednje: 

- Razpored izvornega projekta se kopira v predlogo. 
- Splošni viri se kopirajo v ekipo, vse dodelitve splošnih virov pa so ohranjene. Zahteve za splošne vire niso kopirane.    
- Poimenovani viri, dodeljeni ali nedodeljeni, so odstranjeni iz ekipe in zamenjani s splošnimi viri.
- Če so na voljo, so podatki o strankah odstranjeni. 
- Če so na voljo, so sklici na ponudbe in pogodbe odstranjeni. 

### <a name="create-a-project-from-a-template"></a>Ustvari projekt iz predloge
Ko v storitvi Project Service Automation različice 3 ustvarite nov projekt iz predloge, se zgodi naslednje:

- Razpored, ekipa in dodelitve se kopirajo v nov projekt.   
- Začetni datum je datum kopiranja ali datum, ki ga izbere uporabnik.   
- Za splošne člane ekipe, ki imajo zahteve za vire v predlogi, se zahteve ne kopirajo in ne ustvarijo samodejno. Morate jih ustvariti. 

## <a name="copy-a-project"></a>Kopiranje projekta
Ko v storitvi Project Service Automation različice 3 kopirate projekt, se zgodi naslednje: 

- Ocenjeni začetni datum je kopiran, vendar ga je mogoče spremeniti.  
- Razpored projekta in opravila se kopirajo. 
- Splošni viri in njihove dodelitve se kopirajo. Zahteve virov za splošne vire niso kopirane. Morate jih znova ustvariti. 
- Pravi viri in njihove dodelitve se ne kopirajo. Namesto tega so zamenjani s splošnimi viri. 
- Dejanske vrednosti niso kopirane v novi projekt. 

## <a name="move-a-scheduled-project"></a>Premikanje načrtovanega projekta
Ko razpored obstoječega projekta premaknete naprej, se zgodi naslednje: 

- Datumi opravil se zaradi ujemanja z obdobjem premika premaknejo samodejno. 
- Dodeljeni splošni viri ostanejo dodeljeni.   
- Če so ustvarjeni pred premikom projekta, zahteve za splošni vir ostanejo enake in se samodejno ne ustvarijo znova. Znova jih boste morali ustvariti, da bodo odražale nove dodelitve zaradi premikanja opravila. 
- Dodelitve v pravih virih se spremenijo, da ustrezajo premiku datuma opravila. Rezervacije v pravih virih se ne spremenijo. Rezervacije boste morali spremeniti s pogledom za usklajevanje. 
- Viri skupin, ki imajo rezervacije in nimajo dodelitev, se ne spremenijo. 
- Dejanske vrednosti se ne premaknejo. 

## <a name="estimates"></a>Ocene
Ocene so razdeljene na dva zavihka: **Dodelitve virov** in **Ocene**. Zavihek **Dodelitve virov** vsebuje ocene obsega dela in prikazuje dodelitve virov za opravila v časovno razporejenem pogledu. Ocene lahko uredite glede na vrednosti, ki jih ustvari mehanizem za razporejanje.

![Zavihek »Dodelitve virov«, ki prikazuje ocene obsega dela in dodelitve virov za opravila.](media/resource-assignments-tab-02.png)

Zavihek **Ocene** prikazuje zneske stroškov in prodajne zneske za dodelitve virov. Zneski so samo za branje. Zneski stroškov in prodajni zneski zdaj temeljijo na dodelitvah člankov ekipe na razporedu. Če imate opravilo brez dodelitev, to pomeni, da bo opravilo prikazano v nedodeljenem vedru. To pomeni tudi, da brez **vloge**, ki je privzeta cenovna razsežnost, ne bo predvidenih stroškov ali prodaje, če imate kupca ali pogodbo/ponudbo, povezano s projektom. 

![Zavihek »Ocene« , ki prikazuje zneske stroškov in prodajne zneske.](media/estimates-tab-03.png)
  
Kategorija je podprta tudi pri opravilih v pogledu razporeda. Združevanje po kategorijah v časovno razporejenem pogledu ocen bo zagotovilo boljšo izkušnjo, še posebej, če imate v projektu tudi ocene stroškov. Ocene stroškov so vnesene z mrežo na ločenem zavihku. 

Ocene stroškov se lahko vnesejo v mreži na zavihku **Ocene stroškov**. 

![Zavihek »Ocene stroškov«, ki prikazuje mrežo z ocenami stroškov.](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Upravljanje virov
V različici 3 storitve Project Service Automation, ki vključuje nov poenoteni uporabniški vmesnik in spremenjene odnose med rezervacijami in dodelitvami, se je dodelitev osebja za projekt s splošnimi ali pravimi viri precej spremenila glede na različici 2 in 1. Vendar pa so koncepti **pravih** in **splošnih** virov, ki jih je mogoče rezervirati, ostali enaki, tako kot člani ekipe, zahteve, dodelitve in rezervacije.   

![Uporaba izbirnika za vire.](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Dodeljevanje pravega vira, ki ga je mogoče rezervirati 
V različici 3 storitve Project Service Automation pa rezervacije in dodelitve opravil niso tako tesno prepletene kot v prejšnjih različicah storitve Project Service Automation. Mrežo ekipe lahko uporabite, da rezervirate **pravega** člana ekipe, podobno kot na trgu.

Z izbirnikom za vire na razporedu lahko izberete člana ekipe, ki ste ga ustvarili v pogledu ekipe, in ga nato dodelite opravilom. Še naprej mu lahko dodeljujete opravila, tudi mimo njegovih rezervacij. Uporabite zavihek **Uskladitev**, da uskladite člane skupine z razlikami pri rezervacijah in dodelitvah.

Izbirnik za vire bo prikazal člane ekipe za projekt. Izbirnik za vire lahko uporabite tudi za iskanje in ogled drugih virov, ki jih je mogoče rezervirati in niso del projektne ekipe. Vire lahko dodelite opravilu in postali bodo del projektne ekipe. Rezervirati jih morate s **ploščo razporeda** ali z zavihkom **Uskladitev**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Dodeljevanje splošnega vira, ki ga je mogoče rezervirati, v opravilu in projektni ekipi ter nadaljnja izpolnitev s pravim virom prek plošče razporeda 
V storitvi Project Service Automation različice 3 se funkcija za ustvarjanje ekipe ne uporablja za splošne vire. Namesto tega lahko ustvarite in neposredno dodelite splošni vir iz razporeda tako, da v celico vira na razporedu vnesete ime položaja splošnega vira. Lahko pa izberete ikono vira v celici in nato z izbirnikom za vire vnesete ime splošnega vira, ki ga želite ustvariti. Odprla se bo plošča za hitro ustvarjanje, ki vam omogoča, da nastavite vlogo in organizacijsko enoto člana ekipe splošnih virov. Ko ustvarite vir, je dodeljen opravilu in ta splošni vir lahko še naprej dodeljujete drugim opravilom v razporedu.    
 
Ko vir dodelite vsem ustreznim opravilom, lahko ustvarite zahtevo za vir in jo nato izpolnite z neposredno rezervacije prek **plošče razporeda** ali s pošiljanjem zahteve za vir. Splošne vire lahko tudi neposredno dodate v mrežo člana ekipe. 

Dokler se ne ustvari zahteva za vir, so splošni viri dodani projektni ekipi brez zahtev za vire in z začetnimi/končnimi datumi projekta. Če želite ustvariti zahtevo, izberite splošni vir in kliknite **Ustvari**. Prikaže se povezava zahteve in zahtevane ure dela bodo izpolnjene z dodeljenimi urami. Za odpiranje in posodobitev zahteve kliknite povezavo.
  
Ko je rezervacija dokončana in v celoti izpolnjena s poimenovanim virom, se splošni vir zamenja s poimenovanim virom, dodelitev na razporedu pa se posodobi s poimenovanim virom. 

Predlagani viri za zahteve so zdaj shranjeni na zavihku namesto v ločenem razdelku.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Več poimenovanih virov, ki izpolnjujejo splošni vir
Ko je zahteva izpolnjena z več viri, splošni vir ostane v ekipi in dodeljen opravilu. Rezervirani poimenovani člani ekipe niso dodeljeni kot del položaja. Vodja projekta lahko delo po potrebi dodeli pravim virom.  Pogled **Uskladitev** zagotavlja razčlenitev rezervacij v več virih na več dodelitev opravil. To se ne izvede samodejno, ker je v bolj zapletenih scenarijev, npr. ko imate paket opravil, ki sestavljajo zahtevo, treba domnevati način, na katerega želi vodja projekta dodeliti opravila. Ker sistem ne more razumeti tega namena, bodo predpostavke verjetno drugačne od predvidenih in lahko pride do napačnih ali nepredvidljivih rezultatov. Predvidljiv rezultat je, da splošni vir ostane dodeljen, dokler vodja projekta namenoma ne dodeli virov prek pogleda **Uskladitev**.

### <a name="reconciliation"></a>Uskladitev
Zavihek **Uskladitev** prikazuje rezervacije in vse dodelitve za vsakega člana projektne ekipe. Pogled prikazuje ure v celicah, ki lahko predstavljajo časovne točke od mesecev do dnevov. Ta pogled omogoča vodjam projektov, da uskladijo rezervacije članov ekipe in njihove dodelitve za projektno ekipo. To je uporabno, ker rezervacije in dodelitve opravil niso tesno povezane, kar omogoča večjo prilagodljivost pri načrtovanju projekta. 

![Zavihek »Uskladitev«, ki prikazuje rezervacije in dodelitve za člane projektne ekipe.](media/resource-reconciliation-tab-06.png)

Pogled upošteva razliko med rezervacijami člana ekipe in skupno vrednostjo njegovih dodelitev opravil za vsak vir ter prikazuje naslednji razliki, do katerih lahko pride pri rezervacijah in dodelitvah v projektu: 

- **Primanjkljaj rezervacij** – do primanjkljaja rezervacij pride, ko ima vir več dodelitev kot rezervacij. Ker ta zmogljivost ni bila rezervirana, lahko vodja projekta odpravi to napako tako, da razširi rezervacije vira za kritje primanjkljaja. 
- **Odvečne rezervacije** – do odvečnih rezervacij pride, ko je vir rezerviran za projekt, vendar ni bil dodeljen opravilom.  To je lahko sprejemljivo, če je bil vir na primer rezerviran pred dodelitvijo opravila. Vendar v drugih primerih morda vir ni načrtovan za dodeljevanje, vodja projekta pa bi moral razmisliti o preklicu rezervacij vira, da omogoči uporabo zmogljivosti za drug projekt. 

Če imate dodelitve opravil za vir brez rezervacij (primanjkljaj rezervacij), lahko izberete združeni primanjkljaj rezervacij in kliknete možnost **Podaljšaj rezervacijo**. Tukaj si lahko ogledate rezervacijo, ki je potrebna za obravnavo primanjkljaja vira in njegovo razpoložljivost. 
 
## <a name="time-and-expense"></a>Čas in strošek
V tem razdelku so navedene informacije o spremembah časa, stroškov in odobritev v različici 3 storitve Project Service Automation. Kot del rešitve Dynamics 365 Project Service Automation je bila funkcija **Časovni vnos** osvežena za uporabo ogrodja poenotenega vmesnika. To zagotavlja skladen in enoten uporabniški vmesnik, ki sledi odzivnemu oblikovanju za optimalen prikaz na zaslonu poljubne velikosti ali kateri koli napravi. 

### <a name="landing-page"></a>Ciljna stran
Nerazširljiva izkušnja časovnega vnosa po meri je v različici 3 zastarela. Namesto tega je na voljo razširljiva in dostopna izkušnja izvorne mreže. Do funkcije časovnega vnosa lahko dostopate z zemljevidom mesta na levi strani. Zaradi te spremembe ne boste več mogli hkrati vnesti časa za en teden. Namesto tega boste morali ustvariti časovni vnos za vsak dan v mreži. Po ustvarjanju nekaj časovnih vnosov lahko uporabniki množično ustvarjajo časovne vnose s funkcijo **Kopiraj**, kot je razloženo v nadaljevanju te teme. 

![Ciljna stran za časovne vnose.](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Ustvarjanje novih časovnih vnosov 
V traku kliknite možnost **Novo**, da odprete stran za hitro ustvarjanje za časovni vnos, kjer lahko vnesete trajanje v minutah, urah ali dnevih. Če želite to narediti, začnite vnašati »h«, »m« ali »d« skupaj s količino.  

![Hitro ustvarjanje časovnega vnosa.](media/quick-create-time-entry-08.png)

Polja za iskanje so podprta s sistemskimi pogledi. Ko na primer vnesete podatke o projektu, je polje **Projektno opravilo** privzeto nastavljeno na pogled **Moja odprta projektna opravila**. Če želite ustvariti časovne vnose za opravila, ki niso dodeljena uporabniku, v iskalnem polju kliknite **Spremeni pogled** in izberite možnost **Vsa dejavna projektna opravila**. Ko je časovni vnos ustvarjen in prikazan v mreži, lahko vse vrednosti vrstice uredite neposredno v mreži.  

### <a name="bulk-createcopy"></a>Množično ustvarjanje/kopiranje 
Ko ustvarite nekaj časovnih vnosov, lahko uporabite funkcijo kopiranja za množično ustvarjanje dodatnih časovnih vnosov. Za odpiranje pogovornega okna **Kopiranje** kliknite možnost **Kopiraj**. V možnosti **Od obdobja: začetni datum** nastavite datumski obseg, iz katerega bodo kopirana časovna obdobja. V možnosti **Do obdobja: začetni datum** določite datum, za katerega je treba ustvariti časovne vnose. Kliknite **Kopiraj**, da časovne vnose kopirate v ustrezen dan v tednu, ki je označen v možnosti **Do obdobja**. Ponedeljkov časovni vnos iz prejšnjega tedna bo kopiran v ponedeljek za teden, ki je označen v možnosti **Do obdobja**. 

![Množično kopiranje časovnih vnosov.](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Uvažanje podatkov 
Dodelitve in izmenjava sledijo istemu vzorcu uporabniškega vmesnika, kar uporabniku omogoča, da določi datumski obseg, iz katerega je treba uvoziti rezervacije. Nato morate posebej izbrati rezervacije, ki jih želite kopirati v časovne vnose **Osnutek**. V različici 3 ni mogoče videti vzorca **predlaganih** časovnih vnosov v mreži in koledarju.  

### <a name="change-in-calendar-control"></a>Spremembe kontrolnika za koledar
V različici 3 ni več v uporabi kontrolnik za koledar po meri; uvedli smo koledar UC za prikazovanje časovnih vnosov za teden. S tem koledarjem si lahko ogledate dan, teden in mesec. 

> [!NOTE]
> Koledar je omejen, ker ta kontrolnik ne podpira dejanj v posameznih elementih koledarja. Ne boste na primer mogli izbrati enega ali več elementov koledarja in jih poslati ali izbrisati. Če kliknete element koledarja, se za dodatna dejanja odpre stran **Entiteta časovnih vnosov**. 

### <a name="extensibility"></a>Razširljivost
**Beleženje podatkov iz polj po meri samo v entiteti časovnih vnosov in entiteti vnosov stroškov** – časovni vnos uporablja mrežo za branje, ki jo je mogoče urejati, in kontrolnike za koledar iz platforme. Vsi kontrolniki so izvorni in zato podpirajo prilagoditve. V različici 3 storitve Project Service Automation lahko dodajate dodatna polja po meri, nastavljate polja za iskanje in jih varnostno kopirate s pogledi po meri. Lahko nastavite tudi poslovno logiko po meri na podlagi izbranih vrednosti v poljih po meri.  

**Beleženje podatkov iz polj po meri v časovnih vnosih in vnosih stroškov ter njihovo posredovanje prek entitet, ki podpirajo potek pošiljanja in odobritve** – običajna obdelava časovnih vnosov je prikazana v spodnjem diagramu.

![Obdelava poteka časovnih vnosov.](media/process-time-entries-10.png)

Če poslovne zahteve določajo, da morata entiteta časovnih vnosov in entiteta stroškov zajeti cenovne razsežnosti po meri in razširiti vrednosti, ki so nastavljene z virom časa in vnosa v cenovni razsežnosti po meri, v vseh entitetah iz prejšnjega grafičnega prikaza, glejte temo [Nastavitev polj po meri kot cenovnih razsežnosti](set-up-pricing-dimensions.md).

Za podpiranje poslovnih zahtev, pri katerih morata entiteta časovnih vnosov in entiteta stroškov zajemati razsežnosti po meri, ki niso cenovne, in razširjati vrednosti, lahko uporabite nastavitev cenovnih razsežnosti in razsežnosti po meri določite kot cenovne razsežnosti brez mere stroškov ali obračunske stopnje. Lahko pa vsaki entiteti dodate polje po meri, pri čemer v vseh entitetah uporabite isto ime polja. Če želite povezati zapise v entitetah, ki sodelujejo v poteku pošiljanja/odobritve, lahko z entiteto izvora transakcije in entiteto povezave transakcije ustvarite vtičnike po meri.  

### <a name="delegate-time-and-expense-entry"></a>Pooblastitve za vnos časa in stroškov
Platforma Common Data Service ne podpira uporabnika, ki pooseblja drugega, kar pomeni, da v različici 3 storitve Project Service Automation ni mogoče določati pooblastitev za vnos časa in stroškov. Vendar so partnerji in stranke izkoristili rešitev, da omogočijo podporo za izkušnje pooblastitev za časovne vnose v različici 3. To ni samo začasna rešitev, in ne dokončna, zato je pomembno, da razumete omejitve in ta pristop uporabite le, če so omejitve sprejemljive. 

> [!IMPORTANT]
> Te informacije obravnavajte le kot predlagane smernice za izvedbo po meri partnerja/stranke. Ekipa za izdelka ne bo zagotavljala uradne podpore za to funkcijo prek nobenega od naših kanalov za podporo.

### <a name="customization-details"></a>Podrobnosti o prilagajanju 
Prilagajanje omogoča dodajanje **Vira, ki ga je mogoče rezervirati** v izkušnje ustvarjanja in urejanja, kar bo uporabniku omogočilo, da deluje kot pooblaščenec tako, da polje **Vir, ki ga je mogoče rezervirati** dodeli drugemu uporabniku, za katerega je treba zabeležiti vnose časa in stroškov. Naslednji koraki zajemajo pooblaščanje za časovne vnose. Isti podatki veljajo za pooblastitve vnosov stroškov. 
 
1.  Prepričajte se, da pooblaščeni uporabnik ima globalni varnostni dostop do projektov in projektnih opravil. 
1.  Ker polje **Vir, ki ga je mogoče rezervirati** v entiteti **Časovni vnos** ni prikazano na strani za **hitro ustvarjanje**, ga morate dodati.

    –ali–

    Če si želite ogledati samo časovne vnose, ustvarjene za vir, ustvarite pogled po meri, ki vključuje stolpec **Vir, ki ga je mogoče rezervirati**. Objavite prilagoditve oblikovalnika modula aplikacije za ta pogled, da se prikaže v možnosti **Izbirnik pogledov** na strani **Časovni vnosi**. Obstajata dva vtičnika, ki obravnavata nastavitev vodje za časovne vnose, ki niso povezani s projektom:

    - »PreValidateTimeEntryCreate«
    - »PreValidateTimeEntryUpdate«
 
1. Ustvarite nov vtičnik, da prepišete polje **Vodja** z vodjo uporabnika, ki je dodeljen v polju **Vir, ki ga je mogoče rezervirati**. Uporabite isto **stopnjo izvedbe** kot vtičnik zunaj pasu (OOB) (pred preverjanjem veljavnosti) in **Vrstni red izvedbe**, ki je na višji ravni kot vtičniki OOB (več kot 1). S tem boste zagotovili, da se vtičnik po meri izvede po vtičnikih OOB.  
 
### <a name="end-user-experience"></a>Izkušnja končnega uporabnika
1.  Ko ustvarite časovni vnos na strani za hitro ustvarjanje, vnesite podrobnosti o projektu in projektnem opravilu ter nato izberite uporabnika v polja **Vir, ki ga je mogoče rezervirati**, za katerega želite zabeležiti časovne vnose. 
2.  Privzeta vrednost za to polje je prijavljeni uporabnik, toda glede na to, da je uporabnik preglasil to polje, je časovni vnos zdaj ustvarjen za izbrani **Vir, ki ga je mogoče rezervirati**.
3.  Ko pošljete časovne vnose, ki ste jih ustvarili za te zapise, bodo vnosi v skladu s pričakovanji v čakalni vrsti odobritelja v projektu. 
4.  Ko časovne vnose, ustvarjene za drugega uporabnika, prekličete, bodo vrnjeni v stanje **Osnutek** s poljem **Vir, ki ga je mogoče rezervirati**, ki je nastavljeno za drugega uporabnika. 
5.  Izbirno lahko preklopite na pogled po meri, da filtrirate časovne vnose, ustvarjene za drugega uporabnika. 
 
### <a name="limitations"></a>Omejitve
Funkcija za **kopiranje** in **uvoz** deluje samo v okviru prijavljenega uporabnika. To pomeni, da časovnih vnosov ni mogoče kopirati ali izvoziti, če so ustvarjeni za uporabnika, ki je prijavljen kot vir, ki ga je mogoče rezervirati.

Časovni vnosi, ki niso za projekt, bodo usmerjeni v odobritev k vodji vira, ki ga je mogoče rezervirati, samo če ste izvedli korak 4 iz zgornjega razdelka **Podrobnosti o prilagajanju**. Sicer bodo časovni vnosi, ki niso del projekta, za drugega uporabnika neustrezno usmerjeni k vodji prijavljenega uporabnika. 

### <a name="other-changes"></a>Druge spremembe 
Funkcija **Rezervacije in opravila** je odstranjena. 

## <a name="multidimensional-pricing"></a>Večdimenzionalno oblikovanje cen
Za večjo prilagodljivost in izpolnjevanje različnih poslovnih zahtev je v različici 3 aplikacije Project Service Automation podprta ločena uporaba naborov cenovnih razsežnosti za mere stroškov in deleže obračunavanja. Vrednosti razsežnosti je mogoče nastaviti kot privzete in jih nato razširiti v postopku razčlenitve stroškov in oblikovanja cen: od profiliranja virov prek časovnih vnosov do projektnih dejanskih vrednosti. Konfiguracije in spreminjanja ali razširitve, značilne za stranko, uporabljajo standardno infrastrukturo prilagoditev.

Storitev Project Service Automation vključuje privzet nabor cenovnih razsežnosti, vlog in enot virov ter omogoča nastavitev cen in stroškov za vsako kombinacijo vlog in organizacijskih enot.

Za stranke storitve Project Service Automation, ki želijo še naprej uporabljati ta vnaprej pripravljena polja kot cenovne razsežnosti v različici 3, ni nobene opaznejše spremembe. Project Service Automation lahko še naprej uporabljate kot običajno. Če pa morate zagotoviti ceno ali strošek za svoje vire z drugimi dodatnimi atributi, vam različica 3 omogoča dodajanje lastnih cenovnih razsežnosti v storitev Project Service Automation. Razširitev cenovnih razsežnosti po meri je zapletena izkušnja konfiguracije. 

## <a name="quotes-and-contracts"></a>Ponudbe in pogodbe
V različici 3 storitve Project Service Automation so spremenjeni vidiki nastavitev in upravljanja ponudb in pogodb. Podrobnejše informacije so navedene v naslednjih razdelkih.

### <a name="set-up-chargeability-options"></a>Nastavitev možnosti zaračunavanja
V različicah 1 in 2 je bila nastavitev možnosti zaračunavanja za vloge in kategorije za posebne ponudbe in pogodbe opravljena s pogledom **Možnosti zaračunavanja**, ki je bil v zgornji vrstici za krmarjenje po vrstici ponudbe ali podrobnostih pogodbe. V tej možnosti je bilo mogoče nastaviti tudi cene za vloge in kategorije stroškov.

Od različice 3 bo nastavitev možnosti zaračunavanja po vlogi in kategoriji stroškov opravljena na stopnji vrstice ponudbe ali podrobnosti pogodbe. Nastavitev cen in nastavitev možnosti zaračunavanja sta ločeni. Zavihka **Vloge, ki se zaračunajo** in **Kategorije, ki se zaračunajo** lahko najdete na straneh **Vrstica ponudbe** in **Podrobnosti pogodbe**, pri čemer vam ni treba uporabljati zgornje vrstice za krmarjenje.

![Vloge, ki se zaračunajo.](media/chargeable-12.png)
 
Nastavitev vlog in kategorij, ki se zaračunajo, se uporablja tudi pri vnaprej pripravljenem kontrolniku za mrežo, ki jo je mogoče urejati. Za vsako vlogo in kategorijo ostanejo podprte možnosti za vrsto obračunavanja med fazo oblikovanja ponudb in sklepanja pogodb nespremenjene glede na prejšnje različice, **Se zaračuna** in **Se ne zaračuna**. Vrsta **Brezplačno** ni podprta med fazo oblikovanja ponudb in sklepanja pogodb. Vrsta **Brezplačno** je podprta samo med odobritvijo časa ali stroškov.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Ustvarjanje in urejanje cen po meri za ponudbo in projektno pogodbo storitve Project Service Automation
V različicah 1 in 2 je bila uporaba cenika po meri za določene ponudbe in pogodbe izvedena s funkcijo **Urejanje cen** iz pogleda **Možnosti zaračunavanja**. Pogled **Možnosti zaračunavanja** je bil prikazan v zgornjo vrstici za krmarjenje po vrstici ponudbe ali podrobnostih pogodbe. V tej možnosti je bilo mogoče nastaviti tudi možnosti zaračunavanja za vloge ali kategorije stroškov.

Od različice 3 sta ustvarjanje in uporaba cenika projekta po meri v ponudbi storitve Project Service Automation in projektni pogodbi storitve Project Service Automation ločena od nastavitve možnosti zaračunavanja. Ponudba storitve Project Service Automation in projektne pogodbe storitve Project Service Automation imajo nov zavihek, imenovan **Projektni ceniki**. Ta zavihek prikazuje povezan pogled vseh projektnih cenikov, ki so priloženi ponudbi ali projektni pogodbi storitve Project Service Automation. Če želite ustvariti cenik po meri iz obstoječega cenika, ki je že povezan s projektno ponudbo ali pogodbo, kliknite možnost **Ustvari cenik po meri**. S tem boste kopirali vse povezane cenike in jih priložili ponudbi ali pogodbi. Zdaj lahko cenik odprete in uredite vlogo ali ceno kategorije stroškov, da bodo te spremembe cen veljale samo za to ponudbo ali pogodbo. 
  
Naslednji grafični prikaz je prikaz pred ustvarjanjem cenikov po meri.

![Pred ustvarjanjem cenikov po meri.](media/before-custom-price-lists-13.png)

Naslednji grafični prikaz je prikaz po ustvarjanju cenikov po meri.

![Po ustvarjanju cenikov po meri.](media/after-custom-price-lists-14.png)

> [!NOTE]
> Lahko pride do krajšega zamika med klikom možnosti **Ustvari cenik po meri** in ustvarjanjem cenika po meri. Priporočamo, da namesto večkratnih klikov osvežite mrežo. Cenik po meri je ustvarjen, če ima ime povezanega cenika priloženo ime ponudbe ali projektne pogodbe.


[!INCLUDE[footer-include](../includes/footer-banner.md)]