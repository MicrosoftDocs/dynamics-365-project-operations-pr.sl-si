---
title: Prehodi stanja pri računu dobavitelja
description: V tem članku so pojasnjeni prehodi stanj na računu dobavitelja v aplikaciji Microsoft Dynamics 365 Project Operations.
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

V tem članku so pojasnjeni prehodi stanj na računu dobavitelja v aplikaciji Microsoft Dynamics 365 Project Operations. Uporabljajo se naslednja stanja: **Osnutek**, **V pregledu**, **Potrjeno**, **Zadržano** in **Preklicano**.

Naslednje slike prikazujejo prehode stanj.

![Model prehoda stanja pri podizvajalski pogodbi.](../media/VI_State_Model.jpg)

Naslednja tabela pojasnjuje, kaj vsako stanje predstavlja v življenjskem ciklu računa dobavitelja v aplikaciji Project Operations.

| Država/regija | Description | Dovoljeni prehodi |
| --- | --- | --- |
| Osnutek | To stanje je začetno stanje računa dobavitelja. Vrstice in cene se lahko spremenijo. Računa dobavitelja v tem stanju ni mogoče urediti in izbrisati. | V teku |
| V pregledu | To stanje predstavlja stanje obdelave računa dobavitelja. Vsaj ena vrstica računa dobavitelja ima stanje preverjanja **V teku**. | Potrjeno, Zadržano |
| Potrjeno | To stanje predstavlja stopnjo računa dobavitelja, kjer je aplikacija ustvarila dejanske stroške za vsako vrstico računa dobavitelja. Vsi povezani dejanski stroški, ki so bili usklajeni z vrsticami računa dobavitelja, so bili razveljavljeni in nadomeščeni z dejanskimi stroški iz teh vrstic računa dobavitelja. Računa dobavitelja v tem stanju ni mogoče urediti ali izbrisati. Lahko uporabite gumb **Prekliči**, da prekličete potrjeni računa dobavitelja. Dejanje »Prekliči« razveljavi učinek dejanja »Potrdi«. | Preklicano |
| Zadržano | <p>To stanje predstavlja stopnjo računa dobavitelja, kjer se račun dobavitelja ne more premakniti zaradi težave z računom ali stanjem dobavitelja. Računa dobavitelja v tem stanju ni mogoče potrditi, preklicati, urediti ali izbrisati.</p><p>Z dejanjem »Ponovno odpri« lahko premaknete račun dobavitelja v stanje **Osnutek** ali **V pregledu**. Če ima vsaj ena vrstica na računu dobavitelja stanje preverjanja **V postopku** ali **Dokončano**, bo račun dobavitelja ponovno odprt v stanju **V pregledu**. Če imajo vse vrstice na računu dobavitelja stanje preverjanja **Ni začeto**, bo račun dobavitelja ponovno odprt v stanju **Osnutek**.</p> | Osnutek, V pregledu |
| Preklicano | To stanje predstavlja stopnjo podizvajalske pogodbe, kjer ni več potrebna dejanska dobava materiala in/ali dela podizvajalcev. Podizvajalske pogodbe v tem stanju ni mogoče uporabiti za oceno in zahteve osebja projekte za vire in materiale, prav tako pa se ne morete sklicevati na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urediti ali izbrisati. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
