---
title: Upravljanje več strank v ponudbah za projekte
description: Ta tema vsebuje informacije o delu s ponudbami, ki vključujejo več strank, ki bodo financirale projekt.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908610"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Upravljanje več strank v ponudbah za projekte

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Ponudbe za projekte podpirajo scenarij, v katerem predlog vključuje več strank, ki bodo financirale posel. Na zavihku **Povzetek** ponudbe je polje **Potencialna stranka**, ki opredeljuje primarno stranko posla. Druge stranke za posel lahko nastavite na zavihku **Stranke** pri ponudbi za projekt.

Vse stranke ponudbe na zavihku **Stranke** ponudbe za projekt so privzeto nastavljene kot stranke v podrobnostih ponudbe pri katerih koli **novih** podrobnostih ponudbe, ki temeljijo na projektu, ustvarjenih za ponudbo. Morebitne obstoječe podrobnosti ponudbe, ki temelji na projektu, ne bodo podedovale novih zapisov strank o ponudbah, ki so bili ustvarjeni pozneje.

Stranke ponudbe in stranke v podrobnostih ponudbe lahko kadar koli dodate, posodobite ali izbrišete, preden je pridobljena ponudba. Veljavna stranka na ponudbi mora biti nastavljena kot stranka v lastniškem podjetju ali pravni osebi na strani **Stranke**. Pravne osebe so nastavljene v modulu **Vodenje projektov in računovodstvo** v storitvi Dynamics 365 Project Operations ter so na voljo kot podjetja v modulih storitve Project Operations **Prodaja in izvedba projektov**.

## <a name="concept-of-a-primary-customer"></a>Koncept primarne stranke

Stranka, ki je na zavihku ponudbe projekta **Povzetek** navedena kot potencialna stranka, je primarna stranka ponudbe. Če poskušate izbrisati primarno stranko s seznama strank v ponudbi, bo prikazana napaka, da zapisa primarne stranke v ponudbi ni mogoče izbrisati.

Primarne stranke se ne sme posodabljati s seznama strank na ponudbi. Na primarno stranko pa lahko vplivate tako, da spremenite potencialno stranko na zavihku ponudbe **Povzetek**. Ko je to polje posodobljeno na **Povzetek ponudbe**, je na novo izbrana potencialna stranka dodana kot stranka za novo ponudbo z nastavljeno zastavico **Primarno**. Stara potencialna stranka bo še vedno stranka na ponudbi.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Ustvarjanje, posodobitev oz. brisanje zapisa stranke ponudbe

Stranko ponudbe lahko ustvarite, posodobite ali izbrišete na zavihku **Stranke ponudbe** na strani **Ponudba**. Polja, navedena v naslednji tabeli, so pri zapisu stranke ponudbe za ponudbo za projekt.

| **Polje** | **Mesto** | **Ustreznost, namen in smernice** | **Nadaljnji vpliv** |
| --- | --- | --- | --- |
| Kupec | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | Navedeni so vsi aktivni kupci. Po ustvarjanju zapisa je to polje zaklenjeno. Če ga želite posodobiti, izbrišite zapis in ga znova ustvarite. Če ste zabeležili kakršne koli dejanske podatke ali če je zapis s stranko ponudbe primarna stranka, boste lahko zapis izbrisali. | Stranke ponudbe se kopirajo kot stranke v podrobnostih pogodbe, ko se ustvari podrobnost ponudbe. Stranke ponudbe se kopirajo tudi med stranke v pogodbi za projekt, ko je pridobljena ponudba. |
| Odstotek delitve za izstavitev računa | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | Predstavlja odstotek vsake neobračunane prodajne transakcije, ki bo pripisana tej stranki ponudbe. | Kopirano v nove ustvarjene podrobnosti ponudbe in stranke v pogodbi za projekt. |
| Ime stika za plačilo | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | To je besedilno polje in ga je treba uporabiti za identifikacijo stika za izstavljanje računa za to stranko. Te možnosti so privzeto nastavljene prek povezanega zapisa kupca | Kopirano v stranke v pogodbi za projekt, ko je pridobljena ponudba, nato pa hkrati tudi v polje »Ime pogodbe za plačilo« na računu, ki se ustvari za to stranko. |
| Ime osebe za plačilo | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | To je besedilno polje in ga je treba uporabiti za identifikacijo stika za izstavljanje računa za to stranko. | Kopirano v stranke v pogodbi za projekt, ko je pridobljena ponudba, nato pa hkrati tudi v polje **Ime pogodbe za plačilo** na računu, ki se ustvari za to stranko. |
| Plačilni pogoji | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | To je nabor možnosti z vrednostmi, ki so privzeto nastavljene prek povezanega zapisa kupca. | Kopirano v stranke v pogodbi za projekt, ko je pridobljena ponudba, nato pa hkrati tudi v polje **Ime pogodbe za plačilo** na računu, ki se ustvari za to stranko. |
| Je zaokroževanje | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | Označuje, ali je ta stranka privzeta stranka za zaokroževanje za ta posel. | Kopirano med stranke v pogodbi za projekt, ko je pridobljena ponudba. |
| Lastniško podjetje | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | Pravna oseba, pri kateri je ta stranka nastavljena v modulu **Vodenje projektov in računovodstvo**. To polje je samo za branje in je nastavljeno na lastniško podjetje same ponudbe. Seznam strank, ki jih želite dodati v polje **Kupec**, je že filtrirano na seznam od tega lastniškega podjetja v modulu Project Operations **Vodenje projektov in računovodstvo**. | Lastniško podjetje je enako konceptu pravne osebe v modulu **Vodenje projektov in računovodstvo** storitve Project Operations. Vsi stroški in prihodki, ki nastanejo pri tem projektu, se zabeležijo v glavni knjigi lastniškega podjetja. |
| Omejitev »Ni dovoljeno preseči« | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | Označuje, ali obstaja dogovorjena omejitev ali zgornja meja skupnega zneska, ki bo tej stranki zaračunan za interakcijo. | Kopirano med stranke v pogodbi za projekt, ko je pridobljena ponudba. |

## <a name="editing-billing-split-percentages"></a>Urejanje odstotkov razdelitve stroškov

Odstotke razdelitve stroškov lahko uredite z izkušnjo urejanja mreže v vrstici. Ko odstotki razdelitve stroškov ne znašajo skupno 100 %, pride do napake. Ko posodobite odstotke razdelitve stroškov, osvežite stran, da odstranite napako.

Lahko tudi poskusite izbrati **Enakomerna porazdelitev** na podmreži strank ponudbe. To dejanje dodeli odstotke razdelitve stroškov vsem strankam ponudbe. Če je prisoten dejavnik zaokroževanja, bo to dodano stranki za zaokroževanje. Ena od strank ponudbe je vedno označena kot stranka za zaokroževanje. To pomeni, da ima zapis stranke ponudbe zastavico **Zaokroževanje** nastavljeno na **Da**. Običajno je to primarna stranka ponudbe, vendar je to mogoče spremeniti.