---
title: Potrditev računov dobavitelja za projekt
description: V tem članku je pojasnjeno, kako potrditi račun dobavitelja za projekt v programu Microsoft Dynamics 365 Project Operations, in opisano, kakšen je finančni učinek potrditve računa dobavitelja za projekt.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475490"
---
# <a name="confirm-project-vendor-invoices"></a>Potrditev računov dobavitelja za projekt

**Velja za**: za scenarije v aplikaciji Project Operations, ki temeljijo na virih/nezalogi

Ko je omogočen parameter **Potrebna je ročna potrditev vodje projekta**, imajo računi dobavitelja, ki so ustvarjeni v Microsoft Dataverse, stanje **Osnutek**. Tako oblikovane račune dobaviteljev je treba pregledati in ročno potrditi. Ko je parameter **Potrebna je ročna potrditev vodje projekta** onemogočen, so računi dobavitelja, ki so ustvarjeni v Dataverse, samodejno potrjeni. Nadaljnja dejanja niso potrebna. 

Ko preverite vse vrstice na računu dobavitelja v aplikaciji Dynamics 365 Project Operations, izberite možnost **Potrdi** za potrditev računa dobavitelja.

Ko izberete možnost **Potrdi** na računu dobavitelja, se zgodi naslednje:

1. Stanje računa dobavitelja se posodobi na **Potrjeno**.
1. Potrjeni račun dobavitelja in z njim povezani zapisi postanejo dostopni samo za branje in jih ni mogoče urejati ali brisati.
1. Če se kateri koli dejanski stroški sklicujejo na vrstico računa dobavitelja kot del postopka ujemanja, so vsi dejanski stroški, ki so povezani z referenčno vrstico računa dobavitelja, stornirani.
1. Novi dejanski stroški se ustvarijo z uporabo informacij v vrstici računa dobavitelja.
1. Ne morete več ustvarjati popravkov dnevnika, obdelovati preklicanih časovnih vnosov ali preklicati odobritve prvotnega časa, stroškov ali dejanskih vrednosti materiala, ki so bile stornirane.
1. V aplikaciji Dynamics 365 Finance se vrednost **Stroški projekta** posodobi z uporabo dnevnika integracij projekta, račun za integracijo naročil pa je po objavi dnevnika integracij projekta *storniran*.

> [!NOTE]
> Če ima katera koli vrstica na računu dobavitelja stanje preverjanja, ki ni **Končano**, računa dobavitelja ni mogoče potrditi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
