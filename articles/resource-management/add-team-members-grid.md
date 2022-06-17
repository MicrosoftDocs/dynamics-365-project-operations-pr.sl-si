---
title: Dodajanje članov ekipe iz mreže članov ekipe
description: Ta članek vsebuje informacije o tem, kako lahko upravljate vire članov ekipe.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3c0c277ca1fe2b709a6ff1c626f5ea7ec63705d6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928590"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Dodajanje članov ekipe iz mreže članov ekipe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Aplikacija Dynamics 365 Project Operations vključuje nadzorno ploščo vodnika za upravljanje virov, ki zagotavlja ponazoritev povpraševanja po virih in njihove uporabe v organizaciji. Grafikone na tej nadzorni plošči lahko uporabite za upodobitev teh informacij:

- **Povpraševanje po virih** : grafikon **Zahteve za dejavne vire** prikaže vire, ki so bili poslani. Viri so združeni po vlogi ali projektu.
- **Neposlano povpraševanje po virih**: grafikon **Povpraševanje po nedodeljenih virih** prikazuje vse zahteve za vir, ki niso bile poslane. Grafikon upraviteljem virov pomaga, da si ogledajo povpraševanje, ki ni potrjeno in ga je mogoče poslati prek zahteve za vir.
- **Zaračunana uporaba za pretekli teden**: grafikon **Uporaba po vlogi** prikazuje odstotek dejanske zaračunane uporabe po vlogi v primerjavi s ciljno zaračunano uporabo po vlogi v organizaciji.

    > [!NOTE]
    > Če želite, da je grafikon **Uporaba po vlogi na voljo**, ustvarite posel, ki zažene potek dela **UpdateRoleUtilization**. Ta ponavljajoči se posel se zažene vsakih sedem dni, da izračuna zaračunano uporabo za preteklih sedem dni. Rezultati se združijo po vlogi.

## <a name="manage-project-team-members"></a>Upravljanje članov projektne ekipe

Vodje projektov lahko za upravljanje virov v projektih uporabijo nadzorno ploščo za upravljanje virov. Lahko na primer dodajo člana ekipe neposredno v projekt in rezervirajo člana ekipe, da izpolnijo zahteve za vir, ki jih je zajel splošni vir.

### <a name="add-a-team-member-directly-to-a-project"></a>Dodajanje člana ekipe neposredno v projekt

Če želite člana ekipe dodati neposredno v projekt, na obrazcu **Projekti** na zavihku **Ekipa** izberite možnost **Novo**. Prikaže se pogovorno okno **Hitro ustvarjanje: član projektne ekipe**. V tem pogovornem oknu lahko izvedete ta opravila:

- **Rezervirajte poimenovani vir** v polju **Vir, ki ga je mogoče rezervirati** izberite ime vira. Nato izberite vlogo, nastavite obdobje in izberite način dodelitve. Poimenovani vir, ki ste ga izbrali, se doda projektu z uporabo izbranega načina dodelitve in koledarja virov.
- **Dodajte splošni vir**: pustite polje **Vir, ki ga je mogoče rezervirati** prazno, in nato izberite vlogo, nastavite obdobje ter izberite želeni način dodeljevanja. Ekipi se doda splošni vir v obliki ograde. Ograda ima vzorec povpraševanja, ki se uporablja za rezervacijo imenovanih virov v ekipi. Zahteva je ustvarjena v skladu s koledarjem projekta.
- **Ekipi dodajte poimenovani vir, ne da bi porabili zmogljivost vira**: v polju **Vir, ki ga je mogoče rezervirati** izberite vir. Izberite obdobje in nato kot način dodelitve izberite možnost **Brez**. Vir se doda ekipi, vendar rezervacija ne porabi zmogljivosti vira.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Rezervacija člana ekipe za izpolnjevanje zahtev za vir pri splošnem viru

V storitvi Project Operations lahko rezervirate splošno vir za projektno skupino. Določite lahko tudi vlogo, zahtevano zmogljivost in kako se ta zmogljivost porazdeli. V zahtevi za vir lahko določite atribute, ki so povezani s splošnim virom. Ti atributi vključujejo zahtevana znanja, želeno organizacijsko enoto in želene vire.

Če želite določiti zahtevana znanja v splošnem viru za razvijalca, opravite spodnje korake.

