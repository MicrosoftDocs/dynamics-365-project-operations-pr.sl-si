---
title: Določitev prodajnih cen za ocene in dejanske vrednosti projektov
description: Ta članek vsebuje informacije o tem, kako se določijo prodajne cene za ocene in dejanske vrednosti projekta.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475205"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Določitev prodajnih cen za ocene in dejanske vrednosti projektov

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Za določitev prodajnih cen na podlagi ocen in dejanskih vrednosti v Microsoftu Dynamics 365 Project Operations, sistem najprej uporabi datum in valuto v dohodnem predračunu ali dejanskem kontekstu za določitev prodajnega cenika. Konkretno v dejanskem kontekstu sistem uporablja **Datum transakcije** polje za določitev, kateri cenik velja. The **Datum transakcije** vrednost vhodne ocene ali dejanske primerja z **Učinkovit začetek (neodvisno od časovnega pasu)** in **Dejanski konec (neodvisno od časovnega pasu)** vrednosti na ceniku. Po določitvi prodajnega cenika sistem določi prodajni oziroma obračunski tečaj.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Določanje prodajnih stopenj na dejanskih in ocenjenih vrsticah za Čas

Ocenite kontekst za **Čas** se nanaša na:

- Navedite podrobnosti vrstice za **Čas**.
- Podrobnosti pogodbene linije za **Čas**.
- Dodeljevanje virov na projektu.

Dejanski kontekst za **Čas** se nanaša na:

- Vrstice dnevnika vnosa in popravkov za **Čas**.
- Vrstice dnevnika, ki se ustvarijo, ko je oddan vnos časa.
- Podrobnosti vrstice računa za **Čas**. 

Ko je cenik za prodajo določen, sistem dokonča naslednje korake za vnos privzete obračunske stopnje.

1. Sistem se ujema s kombinacijo **Vloga** in **Enota za vire** polja v oceni ali dejanskem kontekstu za **Čas** glede na cene vlog na ceniku. To ujemanje predpostavlja, da za cene računov uporabljate vnaprej pripravljene dimenzije cen. Če ste konfigurirali cene tako, da temeljijo na poljih, ki niso ali poleg **Vloga** in **Enota za vire**, se ta kombinacija polj uporablja za pridobitev ujemajoče se linije cene vloge.
1. Če sistem najde linijo cen vloge, ki ima obračunsko stopnjo za **Vloga** in **Enota za vire** kombinacija, se ta obračunska stopnja uporablja kot privzeta obračunska stopnja.
1. Če se sistem ne more ujemati z **Vloga** in **Enota za vire** vrednosti, pridobi vrstice cen vlog, ki imajo ujemajoče se vrednosti za **Vloga** vendar ničelne vrednosti za **Enota virov** polje. Ko sistem najde ujemajoč se zapis cene vloge, bo stopnja računa iz tega zapisa uporabljena kot privzeta stopnja računa. To ujemanje predpostavlja vnaprej pripravljeno konfiguracijo za relativno prednost **Vloga** proti **Enota za vire** kot dimenzija prodajnih cen.

> [!NOTE]
> Če konfigurirate drugačno prednostno razvrščanje **Vloga** in **Enota za vire** polja ali če imate druge dimenzije z višjo prednostjo, se bo prejšnje vedenje ustrezno spremenilo. Sistem pridobi zapise cen vlog, ki imajo vrednosti, ki se ujemajo z vsako vrednostjo dimenzije cen po prednostnem vrstnem redu. Vrstice z ničelnimi vrednostmi za te dimenzije so zadnje.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Določanje stopenj prodaje v dejanskih in ocenjenih vrsticah za stroške

Ocenite kontekst za **Stroški** se nanaša na:

- Navedite podrobnosti vrstice za **Stroški**.
- Podrobnosti pogodbene linije za **Stroški**.
- Vrstice ocene stroškov za projekt.

Dejanski kontekst za **Stroški** se nanaša na:

- Vrstice dnevnika vnosa in popravkov za **Stroški**.
- Vrstice dnevnika, ki se ustvarijo, ko je oddan vnos stroškov.
- Podrobnosti vrstice računa za **Stroški**. 

Ko je cenik za prodajo določen, sistem dokonča naslednje korake za vnos privzete prodajne cene na enoto.

1. Sistem se ujema s kombinacijo **Kategorija** in **Enota** polja na vrstici ocene za **Stroški** glede na cenovne vrstice kategorije na ceniku.
1. Če sistem najde cenovno linijo kategorije, ki ima prodajno stopnjo za **Kategorija** in **Enota** kombinacija, se ta stopnja prodaje uporablja kot privzeta stopnja prodaje.
1. Če sistem najde ujemajočo se cenovno vrstico kategorije, se lahko za vnos privzete prodajne cene uporabi metoda oblikovanja cen. Naslednja tabela prikazuje privzeto vedenje za cene stroškov v Project Operations.

    | Kontekst | Način oblikovanja cen | Privzeta cena |
    | --- | --- | --- |
    | Oceni | Cena na enoto | Na podlagi cenovne linije kategorije. |
    |        | Nabavna cena | 0.00 |
    |        | Pribitek na ceno | 0.00 |
    | Dejansko | Cena na enoto | Na podlagi cenovne linije kategorije. |
    |        | Nabavna cena | Na podlagi povezanih dejanskih stroškov. |
    |        | Pribitek na ceno | Pribitek se uporabi, kot je določeno s cenovno linijo kategorije, na stopnjo stroškov na enoto povezanih dejanskih stroškov. |

1. Če se sistem ne more ujemati z **Kategorija** in **Enota** vrednosti, stopnja prodaje je nastavljena na **0** (nič) privzeto.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Določanje prodajnih količin na dejanskih in ocenjenih postavkah za Material

Ocenite kontekst za **Material** se nanaša na:

- Navedite podrobnosti vrstice za **Material**.
- Podrobnosti pogodbene linije za **Material**.
- Stroški ocene materiala na projektu.

Dejanski kontekst za **Material** se nanaša na:

- Vrstice dnevnika vnosa in popravljanja za **Material**.
- Vrstice dnevnika, ki se ustvarijo, ko je predložen dnevnik porabe materiala.
- Podrobnosti vrstice računa za **Material**. 

Ko je cenik za prodajo določen, sistem dokonča naslednje korake za vnos privzete prodajne cene na enoto.

1. Sistem se ujema s kombinacijo **Izdelek** in **Enota** polja na vrstici ocene za **Material** proti vrsticam postavk cenika na ceniku.
1. Če sistem najde vrstico postavke cenika, ki ima prodajno stopnjo za **Izdelek** in **Enota** kombinacija, in če je metoda oblikovanja cen **Znesek valute**, se uporabi prodajna cena, ki je navedena v vrstici cenika. 
1. Če je **Izdelek** in **Enota** vrednosti polj se ne ujemajo ali če je metoda oblikovanja cen nekaj drugega kot **Znesek valute**, stopnja prodaje je nastavljena na **0** (nič) privzeto. Do tega vedenja pride, ker Project Operations podpira samo **Znesek valute** metoda oblikovanja cen za materiale, ki se uporabljajo pri projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
