---
title: Razrešitev prodajnih cen za ocene in dejanske vrednosti
description: Ta tema vsebuje informacije o tem, kako razrešiti prodajne zneske za ocene in dejanske vrednosti.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c18dd734312b2dd147381169f5c3dc38a68a601
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119573"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Razrešitev prodajnih cen za ocene in dejanske vrednosti

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ko so prodajne cene ocen in dejanskih vrednosti razrešene v aplikaciji Dynamics 365 Project Operations, sistem najprej uporabi datum in valuto ustrezne ponudbe ali pogodbe za projekt za razreševanje prodajnega cenika. Po razrešitvi prodajnega cenika sistem razreši prodajni znesek ali delež obračunavanja.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Razrešitev prodajnih zneskov vrstic dejanskih podatkov za čas ali vrstic ocen za čas

V aplikaciji Project Operations se vrstice ocene za čas uporabljajo za označevanje vrstice ponudbe in podrobnosti pogodbe za čas in dodelitve virov na projektu.

Ko je prodajni cenik razrešen, sistem izvede naslednje korake za nastavitev privzetega deleža obračunavanja.

1. Sistem uporablja polja **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira**, ki so v vrstici ocene za čas, za ujemanje z vrsticami s cenami vloge v razrešenem ceniku. To ujemanje predpostavlja, da se za deleže obračunavanja uporabljajo vnaprej pripravljene cenovne razsežnosti. Če ste cene nastavili na podlagi katerega koli drugega polja namesto polj **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira** ali poleg teh polj, potem je to kombinacija, ki bo uporabljena za pridobivanje vrstic s cenami vloge.
2. Če sistem poišče vrstico s cenami vloge, ki ima delež obračunavanja za kombinacijo polj **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira**, potem je ta delež obračunavanja privzet.
3. Če se sistem ne more ujemati z vrednostmi polj **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira**, vrstice s cenami vloge pridobi z ujemajočo se vlogo, vendar z ničelnimi vrednosti polja **Enota vira**. Ko sistem najde ujemajoč zapis o ceni vlog, nastavi delež obračunavanja tega zapisa kot privzet. To ujemanje predpostavlja vnaprej pripravljeno konfiguracijo za relativno prednost polja **Vloga** v primerjavi s poljem **Enota vira** kot razsežnost prodajnih cen.

> [!NOTE]
> Če ste konfigurirali drugo določanje prednosti polj **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira**, ali če imate druge dimenzije z večjo prioriteto, se bo to vedenje ustrezno spremenilo. Sistem pridobi zapise o cenah vlog z ujemajočimi se vrednostmi vsake cenovne razsežnosti v prednostnem vrstnem redu z vrsticami, ki imajo ničelne vrednosti za razsežnosti, ki prihajajo nazadnje.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Razrešitev prodajnih zneskov vrstic dejanskih podatkov za stroške ali vrstic ocen za stroške

V aplikaciji Project Operations se vrstice ocen za stroške uporabljajo za označevanje vrstice ponudbe in podrobnosti pogodbe za stroške in vrstic ocen stroškov na projektu.

Ko je prodajni cenik razrešen, sistem izvede naslednje korake za nastavitev privzete prodajne cene enote.

1. Sistem uporablja kombinacijo polj **Kategorija** in **Enota**, ki so v vrstici ocene za stroške, za ujemanje z vrsticami s cenami kategorij v ceniku, ki je bil razrešen.
2. Če sistem poišče vrstico s cenami kategorij, ki ima prodajni znesek za kombinacijo polj **Kategorija** in **Enota**, potem je to privzeti prodajni znesek.
3. Če sistem najde ujemajočo se vrstico s cenami kategorij, se lahko za nastavitev privzete prodajne cene uporabi način oblikovanja cen. Spodnja tabela prikazuje privzeto vedenje cene stroškov v aplikaciji Project Operations.

    | Kontekst | Način oblikovanja cen | Privzeta cena |
    | --- | --- | --- |
    | Oceni | Cena na enoto | Na osnovi vrstice s cenami kategorij |
    | &nbsp; | Nabavna cena | 0.00 |
    | &nbsp; | Pribitek na ceno | 0.00 |
    | Dejansko | Cena na enoto | Na osnovi vrstice s cenami kategorij |
    | &nbsp; | Nabavna cena | Na osnovi povezanih dejanskih stroškov |
    | &nbsp; | Pribitek na ceno | Z uporabo pribitka, ki je določen z vrstico s cenami kategorij na meri stroškov enote povezanih dejanskih stroškov |

4. Če se sistem ne more ujemati z vrednostmi polj **Kategorija** in **Enota**, se prodajni znesek privzeto nastavi na nič (0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]