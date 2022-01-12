---
title: Prehodi držav na podizvajalsko pogodbo v projektnih operacijah
description: Ta tema pojasnjuje prehode stanja na podizvajalski pogodbi v Microsoftu Dynamics 365 Project Operations ko je podizvajalska pogodba ustvarjena, izvedena in zaključena.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4ca658440c7a9b29a927098f24c092d72d9eb0c9
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903099"
---
# <a name="state-transitions-on-a-subcontract-in-project-operations"></a>Prehodi držav na podizvajalsko pogodbo v projektnih operacijah

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta tema pojasnjuje prehode stanja na podizvajalski pogodbi v Microsoftu Dynamics 365 Project Operations. Vsako stanje je predstavljeno kot osnutek, potrjeno, zaprto ali preklicano. Naslednja slika predstavlja prehode stanja.

![Model stanja podizvajalcev](../media/SubconStates.png)  

V naslednji tabeli je opisano, kaj vsako stanje predstavlja v življenjskem ciklu podizvajalske pogodbe v Project Operations.

| Država/regija | Description | Dovoljeni prehodi |
| --- | --- | --- |
| Osnutek | To predstavlja začetno stanje podizvajalske pogodbe. Pogajanja s prodajalcem so v teku. Linije in cene se lahko spremenijo. Podizvajalsko pogodbo v tem stanju je mogoče uporabiti za oceno in kadrovske zahteve projekta po virih in materialih. Lahko se navede tudi glede časa, stroškov in porabe materiala pri projektu. Podizvajalsko pogodbo v tem stanju je mogoče urediti in izbrisati. | Potrjeno |
| Potrjeno | To predstavlja fazo podizvajalca, potem ko so pogajanja s prodajalcem o cenah in artiklih, ki se kupujejo, končana. Vendar pa dejanska dobava materialov in/ali del s podizvajalci še vedno poteka. Podizvajalsko pogodbo v tem stanju je mogoče uporabiti za oceno in kadrovske zahteve projekta po virih in materialih. Lahko se navede tudi glede časa, stroškov in porabe materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali izbrisati. The **Prekliči** gumb omogoča preklic potrjene podizvajalske pogodbe. The **Ponovno odpri** Gumb vam omogoča, da znova odprete podizvajalsko pogodbo, da jo vrnete **Osnutek** stanje. Uporabi **Zapri** gumb za zapiranje potrjene podizvajalske pogodbe. | Zaključevanje <br> Preklicano <br> Osnutek |
| Zaključevanje | To predstavlja fazo podizvajalca, ko je dejanska dobava materiala in/ali dela s podizvajalskimi sredstvi zaključena. Podizvajalske pogodbe v tem stanju ni več mogoče uporabiti za oceno in osebje projektnih potreb po virih in materialih. Prav tako se ne more več sklicevati na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali izbrisati. | Ni priprav ali omejitev |
| Preklicano | To predstavlja fazo podizvajalske pogodbe, ko dejanska dobava materiala in/ali dela s podizvajalci ni več potrebna. Podizvajalske pogodbe v tem stanju ni mogoče uporabiti za oceno in osebje projektnih potreb po virih in materialih, niti se nanjo ni mogoče sklicevati na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali izbrisati. | Ni priprav ali omejitev |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
