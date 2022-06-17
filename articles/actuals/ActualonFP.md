---
title: Dejanski vpliv na dogovor s fiksno ceno
description: Ta članek vsebuje informacije o vplivu na tabelo Dejanske vrednosti pri različnih dogodkih v življenjskem ciklu pogodbe s fiksno ceno v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918148"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Dejanski vpliv na dogovor s fiksno ceno

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Naslednja tabela navaja dejansko stanje različnih vrst transakcij, ki so ustvarjene ob različnih dogodkih v poslu s fiksno ceno.

| Dogodek | Dejanska cena | Dejanski nezaračunani znesek prodaje | Zaračunana dejanska prodaja | Primer |
|---|---|---|---|---|
| Čas je ustvarjen. | Ni na voljo. | Ni na voljo. | Ni na voljo. | <p>Bob Kozack iz organizacijske enote Fabrikam v ZDA, ki ima cenovno stopnjo 100 ameriških dolarjev (100 USD) na uro, dela na projektu, ki se imenuje "Namestitev armature v Adatumu." Ta projekt je preslikan na metodo obračunavanja s fiksno ceno na pogodbeni vrstici. Tukaj je vzorčni vnos časa Boba Kozaka:</p><p>Bob Kozack - 8 ur</p> |
| Čas je oddan. | Ni na voljo. | Ni na voljo. | Ni na voljo. | Za vnos časa se ustvari vrstica stroškovnega dnevnika. Privzeta stroškovna stopnja se vnese v temeljnico. |
| Časovni vnos se prikliče, preden je odobren. | Ni na voljo. | Ni na voljo. | Ni na voljo. | |
| Čas je odobren. | Ustvari se dejanski strošek. | Ni na voljo. | Ni na voljo. | <p>Novo dejansko, ki je ustvarjeno:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, USD 800</li></ul> |
| Odobritev časa je preklicana. | <p>Stanje prilagoditve dejanskih prvotnih stroškov je posodobljeno na **Prilagojen**.</p><p>Ustvari se dejanski strošek razveljavitve, ki ima status prilagoditve **Nenastavljiva**.</p> | Ni na voljo. | Ni na voljo. | <p>Obstoječe dejansko, ki je posodobljeno:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, USD 800, *Prilagojen*</li></ul><p>Novo dejansko stanje, ki je ustvarjeno za razveljavitev prejšnjega finančnega učinka:</p><ul><li>**Dejanski strošek:** Bob Kozack, (8 ur), (800 USD), *Nenastavljiva*</li></ul> |
| Časovni vnos se prikliče, ko je odobren. | <p>Stanje prilagoditve dejanskih prvotnih stroškov je posodobljeno na **Prilagojen**.</p><p>Ustvari se dejanski strošek razveljavitve, ki ima status prilagoditve **Nenastavljiva**.</p> | Ni na voljo. | Ni na voljo. | <p>Obstoječe dejansko, ki je posodobljeno:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, USD 800, *Prilagojen*</li></ul><p>Novo dejansko stanje, ki je ustvarjeno za razveljavitev prejšnjega finančnega učinka:</p><ul><li>**Dejanski strošek:** Bob Kozack, (8 ur), (800 USD), *Nenastavljiva*</li></ul> |
| Pogodba je potrjena. | <p>Stanje prilagoditve starih dejanskih stroškov je posodobljeno na **Prilagojen**.</p><p>Ustvarijo se dejanski stroški odprave stroškov, ki imajo status prilagoditve **Nenastavljiva**.</p><p>Novi dejanski stroški se ustvarijo po ponovni oceni pogodbenih pravil.</p> | Ni na voljo. | Ni na voljo. | <p>Obstoječe dejansko, ki je posodobljeno:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, USD 800, *Prilagojen*</li></ul><p>Novo dejansko stanje, ki je ustvarjeno za razveljavitev prejšnjega finančnega učinka:</p><ul><li>**Dejanski strošek:** Bob Kozack, (8 ur), (800 USD), *Nenastavljiva*</li></ul><p>Novo dejansko stanje, ki je ustvarjeno za ponovno ovrednoten finančni učinek:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, USD 800</li></ul> |
| Ustvarjen je račun. | Ni na voljo. | Ni na voljo. | Ni na voljo. | |
| Račun je potrjen z mejnikom. | Ni na voljo. | Ni na voljo. | Ustvarjajo se novi dejanski podatki o zaračunani prodaji na podlagi mejnikov. | <p>Obstoječe dejansko, ki ostane nespremenjeno:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, USD 800</li></ul><p>Novo dejansko stanje, ki je ustvarjeno za beleženje obračunanih prodajnih vrednosti:</p><ul><li>**Dejanska zaračunana prodaja:** Mejnik, USD 5,000</li></ul> |
| Račun je popravljen tako, da se pripiše mejnik. | Ni na voljo. | Ni na voljo. | Ustvarjene so dejanske prodajne vrednosti zaračunane prodaje. | <p>Obstoječe dejansko, ki ostane nespremenjeno:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, 800 USD</li></ul><p>Obstoječe dejansko, ki je posodobljeno:</p><ul><li>**Dejanska zaračunana prodaja:** Mejnik, USD 5,000, *Prilagojen*</li></ul><p>Novo dejansko stanje, ki je ustvarjeno za razveljavitev prejšnjih zaračunanih prodajnih vrednosti:</p><ul><li>**Dejanska zaračunana prodaja:** Mejnik, (5.000 USD), *Nenastavljiva*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
