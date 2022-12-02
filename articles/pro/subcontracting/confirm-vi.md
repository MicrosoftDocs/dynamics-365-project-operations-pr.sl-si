---
title: Potrditev računa dobavitelja za projekt
description: V tem članku je pojasnjeno, kako potrditi račun dobavitelja za projekt v programu Microsoft Dynamics 365 Project Operations in kakšen je finančni učinek potrditve računa dobavitelja za projekt.
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

Ko preverite vse vrstice na računu dobavitelja v programu Microsoft Dynamics 365 Project Operations, lahko z dejanjem »Potrdi« potrdite račun dobavitelja.

Ko izberete možnost **Potrdi** na računu dobavitelja, se zgodi naslednje:

1. Stanje računa dobavitelja se posodobi na **Potrjeno**.
2. Potrjeni račun dobavitelja in z njim povezani zapisi postanejo dostopni samo za branje in jih ni mogoče urejati ali brisati.
3. Če se kateri koli dejanski stroški sklicujejo na vrstico računa dobavitelja kot del postopka ujemanja, so vsi dejanski stroški, ki so povezani z referenčno vrstico računa dobavitelja, stornirani.
4. Novi dejanski stroški se ustvarijo z uporabo informacij v vrstici računa dobavitelja.
5. Ko je račun dobavitelja potrjen, ne morete več ustvarjati popravkov dnevnika, obdelovati preklicanih časovnih vnosov ali preklicati odobritev prvotnega časa, stroškov ali dejanskih vrednosti materiala, ki so stornirane.

> [!NOTE]
> Če ima katera koli vrstica na računu dobavitelja stanje preverjanja, ki ni **Končano**, računa dobavitelja ni mogoče potrditi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
