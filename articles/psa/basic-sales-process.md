---
title: Prodajni postopki
description: V tej temi so na voljo informacije o osnovnih prodajnih postopkih.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 2561a54af6bdb9764a318f012fdc53f7b3298893
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145198"
---
# <a name="sales-processes"></a>Prodajni postopki

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Prodajni postopki, ki se uporabljajo v organizaciji, v kateri poslovanje poteka na podlagi projektov, se razlikujejo od prodajnih postopkov, ki se uporabljajo v organizaciji, v kateri poslovanje poteka na podlagi izdelkov. Ta razlika se pojavi, ker so prodajni cikli za organizacije, v katerih poslovanje poteka na podlagi projektov, daljši in zahtevajo prilagojene tehnike ocenjevanja za analiziranje in ustvarjanje ponudb za vsak posel. Dynamics 365 Project Service Automation uporablja nekatere iste funkcije, ki so uporabljene v prodajnem postopku za Dynamics 365 Sales. Tukaj je nekaj primerov:

- Entiteta možne stranke se uporablja za spremljanje prodajnega postopka.
- Potrjevanje možnih strank se beleži kot priložnosti. Prodajni postopek se lahko začne tudi s priložnostjo.
- Mogoče je dostopati do vseh povezanih artefaktov za priložnost. Ti artefakti vključujejo ekipo za prodajo, zainteresirane skupine, verjetnost, oceno, faze prodaje in poslovne postopke.
- Za priložnost je ustvarjenih več ponudb.
- Za ustvarjanje prodajnega naloga je ponudba označena kot **Zaključena kot pridobljena**. V aplikaciji PSA je prodajni nalog prilagojen in se imenuje projektna pogodba.

Na spodnji sliki je prikazan običajen prodajni postopek v organizaciji, v kateri poslovanje temelji na projektih.

