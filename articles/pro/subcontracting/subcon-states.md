---
title: Prehodi stanja pri podizvajalski pogodbi
description: V tem članku so razloženi prehodi stanj pri podizvajalski pogodbi v Microsoftu Dynamics 365 Project Operations ko je podizvajalska pogodba ustvarjena, izvedena in zaključena.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522955"
---
# <a name="state-transitions-on-a-subcontract"></a>Prehodi stanja pri podizvajalski pogodbi 

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V tem članku so razloženi prehodi stanj pri podizvajalski pogodbi v Microsoftu Dynamics 365 Project Operations. Vsako stanje je predstavljeno kot osnutek, potrjen, zaprt ali preklican. Naslednja slika predstavlja prehode stanj.

![Model podizvajalske države](../media/SubconStates.png)  

Naslednja tabela ponuja opis tega, kaj vsako stanje predstavlja v življenjskem ciklu podizvajalske pogodbe v projektnih operacijah.

| Država/regija | Description | Dovoljeni prehodi |
| --- | --- | --- |
| Osnutek | To predstavlja začetno stanje podizvajalske pogodbe. Pogajanja s prodajalcem so v teku. Linije in cene se lahko spremenijo. Podizvajalsko pogodbo v tem stanju je mogoče uporabiti za oceno in kadrovske potrebe projekta glede virov in materialov. Lahko se tudi sklicuje na čas, stroške in porabo materiala pri projektu. Podizvajalsko pogodbo v tem stanju je mogoče urejati in brisati. | Potrjeno |
| Potrjeno | To predstavlja stopnjo podizvajalske pogodbe, potem ko so pogajanja s prodajalcem o cenah in predmetih naročila zaključena. Dejanska dobava materiala in/ali dela s strani podizvajalcev pa še vedno poteka. Podizvajalsko pogodbo v tem stanju je mogoče uporabiti za oceno in kadrovske potrebe projekta glede virov in materialov. Lahko se tudi sklicuje na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali brisati. The **Prekliči** gumb omogoča preklic potrjene podizvajalske pogodbe. The **Ponovno odpri** gumb vam omogoča, da ponovno odprete podizvajalsko pogodbo, da jo ponovno vključite **Osnutek** stanje. Uporabi **Zapri** gumb za zaključek potrjene podizvajalske pogodbe. | Zaključevanje <br> Preklicano <br> Osnutek |
| Zaključevanje | To predstavlja fazo podizvajalske pogodbe, ko je dejanska dobava materiala in/ali dela s strani podizvajalcev zaključena. Podizvajalske pogodbe v tem stanju ni več mogoče uporabiti za oceno in osebje projektnih potreb za vire in materiale. Prav tako se ne more več sklicevati na čas, stroške in porabo materiala v projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali brisati. | Ni priprav ali omejitev |
| Preklicano | To predstavlja fazo podizvajalske pogodbe, ko dejanska dobava materiala in/ali dela s strani podizvajalcev ni več potrebna. Podizvajalske pogodbe v tem stanju ni mogoče uporabiti za ocenjevanje in zaposlovanje projektnih potreb glede virov in materialov, niti se ne more sklicevati na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali brisati. | Ni priprav ali omejitev |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
