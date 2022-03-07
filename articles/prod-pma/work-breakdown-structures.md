---
title: Pregled strukturirane členitve dela
description: Strukturirana členitev dela (SČD) je opis dela, ki bo opravljeno za projekt. Gre za hierarhijo opravil, ki predstavlja razumevanje projektne skupine glede sestave dela ter velikosti, stroškov in trajanja vsake komponente ali opravila.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 093f9901aec0db1fa8f920533c0084f877f26445fd07159e8e1ae0cf53849641
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998841"
---
# <a name="work-breakdown-structures-overview"></a>Pregled strukturirane členitve dela

[!include [banner](../includes/banner.md)]

Strukturirana členitev dela (SČD) je opis dela, ki bo opravljeno za projekt. Gre za hierarhijo opravil, ki predstavlja razumevanje projektne skupine glede sestave dela ter velikosti, stroškov in trajanja vsake komponente ali opravila. SČD ima tri glavne namene:

-   Opis razčlenitve ali sestave dela pri opravilih.
-   Načrtovanje dela na projektu.
-   Ocenitev stroškov posameznega opravila.

Stopnja podrobnosti v vmesniku SČD je odvisna od ravni natančnosti, ki se zahteva v ocenah, in ravni sledenja, ki se zahteva glede na te ocene. Projekti, ki imajo zelo nizko toleranco do zamud po urniku ali odmik od predvidenih stroških, običajno zahtevajo podrobnejši vmesnik SČD in natančnejše sledenje napredku dela in stroškom glede na vmesnik SČD. Takšni projekti so pogosti v gradbeni in inženirski industriji. 

Nasprotno pa so projekti v določenih panogah (npr. mediji in oglaševanje, programska oprema in informacijska infrastruktura) običajno edinstveni, produktivnost pa je odvisna od izkušenj in usposobljenosti posameznika, ki opravlja opravilo. Zato te industrije uporabljajo vmesnik SČD, da dobijo približek velikosti projekta, ne da bi podrobno spremljale napredek tega projekta. 

Izdelava vmesnika SČD je intenziven postopek, ki se običajno izvaja v daljšem obdobju in zahteva sodelovanje in informacije najrazličnejših ljudi. Ta tema opisuje, kako lahko z izboljšavami vmesnika SČD izpolnite svoje zahteve za ocene in sledenje.

## <a name="prerequisites-for-creating-a-wbs"></a>Predpogoji za ustvarjanje vmesnika SČD
Če želite ustvariti vmesnik SČD, morate biti sposobni ustvariti delovni urnik in oceniti stroške dela.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Predpogoji za ustvarjanje delovnega urnika

Če želite uporabiti celotne zmogljivosti vmesnika SČD za načrtovanje, dokončajte naslednjo nastavitev:

1.  Nastavite privzeti koledar in koledar projekta:
    1.  Pomaknite se v razdelek **Vodenje projekta in računovodstvo** &gt; **Nastavitve** &gt; **Vodenje projekta in računovodski parametri** &gt; **Načrtovanje**. V polju **Privzeti delovni koledar** določite privzeti koledar. To bo privzeti delovni koledar za vsak nov projekt, ki je ustvarjen.
    2.  Privzeti koledar lahko spremenite za določen projekt. Kliknite stran s podrobnostmi o projektu in nato na hitrem dostopu **Projektna ekipa in načrtovanje** posodobite polje **Koledar za načrtovanje** tako, da izberete drug koledar.

2.  Nastavite običajne delovne dni in delovni čas. Koledar, ki ste ga za projekt nastavili kot delovni koledar, bo v vmesniku SČD uporabljen za določitev naslednjih informacij:

-   Delovni dnevi in prazniki
-   Število delovnih ur v dnevu

Če želite nastaviti delovne dni in delovne ure za koledar ali ustvariti nov koledar, se pomaknite v razdelek **Uprava organizacije** &gt; **Splošno** &gt; **Koledarji**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Predpogoji za ocenjevanje stroškov dela

Če želite uporabiti zmogljivosti vmesnika SČD za ocenjevanje celotnih stroškov, nastavite stroške in prodajne cene za delavce, kategorije dela, stroške in pristojbine ter izdelke.

