---
title: Razreševanje lastnih cen za ocene in dejanske vrednosti
description: Ta tema vsebuje informacije o tem, kako razrešiti lastne cene za ocene in dejanske vrednosti.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d3422ef2eacc1e0617e60d41b7ddbcefe44d5b90
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084618"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Razreševanje lastnih cen za ocene in dejanske vrednosti

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Za razrešitev lastnih cen in cenika lastnih cen za ocene in dejanske podatke sistem uporablja podatke v poljih **Datum** , **Valuta** in **Pogodbena enota** povezanega projekta. Ko je cenik lastnih cen razrešen, aplikacija razreši mero stroškov.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Razrešitev mere stroškov vrstic dejanskih podatkov ali vrstic ocen za čas

Vrstice ocen za čas se nanašajo na podrobnosti ponudbe in pogodbe za dodelitev časa in virov v projektu.

Ko je cenik lastnih cen razrešen, sistem uporabi polja **Vloga** , **Podjetje, ki zagotavlja vire** in **Enota vira** , ki so v vrstici ocene za čas, za ujemanje z vrsticami za cene vloge v ceniku. To ujemanje predpostavlja, da za strošek dela uporabljate vnaprej pripravljene cenovne razsežnosti. Če ste sistem nastavili tako, da se ujema s polji, ki niso **Vloga** , **Podjetje, ki zagotavlja vire** in **Enota vira** ali še s kakšnimi poleg teh polj, potem bo uporabljena drugačna kombinacija za pridobivanje vrstic za cene vloge. Če aplikacija poišče vrstico za cene vloge z mero stroškov za kombinacijo polj **Vloga** , **Podjetje, ki zagotavlja vire** in **Enota vira** , potem je to privzeta stopnja stroška. Če aplikacija ne more najti ujemanja med vrednostmi polj **Vloga** , **Podjetje, ki zagotavlja vire** in **Enota vira** , vrstice za cene vloge pridobi z ujemajočo se vlogo, vendar z ničelnimi vrednosti polja **Enota vira**. Ko ima mera stroškov ujemajoč zapis o ceni vloge, se privzeto nastavi iz tega zapisa. 

> [!NOTE]
> Če ste konfigurirali drugo določanje prednosti polj **Vloga** , **Podjetje, ki zagotavlja vire** in **Enota vira** , ali če imate druge dimenzije z večjo prioriteto, se bo to vedenje ustrezno spremenilo. Sistem pridobi zapise o cenah vlog z ujemajočimi se vrednostmi vsake cenovne razsežnosti v prednostnem vrstnem redu z vrsticami, ki imajo ničelne vrednosti za razsežnosti, ki prihajajo nazadnje.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Razrešitev mer stroškov vrstic dejanskih podatkov ali vrstic ocen za strošek

Ocena vrstic za strošek se nanaša na ponudbo in podrobnosti pogodbe za stroške ter na vrstice ocen stroškov za projekt.

Ko je cenik lastnih cen razrešen, sistem uporabi kombinacijo polj **Kategorija** in **Enota** , ki so v vrstici ocene za strošek, za ujemanje z vrsticami **Cena kategorije** na razrešenem ceniku. Če sistem poišče vrstico s cenami kategorij, ki ima mero stroškov za kombinacijo polj **Kategorija** in **Enota** , potem je to privzeta mera stroškov. Če sistem ne more povezati vrednosti **Kategorija** in **Enota** ali če lahko najde ujemajočo se cenovno vrstico kategorije, način obračunavanja ni **Cena na enoto** , se mera stroškov privzeto nastavi na nič (0).
