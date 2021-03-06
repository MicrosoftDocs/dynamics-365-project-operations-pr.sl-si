---
title: Popravljeni računi
description: Ta tema vsebuje informacije o popravljenih računih.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898101"
---
# <a name="corrected-invoices"></a>Popravljeni računi

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Potrjene račune lahko uredite. Ko uredite potrjeni račun, se ustvari osnutek popravljenega računa. Ker se predpostavlja, da želite stornirati vse transakcije in količine iz izvirnega računa, popravljeni račun vključuje vse transakcije iz izvirnega računa, vse količine na njem pa imajo vrednost nič (0).

Ko transakcije ne potrebujejo popravka, jih lahko odstranite iz osnutka korektivnega računa. Za storniranje ali vrnitev le delne količine, lahko uredite polje »Količina« v podrobnosti vrstice. Če odprete podrobnost vrstice računa, si lahko ogledate količino na izvirnem računu. Nato lahko uredite količino na trenutnem računu, tako da je manjša ali večja od količine na izvirnem računu.

Ko potrdite korektivni račun, je prvotna obračunana dejanska prodaja stornirana in ustvari se nova obračunana dejanska prodaja. Če ste zmanjšali količino, se bo zaradi razlike ustvarila tudi nova neobračunana dejanska prodaja. Če je bila na primer prvotna obračunana prodaja za osem ur, v podrobnosti vrstice popravljenega računa pa je količina zmanjšana na šest ur, se vrstica izvirne obračunane prodaje stornira in ustvarita se dve novi dejanski vrednosti:

- Obračunana dejanska prodaja za šest ur.
- Neobračunana dejanska prodaja za preostali dve uri. Ta transakcija je lahko obračunana pozneje ali označena kot transakcija, ki se ne zaračuna, odvisno od pogajanj s stranko.