-   Če želite nastaviti stroške in prodajno ceno dela ter kategorije stroškov in pristojbin, kliknite možnost **Vodenje projekta in računovodstvo** &gt; **Nastavitev** &gt; **Cene**.
-   Za nastavitev stroškov in prodajne cene izdelkov v razdelku »Upravljanje informacij o izdelku« za vsak izdelek na strani s seznamom **Izdani izdelki**, uporabite stran **Trgovinski sporazumi**.

## <a name="creating-a-wbs"></a>Ustvarjanje vmesnika SČD
Ustvarjanje vmesnika SČD vključuje tri dejavnosti:

1.  **Razčlenitev dela** – razčlenitev dela na manjše, obvladljive dele ali opravila.
2.  **Delovni urnik** – ocenjevanje časa, potrebnega za dokončanje opravila, nastavitev soodvisnosti opravil ter izbira začetnega in končnega datuma za opravila.
3.  **Ocena stroškov** – ocena stroškov za posamezno opravilo.

V naslednjih razdelkih je pojasnjeno, kako lahko zmogljivosti vmesnika SČD pomagajo pri vsaki od teh dejavnosti.

### <a name="work-decomposition"></a>Razčlenitev dela

Ustvarjanje razčlenitve dela je običajno prvi korak v postopku ustvarjanja vmesnika SČD. Funkcionalnost vmesnika SČD podpira naslednje osnovne postopke za členitev ali razčlenitev dela. 

**Koreninsko opravilo projekta** koreninsko opravilo projekta je opravilo povzetka na najvišji ravni za projekt. Vsa druga opravila projekta so ustvarjena pod njim. Ime korenskega opravila je vedno nastavljeno na ime projekta. Obseg dela, datumi in trajanje korenskega vozlišča povzemajo vrednosti za opravila pod korenskim opravilom. Lastnosti korenskega vozlišča lahko urejate ali izbrišete.

**Opravila povzetka ali vsebnika** opravilo povzetka je opravilo, ki ima podopravila ali sestavna opravila pod njim. Opravilo povzetka nima svojega obsega dela ali stroškov. Namesto tega sta obsega dela in stroškov opravila povzetka vsota obsega dela in stroškov njegovih sestavnih opravil. Prvi začetni datuma sestavnih opravil je uporabljen kot začetni datum opravila povzetke in zadnji končni datum sestavnih opravil je uporabljen kot končni datum. Ime opravila povzetka lahko urejate, lastnosti razporejanja za obseg, datume in trajanje pa ne. Če izbrišete opravilo povzetka, izbrišete tudi vsa njegova sestavna opravila. 

**Opravila listnega vozlišča** opravilo listnega vozlišča predstavlja najbolj podroben delovni paket v projektu. Listno vozlišče vključuje predvideni obseg dela, načrtovano število virov, načrtovani začetni in končni datum ter trajanje. 

Če želite omogočiti ustvarjanje hierarhije dela ali razčlenitve dela za projekt, dokončajte naslednje postopke hierarhije. 

**Novo opravilo** vsako novo opravilo, ki ga ustvarite, se samodejno doda pod korensko vozlišče in vsakemu opravilu se samodejno dodeli številka SČD. Številka SČD predstavlja raven opravila v hierarhiji. Za opravila na prvi ravni pod korenskim opravilom projekta se uporablja shema oštevilčevanja 1, 2, 3 in tako naprej. Za opravila pod prvo ravnjo se uporablja shema oštevilčevanja 1.1, 1.2, 1.3 in tako naprej. Za vsako raven, ki je dodana pod prejšnjo ravnjo, je dodana nova serija števil, zapisana s pikami. 

Trenutno ne morete prilagoditi oštevilčenja SČD. 

**Zamakni opravilo** ko opravilo zamaknete, postane podrejeno opravilu, ki ji je pred njim. Številka SČD novega podrejenega opravila se samodejno preračuna na podlagi številke SČD njegovega novega nadrejenega opravila. Nadrejeno opravilo je zdaj opravilo povzetka ali vsebnika in zato postane skupek svojih sestavnih opravil. 

> [!NOTE] 
> Ko zamaknete opravila pod opravilo, ki je bilo pred postopkom zamikanja listno vozlišče, na novo ustvarjeno opravilo povzetka izgubi svoje datume, obseg dela in številne vire. Zdaj uporablja povzetek vrednot svojih novih sestavnih opravil. 

