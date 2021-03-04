---
title: Razporedi projektov
description: Ta tema vsebuje informacije o ustvarjanju razporeda.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 2877f12a9ea3d288c4cf41f406cd8ca3e6cee821
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148438"
---
# <a name="project-schedules"></a>Razporedi projektov 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Razpored projekta sporoča, katera opravila je treba opraviti, kateri viri jih bodo opravili in kakšen je časovni okvir, v katerem je treba opraviti delo. Odraža celotno delo, ki je povezano s pravočasno oddajo projekta. V aplikaciji Dynamics 365 Project Service Automation ustvarite razpored projekta tako, da razčlenite delo v obvladljiva opravila, ocenite čas, ki je potreben za vsako opravilo, nastavite odvisnosti opravila in trajanje opravila ter ocenite splošne vire, ki bodo izvedli opravila. Razpored projekta se ustvari na zavihku **Načrtovanje** na strani projekta.
 
## <a name="tasks"></a>Opravila

Prvi korak pri ustvarjanju razporeda projekta je razčlenitev dela v obvladljive dele. Razpored v PSA podpira te funkcije:

- Korensko vozlišče projekta
- Opravila povzetka ali vsebnika
- Opravila listnega vozlišča

### <a name="project-root-node"></a>Korensko vozlišče projekta

Korensko vozlišče projekta je opravilo povzetka na najvišji ravni za projekt. Vsa druga opravila projekta so ustvarjena pod njim. Ime korenskega vozlišča je vedno nastavljeno na ime projekta. Obseg dela, datumi in trajanje korenskega vozlišča so povzeti glede na vrednosti v hierarhiji pod njim. Lastnosti korenskega vozlišča ne morete urejati. Prav tako ne morete izbrisati korenskega vozlišča.

### <a name="summary-or-container-tasks"></a>Opravila povzetka ali vsebnika 

Opravila povzetka imajo pod sabo podopravila ali opravila vsebnika. Nimajo pa svojega obsega dela ali stroškov. Namesto tega so njihov obseg dela in stroški skupna vrednost obsega dela in stroškov opravil vsebnika. Začetni datum opravila povzetka je začetni datum opravil vsebnika, končni datum pa končni datum opravil vsebnika. Ime opravila povzetka lahko urejate, lastnosti razporejanja (obseg, datumi in trajanje) pa ne. Če izbrišete opravilo povzetka, izbrišete tudi vsa njegova opravila vsebnika.

### <a name="leaf-node-tasks"></a>Opravila listnega vozlišča

Opravila listnega vozlišča predstavljajo najbolj razčlenjeno delo v projektu. Imajo predvideni obseg dela, vire, načrtovani začetni in končni datum ter trajanje.
 
## <a name="creating-a-task-hierarchy"></a>Ustvarjanje hierarhije opravil

Za ustvarjanje hierarhije opravil lahko uporabite te možnosti:

- Gumb **Dodaj opravilo**
- Gumb **Zamakni opravilo**
- Gumb **Primakni opravilo**
- Gumba **Premakni gor** in **Premakni dol**
- Pripomočki za osebe s posebnimi potrebami in bližnjice na tipkovnici

### <a name="add-task"></a>Dodaj opravilo

Gumb **Dodaj opravilo** vam omogoča ustvarjanje novega opravila v hierarhiji. Če ne izberete mesta, se opravilo vstavi na koncu. 

Vsakemu opravilu je dodeljen ID razporeda. ID razporeda predstavlja globino in mesto opravila v hierarhiji. Uporablja oštevilčevanje orisa. Za opravila na prvi ravni pod korenskim vozliščem projekta se uporablja shema oštevilčevanja 1, 2, 3 in tako naprej. Za opravila pod prvo ravnjo se uporablja shema oštevilčevanja 1.1, 1.2, 1.3 in tako naprej.

### <a name="indent-task"></a>Zamakni opravilo

Ko je opravilo zamaknjeno, postane podrejeni element opravila, ki je neposredno nad njim. ID razporeda opravila se nato znova izračuna tako, da temelji na ID-ju razporeda njegovega novega nadrejenega elementa in sledi shemi za oštevilčevanje orisa. Nadrejeno opravilo je zdaj opravilo povzetka ali opravilo vsebnika. Zato postane skupna vrednost podrejenih opravil.

### <a name="outdent-task"></a>Primakni opravilo 

Ko primaknete opravilo, ni več podrejeni element svojega nadrejenega opravila. ID razporeda se nato znova izračuna tako, da odraža posodobljeno globino in mesto opravila v hierarhiji. Obseg dela, cena in datumi prejšnjega nadrejenega opravila se preračunajo, tako da ne vključujejo tega opravila.

### <a name="move-up-and-move-down"></a>Premakni gor in Premakni dol 

Gumba **Premakni gor** in **Premakni dol** spremenita mesto opravila v njegovi nadrejeni hierarhiji. Spremembe te vrste ne vplivajo na obseg dela, ceno, datume ali trajanje opravila. Vplivajo samo na ID razporeda opravila. ID razporeda se nato znova izračuna tako, da odraža novo mesto opravila na nadrejenem seznamu podrejenih opravil.

### <a name="accessibility-and-keyboard-shortcuts"></a>Pripomočki za osebe s posebnimi potrebami in bližnjice na tipkovnici

