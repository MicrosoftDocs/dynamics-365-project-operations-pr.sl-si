---
title: Uspešnost predlogov za račune projekta
description: Ta tema vsebuje informacije o izboljšavah učinkovitosti delovanja predlogov računov za projekte.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269810"
---
# <a name="project-invoice-proposal-performance"></a>Uspešnost predlogov za račune projekta

[!include [banner](../includes/banner.md)]

Ko ustvarite nov predlog računa, lahko naletite na težave z učinkovitostjo delovanja, saj se število projektov in podprojektov poveča. Za izboljšanje učinkovitosti delovanja je na voljo funkcija, ki skrajša čas, potreben za izdelavo novega predloga računa za objavljene transakcije projekta.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Omogočanje izboljšane učinkovitosti delovanja predlogov za račune projekta
Če želite omogočiti funkcijo izboljšanja učinkovitosti delovanja predlogov za račune projekta, izvedite naslednje korake.

1.  Pojdite v **Upravljanje funkcij** > **Vse**. Na seznamu funkcij poiščite **Izboljšanje učinkovitosti delovanja predlogov za račune projekta**.
2.  Izberite **Omogoči zdaj**.
3.  Osvežite brskalnik in ustvarite nov predlog računa.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Izklop izboljšane učinkovitosti delovanja predlogov za račune projekta
Če želite izklopiti izboljšanje učinkovitosti delovanja predlogov za račune projekta, izvedite naslednje korake.

1.  Pojdite v **Upravljanje funkcij** > **Vse**. Na seznamu funkcij poiščite **Izboljšanje učinkovitosti delovanja predlogov za račune projekta**.
2.  Izberite **Onemogoči**.
3.  Osvežite brskalnik.

> [!NOTE]
> Uspešnost predloga za račun ne more biti uporabljena, ko so pravila za izstavitev računa onemogočena.
> 
> Med paketno obdelavo za ustvarjanje predloga za račun bodo številna podopravila, ne glede na to, kaj ste vnesli, na podlagi števila pogodb s transakcijami, ki se zaračunajo, opravila razdelila na največje možno število opravil. Če označite, da serija zajema **3** podopravila za ustvarjanje predloge za račun, obstajata pa samo dve pogodbi s transakcijami, za katere se lahko izda račun, bosta ustvarjeni samo dve podopravili.