**Primakni opravilo** ko opravilo primaknete, to ni več sestavno opravilo njegovega nadrejenega. Številka SČD tega opravila se samodejno preračuna, da odraža novo raven opravila v hierarhiji. Obseg dela, stroški in datumi prejšnjega nadrejenega opravila se preračunajo tako, da ne vključujejo tega opravila. 

**Premakni gor in Premakni dol** ko kliknete možnosti **Premakni gor** in **Premakni dol**, spremenite položaj opravila v hierarhiji nadrejenega. Položaj opravila ne vpliva na obseg dela, ceno, datume ali trajanje opravila. Številka SČD tega opravila se samodejno preračuna, da odraža nov položaj opravila.

### <a name="schedule-estimation"></a>Ocena razporeda

Ocena razporeda je običajno drugi korak pri ustvarjanju vmesnika SČD. Priporočamo, da po tem, ko ustvarite opravila, dokončate oceno razporeda. Stran **Strukturirana členitev dela** v rešitvi Finance ima dva razdelka. Zgornje podokno je namenjeno oceni razporeda, spodnje pa vključuje zavihek **Ocenjeni stroški in prihodki**, ki ga lahko uporabite za oceno stroškov. 
**Odvisnosti opravila** v vmesniku SČD lahko med opravili ustvarite predhodne odnose. Ko opravilu dodelite predhodna opravila, se to opravilo lahko začne šele, ko so njegova predhodna opravila dokončana. Načrtovani datum začetka opravila se samodejno nastavi na zadnji datum vseh njegovih predhodnikov. 

**Načrtovanje opravil** naslednji dejavniki določajo načrtovanje opravil listnega vozlišča:

-   Predhodniki
-   Obseg dela
-   Število virov
-   Začetni in končni datumi

Začetni datum opravila listnega vozlišča brez predhodnih opravil je privzeto nastavljen na začetni datum projekta. Trajanje opravila listnega vozlišča se vedno izračuna kot število delovnih dni med začetnim in končnim datumom. 

*<strong><em>Pravila za načrtovanje</em></strong>* ko je vklopljena pomoč za samodejno načrtovanje, za načrtovanje opravil listnega vozlišča veljajo naslednja pravila:

-   Začetni in končni datum opravila morata biti delovna dneva glede na koledar za načrtovanje projekta.
-   Začetni datum opravila s predhodnimi opravili je samodejno nastavljen na najpoznejši končni datum predhodnih opravil.
-   Obseg dela za opravilo se samodejno izračuna na naslednji način:

Število ljudi × trajanje × št. ur v standardnem delovnem dnevu v koledarju projekta. 

V nekaterih primerih boste morda želeli odstopati od teh pravil. Samodejno načrtovanje lahko izklopite, če želite preprečiti, da bi rešitev Finance samodejno nastavljala ali popravljala lastnosti opravil listnega vozlišča. Ko vnesete informacije za opravilo, ki povzroči kršitev pravil za načrtovanje, se za opravilo prikaže ikona napake pri načrtovanju. Če ne želite, da se prikažejo napake pri načrtovanju, kliknite možnost **Prikazane so napake pri načrtovanju**, da izklopite funkcijo. 

> [!NOTE] 
> Vrednosti za opravilo povzetka ali vsebnika se še naprej izračuna kot vsota vrednosti sestavnih opravil, ne glede na to, ali je pomoč pri samodejnem načrtovanju vklopljena ali izklopljena. 

**Odpravljanje napak pri načrtovanju** ko je vklopljena pomoč za samodejno načrtovanje, se verjetno ne bodo pojavile napake pri načrtovanju. Če pa samodejno pomoč pri razporejanju izklopite in jo pozneje znova vklopite, se bodo v vmesniku SČD morda pojavile ikone napak pri načrtovanju. 

**Odpravljanje napak pri načrtovanju glede na opravilo** ko dvokliknete ikono napake razporeda za določeno opravilo, se v pogovornem oknu prikažejo vse napake pri načrtovanju za to opravilo. Odločite se lahko, katere napake pri načrtovanju želite odpraviti za opravilo. 

