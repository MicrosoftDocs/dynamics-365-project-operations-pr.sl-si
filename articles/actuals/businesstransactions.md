---
title: Poslovne transakcije v aplikaciji Project Operations
description: Ta članek ponuja pregled koncepta poslovnih transakcij v Microsoftu Dynamics 365 Project Operations.
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

V Microsoftu Dynamics 365 Project Operations, *transakcija* je abstrakten koncept, ki ga ne predstavlja nobena entiteta. Vendar so nekatera skupna področja in procesi za entitete zasnovani tako, da uporabljajo koncept poslovnih transakcij. Ta abstraktni element uporabljajo naslednje entitete:

- Podrobnosti vrstice ponudb
- Podrobnosti vrstice pogodb
- Vrstice ocen
- Vrstice dnevnikov
- Opravljeno delo

Od teh entitet so podrobnosti vrstice ponudbe, podrobnosti pogodbene vrstice in vrstice ocene preslikane v *faza ocene* v življenjskem ciklu projekta. Entitete vrstice dnevnika in dejanske vrednosti so preslikane v *faza izvedbe* v življenjskem ciklu projekta.

Projektno poslovanje obravnava evidence v vseh petih od teh subjektov kot poslovne transakcije. Edina razlika je v tem, da se upoštevajo zapisi v entitetah, ki so preslikani v fazo ocene (podrobnosti vrstice ponudbe, podrobnosti pogodbene vrstice in vrstice ocene).*finančne napovedi*, medtem ko se upoštevajo zapisi v entitetah, ki so preslikani na fazo izvajanja (vrstice dnevnika in dejanske vrednosti).*finančna dejstva* ki so se že zgodile.

Če želite več informacij, glejte [Ocene](../project-management/estimating-projects-overview.md) in [Dejanske vrednosti](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepti, ki so značilni za poslovne transakcije

Naslednji koncepti so značilni za koncept poslovnih transakcij:

- Vrsta transakcije
- Razred transakcije
- Izvor transakcije
- Povezava transakcije

### <a name="transaction-type"></a>Vrsta transakcije

Vrsta transakcije predstavlja čas in kontekst finančnega učinka na projekt. Opredeljuje ga nabor možnosti, ki ima naslednje podprte vrednosti v projektnih operacijah:

- Cena
- Projektna pogodba
- Neobračunana prodaja
- Obračunana prodaja
- Prodaja znotraj organizacije
- Cena enote vira

### <a name="transaction-class"></a>Razred transakcije

Razred transakcije predstavlja različne vrste stroškov, ki nastanejo pri projektih. Opredeljuje ga nabor možnosti, ki ima naslednje podprte vrednosti v projektnih operacijah:

- Čas
- Stroški
- Material
- Dajatev
- Mejnik
- Davek

> [!NOTE]
> The **Mejnik** vrednost običajno uporablja poslovna logika za obračunavanje s fiksno ceno v Project Operations.

### <a name="transaction-origin"></a>Izvor transakcije

Izvor transakcije je entiteta, ki shranjuje izvor vsake poslovne transakcije za pomoč pri poročanju in sledljivosti. Ko se izvedba projekta začne, vsaka poslovna transakcija ustvari drugo poslovno transakcijo, ki bo posledično ustvarila drugo poslovno transakcijo itd.

### <a name="transaction-connection"></a>Povezava transakcije

Transakcijska povezava je entiteta, ki shranjuje razmerje med dvema podobnima poslovnima transakcijama, kot so dejanski stroški in z njimi povezani prodajni stroški ali razveljavitve transakcij, ki jih sprožijo dejavnosti obračunavanja, kot so potrditev računa ali popravki računa.

Entiteti izvor transakcije in povezave transakcije vam skupaj pomagajo slediti Odnosi med poslovnimi transakcijami in dejanji, zaradi katerih je bila ustvarjena določena poslovna transakcija.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
