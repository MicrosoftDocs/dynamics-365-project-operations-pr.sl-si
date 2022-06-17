---
title: Pregled načinov upravljanja virov
description: Ta članek vsebuje informacije o funkcionalnosti upravljanja virov v Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dd50d12686a6ad17f6a95ccf0c2f1447cc470bf7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928452"
---
# <a name="resource-management-modes-overview"></a>Pregled načinov upravljanja virov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


Dynamics 365 Project Operations podpira dva načina za izvajanje celotnega poteka rezervacije. Način upravljanja je opredeljen kot projektni parameter in ga je mogoče spremeniti ob spremembi vašega poslovanja.    

## <a name="central-mode"></a>Osrednji način
Organizacijam, ki centralizirajo dodelitev virov projektom, osrednji način omogoča, da lahko vodje projektov določijo zahtevane pogoje za vire na ravni projekta. Izpolnjevanje zahtevanih pogojev za vire je preneseno na upravitelja virov. Vodje projektov lahko sprejmejo ali zavrnejo vire, ki jih predlaga upravitelj virov.

![Osrednji način.](./media/resource-management-central.png)

Za upravljanje virov v osrednjem načinu glejte:

- [Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in ustvarjanje zahtevanih pogojev za vir](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervacija poimenovanih virov iz zahtevanih pogojev za vire](/dynamics365/project-service/book-named-resource)
- [Pošiljanje zahteve za vir](/dynamics365/project-service/submit-resource-request)
- [Izpolnjevanje zahteve za vir](/dynamics365/project-service/resource-management-fulfill-requests)
- [Sprejem ali zavrnitev predlaganega projektnega vira iz zahteve za vir](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibridni način
Organizacijam, ki potrebujejo prilagodljivost pri dodeljevanju virov, hibridni način omogoča, da vodje projektov in upravitelji virov rezervirajo vire.

![Hibridni način.](./media/resource-management-hybrid.png)

Poleg podprtega postopka centralnega načina si oglejte naslednje članke za upravljanje vseh drugih podprtih tokov rezervacij v hibridnem načinu:

Rezervacija vira neposredno iz projekta:
- [Rezervacija poimenovanih virov, ki jih je mogoče rezervirati, za projektno ekipo in dodelitev opravil](/dynamics365/project-service/assign-named-bookable-resource)

Rezervacija vira iz zahtevanega pogoja za vir:
- [Dodeljevanje splošnih virov, ki jih je mogoče rezervirati, opravilu in ustvarjanje zahtevanih pogojev za vir](/dynamics365/project-service/assign-generic-bookable-resource)
- [Rezervacija poimenovanih virov iz zahtevanih pogojev za vire](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]