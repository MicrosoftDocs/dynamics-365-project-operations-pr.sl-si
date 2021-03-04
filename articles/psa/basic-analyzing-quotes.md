---
title: Analiza ponudb za projekte
description: Ta tema vsebuje informacije o analizi ponudb za projekte.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 361a940261811467c46222c3d58c9504434ec882
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145243"
---
# <a name="analysis-of-project-quotes"></a>Analiza ponudb za projekte

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation analizira ponudbe za projekte, da lahko oceni dobičkonosnost. Analizira tudi, kako dobro je ponudba usklajena s pričakovanji kupcev o datumu dostave ali datum zaključka, in o proračunu.

## <a name="profitability-analysis"></a>Analiza dobičkonosnosti

Project Service Automation analizira dobičkonosnost tako, da uporabi stopnjo bruto dobička in prilagojeno stopnjo bruto dobička.

- Stopnja bruto dobička se izračuna z naslednjo formulo:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Prilagojena stopnja bruto dobička se izračuna z naslednjo formulo:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Če se vrednosti za stopnjo bruto dobička in prilagojeno stopnjo bruto dobička precej razlikujeta, je veliko dela v ponudbi razvrščeno delo, ki se ne zaračuna.

## <a name="analysis-of-customer-expectations"></a>Analiza pričakovanj strank

Ponudbe lahko analizirate in ustvarite grafikone pričakovanj strank v zvezi z razporedom in proračunom.

- Polje **Zahtevani datum dostave** v glavi ponudbe
- Polje **Proračun stranke** za vsako vrstico ponudbe (za vrstice, ki temeljijo na projektih, in vrstice, ki temeljijo na izdelkih)

Analiza pričakovanj strank glede razporeda se izvede s primerjavo najnovejšega končnega datuma podrobnosti vrstice ponudbe z zahtevanim datumom dostave v vseh vrsticah ponudbe v ponudbi.

Analiza pričakovanj strank v zvezi s proračunom se izvede s primerjavo vsote celotnega proračuna kupca z zneskom za ponudbo v vseh vrsticah ponudbe.


[!INCLUDE[footer-include](../includes/footer-banner.md)]