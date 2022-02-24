---
title: Upravljanje virov
description: Ta tema vsebuje informacije o upravljanju virov.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 37377367751592fc533447748b80b124cb6548ad
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151363"
---
# <a name="manage-resources"></a>Upravljanje virov

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation vključuje nadzorno ploščo za upravljanje virov, ki zagotavlja vizualni pregled povpraševanja po virih in njihove uporabe v organizaciji. Grafikone na tej nadzorni plošči lahko uporabite za upodobitev teh informacij:

- **Povpraševanje po virih** – grafikon **Zahteve za dejavne vire** prikaže vire, ki so bili poslani. Viri so združeni po vlogi ali projektu.
- **Neposlano povpraševanje po virih** – grafikon **Povpraševanje po nedodeljenih virih** prikazuje vse zahteve za vir, ki niso bile poslane. Upraviteljem virov pomaga, da si ogledajo povpraševanje, ki ni potrjeno in ga je mogoče poslati prek zahteve za vir.
- **Zaračunana uporaba za pretekli teden** – grafikon **Uporaba po vlogi** prikazuje odstotek dejanske zaračunane uporabe po vlogi v primerjavi s ciljno zaračunano uporabo po vlogi v organizaciji.

    > [!NOTE]
    > Če želite, da je grafikon **Uporaba po vlogi** na voljo, ustvarite posel, ki zažene potek dela UpdateRoleUtilization. Ta ponavljajoči se posel se zažene vsakih sedem dni, da izračuna zaračunano uporabo za preteklih sedem dni. Rezultati se združijo po vlogi.

## <a name="manage-project-team-members"></a>Upravljanje članov projektne ekipe

Vodje projektov lahko za upravljanje virov v projektih uporabijo nadzorno ploščo za upravljanje virov. Lahko na primer dodajo člana ekipe neposredno v projekt in rezervirajo člana ekipe, da izpolnijo zahteve za vir, ki jih je zajel splošni vir.

### <a name="add-a-team-member-directly-to-a-project"></a>Dodajanje člana ekipe neposredno v projekt

Če želite člana ekipe dodati neposredno v projekt, na strani **Projekti** na zavihku **Ekipa** izberite **Novo**. Prikaže se pogovorno okno **Hitro ustvarjanje: član projektne ekipe**. V tem pogovornem oknu lahko izvedete ta opravila:

- **Rezervirajte poimenovani vir** – v polju **Vir, ki ga je mogoče rezervirati** izberite ime vira. Nato izberite vlogo, nastavite obdobje in izberite način dodelitve. Poimenovani vir, ki ste ga izbrali, se doda projektu z uporabo izbranega načina dodelitve in koledarja virov.
- **Dodajte splošni vir** – pustite polje **Vir, ki ga je mogoče rezervirati** prazno, in nato izberite vlogo, nastavite obdobje ter izberite želeni način dodeljevanja. Splošni vir se ekipi doda kot označba mesta za hranjenje vzorca povpraševanja, ki se uporablja za rezervacijo poimenovanih virov v ekipi. Zahteva je ustvarjena v skladu s koledarjem projekta.
- **Ekipi dodajte poimenovani vir, ne da bi porabili zmogljivost vira** – v polju **Vir, ki ga je mogoče rezervirati** izberite vir. Nato izberite obdobje in **Brez** kot način dodelitve. Vir se doda ekipi, vendar rezervacija ne porabi zmogljivosti vira.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezervacija člana ekipe za izpolnjevanje zahtev za vir pri splošnem viru

V PSA lahko v projektni ekipi rezervirate splošni vir in določite vlogo, zahtevano zmogljivost in način porazdelitve zmogljivosti. V zahtevi za vir lahko določite atribute, ki so povezani s splošnim virom. Ti atributi vključujejo zahtevana znanja, želeno organizacijsko enoto in želene vire.

