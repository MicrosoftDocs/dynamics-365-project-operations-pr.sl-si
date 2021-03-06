---
title: Pregled načinov upravljanja virov
description: Ta tema vsebuje informacije o funkciji »Upravljanje virov« v storitvi Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930111"
---
# <a name="resource-management-modes-overview"></a>Pregled načinov upravljanja virov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


Dynamics 365 Project Operations podpira dva načina za izvajanje celotnega poteka rezervacije. Način upravljanja je opredeljen kot projektni parameter in ga je mogoče spremeniti ob spremembi vašega poslovanja.    

## <a name="central-mode"></a>Osrednji način
Organizacijam, ki centralizirajo dodelitev virov projektom, osrednji način omogoča, da lahko vodje projektov določijo zahtevane pogoje za vire na ravni projekta. Izpolnjevanje zahtevanih pogojev za vire je preneseno na upravitelja virov. Vodje projektov lahko sprejmejo ali zavrnejo vire, ki jih predlaga upravitelj virov.

![Osrednji način](./media/resource-management-central.png)

Za upravljanje virov v osrednjem načinu glejte:

- [Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in ustvarjanje zahtevanih pogojev za vir](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervacija poimenovanih virov iz zahtevanih pogojev za vire](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Pošiljanje zahteve za vir](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Izpolnjevanje zahteve za vir](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Sprejem ali zavrnitev predlaganega projektnega vira iz zahteve za vir](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibridni način
Organizacijam, ki potrebujejo prilagodljivost pri dodeljevanju virov, hibridni način omogoča, da vodje projektov in upravitelji virov rezervirajo vire.

![Hibridni način](./media/resource-management-hybrid.png)

Poleg podprtega postopka v osrednjem načinu glejte tudi naslednje teme za upravljanje vseh drugih podprtih potekov za rezervacije v hibridnem načinu:

Rezervacija vira neposredno iz projekta:
- [Rezervacija poimenovanih virov, ki jih je mogoče rezervirati, za projektno ekipo in dodelitev opravil](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Rezervacija vira iz zahtevanega pogoja za vir:
- [Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in ustvarjanje zahtevanih pogojev za vir](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervacija poimenovanih virov iz zahtevanih pogojev za vire](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
