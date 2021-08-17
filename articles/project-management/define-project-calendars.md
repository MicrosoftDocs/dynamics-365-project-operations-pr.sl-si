---
title: Določitev koledarjev projektov
description: Ta tema vsebuje informacije o tem, kako uporabiti predlogo koledarja v projektu za sledenje razporedu projekta.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 181032b27ee67591a3bb40ab080477c51c1e34a46e9aac20039e4e5df3a5ab1d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000956"
---
# <a name="define-project-calendars"></a>Določitev koledarjev projektov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

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

Delovno predlogo lahko zdaj povežete s predlogo koledarja projekta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

