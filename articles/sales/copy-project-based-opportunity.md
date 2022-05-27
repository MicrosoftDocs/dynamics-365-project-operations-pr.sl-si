---
title: Kopiranje priložnosti, ki temeljijo na projektu
description: Ta tema vsebuje informacije o kopiranju priložnosti, ki temeljijo na projektih, v aplikaciji Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ca48125d90ee50c5621780be19bd4ceb2130d2d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577808"
---
# <a name="copy-project-based-opportunities"></a>Kopiranje priložnosti, ki temeljijo na projektu

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


Priložnosti za projekte lahko enostavno kopirate in tako ustvarite nove priložnosti za projekte. 

1. Na strani s seznamom **Priložnosti za projekte** s seznama izberite priložnost. Ali pa odprite stran s podrobnostmi o posamezni priložnosti. 
2. Na eni strani izberite možnost **Kopiraj**. Odpre se pogovorno okno, ki vsebuje naslednje podatke o polju. Postopek kopiranja se lahko spremeni glede na izbiro vrednosti v pogovornem oknu.

    | **Polje** | **Opis** | **Nadaljnji vpliv** |
    | --- | --- | --- |
    | Tema | Vnesite relevantno temo ciljne priložnosti. Ko se pogovorno okno odpre, ga sistem nastavi na temo izvorne priložnosti, pri čemer je dodana končnica **-copy**. | To polje nima nadaljnjega vpliva. |
    | Račun | Sklic na zapis strankinega podjetja ali kupca Ko se pogovorno okno odpre, ga sistem nastavi na kupca iz izvorne priložnosti. | Vrednost polja je primarna stranka v priložnosti. |
    | Pogodbena enota | Organizacijska enota, ki je odgovorna za izvedbo projektov, povezanih s tem poslom Ko se pogovorno okno odpre, ga sistem nastavi na pogodbeno enoto iz izvorne priložnosti. | Pogodbena enota je oddelek podjetja, ki bo izvajal projekte po zaključku posla. Vsaka pogodbena enota ima valuto in ta valuta se uporablja za poročanje o ocenjenih in dejanskih stroških, nastalih med projektom. |
    | Valuta | Valuta, v kateri poteka transakcija posla. Ko se odpre pogovorno okno, ga bo sistem nastavil na valuto iz izvorne priložnosti. | Valuta se uporablja za privzeto ustvarjanje cenika in oblikovanje finančnih ocen v ponudbi. Nato se valuta uporablja še za izdajo računa kupcu, ko je posel pridobljen. |
    | Kopiranje cen | Vrednost Da/ Ne, ki označuje, ali je treba cene za priložnost kopirati iz izvorne priložnosti. | Če je izbrana možnost **Da**, se ceniki kopirajo iz izvorne v ciljno priložnost. Če je izbrana možnost **Ne**, se privzeto znova nastavijo ceniki na podlagi najnovejših cenikov, ki so bili nastavljeni. |

3. Izberite **V redu**. Sistem na podlagi izbranih parametrov ustvari kopijo projektne priložnosti in odpre se nova priložnost za projekt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]