1. Na obrazcu **Projekti** na zavihku **Ekipa** izberite možnost **Novo**, da rezervirate splošni vir.
2. V pogledu **Vsi člani ekipe** v stolpcu **Zahtevani pogoj za vir** izberite povezavo, da dodate zahtevana znanja za splošni vir.
3. Na obrazcu **Zahtevani pogoj za vir** v mreži **Znanja** izberite tri pike (**...**), nato pa izberite možnost **Dodaj novo lastnost zahteve**, da dodate zahtevana znanja za razvijalca.
4. V obrazcu **Hitro ustvarjanje: lastnosti zahteve** v polju **Lastnost** izberite zahtevano znanje.
5. V polju **Vrednost ocene** izberite stopnjo usposobljenosti za to znanje. 
6. V polju **Zahtevani pogoj za vir** pa nastavite zahtevane pogoje za izvorne vire iz organizacijskih enot ali celo poimenovanih virov. Ko končate, izberite **Shrani**.
7. Na obrazcu **Zahtevani pogoj za vir** izberite **Rezerviraj**, da izpolnite zahtevani pogoj za vir. Izberete lahko tudi splošni vir v mreži **Vsi člani ekipe** in nato **Rezerviraj.**

    > [!NOTE]
    > V tem primeru je 40 zahtevanih ur, vendar ni dejanskih rezerviranih ur, ker splošni viri nimajo rezervacij. Poleg tega ni dodeljenih ur, ker je bil splošni vir dodan neposredno ekipi, namesto da bi bil dodan prek dodelitve opravila.

    Na obrazcu **Pomočnik za razporejanje** lahko filtrirate razpoložljive vire po zahtevah, ki so določene v zahtevanem pogoju za vir. Viri so razvrščeni glede na parametre razvrščanja, ki so določeni na plošči razporeda.

   Med najpogosteje uporabljene filtre spadajo:

    - **Lastnosti skupaj z oceno**: filtrirajte po znanjih, potrdilih in drugih kakovostih virov poleg ocen usposobljenosti.
    - **Vloge**: filtrirajte po privzetih vlogah, ki so dodeljene virom, ki jih je mogoče rezervirati.
    - **Organizacijske enote** : filtrirajte vire, ki jih je mogoče rezervirati, po organizacijskih enotah, ki so jim dodeljeni.

8. Če niste zadovoljni z rezultati prvotnega iskanja zahteve, lahko spremenite kriterije filtra. Razširite podokno **Pogled filtra** na levi in nato izberite **Iskanje**, da poiščete dodatne vire. Če želite spremeniti način razvrščanja rezultatov, izberite **Razvrsti**.
9. Izberite vire glede na zahtevo, ki je določena v pogoju, kot je navedeno na vrhu mreže. Počistite lahko izbor celic v mreži in zmogljivost vira pustite odprto. Samo en vir je lahko naenkrat izbran kot rezerviran.
10. Izberite **Rezerviraj**, da rezervirate izbrani vir in pustite ploščo razporeda odprto, tako da lahko izberete dodatne vire. Lahko pa izberete tudi **Rezerviraj in zapri**, da rezervirate izbrani vir in zaprete ploščo razporeda.
11. Vrnite se v pogled **Vsi člani ekipe**. V mreži lahko vidite, da je bil splošni vir zamenjan s poimenovanim virom in da je 40 ur navedenih kot rezerviranih za ta vir.

    > [!NOTE]
    > Dodeljene ure niso prikazane, ker so bile rezervirane neposredno v ekipi. Niso bile rezervirane prek dodelitve opravila.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Dodeljevanje splošnih virov opravilom in ustvarjanje pogojev za vir

V storitvi Project Operations lahko ustvarite opravila in jim nato dodelite splošne vire. Povpraševanje po virih lahko nato predstavljajo ograde, medtem ko ocenjujete urnik in finančne številke. Nato lahko ustvarite pogoje za vir za splošne vire in jih izpolnite.

1. Na obrazcu **Projekti** na zavihku **Načrtovanje** izberite možnost **Dodaj**, da ustvarite opravilo.
2. V polju **Viri** izberite simbol za **Izbirnik za vire**. Prikaže se izbirnik za vire in prikaže obstoječe člane ekipe za projekt.
3. Vnesite ime novega splošnega vira in nato **Ustvari.**
4. V pogovornem oknu **Hitro ustvarjanje: član projektne ekipe**, ki se prikaže, v polju **Vloga** izberite vlogo za splošni vir. 
5. V polju **Enota vira** izberite organizacijsko enoto za splošni vir. Nato izberite **Shrani**. Generični član ekipe je zdaj dodeljen opravilu.

   Na zavihku **Ekipa** boste videli novega generičnega člana ekipe. Opazili boste, da ima samo dodeljene ure. Te ure so vsota vseh opravil, ki so dodeljena generičnemu članu ekipe. Splošni član ekipe nima zahtevanih ur ali pogoja za vir.

