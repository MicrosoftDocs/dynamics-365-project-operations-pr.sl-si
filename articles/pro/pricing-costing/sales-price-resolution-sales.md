---
title: Razreševanje prodajne cene za ocene in dejanske vrednosti – poenostavljeno
description: Ta tema vsebuje informacije o razreševanju prodajnih cen ocen in dejanskih vrednosti.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 92cebbe851c3cface86d0580e7e060134295e8c2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176766"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a>Razreševanje prodajne cene za ocene in dejanske vrednosti – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ko so prodajne cene ocen in dejanskih vrednosti razrešene v aplikaciji Dynamics 365 Project Operations, sistem najprej uporabi datum in valuto ustrezne ponudbe ali pogodbe za projekt za razreševanje prodajnega cenika. Po razrešitvi prodajnega cenika sistem razreši prodajni znesek ali delež obračunavanja.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Razrešitev prodajnih zneskov vrstic dejanskih podatkov za čas ali vrstic ocen za čas

V aplikaciji Project Operations se vrstice ocene za čas uporabljajo za označevanje vrstice ponudbe in podrobnosti pogodbe za čas in dodelitve virov na projektu.

Ko je prodajni cenik razrešen, sistem izvede naslednje korake za nastavitev privzetega deleža obračunavanja.

1. Sistem uporablja polji **Vloga** in **Enota vira**, ki so v vrstici ocene za čas, za ujemanje z vrsticami s cenami vloge v razrešenem ceniku. To ujemanje predpostavlja, da se za deleže obračunavanja uporabljajo vnaprej pripravljene cenovne razsežnosti. Če ste cene nastavili na podlagi katerega koli drugega polja namesto polj **Vloga** in **Enota vira** ali poleg teh polj, potem je to kombinacija, ki bo uporabljena za pridobivanje vrstic s cenami vloge.
2. Če sistem poišče vrstico s cenami vloge, ki ima delež obračunavanja za kombinacijo polj **Vloga** in **Enota vira**, potem je ta delež obračunavanja privzet.
3. Če se sistem ne more ujemati z vrednostmi polj **Vloga** in **Enota vira**, vrstice s cenami vloge pridobi z ujemajočo se vlogo, vendar z ničelnimi vrednosti polja **Enota vira**. Ko sistem najde ujemajoč zapis o ceni vlog, nastavi delež obračunavanja tega zapisa kot privzet. To ujemanje predpostavlja vnaprej pripravljeno konfiguracijo za relativno prednost polja **Vloga** v primerjavi s poljem **Enota vira** kot razsežnost prodajnih cen.

> [!NOTE]
> Če ste konfigurirali drugo določanje prednosti polj **Vloga** in **Enota vira**, ali če imate druge dimenzije z večjo prioriteto, se bo to vedenje ustrezno spremenilo. Sistem pridobi zapise o cenah vlog z ujemajočimi se vrednostmi vsake cenovne razsežnosti v prednostnem vrstnem redu z vrsticami, ki imajo ničelne vrednosti za razsežnosti, ki prihajajo nazadnje.

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
    | &nbsp; | Pribitek na ceno | Uporaba pribitka, ki je določen z vrstico s cenami kategorij na meri stroškov enote povezanih dejanskih stroškov |

4. Če se sistem ne more ujemati z vrednostmi polj **Kategorija** in **Enota**, se prodajni znesek privzeto nastavi na nič (0).
