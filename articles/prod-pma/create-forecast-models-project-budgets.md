---
title: Ustvarjanje modelov napovedi za proračune projektov
description: Ta tema opisuje, kako ustvariti model napovedi za preostale proračune.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084892"
---
# <a name="create-forecast-models-for-project-budgets"></a>Ustvarjanje modelov napovedi za proračune projektov 

[!include [banner](../includes/banner.md)]

Ta tema opisuje, kako ustvariti model napovedi za preostale proračune. Projekt, ki je podrejen proračunskemu nadzoru, uporablja dve vrsti proračuna: prvotni in preostali proračun. Ko ustvarite proračun projekta, morate navesti model napovedi prvotnega in preostalega proračuna, ki sta bila ustvarjena na strani **Modeli napovedi**. Proračuni projektov, ki temeljijo na določenih modelih, se ustvarijo, ko potrdite proračun projekta.

> [!NOTE]
> Model napovedi, ki se uporablja za nadzor proračuna, ne more imeti podmodela ali biti uporabljen kot podmodel.

1. Izberite **Vodenje projektov in računovodstvo** > **Nastavitev** > **Napovedi**  > **Modeli napovedi**.
2. Izberite **Novo** , da ustvarite nov model napovedi in nato vnesite ID številko modela in ime novega modela. 
3. Nastavite možnost **Ustavljeno** na **Da** , da preprečite kakršne koli spremembe vrstic napovedi za model napovedi. 
4. Če bi želeli, da vrstice napovedi, s katerimi je povezan model, generirajo napovedi denarnih tokov v glavni knjigi, nastavite **Vključi v napovedi denarnih tokov** na **Da.** 
5. Če želite datum projekta uporabiti kot datum računa, nastavite **Napovedani datum računa** na **Da**. 
6. V polju **Vrsta proračuna** izberite eno od naslednjih vrst modelov:

   - **Prvotni proračun** : uporabite prvotne zneske proračuna, ki so vneseni, ko je začetni proračun ustvarjen in odobren.
   - **Preostali proračun** : uporabite preostale proračunske zneske v času trajanja projekta. Stanja v tem modelu napovedi se zmanjšajo za dejanske transakcije in povečajo ali zmanjšajo s popravki proračuna.
   - **Prenos naprej** : uporabite zneske prenosa proračuna za projekt. Prenos naprej je neobvezen postopek, ki ga je mogoče zagnati za prenos neuporabljenih proračunskih zneskov iz enega proračunskega leta v drugega.

7. Po potrebi nastavite naslednje možnosti:

   - Omogočite **Napovedani datum računa** , če želite datum projekta uporabiti kot datum računa.
   - Omogočite **Napoved z WIP** za napovedovanje na podlagi dela v teku (WIP) in nato izberite vrsto WIP. 
   - Privzeta možnost **Vrsta proračuna** lahko ostane **Brez** , sicer vnesite novo vrsto. Po spremembi zapisa ni mogoče spremeniti vrste proračuna.     
    > [!NOTE]
    > Če spremenite privzeto vrsto proračuna, druge možnosti ne bodo na voljo za posodobitev in tega modela napovedi ne boste mogli ponovno uporabiti. 
   


 