6. Generičnega člana skupine lahko zdaj z izbirnikom virov dodelite drugim opravilom.

   Ko dokončate dodeljevanje splošnih virov opravilom, lahko ustvarite pogoj za vir za splošni vir.

7. Na zavihku **Ekipa** izberite splošni vir in nato **Ustvari zahtevo**. Ko je zahteva ustvarjena, bo generični član ekipe imel zahtevane ure in povezavo za pogoj za vir.

  Ko rezervirate poimenovani vir, je splošni vir odstranjen iz ekipe zamenjan s poimenovanim virom. Na zavihku **Načrtovanje** so dodelitve splošnega vira odstranjene in zamenjane s poimenovanim virom.

  > [!NOTE]
  > To se zgodi le, če je poimenovani vir v celoti rezerviran za zahtevo za splošni vir. Če poimenovani vir delno zamenja zahtevo za splošni vir ali več poimenovanih virov zamenja zahtevo za splošni vir, splošni vir ostane dodeljen opravilu.

Storitev Project Operations opravilu ne dodeli obeh virov, saj bi bil zaradi tega urnik manj predvidljiv. V tem enostavnem primeru je enostavno razdeliti ure enakomerno med dvema viroma. Vendar pa bi morala PSA v bolj zapletenih scenarijih, ki vključujejo več opravil in več virov, predpostaviti, kako naj dodeli rezervacije, prejete za več virov v več opravilih.

Zato je v teh scenarijih vodja projekta odgovoren za razčlenjevanje več rezervacij in njihovo dodeljevanje, če je to potrebno. Za dodeljevanje rezervacij vodja projekta dodeli opravila iz splošnih virov v poimenovane vire in nato uporabi pogled **Uskladitev**, da zagotovi, da dodelitev deluje z rezervacijami.

### <a name="edit-a-resource-requirement"></a>Urejanje pogoja za vir

Ko je pogoj za vir ustvarjen, lahko vodja projekta ali upravitelj virov uredi podrobnosti, da natančneje določi merila iskanja, ko uporablja ploščo razporeda. Če želite urediti pogoj za vir, sledite spodnjim korakom.

1. Na obrazcu **Projekti** na zavihku **Ekipa** izberite povezavo do katerekoli zahteve v splošnem viru.
2. Na obrazcu **Zahtevani pogoj za vir**, ki se pojavi, vnesite potrebne informacije o polju.

   Na obrazcu **Zahtevani pogoj za vir** lahko vodja projekta ali upravitelj virov opredeli tudi spretnosti, vloge, nastavitve virov in želeno organizacijsko enoto.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Posodabljanje rezervacij virov po tem, ko so rezervirani v projektu

Ko v projektno ekipo dodate splošni ali poimenovani vir, lahko spremenite rezervacije vira.

1. Na strani **Projekti** na zavihku **Ekipa** izberite člana ekipe in nato še možnost **Upravljaj rezervacije**.
 
   Prikaže se plošča razporeda, na kateri so prikazane rezervacije člana projektne ekipe. Razširite zapis člana ekipe in si oglejte ure, ki so bile rezervirane za ta projekt in druge projekte, ki porabljajo zmogljivost člana ekipe.

2. Izberite in povlecite rezervacijo, da jo razširite ali skrajšate. Prikaže se pogovorno okno **Ustvarjanje rezervacije vira**, ki vam omogoča prilagoditev rezervacije.
3. Z desno tipko miške kliknite rezervacijo. Nato lahko uporabite priročni meni in dokončate ta dejanja:

    - Spreminjanje stanja rezervacije
    - Urejanje rezervacije
    - Zamenjava vira v projektni ekipi

### <a name="change-the-booking-status"></a>Spreminjanje stanja rezervacije

Spremenite lahko katero koli privzeto stanje rezervacije ali stanje rezervacije po meri.

V storitvi Project Operations: so na voljo ta stanja:

