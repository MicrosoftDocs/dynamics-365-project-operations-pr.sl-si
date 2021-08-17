---
title: Finančne ocene za materiale v projektih
description: Ta tema vsebuje informacije o določanju ali ocenjevanju materialov, ki temeljijo na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1717abb8f37acb7ab5f4e24b9323b3d958b40b13d7da44c0bbfa88eea28b99ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992631"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Finančne ocene za materiale v projektih

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dynamics 365 Project Operations omogoča projektnim vodjem, da za vsak projekt ali opravilo določijo stroške materiala, ki temelji na projektu. Vsaka ocena materiala je lahko povezana z določenim projektnim opravilom. Stroški so razvrščeni v različne kategorije stroškov, ki so opredeljene na organizacijski ravni. V ceniku je opredeljeno določanje cen in izračun stroškov za vsako kategorijo stroškov. 

Dokončajte naslednje korake za ogled, dodajanje ali brisanje ocene projektnega materiala.

1. Pojdite v možnost **Projekti** in izberite projekt, ki ga želite posodobiti.
2. V zavihku **Ocene materiala** si oglejte seznam ocen projektnega gradiva.
3. Če želite ustvariti novo oceno materiala, izberite možnost **Nova ocena materiala**. Ali pa izberite oceno gradiva, ki jo želite izbrisati, in nato izberite možnost **Izbriši oceno materiala**.

Naslednja tabela vsebuje informacije o poljih za projekt na strani **Vrstica ocene materiala**. 

| **Polje** | **Opis** | **Nadaljnji vpliv** |
| --- | --- | --- |
| Opravilo | Seznam vseh opravil v projektu. To vključuje opravila povzetka in listnega vozlišča. | Ko izberete opravilo za vrstico ocene materiala, to vpliva na ocenjeno ceno materiala in ocenjeno prodajo materiala za nalogo. Če je to polje prazno, se ocena stroškov spremlja in povzema samo na ravni projekta. |
| Izbira izdelka |  Določite lahko, ali naj bo vrstica ocene predvidena za obstoječ izdelek (iz kataloga) ali izdelek, ki ni v katalogu. | To polje določa, ali izberete izdelek iz kataloga ali izdelek, ki ni v katalogu. |
| Izdelku | ID izdelka iz kataloga izdelkov. Ko izberete ID izdelka, se vrednost polja **Izbira izdelka** samodejno posodobi na **Obstoječi izdelek**. ID se uporablja za iskanje cen stroškov in prodaje iz cenika. | To polje nima nadaljnjega vpliva. |
| Opis izdelka, ki ni v katalogu | Besedilno polje za zapis imena izdelka. To polje naj se uporabi le, če je izbran **izdelek, ki ni v katalogu** v polju **Izberite izdelek**.| To polje nima nadaljnjega vpliva. |
| Datum začetka | Predviden datum, ko naj bi se material uporabil. | To polje nima nadaljnjega vpliva. |
| Skupina enot | Privzeta vrednost v tem polju prihaja iz privzete skupine enot za katalog izdelkov. Če želite izbrati drugo skupino enot, lahko to polje posodobite. | To polje nima nadaljnjega vpliva. |
| Enota | Vrednost v tem polju je privzeta enota izbranega izdelka. Če želite izbrati drugo enoto, lahko to polje posodobite. | Sprememba enote povzroči drugačno privzeto ceno in stroške enote. |
| Količina | Ocenjena količina izdelka, ki bo uporabljen za projekt. | To polje nima nadaljnjega vpliva. |
| Strošek na enoto | Cena na enoto za izbrani izdelek in kombinacijo enot, kot je določena v veljavnem ceniku z lastnimi cenami. | Cena na enoto je vedno prikazana v valuti cene projekta. Če v ceniku niso nastavljene cene na enoto za kombinacijo izdelka in enote, bodo stroški na enoto privzeto 0,00. |
| Cena enote | Cena za izbrani izdelek in kombinacijo enot, kot je določena v veljavnem prodajnem ceniku. | Cena na enoto je vedno prikazana v valuti prodaje projekta. Če v ceniku niso nastavljene cene za kombinacijo izdelka in enote, bo cene na enoto privzeto 0,00.|
| Skupna cena | Cena, ki se izračuna kot količina \* cena na enoto.| Cena je vedno prikazana v valuti cene projekta. |
| Skupna prodaja | Znesek prodaje, ki se izračuna kot količina \* cena na enoto. | Znesek prodaje je vedno prikazan v valuti prodaje projekta. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
