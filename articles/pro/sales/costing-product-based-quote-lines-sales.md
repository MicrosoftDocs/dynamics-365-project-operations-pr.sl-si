---
title: Podrobnosti ponudb, ki temeljijo na stroškovnih izdelkih
description: Ta tema vsebuje informacije o uveljavljanju lastne cene v vrstici ponudbe, ki temelji na izdelku.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d9c03fa1a8f43cc110565efbafd7f5aba69f65f96bec7f15f2bd492123f639c7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001901"
---
# <a name="costing-product-based-quote-lines"></a>Podrobnosti ponudb, ki temeljijo na stroškovnih izdelkih

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


Podrobnosti ponudb, ki temeljijo na izdelkih, imajo v aplikaciji Dynamics 365 Project Operations tudi polje **Lastna cena**. Polje se uporablja za sledenje lastni ceni izdelka v vrstici ponudbe in za izračune nadaljnje donosnosti.

Ko se za kataloški izdelek ustvari vrstica ponudbe, ki temelji na izdelku, je cena za vrstico samodejno privzeta iz polja **Standardna cena** v katalogu izdelkov. Polje standardne cene v katalogu izdelkov je nastavljeno v osnovni valuti organizacije. Privzeta cena na enoto v vrstici ponudbe, ki temelji na izdelku, se za ponudbo pretvori v valuto prodaje.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Cena na enoto v vrstici ponudbe, ki temelji na izdelku

Namen določitve cene na enoto v vrstici ponudbe, ki temelji na izdelku, je omogočiti različno ceno za izdelek za posamezno prodajo. Tak scenarij sicer ni najbolj običajen, vendar pa včasih dobavitelj zniža ceno izdelka glede na končno stranko.

Na primer:

Družba Fabrikam Robotics namešča robotske roke na montažne trakove korporacije A Datum. Družba Fabrikam izvaja storitve namestitve, robotske roke pa dobavlja družba Trey robotics. Če namestitev robotskih rok za korporacijo A Datum odpre novo navpičnico panoge za družbo Trey robotics, bi ta družba lahko družbi Fabrikam za ta posel priznala poseben popust.

V tem primeru družba Fabrikam za družbo Trey robotics ustvari vrstico ponudbe, ki temelji na izdelku, in za to ponudbo vnese posebno ceno na enoto. Ta cena se razlikujejo od standardne cene družbe Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]