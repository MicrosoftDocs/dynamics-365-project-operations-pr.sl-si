---
title: Razreševanje prodajnih cen za ocene in dejanske vrednosti projektov
description: Ta članek vsebuje informacije o reševanju prodajnih cen na podlagi projektnih ocen in dejanskih vrednosti.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9a6a19a866ab3218f2a0fa297b5f6a00ed809d2f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917504"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Razreševanje prodajnih cen za ocene in dejanske vrednosti projektov

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ko so prodajne cene za ocene in dejanske vrednosti razrešene v aplikaciji Dynamics 365 Project Operations, sistem uporabi datum in valuto povezane ponudbe projekta ali pogodbe, da najprej razreši prodajni cenik. Po razrešitvi prodajnega cenika sistem razreši prodajni znesek ali delež obračunavanja.

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

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Reševanje mer prodaje na dejanskih vrsticah in vrsticah ocen za material

V storitvi Project Operations se vrstice ocene za material se nanašajo na vrstico ponudbe in podrobnosti pogodbe za materiale in podrobnosti ocene materiala za projekt.

Ko je prodajni cenik razrešen, sistem izvede naslednje korake za nastavitev privzete prodajne cene enote.

1. Sistem uporablja kombinacijo polj **Izdelek** in **Enota** na vrstici ocene za material, ki se ujema s vrstico elementa cenika v razrešenem ceniku.
2. Če sistem najde vrstico elementa cenika, ki ima stopnjo prodaje za kombinacijo polj **Izdelek** in **Enota** in metodo za določanje cen **Valutni znesek**, se uporablja prodajna cena, navedena v vrstici cenika.
3. Če se vrednosti polj **Izdelek** in **Enota** ne ujemata, je stopnja prodaje privzeto ničelni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
