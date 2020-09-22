---
title: Iskanje virov za projekt
description: Ta tema vsebuje informacije o iskanju virov za projekt.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755732"
---
# <a name="project-resourcing"></a>Iskanje virov za projekt

[!include [banner](../includes/banner.md)]

Ta tema vsebuje informacije o iskanju virov za projekt.

Eden od izzivov za projektne vodje in upravitelje virov v fazi načrtovanja projekta je dodeljevanje virov, kjer morajo določiti in rezervirati pravi vir za delo na projektu. V storitvi Dynamics 365 Finance vam zmogljivosti iskanja virov za projekte omogočajo opredelitev vlog, ki se obravnavajo kot začasni viri, ki jih je mogoče rezervirati za specifičen angažma ali del angažmaja. Ta vrsta iskanja virov omogoča projektnim vodjem in upraviteljem virov, da izvedejo naslednja opravila:

- Opredelitev vloge, ki ima zahtevane sposobnosti, da je zanjo enostavno najti ujemajoče se vire.
- Uporaba vlog za opredelitev prvotnega razporeda angažmaja, ki temelji na rezerviranih virih.
- Ocena stroškov in določitev prvotnega proračuna, na podlagi dodeljenih vlog in virov za projekt.
- Uporaba vlog za oceno števila rezervacij virov, ki so potrebne za vsak angažma.
- Ocena števila virov, ki so potrebni za celoten življenjski cikel projekta.
- Priprava osnutka strukturirane členitve dela (WBS) z uporabo prvotnih angažmajev virov.

