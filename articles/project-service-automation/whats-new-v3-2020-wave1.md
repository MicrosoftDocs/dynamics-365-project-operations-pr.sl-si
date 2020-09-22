---
title: Novosti ali spremembe v storitvi Project Service Automation različice 3.x, 1. faza za leto 2020
description: V tej temi so na voljo informacije o novostih in spremembah v storitvi Project Service Automation različice 3, 1. faza za leto 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755791"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novosti ali spremembe v storitvi Project Service Automation različice 3, 1. faza za leto 2020
V tej temi so izpostavljeni ključni vidiki nadgradnje pri posodobitvi na zadnjo izdajo storitve Project Service Automation (PSA) različice 3.x, 1. faza za leto 2020.

## <a name="time-entry"></a>Časovni vnos
Izkušnja časovnih vnosov je bila razširjena, da omogoča zmogljivosti za razširitev časovnega vnosa v več scenarijev stranke. To vključuje zmogljivost za dodajanje vrst vnosov, ki zdaj spodbujajo specifično vedenje na podlagi imena sheme polja **Nastavitve časovnega vnosa**, prikazanega kot **Časovni vir**.

### <a name="upgrade-consideration"></a>Vidik nadgradnje
Za podporo te funkcionalnosti so bile vloge znotraj storitve PSA posodobljene, da vključujejo nove pravice. Te pravice podeljujejo dostop za branje novi entiteti **Nastavitve časovnega vnosa**.

Uporabnikom, ki potrebujejo zmogljivost beleženja časa, bi morala biti dodeljena uporabniška vloga **Uporabnik časovnega vnosa** poleg obstoječih vlog. Ta vloga vključuje novo funkcionalnost in zagotavlja, da bo časovni vnos še naprej deloval.

### <a name="currently-extended-time-entry-changes"></a>Trenutne razširjene spremembe časovnih vnosov
Za zmanjšanje vpliva na trenutne uporabnike časovnega vnosa je ta sprememba vloge edina bistvena zahteva, potrebna za nadaljevanje uporabe časovnega vnosa. Če ste ustvarili poglede po meri ali ločene izkušnje časovnega vnosa, morate nastaviti polja **Nastavitev časovnega vnosa** na pravilno vrednost PSA.
