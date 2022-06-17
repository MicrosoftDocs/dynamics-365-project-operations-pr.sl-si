---
title: Potrditev projektne pogodbe
description: Ta članek vsebuje informacije o potrditvi pogodbe v Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e92dc42c4ff6bdc40c479511c80d3e500df781a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930016"
---
# <a name="confirm-a-project-contract"></a>Potrditev projektne pogodbe

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Projektna pogodba v aplikaciji Dynamics 365 Project Operations je lahko dejavna z razlogom **Potrjeno** ali zaprta z razlogom **Izgubljeno**. Če potrdite projektno pogodbo, se stanje **Osnutek** posodobi na **Aktivno** , razlog stanja pa je možnost **Potrjeno**. Dejavne ali zaprte pogodbe ni mogoče urejati ali znova odpirati. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Finančni vpliv potrditve projektne pogodbe

Ko je projektna pogodba potrjena, bo aplikacija znova izračunala stroške tako, da bo stornirala starejše dejanske vrednosti stroškov in ustvarila nove. Nove dejanske vrednosti stroškov bodo nato obdelane na podlagi metode obračunavanja v povezani podrobnosti pogodbe. Če se dejanske vrednosti stroškov sklicujejo na podrobnost pogodbe »Čas in material«, se v aplikaciji samodejno znova ustvarijo pripadajoče dejanske vrednosti neobračunane prodaje. Če se dejanske vrednosti stroškov sklicujejo na podrobnost pogodbe s fiksno ceno, se v aplikaciji njihova obdelava ustavi.

Omejitve, ki se jih ne sme preseči, nastavitve zaračunljivosti ter cene in stroški dejanskih vrednosti so ocenjeni in nato posodobljeni kot del postopka potrditve.

## <a name="close-a-project-contract-as-lost"></a>Zapiranje projektne pogodbe kot izgubljene

Ko projektno pogodbo zaprete kot izgubljeno, se stanje pogodbe posodobi na **Zaprto**, razlog stanja pa je **Izgubljeno**. Projektna pogodba postane na voljo samo za branje. Pred dokončanjem sprememb se pojavi pogovorno okno za potrditev, saj zaprte projektne pogodbe ni mogoče znova odpreti.

Če se projektna pogodba, ki je zaprta kot izgubljena, v svojih vrsticah sklicuje na projekt, je tudi ta projekt označen kot zaprt. Vse rezervacije virov od tega dne naprej so preklicane. Vse neobračunane dejanske vrednosti prodaje v projektni pogodbi, ki še niso na računu, bodo stornirane.

> [!NOTE]
> Če v aplikaciji Dynamics 365 Project Operations projektno pogodbo zaprete kot izgubljeno, to ne vpliva na stanje povezane priložnosti. Priložnost ostane odprta in jo je treba ročno zapreti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]