- **Preklicano**: to stanje prekliče rezervacijo vira in sprosti zmogljivost vira.
- **Veljavna rezervacija**: to stanje porablja zmogljivost vira. Rezervacija ima to stanje običajno takrat, ko na obrazcu **Projekti** odprete **Upravljanje rezervacij** iz mreže **Vsi člani ekipe**.
- **Začasna rezervacija** : to stanje doda vir ekipi, vendar ne porabi zmogljivosti vira. Stanje pomeni, da je bil vir rezerviran za morebitno delo, vendar ima še vedno zmogljivost, če ga potrebujete pri drugih poslih. Z vidika splošne razpoložljivosti virov imajo začasne rezervacije drugačno stanje kot veljavne rezervacije.
- **Predlagano** to stanje predstavlja predlog za vir za upravitelja virov ali vodjo projekta. Predlogi ne porabijo zmogljivosti vira in vir ni dodan projektni ekipi. Za veljavno rezervacijo vira v ekipi mora vodja projekta sprejeti predlog.

### <a name="submit-resource-requests"></a>Pošiljanje zahtev za vire

Zahteve za vir se uporabljajo za hranjenje zahteve ali zahtevanega pogoja za vir, ki ga mora izpolniti upravitelj virov. Za splošni vir, ki je že v ekipi, lahko zahtevo za vir pošljete neposredno. Zahtevo za vir je mogoče izpolniti na dva načina:

- Upravitelj virov neposredno izpolni zahtevo. V tem primeru se splošni vir zamenja z veljavno rezervacijo s poimenovanim virom.
- Upravitelj virov predlaga vir vodji projekta, vodja projekta pa odobri ali zavrne predlagani vir.

#### <a name="direct-fulfillment-of-resource-requests"></a>Neposredna izpolnitev zahtev za vir

Ko je ustvarjen zahtevani pogoj za vir, lahko vodja projekta pošlje zahtevo za vir za splošni vir tako, da izbere vir in nato možnost **Pošlji zahtevo**. Komentarje o viru je mogoče posredovati upravitelju virov, ki izpolnjuje zahtevo. Po predložitvi zahteve se polje **Stanje** za člana ekipe spremeni v **Poslano**. Ko upravitelj virov izpolni zahtevo, je splošni član ekipe zamenjan s poimenovanim virom v mreži **Vsi člani ekipe**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Uporaba predlaganega vira za zahteve za vir

Namesto neposredne rezervacije vira v zahtevi za vir lahko upravitelj virov predlaga vir vodji projekta. Upravitelj virov lahko uporabi to možnost, ko natančno ujemanje za zahtevane pogoje ni na voljo. Ko upravitelj virov predlaga vir, vodja projekta vidi, da je polje **Stanje** za splošnega člana ekipe spremenjeno v **Potreben pregled**.

Predlagani vir si lahko ogledate skupaj z vizualizacijo učinka rezervacije predloga. 

1. Dvokliknite člana ekipe s statusom **Potreben pregled**. 
2. Izberite zavihek **Predlagani viri**.
3. Izberite **Sprejmi vse predloge**, da sprejmete vse predlagane vire, ali **Zavrni vse predloge**, da jih zavrnete. Če sprejmete predlagane vire, so v projektu veljavno rezervirani kot člani ekipe in zamenjajo splošne vire.

> [!NOTE]
> Sprejeti ali zavrniti morate vse predlagane vire. Ne morete jih delno sprejeti ali zavrniti.

### <a name="substitute-a-resource-on-the-project-team"></a>Zamenjava vira v projektni ekipi

Včasih mora vodja projekta zamenjati rezerviranega člana ekipe v projektu.

1. Na obrazcu **Projekti** na zavihku **Ekipa** izberite vir, ki potrebuje zamenjavo, nato pa izberite možnost **Upravljaj rezervacije**.
2. Razširite vir, da prikažete projekte, ki jim je dodeljen.
3. Z desno tipko miške kliknite projekt in nato izberite **Nadomeščanje vira**.
4. Če poznate vir, s katerim želite nadomestiti trenutni vir, izberite ali vnesite ime in nato izberite možnost **Znova dodeli**.

oziroma izvedite naslednje korake, če želite poiskati vir.

1. Izberite **Najdi nadomestitev**.

   Pomočnik za razporejanje vrne seznam nadomestkov, ki so na voljo. V pomočniku za razporejanje lahko dodatno filtrirate razpoložljive vire, da poiščete ustrezen nadomestek.

2. Če želite nadomestiti vir, izberite želeni vir in nato izberite **Nadomestek**.   

   Rezervacije in dodelitve se nadomestijo z novim virom.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Usklajevanje rezervacij in dodelitev člana ekipe

