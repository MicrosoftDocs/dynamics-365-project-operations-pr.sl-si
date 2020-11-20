---
title: Zakaj ne morem izbrisati zapisov iz entitete opravljenega dela?
description: V tej temi so na voljo informacije o tem, zakaj ne morete izbrisati zapisov iz entitete opravljenega dela.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127178"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="52a01-103">Zakaj ne morem izbrisati zapisov iz entitete »Opravljeno delo«?</span><span class="sxs-lookup"><span data-stu-id="52a01-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="52a01-104">Project Service Automation (PSA) ne omogoča brisanja opravljenega dela, ker služi kot dokaz za transakcije, ki imajo finančne posledice za sisteme iz strežnika, na primer glavno knjigo.</span><span class="sxs-lookup"><span data-stu-id="52a01-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="52a01-105">Če bi se opravljeno delo lahko izbrisalo, bi bila celovitost transakcij v finančnih poročilih lahko vprašljiva.</span><span class="sxs-lookup"><span data-stu-id="52a01-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="52a01-106">Stranke lahko uporabijo dnevnike, da ustvarijo transakcije, in tako vzpostavijo nadzorno sled.</span><span class="sxs-lookup"><span data-stu-id="52a01-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

