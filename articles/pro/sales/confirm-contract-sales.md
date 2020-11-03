---
title: Potrditev projektne pogodbe
description: Ta tema vsebuje informacije o tem, kako se v aplikaciji Project Operations potrdi pogodbo.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084876"
---
# <a name="confirm-a-project-contract"></a>Potrditev projektne pogodbe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V aplikacij Dynamics 365 Project Operations je projektna pogodba lahko dejavna z razlogom stanja **Potrjeno** ali zaprta z razlogom stanja **Izgubljeno**. Če potrdite projektno pogodbo, se stanje **Osnutek** posodobi na **Aktivno** , razlog stanja pa je možnost **Potrjeno**. Dejavne ali zaprte pogodbe ni mogoče urejati ali znova odpirati. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Finančni vpliv potrditve projektne pogodbe

Ko je projektna pogodba potrjena, bo aplikacija znova izračunala stroške tako, da bo stornirala starejše dejanske vrednosti stroškov in ustvarila nove. Nove dejanske vrednosti stroškov bodo nato obdelane na podlagi metode obračunavanja v povezani podrobnosti pogodbe. Če se dejanske vrednosti stroškov sklicujejo na podrobnost pogodbe »Čas in material«, se v aplikaciji samodejno znova ustvarijo pripadajoče dejanske vrednosti neobračunane prodaje. Če se dejanske vrednosti stroškov sklicujejo na podrobnost pogodbe s fiksno ceno, se v aplikaciji njihova obdelava ustavi.

Omejitve, ki se jih ne sme preseči, nastavitve zaračunljivosti ter cene in stroški dejanskih vrednosti so ocenjeni in nato posodobljeni kot del postopka potrditve.

## <a name="close-a-project-contract-as-lost"></a>Zapiranje projektne pogodbe kot izgubljene

Ko projektno pogodbo zaprete kot izgubljeno, se stanje pogodbe posodobi na **Zaprto** , razlog stanja pa je **Izgubljeno**. Projektna pogodba postane na voljo samo za branje. Pred dokončanjem sprememb se pojavi pogovorno okno za potrditev, saj zaprte projektne pogodbe ni mogoče znova odpreti.

Če se projektna pogodba, ki je zaprta kot izgubljena, v svojih vrsticah sklicuje na projekt, je tudi ta projekt označen kot zaprt. Vse rezervacije virov od tega dne naprej so preklicane. Vse neobračunane dejanske vrednosti prodaje v projektni pogodbi, ki še niso na računu, bodo stornirane.

> [!NOTE]
> Zapiranje projektne pogodbe v programu Dynamics 365 Project Operations kot izgubljene, ne bo vplivalo na stanje z njo povezane priložnosti. Priložnost ostane odprta in jo je treba ročno zapreti.
