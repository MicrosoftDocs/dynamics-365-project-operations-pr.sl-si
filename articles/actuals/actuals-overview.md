---
title: Dejanske vrednosti
description: Ta članek vsebuje informacije o delu z dejanskimi vrednostmi v aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924818"
---
# <a name="actuals"></a>Dejanske vrednosti

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Dejanske vrednosti predstavljajo pregledane in odobrene finančne in časovne napredke projekta. Ustvarijo se, ko so odobreni čas, strošek, vnosi porabe materiala, vknjižbe in računi.

> [!IMPORTANT]
> Dejanskih vrednosti ne smete urejati ali jih brisati iz sistema. V nasprotnem primeru bi to lahko negativno vplivalo na finančno integriteto in kakršno koli integracijo z drugimi finančnimi in računovodskimi sistemi. Microsoft Dynamics 365 Project Operations omogoča uporabo storniranja in zamenjave dejanskih vrednosti za urejanje dejanskih vrednosti na različnih točkah življenjskega cikla poslovnega procesa vaših projektov.

## <a name="recording-actuals-based-on-project-events"></a>Zapisovanje dejanskih podatkov na podlagi projektnih dogodkov

Aplikacija Project Operations beleži finančne transakcije, ki se v življenjskem ciklu projektne interakcije pojavijo kot dejanske vrednosti. Ustvarjanje dejanskih vrednosti ob različnih dogodkih v življenjskem ciklu se razlikuje glede na to, ali projektna interakcija uporablja model obračunavanja časa in materiala ali model obračunavanja po fiksni ceni in ali je v fazi predprodaje ali je interni projekt.

Naslednji članki pojasnjujejo vpliv na tabelo »Dejanske vrednosti« ob različnih dogodkih za različne različice:

- [Vpliv dejanskih vrednosti pri interakciji časa in materialov](ActualsonTM.md)
- [Vpliv dejanskih vrednosti pri interakciji s fiksno ceno](ActualonFP.md)
- [Vpliv dejanskih vrednosti med fazo predprodaje interakcije](ActualonPreSales.md)
- [Vpliv dejanskih vrednosti na interni projekt](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
