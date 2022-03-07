---
title: Ustvarjanje predloge delovnih ur
description: V tej temi so opisana navodila za ustvarjanje predloge delovnih ur v storitvi Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 90525cf1e7cd487a03b064466ad1b13f8afb7819443fc4bacf9c7d3eee86f0b6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987411"
---
# <a name="create-a-work-hours-template-project-service"></a>Ustvarjanje predloge delovnih ur (rešitev Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Če želite ustvariti projekt in ga upravljati, morate za projekt uporabiti predlogo koledarja. Predloga koledarja opredeljuje naslednje atribute projekta:

- Delovni čas, vključno z začetnim in končnim časom
- Delovni dnevi
- Izjeme v koledarju, kot so prosti dnevi

Predloga koledarja, ki se uporablja za projekt, je kopija predloge koledarja, določene v nastavitvah vaše organizacije.

> [!NOTE]
> Če spremenite predlogo koledarja, se te spremembe ne bodo razširile na delovni čas projekta. Za spremembo delovnega časa projekta je treba uporabiti novo predlogo.

Če želite ustvariti predlogo koledarja za svojo organizacijo, je treba upoštevati ključni zahtevi:

- Določite želeni delovni čas predloge z novim ali obstoječim virom, ki ga je mogoče rezervirati.
- Ustvarite novo predlogo koledarja in jo povežite z virom, ki ga je mogoče rezervirati.

**Določanje delovnega časa predloge**

1. Odprite možnost **Viri** \> **Viri**.
2. Ustvarite nov vir za sklicevanje v predlogi koledarja ali izberite obstoječega.
3. Izberite zavihek **Delovni čas** vira in upoštevajte navodila v članku [Nastavitev delovnih ur za vir](/dynamics365/field-service/set-work-hours-resource.md), da konfigurirate pravila koledarja.

**Ustvarjanje nove predloge koledarja**

1. Odprite razdelek **Nastavitve** \> **Predloga koledarja**.
2. Izberite možnost **Novo** in vnesite ime, opis in vir predloge.


> [!NOTE]
> Ko je vir naveden v predlogi koledarja, je kopija koledarja vira povezana s predlogo koledarja. Če se delovni časi kopije predloge spremenijo, se te spremembe ne bodo razširile na predlogo projekta.


### <a name="see-also"></a>Glejte tudi  
 [Nastavitev virov](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
