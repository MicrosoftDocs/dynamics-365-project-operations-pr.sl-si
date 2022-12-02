---
title: Kopiranje pogodb, ki temeljijo na projektih
description: Ta članek vsebuje informacije o kopiranju projektnih pogodb v programu Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410388"
---
# <a name="copy-project-based-contracts"></a>Kopiranje pogodb, ki temeljijo na projektih

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Nove projektne pogodbe lahko enostavno ustvarite tako, da na enega od teh dveh načinov kopirate obstoječe pogodbe:

- Na strani s seznamom **Projektne pogodbe** izberite projektno pogodbo in nato izberite možnost **Kopiraj**.
- Na strani s podrobnostmi **Projektne pogodbe** izberite možnost **Kopiraj**.

V obeh primerih se odpre pogovorno okno, kjer lahko nastavite parametre kopirane pogodbe. Pogovorno okno vključuje naslednja polja. Odvisno od izbranih vrednosti se lahko postopek kopiranja spremeni.

| Polje | Description | Nadaljnji vpliv |
| --- | --- | --- |
| Tema | Vnesite temo ciljne pogodbe. Ko se pogovorno okno odpre, sistem to polje nastavi na ime izvorne pogodbe z dodano besedo »kopija«. | To polje nima nadaljnjega vpliva. |
| stranka | Sklic na zapis strankinega podjetja ali kupca. Ko se odpre pogovorno okno, sistem to polje nastavi na kupca iz izvorne ponudbe. | Vrednost polja je primarna stranka v pogodbi. |
| Lastniško podjetje | Podjetje, ki je odgovorno za izvedbo projektov, povezanih s tem poslom. Ko se odpre pogovorno okno, sistem to polje nastavi na lastniško podjetje iz izvorne ponudbe. | Lastniško podjetje je pravna oseba, ki bo po sklenitvi posla izvajala projekt. Valuta lastniškega podjetja se mora ujemati z valuto pogodbene enote. |
| Pogodbena enota | Organizacijska enota, ki je odgovorna za izvedbo projektov, povezanih s tem poslom. Ko se odpre pogovorno okno, sistem to polje nastavi na pogodbeno enoto iz izvorne ponudbe. | Pogodbena enota je oddelek podjetja, ki bo izvajal projekte po zaključku posla. Vsaka pogodbena enota ima valuto. Valuta se uporablja za poročanje o ocenjenih in dejanskih stroških, ki so nastali med izvajanjem projekta. |
| Valuta | Valuta, v kateri poteka transakcija posla. Ko se odpre pogovorno okno, sistem nastavi polje na valuto iz izvorne pogodbe. Valuto je mogoče spremeniti. Če jo spremenite, je polje **Kopiranje cen** vedno nastavljeno na možnost **Ne**, saj ceniki iz izvorne pogodbi niso več ustrezni. | Ta valuta se uporablja za privzeti cenik pri izdelavi finančnih ocen v pogodbi in za izdajanje računov stranki, ko je pridobljen posel. |
| Zahtevani datum dostave | Datum izvedbe, ki ga je zahtevala stranka. | Datum se uporablja kot končni datum pri ustvarjanju datumov izdajanja računov z določeno pogostostjo. |
| Kopiranje cen | Vrednost, ki označuje, ali je treba cene za pogodbo kopirati iz izvorne ponudbe. | Če je v polju izbrana možnost **Da**, se sklici na cenik projekta in cenik izdelkov kopirajo iz izvorne pogodbe v ciljno. Če je nastavljena možnost **Ne**, se uporabijo privzeti ceniki na podlagi najnovejših cenikov, ki so bili nastavljeni kot parametri stranke ali projekta. |

Ko v pogovornem oknu izberete možnost **V redu**, sistem ustvari kopijo pogodbe na podlagi vrednosti parametrov, ki jih nastavite. Nato se odpre nova pogodba.

Naslednje informacije so **ne** kopirajo iz izvorne v ciljno pogodbo, ker so specifične za vsako pogodbo:

- Razporedi izdajanja računov
- Stranke pogodbe in podrobnosti pogodbe
- Sklic projekta v podrobnostih pogodbe, ki temeljijo na projektu
- Podatki o proračunu stranke

Kopirane so podrobnosti pogodb za projekte in izdelke, ocene v podrobnostih pogodbe ter vrednosti, ki jih na ravni pogodbe ni dovoljeno preseči. Vnos privzetih vrednosti cen in mer stroškov je odvisen od izbire v polju **Kopiraj cene** v pogovornem oknu **Kopiraj parametre**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
