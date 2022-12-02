---
title: Vpliv dejanskih vrednosti pri interakciji s fiksno ceno
description: Ta članek vsebuje informacije o vplivu na tabelo »Dejanske vrednosti« ob različnih dogodkih v življenjskem ciklu pri interakciji s fiksno ceno v programu Microsoft Dynamics 365 Project Operations.
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
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Vpliv dejanskih vrednosti pri interakciji s fiksno ceno

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Naslednja tabela navaja dejanske vrednosti različnih vrst transakcij, ki se ustvarijo ob različnih dogodkih pri interakciji s fiksno ceno.

| Dogodek | Dejanska cena | Dejanski nezaračunani znesek prodaje | Dejanski znesek obračunane prodaje | Primer |
|---|---|---|---|---|
| Čas je ustvarjen. | Ni na voljo. | Ni na voljo. | Ni na voljo. | <p>Bob Kozack iz organizacijske enote Fabrikam ZDA, ki ima mero stroškov 100 ameriških dolarjev (100 USD) na uro, dela na projektu, ki se imenuje »Namestitev roke v podjetju Adatum«. Ta projekt je preslikan v način obračunavanja po fiksni ceni v podrobnostih pogodbe. Tukaj je vzorec časovnega vnosa Boba Kozaka:</p><p>Bob Kozack – 8 ur</p> |
| Čas je poslan. | Ni na voljo. | Ni na voljo. | Ni na voljo. | Ustvari se vrstica dnevnika stroškov za časovni vnos. Privzeta stopnja stroška je vnesena v dnevniški zapis. |
| Časovni vnos je preklican, preden je odobren. | Ni na voljo. | Ni na voljo. | Ni na voljo. | |
| Čas je odobren. | Ustvarjena je dejanska cena. | Ni na voljo. | Ni na voljo. | <p>Nova dejanska vrednost, ki je ustvarjena:</p><ul><li>**Dejanska cena:** Bob Kozack, 8 ur, 800 USD</li></ul> |
| Odobritev časa je preklicana. | <p>Stanje prilagoditve prvotne dejanske cene se posodobi na **Prilagojeno**.</p><p>Ustvari se dejanska cena storniranja, ki ima stanje prilagoditve **Ni mogoče prilagoditi**.</p> | Ni na voljo. | Ni na voljo. | <p>Obstoječa dejanska vrednost, ki je posodobljena:</p><ul><li>**Dejanska cena:** Bob Kozack, 8 ur, 800 USD, *Prilagojeno*</li></ul><p>Nova dejanska vrednost, ki je ustvarjena za storniranje prejšnjega finančnega učinka:</p><ul><li>**Dejanska cena:** Bob Kozack, (8 ur), (800 USD), *Ni mogoče prilagoditi*</li></ul> |
| Časovni vnos se prekliče, ko je odobren. | <p>Stanje prilagoditve prvotne dejanske cene se posodobi na **Prilagojeno**.</p><p>Ustvari se dejanska cena storniranja, ki ima stanje prilagoditve **Ni mogoče prilagoditi**.</p> | Ni na voljo. | Ni na voljo. | <p>Obstoječa dejanska vrednost, ki je posodobljena:</p><ul><li>**Dejanska cena:** Bob Kozack, 8 ur, 800 USD, *Prilagojeno*</li></ul><p>Nova dejanska vrednost, ki je ustvarjena za storniranje prejšnjega finančnega učinka:</p><ul><li>**Dejanska cena:** Bob Kozack, (8 ur), (800 USD), *Ni mogoče prilagoditi*</li></ul> |
| Pogodba je potrjena. | <p>Stanje prilagoditve starih dejanskih cen se posodobi na **Prilagojeno**.</p><p>Ustvarijo se dejanske cene storniranja, ki imajo stanje prilagoditve **Ni mogoče prilagoditi**.</p><p>Nove dejanske cene se ustvarijo po ponovni oceni pogodbenih pravil.</p> | Ni na voljo. | Ni na voljo. | <p>Obstoječa dejanska vrednost, ki je posodobljena:</p><ul><li>**Dejanska cena:** Bob Kozack, 8 ur, 800 USD, *Prilagojeno*</li></ul><p>Nova dejanska vrednost, ki je ustvarjena za storniranje prejšnjega finančnega učinka:</p><ul><li>**Dejanska cena:** Bob Kozack, (8 ur), (800 USD), *Ni mogoče prilagoditi*</li></ul><p>Nova dejanska vrednost, ki je ustvarjena za ponovno ovrednoten finančni učinek:</p><ul><li>**Dejanska cena:** Bob Kozack, 8 ur, 800 USD</li></ul> |
| Račun je ustvarjen. | Ni na voljo. | Ni na voljo. | Ni na voljo. | |
| Račun je potrjen z zneskom mejnika. | Ni na voljo. | Ni na voljo. | Ustvarjene so nove dejanske vrednosti obračunane prodaje na podlagi mejnikov. | <p>Obstoječa dejanska vrednost, ki ostane nespremenjena:</p><ul><li>**Dejanska cena:** Bob Kozack, 8 ur, 800 USD</li></ul><p>Nova dejanska vrednost, ki je ustvarjena za beleženje obračunanih prodajnih vrednosti:</p><ul><li>**Dejanski znesek obračunane prodaje:** mejnik, 5.000 USD</li></ul> |
| Račun je popravljen v dobro mejnika. | Ni na voljo. | Ni na voljo. | Ustvarjene so stornirane dejanske vrednosti obračunane prodaje. | <p>Obstoječa dejanska vrednost, ki ostane nespremenjena:</p><ul><li>**Dejanska cena:** Bob Kozack, 8 ur, 800 USD</li></ul><p>Obstoječa dejanska vrednost, ki je posodobljena:</p><ul><li>**Dejanski znesek obračunane prodaje:** mejnik, 5.000 USD, *Prilagojeno*</li></ul><p>Nova dejanska vrednost, ki je ustvarjena za storniranje prejšnjih obračunanih prodajnih vrednosti:</p><ul><li>**Dejanski znesek obračunane prodaje:** mejnik, (5.000 USD),*Ni mogoče prilagoditi*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
