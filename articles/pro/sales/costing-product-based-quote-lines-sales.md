---
title: Podrobnosti ponudb, ki temeljijo na stroškovnih izdelkih
description: Ta tema vsebuje informacije o uveljavljanju lastne cene v vrstici ponudbe, ki temelji na izdelku.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906334"
---
# <a name="costing-product-based-quote-lines"></a>Podrobnosti ponudb, ki temeljijo na stroškovnih izdelkih

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


Vrstice ponudb, ki temeljijo na izdelku, imajo v aplikaciji Dynamics 365 Project Operations tudi polje za **lastno ceno**. Polje se uporablja za sledenje lastni ceni izdelka v vrstici ponudbe in za izračune nadaljnje donosnosti.

Ko se za kataloški izdelek ustvari vrstica ponudbe, ki temelji na izdelku, je cena za vrstico samodejno privzeta iz polja **Standardna cena** v katalogu izdelkov. Polje standardne cene v katalogu izdelkov je nastavljeno v osnovni valuti organizacije. Privzeta cena na enoto v vrstici ponudbe, ki temelji na izdelku, se za ponudbo pretvori v valuto prodaje.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Cena na enoto v vrstici ponudbe, ki temelji na izdelku

Namen določitve cene na enoto v vrstici ponudbe, ki temelji na izdelku, je omogočiti različno ceno za izdelek za posamezno prodajo. Tak scenarij sicer ni najbolj običajen, vendar pa včasih dobavitelj zniža ceno izdelka glede na končno stranko.

Na primer:

Družba Fabrikam Robotics namešča robotske roke na montažne trakove korporacije A Datum. Družba Fabrikam izvaja storitve namestitve, robotske roke pa dobavlja družba Trey robotics. Če namestitev robotskih rok za korporacijo A Datum odpre novo navpičnico panoge za družbo Trey robotics, bi ta družba lahko družbi Fabrikam za ta posel priznala poseben popust.

V tem primeru družba Fabrikam za družbo Trey robotics ustvari vrstico ponudbe, ki temelji na izdelku, in za to ponudbo vnese posebno ceno na enoto. Ta cena se razlikujejo od standardne cene družbe Trey Robotic Arms.