**Odpravljanje vseh napak pri načrtovanju** če želite, da rešitev Finance v vmesniku SČD popravi vse napake pri načrtovanju, v podoknu za dejanja kliknite **Odpravite vsa neskladja pri načrtovanju**. 

> [!NOTE] 
> Ta funkcija lahko povzroči pomembne spremembe v vmesniku SČD. Napake so popravljene v naslednjem vrstnem redu:

1.  Ocenjeni obseg dela pri vseh opravilih se spremeni tako, da je enak zmogljivosti, ki je opredeljena v koledarju projekta.
2.  Datum začetka vsakega opravila se spremeni tako, da se opravilo začne po zaključku vseh predhodnih opravil.
3.  Začetni datum vsakega opravila se spremeni, da se odpravijo vrzeli v začetnih datumih predhodnih opravil.

### <a name="cost-estimation"></a>Ocena stroškov

Kot je bilo v tem dokumentu že omenjeno, oceno stroškov za vsako opravilo listnega vozlišča vnesete tako, da na strani **Strukturirana členitev dela** v spodnjem podoknu izberete zavihek **Ocenjeni stroški in prihodki**. 

> [!NOTE] 
> Ocene stroškov za opravilo povzetka ali vsebnika ne morete spremeniti. Ocena stroškov za opravilo povzetka je enaka vsoti ocene stroškov opravil listnega vozlišča. Skupni ocenjeni stroški za vsako opravilo se izračunajo kot vsota ocenjenih zneskov stroškov za naslednje vrste transakcij:

-   Delo
-   Izdelek ali material
-   Stroški

Vrsta transakcije s **pristojbino** se uporablja za oceno prihodkov, ki temeljijo na pristojbinah. Ta vrsta transakcije nima komponente stroškov, zato se pri oceni stroškov ne upošteva. 

Vrsta transakcije s plačilom **na kredit** se uporablja za beleženje pogodbene prodajne vrednosti pri projektu s fiksno vrednostjo. Tudi ta vrsta transakcije ni upoštevana pri oceni stroškov. 

Ko ocenjujete stroške dela, materiala in stroške za vsako opravilo, morate ocenjenim stroškom dodeliti kategorijo projekta. 

**Ocena stroškov dela** za vsako opravilo listnega vozišča dodelite obseg dela v urah in privzeto kategorijo. Ko torej nastavite razpored za opravilo, se ocena stroškov dela za to opravilo samodejno doda v privzeto kategorijo za delo. Ta ocena stroškov je prikazana na zavihku **Ocenjeni stroški in prihodki** v mreži za to opravilo **Podrobnosti vrstice**. Če potrebujete več ocen stroškov dela, jih lahko dodate na tem zavihku. Če povečate ali zmanjšate delovne ure na oceni stroškov dela, se urnik za opravilo samodejno preračuna. 

**Ocena stroškov in stroškov materiala** če potrebujete ocene, lahko na zavihku **Ocenjeni stroški in prihodki** ocenite stroške in stroške materiala za opravilo. 

Stroški in prodajna cena za vsako vrstico z oceno dela ali stroška temeljijo na nastavitvi, ki je za vsako kategorijo določena v tabelah cen, so v razdelku **Vodenje projekta in računovodstvo** &gt; **Nastavitev** &gt; **Oblikovanje cen**. Za izdelke so stroškov in prodajne cene privzeto dodane iz trgovinskega sporazuma ali sporazuma o izdelkih v razdelku »Upravljanje informacij o izdelku« na strani s seznamom **Izdani izdelki**.

## <a name="tracking-progress-on-the-wbs"></a>Sledenje napredku v vmesniku SČD
Nekatere panoge zelo natančno spremljajo napredek projekta v zvezi z vmesnikom SČD, druge pa napredek spremljajo na višji ravni vmesnika SČD. V tem razdelku je opisano, kako lahko sledenje v vmesniku SČD uporabite za svoje projektne zahteve. 

Rešitev Finance imajo za SČD projekta tri poglede: pogled načrtovanja, pogled sledenja obsegu dela in pogled za sledenje stroškov.

### <a name="planning-view"></a>Pogled načrtovanja

