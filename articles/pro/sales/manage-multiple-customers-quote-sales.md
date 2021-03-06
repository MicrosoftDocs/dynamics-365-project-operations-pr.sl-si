---
title: Upravljanje več strank v projektnih ponudbah
description: Ta tema vsebuje informacije o delu s ponudbami z več strankami, ki bodo financirale projekt. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966866"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a>Upravljanje več strank v projektnih ponudbah (Sales)

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ponudbe za projekte podpirajo scenarij, v katerem predlog vključuje več strank, ki bodo financirale posel. Na zavihku **Povzetek** ponudbe je polje **Potencialna stranka**, ki opredeljuje primarno stranko posla. Druge stranke za posel lahko nastavite na zavihku **Stranke** pri ponudbi za projekt.

Vse stranke ponudbe na zavihku **Stranke** ponudbe za projekt so privzeto nastavljene kot stranke v podrobnostih ponudbe pri katerih koli **novih** podrobnostih ponudbe, ki temeljijo na projektu, ustvarjenih za ponudbo. Morebitne obstoječe podrobnosti ponudbe, ki temelji na projektu, ne bodo podedovale novih zapisov strank o ponudbah, ki so bili ustvarjeni pozneje.

Podrobnosti ponudb, ki temeljijo na izdelkih, so samodejno povezane s primarno stranko, ki je hkrati tudi stranka v polju **Potencialna stranka** na zavihku ponudbe **Povzetek**.

Stranke ponudbe in stranke v podrobnostih ponudbe lahko kadar koli dodate, posodobite ali izbrišete, preden je pridobljena ponudba.

## <a name="concept-of-a-primary-customer"></a>Koncept primarne stranke

Stranka, ki je na zavihku s povzetkom ponudbe projekta kot potencialna stranka, je primarna stranka ponudbe. Ko poskušate izbrisati primarno stranko s seznama strank v ponudbi, bo prikazana napaka, da zapisa primarne stranke v ponudbi ni mogoče izbrisati.

Primarne stranke se ne sme posodabljati s seznama strank na ponudbi. Na primarno stranko pa lahko vplivate tako, da spremenite potencialno stranko na zavihku ponudbe **Povzetek**. Ko je to polje posodobljeno na **Povzetek ponudbe**, je na novo izbrana potencialna stranka dodana kot stranka za novo ponudbo z nastavljeno zastavico **Primarno**. Stara potencialna stranka bo še vedno stranka na ponudbi.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Ustvarjanje, posodobitev oz. brisanje zapisa stranke ponudbe

Stranko ponudbe lahko ustvarite, posodobite ali izbrišete na zavihku **Stranke ponudbe** na strani **Ponudba**. Polja, navedena v naslednji tabeli, so pri zapisu stranke ponudbe za ponudbo za projekt.

| **Polje** | **Mesto** | **Ustreznost, namen in smernice** | **Nadaljnji vpliv** |
| --- | --- | --- | --- |
| Račun | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | Navedeni so vsi aktivni kupci. Po ustvarjanju zapisa je to polje zaklenjeno. Če ga želite posodobiti, izbrišite zapis in ga znova ustvarite. Če ste zabeležili kakršne koli dejanske podatke ali če je zapis s stranko ponudbe primarna stranka, boste lahko zapis izbrisali. | Stranke ponudbe se kopirajo kot stranke v podrobnostih pogodbe, ko se ustvari podrobnost ponudbe. Stranke ponudbe se kopirajo tudi med stranke v pogodbi za projekt, ko je pridobljena ponudba. |
| Odstotek delitve za izstavitev računa | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | Predstavlja odstotek vsake neobračunane prodajne transakcije, ki bo pripisana tej stranki ponudbe. | Kopirano v nove podrobnosti ponudbe in stranke v pogodbi za projekt. |
| Ime stika za plačilo | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | To je besedilno polje in ga je treba uporabiti za identifikacijo stika za izstavljanje računa za to stranko. Te možnosti so privzeto nastavljene prek povezanega zapisa kupca | Kopirano v stranke v pogodbi za projekt, ko je pridobljena ponudba, nato pa hkrati tudi v polje »Ime pogodbe za plačilo« na računu, ki se ustvari za to stranko. |
| Ime osebe za plačilo | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | To je besedilno polje in ga je treba uporabiti za identifikacijo stika za izstavljanje računa za to stranko. | Kopirano v stranke v pogodbi za projekt, ko je pridobljena ponudba, nato pa hkrati tudi v polje **Ime pogodbe za plačilo** na računu, ki se ustvari za to stranko. |
| Plačilni pogoji | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | To je nabor možnosti z vrednostmi, ki so privzeto nastavljene prek povezanega zapisa kupca. | Kopirano v stranke v pogodbi za projekt, ko je pridobljena ponudba, nato pa hkrati tudi v polje **Ime pogodbe za plačilo** na računu, ki se ustvari za to stranko. |
| Je zaokroževanje | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | Označuje, ali je ta stranka privzeta stranka za zaokroževanje za ta posel. | Kopirano med stranke v pogodbi za projekt, ko je pridobljena ponudba. |
| Omejitev »Ni dovoljeno preseči« | Mreža, ki jo je mogoče urejati, na zavihku **Stranke ponudbe** ter **glavnem** obrazcu in obrazcu za **hitro ustvarjanje** za stranko ponudbe. | Označuje, ali obstaja dogovorjena omejitev ali zgornja meja skupnega zneska, ki bo tej stranki zaračunan za interakcijo. | Kopirano med stranke v pogodbi za projekt, ko je pridobljena ponudba. |

## <a name="editing-billing-split-percentages"></a>Urejanje odstotkov razdelitve stroškov

Odstotke razdelitve stroškov lahko uredite z izkušnjo urejanja mreže v vrstici. Ko odstotki razdelitve stroškov ne znašajo skupno 100 %, pride do napake. Ko posodobite odstotke razdelitve stroškov, osvežite stran, da odstranite napako.

Lahko tudi poskusite izbrati **Enakomerna porazdelitev** na podmreži strank ponudbe. To dejanje dodeli odstotke razdelitve stroškov vsem strankam ponudbe. Če je prisoten dejavnik zaokroževanja, bo to dodano stranki za zaokroževanje. Ena od strank ponudbe je vedno označena kot stranka za zaokroževanje. To pomeni, da ima zapis stranke ponudbe zastavico **Zaokroževanje** nastavljeno na **Da**. Običajno je to primarna stranka ponudbe, vendar je to mogoče spremeniti.
