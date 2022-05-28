---
title: Prehodi stanja na računu prodajalca
description: Ta tema pojasnjuje prehode stanja na računu prodajalca v Microsoftu Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584708"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Prehodi stanja na računu prodajalca

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta tema pojasnjuje prehode stanja na računu prodajalca v Microsoftu Dynamics 365 Project Operations. Uporabljajo se naslednja stanja: **Osnutek**, **pregledu**, **·**, **čakanju**, in **Prekinjeno**.

Naslednje slike prikazujejo prehode stanja.

![Model prehoda stanja podizvajalcev.](../media/VI_State_Model.jpg)

Naslednja tabela pojasnjuje, kaj vsako stanje predstavlja v življenjskem ciklu računa prodajalca v Project Operations.

| Država/regija | Description | Dovoljeni prehodi |
| --- | --- | --- |
| Osnutek | To stanje je začetno stanje računa prodajalca. Linije in cene se lahko spremenijo. Račun prodajalca v tem stanju je mogoče urediti in izbrisati. | V teku |
| V pregledu | To stanje predstavlja stanje obdelave računa prodajalca. Vsaj ena vrstica računa prodajalca ima status preverjanja **V teku**. | Potrjeno, na čakanju |
| Potrjeno | To stanje predstavlja stopnjo računa prodajalca, kjer je aplikacija ustvarila dejanske stroške za vsako vrstico računa prodajalca. Vsi povezani dejanski stroški, ki so se ujemali z vrsticami računa prodajalca, so bili obrnjeni in nadomeščeni z dejanskimi stroški iz teh vrstic faktur prodajalca. Računa prodajalca v tem stanju ni mogoče urejati ali izbrisati. Lahko uporabite **Prekliči** gumb za preklic potrjenega računa prodajalca. Dejanje Prekliči obrne učinek dejanja Potrdi. | Preklicano |
| Zadržano | <p>To stanje predstavlja stopnjo računa prodajalca, kjer se račun prodajalca ne more premakniti zaradi težave z računom ali statusom prodajalca. Računa prodajalca v tem stanju ni mogoče potrditi, preklicati, urediti ali izbrisati.</p><p>Z dejanjem Ponovno odpri lahko pomaknete račun prodajalca na stanje **Osnutek** ali **V pregledu**. Če ima vsaj ena vrstica na računu prodajalca stanje preverjanja **V teku** ali **Dokončano**, bo račun prodajalca ponovno odprt s stanjem **V pregledu**. Če imajo vse vrstice na računu prodajalca stanje preverjanja **Ni se začelo**, bo račun prodajalca ponovno odprt s stanjem **Osnutek**.</p> | Osnutek, v pregledu |
| Preklicano | To stanje predstavlja stopnjo podizvajalca, kjer dejanska dobava materialov in/ali dela s podizvajalci ni več potrebna. Podizvajalske pogodbe v tem stanju ni mogoče uporabiti za oceno in zaposlovanje projektnih potreb po virih in materialih, prav tako pa se ni mogoče sklicevati na čas, stroške in porabo materiala pri projektu. Podizvajalske pogodbe v tem stanju ni mogoče urejati ali izbrisati. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
