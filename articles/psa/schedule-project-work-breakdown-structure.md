---
title: Načrtovanje projekta s strukturirano členitvijo dela
description: Kako načrtovati projekt s strukturirano členitvijo dela v rešitvi Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: cf12cc3bcf061e1daffafb248cfd76809c6444ec
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149833"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Načrtovanje projekta s strukturirano členitvijo dela (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Načrtovanje projekta vključuje postopke, ki jih je treba opraviti, kateri viri jih bodo izvajali ter časovni okvir, v katerem jih je treba opraviti. Načrt projekta vključuje vse postopke, ki so povezani s pravočasno oddajo projekta. Eden od prvih korakov v začetek fazi projekta je določitev načrta projekta. Za določanje načrta projekta morate ustvariti strukturirano členitev dela.  
  
 Strukturo projekta ustvarite s strukturirano členitvijo dela, ki vam bo pomagala v teh točkah:  
  
- Razčlenitev dela v obvladljiva opravila  
  
- Ocenjevanje časa, potrebnega za dokončanje opravila  
  
- Nastavitev odvisnosti opravil in trajanje opravila  
  
- Določanje vlog, ki so potrebne za dokončanje opravila  
  
  Načrt projekta v strukturirani členitvi dela je uporabnikom poznan, vključuje pa tudi Ganttov grafikon.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Ustvarjanje strukturirane členitve dela za projekt  
 Ustvarite strukturirano členitev dela, ki bo predstavljala zaporedje opravil v projektu. Strukturirana členitev dela vključuje opravila, zahteve za vsako opravilo ter informacije o prihodkih in stroških. V strukturirani členitvi dela lahko dodate naslednje:  
  
-   Zaporedje opravil v hierarhiji  
  
-   Morebitna druga opravila, ki jih je treba dokončati pred začetkom opravila  
  
-   Začetni datum, končni datum in trajanje opravila  
  
-   Število ur, potrebnih za opravilo  
  
-   Zahtevane sposobnosti in izobrazba delavca  
  
-   Delavci, ki so dodeljeni opravilu  
  
-   Predvideni prihodki in stroški  
  
## <a name="task-types"></a>Vrste opravil  
Pri ustvarjanju strukturirane členitve dela boste uporabljali naslednje vrste opravil:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Korensko vozlišče projekta** | Opravilo povzetka na najvišji ravni za projekt. Vsa druga opravila projekta so ustvarjena pod njim. Ime korenskega opravila je ime projekta. Obseg dela, datumi in trajanje korenskega vozlišča temeljijo na vrednostih v hierarhiji pod njim. Lastnosti korenskega vozlišča ni mogoče urejati, prav tako ga ne morete izbrisati. | 
| **Opravila povzetka ali vsebnika** | Opravilo povzetka je opravilo, ki vsebuje podopravila. Opravilo povzetka nima svojega obsega dela ali stroškov. Obseg dela in stroški opravila povzetka so skupna vrednost vseh njegovih podopravil. Ime opravila povzetka lahko spremenite, ne morete pa spremeniti obsega dela, datumov ali trajanja, saj se ti izračunajo samodejno. Če izbrišete opravilo povzetka, izbrišete opravilo in vsa podopravila v njem.|  
| **Opravila listnega vozlišča** | Opravilo listnega vozlišča predstavlja najpodrobnejše delo v projektu. Vključuje predvideni obseg dela, načrtovano število virov, načrtovani začetni in končni datum ter trajanje.|

  
## <a name="task-hierarchy"></a>Hierarhija opravil  
 Pri ustvarjanju hierarhije opravil so na voljo naslednje možnosti:  
  
- **Dodaj opravilo**.   Na izbranem mestu v hierarhiji opravil lahko dodate opravilo. Če ne izberete želenega mesta, se novo opravilo prikaže na koncu.  
  
- **Zamakni opravilo**.   Zamaknite opravilo, da bo podrejeno opravilu neposredno nad njim.  
  
- **Primakni opravilo**.   Primaknite opravilo, da ne bo več podopravilo izvornega nadrejenega opravila.  
  
- **Premakni gor in Premakni dol**.   Premikajte opravila gor in dol v hierarhiji nadrejenega opravila. Premikanje opravila gor ali dol ne vpliva na njegov obseg dela, stroške, datume ali trajanje.  
  
## <a name="task-attributes"></a>Atributi opravila  
 Ime opravila opisuje delo, ki ga je treba izvesti. Za opisovanje načrtovanja in zahtev za dodeljevanje opravila posameznikom uporabljate različne atribute opravila.  
  
### <a name="schedule-attributes"></a>Atributi načrtovanja

 - Dodelite vrednosti za **Število ur obsega dela**, **Število virov**, **Začetni datum**, **Končni datum** in **Trajanje**, da določite načrt opravila. 
 - **Obseg dela** je predvideno število ur, potrebnih za dokončanje opravila.
 - **Število virov** je predvidena vrednost, ki jo vodja projekta vnese v opravilo, da ustvari optimalen načrt. 
 - **Trajanje** (v dnevih) označuje število delovnih dni, potrebnih za dokončanje opravila.  
  
