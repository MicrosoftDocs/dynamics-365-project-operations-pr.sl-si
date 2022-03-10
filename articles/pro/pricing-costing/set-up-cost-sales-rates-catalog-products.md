---
title: Nastavitev cen in prodaje za izdelke iz kataloga – poenostavljeno
description: Ta tema vsebuje informacije o nastavitvi mer stroškov in prodajnih zneskov za elemente v katalogu izdelkov.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996051"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Nastavitev cen in prodaje za izdelke iz kataloga – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_


Nastavitev cen za elemente kataloga izdelkov v storitvi Dynamics 365 Project Operations je enako kot v Dynamics 365 Sales.

V storitvi Project Operations izdelkov ni mogoče oceniti ali uporabiti na projektih, zato ni nujno, da so nastavljene cene kataloga izdelkov na projektnih cenikih za ponudbe in pogodbe.

Uporabite polja **Cena izdelka** za ponudbo, pogodbo ali kupca, da nastavite cene kataloga izdelkov. Ne nastavljajte cen kataloga izdelkov v projektnih cenikih. Ceniki za projekte so uporabljeni izključno v aplikaciji Project Operations. Poslovna logika, specifična za aplikacije, kopira cenike iz ponudbe v pogodbo. Rezultat tega je poseben cenik za pogodbo. Kopiranje lahko odloži postopek pridobivanja ponudbe, če cenik za projekte v ponudbi postane prevelik. Ceniki za izdelke se ne kopirajo, da bi v pogodbah ustvarili cenike po meri. Ker ni vključenega kopiranja, ni vplivov na delovanje postopka ponudbe.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]