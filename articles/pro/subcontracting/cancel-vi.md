---
title: Preklic računa dobavitelja za projekt
description: V tem članku je pojasnjeno, kako preklicati račun dobavitelja za projekt v programu Microsoft Dynamics 365 Project Operations, in finančni učinek preklica računa dobavitelja za projekt.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261111"
---
# <a name="cancel-a-project-vendor-invoice"></a>Preklic računa dobavitelja za projekt

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Po potrditvi računa dobavitelja, računa ni mogoče urediti ali ga izbrisati. Če je prišlo do napake na računu dobavitelja, ki je bil potrjen, lahko uporabite dejanje »Prekliči«, da razveljavite vpliv računa dobavitelja in ustvarite nov račun dobavitelja.

Ko izberete možnost **Prekliči** na računu dobavitelja, se zgodi naslednje:

1. Stanje računa dobavitelja se posodobi na **Preklicano**.
2. Preklicani račun dobavitelja in z njim povezani zapisi postanejo dostopni samo za branje in jih ni mogoče urejati ali brisati.
3. Morebitni dejanski stroški, ki so bili ustvarjeni na podlagi vrstic računa dobavitelja kot del potrditve računa dobavitelja, se razveljavijo.
4. Če so bili kakršni koli dejanski stroški povezani z vrsticami računa dobavitelja kot del postopka ujemanja, jih je izvirna potrditev računa dobavitelja razveljavila. Med preklicevanjem računa dobavitelja se ti dejanski stroški ponovno ustvarijo. Izvor kaže na vnose časa, stroškov ali porabe materiala.
5. Ko je račun dobavitelja preklican, lahko znova ustvarite popravke dnevnika, obdelate preklicane časovne vnose in prekličete odobritev prvotnega časa, stroškov ali dejanskih vrednosti materiala.

> [!NOTE]
> Preklicati je mogoče samo potrjene račune dobavitelja za projekt. Računov dobaviteljev iz drugih držav ni mogoče preklicati.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
