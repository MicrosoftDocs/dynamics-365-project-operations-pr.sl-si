---
title: Določite stopnje stroškov za ocene projekta in dejanske vrednosti
description: Ta članek vsebuje informacije o tem, kako se določijo stopnje stroškov za ocene in dejanske vrednosti projekta.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410179"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Določite stopnje stroškov za ocene projekta in dejanske vrednosti

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Za določitev cenika stroškov in stroškovnih stopenj v predračunskem in dejanskem kontekstu sistem uporablja informacije v **Datum**, **·**, in **Pogodbena enota** področja povezanega projekta.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Določanje stroškovnih stopenj v predračunskem in dejanskem kontekstu za čas

Ocenite kontekst za **Čas** se nanaša na:

- Navedite podrobnosti vrstice za **Čas**.
- Podrobnosti pogodbene linije za **Čas**.
- Dodeljevanje virov na projektu.

Dejanski kontekst za **Čas** se nanaša na:

- Vrstice dnevnika vnosa in popravkov za **Čas**.
- Vrstice dnevnika, ki se ustvarijo, ko je oddan vnos časa.

Ko je določen cenik stroškov, sistem izvede naslednje korake za vnos privzete stopnje stroškov.

1. Sistem se ujema s kombinacijo **Vloga** in **Enota za vire** polja v oceni ali dejanskem kontekstu za **Čas** glede na cene vlog na ceniku. To ujemanje predpostavlja, da uporabljate standardne dimenzije cen za stroške dela. Če ste konfigurirali sistem za ujemanje s polji, ki niso ali poleg **Vloga** in **Enota za vire**, se za pridobitev ujemajoče se vrstice cene vloge uporabi drugačna kombinacija.
1. Če sistem najde vrstico cen vlog, ki ima stopnjo stroškov za **Vloga** in **Enota za vire** kombinaciji, se ta stopnja stroškov uporablja kot privzeta stopnja stroškov.
1. Če se sistem ne more ujemati z **Vloga** in **Enota za vire** vrednosti, pridobi vrstice cen vlog, ki imajo ujemajoče se vrednosti za **Vloga** vendar ničelne vrednosti za **Enota za vire** polje. Ko ima sistem ujemajoč se zapis cene vloge, bo stopnja stroškov iz tega zapisa uporabljena kot privzeta stopnja stroškov.

> [!NOTE]
> Če konfigurirate drugačno prednostno nalogo **Vloga** in **Enota za vire** polja ali če imate druge dimenzije z višjo prednostjo, se bo prejšnje vedenje ustrezno spremenilo. Sistem pridobi zapise cen vlog, ki imajo vrednosti, ki se ujemajo z vsako vrednostjo dimenzije cen po prednostnem vrstnem redu. Vrstice z ničelnimi vrednostmi za te dimenzije so zadnje.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Določanje stopenj stroškov v dejanskih in ocenjenih vrsticah za stroške

Ocenite kontekst za **Stroški** se nanaša na:

- Navedite podrobnosti vrstice za **Stroški**.
- Podrobnosti pogodbene linije za **Stroški**.
- Ocena stroškov za projekt.

Dejanski kontekst za **Stroški** se nanaša na:

- Vrstice dnevnika vnosa in popravkov za **Stroški**.
- Vrstice dnevnika, ki se ustvarijo, ko je oddan vnos stroškov.

Ko je določen cenik stroškov, sistem izvede naslednje korake za vnos privzete stopnje stroškov.

1. Sistem se ujema s kombinacijo **Kategorija** in **Enota** polja v oceni ali dejanskem kontekstu za **Stroški** glede na cenovne vrstice kategorije na ceniku.
1. Če sistem najde cenovno vrstico kategorije, ki ima stopnjo stroškov za **Kategorija** in **Enota** kombinaciji, se ta stopnja stroškov uporablja kot privzeta stopnja stroškov.
1. Če se sistem ne more ujemati z **Kategorija** in **Enota** vrednosti, cena je nastavljena na **0** (nič) privzeto.
1. V kontekstu ocenjevanja, če lahko sistem najde ujemajočo se cenovno linijo kategorije, vendar je metoda oblikovanja cen nekaj drugega kot **Cena na enoto**, je stopnja stroškov nastavljena na **0** (nič) privzeto.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Določanje stroškovnih stopenj na dejanskih in predračunskih postavkah za Material

Ocenite kontekst za **Material** se nanaša na:

- Navedite podrobnosti vrstice za **Material**.
- Podrobnosti pogodbene linije za **Material**.
- Ocene materiala na projektu.

Dejanski kontekst za **Material** se nanaša na:

- Vrstice dnevnika vnosa in popravkov za **Material**.
- Vrstice dnevnika, ki se ustvarijo, ko je predložen dnevnik porabe materiala.

Ko je določen cenik stroškov, sistem izvede naslednje korake za vnos privzete stopnje stroškov.

1. Sistem uporablja kombinacijo **Izdelek** in **Enota** polja v oceni ali dejanskem kontekstu za **Material** proti vrsticam postavk cenika na ceniku.
1. Če sistem najde vrstico postavke cenika, ki ima stopnjo stroškov za **Izdelek** in **Enota** kombinaciji, se ta stopnja stroškov uporablja kot privzeta stopnja stroškov.
1. Če se sistem ne more ujemati z **Izdelek** in **Enota** vrednosti, je cena enote nastavljena na **0** (nič) privzeto.
1. V okviru ocene ali dejanskega konteksta, če lahko sistem najde ujemajočo se vrstico postavke cenika, vendar je metoda oblikovanja cen nekaj drugega kot **Znesek valute**, je cena enote nastavljena na **0** privzeto. Do tega vedenja pride, ker Project Operations podpira samo **Znesek valute** metoda oblikovanja cen za materiale, ki se uporabljajo pri projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
