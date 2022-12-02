---
title: Določitev prodajnih cen za ocene in dejanske vrednosti, ki temeljijo na projektu
description: Ta članek vsebuje informacije o tem, kako se določijo prodajne cene v ocenah, ki temeljijo na projektu, in dejanskih vrednostih.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475390"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Določitev prodajnih cen za ocene in dejanske vrednosti, ki temeljijo na projektu

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Za določitev cen prodaje na podlagi ocen in dejanskih vrednosti v programu Microsoft Dynamics 365 Project Operations sistem najprej uporabi datum in valuto v dohodni oceni ali dejanskem kontekstu, da določi prodajni cenik. Konkretno v dejanskem kontekstu sistem uporablja polje **Datum transakcije** za določitev, kateri cenik velja. Vrednost **Datum transakcije** dohodne ocene ali dejanske vrednosti se primerja z vrednostma **Veljavni datum začetka (neodvisno od časovnega pasu)** in **Veljavni datum konca (neodvisno od časovnega pasu)** na ceniku. Po določitvi prodajnega cenika sistem določi prodajni znesek ali delež obračunavanja.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Določitev prodajnih zneskov vrstic dejanskih podatkov za čas ali vrstic ocen za čas

Kontekst ocenjevanja za **Čas** se nanaša na:

- Podrobnosti vrstice ponudb za **Čas**.
- Podrobnosti vrstice pogodb za **Čas**.
- Dodelitev virov v projektu.

Dejanski kontekst za **Čas** se nanaša na:

- Vrstice dnevnika vnosa in popravkov za **Čas**.
- Vrstice dnevnika, ki se ustvarijo, ko je poslan časovni vnos.
- Podrobnosti vrstice računa za **Čas**. 

Ko je prodajni cenik določen, sistem izvede naslednje korake za vnos privzetega deleža obračunavanja.

1. Sistem se ujema s kombinacijo polj **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira** v oceni ali dejanskem kontekstu za **Čas** proti vrsticam s cenami vlog v ceniku. To ujemanje predpostavlja, da se za deleže obračunavanja uporabljajo vnaprej pripravljene cenovne razsežnosti. Če ste cene nastavili na podlagi katerega koli drugega polja namesto polj **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira** ali poleg teh polj, potem je to kombinacija polj, ki bo uporabljena za pridobivanje vrstic s cenami vloge.
1. Če sistem poišče vrstico s cenami vloge, ki ima delež obračunavanja za kombinacijo polj **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira**, potem je ta delež obračunavanja uporabljen kot privzet.

> [!NOTE]
> Če ste konfigurirali drugo določanje prednosti polj **Vloga**, **Podjetje, ki zagotavlja vire** in **Enota vira**, ali če imate druge dimenzije z večjo prioriteto, se bo predhodno vedenje ustrezno spremenilo. Sistem pridobi zapise o cenah vlog z vrednostmi, ki se ujemajo z vsako vrednostjo razsežnosti cen po prednostnem vrstnem redu. Vrstice z ničelnimi vrednostmi za te razsežnosti so zadnje.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Določitev prodajnih zneskov vrstic dejanskih podatkov za stroške ali vrstic ocen za stroške

Kontekst ocenjevanja za **Stroški** se nanaša na:

- Podrobnosti vrstice ponudb za **Stroški**.
- Podrobnosti vrstice pogodb za **Stroški**.
- Vrstice ocene stroškov projekta.

Dejanski kontekst za **Stroški** se nanaša na:

- Vrstice dnevnika vnosa in popravkov za **Stroški**.
- Vrstice dnevnika, ki se ustvarijo, ko je poslan vnos stroška.
- Podrobnosti vrstice računa za **Stroški**. 

Ko je prodajni cenik določen, sistem izvede naslednje korake za vnos privzete prodajne cene enote.

1. Sistem ujema kombinacijo polj **Kategorija** in **Enota**, ki so v vrstici ocene **Stroški**, z vrsticami s cenami kategorij v ceniku.
1. Če sistem poišče vrstico s cenami kategorij, ki ima prodajni znesek za kombinacijo polj **Kategorija** in **Enota**, potem je ta prodajni znesek uporabljen kot privzet.
1. Če sistem najde ujemajočo se vrstico s cenami kategorij, se lahko za vnos privzete prodajne cene uporabi način oblikovanja cen. Naslednja tabela prikazuje privzeto vedenje cene stroškov v aplikaciji Project Operations.

    | Kontekst | Način oblikovanja cen | Privzeta cena |
    | --- | --- | --- |
    | Oceni | Cena na enoto | Na osnovi vrstice s cenami kategorij. |
    |        | Nabavna cena | 0.00 |
    |        | Pribitek na ceno | 0.00 |
    | Dejansko | Cena na enoto | Na osnovi vrstice s cenami kategorij. |
    |        | Nabavna cena | Na osnovi povezanih dejanskih stroškov. |
    |        | Pribitek na ceno | Pribitek se uporabi, kot je določeno z vrstico s cenami kategorij na meri stroškov enote povezanih dejanskih stroškov. |

1. Če se sistem ne more ujemati z vrednostma **Kategorija** in **Enota**, je stopnja prodaje privzeto nastavljena na **0** (nič).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Določitev mer prodaje na dejanskih vrsticah in vrsticah ocen za material

Kontekst ocenjevanja za **Material** se nanaša na:

- Podrobnosti vrstice ponudb za **Material**.
- Podrobnosti vrstice pogodb za **Material**.
- Vrstice ocene materiala za projekt.

Dejanski kontekst za **Material** se nanaša na:

- Vrstice dnevnika vnosa in popravkov za **Material**.
- Vrstice dnevnika, ki se ustvarijo, ko je poslan dnevnik uporabe materiala.
- Podrobnosti vrstice računa za **Material**. 

Ko je prodajni cenik določen, sistem izvede naslednje korake za vnos privzete prodajne cene enote.

1. Sistem ujema kombinacijo polj **Izdelek** in **Enota** na vrstici ocene za **Material** z vrstico elementa cenika.
1. Če sistem najde vrstico elementa cenika, ki ima stopnjo prodaje za kombinacijo polj **Izdelek** in **Enota** in metodo za določanje cen **Valutni znesek**, se uporablja prodajna cena, navedena v vrstici cenika. 
1. Če se vrednosti polj **Izdelek** in **Enota** ne ujemajo ali če je način nastavljanja cen drugo kot **Valutni znesek**, je stopnja prodaje privzeto nastavljena na **0** (nič). Do tega pride, ker aplikacija Project Operations podpira samo način oblikovanja cen **Valutni znesek** za materiale, ki se uporabljajo pri projektu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
