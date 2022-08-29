---
title: Potrditev računa dobavitelja za projekt
description: V tem članku je razloženo, kako potrditi račun prodajalca projekta v Microsoftu Dynamics 365 Project Operations in finančni učinek potrditve računa prodajalca projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261533"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potrditev računa dobavitelja za projekt

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Potem ko ste v Microsoftu preverili vse vrstice na računu dobavitelja Dynamics 365 Project Operations, lahko uporabite dejanje Potrdi, da potrdite račun dobavitelja.

Ko izberete **Potrdi** na računu prodajalca se zgodi naslednje:

1. Stanje računa dobavitelja se posodobi na **Potrjeno**.
2. Potrjeni račun dobavitelja in z njim povezani zapisi postanejo samo za branje in jih ni mogoče urejati ali brisati.
3. Če se kateri koli dejanski stroški sklicujejo na vrstico računa dobavitelja kot del postopka ujemanja, so vsi dejanski stroški, ki so povezani z referenčno vrstico računa dobavitelja, obrnjeni.
4. Novi dejanski stroški se ustvarijo z uporabo informacij v vrstici računa dobavitelja.
5. Ko je račun dobavitelja potrjen, ne morete več ustvarjati dnevnikov popravkov, odpoklica vnosa časa obdelave ali preklicati odobritve prvotnega časa, stroškov ali materialnih dejanskih vrednosti, ki so bile razveljavljene.

> [!NOTE]
> Če ima katera koli vrstica na računu dobavitelja status preverjanja, ki ni **Popolna**, računa dobavitelja ni mogoče potrditi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
