---
title: Potrdite račun dobavitelja projekta
description: Ta tema pojasnjuje, kako potrditi račun dobavitelja projekta v Microsoftu Dynamics 365 Project Operations in finančni učinek potrditve računa prodajalca projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595748"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potrdite račun dobavitelja projekta

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ko preverite vse vrstice na računu prodajalca v Microsoftu Dynamics 365 Project Operations, lahko uporabite dejanje Potrdi za potrditev računa prodajalca.

Ko izberete **Potrdi** na računu prodajalca se zgodi naslednje vedenje:

1. Stanje računa prodajalca je posodobljeno na **Potrjeno**.
2. Potrjeni račun prodajalca in z njim povezani zapisi postanejo samo za branje in jih ni mogoče urejati ali izbrisati.
3. Če se kateri koli dejanski stroški sklicujejo na vrstico računa prodajalca kot del postopka ujemanja, se vsi dejanski stroški, ki so povezani z referenčno vrstico računa prodajalca, obrnejo.
4. Novi dejanski stroški se ustvarijo z uporabo informacij v vrstici računa prodajalca.
5. Ko je račun prodajalca potrjen, ne morete več ustvarjati dnevnikov popravkov, obdelovati odpoklic vnosov časa ali preklicati odobritev prvotnega časa, stroškov ali materialnih dejanskih dejstev, ki so bili stornirani.

> [!NOTE]
> Če ima katera koli vrstica na računu prodajalca status preverjanja, ki ni **Dokončano**, računa prodajalca ni mogoče potrditi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
