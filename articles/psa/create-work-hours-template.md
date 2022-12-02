---
title: Ustvarjanje predloge delovnih ur
description: V tem članku so opisana navodila za ustvarjanje predloge delovnih ur v storitvi Project Service.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f3ac17a29e79f86f7c3ce127edb4b02ca63ea04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916078"
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
3. Izberite zavihek **Delovni čas** vira in upoštevajte navodila v članku [Nastavitev delovnih ur za vir](/dynamics365/field-service/set-work-hours-resource), da konfigurirate pravila koledarja.

**Ustvarjanje nove predloge koledarja**

1. Odprite razdelek **Nastavitve** \> **Predloga koledarja**.
2. Izberite možnost **Novo** in vnesite ime, opis in vir predloge.


> [!NOTE]
> Ko je vir naveden v predlogi koledarja, je kopija koledarja vira povezana s predlogo koledarja. Če se delovni časi kopije predloge spremenijo, se te spremembe ne bodo razširile na predlogo projekta.


### <a name="see-also"></a>Glejte tudi  
 [Nastavitev virov](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
