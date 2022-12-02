---
title: Vpliv dejanskih vrednosti na interni projekt
description: Ta članek vsebuje informacije o vplivu na tabelo »Dejanske vrednosti« ob različnih dogodkih za interni projekt v programu Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921368"
---
# <a name="actuals-impact-for-an-internal-project"></a>Vpliv dejanskih vrednosti na interni projekt

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Naslednja tabela navaja dejanske vrednosti različnih vrst transakcij, ki se ustvarijo ob različnih dogodkih pri interakciji z internim projektom.

| Dogodek | Dejanska cena | Primer |
|---|---|---|
| Čas je ustvarjen. | Ni na voljo. | <p>Bob Kozack iz organizacijske enote Fabrikam ZDA, ki ima mero stroškov 100 ameriških dolarjev (100 USD) na uro, dela na projektu, ki se imenuje »Namestitev roke v podjetju Adatum«. Ta projekt je preslikan v način obračunavanja po fiksni ceni v podrobnostih pogodbe. Tukaj je vzorec časovnega vnosa Boba Kozaka:</p><p>Bob Kozack – 8 ur</p> |
| Čas je poslan. | Ni na voljo. | Ustvari se vrstica dnevnika stroškov za časovni vnos. Privzeta stopnja stroška je vnesena v dnevniški zapis. |
| Časovni vnos je preklican, preden je odobren. | Ni na voljo. | |
| Čas je odobren. | Ustvarjena je dejanska cena. | <p>Nova dejanska vrednost, ki je ustvarjena:</p><ul><li>**Dejanska cena:** Bob Kozack, 8 ur, 800 USD</li></ul> |
| Odobritev časa je preklicana. | <p>Stanje prilagoditve prvotne dejanske cene se posodobi na **Prilagojeno**.</p><p>Ustvari se dejanska cena storniranja, ki ima stanje prilagoditve **Ni mogoče prilagoditi**.</p> | <p>Obstoječa dejanska vrednost, ki je posodobljena:</p><ul><li>**Dejanska cena:** Bob Kozack, 8 ur, 800 USD, *Prilagojeno*</li></ul><p>Nova dejanska vrednost, ki je ustvarjena za storniranje prejšnjega finančnega učinka:</p><ul><li>**Dejanska cena:** Bob Kozack, (8 ur), (800 USD), *Ni mogoče prilagoditi*</li></ul> |
| Časovni vnos se prekliče, ko je odobren. | <p>Stanje prilagoditve prvotne dejanske cene se posodobi na **Prilagojeno**.</p><p>Ustvari se dejanska cena storniranja, ki ima stanje prilagoditve **Ni mogoče prilagoditi**.</p> | <p>Obstoječa dejanska vrednost, ki je posodobljena:</p><ul><li>**Dejanska cena:** Bob Kozack, 8 ur, 800 USD, *Prilagojeno*</li></ul><p>Nova dejanska vrednost, ki je ustvarjena za storniranje prejšnjega finančnega učinka:</p><ul><li>**Dejanska cena:** Bob Kozack, (8 ur), (800 USD), *Ni mogoče prilagoditi*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
