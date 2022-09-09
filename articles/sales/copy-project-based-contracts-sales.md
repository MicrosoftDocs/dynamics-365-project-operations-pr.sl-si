---
title: Kopirajte projektne pogodbe
description: Ta članek ponuja informacije o kopiranju projektnih pogodb v Microsoftu Dynamics 365 Project Operations.
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
# <a name="copy-project-based-contracts"></a>Kopirajte projektne pogodbe

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Nove projektne pogodbe lahko preprosto ustvarite tako, da kopirate obstoječe pogodbe na enega od dveh načinov:

- Na **Projektne pogodbe** stran s seznamom, izberite projektno pogodbo in nato izberite **Kopirati**.
- Na strani s podrobnostmi **Projektne pogodbe** izberite možnost **Kopiraj**.

V obeh primerih se pojavi pogovorno okno, kjer lahko nastavite parametre kopirane pogodbe. Pogovorno okno vključuje naslednja polja. Postopek kopiranja se lahko spremeni glede na vrednosti, ki jih izberete.

| Polje | Description | Nadaljnji vpliv |
| --- | --- | --- |
| Tema | Vnesite temo ciljne pogodbe. Ko se odpre pogovorno okno, sistem nastavi polje na ime izvorne pogodbe, vendar mu je dodana beseda "kopija". | To polje nima nadaljnjega vpliva. |
| stranka | Sklic na zapis strankinega podjetja ali kupca. Ko se odpre pogovorno okno, sistem nastavi polje na račun na izvorni pogodbi. | Vrednost polja je primarna stranka v pogodbi. |
| Lastniško podjetje | Podjetje, ki je odgovorno za izvedbo projektov, povezanih s tem poslom. Ko se odpre pogovorno okno, sistem nastavi polje na lastniško podjetje izvorne pogodbe. | Lastniško podjetje je pravna oseba, ki bo po sklenitvi posla izvajala projekt. Valuta lastniškega podjetja se mora ujemati z valuto pogodbene enote. |
| Pogodbena enota | Organizacijska enota, ki je odgovorna za izvedbo projektov, povezanih s tem poslom. Ko se odpre pogovorno okno, sistem nastavi polje na pogodbeno enoto izvorne pogodbe. | Pogodbena enota je oddelek podjetja, ki bo izvajal projekte po zaključku posla. Vsaka pogodbena enota ima valuto. Ta valuta se uporablja za poročanje o ocenjenih in dejanskih stroških, ki nastanejo med projektom. |
| Valuta | Valuta, v kateri poteka transakcija posla. Ko se odpre pogovorno okno, sistem nastavi polje na valuto izvorne pogodbe. Valuto je mogoče spremeniti. Če je, **Cene kopij** polje je vedno nastavljeno na **št**, ker ceniki na izvorni pogodbi niso več aktualni. | Ta valuta se uporablja za privzete cenike, za ustvarjanje finančnih ocen pogodbe in za izdajanje računov stranki, ko je posel dosežen. |
| Zahtevani datum dostave | Datum dostave, ki ga zahteva stranka. | Ta datum se uporablja kot končni datum, ko ustvarjate datume izdajanja računov ob določeni pogostosti. |
| Kopiranje cen | Vrednost, ki označuje, ali je treba cene v pogodbi kopirati iz izvorne pogodbe. | Če je polje nastavljeno na **ja**, reference projektov in cenikov izdelkov se kopirajo iz izvorne pogodbe v ciljno pogodbo. Če je nastavljeno na **št**, se uporabljajo privzeti ceniki, ki temeljijo na zadnjih cenikih v parametrih računa ali projekta. |

Ko izberete **v redu** v pogovornem oknu sistem ustvari kopijo pogodbe na podlagi vrednosti parametrov, ki ste jih nastavili. Nato se odpre nova pogodba.

Naslednje informacije so **ne** kopirati iz izvorne pogodbe v ciljno pogodbo, ker je specifična za vsako pogodbo:

- Razporedi izdajanja računov
- Stranke pogodbe in podrobnosti pogodbe
- Sklic projekta v podrobnostih pogodbe, ki temeljijo na projektu
- Podatki o proračunu stranke

Kopirajo se pogodbene vrstice za projekte in izdelke, ocene v podrobnostih pogodbene vrstice in vrednosti, ki jih ni treba preseči na ravni pogodbe. Vnos privzetih cen in stroškovnikov je odvisen od izbire v **Cene kopij** polje v **Kopiraj parametre** pogovorno okno.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
