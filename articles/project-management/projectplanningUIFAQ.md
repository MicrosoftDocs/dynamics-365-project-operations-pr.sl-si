---
title: Odpravljanje težav dela v mreži opravil
description: Ta tema zagotavlja informacije o odpravljanju težav, potrebne pri delu v mreži opravil.
author: ruhercul
ms.date: 09/22/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 67136229d84a09886fffe9677b10f671aea3c393
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547219"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Odpravljanje težav dela v mreži opravil 


_**Velja za:** aplikacija Project Operations za okoliščine, ki temeljijo na virih/nezalogi, poenostavljeno uvajanje – posel do izstavitve predračuna, storitev Project for the web_

Mreža opravil, ki jo je uporabila aplikacija Dynamics 365 Project Operations, je gostujoči element iframe znotraj storitve Microsoft Dataverse. Zaradi te uporabe morajo biti izpolnjene posebne zahteve za zagotovitev pravilnega delovanja preverjanja pristnosti in avtorizacije. Ta tema opisuje pogoste težave, ki lahko vplivajo na možnost upodabljanja mreže ali upravljanja opravil v strukturirani členitvi dela (SČD).

Pogoste težave vključujejo:

- Zavihek **Opravilo** v mreži opravil je prazen.
- Ko se projekt odpre, se projekt ne naloži, uporabniški vmesnik pa je obtičal na vrtavki za nalaganje.
- Skrbništvo pravic za storitev **Project for the Web**.
- Ko ustvarite, posodobite ali izbrišete opravilo, se spremembe ne shranijo.

## <a name="issue-the-task-tab-is-empty"></a>Težava: Zavihek Opravilo je prazen

### <a name="mitigation-1-enable-cookies"></a>Rešitev št. 1: Omogočite piškotke

Aplikacija Project Operations zahteva, da so piškotki tretjih oseb omogočeni za upodabljanje strukturirane členitve dela. Če piškotki tretjih oseb niso omogočeni, boste namesto, da bi videli opravila, videli prazno stran, ko izberete zavihek **Opravila** na strani **Projekti**.

Za brskalnike Microsoft Edge ali Google Chrome naslednji postopki orisujejo, kako posodobiti nastavitve brskalnika, da se omogočijo piškotki tretjih oseb.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Odprite brskalnik Edge.
2. V desnem zgornjem kotu izberite **tri pike** (...) in nato izberite **Nastavitve**.
3. Pod možnostjo **Piškotki in dovoljenja za mesta** izberite **Piškotki in podatki o mestih**.
4. Izklopite **Blokiraj piškotke tretjih oseb**.
5. Osvežite brskalnik. 

#### <a name="google-chrome"></a>Google Chrome

1. Odprite brskalnik Chrome.
2. V desnem zgornjem kotu izberite tri navpične pike in nato izberite **Nastavitve**.
3. Pod možnostjo **Zasebnost in varnost** izberite **Piškotki in drugi podatki mesta**.
4. Izberite možnost **Dovoli vse piškotke**.
5. Osvežite brskalnik. 

> [!NOTE]
> Če blokirate piškotke tretjih oseb, bodo vsi piškotki in podatki mesta iz drugih mest blokirani, tudi če je mesto dovoljeno na seznamu izjem.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Rešitev št. 2: Preverite, da je bila končna točka PEX pravilno konfigurirana

Project Operations zahteva, da se parametri projekta sklicujejo na končno točko PEX. Ta končna točka je potrebna za komunikacijo s storitvijo, ki se uporablja za upodabljanje strukturirane členitve dela. Če parameter ni omogočen, se prikaže napaka »Parameter projekta ni veljaven«. Če želite končno točko PEX posodobiti, upoštevajte naslednje korake.

1. Dodaj polje **Končna točka PEX** na stran **Projektni parametri**.
2. Določite vrsto izdelka, ki ga uporabljate. Ta vrednost se uporablja, ko je nastavljena končna točka PEX. Pri pridobivanju končne točke PEX je vrsta izdelka že določena. Ohranite to vrednost.
3. Posodobite polje z naslednjo vrednostjo: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Spodnja tabela prikazuje parametre vrste, ki jih je treba uporabiti glede na vrsto izdelka.

      | **Vrsta izdelka**                     | **Vrsta parametra** |
      |--------------------------------------|--------------------|
      | Storitev Project for the Web v privzeti organizaciji   | tipa=0             |
      | Storitev Project for the Web v organizaciji CDS | tipa=1             |
      | Project Operations                   | tipa=2             |

4. Odstranite polje s strani **Projektni parametri**.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Težava: Projekt se ne naloži in uporabniški vmesnik je obtičal na vrtavki