Pogled načrtovanja prikazuje načrtovano ali osnovno oceno razporeda in informacije o stroških. Čeprav ni funkcij za sledenje različici in izhodišču za SČD projekt, so vrednosti v tem pogledu namenjene predstavitvi osnovne različice. Razdelka za oceno razporeda in oceno stroškov te teme opisujeta ta pogled in to, kako je uporabljen za ustvarjanje vmesnika SČD.

### <a name="effort-tracking-view"></a>Pogled sledenja obsegu dela

Pogled sledenja obsegu dela prikazuje spremljanje napredka opravil v vmesniku SČD. Primerja zbrane dejanske ure obsega dela za opravilo z načrtovanimi urami obsega dela. Naslednje formule zagotavljajo vrednosti v pogledu sledenja obsegu dela:

-   Odstotek napredka = dejanski obseg dela do danes ÷ načrtovani obseg dela za opravilo
-   Preostali obseg dela (znan tudi kot predvideni obseg dela do zaključka \[ETC\]) = načrtovani obseg dela – dejanski obseg dela do danes
-   Ocena končnih stroškov = preostali obseg dela + dejanski obseg dela do danes
-   Predvideni odmik od obsega dela = načrtovan obseg dela – ocena končnih stroškov

Pogled za sledenje obsegu dela prikazuje projekcijo odmika od obsega dela za opravilo glede na to, ali je ocena končnih stroškov večja ali manjša od načrtovanega obsega dela:

-   Če je ocena končnih stroškov večja od načrtovanega obsega dela, bo opravilo predvidoma trajalo dlje časa, kot je bilo prvotno načrtovano, in zamuja načrtovani rok.
-   Če je ocena končnih stroškov manjša od načrtovanega obsega dela, bo opravilo predvidoma trajalo manj časa, kot je bilo prvotno načrtovano, in bo opravljeno pred predvidenim rokom.

**Ponovna projekcija stroškov vodje projekta** občasno bo moral vodja projekta ali druga oseba, ki spremlja napredek projekta, revidirati prvotne ocene za opravilo. Opravilo se lahko zaradi različnih razlogov premika hitreje ali počasneje, kot je bilo prvotno predvideno. Na primer, obseg je bil zmanjšan ali pa imajo delavci manj izkušenj, kot je bilo prvotno načrtovano. Projekcije projekta so dojemanje ocen vodje projekta glede na trenutno stanje projekta. Na splošno priporočamo, da ne spreminjate osnovnih številk, saj osnova projekta predstavlja objavljeni dokument za načrtovanje projekta in oceno stroškov, s čimer so se strinjale vse zainteresirane skupine, ki sodelujejo v projektu. 

Projektne vodje lahko spremenijo obseg dela v opravilih na dva načina:

-   Spremenite preostali obseg dela, ki je samodejno nastavljen tako, da posodobi dejanski preostali obseg dela v opravilu.
-   Spremenite odstotek napredka, ki je samodejno nastavljen tako, da posodobi dejanski odstotek napredka v opravilu.

Oba pristopa povzročita ponoven izračun ETA, ocene končnih stroškov in odstotka napredka ter predvidenega odmika od obsega dela v opravilu. Ponovno se izračunajo tudi RAC, ocena končnih stroškov in odstotek napredka v opravilih povzetkov in njihov predvideni odmik od obsega dela je posodobljen. 

**Spremenjen obseg dela v opravilih povzetka** spremenite lahko obseg dela v opravilih povzetka ali vsebnika. Ne glede na to, ali spremenite te vrednosti tako, da uporabite preostali obseg dela ali odstotek napredka, se izračuni samodejno izvedejo v naslednjem vrstnem redu:

1.  Izračunajo se ocena končnih stroškov, ETC in odstotek napredka v opravilu.
2.  Nova ocena končnih stroškov se porazdeli na podrejena opravila v enakem razmerju kot pri prvotnem znesku ocene končnih stroškov.
3.  Izračuna se nova ocena končnih stroškov za vsako opravilo listnega vozlišča.
4.  Preostali obseg dela in odstotek napredka se preračunata za vsa prizadeta podrejena opravila na podlagi nove vrednosti ocene končnih stroškov. Znova je izračunan odmik od obsega dela v opravilu.
5.  Znova je izračunana ocena končnih stroškov opravil povzetka iz listnih vozlišč.

