---
title: Nastavitev potekov dela za upravljanje stroškov
description: Nastavite lahko proces poteka dela, ki se uporablja za pregled in odobritev dokumentov glede poti in stroškov.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084783"
---
# <a name="set-up-workflows-for-expense-management"></a>Nastavitev potekov dela za upravljanje stroškov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Nastavite lahko proces poteka dela za pregled in odobritev dokumentov glede poti in stroškov. Opredelite lahko poteke dela za poročila o stroških, zahteve za pot in zahteve za denarne predujme.

Potek dela predstavlja poslovni proces in določa, kako dokument teče skozi sistem. Potek dela tudi označuje, kdo mora dokončati opravilo ali odobriti dokument. Uporaba sistema poteka dela v vaši organizaciji ima več prednosti:

- **Dosledni procesi** : določite lahko postopek odobritve za določene dokumente, na primer zahteve za nakup in poročila o stroških. Uporaba sistema poteka dela pomaga zagotoviti dosledno in učinkovito obdelavo in odobritev dokumentov.
- **Vidljivost procesa** : sledite lahko meritvam stanja, zgodovine in uspešnosti določenega primerka poteka dela. To vam pomaga določiti, ali bi bilo treba potek dela spremeniti za izboljšanje učinkovitosti.
- **Centraliziran delovni seznam** : uporabniki si lahko ogledajo centraliziran delovni seznam, da si ogledajo opravila poteka dela in odobritve, ki so jim dodeljene. 

## <a name="workflow-types"></a>Vrste poteka dela

V naslednji tabeli so navedene vrste poteka dela, ki jih lahko ustvarite v možnosti **Upravljanje stroškov**.


|              <strong>Vrsta </strong>              |                   <strong>Uporabite to vrsto za</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Samodejno odobritev poročil o stroških</strong> |            Ustvarite poteke dela odobritve za poročila o stroških.             |
|  <strong>Samodejno knjiženje poročil o stroških</strong>   |        Ustvarite poteke dela samodejnega knjiženja za poročila o stroških.        |
|       <strong>Postavka vrstice stroška</strong>        |     Ustvarite poteke dela odobritve za postavke vrstice v poročilih o stroških.      |
| <strong>Samodejno knjiženje postavke vrstice stroška</strong> | Ustvarite poteke dela samodejnih knjiženj za postavke vrstice v poročilih o stroških. |
|       <strong>Zahteva za pot</strong>       |          Ustvarite poteke dela odobritve za zahteve za pot.           |
|      <strong>Zahteva za denarni predujem</strong>      |         Ustvarite poteke dela odobritve za zahteve za denarni predujem.          |
|        <strong>Izterjava davka DDV</strong>        | Ustvarite poteke dela odobritve za izterjavo davka na dodano vrednost (DDV).  |