---
title: Analiza ponudb za projekte
description: Ta tema vsebuje informacije o analizi ponudb za projekte.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755737"
---
# <a name="analysis-of-project-quotes"></a>Analiza ponudb za projekte

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
