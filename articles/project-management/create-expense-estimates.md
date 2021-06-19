---
title: Finančne ocene za stroške v projektih
description: Ta tema vsebuje informacije o določanju ali oceni stroškov za posamezen projekt.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 18d8568fae35fc251d9cf48d900b8a436e2e4500
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014181"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Finančne ocene za stroške v projektih
_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dynamics 365 Project Operations omogoča projektnim vodjem, da za vsak projekt ali opravilo določijo stroške, ki temelji na projektu. Vsak element stroška je lahko povezan z določenim projektnim opravilom. Stroški so razvrščeni v različne kategorije stroškov, ki so opredeljene na organizacijski ravni. V ceniku je opredeljeno določanje cen in izračun stroškov za vsako kategorijo stroškov. 

Za ogled, dodajanje ali brisanje stroškov projekta izvedite naslednje korake.

1. Na obrazcu **Projekti** izberite projekt, na katerem želite delati.
2. Na zavihku **Ocene projekta** si oglejte seznam stroškov projekta.
3. Izberite možnost **Novi stroški**, da dodate strošek. Ali pa izberite strošek, ki ga želite izbrisati, in nato izberite možnost **Izbriši strošek**.

Naslednja tabela vsebuje informacije o poljih za projekt na strani **Vrstica ocene stroškov**. 

| **Polje** | **Opis** | **Nadaljnji vpliv** |
| --- | --- | --- |
| Opravilo | Seznam vseh opravil v projektu. To vključuje opravila povzetka in listnega vozlišča. | Izbira opravila za vrstico ocene stroškov bo vplivala na ocenjene stroške in ocenjene stroške prodaje za opravilo. Če je to polje prazno, se ocena stroškov spremlja in povzema samo na ravni projekta. |
| Kategoriji | Seznam kategorij transakcij, ki so v aplikaciji povezale kategorije stroškov. | Izbira kategorije spodbuja določanje cen in izračun stroškov v vrstici ocene stroškov. |
| Datum začetka | Predviden datum nastanka stroškov. | To polje nima nadaljnjega vpliva. |
| Skupina enot | Privzeta vrednost v tem polju prihaja iz skupine enot, ki je za izbrano kategorijo nastavljena kot privzeta. Če želite izbrati drugo skupino enot, lahko to polje posodobite. | To polje nima nadaljnjega vpliva. |
| Enota | Privzeta vrednost v tem polju je privzeta enota izbrane kategorije. Če želite izbrati drugo enoto, lahko to polje posodobite. | Sprememba enote povzroči drugačno privzeto ceno in stroške enote. |
| Količina | Količina predvidenih stroškov. | To polje nima nadaljnjega vpliva. |
| Strošek na enoto | Cena za izbrano kategorijo in kombinacijo enot, kot je določena v veljavnem ceniku z lastnimi cenami | Cena na enoto je vedno prikazana v valuti cene projekta. |
| Cena enote | Cena za izbrano kategorijo in kombinacijo enot, kot je določena v veljavnem prodajnem ceniku. | Cena na enoto je vedno prikazana v valuti prodaje projekta. |
| Skupna cena | Cena, ki se izračuna kot količina \* cena na enoto.| Cena je vedno prikazana v valuti cene projekta. |
| Skupna prodaja | Znesek prodaje, ki se izračuna kot količina \* cena na enoto. | Znesek prodaje je vedno prikazan v valuti prodaje projekta. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
