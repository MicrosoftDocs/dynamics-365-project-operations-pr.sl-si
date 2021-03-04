---
title: Podrobnosti pogodbe, ki temeljijo na stroškovnih izdelkih – poenostavljena različica
description: Ta tema vsebuje informacije o ustvarjanju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764479"
---
# <a name="cost-product-based-contract-lines---lite"></a>Podrobnosti pogodbe, ki temeljijo na stroškovnih izdelkih – poenostavljena različica

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_


Podrobnosti pogodbe, ki temeljijo na izdelkih, v aplikaciji Dynamics 365 Project Operations vključujejo polje **Lastna cena**, ki shranjuje lastno ceno izdelka za nadaljnje izračune donosnosti.

Ko se za izdelek v katalogu ustvarijo podrobnosti pogodbe, ki temeljijo na izdelkih, se cena v vrstici v katalogu izdelkov ponastavi iz polja **Standardni stroški**. Polje **Standardna cena** v katalogu izdelkov je nastavljeno v osnovni valuti organizacije. Ko se stroški na enoto privzamejo iz podrobnosti pogodbe, se pretvorijo v prodajno valuto v pogodbi.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Cena na enoto v podrobnostih pogodbe na podlagi izdelka

Določitev cene na enoto v podrobnostih pogodbe na podlagi izdelka omogoča različno ceno za izdelek za posamezno prodajo enote. Čeprav to ni vedno potrebno, obstajajo določeni scenariji, ko dobavitelj stranki lahko zniža stroške izdelka. Oglejte si ta primer:

Družba Fabrikam Robotics namešča robotske roke na montažne trakove korporacije Adatum. Fabrikam ponuja storitve namestitve, toda robotske roke izdeluje podjetje Trey Research. Če namestitev robotskih rok za družbo Adatum Corporation odpre novo navpičnico panoge za družbo Trey Research, bi lahko družbi Fabrikam za ta posel priznala poseben popust. V tem primeru Fabrikam za Robotics Arms ustvari podrobnosti pogodbe, ki temeljijo na izdelku. Za to pogodbo se vnese cena na enoto. Cena se razlikuje od cene robotskih rok podjetja Trey Research.