Če želite določiti zahtevana znanja v splošnem viru za razvijalca, sledite spodnjim korakom.

1. Na strani **Projekti** na zavihku **Ekipa** izberite **Novo**, da rezervirate splošni vir.

    ![Splošni vir je rezerviran v ekipi](media/Resource-Management-image9.png)

2. V pogledu **Vsi člani ekipe** v stolpcu **Zahtevani pogoj za vir** izberite povezavo, da dodate zahtevana znanja za splošni vir.

    ![Povezava do zahteve](media/Resource-Management-image10.png)

3. Na strani **Zahtevani pogoj za vir**, ki se prikaže, v mreži **Znanja** izberite tri pike (**...**) in nato **Dodaj novo lastnost zahteve**, da dodate zahtevana znanja za razvijalca.

    ![Ukaz »Dodaj novo lastnost zahteve«](media/Resource-Management-image11.png)

4. V pogovornem oknu **Hitro ustvarjanje: lastnosti zahteve**, ki se prikaže, v polju **Lastnost** izberite zahtevano znanje. Nato v polju **Vrednost ocene** izberite stopnjo usposobljenosti za to znanje. Na koncu v polju **Zahtevani pogoj za vir** nastavite zahtevane pogoje za izvorne vire iz organizacijskih enot ali celo poimenovanih virov. Ko končate, izberite **Shrani**.

    ![Pogovorno okno »Hitro ustvarjanje: značilnost zahteve«](media/Resource-Management-image12.png)

5. Na strani **Zahtevani pogoj za vir** izberite **Rezerviraj**, da izpolnite zahtevani pogoj za vir.

    ![Gumb »Rezerviraj« na strani »Zahtevani pogoj za vir«](media/Resource-Management-image13.png)

    Izberete lahko tudi splošni vir v mreži **Vsi člani ekipe** in nato **Rezerviraj.**

    ![Gumb »Rezerviraj« nad mrežo »Vsi člani ekipe«](media/Resource-Management-image14.png)

    > [!NOTE]
    > V tem primeru je 40 zahtevanih ur, vendar ni dejanskih rezerviranih ur, ker splošni viri nimajo rezervacij. Poleg tega ni dodeljenih ur, ker je bil splošni vir dodan neposredno ekipi. Ni bil dodan prek dodelitve opravila.

    Na strani **Pomočnik za razporejanje** lahko filtrirate razpoložljive vire po zahtevah, ki so določene v zahtevanem pogoju za vir. Viri so razvrščeni glede na parametre razvrščanja, ki so določeni na plošči razporeda.

    ![Stran »Pomočnik za razporejanje«](media/Resource-Management-image15.png)

    Tukaj je nekaj filtrov, ki se pogosto uporabljajo:

    - **Lastnosti skupaj z oceno** – filtrirajte po znanjih, potrdilih in drugih kakovostih virov poleg ocen usposobljenosti.
    - **Vloge** – filtrirajte po privzetih vlogah, ki so dodeljene virom, ki jih je mogoče rezervirati.
    - **Organizacijske enote** – filtrirajte vire, ki jih je mogoče rezervirati, po organizacijskih enotah, ki so jim dodeljeni.

6. Če niste zadovoljni z rezultati prvotnega iskanja zahteve, lahko spremenite kriterije filtra. Razširite podokno **Pogled filtra** na levi in nato izberite **Iskanje**, da poiščete dodatne vire.

    ![Podokno »Pogled filtra«](media/Resource-Management-image16.png)

7. Če želite spremeniti način razvrščanja rezultatov, izberite **Razvrsti**.

    ![Ukaz »Razvrsti«](media/Resource-Management-image17.png)

8. Izberite vire glede na zahtevo, ki je določena v pogoju, kot je navedeno na vrhu mreže. Počistite lahko izbor celic v mreži in zmogljivost vira pustite odprto. Samo en vir je lahko naenkrat izbran kot rezerviran.

