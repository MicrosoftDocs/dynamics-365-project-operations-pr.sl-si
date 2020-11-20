---
title: Podrobnosti pogodbe, ki temeljijo na stroškovnih izdelkih – poenostavljena različica
description: Ta tema vsebuje informacije o ustvarjanju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177261"
---
# <a name="cost-product-based-contract-lines---lite"></a>Podrobnosti pogodbe, ki temeljijo na stroškovnih izdelkih – poenostavljena različica

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_


Podrobnosti pogodbe na podlagi izdelkov v storitvi Dynamics 365 Project Operations vključujejo polje **Lastna cena**, ki označuje lastno ceno izdelka za izračune nadaljnje donosnosti.

Ko se za kataloški izdelek ustvarijo podrobnosti pogodbe na podlagi izdelka, je cena za podrobnosti pogodbe samodejno privzeta iz polja **Standardna cena** v katalogu izdelkov. Polje **Standardna cena** v katalogu izdelkov je nastavljeno v osnovni valuti organizacije. Ko se stroški na enoto privzamejo iz podrobnosti pogodbe, se pretvorijo v prodajno valuto v pogodbi.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Cena na enoto v podrobnostih pogodbe na podlagi izdelka

Določitev cene na enoto v podrobnostih pogodbe na podlagi izdelka omogoča različno ceno za izdelek za posamezno prodajo enote. Čeprav to ni vedno potrebno, obstajajo določeni scenariji, ko dobavitelj stranki lahko zniža stroške izdelka. Oglejte si ta primer:

Družba Fabrikam Robotics namešča robotske roke na montažne trakove korporacije Adatum. Družba Fabrikam izvaja storitve namestitve, robotske roke pa dobavlja družba Trey Research. Če namestitev robotskih rok za družbo Adatum Corporation odpre novo navpičnico panoge za družbo Trey Research, bi lahko družbi Fabrikam za ta posel priznala poseben popust. V tem primeru Fabrikam ustvari podrobnosti pogodbe na podlagi izdelka za Robotic Arms in vnese stroške na enoto za to pogodbo, ki se razlikujejo od standardnih stroškov robotskih rok družbe Trey Research.