[![Življenjski cikel projekta](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Ko se načrtovanje projekta nadaljuje, je mogoče načrtovane vire zamenjati z zaposlenimi viri. Projektni vodja se lahko tudi vrača in posodablja rezervacije ob iskanju virov v kateri koli fazi projekta.

## <a name="set-up-project-resources"></a>Nastavitev virov projekta
Nastaviti morate koledar in ga povezati z zaposlenim ali delavcem. Koledar se uporablja za načrtovanje projekta in delovnega časa virov, ki so rezervirani za projekt. Med nastavitvijo koledarja lahko projektni vodje opravijo izravnavo virov kot del optimizacije virov. Na podlagi razporeda koledarja je mogoče uvesti omejitve za vire. Koledar lahko nastavite na strani **Koledarji**.

Ko nastavljate delavca kot vir projekta, lahko izbirate med delavci, ki delajo v podjetju, za katero nastavljate vire. Lahko pa izberete delavce iz drugih podjetij v organizaciji. Ti delavci so znani kot medpodjetniški viri.

Z naslednjimi postopki je pojasnjeno, kako nastavite delavca kot vir projekta v vašem podjetju in kako nastavite medpodjetniški vir projekta.

### <a name="set-up-a-worker-as-a-project-resource"></a>Nastavitev delavca kot vir projekta

1. Na strani **Delavci** na seznamu **Delavci** izberite delavca, ki ga dodajate kot vir projekta, in odprite zapis delavca.
2. V podoknu za dejanja izberite **Projekt** &gt; **Nastavitev** &gt; **Nastavitev projekta**.
3. Izberite koledar in nato zaprite stran.

Določite lahko tudi privzete projekte za vire kot vrsto preddodelitve. Preddodelitve je mogoče uporabiti, ko upravitelj virov ali projektni vodja vnaprej ve, na katerih projektih bo delal vir. Preddodelitve lahko temeljijo tudi na zahtevi sponzorja ali stranke projekta. Za preddodelitev projekta na strani **Dodelitve projektov** na zavihku **Projekti** v seznamu **Preostali projekti** izberite primeren projekt.

### <a name="set-up-an-intercompany-resource"></a>Nastavitev medpodjetniškega vira

Ko nastavite delavca kot medpodjetniški vir, morate izvesti nastavitev v podjetju posojevalcu in podjetju izposojevalcu.

**V podjetju posojevalcu**

1. V storitvi Finance potrdite, da je izbrano podjetje posojevalec in nato izvedite postopke v prejšnjem razdelku »Nastavitev delavca kot vir projekta«.
2. Na strani **Medpodjetniško računovodstvo** izberite možnost **Novo**.
3. V polju **ID pravne osebe** izberite podjetje posojevalca. Izpolnite preostala polja, kot je primerno, in nato izberite **Shrani**.
4. Na strani **Cena prenosa** izberite možnost **Novo**.
5. V polju **Pravna oseba izposojevalka** izberite ustrezno podjetje.
6. Da bi podjetju izposojevalcu posodili samo vir, ki ste ga ustvarili na začetku tega razdelka, v polju **Vir** izberite ime vira, ki ste ga ustvarili. Da bi dali vse vire v podjetju posojevalcu na voljo podjetju izposojevalcu, pustite polje **Vir** prazno.
7. Na strani **Vodenje projektov in računovodski parametri** na zavihku **Medpodjetniško** nastavite možnost **Omogoči medpodjetniško razporejanje virov in časovne liste** na **Da**.

**V podjetju izposojevalcu**

- Na strani **Seznam virov** v iskalni filter vnesite ime vira, ki ste ga ustvarili za podjetje posojevalca, da preverite, ali je ime vključeno na seznam virov za podjetje izposojevalca.

## <a name="manage-resource-competencies"></a>Upravljanje sposobnosti virov
Sposobnosti virov so bistveni del upravljanja virov. Sposobnosti je mogoče uporabiti kot izhodišče za določanje virov, ki imajo pravo ravnovesje znanj, izobrazbe, potrdil in projektnih izkušenj. Te informacije bi morali nastaviti za vsak vir in jih redno posodabljati. Na ta način lahko povečate zmogljivosti, ko so najdena ujemanja za sposobnosti določenega vira med dodelitvijo vira projekta.

[![Primeri znanj, potrdil, izobrazbe in projektnih izkušenj](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Z naslednjimi postopki je pojasnjeno, kako nastavite nekatere sposobnosti za vir.

Za nastavitev sposobnosti za delavca lahko uporabite bodisi stran seznama **Delavci** v možnosti »Človeški viri« ali stran seznama **Viri** v možnosti »Vodenje projektov in računovodstvo«. Za naslednje postopke se uporablja stran seznama **Delavci** v možnosti »Človeški viri«.

### <a name="set-up-competencies-certificates"></a>Nastavitev sposobnosti: potrdila

1. Na strani seznama **Delavci** izberite vrstico za delavca, za katero želite dodati informacije o potrdilu.
2. V podoknu za dejanja na zavihku **Delavec** v skupini **Sposobnosti** izberite **Potrdila**.
3. Izberite **Novo**, nato pa v polju **Vrsta potrdila** izberite **PMP**.
4. V polju **Začetni datum** izberite **1. 10. 2015**, nato pa izberite **Shrani**.

### <a name="set-up-competencies-skills"></a>Nastavitev sposobnosti: znanja

1. Na strani s seznamom **Delavci** zagotovite, da je delavec, ki ste ga uporabljati v prejšnjem postopku, še vedno izbran. Nato v podoknu za dejanja na zavihku **Delavec** v skupini **Sposobnosti** izberite **Znanja**.
2. Izberite **Novo**.
3. V polju **Znanja** izberite **Vodenje projektov**.
4. V polju **Raven** izberite **5 Izvedenec**.
5. V polju **Datum ravni** izberite **14. 1. 2014**.
6. V polje **Leta izkušenj** vnesite **10**.
7. Izberite **Shrani** in nato zaprite stran.

## <a name="create-a-new-project"></a>Ustvarite nov projekt
1. Na strani **Vodenje projektov** izberite **Nov projekt**, nato pa vnesite naslednje vrednosti:

    - **Vrsta projekta:** Čas in material
    - **Ime projekta:** 2. faza nadgradnje XYZ
    - **Projektna skupina:** TM\_WIP
    - **ID projektne pogodbe:** 00000002

2. Izberite **Ustvarjanje projekta**.

### <a name="assign-a-resource-to-a-project"></a>Dodeljevanje vira projektu

1. Na strani **Delavci** na seznamu **Delavci** izberite zapis za delavca, za katerega ste prej nastavili spodobnosti, in odprite zapis delavca.
2. V podoknu za dejanja na zavihku **Projekt** v skupini **Nastavitev** izberite **Dodelitve projektov**.
3. Na strani **Dodelitve projekta potrjevanja vira** na zavihku **Projekti** v polju **Dodaj projekt v izbrane projekte** filtrirajte na projekt **2. faza nadgradnje XYZ**.
4. V podoknu **Preostali projekti** izberite projekt in nato izberite gumb puščice, da ga dodate v podokno **Izbrani projekti**.

Prav tako lahko dodelite kategorije za vir, kot je potrebno. Vrsta kategorije je bodisi **Stroški** ali **Prihodki**. Vrsto kategorije določa vaša organizacija. Če za vir ni dodeljene nobene kategorije, storitev Finance poišče privzeto kategorijo urnih cen stroškov in prihodkov.

### <a name="set-up-project-resource-and-role-characteristics"></a>Nastavitev vira projekta in značilnosti vloge

Projektni vodja lahko uporabi funkcionalnost iskanja virov za projekt, da ustvari vloge, ki so potrebne za projekt. Vloge se lahko uporabijo, če so potrjeni viri še vedno neznani, ko se viri rezervirajo. Vloge so lahko začasno rezervirane kot načrtovani viri, da lahko nadaljujete faze načrtovanja projekta.

[![Primer vloge](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarij:** Podjetje Contoso je prejelo naročilo za izpolnitev časovnega in materialnega projekta, ki ima odobreno projektno listino. Mlajši projektni vodja še vedno izpolnjuje obseg projekta. Upravitelj virov trenutno prepoznava specifične vire, ki bodo rezervirani za delo na novem projektu. Zaradi kritične narave projekta je sponzor projekta za eno od vlog zahteval višjega projektnega vodjo. Upravitelj virov mora pridobiti nov vir in določiti vlogo v sistemu, če mlajši projektni vodja med načrtovanjem projekta zahteva informacije o viru.

Naslednji koraki prikazujejo, kako lahko upravitelj virov nastavi vlogo višjega projektnega vodje in z njo poveže značilnosti vira. Pozneje lahko vlogo uporabimo za iskanje razpoložljivih virov, ki se ujemajo z zahtevanimi sposobnostmi virov.

1. Na strani **Nastavitev vlog** izberite **Novo**, nato pa vnesite naslednje vrednosti:

    - **ID vloge:** Višji projektni vodja
    - **Opis:** Višji projektni vodja

2. Izberite **Ustvari**.
3. Izberite vlogo **Višji projektni vodja** in nato izberite **Konfiguracija značilnosti**.
4. V polju **Vrsta značilnosti** izberite **Znanje**.
5. V polju **Razpoložljive značilnosti** vnesite znanje, po katerem se išče.
6. V polju **Vrsta značilnosti** izberite **Potrdilo**.
7. V polju **Razpoložljive značilnosti** vnesite vrsto potrdila, po katerem se išče.

### <a name="assign-a-project-resource-to-a-project"></a>Dodeljevanje vira projekta projektu

1. Na strani **Vsi projekti** izberite projekt **2. faza nadgradnje XYZ**.
2. Na zavihku **Projektna ekipa in načrtovanje** izberite **Dodaj**.
3. V polju **Vloga** izberite **Član ekipe**.
4. Izberite **Rezervacija iz koledarja**.
5. Na strani **Razpoložljivost vira** izberite **Nastavitve pogleda**.
6. Na strani **Prilagajanje nastavitev pogleda** vnesite naslednje vrednosti:

    - **Oblika za pogled datumskega obsega:** Dan
    - **Prikaz opisov razpoložljivosti:** Da
    - **Prikaz preostale zmogljivosti:** Da

7. Na seznamu virov izberite vir.
8. Izberite **Veljavna rezervacija** in **Polna zmogljivost**.


### <a name="assign-a-resource-to-a-default-role"></a>Dodeljevanje vira privzeti vlogi

Kot pomoč lahko projektni vodje ali upravitelji virov prikažejo vire, ki jih je mogoče rezervirati za projekt, na ravni z več podrobnostmi. Privzeto vlogo lahko povežete z obstoječim virom ali novo pridobljenim virom. Na primer, Daniel je imel ob začetku sodelovanja izkušnje in znanja za zapolnitev vloge poslovnega analitika. Upravitelj virov je to vlogo določil kot privzeto vlogo za Daniela. Zato je upravitelj virov Daniela dodal v skupino poslovnih analitikov, ki so na voljo za delo na projektih.

Med rezervacijo virov lahko projektni vodje filtrirajo vire z vlogo, ki so na voljo za delo na projektih. Te informacije lahko uporabijo kot eno merilo, kadar med zapolnitvijo virov izvajajo analizo odločitev z več merili. V filter lahko dodajo tudi druge značilnosti virov za iskanje virov s posebnimi znanji, izobrazbo in izkušnjami za določen projekt.

**Scenarij:** Odobren projekt se je začel in vloga višjega projektnega vodje je bila rezervirana kot načrtovani vir v fazi načrtovanja projekta. Upravitelj virov je zdaj pridobil vir za zapolnitev vloge višjega projektnega vodje.

1. Na strani **Seznam virov** izberite **Daniel Goldschmidt**.
2. Na strani **Vloga vira** izberite **Novo**, nato pa vnesite naslednje vrednosti:

    - **Datum začetka veljavnosti:** Vnesite trenutni datum.
    - **Datum poteka:** Vnesite **Nikoli**.
    - **Vloga:** Vnesite **Višji projektni vodja**.

3. Izberite **Shrani** in nato zaprite stran.
4. Na zavihku **Sposobnosti** dodajte znanje **Vodenje projektov** in potrdilo **PMP**.

## <a name="set-up-role-based-pricing"></a>Nastavitev cen na podlagi vlog
Za vloge je mogoče nastaviti vse lastne cene, prodajne cene in cene prenosa.

1. Na strani **Prodajna cena (ura)** izberite **Novo** in vnesite datum začetka veljavnosti.
2. V stolpcu **Vloga** izberite vlogo.
3. V stolpcu **Cene** vnesite ceno za izbrano vlogo vira.

## <a name="form-a-project-team"></a>Oblikovanje projektne ekipe
Za uporabo vlog, ki so bile predhodno nastavljene v projektu, mora projektni vodja vloge povezati s projektom. Za projekt je mogoče dodeliti več vlog. Da bi preprečili zmedo, so te vloge med rezervacijo samodejno označene. Na primer, če projektni vodja zahteva tri inženirje programske opreme, so samodejno ustvarjene tri vloge inženirjev programske opreme, ki imajo kot oznake **inženir programske opreme 1**, **inženir programske opreme 2** in **inženir programske opreme 3**. Če so bile značilnosti vloge prej nastavljene za vlogo, so uporabljene kot filter med iskanji za vir. Po potrebi se lahko dodajo dodatne značilnosti za nadaljnje podrobneje določanje iskanja.

Nastavitve pogleda lahko prilagodite tudi za boljši pregled razpoložljivosti virov. Obstajajo možnosti prikaza urne, dnevne, tedenske, mesečne, četrtletne in letne razpoložljivosti. Obstaja tudi možnost prikaza razpoložljive in preostale zmogljivosti virov. Ta možnost je uporabna za upravljanje časa, ko ocenjujete razpoložljivi čas za dejavnosti ali razpoložljivost virov.

Projektni vodja lahko na strani izbere vlogo in nato, če je na voljo vir, ki ustreza zahtevi, izbere rezervacijo vira za zapolnitev vloge. Upoštevajte, da virov na tej točki v fazi načrtovanja ni treba rezervirati. Ko ustvarite SČD, lahko vloge nadomestite z zaposlenimi viri za projekt. Če se vloge v SČD nadomestijo z dodeljenimi viri, nastavitev virov samodejno posodobi seznam in razporejanje projektne skupine.

[![Seznam projektne skupine, ki vključuje vloge in dejanske vire](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projektni vodja ima različne možnosti za rezervacijo vira za projekt, npr. **Preostala zmogljivost**, **Polna zmogljivost**, **Odstotek zmogljivosti** in **Določanje ur**. Te možnosti rezervacije lahko kadar koli prekličete, če se dodelitve virov spremenijo. Podprti sta dve vrsti rezervacij:

- **Veljavna rezervacija** – Rezervacija vira je bila odobrena in potrjena za delo na angažmaju za navedeno trajanje.
- **Začasna rezervacija** – Rezervacija vira je bila okvirno nastavljena za delo na angažmaju za navedeno trajanje.

Naslednji postopek opisuje, kako ustvarite projektno ekipo.

### <a name="create-a-project-team"></a>Ustvarjanje projektne ekipe

1. Na strani seznama **Vsi projekti** izberite projekt, nato pa izberite **Uredi**.
2. Na zavihku **Projektna ekipa in načrtovanje** v polju **Končni datum urnika** vnesite začetni datum urnika plus en mesec. Na primer, če je začetni datum urnika 24. junij 2017 (24. 6. 2017), vnesite **24. 6. 2017**.
3. Izberite **Dodaj**.
4. V podoknu **Dodaj vloge v projekt** v polju **Vloga** izberite **Višji projektni vodja**.
5. Izberite **Zahtevane sposobnosti**.
6. Na strani **Izbira značilnosti** so značilnosti, ki ste jih prej nastavili za vlogo višjega projektnega vodje, privzeto izbrane. Izberite **V redu**.
7. Na strani **Dodaj vloge v projekt** v polje **Število virov** vnesite **1**.
8. V polju **Vir** iskanje prikaže vse vire, ki imajo zahtevane sposobnosti. Izberite **Daniel Goldschmidt**, nato pa izberite **Ustvari**.
9. Na strani **Projekt** izberite **Dodaj**.
10. V podoknu **Dodaj vloge v projekt** v polju **Vloga** izberite **Član ekipe**. V polje **Število virov** vnesite **5**.
11. Izberite **Ustvari**.
12. Na strani **Projekti** izberite **Zapolni vir**.

## <a name="resource-capacity-synchronization"></a>Sinhronizacija zmogljivosti vira
Procesi za sinhronizacijo virov pomagajo zagotoviti, da se informacije za koledar in osnovni koledar stekajo navzdol v razporejanje virov projekta. Če je koledar spremenjen, procesi izvedejo zahtevane spremembe za razporejanje virov projekta. Procesi pripomorejo tudi k izboljšanju učinkovitosti, ker se informacije o virih koledarja vnaprej sinhronizirajo. Zato se posodobitve informacij o razporejanju virov pojavijo hitreje. Priporočamo, da procese razporedite kot paket, namesto enega po enega. V nasprotnem primeru obstaja nevarnost, da bo kdo pozabil vključujoče datume, ko so bile informacije nazadnje sinhronizirane. Če se ne uporabljajo vključujoči datumi, lahko med sinhronizacijo datumov pride do vrzeli.

![Sinhronizacija koledarja](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sinhronizacija zbiranj zmogljivosti vira

Proces sinhronizacije je zasnovan za sinhronizacijo vseh informacij koledarja virov. Te informacije vključujejo informacije osnovnega koledarja o vseh spremembah tabele zmogljivosti koledarja virov projekta. Če so v projekt dodani novi viri, sinhronizacija pomaga zagotoviti, da so na voljo posodobljene informacije koledarja. To sinhronizacijo lahko izvedete kadar koli.

Priporočamo uporabo paketa. Možnosti so na voljo med sinhronizacijo rezervacij zmogljivosti.

1. Izberite **Vodenje projektov in računovodstvo** &gt; **Redno** &gt; **Sinhronizacija zmogljivosti** &gt; **Sinhronizacija zbiranj zmogljivosti vira**.
2. Nastavite možnosti v naslednji tabeli.

    | Možnost      | Opis |
    |-------------|-------------|
    | Koda obdobja | Izbirno izberite kodo intervala datuma glavne knjige, da nastavite začetni in končni datum za proces sinhronizacije za zbiranja zmogljivosti vira. |
    | Začetni datum  | Vnesite začetni datum za proces sinhronizacije za zbiranja zmogljivosti vira. |
    | Končni datum    | Vnesite končni datum za proces sinhronizacije za zbiranja zmogljivosti vira. |

[![Proces sinhronizacije](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Nastavitev vloge na predlogah SČD
Projektni vodje lahko nastavijo predloge SČD, ki jih lahko uporabijo, ko ustvarjajo SČD za nove projekte. Projektni vodje lahko dodajo vloge, ko ustvarijo predlogo. Uporabite naslednji postopek za dodelitev vloge predlogi SČD.

1. Izberite **Vodenje projektov in računovodstvo** &gt; **Nastavitev** &gt; **Projekti** &gt; **Predloge strukturirane členitve dela**.
2. Izberite **Podrobnosti** za izbrano predlogo SČD.
3. Izberite opravilo na seznamu in nato v polju **Vloga** izberite vlogo za dodelitev opravilu.

### <a name="work-with-a-wbs"></a>Delo s SČD

Ustvarite lahko nov SČD, lahko pa kopirate SČD iz obstoječe predloge SČD. Projektni vodja lahko zlahka upravlja vire z dodeljevanjem vlog novim opravilom v SČD. Vloge je mogoče zamenjati po pridobitvi vira ali po prepoznavanju potrjenega vira za delo na opravilu. Ta prilagodljivost omogoča projektnim vodjem izvajanje naslednjih opravil:

- Prepoznavanje števila virov, ki so potrebni za delovne pakete SČD.
- Ocenjevanje stroškov projektov.
- Določanje predhodnega proračuna.
- Ocenjevanje trajanja dejavnosti na podlagi vlog in virov.
- Razvoj nekaterih načrtov vodenja projektov na podlagi razpoložljivih informacij o projektu.

Dodatne možnosti so bile dodane v SČD za boljšo uporabo funkcije iskanja virov.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Možnost</th>
<th>Opis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dodelitve virov</td>
<td>Oglejte si dodeljene vire, datume, število ur in vrsto rezervacije za opravila v SČD.</td>
</tr>
<tr class="even">
<td>Samodejno ustvarjanje ekipe</td>
<td>Samodejno dodajte načrtovane vire z uporabo vlog, ki so povezane z opravilom. Storitev Finance samodejno predlaga načrtovane vire z uporabo analize odločitev z več merili, ki temelji na vlogah. Ko so bile vloge in obseg (ure) nastavljeni za opravila v SČD ter je bila struktura izdana, izberite <strong>Samodejno ustvarjanje ekipe</strong>. Zahtevano število načrtovanih virov se doda v SČD in zavihek <strong>Načrtovanje projekta in ekipe</strong>.</td>
</tr>
<tr class="odd">
<td>Vir (spustni seznam)</td>
<td>Na strani <strong>Zagon dodelitve vira</strong> lahko izberete vire za veljavne rezervacije ali začasne rezervacije na podlagi določenega trajanja. Prilagodite lahko nastavitve ogleda, da vidite in nastavite trajanje dejavnosti virov. Lahko izberete in dodelite vire na ravni delovnega paketa z uporabo naslednjih možnosti:
<ul>
<li><strong>Sprejem</strong> – Potrdite spremembe vira, ki je dodeljen opravilu.</li>
<li><strong>Preklic</strong> – Prekličite spremembe vira, ki je dodeljen opravilu.</li>
<li><strong>Samodejna dodelitev</strong> – Razpoložljivi zaposleni vir, ki ima ujemajočo se vlogo, je samodejno izbran in dodeljen izbranemu opravilu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na strani **Vsi projekti** izberite projekt **2. faza nadgradnje XYZ**.
2. Izberite **Načrtovanje** &gt; **Dejavnosti** &gt; **Strukturirana členitev dela**.
3. Izberite **Novo**, da dodate naslednje dejavnosti prve stopnje v SČD:

    - Zagon
    - Načrtovanje
    - Izvajanje
    - Spremljanje in nadzor
    - Zaprto

4. Nastavite datume in obseg (ure), kot je prikazano na naslednji sliki.

    [![Nastavitev datumov in obsega](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Izberite vrstico opravila **Zagon** in nato v polju **Vloga** izberite **Višji projektni vodja**.
6. Izberite **Objavi**.
7. V isti vrstici v polju **Vir** izberite **Daniel Goldschmidt**, nato pa izberite **Sprejem**.
8. Izberite vrstico opravila **Načrtovanje** in nato v polju **Vloga** izberite **Poslovni analitik**.
9. Izberite **Objava**, nato pa izberite **Samodejno ustvarjanje ekipe**.
10. V polju za sporočilo, ki se prikaže, izberite **Da**.
11. V polju **Vir** potrdite, da je vrednost **Poslovni analitik 1**.
12. Za vir **Poslovni analitik 1** odprite iskanje in izberite **Zagon dodelitev virov**. Nato izberite delavca za opravilo.
13. Izberite **Začasna rezervacija** &gt; **Polna zmogljivost**.

    > [!NOTE] 
    > Ne prejmete opozorila, da je navedeni vir zdaj 2, ker število virov ostaja 1.

14. Na strani **Strukturirana členitev dela** potrdite dodelitve virov na SČD in nato izberite **Shrani**.

## <a name="resource-fulfillment-for-planned-resources"></a>Zapolnitev virov za načrtovane vire
Projektni vodja lahko načrtuje zahtevane vloge virov za projekt. Upravitelj virov bo te načrtovane vire videl kot zahteve na strani **Zapolnitev virov** in lahko dodeli dejanske vire.

1. Na strani **Vsi projekti** izberite projekt **2. faza nadgradnje XYZ**.
2. Izberite **Projekt** in nato izberite **Uredi**.
3. Na zavihku **Projektna ekipa in načrtovanje** izberite **Dodaj**.
4. V pogovornem oknu **Dodaj vloge** izberite vlogo **Razvijalec programske opreme**.
5. Izberite **Ustvari** in nato zaprite stran projekta.
6. Na strani **Zapolnitev virov** izberite **Razvijalec programske opreme 1** za projekt **2. faza projekta posodobitve XYZ**.
7. Izberite delavca in nato izberite **Dodeli**.
8. Potrdite, da je bila vrstica za **Razvijalec programske opreme 1** odstranjena za projekt **2. faza projekta nadgradnje XYZ**.
9. Na zavihku **Projektna ekipa in načrtovanje** za projekt **2. faza nadgradnje XYZ** potrdite, da je bil delavec, ki ste ga izbrali v prejšnjem koraku, dodan kot **Razvijalec programske opreme**.

## <a name="requests-for-project-resources"></a>Zahteve za vire projekta
Funkcionalnost za razporejanje virov projekta samo upraviteljem virov omogoča razporejanje zaposlenih virov angažmajem ali projektom. Če želite omogočiti to funkcionalnost, dokončajte naslednja opravila ali potrdite, da so bila dokončana:

- Nastavite zaporedja številk.
- Nastavite poteke dela vodenja projektov in računovodstva.
- Omogočite poteke dela zahtev za vire.

Ko so prejšnja opravila dokončana, lahko izvedete naslednja opravila, kot je potrebno:

- Ustvarite zahtevo za vir iz začasno rezerviranega zaposlenega vira.
- Spremljajte zahteve za vire.
- Izpolnite zahteve za vire.
- Zahtevajte zaposleni vir iz SČD.
- Rezervirajte vire za projekt, ne da bi morali zahtevati zaposleni vir.

## <a name="monitor-project-teams"></a>Spremljanje projektnih ekip
1. Na strani **Vsi projekti** izberite povezavo **ID projekta** za projekt **2. faza nadgradnje XYZ**.
2. Na zavihku za hiter dostop **Projektna ekipa in načrtovanje** potrdite, da so viri projekta, ki so navedeni, pravilni.