9. Izberite **Rezerviraj**, da rezervirate izbrani vir in pustite ploščo razporeda odprto, tako da lahko izberete dodatne vire. Lahko pa izberete tudi **Rezerviraj in zapri**, da rezervirate izbrani vir in zaprete ploščo razporeda.

    ![Vir za rezervacijo](media/Resource-Management-image19.png)

    Prejmete obvestilo o rezerviranih urah. Kazalniki povpraševanja prikazujejo, v kolikšni meri je izpolnjena zahteva rezervacije in kakšen je preostanek. Vidite lahko tudi, koliko zmogljivosti izbranega vira je porabljene. Izberite **Razširi**, da prikažete več podrobnosti o rezervacijah virov.

9. Vrnite se v pogled **Vsi člani ekipe**. V mreži lahko vidite, da je bil splošni vir zamenjan s poimenovanim virom in da je 40 ur navedenih kot rezerviranih za ta vir.

    ![Posodobljena mreža v pogledu »Vsi člani skupine«](media/Resource-Management-image20.png)

    > [!NOTE]
    > Dodeljene ure niso prikazane, ker so bile rezervirane neposredno v ekipi. Niso bile rezervirane prek dodelitve opravila.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Dodeljevanje splošnih virov opravilom in ustvarjanje pogojev za vir

V PSA lahko ustvarite opravila in jim nato dodelite splošne vire. Na ta način lahko povpraševanje po virih predstavljajo označbe mesta, medtem ko ocenjujete urnik in finančne številke. Nato lahko ustvarite pogoje za vir za splošne vire in jih izpolnite.

1. Na strani **Projekti** na zavihku **Načrtovanje** izberite **Dodaj**, da ustvarite opravilo.

    ![Ustvarjeno je novo opravilo](media/Resource-Management-image21.png)

2. V polju **Viri** izberite simbol za **Izbirnik za vire**. Prikaže se izbirnik za vire in prikaže obstoječe člane ekipe za projekt.

    ![Izbirnik za vire](media/Resource-Management-image22.png)

3. Vnesite ime novega splošnega vira in nato **Ustvari.**

    ![Vneseno je ime novega splošnega vira](media/Resource-Management-image23.png)

4. V pogovornem oknu **Hitro ustvarjanje: član projektne ekipe**, ki se prikaže, v polju **Vloga** izberite vlogo za splošni vir. V polju **Enota vira** izberite organizacijsko enoto za splošni vir. Nato izberite **Shrani**.

    ![Pogovorno okno »Hitro ustvarjanje: član projektne ekipe«](media/Resource-Management-image24.png)

    Generični član ekipe je zdaj dodeljen opravilu.

    ![Generični član ekipe je dodeljen opravilu](media/Resource-Management-image25.png)

    Na zavihku **Ekipa** boste videli novega generičnega člana ekipe. Opazili boste, da ima samo dodeljene ure. Te ure so vsota vseh opravil, ki so dodeljena generičnemu članu ekipe. Generični član ekipe še nima zahtevanih ur ali pogoja za vir.

    ![Generični član ekipe na zavihku »Ekipa«](media/Resource-Management-image26.png)

5. Generičnega člana skupine lahko zdaj z izbirnikom virov dodelite drugim opravilom.

    ![Generični član ekipe v izbirniku virov](media/Resource-Management-image27.png)

    Ko dokončate dodeljevanje splošnih virov opravilom, lahko ustvarite pogoj za vir za splošni vir.

