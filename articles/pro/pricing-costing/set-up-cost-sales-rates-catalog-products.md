---
title: Nastavitev cen in prodaje za izdelke iz kataloga – poenostavljeno
description: Ta tema vsebuje informacije o nastavitvi mer stroškov in prodajnih zneskov za elemente v katalogu izdelkov.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274478"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Nastavitev cen in prodaje za izdelke iz kataloga – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_


Nastavitev cen za elemente kataloga izdelkov v storitvi Dynamics 365 Project Operations je enako kot v Dynamics 365 Sales.

V storitvi Project Operations izdelkov ni mogoče oceniti ali uporabiti na projektih, zato ni nujno, da so nastavljene cene kataloga izdelkov na projektnih cenikih za ponudbe in pogodbe.

Uporabite polja **Cena izdelka** za ponudbo, pogodbo ali kupca, da nastavite cene kataloga izdelkov. Ne nastavljajte cen kataloga izdelkov v projektnih cenikih. Ceniki za projekte so uporabljeni izključno v aplikaciji Project Operations. Poslovna logika, specifična za aplikacije, kopira cenike iz ponudbe v pogodbo. Rezultat tega je poseben cenik za pogodbo. Kopiranje lahko odloži postopek pridobivanja ponudbe, če cenik za projekte v ponudbi postane prevelik. Ceniki za izdelke se ne kopirajo, da bi v pogodbah ustvarili cenike po meri. Ker ni vključenega kopiranja, ni vplivov na delovanje postopka ponudbe.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]