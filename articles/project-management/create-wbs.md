---
title: Ustvarjanje strukturirane členitve dela
description: V tej temi je pojasnjeno, kako ustvarite strukturirano členitev dela (SČD), ki vključuje osnovne kontrolnike v novem vmesniku za načrtovanje.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d7fa645e78d2206e333d9f85fcec0f7a9c213c23
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841403"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Ustvarjanje strukturirane členitve dela (SČD)

Razpored projekta sporoča, katera opravila je treba opraviti, kateri viri jih bodo opravili in kakšen je časovni okvir, v katerem je treba dokončati delo. Načrt vključuje vsa opravila, ki so povezana s pravočasno oddajo projekta. V rešitvi Dynamics 365 Project Operations ustvarite urnik projekta tako:

  - Razčlenite delo v obvladljiva opravila.
  - Ocenite, koliko časa je potrebnega za izvedbo posameznega opravila.
  - Nastavite odvisnosti opravil.
  - Nastavite trajanje opravil.
  - Ocenite splošne vire, ki bodo izvedi opravila. 

Razpored projekta se ustvari na zavihku **Načrtovanje** na strani **Projekt**.

## <a name="tasks"></a>Opravila

Prvi korak pri ustvarjanju razporeda projekta je razčlenitev dela v obvladljive dele. Razpored v aplikaciji Project Operations podpira te funkcije:

- Opravila povzetka ali vsebnika
- Opravila listnega vozlišča

### <a name="summary-tasks"></a>Opravila povzetka

Opravila povzetka lahko shranijo druga opravila povzetka ali opravila listnega vozlišča. Nimajo pa svojega obsega dela ali stroškov. Namesto tega so njihov obseg dela in stroški skupna vrednost obsega dela in stroškov opravil vsebnika. Začetni datum opravila povzetka je začetni datum opravil vsebnika, končni datum pa končni datum opravil vsebnika. Ime opravila povzetka lahko urejate, lastnosti razporejanja, vključno z obsegom, datumi in trajanjem, pa ne. Če izbrišete opravilo povzetka, izbrišete tudi vsa njegova opravila vsebnika.

### <a name="leaf-node-tasks"></a>Opravila listnega vozlišča

Opravila listnega vozlišča predstavljajo najbolj razčlenjeno delo v projektu. Imajo predvideni obseg dela, vire, načrtovani začetni in končni datum ter trajanje.

## <a name="create-a-task-hierarchy"></a>Ustvarjanje hierarhije opravil

### <a name="add-a-task"></a>Dodajanje opravila

Sledite spodnjim korakom, da dodate eno ali več opravil.

1. Pojdite na **Projekti** ter izberite in odprite zapis projekta, za katerega želite ustvariti razpored. 
2. Izberite zavihek **Opravila**. 
3. Izberite **Dodaj novo opravilo**, vnesite ime opravila in pritisnite Enter.
2. Vnesite novo ime opravila in znova pritisnite Enter, da ustvarite celoten seznam opravil.

### <a name="manage-hierarchy-of-a-task"></a>Upravljanje hierarhije opravila

Ko je opravilo zamaknjeno, postane podrejeni element opravila, ki je neposredno nad njim. ID razporeda opravila se nato znova izračuna tako, da temelji na ID-ju razporeda njegovega novega nadrejenega elementa in sledi shemi za oštevilčevanje orisa. Nadrejeno opravilo je zdaj opravilo povzetka. Zato postane skupna vrednost podrejenih opravil. Ko opravilo povišate, ni več podrejeni element svojega nadrejenega opravila. ID razporeda se nato znova izračuna tako, da odraža posodobljeno globino in mesto opravila v hierarhiji. Obseg dela, cena in datumi prejšnjega nadrejenega opravila se preračunajo, tako da ne vključujejo tega opravila.

Sledite spodnjim korakom, da zamaknete ali povišate opravilo.

1. Na strani **Projekt** na zavihku **Opravila** pod možnostjo **Opravila povzetka** izberite tri navpične pike ob imenu opravila in nato **Ustvari podopravilo**. 
2. Izberite opravilo, ki ga želite zamakniti ali povišati. Če želite izbrati več opravil, izberite opravilo, pritisnite in držite Ctrl ter nato izberite dodatna opravila.
2. Izberite **Zamik** ali **Povišaj podopravilo**, da premaknete opravila pod opravila povzetka ali iz njih.

### <a name="move-tasks-up-and-down"></a>Premikanje opravil gor in dol