5. Na zavihku **Ekipa** izberite splošni vir in nato **Ustvari zahtevo**.

    ![Ukaz »Ustvari zahtevo«](media/Resource-Management-image28.png)

    Ko je zahteva ustvarjena, bo generični član ekipe imel zahtevane ure in povezavo za pogoj za vir.

    ![Povezava za pogoj za vir](media/Resource-Management-image29.png)

    Ko rezervirate poimenovani vir, je splošni vir odstranjen iz ekipe zamenjan s poimenovanim virom.

    ![Splošni vir je zamenjan s poimenovanim virom](media/Resource-Management-image30.png)

    Na zavihku **Načrtovanje** so dodelitve splošnega vira odstranjene in zamenjane s poimenovanim virom.

    ![Dodelitve splošnega vira so zamenjane s poimenovanim virom na zavihku »Načrtovanje«](media/Resource-Management-image31.png)

    > [!NOTE]
    > To se zgodi le, če je poimenovani vir v celoti rezerviran za zahtevo za splošni vir. Če poimenovani vir delno zamenja zahtevo za splošni vir ali več poimenovanih virov zamenja zahtevo za splošni vir, splošni vir ostane dodeljen opravilu.

    Na spodnji sliki je bilo načrtovano 80-urno opravilo za pet dni (16 ur na dan v petih dneh) in dodeljeno splošnemu viru z imenom **Funkcionalno**.

    ![80-urno, petdnevno opravilo dodeljeno splošnemu viru »Funkcionalno«](media/Resource-Management-image32.png)

    Ko ustvarite zahtevo, je ustvarite za 80 ur v petih dneh.

    ![Zahteva, ustvarjena za 80 ur v petih dneh](media/Resource-Management-image33.png)

    Ker razpoložljivi viri delajo le osem ur na dan, sta izpolnitev zahteve potrebna dva vira.

    ![Drugi vir](media/Resource-Management-image35.png)

    Na zavihku **Ekipa** lahko zdaj vidite, da splošni vir nima zahtevanih ur, temveč so dodeljene ure še vedno prikazane skupaj z obema poimenovanima viroma, ki zagotavljata izpolnitev.

    ![Dva poimenovana vira na zavihku »Ekipa«](media/Resource-Management-image36.png)

    Na zavihku **Načrtovanje** splošni vir ostane dodeljen opravilu.

    ![Splošni viri na zavihku »Načrtovanje«](media/Resource-Management-image37.png)

PSA ne dodeli obeh virov opravilu, saj bi bil zaradi tega urnik manj predvidljiv. V tem enostavnem primeru je enostavno razdeliti ure enakomerno med dvema viroma. Vendar pa bi morala PSA v bolj zapletenih scenarijih, ki vključujejo več opravil in več virov, predpostaviti, kako naj dodeli rezervacije, prejete za več virov v več opravilih.

Zato je v teh scenarijih vodja projekta odgovoren za razčlenjevanje več rezervacij in njihovo dodeljevanje, če je to potrebno. Za dodeljevanje rezervacij vodja projekta dodeli opravila iz splošnih virov v poimenovane vire in nato uporabi pogled **Uskladitev**, da zagotovi, da dodelitev deluje z rezervacijami.

### <a name="edit-a-resource-requirement"></a>Urejanje pogoja za vir

Ko je pogoj za vir ustvarjen, lahko vodja projekta ali upravitelj virov uredi podrobnosti, da natančneje določi merila iskanja, ko uporablja ploščo razporeda. Če želite urediti pogoj za vir, sledite spodnjim korakom.

1. Na strani **Projekti** na zavihku **Ekipa** izberite povezavo do katerekoli zahteve v splošnem viru.
2. Na strani **Pogoj za vir**, ki se prikaže, lahko posodobite več atributov. Tukaj je nekaj primerov:

    - Ime
    - Od datuma
    - Do datuma
    - Trajanje
    - Vrsta vira

Na strani **Pogoj za vir** lahko vodja projekta ali upravitelj virov določi tudi te informacije:

- Znanja
- Vloge
- Nastavitve virov
- Želena organizacijska enota

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Posodabljanje rezervacij virov po tem, ko so rezervirani v projektu

Ko v projektno ekipo dodate splošni ali poimenovani vir, lahko spremenite rezervacije vira.

