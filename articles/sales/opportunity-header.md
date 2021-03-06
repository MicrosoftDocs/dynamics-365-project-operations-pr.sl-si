---
title: Glava/povzetek priložnosti
description: Ta tema vsebuje informacije o poslih, ki temeljijo na projektih, in podrobnostih priložnosti, ki temeljijo na projektih.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c4e91c1a869347ac1182db2de1ab9244309eb856
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908599"
---
# <a name="opportunity-headersummary"></a>Glava/povzetek priložnosti

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_


Glava ali povzetek »Priložnost« zajema splošne informacije o poslu, ki temelji na projektu in velja za vse podrobnosti pri priložnosti, ki temelji na projektu.

Priložnosti, ki temeljijo na projektu, v storitvi Dynamics 365 Project Operations so razširitve priložnosti v storitvi Dynamics 365 Sales. Te razširitve zagotavljajo dodatne funkcije, ki so specifične in potrebne za priložnosti, ki temeljijo na projektih. Te razširitve lahko vključujejo nova polja in dejanja traku, ki so na voljo pri priložnostih, ki temeljijo na projektih. Morda boste ugotovili, da nekatera polja, funkcije in privzeta logika, ki so na voljo v storitvi Sales, niso na voljo v storitvi Project Operations.

Naslednja tabela vključuje polja pri priložnosti, ki temelji na projektih, ki so na voljo le v storitvi Project Operations ali pa imajo nekatere pomembne spremembe v delovanju, po katerih se ločijo od priložnosti v storitvi Sales.

| **Polje** | **Mesto** | **Ustreznost, namen in smernice** | **Nadaljnji vpliv** |
| --- | --- | --- | --- |
| Vnesi | Zavihek »Splošno« (skrito) | To polje z naborom možnosti ima naslednje možnosti:</br>- temelji na delu (na voljo samo ob namestitvi storitve Project Operations)</br>- temelji na elementu (na voljo samo, če sta nameščeni storitvi Project Operations in Sales)</br>- temelji na vzdrževanju storitev (na voljo, ko je nameščena storitev Field Service) | Ko uporabljate Project Operations, je vrednost tega polja samodejno nastavljena na **Temelji na delu**, ki priložnost uvršča med priložnosti, ki temeljijo na projektih. Priložnost mora temeljiti na projektu, da lahko omogoča vse razširitve in funkcije, specifične za projekt, v nadaljnjem prodajnem postopku za ta posel. |
| Lastniško podjetje | Zavihek Splošno | To je podjetje ali pravna oseba, ki bo projekt dostavila stranki. | Podatki tega polja bodo kopirani v ustrezno polje v projektni ponudbi, ki je ustvarjena iz te priložnosti. |
| Stik | Zavihek Splošno | Sklic na primarni stik stranke za ta posel. | |
| Račun | Zavihek Splošno | Sklic na zapis strankinega podjetja ali kupca. | |
| Vodja za upravljanje kupcev | Zavihek Splošno | Ime upravitelja kupcev za to priložnost, ki temelji na projektu. | Upravitelj kupcev je odgovoren za upravljanje odnosa s stranko do zaključka tega projekta. Na podlagi zapisa vira, ki ga je mogoče rezervirati in je povezan z upraviteljem kupcev, je privzeto nastavljena pogodbena enota. |
| Pogodbena enota | Zavihek Splošno | Organizacijska enota, ki je odgovorna za izvedbo projektov, povezanih s tem poslom. | Pogodbena enota je oddelek podjetja, ki bo izvedel projekte po zaključku posla. Vsaka pogodbena enota ima valuto in ta valuta se uporablja za poročanje o ocenjenih in dejanskih stroških, nastalih med projektom. |

Za vsa druga polja in razdelke v zavihku priložnosti **Povzetek** glejte [Ustvarjanje ali urejanje priložnosti (Sales in središče za prodajo)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).