Pri članih ekipe so rezervacije in dodelitve ohlapno povezane. Z drugimi besedami, viri imajo lahko dodelitve brez rezervacij ali pa rezervacije brez dodelitev. V idealnem primeru so rezervacije in dodelitve usklajene, tako da imajo viri določeno zmogljivost za izvajanje dodelitev opravila. Vendar pa lahko rezervacije temeljijo na razpoložljivosti, časi opravil pa se lahko spremenijo, ko se projekt nadaljuje. Zato ohlapno povezovanje rezervacij in dodelitev zagotavlja prilagodljivost.

V storitvi Project Operations je zavihek **Uskladitev**, ki omogoča vodjam projektov, da uskladijo rezervacije članov ekipe in njihove dodelitve za projektne ekipe.

Zavihek **Uskladitev** prikaže rezervacije in dodelitve vse do ravni dodelitve posameznega opravila za vsakega člana ekipe. Ure so prikazane v celicah, ki predstavljajo časovna obdobja od mesecev do dni.

Zavihek prikazuje tudi skupno neto vsoto za projekt, skupaj s stolpcem s skupnim izračunom.

Zavihek za vsak vir izračuna razliko med rezervacijami člana ekipe in skupno vrednostjo dodelitev opravil člana ekipe. V idealnem primeru je ta razlika 0 (nič). Z drugimi besedami, med rezervacijami in dodelitvami ne bi smelo biti razlike. Razlike so obarvane in osenčene, da opozorijo na dva pogoja:

- **Primanjkljaj rezervacij**: do primanjkljaja rezervacij pride, ko ima vir več dodelitev kot rezervacij. Ker ta zmogljivost ni bila rezervirana, lahko vodja projekta odpravi to stanje tako, da razširi rezervacije vira za kritje primanjkljaja.
- **Odvečne rezervacije** : do odvečnih rezervacij pride, ko je vir rezerviran za projekt, vendar ni bil dodeljen opravilom. Ta pogoj je morda sprejemljiv v primerih, ko je bil vir rezerviran za projekt, preden je prišlo do dodelitve opravila. V drugih primerih pa vir morda ni načrtovan za dodelitev opravilom. V takem primeru mora upravitelj projekta razmisliti o preklicu rezervacij vira, da se lahko zmogljivost uporabi za drug projekt.

Ko si ogledujete čas na višji ravni, kot je dnevna raven (npr. na ravni meseca), se v nekaterih primerih za vir lahko prikaže neto razlika nič. Z drugimi besedami, rezervacije = dodelitve. Če pa pogledate čas na tedenski ravni, boste morda videli, da obstajajo dodelitve z nič urami in rezervacije s 40 urami v prvem tednu ter dodelitve s 40 urami in rezervacije z nič urami v drugem tednu meseca. Na splošno so rezervacije in dodelitve usklajene, vendar se razlikujejo od enega tedna do drugega.

Ko prikažete čas na višjih ravneh, imajo celice na zavihku **Usklajevanje** kazalnik, ki vas obvesti, da obstajajo razlike na nižjih ravneh. Z dvojnim klikom v celici lahko povečate prikaz in si ogledate razliko. Nato lahko kliknete z desno tipko miške, da pomanjšate prikaz. Če izberete vir in nato uporabite kontrolnik **Naslednja razlika** v orodni vrstici mreže, se lahko pomaknete na naslednjo razliko med rezervacijami in dodelitvami za ta vir. Izberite možnost **Prejšnja razlika** za vrnitev. Prav tako lahko v meniju **Nastavitve** izklopite kazalnik razlike in delovanje krmarjenja.

Če imate dodelitve opravil za vir, a nimate rezervacij, na obrazcu **Projekti** na zavihku **Usklajevanje** izberite primanjkljaj rezervacij in nato izberite možnost **Podaljšaj rezervacijo**. Prikaže se pogovorno **Podaljšaj rezervacijo** in prikaže rezervacijo, ki je potrebna za odpravo primanjkljaja vira. Pogovorno okno prikazuje tudi obstoječe rezervacije vira za vse projekte ali druge entitete, ki jih je mogoče razporediti. Če izberete **V redu**, da ustvarite rezervacijo za vir, lahko ne glede na razpoložljivost tega vira ustvarite prekomerno rezervacijo.

Vodja projekta ali upravitelj virov lahko nato s ploščo razporeda reši vse primere, kjer ima vir preveliko število rezervacij glede na svojo zmogljivost.


[!INCLUDE[footer-include](../includes/footer-banner.md)]