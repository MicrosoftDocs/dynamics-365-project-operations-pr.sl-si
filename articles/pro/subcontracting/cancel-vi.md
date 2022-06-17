---
title: Preklic računa dobavitelja za projekt
description: Ta članek pojasnjuje, kako preklicati račun dobavitelja projekta v Microsoftu Dynamics 365 Project Operations in finančni učinek preklica računa prodajalca projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911570"
---
# <a name="cancel-a-project-vendor-invoice"></a>Preklic računa dobavitelja za projekt

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ko je račun prodajalca potrjen, ga ni mogoče urejati ali izbrisati. Če je prišlo do napake na računu prodajalca, ki je bil potrjen, lahko uporabite dejanje Prekliči, da razveljavite vpliv računa prodajalca in ustvarite nov račun prodajalca.

Ko izberete **Prekliči** na računu prodajalca se zgodi naslednje vedenje:

1. Stanje računa prodajalca je posodobljeno na **Prekinjeno**.
2. Preklicani račun prodajalca in z njim povezani zapisi postanejo samo za branje in jih ni mogoče urejati ali izbrisati.
3. Vsi dejanski stroški, ki so bili ustvarjeni na podlagi vrstic računa prodajalca kot del potrditve računa prodajalca, se razveljavijo.
4. Če so bili kakršni koli dejanski stroški povezani z vrsticami računa prodajalca kot del postopka ujemanja, jih je izvirna potrditev računa prodajalca razveljavila. Med preklicem računa prodajalca se ti dejanski stroški ponovno ustvarijo. Izvor kaže na vnose časa, stroškov ali porabe materiala.
5. Ko je račun prodajalca preklican, lahko znova ustvarite dnevnik popravkov, obdelate odpoklice vnosa časa in prekličete odobritev prvotnih dejanskih časov, stroškov ali materiala.

> [!NOTE]
> Preklicati je mogoče samo potrjene račune dobavitelja projekta. Računov prodajalcev v drugih državah ni mogoče preklicati.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
