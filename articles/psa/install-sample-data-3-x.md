---
title: Namestitev vzorčnih podatkov
description: Ta tema vsebuje informacije o namestitvi vzorčnih podatkov v storitvi Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 3c9cca7aa9d85bb38e48820b361ba07923ceddbd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132443"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Namestitev vzorčnih podatkov za aplikacijo Project Service

Microsoft vam za lažje ustvarjanje predstavitvenih okolij nudi pakete vzorčnih podatkov, ki jih lahko prenesete in ki prikazujejo zmogljivosti vaših aplikacij. Obstajata dve vrsti paketov vzorčnih podatkov:
- referenčni/namestitveni podatki
- predstavitveni podatki (referenčni/namestitveni in transakcijski podatki, kot so delovni nalogi in projekti)

Vzorčne **referenčne** pakete podatkov lahko prenesete v treh različnih paketih, da lahko namestite podatke samo za Project Service oz. Field Service ali pa namestite vzorčne podatke za obe aplikaciji hkrati.

Vzorčni paketi namestitvenih/referenčnih podatkov so:

- [**V902PSMasterData** – Project Service, samo različica 3.x](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** – Field Service, samo različica 8.x](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** – Field Service 8.x in Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Najnovejši paket **predstavitvenih** podatkov je:

 - [**FPSDemoData** – Field Service 8.x in Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Navodila za namestitev se nekoliko razlikujejo v razdelku uporabnikov za ustvarjanje in konfiguracijo, ostalo pa je enako kot v prejšnji [**objavi v spletnem dnevniku**](https://aka.ms/fpsdemodatablog). Ta paket vsebuje manjši nabor predstavitvenih podatkov, njegova namestitev pa traja približno 3 ure.

Ti paketi vzorčnih podatkov so na voljo samo v angleščini.

> [!IMPORTANT]
> **Vzorčnih podatkov po namestitvi ni mogoče odstraniti.** Pakete namestite samo v sisteme za predstavitev, ocenjevanje, usposabljanje in preskušanje. Upoštevajte tudi, da ni mogoče namestiti posameznega paketa, potem pa še drugega posameznega paketa. (Z drugimi besedami: ne morete namestiti paketa **FSMasterData** in potem paketa **PSMasterData** ali obratno.) Če menite, da boste kdaj v prihodnosti potrebovali vzorčne podatke za obe aplikaciji, namestite paket **v902FPSMasterData**.

Ko namestite katerega koli od paketov vzorčnih podatkov, bo med postopkom namestitve program:

- Ustvaril ali nastavil privzete parametre za uporabo aplikacije Project Service oz. Field Service ali obeh aplikacij (če so na voljo).

- Uvozil vzorčne podatke za aplikaciji, npr. vire, ki jih je mogoče rezervirati, vloge znotraj aplikacije, cenike s prodajnimi in lastnimi cenami, organizacijske enote, zapise prodajnega postopka in druge entitete, prek katerih so predstavljene ključne zmogljivosti aplikacij.  

S paketom **predstavitvenih podatkov** prejmete zgornje in dodatne transakcijske podatke, kot so delovni nalogi in projekti.

Se sprašujete, katere zmogljivosti lahko preizkusite z uporabo vzorčnih podatkov? Oglejte si izmišljeni scenarij za Fabrikam Robotics, ki je na voljo v [tehničnih opombah](#technical-notes).

Če imate vprašanja glede namestitve paketov vzorčnih podatkov, [nam pošljite e-poštno sporočilo na naslov fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Zahteve

Namestitveni protokol za vaš ciljni primerek (organizacijo) predvideva naslednje informacije:

- Osnovni jezik je angleščina, osnovna valuta pa ameriški dolar (USD, $).

- Organizacija še nima nobenih podatkov o rešitvah Project Service ali Field Service, razen morda le osnovne privzete podatke, do katerih dostopa vsaka nova organizacija.

- Pravilna različica poslovne aplikacije je že nameščena:
       
    - **Za FPSDemoData ali v902FPSMasterData:** v organizaciji sta nameščeni aplikaciji Field Service (različica 8.x) in Project Service (različica 3.x).

    - **Za v902PSMasterData:** v organizaciji je nameščena aplikacija Project Service, različica 3.x.

    - **Za v902FSMasterData:** v organizaciji je nameščena aplikacija Field Service, različica 8.x.

> [!NOTE]
> Če želite vzorčne podatke namestiti poleg obstoječega preskusnega ali predstavitvenega okolja za Project Service ali Field Service, ki že vsebuje podatke (ni priporočeno), začasno prekinite prva varnostna preverjanja, ki jih izvede namestitveni program. Za več informacij glejte tehnične opombe v spodnjem razdelku.

## <a name="prepare-for-installation"></a>Priprava na namestitev

Namestitveni program zaženite v računalniku z najnovejšo različico operacijskega sistema Windows (priporočamo Windows 10).

Računalnik naj med namestitvijo ostane povezan v omrežje, namestitev pa lahko traja do **1 ure** za **namestitvene/referenčne podatke**. (Običajno namestitev traja približno 30 minut za **FPSMasterData**, kar vsebuje vzorčne podatke za obe aplikaciji.) Za **FPSDemoData** bo namestitev trajala približno **3 ure**.

V računalniku naj bo izklopljena funkcija ohranjevalnika zaslona. V nasprotnem primeru boste ob zagonu ohranjevalnika zaslona morda izgubili poverilnice seje, potrebne za namestitev (razen če bo vaša seja v tem času ostala aktivna).

> [!div class="mx-imgBorder"]
> ![Posnetek zaslona nastavitev ohranjevalnika zaslona z izklopljenim ohranjevalnikom zaslona](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Prenos in razpakiranje

Namestitveni program za vzorčne podatke rešitev Project Service in Field Service je na voljo kot samorazširljiva izvedljiva datoteka. Koraki so enaki ne glede na paket, ki ga nameščate, z izjemo imen datotek, ki so odvisna od nameščenega paketa vzorčnih podatkov.

Po prenosu paketa zaženite datoteko .exe ter sprejmite pogoje in določila, da razpakirate stisnjeno datoteko .zip. Vsebino datoteke nato izvlecite v želeno mapo v računalniku.

Ko razpakirate datoteko .zip, morate v skladu z vašim operacijskim sistemom in varnostnimi nastavitvami izvesti naslednje korake:

1. Poiščite in z desno tipko miške kliknite datoteko **FPSDemoData.dll** v mapi **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Izberite **Odblokiraj**.

3. Izberite **Uporabi**.

4. izberite **V redu**.


## <a name="create-or-configure-users"></a>Ustvarjanje in konfiguracija uporabnikov

Za paket **FPSDemoData** je potrebnih šest uporabnikov, medtem ko je za paket **FPSMasterData** potreben en uporabnik. Glejte ustrezen paket za svoj paket vzorčnih podatkov.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Ustvarjanje in konfiguracija uporabnikov – paketi namestitvenih/referenčnih podatkov

Ko namestite paket **FPSMasterData**, izberite uporabnika, imenovanega »Spencer Low«, in zanj uporabite opisane nastavitve. Za pravilno namestitev paketa ustvarite (ali začasno preimenujte) uporabnike v okolju, tako da bodo ustrezali konfiguraciji vzorčnih podatkov.

Za ustvarjanje ali konfiguracijo uporabnikov kliknite **Nastavitve** > **Varnost** > **Uporabniki** in sledite navodilom:

1. Uporabniku UserFullname="Spencer Low" z uporabniškim imenom "spencerl" (**male črke**) dodelite vlogo vodje projekta in upravitelja praks.

2. Izberite uporabnika **Spencer Low** in nato **Upravljanje vlog**. Poiščite in izberite vlogo **Skrbnik sistema**, nato pa izberite **V redu**, da Spencerju Lowu dodelite polne skrbniške pravice. Tako boste zagotovo vzorčne zapise ustvarili s pravilnim uporabniškim lastništvom in torej pravilno izpolnili poglede.

3. Znotraj prenesenega paketa posodobite datoteko za preslikavo podatkov z e-poštnimi naslovi privzetega uporabniškega konteksta. Če želite to storiti, odprite **PkgFolder** ter poiščite in odprite datoteko **ImportUserMapFile.xml** v Beležnici (oz. programu Visual Studio ali drugem urejevalniku XML-jev). Polje **DefaultUserToMapTo=** nastavite na e-poštni naslov uporabnika Spencerja Lowa.

4. Če za uporabnika niste izbrali Spencerja Lowa z uporabniškim imenom **spencerl**, boste morali posodobiti dodatno datoteko. Odprite datoteko **DemoDataPreImportConfig.xml** in poiščite oznako **userstocreateandconfigure**. Oznako **\<login\>** posodobite z uporabniškim imenom uporabnika Jana Mlinarja. Za več informacij glejte [tehnične opombe](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Ustvarjanje in konfiguracija uporabnikov – paket predstavitvenih podatkov

Za paket predstavitvenih podatkov je potrebnih šest uporabnikov. Za pravilno namestitev paketa naredite naslednje:

 1. Ustvarite ali začasno preimenujte obstoječe uporabnike, da bodo ustrezali konfiguraciji vzorčnih podatkov, tako, da se pomaknete v razdelek **Nastavitve** > **Varnost** > **Uporabniki**.
 
    Te vloge so potrebne le za predstavitve, ki temeljijo na osebah.  
    - Polno ime uporabnika = »David So« kot serviser za Field Service   
    - Polno ime uporabnika = »Jamie Reding« kot odpravitelj storitev za stranke in rešitve Field Service   
    - Polno ime uporabnika = »Molly Clark« kot upraviteljica kupcev   
    - Polno ime uporabnika = »Spencer Low« kot upravitelj praks in vodja projektov  
    - Polno ime uporabnika = »Veronica Quek« kot članica skupine   
    - Polno ime uporabnika = »William Contoso«
  
2. Zaradi uvoza predstavitvenih podatkov dodelite šest uporabnikov nad vlogo skrbnika, da se vzročni zapisi pravilno uvozijo. 

3. Odprite mapo **PkgFolder** ter nato poiščite in odprite datoteko **ImportUserMapFile.xml**. Posodobite polja **Novo =** za e-poštne naslove ustreznih uporabnikov v svojem sistemu.

   > [!div class="mx-imgBorder"]
   > ![Posnetek zaslona datoteke UserMapFile](media/sample-data-7.png)

4. Če ima vaše polno uporabniško ime »Spencer Low« drugačen ID uporabnika kot **»spencerl«**, boste morali posodobiti dodatno datoteko. Odprite **DemoDataPreImportConfig.xml** in poiščite oznako **userstocreateandconfigure**. Posodobite oznako **\<login\>** s spremenljivko prijavniId (razlikovanje med velikimi in malimi črkami). 

5. Koledar prvega uporabnika (v oznaki **userstocreateandconfigure**) se uporablja za dopolnitev delovnega časa za vse vire, ki jih je mogoče rezervirati, pri uvozu predstavitvenih podatkov. Pomaknite se na razdelek **Nastavitve** > **Varnost** > **Uporabniki** in poiščite svojega uporabnika z imenom »Spencer Low« ter odprite možnost »Delovni čas«. Uredite obstoječi delovni čas tako, da izberete možnost **Celoten ponavljajoč se tedenski razpored od začetka do konca**. Zagotovite, da je **delovni čas nastavljen na 8.00–17.00 (9 ur) od ponedeljka do petka, časovni pas pa na pacifiški čas (ZDA in Kanada)**. To je potrebno za zagotovitev, da se plošči projekta in razporeda prikažeta, kot je pričakovano.

**Priporočilo:** varnostno kopijo vaše organizacije ustvarite že zdaj, da se vam ne bo treba vrniti na začetek, če gre med namestitvijo vzorčnih podatkov kaj narobe. Za več informacij glejte razdelek [Varnostno kopiranje in obnovitev primerkov](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Zagon čarovnika Package Deployer

1. Poiščite in zaženite datoteko **PackageDeployer.exe** v mapi **v902FPSMasterData** ALI **PackageDeployer_FPSDemoData**.

2. Sprejmite pogoje in določila.

3. V naslednjem oknu:

   a. Izberite vrsto uvajanja programa **Office 365**.

   b. Uporabite uporabniško ime in geslo skrbnika sistema, ki je konfiguriran v razdelku »Ustvarjanje in konfiguriranje uporabnikov« (»Spencer Low«, z uporabniškim imenom »spencerl«).

   c. Prepričajte se, da ste izbrali možnost **Prikaži seznam organizacij, ki so na voljo**.

      > [!div class="mx-imgBorder"]
      > ![Posnetek zaslona orodja Package Deployer z izbrano možnostjo »Prikaži seznam organizacij, ki so na voljo«](media/sample-data-2.png)

4. Izberite organizacijo, v kateri želite namestiti vzorčne podatke.

5. Izberite **Naprej**, da se prikaže pogovorno okno **Nastavitev predstavitvenih podatkov**.

   > [!div class="mx-imgBorder"]
   > ![Posnetek zaslona okna stanja namestitvenega programa predstavitvenih podatkov](media/sample-data-3.png)

6. Preden nadaljujete, upoštevajte, da namestitev vzorčnih podatkov lahko traja do ene ure (običajno okoli 10 minut). Poskrbite, da med namestitvijo računalnik ostane vklopljen in povezan v omrežje ter da vaša seja ostane aktivna.   

7. Ko ste pripravljeni, kliknite **Naprej**, da začnete postopek za namestitev vzorčnih podatkov. Ko so vzorčni podatki naloženi, kliknite **Dokončaj**.

## <a name="verify-the-sample-data-installation"></a>Preverjanje namestitve vzorčnih podatkov

Preverite, ali se ustrezno prikažejo število zapisov in tipi entitet, navedeni v izmišljenem scenariju za Fabrikam Robotics.

Ko se v celoti naložijo vzorčni podatki, se vpišite kot uporabnik Spencer Low in potrdite naslednje:

- Če ste namestili aplikacijo Project Service, kliknite **Project Service** > **Nastavitve** > **Ceniki**. Potrdite, da so za vsako državo/regijo v naboru podatkov na voljo stroški in zneski računov v ustrezni valuti.

- Če ste namestili aplikacijo Project Service, odprite **Universal Resource Scheduling** > **Nastavitve** > **Organizacijske enote**. Potrdite, da je za vsako enoto organizacije (razen pri vnosih mest) na voljo cenik z lastnimi cenami v ustrezni valuti. Če kakšna organizacija manjka, poiščite in z njo povežite pravilni cenik z lastnimi cenami.

- Če ste namestili aplikacijo Field Service, kliknite **Project Service** > **Nastavitve** > **Ceniki**. Potrdite, da so stroški in zneski računov na voljo. Kliknite **Field Service** > **Nastavitve** > **Ceniki** in se prepričajte, da so za vsako državo/regijo v naboru podatkov na voljo stroški in zneski računov v ustrezni valuti.

  > [!div class="mx-imgBorder"]
  > ![Posnetek zaslona aktivnih cenikov](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Posnetek zaslona aktivnih organizacijskih enot](media/sample-data-5.png)

## <a name="technical-notes"></a>Tehnične opombe

Več tehničnih podrobnosti o namestitvi teh podatkov najdete spodaj.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Namestitev vzorčnih podatkov vrh že obstoječih podatkov (ni priporočljivo)

Opomba: če želite namestiti vzorčne podatke poleg obstoječega preskusnega ali predstavitvenega okolja za Field Service ali Project Service, ki že vsebuje lastne podatke, začasno prekinite prva varnostna preverjanja, ki jih izvede namestitveni program.

V ta namen odprite mapo **PkgFolder** ter poiščite in v Beležnici (ali drugem urejevalniku XML) odprite datoteko **DemoDataPreImportConfig.xml**.

Poiščite naslednjo vrednost in nastavitev spremenite z pravilne na napačno:

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Ob tej spremembi bo namestitveni program obšel nekatera pomembna varnostna preverjanja in med drugim potrdil, da:

- Je aktiven le en zapis **organizacijske enote**, ki ga bo nato preimenoval v **Fabrikam ZDA**.

- Je aktiven le en zapis **predloge za delo**.

- Obstaja le en zapis **parametra projekta** in bo nato ta vnos preimenoval v **parametre**.

### <a name="configuration-components"></a>Konfiguracijske komponente

V tej datoteki za konfiguracijo pred uvozom je več drugih konfiguracijskih komponent. Za tehnične uporabnike – nekatere od teh vključujejo:

- **\<RequiredSolutions\>** določa, katere rešitve je treba namestiti, in njihove številke različic.

- **\<InstallSampleData\>** nadzoruje, ali bodo za aplikacije nameščeni vnaprej pripravljeni vzorčni podatki.

    - false – preskoči namestitev teh vgrajenih podatkov (ki so odstranljivi)

    - true – namesti vgrajene podatke sočasno z namestitvijo vzorčnih podatkov rešitev FS in PSA

- **\<PreImportDataCollection\>** določa, katere podatkovne preslikave datotek z nestrukturiranimi podatki in kateri povezani zapisi bodo uvoženi pred namestitvijo glavnih vzorčnih podatkov.

- **\<EntitiesToEnableScheduling\>** določa, katere entitete naj bodo omogočene za rezervacijo v storitvi Microsoft Dynamics Scheduling (oz. Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** določa, kateri viri, ki jih je mogoče rezervirati, bodo ustvarjeni (če še ne obstajajo), preden se izvede uvoz vzorčnih podatkov. Upoštevajte, da se viri vzorčnih podatkov izvornega sistema, ki jih je mogoče rezervirati, ujemajo z zapisi virov ciljnega sistema, ki jih je mogoče rezervirati, kar se tiče polnega imena in podatkov za prijavo. Imen v tej predkonfiguracijski datoteki zato NI mogoče spremeniti, razen če pred tem v ciljni sistem uvozite vzorčne podatke in uporabite ta imena, nato pa vire, ki jih je mogoče rezervirati, preimenujete po lastni izbiri, v skladu z zapisi omogočenih uporabnikov, in ponovno izvozite podatke, da jih nato uvozite v želeni končni sistem (in hkrati ustrezno posodobite nove in stare vnose preslikave **ImportUserMapFile.xml**).

- **\<PluginsToDisable\>** točno določa vtičnike z vrstičnimi postavkami, ki jih je treba onemogočiti pri uvozu vzorčnih podatkov in nato pozneje znova omogočiti.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Izmišljeni scenarij »Fabrikam Robotics«

S paketi vzorčnih referenčnih podatkov za Field Service in Project Service se namesti **rešitev Fabrikam Manufacturing Master Data (v3.0.0.0)** skupaj s približno 4000 zapisi in približno 40 različnimi entitetami. Posamezni paketi vzorčnih podatkov za Field Service oz. Project Service vsebujejo podmnožico vzorčnih podatkov rešitve **v902FPSMasterData** za izbrano aplikacijo. S paketom **predstavitvenih podatkov** se namesti **rešitev Fabrikam Manufacturing Demo Data (v3.0.0.7)** s približno 22.000 zapisi med 148 entitetami.

Izmišljeno podjetje Fabrikam Robotics je proizvajalec elektronskih robotov za tekoči trak in je znano po visoki kakovosti izdelkov, inovacijah in odličnih storitvah za stranke, kar vključuje načrtovanje namestitve, uvajanje in sprotne vzdrževalne storitve. Fabrikam ima sedež v Združenih državah Amerike (Fabrikam ZDA), svoje projektno osnovane storitve pa nudi tudi v Franciji, Indiji, Združenem kraljestvu in Švici.

Postopki za Field Service se izvajajo v Združenih državah, predvsem v širši okolici mesta Seattle. Podjetje se osredotoča na izboljšanje povezljivosti interneta stvari (IoT) ter tako spremlja storilnost sredstev stranke in nudi vedno bolj proaktivne storitve na kraju samem.

Podroben pregled vzorčnih podatkov je, kot sledi:

- Skupni elementi vzorčnih podatkov (velja za obe aplikaciji)

    - 1 uporabnik

    - 71 računov

    - 137 stikov

    - Različni tipi transakcij in kategorije

    - 50 izdelkov in 1 cenik izdelkov

    - 14 cenikov

    - 31 značilnosti (znanja virov) v 2 modelih ocenjevanja s 3 ravni (vrednosti ocen)

- Project Service

    - 8 organizacijskih enot

    - 6 stopenj uporabe glede na vlogo

    - Več kot 2800 specifikacij glede vloge in cene

- Field Service

    - 4 območja

    - 5 tipov delovnih nalogov

    - 22 sredstev stranke

    - 9 tipov nezgod s številnimi povezanimi lastnostmi virov (9), storitvami (13) in opravili storitev (13)
   
S paketom **predstavitvenih podatkov** se namesti približno 179 delovnih nalogov, 12 projektov in povezanih transakcijskih podatkov. 

### <a name="change-the-work-hours-for-sample-resources"></a>Sprememba delovnih ur za vzorčne vire

Za vse vire, ki jih je mogoče rezervirati, je privzet 24-urni koledar delovnih ur.

Če želite spremeniti delovne ure za vzorčne vire, ki jih je mogoče rezervirati, odprite **Universal Resource Scheduling** > **Načrtovanje** > **Viri**.

Izberite uporabnika (na primer »Spencer Low«) in spremenite Spencerjev delovni čas na delovni čas, ki ga želite uporabiti za več uporabnikov. Kliknite **Universal Resource Scheduling** > **Nastavitve** > **Predloge za delovne ure** in uredite zapis **Privzeta predloga za delo**. V polju **Vir predloge** izberite uporabnika z delovnim časom, ki ga želite uporabiti za druge vire. Odprite **Universal Resource Scheduling** > **Razporejanje** > **Viri** > **Aktivni viri, ki jih je mogoče rezervirati**. Izberite vire, ki jih želite spremeniti, in nato izberite **Nastavi koledar**. Na spustnem seznamu **Predloga za delo**, izberite predlogo **Privzeti delovni čas** ali drugo predlogo s pravilnim virom predlog. Pri plošči razporeda bi morali videti, da imajo viri zdaj posodobljen delovni čas.

> [!div class="mx-imgBorder"]
> ![Posnetek zaslona aktivnih virov, ki jih je mogoče rezervirati](media/sample-data-6.png)
