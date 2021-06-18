---
title: Pregled prodajnega procesa
description: V tej temi so na voljo informacije o osnovnih prodajnih postopkih.
author: rumant
ms.date: 10/29/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a03cb4949cafdf0754a89435542f616c41d65a5f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996047"
---
# <a name="sales-process-overview"></a>Pregled prodajnega procesa

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Prodajni postopki, ki se uporabljajo v organizaciji, v kateri poslovanje poteka na podlagi projektov, se razlikujejo od prodajnih postopkov, ki se uporabljajo v organizaciji, v kateri poslovanje poteka na podlagi izdelkov. To pa zato, ker so prodajni cikli za organizacije, v katerih poslovanje poteka na podlagi projektov, daljši in zahtevajo prilagojene tehnike ocenjevanja za analiziranje in ustvarjanje ponudb za vsak posel. Aplikacija Dynamics 365 Project Operations uporablja nekaj naslednjih funkcij, ki se uporabljajo v prodajnem postopku:

- Zapis možne stranke se uporablja za spremljanje prodajnega postopka.
- Potrjevanje možnih strank se beleži kot priložnosti.
- Mogoče je dostopati do vseh povezanih artefaktov za priložnost. Ti artefakti vključujejo ekipo za prodajo, zainteresirane skupine, verjetnost, oceno, faze prodaje in poslovne postopke.
- Za priložnost je ustvarjenih več ponudb.
- Za ustvarjanje prodajnega naloga je ponudba označena s stanjem **Zaključena kot pridobljena**. V storitvi Project Operations je prodajni nalog prilagojen in se imenuje projektna pogodba.

## <a name="estimate-a-sale"></a>Ocenjevanje prodaje
Vrednost prodaje se lahko oceni na podlagi projektov, ki so bili predhodno izvedeni, in njihovi zahtevnosti. Za projekte, ki vključujejo razširitve predhodnih projektov ali projekte, pri katerih je strokovno znanje dobavitelja visoko in so uporabljene dobro znane predloge za delo, lahko uporabite preprostejši postopek ocenjevanja. Običajno imajo bolj zapleteni projekti daljši postopek nakupa. Zato je v postopku ocenjevanja prodaje več faz. V začetnih fazah postopka ekipa za prodajo uporabi vnos upraviteljev kupcev in strokovnjakov z ustreznih področij, da ustvari splošnejšo oceno za vsako različno komponento dela, ki je zajeto v ponudbi. Te komponente dela predstavljajo vrstice ponudbe. 

Lahko ustvarite splošnejšo oceno ponudbe. Sčasoma bo ta splošnejša ocena zamenjana s podrobnejšo oceno, ki temelji na načrtu projekta, ustvarjenem s standardiziranimi predlogami za projekt. S temi predlogami je mogoče ustvariti razpored in določiti denarne vrednosti ponudbe in njenih komponent (vrstice ponudbe). 

Za projekt lahko ustvarite več ponudb in jih združite v en zapis priložnosti. Sčasoma bo ena od ponudb označena kot **Zaključena kot pridobljena** in ustvarjena bo projektna ponudba ali izjava o delu (SOW). Projektna pogodba vsebuje pogodbeno vrednost za vsako komponento (podrobnosti pogodbe), ki jo stranka sprejme za dostavo. Izjava SOW je običajno ustvarjena kot dokument Microsoft Word. Vsi računi, ki so stranki poslani v okviru dostave projekta, se sklicujejo na projektno pogodbo ali SOW.

Lahko ustvarite tudi nadomestne ponudbe v en zapis priložnosti ali nastavite sistem tako, da se projektna pogodba ustvari, ko je ponudba pridobljena. V tem primeru lahko priložite Wordov dokument, ki predstavlja izjavo SOW v zapisu projektne pogodbe.

## <a name="configure-the-sales-process"></a>Konfiguriranje prodajnega postopka
Za konfiguriranje prodajnega postopka lahko uporabite poteke poslovnega procesa. Ti poteki zagotavljajo vodeni vizualni vmesnik za premikanje poslov naprej skozi stopnje prodajnega procesa.

V prodajnem postopku lahko vaše podjetje ima šest naslednjih faz:

1. Kvalificiraj
2. Oceni
3. Notranji pregled
4. Pogodba
5. Dostavi
6. Zaprto
 
Vaša organizacija lahko uporabi različne entitete, da tekom svojega razvoja predstavi isti posel. V začetnih fazah prodajnega postopka je posel predstavljen kot entiteta priložnosti. Ko pa mine nekaj časa in imate na voljo več podrobnosti, lahko uporabite splošnejše ocene, da ustvarite eno ali več ponudb. Če eno od teh ponudb pregledajo notranje zainteresirane skupine in zainteresirane skupine strank, posel predstavlja entiteta ponudbe. Ko stranka sprejme ponudbo, posel predstavlja projektna pogodba ali izjava SOW. Za podporo tega delovanja so poteki poslovnega procesa strukturirani tako, da je vsaka faza v procesu povezana z drugo tabelo zbirke podatkov.

Fazo prodajnega postopka **Potrjevanje** je mogoče shraniti v entiteto priložnosti. Fazi **Ocena** in **Notranji pregled** je mogoče shraniti v entiteto ponudbe. Faze **Pogodba**, **Dostava** in **Zapiranje** je mogoče shraniti v entiteto projektne pogodbe.

Ko boste posle premikali skozi faze, boste pozvani, da ustvarite ustrezen zapis entitete za pomoč in vodenje pri procesu. Faze so lahko pogojne. Če na primer potrebujete notranji pregled ponudbe samo, če ponudba uporablja seznam po meri, lahko ta pogoj konfigurirate v ustrezni fazi poslovnega procesa. Faza **Notranji pregled** je nato prikazana samo za ponudbe, ki uporabljajo cenik po meri. Fazi **Ocena** sledi faza **Pogodba** pri vseh drugih poslih in ponudbah.

> [!NOTE]
> Project Operations ima posebne strani za zapise entitet priložnosti, ponudbe, naročila in računa. Morate ustvariti te zapise na straneh s podatki o projektu za te entitete. Sicer ne boste mogli odpreti zapisov s strani **Podatki o projektu**. Če želite odpreti zapis s strani **Podatki o projektu**, morate izbrisati zapis in ga poustvariti z uporabo strani **Podatki o projektu**, kjer poslovna logika za vsako od teh vrst entitet zagotavlja, da je polje **Vrsta** zapisa pravilno nastavljeno in vsi obvezni koncepti pravilno začeti.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Sledenje popravkom ponudb in projektnih načrtov v prodajnem ciklu
V storitvi Project Operations ni mogoče slediti popravkom, ki so izvedeni v ponudbi. Namesto tega morate obstoječo ponudbo **Zaprta kot izgubljena** označiti in nato ustvariti novo ponudbo. Pogodbo lahko kopirate ali pa klonirate ponudbo, ki temelji na projektu.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Sledenje komentarjem in odobritvam ponudb in projektnih pogodb
Pregled in odobritev ponudb in projektnih pogodb lahko upravljate z zidom z zapisi in objavami. Vaša organizacija lahko ustvari poteke dela in vtičnike po meri za dodeljevanje, preusmerjanje, stopnjevanje in upravljanje obvestil o pregledu in odobritvi delovnih nalogov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]