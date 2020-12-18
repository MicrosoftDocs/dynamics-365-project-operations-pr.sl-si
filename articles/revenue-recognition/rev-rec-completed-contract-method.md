---
title: Upravljanje ocen prihodkov
description: Ta tema vsebuje informacije o tem, kako delati z ocenami prihodkov za projekte.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531555"
---
# <a name="manage-revenue-estimates"></a>Upravljanje ocen prihodkov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ocene prihodkov lahko ustvarite, izračunate, knjižite, razveljavite ali odstranite. To lahko storite ročno ali z uporabo periodičnega postopka. Ta tema vsebuje informacije o tem, kako delati z ocenami prihodkov za projekte.

### <a name="manage-revenue-estimates-manually"></a>Ročno upravljanje ocen prihodkov

V projektu ocene prihodka s fiksno ceno ali strani **Povpraševanje za oceno** (**Upravljanje projektov in računovodstvo** > **Poročila in povpraševanja** > **Povpraševanja in poročila za ocene**) izberite **Ocene**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Upravljanje ocen prihodkov s periodičnim postopkom

Odprite **Upravljanje projektov in računovodstvo** > **Periodično** > **Ocene** in izberite ustrezen postopek.

## <a name="create-a-revenue-estimate"></a>Ustvarjanje ocene prihodka

Če želite ustvariti oceno prihodka, izvedite naslednje korake. 

1. Odprite **Upravljanje projektov in računovodstvo** > **Periodično** > **Ocene**.
2. Izberite **Novo**. Na strani **Ustvarjanje ocene** izberite naslednje parametre:

   - **Koda obdobja**: ta koda določa, kako pogosto se knjižijo ocene.
   - **Datum ocene**: datum obdelave ocene.
   - **Neprekinjeno**: izberite to potrditveno polje, če želite ustvariti ocene samo, če so bile ocene objavljene v prejšnjem obdobju ali če je ta ocena prva, ki je bila ustvarjena. Če ta možnost ni izbrana, se ustvarijo ocene, tudi če v prejšnjem obdobju ni bila objavljena nobena ocena.
   - **Metoda za izračun stroškov za dokončanje**: določite, kako oceniti preostalo projektno delo. Za več informacij glejte [Metoda za izračun stroškov za dokončanje](cost-complete-methods.md).
   - **Način za izračun dokončanja**: izberite enega od spodnjih načinov za izračun dokončanja:
     - **Samodejno**: odstotek dokončanja se izračuna samodejno in temelji na vrsticah cene, vključenih v izračun. Predloga stroškov določa vključene vrstice cene.
     - **Ročno**: odstotek dokončanja je enak odstotku dokončanja zadnje ocene. Po izdelavi ocene lahko spremenite **Ročni izračun** na strani **Ocene**.
     - **Iz predloge stroškov**: kombinacija samodejnega in ročnega načina. Ta možnost se nastavi samodejno ali ročno, odvisno od privzete vrednosti v predlogi stroškov.
   - **Model napovedi**: izberite model napovedi za oceno.
   - **Natisni seznam ocen**: ustvarite in prikažite seznam ocen. Seznam vsebuje stanje trenutne funkcije. Na poročilo lahko natisnete kakršno koli opozorilo glede ocene. Zaradi naslednjih pogojev se na seznamu ocen pojavijo določena opozorila:
     - Odstotek dokončanja znaša več kot 100 odstotkov.
     - Odstotek dokončanja znaša manj kot nič odstotkov.
     - Negativni znesek v stolpcu **Do konca**.
     - Ocena brez ustreznega zneska pogodbe.
     - Ocena brez priložene ocene stroškov.
   - **Pokaži dnevnik z informacijami**: izberite to možnost, če želite prejeti sporočilo, ki vsebuje informacije o ocenjevalnih projektih, ki so bili obdelani med izvajanjem opravila.


## <a name="post-wip-or-accruals"></a>Knjiženje WIP ali razmejitev

Ko so ocene ovrednotene, se ohranijo take, kot so, ali se zmanjšajo oziroma povečajo. WIP lahko nato knjižite, kadar delate z načelom ocenjevanja **Izpolnjena pogodba** oziroma knjižite razmejitve, kadar delate z načelom ocenjevanja **Odstotek dokončanja**.
  
Stanje ocenjevalnega obdobja se spremeni iz **Ustvarjeno** v **Knjiženo**.

## <a name="reverse-wip-or-accruals"></a>Razveljavitev WIP ali razmejitev

Uporabite možnost razveljavitve, da knjižene WIP-e ali razmejitve pišete v dobro in nato ustvarite ocene za obdobje.

> [!NOTE]
> Če želite razveljaviti obdobje znotraj drugih obdobij, razveljavite potrebna ocenjevalna obdobja in jih ponovno poknjižite. Pri tem ne izpustite nobenega obdobja, ker so vsa naslednja obdobja odvisna od ocen iz prejšnjega obdobja.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Izločite ocenjeni projekt in dokončajte projekt

Zadnji korak v postopku ocenjevanja je izločitev ocenjevalnega projekta in zaključitev projekta s fiksno ceno, ko odstotek dokončanja doseže 100 odstotkov.

Med izločitvijo se zgodi naslednje:

- Za projekt s fiksno ceno z zaključeno pogodbo se vrednosti WIP izbrišejo iz bilančnih računov in knjižijo v izkaz poslovnega izida.
- Za projekt s fiksno ceno s stoodstotno dokončanostjo se razmejitve odstranijo iz izkaza poslovnega izida.

Ocena spremeni stanje v **Izločeno**.

> [!NOTE]
> V posebnih primerih lahko odstotek preseže 100 odstotkov. Ko se to zgodi, zmanjšajte odstotek dokončanja z atributom **Nastavi metodo za izračun stroškov za dokončanje na nič**, da dosežete 100 odstotkov.

## <a name="reverse-elimination"></a>Razveljavitev izločitve

1. Pojdite v **Upravljanje projektov in računovodstvo** > **Periodično** > **Ocene** > **Razveljavitev izločitve**. 
2. V podoknu za dejanja na zavihku **Postopek** v skupini **Vzdrževanje** izberite **Ocena**. 
3. Izberite **Razveljavitev izločitve**.

Na tej strani razveljavite vse izločitve z določenim datumom ocene in stanjem ocene **Izločeno**. Stanje transakcije se spremeni, ko izberete ustrezna polja.

S tem boste tudi samodejno spremenili stanje projekta v **V teku**, če je stopnja projekta nastavljena na končano. Stanje ocene projektnega obdobja se spremeni nazaj na **Knjiženo**.
