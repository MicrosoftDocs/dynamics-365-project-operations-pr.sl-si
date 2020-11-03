---
title: Kopiranje priložnosti, ki temeljijo na projektu
description: Ta tema vsebuje informacije o kopiranju priložnosti, ki temeljijo na projektih, v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084695"
---
# <a name="copy-project-based-opportunities"></a>Kopiranje priložnosti, ki temeljijo na projektu

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_


Priložnosti za projekte lahko enostavno kopirate in tako ustvarite nove priložnosti za projekte. 

1. Na strani s seznamom **Priložnosti za projekte** s seznama izberite priložnost. Ali pa odprite stran s podrobnostmi o posamezni priložnosti. 
2. Na eni strani izberite možnost **Kopiraj**. Odpre se pogovorno okno, ki vsebuje naslednje podatke o polju. Postopek kopiranja se lahko spremeni glede na izbiro vrednosti v pogovornem oknu.

    | **Polje** | **Ustreznost, namen in smernice** | **Nadaljnji vpliv** |
    | --- | --- | --- |
    | Tema | Vnesite relevantno temo ciljne priložnosti. Ko se pogovorno okno odpre, ga sistem nastavi na temo izvorne priložnosti, pri čemer je dodana končnica **-copy**. | To polje nima nadaljnjega vpliva. |
    | Račun | Sklic na zapis strankinega podjetja ali kupca Ko se pogovorno okno odpre, ga sistem nastavi na kupca iz izvorne priložnosti. | Vrednost polja je primarna stranka v priložnosti. |
    | Pogodbena enota | Organizacijska enota, ki je odgovorna za izvedbo projektov, povezanih s tem poslom Ko se pogovorno okno odpre, ga sistem nastavi na pogodbeno enoto iz izvorne priložnosti. | Pogodbena enota je oddelek podjetja, ki bo izvajal projekte po zaključku posla. Vsaka pogodbena enota ima valuto in ta valuta se uporablja za poročanje o ocenjenih in dejanskih stroških, nastalih med projektom. |
    | Valuta | Valuta, v kateri poteka transakcija posla. Ko se odpre pogovorno okno, ga bo sistem nastavil na valuto iz izvorne priložnosti. | Valuta se uporablja za privzeto ustvarjanje cenika in oblikovanje finančnih ocen v ponudbi. Nato se valuta uporablja še za izdajo računa kupcu, ko je posel pridobljen. |
    | Kopiranje cen | Vrednost Da/ Ne, ki označuje, ali je treba cene za priložnost kopirati iz izvorne priložnosti. | Če je izbrana možnost **Da** , se ceniki kopirajo iz izvorne v ciljno priložnost. Če je izbrana možnost **Ne** , se privzeto znova nastavijo ceniki na podlagi najnovejših cenikov, ki so bili nastavljeni. |

3. Izberite **V redu**. Sistem na podlagi izbranih parametrov ustvari kopijo projektne priložnosti in odpre se nova priložnost za projekt.