V pogledu sledenja obsegu dela kliknite **Razširi na raven**, da nastavite raven sledenja in vzdrževanja vmesnika SČD. Kadar koli odprete pogled sledenja obsegu dela, se vmesnik SČD samodejno razširi na to raven.

### <a name="cost-tracking-view"></a>Pogled za sledenje stroškom

Pogled za sledenje stroškov prikazuje sledenje porabi stroškov za opravilo. V tem pogledu se dejanski stroški, porabljeni za opravilo do danes, primerjajo z načrtovanimi stroški za opravilo. Naslednje formule zagotavljajo vrednosti v pogledu za sledenje stroškom:

-   Odstotek porabljenih stroškov = dejanski stroški, porabljeni do danes ÷ načrtovani stroški za opravilo
-   Stroški do zaključka (CTC) = načrtovani stroški – dejanski stroški, porabljeni do danes
-   Ocena končnih stroškov = CTC + dejanski stroški, porabljeni do danes
-   Predvideni odmik od stroškov = načrtovani stroški – ocena končnih stroškov

Pogled za sledenje stroškom prikazuje projekcijo odmika od stroškov za opravilo glede na to, ali je ocena končnih stroškov večja ali manjša od načrtovanih stroškov:

-   Če je ocena končnih stroškov večja od načrtovanih stroškov, bo za opravilo predvidoma porabljeno več denarja, kot je bilo prvotno načrtovano, in stroški bodo presegli proračun.
-   Če je ocena končnih stroškov manjša od načrtovanih stroškov, bo za opravilo predvidoma porabljeno manj denarja, kot je bilo prvotno načrtovano, in stroški ne bodo presegli proračuna.

**Ponovna projekcija stroškov vodje projekta** vodje projektov morajo za revidiranje prvotne ocene stroškov za opravilo uporabiti CTC. Vodja projekta lahko spremeni vrednost CTC za stroške, ki so potrebni za dokončanje opravila. Če spremenite vrednost CTC, se preračunajo CTC, ocena končnih stroškov in odstotek porabljenih stroškov ter predvideni odmik od stroškov za opravilo. Ponovno se izračunajo tudi ocena končnih stroškov, ETC in odstotek porabljenih stroškov opravila povzetka ter njihov predvideni odmik od stroškov se posodobi. 

> [!NOTE] 
> Ko revidirate obseg dela za opravilo SČD v pogledu sledenja obsegu dela, se v pogledu za sledenje stroškom preračunajo CTC, ocena končnih stroškov, odstotek porabljenih stroškov in predvideni odmik od stroškov opravila. Vendar revizije stroškov ne vplivajo na vrednosti v pogledu sledenja obsegu dela, ker stroški glede na vrsto transakcije (delo, material ali stroški) ali kategorijo projekta niso revidirani. 

**Projekcija revizije stroškov opravil povzetka** stroške opravil povzetka lahko revidirate in izračuni se bodo samodejno izvedli v naslednjem vrstnem redu:

1.  Ponovno se izračunajo ocena končnih stroškov, CTC in odstotek porabljenih stroškov za opravilo.
2.  Nova ocena končnih stroškov se porazdeli na podrejena opravila v enakem razmerju kot pri prvotni oceni končnih stroškov pri opravilih.
3.  Izračuna se nova ocena končnih stroškov za vsako opravilo.
4.  Znova se izračunata CTS in odstotek porabljenih stroškov za prizadeta podrejena opravila na podlagi vrednosti ocene končnih stroškov. Znova je izračunan odmik od stroškov v opravilu.
5.  Na podlagi te spremembe se preračuna ocena končnih stroškov za vsa opravila povzetka.

V pogledu za sledenje stroškov kliknite **Razširi na raven**, da nastavite raven sledenja in vzdrževanja vmesnika SČD. Kadar koli odprete pogled za sledenje stroškov, se vmesnik SČD samodejno razširi na to raven.

### <a name="earned-value-management"></a>Upravljanje prislužene vrednosti