### <a name="staffing-attributes"></a>Atributi števila delavcev

 - **Vloga**, **Organizacijska enota vira**, **Število virov** in **Viri** opisujejo zahteve za število oseb, potrebnih ta opravilo. 
 - **Vloga** opisuje vrsto vira, potrebnega za opravilo. 
 - **Organizacijska enota vira** označuje organizacijsko enoto, iz katere mora biti oseba, dodeljena opravilu; to vpliva tudi na predvidene stroške in prodajo za opravilo, saj se ta podatek upošteva pri določanju prodajne cene enote za vir. 
 - **Viri** določajo splošen ali poimenski vir, ko je najden samo en.  
  
## <a name="task-dependencies"></a>Odvisnosti opravila  
 Med enim ali več opravili v strukturirani členitvi dela lahko ustvarite odnose predhodnih opravil. Nastavite lahko eno ali več vrednosti za polja predhodnih opravil, da določite opravila, od katerih bodo odvisna. Ko opravilu dodelite predhodnika, se lahko začne šele, ko so vsa predhodna opravila dokončana. Če določite to odvisnost za opravilo, bo načrtovani začetni datum preračunan na najpoznejši končni datum vseh predhodnih opravil. Vplivov, ki jih imajo predhodna opravila na načrtovanje, ne omejuje način, določen za opravilo.  
  
## <a name="task-mode"></a>Način opravila  
 Način opravila je eden od pomembnih dejavnikov, ki določajo razporejanje opravil v listnem vozlišču. Za vsako opravilo sta na voljo dva načina opravila: način samodejnega načrtovanja in način ročnega načrtovanja.  
  
-   **Samodejno razporejanje**   Ko način opravila nastavite na samodejno načrtovan, orodje za načrtovanje opravila uporabi pravila za načrtovanje za naslednje atribute, da določi načrt opravila:  
  
    -   Predhodniki  
  
    -   Obseg dela  
  
    -   Število virov  
  
    -   Začetni in končni datumi  
  
-   **Pravila razporejanja**   Začetni datum opravila listnega vozlišča brez predhodnih opravil je privzeto nastavljen na začetni datum projekta. Trajanje opravila listnega vozlišča se vedno izračuna kot število delovnih dni med začetnim in končnim datumom. Ko je opravilo samodejno načrtovano, orodje za načrtovanje upošteva spodnja pravila:  
  
    -   Začetni in končni datum opravila morata biti vedno delovna dneva glede na koledar za načrtovanje projekta  
  
    -   Začetni datum opravila s predhodnimi opravili je privzeto nastavljen na najpoznejši končni datum predhodnih opravil  
  
    -   Obseg dela = število ljudi * trajanje * št. ur v standardnem delovnem dnevu koledarja projekta  
  
-   **Ročno razporejanje**.   V nekaterih primerih boste morda želeli odstopati od teh pravil. V teh primerih lahko nastavite način opravila na ročno načrtovano. Tako bo orodje za načrtovanje prenehalo izračunavati vrednosti za druge atribute načrtovanja. Nastavitev predhodnikov za opravila vedno vpliva na začetni datum odvisnih opravil.  
  
## <a name="create-a-work-breakdown-structure"></a>Ustvarjanje strukturirane členitve dela  
  
1.  Pojdite na **Project Service > Projekti**.  
  
2.  Kliknite projekt, s katerim se želite ukvarjati.  
  
3.  V vrstici na zgornjem delu zaslona izberite puščico dol poleg imena projekta, nato kliknite »Strukturirana členitev dela«.  
  
4.  Če želite dodati opravilo, kliknite **Dodaj opravilo**. Izpolnite polja za opravilo in kliknite **Shrani**.  
  
5.  Nadaljujte z dodajanjem opravil, dokler strukturirana členitev dela ni popolna. Med ustvarjanjem strukturirane členitve dela lahko za razvrščanje opravil storite naslednje:  
  
    -   Izberite opravilo in kliknite **Zamik**, da ga premaknete pod drugo opravilo, ali »Primakni«, da ga premaknete raven višje.  
  
    -   Izberite opravilo in kliknite **Premakni gor** ali **Premakni dol**, da ga premaknete na seznamu gor ali dol.  
  
    -   Kliknite **Skrij Ganttov grafikon**, da ga skrijete, ali **Pokaži Ganttov grafikon**, da ga znova prikažete.  
  
    -   Izberite drugo obdobje za Ganttov grafikon v možnosti **Časovno merilo**.  
  
6.  Če želite vloge, ki ste jih določili v strukturirani členitvi dela, dodati članom projektne ekipe, kliknite **Ustvari projektno ekipo**.  
  
7.  Ko končate spreminjanje, v spodnjem desnem kotu zaslona kliknite **Shrani**.  
  
### <a name="see-also"></a>Glejte tudi  
 [Priročnik za vodje projektov](../psa/project-manager-guide.md)
