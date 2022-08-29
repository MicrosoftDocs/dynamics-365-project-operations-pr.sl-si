---
title: Prehodi stanja pri podizvajalski pogodbi
description: V tem članku so razloženi prehodi stanj pri podizvajalski pogodbi v Microsoftu Dynamics 365 Project Operations ko je podizvajalska pogodba ustvarjena, izvedena in zaključena.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 02553099a6728c19c219659dff431ff9a5cf10fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261295"
---
# <a name="state-transitions-on-a-subcontract"></a>Prehodi stanja pri podizvajalski pogodbi 

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

V tem članku so razloženi prehodi stanj pri podizvajalski pogodbi v Microsoftu Dynamics 365 Project Operations. Vsako stanje je predstavljeno kot osnutek, potrjen, zaprt ali preklican. Naslednja slika predstavlja prehode stanj.

![Model podizvajalske države](../media/SubconStates.png)  

Naslednja tabela ponuja opis tega, kaj vsako stanje predstavlja v življenjskem ciklu podizvajalske pogodbe v Project Operations.

| Država/regija | Description | Dovoljeni prehodi |
| --- | --- | --- |
| Osnutek | To predstavlja začetno stanje podizvajalske pogodbe. Pogajanja s prodajalcem so v teku. Linije in cene se lahko spremenijo. Podizvajalsko pogodbo v tem stanju je mogoče uporabiti za oceno in kadrovske potrebe projekta glede virov in materialov. Prav tako se lahko sklicuje na čas, stroške in porabo materiala pri projektu. Podizvajalsko pogodbo v tem stanju je mogoče urejati in brisati. | Potrjeno |
| Potrjeno | To predstavlja stopnjo podizvajalske pogodbe, potem ko so pogajanja s prodajalcem o cenah in predmetih naročila zaključena. Dejanska dobava materiala in/ali dela s strani podizvajalcev pa še vedno poteka. Podizvajalsko pogodbo v tem stanju je mogoče uporabiti za oceno in kadrovske potrebe projekta glede virov in materialov. Prav tako se lahko sklicuje na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali brisati. The **Prekliči** gumb omogoča preklic potrjene podizvajalske pogodbe. The **Ponovno odpri** gumb vam omogoča, da ponovno odprete podizvajalsko pogodbo, da jo ponovno vključite **Osnutek** stanje. Uporabi **Zapri** gumb za zaključek potrjene podizvajalske pogodbe. | Zaključevanje <br> Preklicano <br> Osnutek |
| Zaključevanje | To predstavlja fazo podizvajalske pogodbe, ko je dejanska dobava materiala in/ali dela s strani podizvajalcev zaključena. Podizvajalske pogodbe v tem stanju ni več mogoče uporabiti za oceno in osebje projektnih potreb glede virov in materialov. Prav tako se ne more več sklicevati na čas, stroške in porabo materiala v projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali brisati. | Ni priprav ali omejitev |
| Preklicano | To predstavlja fazo podizvajalske pogodbe, ko dejanska dobava materiala in/ali dela s podizvajalskimi viri ni več potrebna. Podizvajalske pogodbe v tem stanju ni mogoče uporabiti za ocenjevanje in zaposlovanje projektnih potreb glede virov in materialov, niti se ne more sklicevati na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali brisati. | Ni priprav ali omejitev |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