Opravila lahko premaknete na poljubno raven v strukturirani členitvi dela na enega od dveh načinov:

- Izberite eno ali več opravil in jih povlecite na želeno mesto.
- Izberite eno ali več opravil, z desno miškino tipko kliknite in izberite **Izreži**, izberite ciljno celico v razporedu in nato z desno miškino tipko kliknite in izberite **Prilepi**.

## <a name="task-attributes"></a>Atributi opravila

Ime opravila opisuje delo, ki ga je treba izvesti. V aplikaciji Project Operations atributi, ki so povezani z opravilom, opisujejo razpored opravila in zahteve za dodelitev osebja.

## <a name="schedule-attributes"></a>Atributi načrtovanja

Atributi **Obseg dela**, **Začetni datum**, **Končni datum** in **Trajanje** določajo razpored za opravilo.

Spodnja tabela prikazuje dodatne atribute razporeda.

| **Končno prikazano ime** | **Končni opis** |
| --- | --- |
| Končni obseg dela (ure) | Dokončano delo za opravilo v urah. |
| Trajanje | Prikaže trajanje opravila v dneh. |
| Skupni obseg dela | Skupno delo za opravilo v urah. |
| Konec | Datum in ura konca. |
| % končano | Odstotek končanega opravila. |
| Vedro projekta | Ploščo opravil lahko razvrstite po vedru tako, da ima vsako vedro svoj stolpec. |
| Preostanek dela (ure) | Preostalo delo za opravilo v urah. |
| Zaženi | Datum in ura začetka. |
| Imenu | Ime opravila. |
| ID | ID opravila v strukturirani členitvi dela. |

## <a name="staffing-attributes"></a>Atributi števila delavcev

Do atributov za dodelitev osebja lahko dostopate prek polja **Viri** v razporedu. Poiščete lahko obstoječi vir ali izberete **Ustvari** in v podoknu **Hitro ustvarjanje** dodate člana projektne ekipe kot nov vir.

Polja **Vloga**, **Enota vira** in **Ime položaja** se uporabljajo za opis zahtev za dodelitev osebja za opravilo. Ti atributi za dodelitev osebja se skupaj z razporedom opravila uporabljajo za iskanje razpoložljivih virov za to opravilo.

   - **Vloga**: določite vrsto vira, ki se zahteva za opravilo.
   - **Enota vira**: določite enoto, iz katere se dodelijo viri za opravilo. Ta atribut vpliva na oceno stroškov in prodaje za opravilo, če sta mera stroškov in delež obračunavanja za vir nastavljena na podlagi enot vira.
   - **Naziv delovnega mesta**: vnesite ime za splošni vir, ki služi kot označba mesta za vir, ki bo opravil delo.

Polje **Viri** vsebuje naziv delovnega mesta splošnega vira ali poimenovanega vira, če ga je mogoče najti.

Polje **Kategorija** vsebuje vrednosti, ki označujejo obširnejšo vrsto dela, v katero je bilo razvrščeno opravilo. To polje ne vpliva na razporejanje ali dodeljevanje osebja. Polje se uporablja samo za poročanje.

## <a name="task-dependencies"></a>Odvisnosti opravila

Razpored v aplikaciji Project Operations lahko uporabite za ustvarjanje odnosov predhodnih opravil med opravili. Polje **Predhodnik** uporabi eno ali več vrednosti, da označi opravila, od katerih je odvisno opravilo. Ko opravilu dodelite vrednosti predhodnega opravila, se opravilo lahko začne šele, ko so vsa predhodna opravila dokončana. Zaradi te odvisnosti se načrtovani začetni datum opravila ponastavi na datum, ko so dokončana predhodna opravila.

Način opravila ne vpliva na posodobitve začetnega in končnega datuma predhodnih/odvisnih opravil.

## <a name="accessibility-and-keyboard-shortcuts"></a>Pripomočki za osebe s posebnimi potrebami in bližnjice na tipkovnici

Mreža **Razpored** v celoti podpira pripomočke za osebe s posebnimi potrebami in se lahko uporablja z bralniki zaslona, kot so Pripovedovalec, JAWS in NVDA. Po mreži se lahko pomikate s puščičnimi tipkami (kot v aplikaciji Microsoft Excel), lahko uporabite tipko Tab za pomikanje po interaktivnih elementih uporabniškega vmesnika, lahko pa uporabite tudi tipko s puščico dol, tipko Enter ali preslednico, da izberete in odprete spustne menije.
