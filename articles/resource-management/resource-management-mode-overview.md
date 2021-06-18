---
title: Pregled načinov upravljanja virov
description: TaTa tema vsebuje informacije o funkciji »Upravljanje virov« v storitvi Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94db65a2ddbdc6a7226c70907bcce4c45b4a3923
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000906"
---
# <a name="resource-management-modes-overview"></a>Pregled načinov upravljanja virov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


Dynamics 365 Project Operations podpira dva načina za izvajanje celotnega poteka rezervacije. Način upravljanja je opredeljen kot projektni parameter in ga je mogoče spremeniti ob spremembi vašega poslovanja.    

## <a name="central-mode"></a>Osrednji način
Organizacijam, ki centralizirajo dodelitev virov projektom, osrednji način omogoča, da lahko vodje projektov določijo zahtevane pogoje za vire na ravni projekta. Izpolnjevanje zahtevanih pogojev za vire je preneseno na upravitelja virov. Vodje projektov lahko sprejmejo ali zavrnejo vire, ki jih predlaga upravitelj virov.

![Osrednji način](./media/resource-management-central.png)

Za upravljanje virov v osrednjem načinu glejte:

- [Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in ustvarjanje zahtevanih pogojev za vir](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervacija poimenovanih virov iz zahtevanih pogojev za vire](/dynamics365/project-service/book-named-resource)
- [Pošiljanje zahteve za vir](/dynamics365/project-service/submit-resource-request)
- [Izpolnjevanje zahteve za vir](/dynamics365/project-service/resource-management-fulfill-requests)
- [Sprejem ali zavrnitev predlaganega projektnega vira iz zahteve za vir](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibridni način
Organizacijam, ki potrebujejo prilagodljivost pri dodeljevanju virov, hibridni način omogoča, da vodje projektov in upravitelji virov rezervirajo vire.

![Hibridni način](./media/resource-management-hybrid.png)

Poleg podprtega postopka v osrednjem načinu glejte tudi naslednje teme za upravljanje vseh drugih podprtih potekov za rezervacije v hibridnem načinu:

Rezervacija vira neposredno iz projekta:
- [Rezervacija poimenovanih virov, ki jih je mogoče rezervirati, za projektno ekipo in dodelitev opravil](/dynamics365/project-service/assign-named-bookable-resource)

Rezervacija vira iz zahtevanega pogoja za vir:
- [Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in ustvarjanje zahtevanih pogojev za vir](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervacija poimenovanih virov iz zahtevanih pogojev za vire](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]