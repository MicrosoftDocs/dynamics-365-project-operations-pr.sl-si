---
title: Kopiranje priložnosti, ki temeljijo na projektu
description: Ta tema vsebuje informacije o kopiranju priložnosti, ki temeljijo na projektih, v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 26ae5cc267bb06f958bbf9cdce2d80ccde9d3d24
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181704"
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