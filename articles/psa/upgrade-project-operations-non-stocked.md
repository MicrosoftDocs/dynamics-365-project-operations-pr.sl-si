---
title: Aplikacijo Project Service Automation nadgradite na aplikacijo Project Operations
description: Ta članek zagotavlja pregled procesa nadgradnje z aplikacije Microsoft Dynamics 365 Project Service Automation na aplikacijo Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736687"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Aplikacijo Project Service Automation nadgradite na aplikacijo Project Operations

Z veseljem objavljamo drugo od treh faz za nadgradnjo z aplikacije Microsoft Dynamics 365 Project Service Automation na aplikacijo Microsoft Dynamics 365 Project Operations. Ta članek zagotavlja pregled za stranke, ki se podajajo na to razburljivo potovanje. 

Program za izvedbo nadgradnje bo razdeljen v tri faze.

| Izvedba nadgradnje | 1. faza (januar 2022) | 2. faza (november 2022) | 3. faza (april 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Brez odvisnosti od strukturirane členitve dela (SČD) za projekte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Vmesnik SČD je vključen v trenutno podprte omejitve aplikacije Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| SČD zunaj trenutno podprtih omejitev aplikacije Project Operations, vključno s podporo za Project desktop client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funkcije procesa nadgradnje 

Kot del procesa nadgradnje smo na zemljevid mesta dodali dnevnike nadgradnje, da skrbnikom omogočimo lažje prepoznavanje napak. Poleg novega vmesnika bodo dodana nova pravila za preverjanje veljavnosti, da se zagotovi celovitost podatkov po nadgradnji. V proces nadgradnje bodo dodane naslednja preverjanja veljavnosti.

| Preverjanje veljavnosti | 1. faza (januar 2022) | 2. faza (november 2022) | 3. faza  |
|-------------|------------------------|---------------------------|---------------------------|
| Veljavnost vmesnika SČD bo preverjena glede na pogoste kršitve celovitosti podatkov (na primer dodelitve virov, ki so povezane z istim nadrejenim opravilom, vendar imajo različne nadrejene projekte). | | :heavy_check_mark: | :heavy_check_mark: |
| Veljavnost vmesnika SČD bo preverjena glede na [znane omejitve za Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| Veljavnost vmesnika SČD bo preverjena glede na znane omejitve za Project Desktop Client. | |  | :heavy_check_mark: |
| Viri, ki jih je mogoče rezervirati, in koledarji projektov bodo ovrednoteni glede na pogoste izjeme pravila za nezdružljive koledarje. | | :heavy_check_mark: | :heavy_check_mark: |

V 2. fazi bodo stranke, ki nadgradijo na aplikacijo Project Operations, svoje obstoječe projekte nadgradile na izkušnjo samo za branje za načrtovanje projektov. V tej izkušnji samo za branje bo celoten vmesnik SČD viden v mreži za sledenje. Za urejanje vmesnika SČD lahko vodje projektov na glavni strani projekta izberejo možnost [**Pretvori**](/PSA-Upgrade-Project-Conversion.md). Postopek v ozadju nato posodobi projekt, tako da podpira novo izkušnjo razporejanja projekta iz storitve Project for the Web. Ta faza je primerna za stranke, ki imajo projekte znotraj [znanih omejitev za Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

V 3. fazi bo dodana podpora za Project Desktop Client za prednost strank, ki želijo še naprej urejati svoje projekte iz te aplikacije. Če pa so obstoječi projekti pretvorjeni v novo izkušnjo Project for the Web, bo dostop do dodatka onemogočen za vsak pretvorjeni projekt.

## <a name="prerequisites"></a>Zahteve

Če želite biti upravičeni do 1. faze nadgradnje, morate izpolnjevati naslednja merila:

- Ciljno okolje ne sme vsebovati nobenih zapisov v entiteti **msdyn_projecttask**.
- Veljavne licence za aplikacijo Project Operations morajo biti dodeljene vsem aktivnim uporabnikom. 
- Proces nadgradnje morate potrditi v vsaj enem neprodukcijskem okolju, ki vsebuje reprezentativen nabor podatkov, ki je usklajen z vašim produkcijskim okoljem.
- Ciljno okolje je treba posodobiti na izdajo posodobitve 37 za aplikacijo Project Service Automation (V3.10.58.120) ali novejšo različico.

Če želite biti upravičeni do 2. faze nadgradnje, morate izpolnjevati naslednja merila:

- Veljavne licence za aplikacijo Project Operations morajo biti dodeljene vsem aktivnim uporabnikom. 
- Proces nadgradnje morate potrditi v vsaj enem neprodukcijskem okolju, ki vsebuje reprezentativen nabor podatkov, ki je usklajen z vašim produkcijskim okoljem.
- Ciljno okolje je treba posodobiti na izdajo posodobitve 37 za aplikacijo Project Service Automation (V3.10.58.120) ali novejšo različico.
- Okolja, ki vsebujejo opravila (msdyn_projecttask), so podprta le, če je skupno število opravil na projekt 500 ali manj.

Predpogoji za 3. fazo bodo posodobljeni, ko se bo bližal datum splošne dostopnosti.

## <a name="licensing"></a>Licenciranje

Če imate aktivne licence za Project Service Automation, lahko namestite in uporabljate aplikacijo Project Operations, ki vključuje vse zmogljivosti aplikacije Project Service Automation in še druge. Na ta način lahko preskusite zmogljivosti aplikacije Project Operations, medtem ko v proizvodnji še vedno uporabljate aplikacijo Project Service Automation. Po poteku licenc za Project Service Automation boste morali preiti na aplikacijo Project Operations. Ko načrtujete ta prehod, morate upoštevati, da licenca za Project Operations ne vključuje licence za Project Service Automation. Stranke, ki imajo scenarije, v katerih je uvedena aplikacija Project Service Automation, in morajo še naprej uporabljati ali povečati svoje licence za PSA, medtem ko načrtujejo prehod na aplikacijo Project Operations, lahko zahtevajo začasne licence za PSA na podlagi kupljenih licenc za Project Operations. Ena licenca za Project Service Automation bo izdana za eno licenco za Project Operations. Začasne licence za storitev PSA lahko zahtevate na tej povezavi: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Preskus in preoblikovanje prilagoditev

Za začetek uvozite vse prilagoditve v čisto okolje Project Operations (poenostavljena različica), s čimer potrdite, da je uvoz uspešen in da poslovni postopki potekajo po pričakovanjih.

Bodite pozorni na naslednje:

- Uvoz morda ne uspe zaradi manjkajočih odvisnosti. To pomeni sklicna polja prilagoditev ali druge komponente, ki so bile odstranjene v aplikaciji Project Operations. V tem primeru odstranite te odvisnosti iz razvojnega okolja.
- Če vaše neupravljane in upravljane rešitve vključujejo komponente, ki niso prilagojene, odstranite te komponente iz rešitve. Ko prilagodite entiteto **Projekt**, svoji rešitvi dodajte na primer samo glavo entitete. Ne dodajte vseh polj. Če ste že dodali vse podkomponente, boste morda morali ročno ustvariti novo rešitev in ji dodati ustrezne komponente.
- Obrazci in pogledi morda ne bodo prikazani po pričakovanjih. Če ste prilagodili katerega koli od pripravljenih obrazcev ali pogledov, lahko v nekaterih primerih prilagoditve preprečijo, da bi nove posodobitve v aplikaciji Project Operations začele veljati. Za prepoznavanje teh težav priporočamo, da vzporedno pregledate čisto namestitev aplikacije Project Operations in namestitev aplikacije Project Operations, ki vključuje vaše prilagoditve. Primerjajte obrazce, ki se najpogosteje uporabljajo v vašem podjetju, s čimer poskrbite, da je vaša različica obrazca še vedno smiselna in ne manjka ničesar od čiste različice obrazca. Opravite isto vrsto vzporednega pregleda za vse poglede, ki ste jih prilagodili.
- Med izvajanjem lahko pride do napake poslovne logike. Ker se veljavnost sklicev na polja v vaših vtičnikih ne preverja v času uvoza, lahko pride do napake poslovne logike zaradi sklicev na polja, ki ne obstajajo več, in morda prejmete sporočilo o napaki, ki je podobno temu primeru: »Entiteta 'Projekt' ne vsebuje atributa z vrednostjo Ime = 'msdyn_plannedhours' in NameMapping = 'Logično'.« V tem primeru spremenite svoje prilagoditve tako, da bodo uporabljale nova polja. Če v logiki vtičnika uporabljate samodejno ustvarjene razrede proxy in močno vrsto sklicev, razmislite o ponovnem generiranju teh proxyjev iz čiste namestitve. Na ta način lahko preprosto prepoznate vsa mesta, kjer so vaši vtičniki odvisni od opuščenih polj.

Ko posodobite svoje prilagoditve za čist uvoz aplikacije Project Operations, nadaljujte z naslednjimi koraki.

## <a name="end-to-end-testing-in-development-environments"></a>Celovito preskušanje v razvojnih okoljih

### <a name="initiate-upgrade"></a>Začetek nadgradnje 

1. V skrbniškem središču za Power Platform poiščite in izberite svoje okolje. Nato v aplikacijah poiščite in izberite možnost **Dynamics 365 Project Operations**.
2. Za začetek nadgradnje izberite možnost **Namesti**. Skrbniško središče za Power Platform bo to namestitev predstavilo kot novo namestitev. Zaznana bo prisotnost prejšnje različice aplikacije Project Service Automation, obstoječa namestitev pa bo nadgrajena.

    Po dokončanju nadgradnje, bi moralo okolje pokazati, da je aplikacija Project Operations nameščena, aplikacija Project Service Automation pa ne.

    Postopek lahko traja več ur, odvisno od količine podatkov v okolju. Osrednja ekipa, ki upravlja nadgradnjo, mora ustrezno načrtovati in izvajati nadgradnjo izven delovnega časa. Če je količina podatkov velika, je treba nadgradnjo v nekaterih primerih izvesti med vikendom. Odločitev o razporejanju bi morala temeljiti na rezultatih preskušanja v nižjih okoljih.

3. Po potrebi nadgradite rešitve po meri. Na tej točki uvedite vse spremembe, ki ste jih naredili v svojih prilagoditvah v razdelku [Preskušanje in preoblikovanje prilagoditev](#testing-and-refactoring-customizations) tega članka.
4. Obiščite spletno mesto **make.powerapps.com**, na spustnem seznamu v zgornjem desnem kotu portala izberite svoje okolje, v levem meniju izberite možnost **Rešitve**, izberite rešitev **Opuščene komponente Project Operations** in možnost **Odstrani**.

    Ta rešitev je začasna rešitev, ki vsebuje obstoječi podatkovni model in komponente, ki so prisotne med nadgradnjo. Če odstranite to rešitev, boste odstranili tudi vsa polja in komponente, ki se ne uporabljajo več. Na ta način pomagate poenostaviti vmesnik ter olajšati integracijo in razširitev.
    
### <a name="upgrade-to-project-operations-lite"></a>Nadgradnja na poenostavljeno različico aplikacije Project Operations

Naslednji koraki opisujejo postopek nadgradnje in povezano zapisovanje dnevnikov napak:

1. **Preverjanje različice PSA:** če želite namestiti aplikacijo Project Operations, morate imeti različico V3.10.58.120 ali novejšo.
1. **Vnaprejšnje preverjanje veljavnosti:** ko skrbnik sproži nadgradnjo, sistem izvede postopek vnaprejšnjega preverjanja veljavnosti za vsako entiteto, ki je jedro rešitve Project Operations. Ta korak preveri, ali so vsi sklici entitet veljavni, in zagotovi, da so podatki, povezani z vmesnikom SČD, znotraj objavljenih omejitev za Project for the Web.
1. **Nadgradnja metapodatkov:** po uspešnem vnaprejšnjem preverjanju veljavnosti sistem sproži spremembe v shemi in ustvari rešitev za opuščene komponente. To opuščeno rešitev lahko odstranite, ko dokončate vse zahtevano preoblikovanje prilagoditev. Ta korak je najdaljši del postopka nadgradnje in lahko traja do štiri ure.
1. **Nadgradnja podatkov:** ko so v koraku nadgradnje metapodatkov opravljene vse zahtevane spremembe sheme, se vaši podatki preselijo v novo shemo, pridobijo se morebitne zahtevane privzete vrednosti in izvedejo ponovni izračuni.
1. **Posodobitev mehanizma razporejanja projekta:** po uspešni nadgradnji podatkov se zavihek **Urnik** na glavni strani preimenuje v **Opravila**. Ko uporabnik po nadgradnji izbere ta zavihek, je usmerjen do mreže za sledenje in si ogleda različico SČD samo za branje. Za urejanje SČD mora sprožiti načrtovanje [procesa pretvorbe](/PSA-Upgrade-Project-Conversion.md). Vsi projekti brez že obstoječega vmesnika SČD lahko novo izkušnjo načrtovanja uporabljajo neposredno in brez pretvorbe.
 
### <a name="validate-common-scenarios"></a>Preverjanje veljavnosti pogostih scenarijev

Ko preverite veljavnost posebnih prilagoditev, priporočamo, da pregledate tudi poslovne procese, ki so podprti v aplikacijah. Ti poslovni procesi vključujejo, vendar niso omejeni na, ustvarjanje prodajnih entitet, kot so ponudbe in pogodbe, ter ustvarjanje projektov, ki vključujejo SČD in odobritev dejanskih vrednosti.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Večje spremembe med aplikacijama Project Service Automation in Project Operations

V tem razdelku je povzetek večjih sprememb, ki jih lahko pričakujete med aplikacijama Project Service Automation in Project Operations.

### <a name="project-planning"></a>Načrtovanje projekta

Zmogljivosti načrtovanja projekta v aplikaciji Project Operations se ne zanašajo več na kombinacijo logike na strani odjemalca in logike na strani strežnika. Namesto tega Project Operations kot mehanizem za razporejanje uporablja Project for the Web. Ta sprememba v zmogljivostih razporejanja omogoča številne nove funkcije, kot so pogledi plošče in Ganttovega grafikona, načrtovanje na podlagi virov, [elementi kontrolnega seznama opravil](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) in načini razporejanja projektov. Nove zmogljivosti razporejanja so podprte tudi z bogatim naborom novih [vmesnikov za programiranje aplikacij (API)](../project-management/schedule-api-preview.md). Ti API-ji zagotavljajo, da noben programski postopek za ustvarjanje, posodabljanje ali brisanje entitete v vmesniku SČD ne pokvari polj z izračunom v urniku.

### <a name="billing-and-pricing"></a>Zaračunavanje in cene

Kot del nenehnih naložb v aplikacijo Project Operations je na voljo več novih zmogljivosti pri zaračunavanju in oblikovanju cen. Tukaj je nekaj primerov:

- [Beleženje uporabe materiala v projektih in projektnih opravilih](../material/material-usage-log.md)
- [Upravljanje podizvajalskih pogodb](../pro/subcontracting/managing-subcontracts-overview.md)
- [Pogodbe za predplačila in honorarje](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Stanje in veljavnosti pogodbe »Ni dovoljeno preseči«](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Obračunavanje na podlagi opravil

### <a name="resource-management"></a>Upravljanje virov

Project Operations ponuja izbirno podporo za ploščo Universal Resource Scheduling (URS) in pomočnika za razporejanje. Ta nova izkušnja bo postala obvezna v fazi aprila 2023.

## <a name="frequently-asked-questions"></a>Pogosto zastavljena vprašanja

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Katere vrste uvajanja so trenutno podprte za nadgradnjo?

| Vir                                                 | Cilj                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Uvedba poenostavljene različice aplikacije Project Operations                        | Podprto               |
| Upravljanje projektov in računovodstvo v aplikacijah Dynamics 365 Finance | Uvedba poenostavljene različice aplikacije Project Operations                        | Trenutno ni podprto |
| Upravljanje finančnih projektov in računovodstvo              | Project Operations za primere uporabe z viri/brez zalog     | Trenutno ni podprto |
| Project Service Automation 3.x                         | Project Operations za primere uporabe z viri/brez zalog     | Trenutno ni podprto |
| Project for the Web (namensko okolje)            | Uvedba poenostavljene različice aplikacije Project Operations                        | Trenutno ni podprto |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kako lahko namestim aplikacijo Project Operations, preden je na voljo orodje za nadgradnjo?

Obstajata dva načina za namestitev aplikacije Project Operations, preden je na voljo orodje za nadgradnjo:

- Omogočite novo okolje.
- Ločeno uvedite Project Operations v kateri koli prodajni organizaciji, kjer aplikacija Project Service Automation ni prisotna.

Če je aplikacija Project Service Automation nameščena v organizaciji, vendar ni bila uporabljen, jo lahko odstranite. Ko popolnoma odstranite aplikacijo Project Service Automation, lahko Project Operations namestite v isto organizacijo.
