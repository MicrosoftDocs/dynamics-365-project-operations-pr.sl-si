---
title: Dejanski vpliv med predprodajno fazo posla
description: Ta članek vsebuje informacije o vplivu na tabelo Dejanske vrednosti na različnih dogodkih, medtem ko je posel v fazi predprodaje v Microsoftu Dynamics 365 Project Operations.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922380"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Dejanski vpliv med predprodajno fazo posla

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V naslednji tabeli so navedeni dejanski podatki različnih vrst transakcij, ki so ustvarjene na različnih dogodkih med predprodajno fazo projektnega posla.

| Dogodek | Dejanska cena | Primer |
|---|---|---|
| Čas je ustvarjen. | Ni na voljo. | <p>Bob Kozack iz organizacijske enote Fabrikam v ZDA, ki ima cenovno stopnjo 100 ameriških dolarjev (100 USD) na uro, dela na projektu, ki se imenuje "Namestitev armature v Adatumu." Ta projekt je preslikan na metodo obračunavanja s fiksno ceno na pogodbeni vrstici. Tukaj je vzorčni vnos časa Boba Kozaka:</p><p>Bob Kozack - 8 ur</p> |
| Čas je oddan. | Ni na voljo. | Za vnos časa se ustvari vrstica stroškovnega dnevnika. Privzeta stroškovna stopnja se vnese v temeljnico. |
| Časovni vnos se prikliče, preden je odobren. | Ni na voljo. | |
| Čas je odobren. | Ustvari se dejanski strošek. | <p>Novo dejansko, ki je ustvarjeno:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, USD 800</li></ul> |
| Odobritev časa je preklicana. | <p>Stanje prilagoditve dejanskih prvotnih stroškov je posodobljeno na **Prilagojen**.</p><p>Ustvari se dejanski strošek razveljavitve, ki ima status prilagoditve **Nenastavljiva**.</p> | <p>Obstoječe dejansko, ki je posodobljeno:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, USD 800, *Prilagojen*</li></ul><p>Novo dejansko stanje, ki je ustvarjeno za razveljavitev prejšnjega finančnega učinka:</p><ul><li>**Dejanski strošek:** Bob Kozack, (8 ur), (800 USD), *Nenastavljiva*</li></ul> |
| Časovni vnos se prikliče, ko je odobren. | <p>Stanje prilagoditve dejanskih prvotnih stroškov je posodobljeno na **Prilagojen**.</p><p>Ustvari se dejanski strošek razveljavitve, ki ima status prilagoditve **Nenastavljiva**.</p> | <p>Obstoječe dejansko, ki je posodobljeno:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, USD 800, *Prilagojen*</li></ul><p>Novo dejansko stanje, ki je ustvarjeno za razveljavitev prejšnjega finančnega učinka:</p><ul><li>**Dejanski strošek:** Bob Kozack, (8 ur), (800 USD), *Nenastavljiva*</li></ul> |
| Ponudba je pridobljena in pogodba se ustvari. | <p>Stanje prilagoditve starih dejanskih stroškov je posodobljeno na **Prilagojen**.</p><p>Ustvarijo se dejanski stroški odprave stroškov, ki imajo status prilagoditve **Nenastavljiva**.</p><p>Novi dejanski stroški se ustvarijo po ponovni oceni pogodbenih pravil.</p> | <p>Obstoječe dejansko, ki je posodobljeno:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, USD 800, *Prilagojen*</li></ul><p>Novo dejansko stanje, ki je ustvarjeno za razveljavitev prejšnjega finančnega učinka:</p><ul><li>**Dejanski strošek:** Bob Kozack, (8 ur), (800 USD), *Nenastavljiva*</li></ul><p>Nove dejanske vrednosti, ki so ustvarjene za ponovno ovrednoteni finančni učinek, ko je ponudba dosežena in je pogodba ustvarjena:</p><ul><li>**Dejanski strošek:** Bob Kozack, 8 ur, USD 800</li><li>**Dejanska neobračunana prodaja:** Bob Kozack, 8 ur, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
