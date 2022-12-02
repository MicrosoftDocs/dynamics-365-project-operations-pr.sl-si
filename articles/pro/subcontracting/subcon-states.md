---
title: Prehodi stanja pri podizvajalski pogodbi
description: V tem članku so pojasnjeni prehodi stanj pri podizvajalski pogodbi v aplikaciji Microsoft Dynamics 365 Project Operations, ko je podizvajalska pogodba ustvarjena, izvedena in zaključena.
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

V tem članku so pojasnjeni prehodi stanj na podizvajalski pogodbi v aplikaciji Microsoft Dynamics 365 Project Operations. Vsako stanje je predstavljeno kot »Osnutek«, »Potrjeno«, »Zaprto« ali »Preklicano«. Naslednje slike prikazujejo prehode stanj.

![Model stanja pri podizvajalski pogodbi](../media/SubconStates.png)  

Naslednja tabela zagotavlja opis, kaj vsako stanje predstavlja v življenjskem ciklu podizvajalske pogodbe v aplikaciji Project Operations.

| Država/regija | Description | Dovoljeni prehodi |
| --- | --- | --- |
| Osnutek | To predstavlja začetno stanje podizvajalske pogodbe. Pogajanja z dobaviteljem so v teku. Vrstice in cene se lahko spremenijo. Podizvajalsko pogodbo v tem stanju je mogoče uporabiti za oceno in potrebe za osebje projekta glede virov in materialov. Lahko se tudi sklicuje na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urediti ali izbrisati. | Potrjeno |
| Potrjeno | To predstavlja stopnjo podizvajalske pogodbe, potem ko so pogajanja z dobaviteljem o cenah in kupljenih vrsticah elementov zaključena. Dejanska dobava materiala in/ali dela podizvajalcev pa še vedno poteka. Podizvajalsko pogodbo v tem stanju je mogoče uporabiti za oceno in potrebe za osebje projekta glede virov in materialov. Lahko se tudi sklicuje na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urediti ali izbrisati. Gumb **Prekliči** omogoča preklic potrjene podizvajalske pogodbe. Gumb **Ponovno odpri** omogoča, da ponovno odprete podizvajalsko pogodbo in jo ponovno pretvorite v stanje **Osnutek**. Uporabite gumb **Zapri** za zaključek potrjene podizvajalske pogodbe. | Zaključevanje <br> Preklicano <br> Osnutek |
| Zaključevanje | To predstavlja stopnjo podizvajalske pogodbe, ko je dejanska dobava materiala in/ali dela podizvajalcev dokončana. Podizvajalsko pogodbo v tem stanju ni več mogoče uporabiti za oceno in potrebe za osebje projekta glede virov in materialov. Prav tako se ne more več sklicevati na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urediti ali izbrisati. | Ni priprav ali omejitev |
| Preklicano | To predstavlja stopnjo podizvajalske pogodbe, ko dejanska dobava materiala in/ali dela podizvajalcev ni več potrebna. Podizvajalske pogodbe v tem stanju ni mogoče uporabiti za oceno in zahteve osebja projekte za vire in materiale, prav tako pa se ne morete sklicevati na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urediti ali izbrisati. | Ni priprav ali omejitev |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
