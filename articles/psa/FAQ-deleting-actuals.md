---
title: Zakaj ne morem izbrisati zapisov iz entitete opravljenega dela?
description: V tej temi so na voljo informacije o tem, zakaj ne morete izbrisati zapisov iz entitete opravljenega dela.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d60a3586fd1f0f688bcd2626d039ebc1aa6b0925c90d676f0e716400d8e8d6dd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002891"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Zakaj ne morem izbrisati zapisov iz entitete »Opravljeno delo«?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ne omogoča brisanja opravljenega dela, ker služi kot dokaz za transakcije, ki imajo finančne posledice za sisteme iz strežnika, na primer glavno knjigo. Če bi se opravljeno delo lahko izbrisalo, bi bila celovitost transakcij v finančnih poročilih lahko vprašljiva. Stranke lahko uporabijo dnevnike, da ustvarijo transakcije, in tako vzpostavijo nadzorno sled.



[!INCLUDE[footer-include](../includes/footer-banner.md)]