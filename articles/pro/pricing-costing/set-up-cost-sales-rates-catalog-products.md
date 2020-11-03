---
title: Nastavitev mer stroškov in prodajnih zneskov za kataloške izdelke
description: Ta tema vsebuje informacije o nastavitvi mer stroškov in prodajnih zneskov za elemente v katalogu izdelkov.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084823"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Nastavitev mer stroškov in prodajnih zneskov za kataloške izdelke

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_


Nastavitev cen za elemente kataloga izdelkov v aplikaciji Dynamics 365 Project Operations je enaka kot v aplikaciji Dynamics 365 Sales.

Ker izdelkov ni mogoče oceniti ali uporabiti v projektih v aplikaciji Project Operations, za ponudbe in pogodbe ni treba nastaviti cen v katalogu izdelkov v cenikih za projekte.

Cene v katalogu izdelkov je treba nastaviti v polju **Cena izdelka** ponudbe, pogodbe ali stranke. Za te entitete v cenikih za projekte ni treba nastaviti cen v katalogu izdelkov. Ceniki za projekte so uporabljeni izključno v aplikaciji Project Operations. Obstaja poslovna logika za aplikacije, ki kopira cenike iz ponudbe v pogodbo. Rezultat tega je poseben cenik za pogodbo. Kopiranje lahko odloži postopek pridobivanja ponudbe, če cenik za projekte v ponudbi postane prevelik. Ceniki za izdelke se ne kopirajo, da bi v pogodbah ustvarili cenike po meri. To pomeni, da ceniki za izdelke ne vplivajo na učinkovitost postopka pridobivanja ponudb.
