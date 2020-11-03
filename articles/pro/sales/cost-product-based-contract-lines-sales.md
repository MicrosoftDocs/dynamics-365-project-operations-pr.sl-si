---
title: Podrobnosti pogodb, ki temeljijo na stroškovnih izdelkih
description: Ta tema vsebuje informacije o ustvarjanju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/20/2020
ms.locfileid: "4084987"
---
# <a name="costing-product-based-contract-lines"></a>Podrobnosti pogodb, ki temeljijo na stroškovnih izdelkih

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_


Podrobnosti pogodbe na podlagi izdelkov v storitvi Dynamics 365 Project Operations vključujejo polje **Lastna cena** , ki označuje lastno ceno izdelka za izračune nadaljnje donosnosti.

Ko se za kataloški izdelek ustvarijo podrobnosti pogodbe na podlagi izdelka, je cena za podrobnosti pogodbe samodejno privzeta iz polja **Standardna cena** v katalogu izdelkov. Polje **Standardna cena** v katalogu izdelkov je nastavljeno v osnovni valuti organizacije. Ko se stroški na enoto privzamejo iz podrobnosti pogodbe, se pretvorijo v prodajno valuto v pogodbi.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Cena na enoto v podrobnostih pogodbe na podlagi izdelka

Določitev cene na enoto v podrobnostih pogodbe na podlagi izdelka omogoča različno ceno za izdelek za posamezno prodajo enote. Čeprav to ni vedno potrebno, obstajajo določeni scenariji, ko dobavitelj stranki lahko zniža stroške izdelka. Oglejte si ta primer:

Družba Fabrikam Robotics namešča robotske roke na montažne trakove korporacije Adatum. Družba Fabrikam izvaja storitve namestitve, robotske roke pa dobavlja družba Trey Research. Če namestitev robotskih rok za družbo Adatum Corporation odpre novo navpičnico panoge za družbo Trey Research, bi lahko družbi Fabrikam za ta posel priznala poseben popust. V tem primeru Fabrikam ustvari podrobnosti pogodbe na podlagi izdelka za Robotic Arms in vnese stroške na enoto za to pogodbo, ki se razlikujejo od standardnih stroškov robotskih rok družbe Trey Research.
