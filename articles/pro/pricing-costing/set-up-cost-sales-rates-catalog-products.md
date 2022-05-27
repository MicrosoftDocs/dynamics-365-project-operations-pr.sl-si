---
title: Nastavitev cen in prodaje za izdelke iz kataloga – poenostavljeno
description: Ta tema vsebuje informacije o nastavitvi mer stroškov in prodajnih zneskov za elemente v katalogu izdelkov.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 12e09d99e9832c93c3aea34ec0d4488cdf6b02fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576842"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Nastavitev cen in prodaje za izdelke iz kataloga – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_


Nastavitev cen za elemente kataloga izdelkov v storitvi Dynamics 365 Project Operations je enako kot v Dynamics 365 Sales.

V storitvi Project Operations izdelkov ni mogoče oceniti ali uporabiti na projektih, zato ni nujno, da so nastavljene cene kataloga izdelkov na projektnih cenikih za ponudbe in pogodbe.

Uporabite polja **Cena izdelka** za ponudbo, pogodbo ali kupca, da nastavite cene kataloga izdelkov. Ne nastavljajte cen kataloga izdelkov v projektnih cenikih. Ceniki za projekte so uporabljeni izključno v aplikaciji Project Operations. Poslovna logika, specifična za aplikacije, kopira cenike iz ponudbe v pogodbo. Rezultat tega je poseben cenik za pogodbo. Kopiranje lahko odloži postopek pridobivanja ponudbe, če cenik za projekte v ponudbi postane prevelik. Ceniki za izdelke se ne kopirajo, da bi v pogodbah ustvarili cenike po meri. Ker ni vključenega kopiranja, ni vplivov na delovanje postopka ponudbe.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]