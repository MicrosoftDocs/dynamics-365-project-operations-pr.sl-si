---
title: Potrditev računa dobavitelja za projekt
description: V tem članku je razloženo, kako potrdite račun dobavitelja projekta v Microsoftu Dynamics 365 Project Operations in finančni učinek potrditve računa prodajalca projekta.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932454"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potrditev računa dobavitelja za projekt

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
