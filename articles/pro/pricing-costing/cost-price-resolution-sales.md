---
title: Razreševanje lastnih cen za ocene in dejanske vrednosti projektov
description: Ta tema vsebuje informacije o tem, kako se rešujejo lastne cene v ocenah projektov in dejanskih vrednostih.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2a2df7672118a4a4d7748795174e8e8238dd7618a48437185879e06a253a381
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997581"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Razreševanje lastnih cen za ocene in dejanske vrednosti projektov 

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Za razrešitev lastnih cen in cenika lastnih cen za ocene in dejanske podatke sistem uporablja podatke v poljih **Datum**, **Valuta** in **Pogodbena enota** povezanega projekta. Ko je cenik lastnih cen razrešen, aplikacija razreši mero stroškov.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Razrešitev mere stroškov vrstic dejanskih podatkov ali vrstic ocen za čas

Vrstice ocen za čas se nanašajo na podrobnosti ponudbe in pogodbe za dodelitev časa in virov v projektu.

Ko je cenik z lastnimi cenami razrešen, se polji **Vloga** in **Enota vira** v vrstici ocene časa ujemata z vrsticami cen vlog na ceniku. To ujemanje predpostavlja, da za stroške dela uporabljate standardne cenovne razsežnosti. Če ste sistem nastavili tako, da se ujema s polji, ki niso **Vloga** in **Enota vira** ali še s kakšnimi poleg teh polj, potem bo uporabljena drugačna kombinacija za pridobivanje vrstic za cene vloge. Če aplikacija poišče vrstico za cene vloge s stopnjo stroška za kombinacijo polj **Vloga** in **Enota vira**, potem je to privzeta stopnja stroška. Če aplikacija ne more najti ujemanja med vrednostmi polj **Vloga** in **Enota vira**, vrstice za cene vloge pridobi z ujemajočo se vlogo, vendar z ničelnimi vrednosti polja **Enota vira**. Ko ima mera stroškov ujemajoč zapis o ceni vloge, se privzeto nastavi iz tega zapisa. 

> [!NOTE]
> Če ste konfigurirali drugo določanje prednosti polj **Vloga** in **Enota vira**, ali če imate druge dimenzije z večjo prioriteto, se bo to vedenje ustrezno spremenilo. Sistem pridobi zapise o cenah vlog z ujemajočimi se vrednostmi vsake cenovne razsežnosti v prednostnem vrstnem redu z vrsticami, ki imajo ničelne vrednosti za razsežnosti, ki prihajajo nazadnje.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Razrešitev mer stroškov vrstic dejanskih podatkov ali vrstic ocen za strošek

Ocena vrstic za strošek se nanaša na ponudbo in podrobnosti pogodbe za stroške ter na vrstice ocen stroškov za projekt.

Ko je cenik z lastnimi cenami razrešen, sistem uporabi kombinacijo polj **Kategorija** in **Enota** polja v vrstici ocene stroškov, da se ujemajo z vrsticami **Cena kategorije** na razrešenem ceniku. Če sistem poišče vrstico s cenami kategorij, ki ima mero stroškov za kombinacijo polj **Kategorija** in **Enota**, potem je to privzeta mera stroškov. Če se vrednosti **Kategorija** in **Enota** v sistemu ne ujemata ali če sistem najde ujemajočo se vrstico cene kategorije, vendar metoda določanja cen ni **Cena na enoto**, se mera stroškov ponastavi na nič (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Reševanje mer stroškov na dejanskih vrsticah in vrsticah ocen za material

Vrstice ocene za material se nanašajo na podrobnosti ponudbe in pogodbe za materiale in podrobnosti ocene materiala za projekt.

Ko je cenik z lastnimi cenami razrešen, sistem na vrstici ocene uporabi kombinacijo polj **Izdelek** in **Enota**, da se ocena materiala ujema z vrsticami **Elementi cenika** na razrešenem ceniku. Če sistem najde ceno izdelka, ki ima mero stroškov za kombinacijo polj **Izdelek** in **Enota**, se uporabi privzeta mera stroškov. Privzeti stroški na enoto so nič, če sistem ne more ujemati vrednosti **izdelka** in **enota** ali če najde ujemajočo se vrstico elementa cenika, vendar metoda določanja cen temelji na standardnih stroških ali tekočih stroških in na izdelku ni določena nobena cena.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
