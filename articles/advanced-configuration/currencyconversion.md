---
title: Nastavite pretvorbo valut za izračun prodajnih cen iz stroškovnih stopenj
description: V tem članku je razloženo, kako konfigurirati vedenje pretvorbe valut, ki bo uporabljeno v Microsoftu Dynamics 365 Project Operations ko se prodajne transakcije ustvarijo iz stroškovnih transakcij.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816701"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Nastavite pretvorbo valut za izračun prodajnih cen iz stroškovnih stopenj

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

V Microsoftu Dynamics 365 Project Operations je mogoče prodajne cene za kategorije stroškov nastaviti kot številske vrednosti ali pa jih nastaviti tako, da se izračunajo na podlagi nastalih stroškov.

Ko so nastavljeni za izračun na podlagi nastalih stroškov, so na voljo naslednje možnosti:

- Nabavna cena
- Odstotek pribitka nad ceno

V scenarijih, kjer strošek odhodka nastane v valuti, ki se razlikuje od prodajne valute za projektno pogodbo, je potrebna pretvorba valute za izračun prodajne cene na podlagi stroškov.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Obnašanje pretvorbe valut, ki uporablja izvorne Dataverse menjalne tečaje

Project Operations privzeto uporablja menjalne tečaje valut, ki so shranjeni v tabeli valut v Dataverse. Če želite konfigurirati Project Operations za uporabo domačih menjalnih tečajev za izračun prodajnih cen iz stroškov, sledite tem korakom.

1. Pojdite na **Operacije projekta \> Nastavitve \> Parametri**.
1. Odprite stran s podrobnostmi **Project Parameter** .
1. Nastavite polje **Logika pretvorbe valut** na prazno vrednost.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Vedenje pretvorbe valut, ki uporablja menjalne tečaje iz aplikacij za finance in poslovanje

Menjalni tečaji v tabeli valut, ki so izvorno na voljo v Dataverse niso veljavni na datum. Zato morda niso vedno prilagojene zahtevam, ki jih imate za izračun prodajnih cen iz stroškovnih stopenj.

Za izračun prodajne cene v prodajni valuti iz stroškovne stopnje v stroškovni valuti lahko uporabite menjalne tečaje iz okolja financ in operacij. Če želite konfigurirati to vedenje pretvorbe valut, sledite tem korakom.

1. Na strani **Parametri projekta** dodajte polje **Logika pretvorbe valut** . Nato shranite in objavite prilagoditev.
1. Pojdite na **Operacije projekta \> Nastavitve \> Parametri**.
1. Odprite stran s podrobnostmi **Project Parameter** . 
1. Nastavite polje **Vedenje pretvorbe valut** na **Razširjeno z nadomestno vrednostjo na privzeto**.
1. Dajte **uporabniku aplikacije za dvojno pisanje** varnostna vloga **Globalno branje** dovoljenje za naslednje tabele:

    - msdyn\_ menjalnice
    - msdyn\_ currencyexchangeratepairs
    - msdyn\_ exchangeratetypes

1. V svojem finančnem in operativnem okolju zaženite naslednje zemljevide dvojnega pisanja z začetno sinhronizacijo:

    - Vrsta menjalnega tečaja (msdyn\_ exchangeratetypes)
    - Valutni par menjalnega tečaja (msdyn\_ currencyexchangeratepairs)
    - Menjalni tečaji CDS (msdyn\_ currencyexchangerates)

Ko so te spremembe končane, bodo z dvojnim zapisovanjem menjalni tečaji iz okolja financ in operacij na voljo v Dataverse. Projektne operacije bodo nato uporabile te menjalne tečaje za pretvorbo stroškov v prodajno valuto pogodbe.

> [!NOTE]
> To vedenje pretvorbe valut velja samo za izračun prodajnih cen iz stroškovnih stopenj. Ne bo uporabljen za splošen izračun vrednosti osnovne valute. Vrednosti osnovne valute bodo vedno uporabljale domače Dataverse menjalne tečaje, ne glede na to, ali dokončate ta postopek.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