> ![Prodajni postopek v organizaciji, v kateri poslovanje temelji na projektih](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Ocenjevanje prodaje
Vrednost prodaje se lahko oceni na podlagi projektov, ki so bili predhodno izvedeni, in njihovi zahtevnosti. Za projekte, ki vključujejo razširitve predhodnih projektov ali projekte, pri katerih je strokovno znanje dobavitelja visoko in so uporabljene dobro znane predloge za delo, lahko uporabite preprostejši postopek ocenjevanja. Običajno imajo bolj zapleteni projekti daljši postopek nakupa. Zato je v postopku ocenjevanja prodaje več faz. V začetnih fazah postopka ekipa za prodajo uporabi vnos upraviteljev kupcev in strokovnjakov z ustreznih področij, da začne ustvarjati splošnejšo oceno za vsako različno komponento dela, ki je zajeto v ponudbi. Te komponente dela predstavljajo vrstice ponudbe. 

Lahko ustvarite splošnejšo oceno ponudbe. Sčasoma bo ta splošnejša ocena zamenjana s podrobnejšo oceno, ki temelji na načrtu projekta, ustvarjenem s standardiziranimi predlogami za projekt. S temi predlogami je mogoče ustvariti razpored in določiti denarne vrednosti ponudbe in njenih komponent (vrstice ponudbe). 

Za projekt lahko ustvarite več ponudb in jih združite v eno vrsto entitete priložnosti. Sčasoma bo ena od teh ponudb označena kot **Zaključena kot pridobljena** in ustvarjena bo projektna ponudba ali izjava o delu (SOW). Projektna pogodba vsebuje pogodbeno vrednost za vsako komponento (podrobnosti pogodbe), ki jo stranka sprejme za dostavo. Izjava SOW je običajno ustvarjena kot dokument Microsoft Word. Vsi računi, ki so stranki poslani v okviru dostave projekta, se sklicujejo na projektno pogodbo ali SOW.

Lahko ustvarite tudi nadomestne ponudbe v eni vrsti entitete priložnosti ali nastavite sistem tako, da se projektna pogodba ustvari, ko je ponudba pridobljena. V tem primeru lahko priložite Wordov dokument, ki predstavlja izjavo SOW v zapisu projektne pogodbe.

![Zapiranje ponudbe za ustvarjanje projektne pogodbe](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Konfiguriranje prodajnega postopka
Za konfiguriranje prodajnega postopka lahko uporabite poteke poslovnega procesa iz aplikacije Microsoft Dynamics 365. Poteki poslovnega procesa vašemu prodajnemu osebju zagotavljajo vodeni vizualni vmesnik, ki ga lahko uporabljajo za premikanje ponudb skozi faze, značilne za vaše podjetje.

V prodajnem postopku lahko vaše podjetje ima šest naslednjih faz:

1. Potrdi
2. Ocena
3. Notranji pregled
4. Pogodba
5. Dostavi
6. Zapri

Teh šest faz predstavljajo škarnice (\>), ki jih izberete za razširitev v vsaki vrsti entitete za priložnost, ki jo ustvarite.

![Konfiguriranje poslovnega procesa v aplikaciji Dynamics 365](media/basic-guide-3.png)
 
Vaša organizacija lahko uporabi različne entitete, da tekom svojega razvoja predstavi isti posel. V začetnih fazah prodajnega postopka je posel predstavljen kot entiteta priložnosti. Ko pa mine nekaj časa in imate na voljo več podrobnosti, lahko uporabite splošnejše ocene, da ustvarite eno ali več ponudb. Če eno od teh ponudb pregledajo notranje zainteresirane skupine in zainteresirane skupine strank, posel predstavlja entiteta ponudbe. Ko stranka sprejme ponudbo, posel predstavlja projektna pogodba ali izjava SOW. Za podporo tega delovanja so poteki poslovnega procesa strukturirani tako, da je vsaka faza v procesu povezana z drugo tabelo zbirke podatkov.

Fazo prodajnega postopka **Potrjevanje** je mogoče shraniti v entiteto priložnosti. Fazi **Ocena** in **Notranji pregled** je mogoče shraniti v entiteto ponudbe. Faze **Pogodba**, **Dostava** in **Zapiranje** je mogoče shraniti v entiteto projektne pogodbe.

Ko boste posle premikali skozi faze, boste pozvani, da ustvarite ustrezen zapis entitete za pomoč in vodenje pri procesu. Faze so lahko pogojne. Če na primer potrebujete notranji pregled ponudbe samo, če ponudba uporablja seznam po meri, lahko ta pogoj konfigurirate v ustrezni fazi poslovnega procesa. Faza **Notranji pregled** je nato prikazana samo za ponudbe, ki uporabljajo cenik po meri. Fazi **Ocena** sledi faza **Pogodba** pri vseh drugih poslih in ponudbah.

> [!NOTE]
> Aplikacija PSA ima določene strani za entitete priložnosti, ponudb, naročil in računov. Morate ustvariti priložnosti, ponudbe, naročila in račune v aplikaciji Project Service s stranmi podatkov o projektu za te entitete. Če za ustvarjanje zapisa uporabite drugo stran, ne boste mogli odpreti zapisa s strani **Podatki o projektu**. Če želite odpreti zapis s strani **Podatki o projektu**, morate zapis izbrisati in ga znova ustvariti s stranjo **Podatki o projektu**. Na strani **Podatki o projektu** zagotavlja poslovna logika za vsako od teh vrst entitet, da je polje zapisa **Vrsta** pravilno nastavljeno ter da so vsi obvezni koncepti ustrezno inicializirani.

> ![Podatki o projektu za novo naročilo](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Razlike med aplikacijama Project Service Automation in Sales
Čeprav prodajni postopek v aplikaciji PSA uporablja osnovne zmožnosti prodajnega postopka iz aplikacije Sales, je bistveno drugačen zaradi sprememb poslovnih praks organizacij, v katerih poslovanje poteka na podlagi projektov. Tukaj je nekaj primerov:

- **Projektne ponudbe** – v aplikaciji Project Service Automation je ponudba zaprta, ko iz nje ustvarite projektno pogodbo. V aplikaciji Sales pa je lahko ponudba odprta tudi po tem, ko jo pridobite. Razlog za to je, da je ujemanje med ponudbo in projektno pogodbo boljše za organizacije, v katerih poslovanje poteka na podlagi projektov. 
- **Aktivacija in popravki** – aktivacija in popravki v aplikaciji PSA niso podprti za projektne ponudbe. V aplikaciji Sales je ponudbo mogoče zakleniti, da preprečite dodatne spremembe.
- **Zapiranje ponudbe kot izgubljene ali pridobljene** – ko je projektna ponudba v aplikaciji PSA zaprta kot izgubljena ali pridobljena, priložnost ostane odprta. Vse druge ponudbe v priložnosti so zaprte kot izgubljene. Ko je ponudba zaprta kot pridobljena ali izgubljena v aplikaciji Sales, je uporabnik pozvan, da izvede dejanje v priložnosti. Odvisno od vnosa uporabnika je temeljno možnost mogoče zapreti ali pustiti odprto.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Sledenje popravkom ponudb in projektnih načrtov v prodajnem ciklu
V aplikaciji PSA ni mogoče slediti popravkom, ki so izvedeni v ponudbi. Namesto tega morate obstoječo ponudbo **Zaprta kot izgubljena** označiti in nato ustvariti novo ponudbo. Z aplikacijo PSA lahko pogodbo kopirate ali pa klonirate ponudbo, ki temelji na projektu.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Sledenje komentarjem in odobritvam ponudb in projektnih pogodb
Pregled in odobritev ponudb in projektnih pogodb lahko upravljate z zidom z zapisi in objavami. Vaša organizacija lahko ustvari poteke dela in vtičnike po meri za dodeljevanje, preusmerjanje, stopnjevanje in upravljanje obvestil o pregledu in odobritvi delovnih nalogov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]