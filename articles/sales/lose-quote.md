---
title: Kopiranje ponudb, ki temeljijo na projektih
description: Ta tema vsebuje informacije o kopiranju ponudb, ki temeljijo na projektih, v storitvi Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 247f9d33bc2e7b0bcbeae8114bb436ed237efce660d0840e58d536d2a290639e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992181"
---
# <a name="copy-project-based-quotes"></a>Kopiranje ponudb, ki temeljijo na projektih

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Novo ponudbo za projekt lahko brez težav ustvarite s kopiranjem obstoječe. 

- Če želite kopirati ponudbo za projekt, na strani s seznamom **Ponudbe za projekte** ali strani s podrobnostmi **Ponudba za projekt** izberite ponudbo za projekt, ki jo želite kopirati, in nato izberite **Kopiraj**.

Odprla se bo stran s pogovornim oknom, kjer lahko vnesete parametre kopije. V spodnji tabeli so navedena polja, ki so vključena na stran s pogovornim oknom. Odvisno od izbranih vrednosti se lahko postopek kopiranja spremeni.

| **Polje** | **Opis** | **Nadaljnji vpliv** |
| --- | --- | --- |
| Tema | Vnesite ustrezno temo ali ime ciljne ponudbe. Ko se pogovorno okno odpre, ga sistem nastavi na temo izvorne ponudbe, pri čemer je dodana končnica **-copy**. | |
| Možna stranka | Sklic na zapis strankinega podjetja ali kupca. Ko se odpre pogovorno okno, ga bo sistem nastavil na račun pri izvorni ponudbi. | To polje je primarna stranka pri ponudbi. |
| Pogodbena enota | Organizacijska enota, ki je odgovorna za izvedbo projektov, povezanih s tem poslom.
Ko se odpre pogovorno okno, ga bo sistem nastavil na pogodbeno enoto pri izvorni ponudbi. | Pogodbena enota je oddelek podjetja, ki bo izvajal projekte po zaključku posla. Vsaka pogodbena enota ima valuto. Valuta se uporablja za poročanje o ocenjenih in dejanskih stroških, ki so nastali med izvajanjem projekta. |
| Valuta | To je valuta, v kateri poteka transakcija posla. Ko se odpre pogovorno okno, ga bo sistem nastavil na valuto pri izvorni ponudbi. To je mogoče spremeniti, in če pride do spremembe, je polje **Kopiranje cen** vedno nastavljeno na **Ne**. To je zato, ker ceniki pri izvorni ponudbi niso več ustrezni. | Valuta se uporablja za nastavitev privzetih vrednosti cenika, za izdelavo finančne ocene pri ponudbi in v končni fazi tudi za izdajanje računov stranki, ko je pridobljen posel. |
| Zahtevani datum dostave | To je datum dostave, ki ga zahteva stranka. | Ta se uporablja kot končni datum pri ustvarjanju datumov izdajanja računov, ob upoštevanju izbrane pogostosti. |
| Kopiranje cen | Vrednost Da/Ne označuje, ali je treba cene pri ponudbi kopirati iz izvorne ponudbe. | Če je izbrana možnost **Da**, se sklici na cenik projekta in cenik izdelkov kopirajo iz izvorne ponudbe v ciljno ponudbo. Če je izbrana možnost **Ne**, se privzeto znova nastavijo ceniki na podlagi najnovejših cenikov, ki so bili nastavljeni pri parametrih računa ali projekta. |

Ko izberete **V redu** na strani s pogovornim oknom, sistem ustvari kopijo ponudbe projekta na podlagi parametrov, izbranih v pogovornem oknu. Odpre se nova ponudba za projekt. 

> [!NOTE]
> Naslednji podatki se ne kopirajo iz izvorne v ciljno ponudbo:
>
> - Razporedi izdajanja računov
> - Ponudba in stranke v podrobnostih ponudbe
> - Sklic na projekt pri podrobnostih ponudb, ki temeljijo na izdelkih – podatki o proračunu stranke
>
>Ker so ti podatki zelo specifični za vsako ponudbo, se ta polja in zapisi ne kopirajo. Kopirajo se podrobnosti ponudb za projekte in izdelke, ocene pri podrobnostih ponudbe in vrednosti, ki jih ni dovoljeno preseči na ravni ponudbe. Privzete vrednosti cen in mer stroškov so odvisne od možnosti **Kopiranje cen**, ki se jo izbere na strani s pogovornim oknom **Kopiraj parametre**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]