1. Na strani **Projekti** na zavihku **Ekipa** izberite člana ekipe in nato **Upravljaj rezervacije**.

    ![Odpre se plošča razporeda za izbranega člana ekipe](media/Resource-Management-image40.png)

    Prikaže se plošča razporeda, na kateri so prikazane rezervacije člana projektne ekipe. Razširite zapis člana ekipe in si oglejte ure, ki so bile rezervirane za ta projekt in druge projekte, ki porabljajo zmogljivost člana ekipe.

2. Izberite in povlecite rezervacijo, da jo razširite ali skrajšate. Prikaže se pogovorno okno **Ustvarjanje rezervacije vira**, ki vam omogoča prilagoditev rezervacije.

    ![Pogovorno okno »Ustvarjanje rezervacije vira«](media/Resource-Management-image41.png)

3. Z desno tipko miške kliknite rezervacijo. Nato lahko uporabite priročni meni in dokončate ta dejanja:

    - Spremenite stanje rezervacije.
    - Uredite rezervacijo.
    - Nadomestite vir v projektni ekipi.

### <a name="change-the-booking-status"></a>Spreminjanje stanja rezervacije

Spremenite lahko katero koli privzeto stanje rezervacije ali stanje rezervacije po meri.

![Ukaz »Spremeni stanje«](media/Resource-Management-image42.png)

V PSA so na voljo ta stanja:

- **Preklicano** – to stanje prekliče rezervacijo vira in sprosti zmogljivost vira.
- **Veljavna rezervacija** – to stanje porablja zmogljivost vira. Rezervacija ima to stanje običajno takrat, ko na strani **Projekti** odprete **Upravljanje rezervacij** iz mreže **Vsi člani ekipe**.
- **Začasna rezervacija** – to stanje doda vir ekipi, vendar ne porabi zmogljivosti vira. To pomeni, da je bil vir rezerviran za morebitno delo, vendar ima še vedno zmogljivost, če ga potrebujete pri drugih poslih. Z vidika splošne razpoložljivosti virov imajo začasne rezervacije drugačno stanje kot veljavne rezervacije.
- **Predlagano** – to stanje predstavlja predlog za vir upravitelja virov ali vodje projekta. Predlogi ne porabijo zmogljivosti vira in vir ni dodan projektni ekipi. Za veljavno rezervacijo vira v ekipi mora vodja projekta sprejeti predlog.

### <a name="submit-resource-requests"></a>Pošiljanje zahtev za vire

Zahteve za vir se uporabljajo za hranjenje zahteve (zahtevanega pogoja za vir), ki ga mora izpolniti upravitelj virov. Za splošni vir, ki je že v ekipi, lahko zahtevo za vir pošljete neposredno. Zahtevo za vir je mogoče izpolniti na dva načina:

- Upravitelj virov neposredno izpolni zahtevo. V tem primeru se splošni vir zamenja z veljavno rezervacijo s poimenovanim virom.
- Upravitelj virov predlaga vir vodji projekta, vodja projekta pa odobri ali zavrne predlagani vir.

#### <a name="direct-fulfillment-of-resource-requests"></a>Neposredna izpolnitev zahtev za vir

Ko je ustvarjen zahtevani pogoj za vir, lahko vodja projekta pošlje zahtevo za vir za splošni vir tako, da izbere vir in nato možnost **Pošlji zahtevo**.

![Gumb »Pošlji zahtevo«](media/Resource-Management-image45.png)

Komentarje o viru je mogoče posredovati upravitelju virov, ki izpolnjuje zahtevo. Po predložitvi zahteve se polje **Stanje** za člana ekipe spremeni v **Poslano**.

![Vnos neobveznih komentarjev](media/Resource-Management-image46.png)

Ko upravitelj virov izpolni zahtevo, je generični član ekipe zamenjan s poimenovanim virom v mreži **Vsi člani ekipe**.

