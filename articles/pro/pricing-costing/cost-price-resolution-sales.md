---
title: Določitev mer stroškov za ocene in dejanske vrednosti projektov
description: Ta članek vsebuje informacije o tem, kako se določijo mere stroškov v ocenah projektov in dejanskih vrednostih.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475256"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Določitev mer stroškov za ocene in dejanske vrednosti projektov

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Za določitev mer stroškov na podlagi ocen in dejanskih vrednosti v programu Microsoft Dynamics 365 Project Operations sistem najprej uporabi datum in valuto v dohodni oceni ali dejanskem kontekstu, da določi cenik z lastnimi cenami. Konkretno v dejanskem kontekstu sistem uporablja polje **Datum transakcije** za določitev, kateri cenik velja. Vrednost **Datum transakcije** dohodne ocene ali dejanske vrednosti se primerja z vrednostma **Veljavni datum začetka (neodvisno od časovnega pasu)** in **Veljavni datum konca (neodvisno od časovnega pasu)** na ceniku. Ko je cenik z lastnimi cenami določen, sistem določi mero stroškov. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Določanje mere stroškov za kontekst ocenjevanja in dejanski kontekst za čas

Kontekst ocenjevanja za **Čas** se nanaša na:

- Podrobnosti vrstice ponudb za **Čas**.
- Podrobnosti vrstice pogodb za **Čas**.
- Dodelitev virov v projektu.

Dejanski kontekst za **Čas** se nanaša na:

- Vrstice dnevnika vnosa in popravkov za **Čas**.
- Vrstice dnevnika, ki se ustvarijo, ko je poslan časovni vnos.

Ko je cenik z lastnimi cenami določen, sistem izvede naslednje korake za vnos privzete mere stroškov.

1. Sistem se ujema s kombinacijo polj **Vloga** in **Enota vira** v oceni ali dejanskem kontekstu za **Čas** proti vrsticam s cenami vlog v ceniku. To ujemanje predpostavlja, da za stroške dela uporabljate standardne cenovne razsežnosti. Če ste sistem nastavili tako, da se ujema s polji, ki niso **Vloga** in **Enota vira** ali še s kakšnimi poleg teh polj, potem je uporabljena drugačna kombinacija za pridobivanje vrstic za cene vloge.
1. Če sistem poišče vrstico za cene vlog z mero stroškov za kombinacijo polj **Vloga** in **Enota vira**, potem je ta mera stroškov uporabljena kot privzeta mera stroškov.
1. Če se sistem ne more ujemati z vrednostmi **Vloga** in **Enota vira**, pridobi vrstice s cenami vlog, ki imajo ujemajoče se vrednosti za polje **Vloga**, vendar ničelne vrednosti za polje **Enota vira**. Ko ima sistem ujemajoč zapis o ceni vlog, se mera stroškov iz tega zapisa uporabi kot privzeta mera stroškov.

> [!NOTE]
> Če ste konfigurirali drugo določanje prednosti polj **Vloga** in **Enota vira**, ali če imate druge dimenzije z večjo prioriteto, se bo prejšnje vedenje ustrezno spremenilo. Sistem pridobi zapise o cenah vlog z vrednostmi, ki se ujemajo z vsako vrednostjo razsežnosti cen po prednostnem vrstnem redu. Vrstice z ničelnimi vrednostmi za te razsežnosti so zadnje.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Določanje mer stroškov vrstic dejanskih podatkov ali vrstic ocen za strošek

Kontekst ocenjevanja za **Stroški** se nanaša na:

- Podrobnosti vrstice ponudb za **Stroški**.
- Podrobnosti vrstice pogodb za **Stroški**.
- Ocene stroškov projekta.

Dejanski kontekst za **Stroški** se nanaša na:

- Vrstice dnevnika vnosa in popravkov za **Stroški**.
- Vrstice dnevnika, ki se ustvarijo, ko je poslan vnos stroška.

Ko je cenik z lastnimi cenami določen, sistem izvede naslednje korake za vnos privzete mere stroškov.

1. Sistem se ujema s kombinacijo polj **Kategorija** in **Enota** v oceni ali dejanskem kontekstu za **Stroški** proti vrsticam s cenami kategorij v ceniku.
1. Če sistem poišče vrstico s cenami kategorij, ki ima mero stroškov za kombinacijo polj **Kategorija** in **Enota**, potem je ta mera stroškov uporabljena kot privzeta mera stroškov.
1. Če se sistem ne more ujemati z vrednostma **Kategorija** in **Enota**, je cena privzeto nastavljena na **0** (nič).
1. Če sistem v kontekstu ocenjevanja najde ujemajočo se vrstico cene kategorije, vendar metoda določanja cen ni **Cena na enoto**, se mera stroškov privzeto nastavi na **0** (nič).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Določanje mer stroškov na dejanskih vrsticah in vrsticah ocen za material

Kontekst ocenjevanja za **Material** se nanaša na:

- Podrobnosti vrstice ponudb za **Material**.
- Podrobnosti vrstice pogodb za **Material**.
- Ocene materiala za projekt.

Dejanski kontekst za **Material** se nanaša na:

- Vrstice dnevnika vnosa in popravkov za **Material**.
- Vrstice dnevnika, ki se ustvarijo, ko je poslan dnevnik uporabe materiala.

Ko je cenik z lastnimi cenami določen, sistem izvede naslednje korake za vnos privzete mere stroškov.

1. Sistem uporablja kombinacijo polj **Izdelek** in **Enota** v kontekstu ocenjevanja ali dejanskem kontekstu za **Material** proti vrsticam elementa cenika v ceniku.
1. Če sistem poišče vrstico elementa cenika, ki ima mero stroškov za kombinacijo polj **Izdelek** in **Enota**, potem je ta mera stroškov uporabljena kot privzeta mera stroškov.
1. Če se sistem ne more ujemati z vrednostma **Izdelek** in **Enota**, je cena na enoto privzeto nastavljena na **0** (nič).
1. Če sistem v kontekstu ocenjevanja ali dejanskem kontekstu najde ujemajočo se vrstico elementa cenika, vendar metoda določanja cen ni **Valutni znesek**, se cena na enoto privzeto nastavi na **0**. Do tega pride, ker aplikacija Project Operations podpira samo način oblikovanja cen **Valutni znesek** za materiale, ki se uporabljajo pri projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
