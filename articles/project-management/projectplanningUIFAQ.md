---
title: Odpravljanje težav dela v mreži opravil
description: Ta tema zagotavlja informacije o odpravljanju težav, potrebne pri delu v mreži opravil.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031557"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Odpravljanje težav dela v mreži opravil 

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Ta tema opisuje, kako odpraviti težave, s katerimi se lahko srečate pri delu z upravljanjem stroškov.

## <a name="enable-cookies"></a>Omogočanje piškotkov

Project Operations zahteva, da so omogočeni piškotki tretjih oseb, da se lahko upodobi strukturirana členitev dela. Če piškotki tretjih oseb niso omogočeni, boste namesto, da bi videli opravila, videli prazno stran, ko izberete zavihek **Opravila** na strani **Projekti**.

![Prazen zavihek, ko piškotki tretjih oseb niso omogočeni](media/blankschedule.png)


### <a name="workaround"></a>Nadomestna rešitev
Za brskalnike Microsoft Edge ali Google Chrome naslednji postopki orisujejo, kako posodobiti nastavitve brskalnika, da se omogočijo piškotki tretjih oseb.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Odprite brskalnik Edge.
2. V desnem zgornjem kotu izberite **tri pike** (...) in nato izberite **Nastavitve**.
3. Pod možnostjo **Piškotki in dovoljenja za mesta** izberite **Piškotki in podatki o mestih**.
4. Izklopite **Blokiraj piškotke tretjih oseb**.

#### <a name="google-chrome"></a>Google Chrome

1. Odprite brskalnik Chrome.
2. V desnem zgornjem kotu izberite tri navpične pike in nato izberite **Nastavitve**.
3. Pod možnostjo **Zasebnost in varnost** izberite **Piškotki in drugi podatki mesta**.
4. Izberite možnost **Dovoli vse piškotke**.

> [!IMPORTANT]
> Če blokirate piškotke tretjih oseb, bodo vsi piškotki in podatki mesta iz drugih mest blokirani, tudi če je mesto dovoljeno na seznamu izjem.

## <a name="pex-endpoint"></a>Končna točka PEX

Project Operations zahteva, da se parametri projekta sklicujejo na končno točko PEX. Ta končna točka je potrebna za komunikacijo s storitvijo, uporabljeno za upodobitev strukturirane členitve dela. Če parameter ni omogočen, se prikaže napaka »Parameter projekta ni veljaven«. 

### <a name="workaround"></a>Nadomestna rešitev
 ![Polje končne točke PEX na parametru projekta](media/projectparameter.png)

1. Dodaj polje **Končna točka PEX** na stran **Projektni parametri**.
2. Posodobi polje z naslednjo vrednostjo: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Odstranite polje s strani **Projektni parametri**.

## <a name="privileges-for-project-for-the-web"></a>Pravice za projekt za splet

Project Operations se zanaša na zunanjo storitev razporejanja. Storitev zahteva, da ima uporabnik več vlog za branje in pisanje dodeljenih entitetam, povezanih s strukturirano členitvijo dela. Te entitete vključujejo projektna opravila, dodelitve virov in odvisnosti opravil. Če uporabnik ne more upodobiti strukturirane členitve dela, ko odpre zavihek **Opravila**, verjetno projekt za Project Operations ni bil omogočen. Uporabnik lahko prejme bodisi napako varnostne vloge ali napako, povezano z zavrnitvijo dostopa.


## <a name="workaround"></a>Nadomestna rešitev

1. Pojdite na **Nastavitev > Varnost > Uporabniki > Uporabniki aplikacije**.  

   ![Bralnik aplikacije](media/applicationuser.jpg)
   
2. Dvokliknite zapis uporabnika aplikacije, da preverite naslednje:

 - Uporabnik ima dostop do projekta. To preverjanje se običajno opravi tako, da se zagotovi, da ima uporabnik varnostno vlogo **Vodja projektov**.
 - Uporabnik aplikacije Microsoft Project obstaja in je pravilno konfiguriran.
 
3. Če ta uporabnik ne obstaja, lahko ustvarite zapis novega uporabnika. Izberite **Novi uporabniki**. Spremenite obrazec za vnos na **Uporabnik aplikacije**, nato pa dodajte **ID aplikacije**.

   ![Podrobnosti uporabnika aplikacije](media/applicationuserdetails.jpg)

4. Prepričajte se, da je bila uporabniku dodeljena pravilna licenca in da je storitev omogočena v podrobnostih naročniških paketov licence.
5. Prepričajte se, da uporabnik lahko odpre project.microsoft.com.
6. Prepričajte se, prek projektnih parametrov, da sistem kaže na pravilno projektno končno točko.
7. Prepričajte se, je ustvarjen uporabnik projektne aplikacije.
8. Uveljavite naslednje varnostne vloge za uporabnika:

  - Uporabnik storitve Dataverse
  - Sistem Project Operations
  - Sistem projekta

## <a name="error-when-updating-the-work-breakdown-structure"></a>Napaka pri posodabljanju strukturirane členitve dela

Ko se izvede ena ali več posodobitev strukturirane členitve dela, spremembe nazadnje niso uspešne in se ne shranijo. Pride do napake v mreži razporeda s sporočilom »Nedavnih sprememb, ki ste jih izvedli, ni bilo mogoče shraniti«.

### <a name="workaround"></a>Nadomestna rešitev

1. Prepričajte se, da je bila uporabniku dodeljena pravilna licenca in da je storitev omogočena v podrobnostih naročniških paketov licence.
2. Prepričajte se, da uporabnik lahko odpre project.microsoft.com.
3. Prepričajte se, da sistem kaže na pravilno projektno končno točko.
4. Prepričajte se, je bil ustvarjen uporabnik projektne aplikacije.
5. Uveljavite naslednje varnostne vloge za uporabnika:
  
  - Uporabnik storitve Dataverse ali osnovni uporabnik
  - Sistem Project Operations
  - Sistem projekta
  - Sistem dvojnega zapisovanja Project Operations (ta vloga je obvezna, če uvajate scenarije, ki temeljijo na virih/nezalogi v storitvi Project Operations.)
