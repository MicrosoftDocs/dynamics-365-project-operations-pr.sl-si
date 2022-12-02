---
title: Zakaj ne morem izbrisati zapisov iz entitete opravljenega dela?
description: V tem članku so na voljo informacije o tem, zakaj ne morete izbrisati zapisov iz entitete opravljenega dela.
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
ms.openlocfilehash: bd446961432a8f18895db45699d7a731d55235b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925600"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Zakaj ne morem izbrisati zapisov iz entitete »Opravljeno delo«?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ne omogoča brisanja opravljenega dela, ker služi kot dokaz za transakcije, ki imajo finančne posledice za sisteme iz strežnika, na primer glavno knjigo. Če bi se opravljeno delo lahko izbrisalo, bi bila celovitost transakcij v finančnih poročilih lahko vprašljiva. Stranke lahko uporabijo dnevnike, da ustvarijo transakcije, in tako vzpostavijo nadzorno sled.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