Z metodo prislužene vrednosti (EVM) lahko sledite napredku projekta. Metrike prisluženih vrednosti si lahko ogledate na začetni strani vodje projekta. Komponenta grafikona prisluženih vrednosti prikazuje časovno razporejene vrednosti načrtovane vrednosti in dejanskih stroškov. Prislužena vrednost od trenutnega datuma je prikazana kot točka. Časovno razporejeni podatki za prisluženo vrednost trenutno niso na voljo. 

Časovna faza na grafikonu prisluženih vrednosti je prikazana po tednih ali mesecih. Ta razdelek opisuje tri temelje metode prislužene vrednosti: načrtovano vrednost, prisluženo vrednost in dejanske stroške. 

**Načrtovana vrednost** teorija EVM navaja, da zasnova načrtovane vrednosti predstavlja hitrost, s katero je projektna ekipa nameravala zaslužiti vrednost na projektu. 

Rešitev Finance uporablja metodo prislužene vrednosti, ko načrtuje načrtovano vrednost. V skladu s tem pravilom je vrednost opravila objavljena v opravilu od njegovega končnega datuma. Nobena vrednost ni objavljena, dokler opravilo ni 100-odstotno dokončano. 

V razdelku »Vodenje projekta in računovodstvo« vnesete končni datum listnih vozlišč in načrtovane stroške. Ko je graf načrtovane vrednosti prikazan po tednih, je načrtovana vrednost povzeta po tednih za vsa opravila listnega vozlišča v času trajanja projekta. 

**Prislužena vrednost** teorija EVM navaja, da zasnova prislužene vrednosti predstavlja hitrost, s katero projektna ekipa dejansko služi vrednost na projektu. 

Rešitev Finance uporablja metodo prislužene vrednosti, ko njeni načrti prislužijo vrednost. V skladu s tem pravilom je vrednost opravila objavljena v opravilu od njegovega končnega datuma. Nobena vrednost ni objavljena, dokler opravilo ni 100-odstotno dokončano. 

Ko se izračuna prislužena vrednost, se upošteva odstotek napredka vsakega opravila. V skladu z metodo prislužene vrednosti se za izračun prislužene vrednosti ob koncu tega obdobja upoštevajo samo opravila, ki so dokončana v določenem obdobju. Prislužena vrednost na projektu se izračuna za vsa opravila, ki so bile dokončana, ko je graf ustvarjen. 

> [!NOTE] 
> Trenutno sistem za sledenje vmesniku SČD nima podatkovnih struktur za shranjevanje zgodovinskih odstotkov napredka pri vsakem opravilu. Zato je mogoče o prisluženi vrednosti poročati samo od trenutka, ko je kocka v obdelavi. Kocko redno obdelujte, da posodobite podatke o prisluženi vrednosti, ki so prikazani na začetni strani. 

**Dejanski stroški** teorija EVM navaja, da dejanski načrt stroškov predstavlja hitrost porabe denarja za projekt. 

Transakcije, ki so objavljene v projektu, se uporabljajo za načrtovanje dejanske vrstice cene. Stroški so povzeti po datumu. Ti podatki se nato uporabijo za prikaz dejanskih stroškov po tednih ali mesecih na grafikonu prisluženih vrednosti.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Kako uporabiti koncepte načrtovane vrednosti, prislužene vrednosti in dejanskih stroškov?

**Odmik od načrta** med načrtovanjem na časovnici ustvarite napoved za delo. Načrtovalci projektov so predvidevali, da bo načrtovana vrednost hitrost, s katero bo delo na projektu dokončano. Po tem ko je projekt v teku, je delo končano in projekt prisluži vrednost. Če primerjate načrtovano vrednost s prisluženo vrednostjo lahko vidite, kako napreduje delo na projektu. Rezultat te primerjave imenujemo odmik od načrta. 

Če je načrtovana vrednost za določeno obdobje večja od prislužene vrednosti, je količina dela, opravljenega na projektu, manjša od načrtovane. Torej je projekt v zaostanku. Ker sta načrtovana in prislužena vrednost izraženi v denarnih vrednostih, je čas zakasnitve na projektu tudi izražen v denarni vrednosti. 

Če je načrtovana vrednost za določeno obdobje manjša od prislužene vrednosti, je količina dela, opravljenega na projektu, večja od načrtovane. Torej projekt prehiteva urnik. Ta pretočni čas je tudi izražen v denarni vrednosti.

