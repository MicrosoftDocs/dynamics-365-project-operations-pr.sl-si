---
title: Kopiranje projektnih pogodb
description: Ta tema vsebuje informacije o kopiranju projektnih pogodb v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6da8e3ba8e062f3e06dc7f440caebdd93e496c65
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084661"
---
# <a name="copying-project-contracts"></a>Kopiranje projektnih pogodb

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Nove projektne pogodbe lahko enostavno ustvarite tako, da na enega od teh dveh načinov kopirate obstoječe pogodbe: 

  - Na strani s seznamom **Projektne pogodbe** izberite projektno pogodbo in nato izberite možnost **Kopiraj**.
  - Na strani s podrobnostmi **Projektne pogodbe** izberite možnost **Kopiraj**.

Odprla se bo stran s pogovornim oknom, kjer lahko izberete parametre kopirane pogodbe. Naslednja polja so del pogovornega okna. Postopek kopiranja se lahko spremeni glede na izbiro vrednosti v pogovornem oknu.

| **Polje** | **Ustreznost, namen in smernice** | **Nadaljnji vpliv** |
| --- | --- | --- |
| Tema | Vnesite temo ciljne pogodbe. Ko se pogovorno okno odpre, sistemu to polje nastavi na ime izvorne pogodbe z dodano končnico **-kopija**. | To polje nima nadaljnjega vpliva. |
| Stranki | Sklic na zapis strankinega podjetja ali kupca. Ko se odpre pogovorno okno, sistem to polje nastavi na kupca iz izvorne ponudbe. | Vrednost polja je primarna stranka v pogodbi. |
| Pogodbena enota | Organizacijska enota, ki je odgovorna za izvedbo projektov, povezanih s tem poslom. Ko se odpre pogovorno okno, ga sistem nastavi na pogodbeno enoto v izvorni pogodbi. | Pogodbena enota je oddelek podjetja, ki bo izvajal projekte po zaključku posla. Vsaka pogodbena enota ima valuto. Valuta se uporablja za poročanje o ocenjenih in dejanskih stroških, ki so nastali med izvajanjem projekta. |
| Valuta | Valuta, v kateri poteka transakcija posla. Ko se odpre pogovorno okno, sistem nastavi polje na valuto iz izvorne pogodbe. Valuto je mogoče spremeniti. Če jo spremenite, je polje **Kopiranje cen** vedno nastavljeno na možnost **Ne**, saj ceniki iz izvorne pogodbi niso več ustrezni. | Valuta se uporablja za privzeti cenik pri izdelavi finančnih ocen v pogodbi in za izdajanje računov stranki, ko je pridobljen posel. |
| Zahtevani datum dostave | Datum izvedbe, ki ga je zahtevala stranka | Datum se uporablja kot končni datum pri ustvarjanju datumov izdajanja računov ob upoštevanju posamezne pogostosti. |
| Kopiranje cen | Označuje, ali je treba cene za pogodbo kopirati iz izvorne ponudbe. | Če je v polju izbrana možnost **Da**, se sklici na cenik projekta in cenik izdelkov kopirajo iz izvorne pogodbe v ciljno. Če je izbrana možnost **Ne**, se privzeto nastavijo ceniki na podlagi najnovejših cenikov, ki so bili nastavljeni kot parametri stranke ali projekta. |

Ko na strani s pogovornim oknom izberete možnost **V redu**, sistem ustvari kopijo pogodbe na podlagi izbranih parametrov. Odpre se nova pogodba.

Naslednji podatki se ne kopirajo iz **Izvorne** v **Ciljno pogodbo**:

  - Razporedi izdajanja računov
  - Stranke pogodbe in podrobnosti pogodbe
  - Sklic projekta v podrobnostih pogodbe, ki temeljijo na projektu
  - Podatki o proračunu stranke

Ker so ti podatki specifični za vsako pogodbo, se ta polja in zapisi ne kopirajo. Kopirane so podrobnosti pogodb za projekte in izdelke, ocene v podrobnostih pogodbe ter vrednosti, ki jih na ravni pogodbe ni dovoljeno preseči. Privzete vrednosti cen in mer stroškov so odvisne od izbire v polju **Kopiraj cene** na strani s pogovornim oknom **Kopiraj parametre**.