![Generični član skupine je zamenjan s poimenovanim virom v mreži »Vsi člani ekipe«](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Uporaba predlaganega vira za zahteve za vir

Namesto neposredne rezervacije vira v zahtevi za vir lahko upravitelj virov predlaga vir vodji projekta. Upravitelj virov lahko uporabi to možnost, ko natančno ujemanje za zahtevane pogoje ni na voljo. Ko upravitelj virov predlaga vir, vodja projekta vidi, da je polje **Stanje** za generičnega člana ekipe spremenjeno v **Potreben pregled**.

![Stanje generičnega člana ekipe se je spremenilo v »Potrebuje pregled«](media/Resource-Management-image48.png)

Če si želite predlagani vir ogledati skupaj z upodobitvijo učinka rezervacije predloga, dvokliknite člana ekipe s stanjem **Potreben pregled**. Nato izberite zavihek **Predlagani viri**.

![Zavihek »Predlagani viri«](media/Resource-Management-image49.png)

Izberite **Sprejmi vse predloge**, da sprejmete vse predlagane vire, ali **Zavrni vse predloge**, da jih zavrnete. Če sprejmete predlagane vire, so v projektu veljavno rezervirani kot člani ekipe in zamenjajo splošne vire.

> [!NOTE]
> Sprejeti ali zavrniti morate vse predlagane vire. Ne morete jih delno sprejeti ali zavrniti.

### <a name="substitute-a-resource-on-the-project-team"></a>Zamenjava vira v projektni ekipi

Včasih mora vodja projekta zamenjati rezerviranega člana ekipe v projektu.

1. Na strani **Projekti** na zavihku **Ekipa** izberite vir, ki potrebuje zamenjavo, in nato **Upravljaj rezervacije**.
2. Razširite vir, da prikažete projekte, ki jim je dodeljen.

    ![Razširjen vir prikazuje dodeljene projekte](media/Resource-Management-image50.png)

3. Z desno tipko miške kliknite projekt in nato izberite **Nadomeščanje vira**.
4. Če poznate vir, s katerim želite nadomestiti trenutni vir, izberite ali vnesite ime in nato izberite **Znova dodeli**.

    ![Določanje nadomestnega vira](media/Resource-Management-image51.png)

    Ali pa sledite spodnjim korakom, da poiščete vir:

    1. Izberite **Najdi nadomestitev**.

        ![Iskanje nadomestnega vira](media/Resource-Management-image52.png)

        Pomočnik za razporejanje vrne seznam nadomestkov, ki so na voljo. V pomočniku za razporejanje lahko dodatno filtrirate razpoložljive vire, da poiščete ustrezen nadomestek.

        ![Seznam nadomestkov, ki so na voljo](media/Resource-Management-image53.png)

    2. Če želite nadomestiti vir, izberite želeni vir in nato izberite **Nadomestek**.

        ![Nadomestni vir je izbran](media/Resource-Management-image54.png)

    Rezervacije in dodelitve se nadomestijo z novim virom.

    ![Rezervacije in dodelitve so nadomeščene z novim virom](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Usklajevanje rezervacij in dodelitev člana ekipe

Pri članih ekipe so rezervacije in dodelitve ohlapno povezane. Z drugimi besedami, viri imajo lahko dodelitve brez rezervacij ali pa rezervacije brez dodelitev. V idealnem primeru so rezervacije in dodelitve usklajene, tako da imajo viri določeno zmogljivost za izvajanje dodelitev opravila. Vendar pa lahko rezervacije temeljijo na razpoložljivosti, časi opravil pa se lahko spremenijo, ko se projekt nadaljuje. Zato ohlapno povezovanje rezervacij in dodelitev zagotavlja prilagodljivost.

PSA ima zavihek **Uskladitev**, ki omogoča vodjam projektov, da uskladijo rezervacije članov ekipe in njihove dodelitve za projektne ekipe.

![Zavihek »Uskladitev«](media/Resource-Management-image56.png)

Zavihek **Uskladitev** prikaže rezervacije in dodelitve vse do ravni dodelitve posameznega opravila za vsakega člana ekipe. Ure so prikazane v celicah, ki predstavljajo časovna obdobja od mesecev do dni.

Zavihek prikazuje tudi skupno neto vsoto za projekt, skupaj s stolpcem s skupnim izračunom.

Zavihek za vsak vir izračuna razliko med rezervacijami člana ekipe in skupno vrednostjo dodelitev opravil člana ekipe. V idealnem primeru je ta razlika 0 (nič). Z drugimi besedami, med rezervacijami in dodelitvami ne bi smelo biti razlike. Razlike so obarvane in osenčene, da opozorijo na dva pogoja:

- **Primanjkljaj rezervacij** – do primanjkljaja rezervacij pride, ko ima vir več dodelitev kot rezervacij. Ker ta zmogljivost ni bila rezervirana, lahko vodja projekta odpravi to stanje tako, da razširi rezervacije vira za kritje primanjkljaja.
- **Odvečne rezervacije** – do odvečnih rezervacij pride, ko je vir rezerviran za projekt, vendar ni bil dodeljen opravilom. Ta pogoj je morda sprejemljiv v primerih, ko je bil vir rezerviran za projekt, preden je prišlo do dodelitve opravila. V drugih primerih pa vir morda ni načrtovan za dodelitev opravilom. V takem primeru bi moral upravitelj projekta razmisliti o preklicu rezervacij vira, da se lahko zmogljivost uporabi za drug projekt.

Ko si ogledujete čas na višji ravni, kot je dnevna raven (npr. na ravni meseca), se v nekaterih primerih za vir lahko prikaže neto razlika nič (z drugimi besedami, rezervacije = dodelitve). Če pa pogledate čas na tedenski ravni, boste morda videli, da obstajajo dodelitve z nič urami in rezervacije s 40 urami v prvem tednu ter dodelitve s 40 urami in rezervacije z nič urami v drugem tednu meseca. Na splošno so rezervacije in dodelitve usklajene, vendar se razlikujejo od enega tedna do drugega.

Ko prikažete čas na višjih ravneh, imajo celice na zavihku **Usklajevanje** kazalnik, ki vas obvesti, da obstajajo razlike na nižjih ravneh. Z dvojnim klikom v celici lahko povečate prikaz in si ogledate razliko. Nato lahko kliknete z desno tipko miške, da pomanjšate prikaz. Če izberete vir in nato uporabite kontrolnik **Naslednja razlika** v orodni vrstici mreže, se lahko pomaknete na naslednjo razliko med rezervacijami in dodelitvami za ta vir. Nato lahko za vrnitev uporabite kontrolnik **Prejšnja razlika**. Prav tako lahko v meniju **Nastavitve** izklopite kazalnik razlike in delovanje krmarjenja.

![Kazalnik razlike](media/Resource-Management-image57.png)

Če imate dodelitve opravil za vir, a nimate rezervacij, na strani **Projekti** na zavihku **Usklajevanje** izberite primanjkljaj rezervacij in nato **Podaljšaj rezervacijo**. Prikaže se pogovorno **Podaljšaj rezervacijo** in prikaže rezervacijo, ki je potrebna za odpravo primanjkljaja vira. Prikazuje tudi obstoječe rezervacije vira za vse projekte ali druge entitete, ki jih je mogoče razporediti. Če izberete **V redu**, da ustvarite rezervacijo za vir, lahko ne glede na razpoložljivost tega vira ustvarite prekomerno rezervacijo.

![Pogovorno okno »Podaljšaj rezervacijo«](media/Resource-Management-image58.png)

Vodja projekta ali upravitelj virov lahko nato s ploščo razporeda reši vse primere, kjer ima vir preveliko število rezervacij glede na svojo zmogljivost.
