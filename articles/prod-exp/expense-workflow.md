---
title: Potek dela upravljanja stroškov
description: Ta tema pojasnjuje, kako lahko uporabljate sistem poteka dela v aplikaciji Microsoft Dynamics 365 Finance, da vzpostavite postopek pregleda poročil o stroških v aplikaciji za upravljanje stroškov.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084911"
---
# <a name="expense-management-workflow"></a>Potek dela upravljanja stroškov

[!include [banner](../includes/banner.md)]

Sistem poteka dela lahko uporabite, da vzpostavite postopek pregleda poročil o stroških v aplikaciji za upravljanje stroškov. Nastavite lahko potek dela, ki uporablja naslednja merila za določanje odobriteljev poročil o stroških:

- Hierarhija poročanja zaposlenih in vnaprej določene omejitve odobritve
- Večstopenjska odobritev, ki podpira začasne in končne odobritelje
- Finančne razsežnosti in projektna odgovornost
- Dodelitev določenim uporabnikom ali uporabniškim skupinam

Odobritve potekov dela je mogoče ustvariti za poročila o stroških, zahteve za pot, denarne predujme in izterjavo davka na dodano vrednost (DDV).

**Primer**

Spodnji proces prikazuje primer poteka dela upravljanja stroškov za poročilo o stroških.

1. Zaposleni ustvari in shrani poročilo o stroških.
2. Zaposleni pošlje poročilo o stroških v odobritev. Odobritelj je določen na podlagi pravil, ki so bila določena ob nastavitvi poteka dela.
3. Odobritelj prejme obvestilo, da je poročilo o stroških pripravljeno na odobritev. Odobritelj pregleda poročilo o stroških in preveri, ali so izpolnjeni naslednji pogoji:

    - Stroški ne kršijo nobenega pravilnika o stroških. Če stroški kršijo pravilnik, odobritelj preveri, ali poročilo o stroških vključuje veljavno poslovno utemeljitev.
    - Elektronski računi so priloženi poročilu o stroških.

4. Odobritelj odobri poročilo o stroških.
5. Poročilo o stroških je dodeljeno koordinatorju obveznosti za knjiženje.
6. Izvede se eden od naslednjih korakov (odvisno od tega, ali je konfigurirano samodejno knjiženje ali ne):

    - Če je konfigurirano samodejno knjiženje, se poročilo o stroških obdela za plačilo in posodobi stanje poročila o stroških.
    - Če samodejno knjiženje ni konfigurirano, koordinator obveznosti preveri, ali so bili predloženi vsi izvirni računi in ali so računi usklajeni s stroški v poročilu o stroških. Vse davčne številke, ki so vpisane v poročilo o stroških, morajo biti preverjene.

Ko so te zahteve preverjene, se poročilo o stroških vknjiži.

Ko je poročilo o stroških vknjiženo, se zanj odobri plačilo, zaposlenemu pa povrnejo stroški.