Za namene preverjanja pristnosti morajo biti omogočena pojavna okna, da se mreža opravil lahko naloži. Če pojavna okna niso omogočena, bo zaslon obtičal na vrtavki za nalaganje. Naslednji grafični prikaz prikazuje spletni naslov z blokirano pojavno oznako v naslovni vrstici, zaradi česar vrtavka obtiči, ko poskuša naložiti stran. 

   ![Nedokončana vrtavka in blokirana pojavna okna.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Rešitev št. 1: Omogočite pojavna okna

Če je vaš projekt obtičal na vrtavki, je mogoče, da pojavna okna niso omogočena.

#### <a name="microsoft-edge"></a>Microsoft Edge

Pojavna okna v brskalniku Edge lahko omogočite na dva načina.

1. V brskalniku Edge izberite obvestilo v zgornjem desnem kotu brskalnika.
2. Izberite **Vedno dovoli pojavna okna in preusmeritve iz** določenega okolja storitve Dataverse.
 
     ![Pojavna okna blokirajo okno.](media/enablepopups.png)

Druga možnost je, da upoštevate naslednje korake:

1. Odprite brskalnik Edge.
2. V zgornjem desnem kotu izberite **tri pike** (...) in nato izberite **Nastavitve** > **Dovoljenja za spletno mesto** > **Pojavna okna in preusmeritve**.
3. Gumb **Pojavna okna in preusmeritve** izklopite, če želite blokirati pojavna okna, ali ga pa vklopite, da v napravi omogočite pojavna okna.
4. Ko omogočite pojavna okna, osvežite brskalnik. 

#### <a name="google-chrome"></a>Google Chrome
1. Odprite brskalnik Chrome.
2. Odprite stran, kjer so pojavna okna blokirana.
3. V naslovni vrstici izberite možnost **Pojavno okno je blokirano**.
4. Izberite povezavo za pojavno okno, ki ga želite videti.
5. Ko omogočite pojavna okna, osvežite brskalnik. 

> [!NOTE]
> Če želite vedno videti pojavna okna za spletno mesto, izberite možnost **Vedno dovoli pojavna okna in preusmeritve iz [spletno mesto]** in nato izberite možnost **Končano**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Težava št. 3: Skrbništvo pravic za storitev Project for the Web

Project Operations se zanaša na zunanjo storitev razporejanja. Storitev zahteva, da ima uporabnik dodeljenih več vlog, ki mu omogočajo branje in pisanje entitetam, povezanim s SČD. Te entitete vključujejo projektna opravila, dodelitve virov in odvisnosti opravil. Če uporabnik ne more upodobiti SČD, ko se pomakne do zavihka **Opravila**, je razlog verjeto to, da **Projekt** za **Aplikacijo Project Operations** ni bil omogočen. Uporabnik lahko prejme bodisi napako varnostne vloge ali napako, povezano z zavrnitvijo dostopa.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Rešitev št. 1: Preverite varnostne vloge uporabnika aplikacije in končnega uporabnika

1. Odprite možnost **Nastavitev** > **Varnost** > **Uporabniki** > **Uporabniki aplikacije**.  

   ![Bralnik aplikacije.](media/applicationuser.jpg)
   
2. Za preverjanje dvokliknite zapis uporabnika aplikacije:

     - Uporabnik ima dostop do projekta. To lahko storite tako, da preverite, ali ima uporabnik varnostno vlogo **Vodje projekta**.
     - Uporabnik aplikacije Microsoft Project obstaja in je pravilno konfiguriran.
 
3. Če ta uporabnik ne obstaja, ustvarite nov zapis uporabnika. 
4. Izberite **Novi uporabniki**, obrazec za vnos spremenite v **Uporabnik aplikacije** in nato dodajte **ID aplikacije**.

   ![Podrobnosti uporabnika aplikacije.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Težava št. 4: Ko ustvarite, posodobite ali izbrišete opravilo, se spremembe ne shranijo

Ko izvedete eno ali več posodobitev SČD, spremembe niso uspešne in se ne shranijo. V mreži razporeda se pojavi napaka s sporočilom: »Nedavne spremembe ni mogoče shraniti«.

### <a name="mitigation-1-validate-the-license-assignment"></a>Rešitev št. 1: Preverite dodeljevanje licenc

1. Prepričajte se, da je bila uporabniku dodeljena pravilna licenca in da je storitev omogočena v podrobnostih naročniških paketov licence.  
2. Prepričajte se, da uporabnik lahko odpre spletno stran **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Rešitev št. 2: Potrditvena konfiguracija uporabnika aplikacije Project
1. Prepričajte se, da je bil uporabnik aplikacije Project ustvarjen.
2. Uveljavite naslednje varnostne vloge za uporabnika:
  
  - Uporabnik storitve Dataverse ali osnovni uporabnik
  - Sistem Project Operations
  - Sistem projekta
  - Sistem dvojnega zapisovanja v aplikaciji Project Operations. Ta vloga je obvezna za okoliščino uvajanja aplikacije Project Operations, ki temelji na virih/nezalogi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
