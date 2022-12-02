---
title: Poslovne transakcije v aplikaciji Project Operations
description: Ta članek nudi pregled koncepta poslovnih transakcij v programu Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923300"
---
# <a name="business-transactions-in-project-operations"></a>Poslovne transakcije v aplikaciji Project Operations

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V programu Microsoft Dynamics 365 Project Operations je *poslovna transakcija* abstrakten koncept, ki ga ne predstavlja nobena entiteta. Vendar so nekatera skupna področja in procesi za entitete zasnovani tako, da uporabljajo koncept poslovnih transakcij. Ta abstraktni element uporabljajo naslednje entitete:

- Podrobnosti vrstice ponudb
- Podrobnosti vrstice pogodb
- Vrstice ocen
- Vrstice dnevnikov
- Opravljeno delo

Od teh entitet so podrobnosti vrstice ponudb, podrobnosti vrstice pogodb in vrstice ocen preslikane na *stopnjo ocenjevanja* v življenjskem ciklu projekta. Entiteti »Vrstice dnevnikov« in »Dejanske vrednosti« sta preslikani na *stopnjo izvedbe* v življenjskem ciklu projekta.

Project Operations zapise v vseh teh petih entitetah obravnava kot poslovne transakcije. Edina razlika je, da se zapisi v entitetah, ki so preslikane na stopnjo ocenjevanja (podrobnosti vrstice ponudb, podrobnosti vrstice pogodb in vrstice ocen), upoštevajo kot *finančne napovedi*, medtem ko se zapisi v entitetah, ki so preslikane na stopnjo izvedbe (vrstice dnevnikov in dejanske vrednosti), upoštevajo kot *finančna dejstva*, ki so se že zgodila.

Če želite več informacij, glejte [Ocene](../project-management/estimating-projects-overview.md) in [Dejanske vrednosti](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepti, ki so značilni za poslovne transakcije

Naslednji koncepti so značilni za koncept poslovnih transakcij:

- Vrsta transakcije
- Razred transakcije
- Izvor transakcije
- Povezava transakcije

### <a name="transaction-type"></a>Vrsta transakcije

Vrsta transakcije predstavlja čas in kontekst finančnega učinka na projekt. Določa jo nabor možnosti, ki ima v aplikaciji Project Operations naslednje podprte vrednosti:

- Cena
- Projektna pogodba
- Neobračunana prodaja
- Obračunana prodaja
- Prodaja znotraj organizacije
- Cena enote vira

### <a name="transaction-class"></a>Razred transakcije

Razred transakcije predstavlja različne vrste stroškov, ki nastanejo pri projektih. Določa jo nabor možnosti, ki ima v aplikaciji Project Operations naslednje podprte vrednosti:

- Čas
- Stroški
- Material
- Dajatev
- Mejnik
- Davek

> [!NOTE]
> Vrednost **Mejnik** se v aplikaciji Project Operations običajno uporablja v poslovni logiki za obračunavanje fiksnih cen.

### <a name="transaction-origin"></a>Izvor transakcije

Izvor transakcije je entiteta, ki hrani izvor vsake poslovne transakcije za pomoč pri poročanju in sledljivosti. Ko se začne izvajati projekt, vsaka poslovna transakcija ustvari še eno poslovno transakcijo, ki bo posledično ustvarila drugo poslovno transakcijo in tako naprej.

### <a name="transaction-connection"></a>Povezava transakcije

Povezava transakcije je entiteta, ki shranjuje odnos med dvema podobnima poslovnima transakcijama, kot so stroški in povezani dejanski podatki o prodaji ali stornirane transakcije, ki jih sprožijo obračunske dejavnosti, kot so potrditev računa ali popravki računa.

Skupaj vam entiteti izvora transakcije in povezave transakcije pomagata slediti odnosom med poslovnimi transakcijami in dejanji, ki povzročijo ustvarjanje določene poslovne transakcije.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
