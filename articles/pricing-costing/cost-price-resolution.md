---
title: Razreševanje lastnih cen za ocene in dejanske vrednosti
description: Ta tema vsebuje informacije o tem, kako razrešiti lastne cene za ocene in dejanske vrednosti.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f9a6c3236c1d523a967155d3f1fdbe05aa00001bcc36b38afd86270c4cd1d7cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003701"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Razreševanje lastnih cen za ocene in dejanske vrednosti

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Za razrešitev lastnih cen in cenika lastnih cen za ocene in dejanske podatke sistem uporablja podatke v poljih **Datum**, **Valuta** in **Pogodbena enota** povezanega projekta. Ko je cenik lastnih cen razrešen, aplikacija razreši mero stroškov.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Razrešitev mere stroškov vrstic dejanskih podatkov ali vrstic ocen za čas

Vrstice ocen za čas se nanašajo na podrobnosti ponudbe in pogodbe za dodelitev časa in virov v projektu.

Ko je cenik lastnih cen razrešen, sistem uporabi polja **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira**, ki so v vrstici ocene za čas, za ujemanje z vrsticami za cene vloge v ceniku. To ujemanje predpostavlja, da za strošek dela uporabljate vnaprej pripravljene cenovne razsežnosti. Če ste sistem nastavili tako, da se ujema s polji, ki niso **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira** ali še s kakšnimi poleg teh polj, potem bo uporabljena drugačna kombinacija za pridobivanje vrstic za cene vloge. Če aplikacija poišče vrstico za cene vloge z mero stroškov za kombinacijo polj **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira**, potem je to privzeta stopnja stroška. Če se aplikacija ne more natančno ujemati s kombinacijo vrednosti **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira**, bo pridobila vrstice cen vlog z ujemajočo se vrednostjo vloge, vendar bosta imeli vrednosti **Enota vira** in **Podjetje, ki zagotavlja vire** vrednost nič. Ko je najden ujemajoč se zapis cene vloge z ujemajočo se vrednostjo vloge, je mera stroškov privzeta iz tega zapisa. 

> [!NOTE]
> Če ste konfigurirali drugo določanje prednosti polj **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira**, ali če imate druge dimenzije z večjo prioriteto, se bo to vedenje ustrezno spremenilo. Sistem pridobi zapise o cenah vlog z vrednostmi, ki se po prednostnem vrstnem redu ujemajo z vsako vrednostjo cenovnih razsežnosti z vrsticami, ki imajo ničelne vrednosti za tiste razsežnosti, ki so zadnje v prednostnem vrstnem redu.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Razrešitev mer stroškov vrstic dejanskih podatkov ali vrstic ocen za strošek

Ocena vrstic za strošek se nanaša na ponudbo in podrobnosti pogodbe za stroške ter na vrstice ocen stroškov za projekt.

Ko je cenik lastnih cen razrešen, sistem uporabi kombinacijo polj **Kategorija** in **Enota**, ki so v vrstici ocene za strošek, za ujemanje z vrsticami **Cena kategorije** na razrešenem ceniku. Če sistem poišče vrstico s cenami kategorij, ki ima mero stroškov za kombinacijo polj **Kategorija** in **Enota**, potem je to privzeta mera stroškov. Če sistem ne more povezati vrednosti **Kategorija** in **Enota** ali če lahko najde ujemajočo se cenovno vrstico kategorije, način obračunavanja ni **Cena na enoto**, se mera stroškov privzeto nastavi na nič (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Reševanje mer stroškov na dejanskih vrsticah in vrsticah ocen za material

Vrstice ocene za material se nanašajo na podrobnosti ponudbe in pogodbe za materiale in podrobnosti ocene materiala za projekt.

Ko je cenik z lastnimi cenami razrešen, sistem na vrstici ocene uporabi kombinacijo polj **Izdelek** in **Enota**, da se ocena materiala ujema z vrsticami **Elementi cenika** na razrešenem ceniku. Če sistem najde ceno izdelka, ki ima mero stroškov za kombinacijo polj **Izdelek** in **Enota**, se uporabi privzeta mera stroškov. Če se sistem ne more ujemati z vrednostma **Izdelek** in **Enota**, so privzeti stroški na enoto enaki nič. To se bo zgodilo tudi, če obstaja ustrezna vrstica elementa cenika, vendar metoda določanja cen temelji na standardnih stroških ali trenutnih stroških, ki v izdelku niso opredeljeni.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