**Odmik od stroškov** prislužena vrednost uporablja lastno ceno kot množitelja, zato prislužena vrednost pomeni stroške dela, opravljenega na projektu. Ko projekt napreduje, transakcijski dnevnik vsebuje beleženje denarja, ki je dejansko porabljen za ta projekt. S primerjavo prislužene vrednosti z dejanskimi stroški si lahko ogledate porabljeni denar v primerjavi s prisluženo vrednostjo. Rezultat te primerjave imenujemo odmik od stroškov. 

Če so dejanski stroški, ki so porabljeni za določeno obdobje, večji od prislužene vrednosti, ste porabili več denarja, kot ste ga zaslužili. Zato projekt presega proračun. 

Če so dejanski stroški, ki so porabljeni za določeno obdobje, manjši od prislužene vrednosti, ste zaslužili več denarja, kot ste ga porabili. Torej projekt ni presegel proračuna.

## <a name="wbs-templates"></a>Predloge SČD
Funkcionalnost predlog SČD lahko uporabite za ustvarjanje standardnih predlog za projekte. Če projekti, ki jih ponuja vaše podjetje, vključujejo veliko ponovljivih del, razmislite o ustvarjanju predloge SČD. 

Predlogo SČD lahko ustvarite iz vmesnika SČD obstoječega projekta, tako da lahko znanje in najboljše prakse, ki ste jih zbrali med načrtovanjem tega projekta, v prihodnosti ponovno uporabite za podobne projekte. Vendar včasih morda ni smiselno shraniti celotnega vmesnika SČD kot predlogo. Zato lahko za projekt ustvarite tudi predloge iz delov vmesnika SČD.

### <a name="saving-a-projects-wbs-as-a-template"></a>Shranjevanje vmesnika SČD projekta kot predlogo

Ko ustvarite predlogo, jo lahko uvozite v vmesnik SČD novega projekta pod korensko vozlišče ali pod katero koli opravilo v vmesniku SČD projekta.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Uvoz predloge SČD v vmesnik SČD projekta

Ko uvozite opravila, so opravila v predlogi organizirana na podlagi začetnega datuma opravila, pod katero so uvožena. Med uvozom se za izračun začetnih datumov uvoženih opravil v predlogih opravil uporablja predhodne odnose. Standardni delovni koledar ciljnega projekta se uporablja za izračun končnih datumov uvoženih opravil tako, da se ohranijo delovni dnevi in standardni delovni čas, ki so določeni v delovnem koledarju trenutnega projekta. 

Zneski stroškov in prodajne cene se v podrobnostih ocene uporabljajo za zagotovitev, da imajo cene, ki so značilne za projekt ali pogodbo za projekt, veljavne datume.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Razlike med vmesnikom SČD projekta in predlogo SČD

-   Opravila v predlogah SČD nimajo začetnih in končnih datumov.

Delovni dnevi in dela prosti dnevi za predloge SČD niso nastavljeni.

-   Predloge SČD vedno uporabljajo koledar za načrtovanje, ki je nastavljen kot privzeti koledar za vse projekte.

Privzeti koledar za načrtovanje se uporablja samo za ugotavljanje ur v običajnem delovnem dnevu.

-   Predhodni odnosi niso kopirani v predlogo SČD.

Ker predloge SČD nimajo datumov, logika začetnega datuma, ki temelji na končnem datumu predhodnika, ni potrebna.

-   Vrstica z oceno stroškov dela se samodejno ustvari, ko je v predlogi SČD ustvarjeno opravilo. Prodajna cena in znesek stroškov sta kopirana pri izbranem delavcu.

Stroške in stroške izdelkov je mogoče ustvariti ročno, tako kot v vmesniku SČD projekta.

-   Napake pri načrtovanju se prikažejo, če obstajajo odstopanja od naslednje formule:

Obseg dela = število virov × trajanje × število ur v običajnem delovnem dnevu 

Če želite odpraviti vse napake pri načrtovanju, kliknite možnost **Odpravljanje vseh napak pri načrtovanju**. 

Napake pri načrtovanju pa lahko odpravite tudi tako, da za vsako opravilo kliknete ikono opozorila.





[!INCLUDE[footer-include](../includes/footer-banner.md)]