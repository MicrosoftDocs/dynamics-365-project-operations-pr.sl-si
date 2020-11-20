---
title: Popravljeni računi
description: Ta tema vsebuje informacije o popravljenih računih.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122408"
---
# <a name="corrected-invoices"></a>Popravljeni računi

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Potrjene račune lahko uredite. Ko uredite potrjeni račun, se ustvari osnutek popravljenega računa. Ker se predpostavlja, da želite stornirati vse transakcije in količine iz izvirnega računa, popravljeni račun vključuje vse transakcije iz izvirnega računa, vse količine na njem pa imajo vrednost nič (0).

Ko transakcije ne potrebujejo popravka, jih lahko odstranite iz osnutka korektivnega računa. Za storniranje ali vrnitev le delne količine, lahko uredite polje »Količina« v podrobnosti vrstice. Če odprete podrobnost vrstice računa, si lahko ogledate količino na izvirnem računu. Nato lahko uredite količino na trenutnem računu, tako da je manjša ali večja od količine na izvirnem računu.

Ko potrdite korektivni račun, je prvotna obračunana dejanska prodaja stornirana in ustvari se nova obračunana dejanska prodaja. Če ste zmanjšali količino, se bo zaradi razlike ustvarila tudi nova neobračunana dejanska prodaja. Če je bila na primer prvotna obračunana prodaja za osem ur, v podrobnosti vrstice popravljenega računa pa je količina zmanjšana na šest ur, se vrstica izvirne obračunane prodaje stornira in ustvarita se dve novi dejanski vrednosti:

- Obračunana dejanska prodaja za šest ur.
- Neobračunana dejanska prodaja za preostali dve uri. Ta transakcija je lahko obračunana pozneje ali označena kot transakcija, ki se ne zaračuna, odvisno od pogajanj s stranko.
