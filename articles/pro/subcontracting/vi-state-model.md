---
title: Prehodi stanja pri računu dobavitelja
description: Ta članek pojasnjuje prehode stanj na računu dobavitelja v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261064"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Prehodi stanja pri računu dobavitelja

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta članek pojasnjuje prehode stanj na računu dobavitelja v Microsoftu Dynamics 365 Project Operations. Uporabljajo se naslednja stanja: **Osnutek**, **pregledu**, **·**, **čakanju**, in **Prekinjeno**.

Naslednje slike prikazujejo prehode stanj.

![Model prehoda stanja podizvajalca.](../media/VI_State_Model.jpg)

Naslednja tabela pojasnjuje, kaj vsako stanje predstavlja v življenjskem ciklu računa dobavitelja v Project Operations.

| Država/regija | Description | Dovoljeni prehodi |
| --- | --- | --- |
| Osnutek | To stanje je začetno stanje računa dobavitelja. Linije in cene se lahko spremenijo. Račun dobavitelja v tem stanju je mogoče urejati in brisati. | V teku |
| V pregledu | To stanje predstavlja stanje obdelave računa dobavitelja. Vsaj ena vrstica računa dobavitelja ima status preverjanja **V postopku**. | Potrjeno, na čakanju |
| Potrjeno | To stanje predstavlja fazo računa dobavitelja, kjer je aplikacija ustvarila dejanske stroške za vsako vrstico računa dobavitelja. Vsi povezani dejanski stroški, ki so bili usklajeni z vrsticami računa dobavitelja, so bili razveljavljeni in nadomeščeni z dejanskimi stroški iz teh vrstic računa dobavitelja. Računa dobavitelja v tem stanju ni mogoče urejati ali brisati. Lahko uporabite **Prekliči** gumb za preklic potrjenega računa dobavitelja. Dejanje Prekliči obrne učinek dejanja Potrditev. | Preklicano |
| Zadržano | <p>To stanje predstavlja stopnjo prodajalčevega računa, kjer se prodajalčev račun ne more premakniti zaradi težave z računom ali statusom prodajalca. Računa dobavitelja v tem stanju ni mogoče potrditi, preklicati, urediti ali izbrisati.</p><p>Z dejanjem Ponovno odpri lahko pomaknete račun prodajalca na stanje **Osnutek** ali **V pregledu**. Če ima vsaj ena vrstica na računu prodajalca stanje preverjanja **V teku** ali **Dokončano**, bo račun prodajalca ponovno odprt s stanjem **V pregledu**. Če imajo vse vrstice na računu prodajalca stanje preverjanja **Ni se začelo**, bo račun prodajalca ponovno odprt s stanjem **Osnutek**.</p> | Osnutek, v pregledu |
| Preklicano | To stanje predstavlja fazo podizvajalske pogodbe, kjer ni več potrebna dejanska dobava materiala in/ali dela s strani podizvajalcev. Podizvajalske pogodbe v tem stanju ni mogoče uporabiti za oceno in osebje projektnih potreb za vire in materiale, prav tako se ne morete sklicevati na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali brisati. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
