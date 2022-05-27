---
title: Prehodi stanja pri podizvajalski pogodbi
description: Ta tema pojasnjuje prehode stanja na podizvajalski pogodbi v Microsoftu Dynamics 365 Project Operations ko se podizvajalska pogodba ustvari, izvede in zapre.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c9533d046398c708c55467e6b1a25acf6abade3e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579188"
---
# <a name="state-transitions-on-a-subcontract"></a>Prehodi stanja pri podizvajalski pogodbi 

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta tema pojasnjuje prehode stanja na podizvajalski pogodbi v Microsoftu Dynamics 365 Project Operations. Vsako stanje je predstavljeno kot osnutek, potrjeno, zaprto ali preklicano. Naslednja slika predstavlja prehode stanja.

![Model stanja podizvajalcev](../media/SubconStates.png)  

V naslednji tabeli je opisano, kaj vsako stanje predstavlja v življenjskem ciklu podizvajalske pogodbe v Project Operations.

| Država/regija | Description | Dovoljeni prehodi |
| --- | --- | --- |
| Osnutek | To predstavlja začetno stanje podizvajalske pogodbe. Pogajanja s prodajalcem so v teku. Linije in cene se lahko spremenijo. Podizvajalsko pogodbo v tem stanju je mogoče uporabiti za oceno in kadrovske potrebe projekta po virih in materialih. Lahko se navede tudi glede časa, stroškov in porabe materiala pri projektu. Podizvajalsko pogodbo v tem stanju je mogoče urediti in izbrisati. | Potrjeno |
| Potrjeno | To predstavlja fazo podizvajalca, potem ko so pogajanja s prodajalcem o cenah in artiklih, ki se kupujejo, končana. Vendar pa dejanska dobava materialov in/ali del s podizvajalci še vedno poteka. Podizvajalsko pogodbo v tem stanju je mogoče uporabiti za oceno in kadrovske potrebe projekta po virih in materialih. Lahko se navede tudi glede časa, stroškov in porabe materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali izbrisati. The **Prekliči** gumb omogoča preklic potrjene podizvajalske pogodbe. The **Ponovno odpri** Gumb vam omogoča, da ponovno odprete podizvajalsko pogodbo, da jo vrnete nazaj **Osnutek** stanje. Uporabi **Zapri** gumb za zapiranje potrjene podizvajalske pogodbe. | Zaključevanje <br> Preklicano <br> Osnutek |
| Zaključevanje | To predstavlja stopnjo podizvajalske pogodbe, ko je dejanska dobava materiala in/ali dela s podizvajalskimi sredstvi zaključena. Podizvajalske pogodbe v tem stanju ni več mogoče uporabiti za oceno in osebje projektnih potreb po virih in materialih. Prav tako se ne more več sklicevati na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali izbrisati. | Ni priprav ali omejitev |
| Preklicano | To predstavlja fazo podizvajalske pogodbe, ko dejanska dobava materiala in/ali dela s podizvajalci ni več potrebna. Podizvajalske pogodbe v tem stanju ni mogoče uporabiti za oceno in osebje projektnih potreb po virih in materialih, niti se nanjo ni mogoče sklicevati na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali izbrisati. | Ni priprav ali omejitev |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