Mreža **Razpored** v celoti podpira pripomočke za osebe s posebnimi potrebami in se lahko uporablja z bralniki zaslona, kot so Pripovedovalec, JAWS in NVDA. Po mreži se lahko pomikate s puščičnimi tipkami (kot v aplikaciji Microsoft Excel), lahko uporabite tipko Tab za pomikanje po interaktivnih elementih uporabniškega vmesnika, lahko pa uporabite tudi tipko s puščico dol, tipko Enter ali preslednico, da izberete in prikličete spustne menije. Glave stolpcev so prav tako interaktivne. Lahko skrijete in prikažete stolpce, uporabite tipko Tab in puščične tipke za pomikanje po glavah stolpcev ter uporabite interaktivne gumbe v orodni vrstici. Poleg tega lahko uporabljate te bližnjice na tipkovnici:

- **Osveži**: ALT + SHIFT + F5
- **Dodaj**: ALT + SHIFT + Insert
- **Izbriši**: ALT + SHIFT + Delete
- **Premakni gor/dol**: ALT + SHIFT + puščica gor/dol
- **Zamakni/primakni**: ALT + SHIFT + puščica levo/desno
- **Razširi/strni hierarhije**: ALT + SHIFT + tipka plus/minus

## <a name="task-attributes"></a>Atributi opravila

Ime opravila opisuje delo, ki ga je treba izvesti. V PSA atributi, ki so povezani z opravilom, opisujejo razpored opravila in zahteve za dodelitev osebja.

> ![Atributi opravila](media/project-2.png)
 
### <a name="schedule-attributes"></a>Atributi načrtovanja

Atributi **Obseg dela**, **Začetni datum**, **Končni datum** in **Trajanje** določajo razpored za opravilo.

Dodatni atributi razporeda vključujejo:

- **Ure dela**: vnesite predvideno število ur, potrebnih za dokončanje opravila. 
- **Trajanje**: določite število delovnih dni, potrebnih za dokončanje opravila.
- **ID razporeda**: ta samodejno ustvarjeni ID se uporablja za razporejanje opravil v hierarhiji. Odvisnosti med opravili upravljajo dejanski vrstni red, v katerem se izvedejo opravila.
 
### <a name="staffing-attributes"></a>Atributi števila delavcev

Do atributov za dodelitev osebja lahko dostopate prek polja **Viri** v razporedu. Poiščete lahko obstoječi vir ali kliknete **Ustvari** in v podoknu **Hitro ustvarjanje** dodate člana projektne ekipe kot nov vir.

Polja **Vloga**, **Enota vira** in **Ime položaja** se uporabljajo za opis zahtev za dodelitev osebja za opravilo. Ti atributi za dodelitev osebja se skupaj z razporedom opravila uporabljajo za iskanje razpoložljivih virov za to opravilo.

**Vloga** – določite vrsto vira, ki se zahteva za opravilo.

**Enota vira** – določite enoto, iz katere se dodelijo viri za opravilo. Ta atribut vpliva na oceno stroškov in prodaje za opravilo, če sta mera stroškov in delež obračunavanja za vir nastavljena na podlagi enot vira.

**Naziv delovnega mesta** – vnesite prijazno ime za splošni vir, ki služi kot označba mesta za vir, ki bo opravil delo.

Polje **Viri** vsebuje naziv delovnega mesta splošnega vira ali poimenovanega vira, če ga je mogoče najti.

Polje **Kategorija** vsebuje vrednosti, ki označujejo obširnejšo vrsto dela, v katero je bilo razvrščeno opravilo. To polje ne vpliva na razporejanje ali dodeljevanje osebja. Uporablja se samo za poročanje.

### <a name="task-dependencies"></a>Odvisnosti opravila 

Razpored v PSA lahko uporabite za ustvarjanje predhodnih odnosov med opravili. Polje **Predhodnik** pod možnostjo **Opravila** uporabi eno ali več vrednosti, da označi opravila, od katerih je odvisno opravilo. Ko opravilu dodelite vrednosti predhodnega opravila, se opravilo lahko začne šele, ko so vsa predhodna opravila dokončana. Zaradi te odvisnosti se načrtovani začetni datum opravila ponastavi na datum, ko so dokončana predhodna opravila.

Način opravila ne vpliva na posodobitve začetnega in končnega datuma predhodnih/odvisnih opravil.

## <a name="task-mode"></a>Način opravila 

Način opravila določa razporejanje opravil v listnem vozlišču. PSA za vsako opravilo podpira dva načina opravila: samodejno razporejanje in ročno razporejanje.

### <a name="auto-scheduling"></a>Samodejno razporejanje 
 
Ko je način opravila nastavljen na **Samodejno razporejeno**, mehanizem razporejanja opravila uporabi pravila za razporejanje v atributih opravila, da določi razpored za opravilo.

#### <a name="scheduling-rules"></a>Pravila razporejanja

Če opravilo v listnem vozlišču nima predhodnih opravil, je njegov začetni datum privzeto nastavljen na načrtovani začetni datum projekta. Trajanje opravila listnega vozlišča se vedno izračuna kot število delovnih dni med začetnim in končnim datumom. Ko je opravilo samodejno razporejeno, mehanizem razporejanja upošteva ta pravila:

- Začetni in končni datum opravila morata biti delovna dneva glede na koledar za načrtovanje projekta. 
- Pri opravilih, ki imajo predhodna opravila, je začetni datum samodejno nastavljen na najpoznejši končni datum predhodnih opravil.
- Obseg dela se izračuna s to formulo: število ljudi × trajanje × ure na standardni delovni dan v koledarju projekta.

### <a name="manual-scheduling"></a>Ročno razporejanje

Če pravila samodejnega razporejanja ne izpolnjujejo vaših zahtev, lahko nastavite način opravila na **Ročno razporejeno**. S to nastavitvijo mehanizem razporejana preneha izračunavati vrednosti za druge atribute razporejanja. Če v opravilih nastavite predhodna opravila, vedno vplivate na začetni datum odvisnega opravila, ne glede na način opravila.
