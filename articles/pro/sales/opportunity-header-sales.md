---
title: Nastavitve priložnosti – poenostavljeno
description: Ta tema vsebuje informacije o poslih, ki temeljijo na projektu, in podrobnostih pri priložnosti, ki temelji na projektu.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f40154fed5790083e3a4d3264cc9f8cc23ae18bc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596852"
---
# <a name="header-details-for-project-opportunities"></a>Podrobnosti glave za projektne priložnosti

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Glava »Priložnost« zajema splošne informacije o poslu, ki temelji na projektu in velja za vse podrobnosti pri priložnosti, ki temelji na projektu.

Priložnosti, ki temeljijo na projektih, v aplikaciji Dynamics 365 Project Operations so razširitve priložnosti v aplikaciji Dynamics 365 Sales. Te razširitve zagotavljajo dodatne funkcije, ki so specifične in potrebne za priložnosti, ki temeljijo na projektih. Te razširitve lahko vključujejo nova polja in dejanja traku, ki so na voljo pri priložnostih, ki temeljijo na projektih. Morda boste ugotovili, da nekatera polja, funkcije in privzeta logika, ki so na voljo v storitvi Sales, niso na voljo v storitvi Project Operations.

Naslednja tabela vključuje polja pri priložnosti, ki temelji na projektih, ki so na voljo le v storitvi Project Operations ali pa imajo nekatere pomembne spremembe v delovanju, po katerih se ločijo od priložnosti v storitvi Sales.

| **Polje** | **Mesto** | **Opis** | **Nadaljnji vpliv** |
| --- | --- | --- | --- |
| Vnesi | Zavihek »Splošno« (skrito) | To polje z naborom možnosti ima naslednje možnosti:</br>- temelji na delu (na voljo samo ob namestitvi storitve Project Operations)</br>- temelji na elementu (na voljo samo, če sta nameščeni storitvi Project Operations in Sales)</br>- temelji na vzdrževanju storitev (na voljo, ko je nameščena storitev Field Service) | Ko uporabljate Project Operations, je vrednost tega polja samodejno nastavljena na **Temelji na delu**, ki priložnost uvršča med priložnosti, ki temeljijo na projektih. Priložnost mora temeljiti na projektu, da lahko omogoča vse razširitve in funkcije, specifične za projekt, v nadaljnjem prodajnem postopku za ta posel. |
| Stik | Zavihek Splošno | Sklic na primarni stik stranke za ta posel. | |
| Račun | Zavihek Splošno | Sklic na zapis strankinega podjetja ali kupca. | |
| Vodja za upravljanje kupcev | Zavihek Splošno | Ime upravitelja kupcev za to priložnost, ki temelji na projektu. | Upravitelj kupcev je odgovoren za upravljanje odnosa s stranko do zaključka tega projekta. Na podlagi zapisa vira, ki ga je mogoče rezervirati in je povezan z upraviteljem kupcev, je privzeto nastavljena pogodbena enota. |
| Pogodbena enota | Zavihek Splošno | Organizacijska enota, ki je odgovorna za izvedbo projektov, povezanih s tem poslom. | Pogodbena enota je oddelek podjetja, ki bo izvedel projekte po zaključku posla. Vsaka pogodbena enota ima valuto in ta valuta se uporablja za poročanje o ocenjenih in dejanskih stroških, nastalih med projektom. |

Za vsa druga polja in razdelke v zavihku priložnosti **Povzetek** glejte [Ustvarjanje ali urejanje priložnosti (Sales in središče za prodajo)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
