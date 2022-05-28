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
ms.reviewer: johnmichalak
ms.openlocfilehash: ff2c951905324d5d05722f399057c03d22f1a1c9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584432"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Zakaj ne morem izbrisati zapisov iz entitete »Opravljeno delo«?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ne omogoča brisanja opravljenega dela, ker služi kot dokaz za transakcije, ki imajo finančne posledice za sisteme iz strežnika, na primer glavno knjigo. Če bi se opravljeno delo lahko izbrisalo, bi bila celovitost transakcij v finančnih poročilih lahko vprašljiva. Stranke lahko uporabijo dnevnike, da ustvarijo transakcije, in tako vzpostavijo nadzorno sled.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
