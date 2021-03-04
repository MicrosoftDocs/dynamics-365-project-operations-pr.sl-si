---
title: Novosti ali spremembe v storitvi Project Service Automation različice 3.x, 1. faza za leto 2020
description: V tej temi so na voljo informacije o novostih in spremembah v storitvi Project Service Automation različice 3, 1. faza za leto 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5110679038ae7ed1e21a3e7dc80a4657e0752b49
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150958"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novosti ali spremembe v storitvi Project Service Automation različice 3, 1. faza za leto 2020

[!include [banner](../includes/psa-now-project-operations.md)]

V tej temi so izpostavljeni ključni vidiki nadgradnje pri posodobitvi na zadnjo izdajo storitve Project Service Automation (PSA) različice 3.x, 1. faza za leto 2020.

## <a name="time-entry"></a>Časovni vnos
Izkušnja časovnih vnosov je bila razširjena, da omogoča zmogljivosti za razširitev časovnega vnosa v več scenarijev stranke. To vključuje zmogljivost za dodajanje vrst vnosov, ki zdaj spodbujajo specifično vedenje na podlagi imena sheme polja **Nastavitve časovnega vnosa**, prikazanega kot **Časovni vir**. V podporo tej funkciji je bila dodana nova rešitev, imenovana TESA (angl. Time, Expense, Statusing, and Approvals – čas, stroški, stanje in odobritve).

### <a name="upgrade-consideration"></a>Vidik nadgradnje
Za podporo te funkcionalnosti so bile vloge znotraj storitve PSA posodobljene, da vključujejo nove pravice. Te pravice podeljujejo dostop za branje novi entiteti **Nastavitve časovnega vnosa**.

Uporabnikom, ki potrebujejo zmogljivost beleženja časa, bi morala biti dodeljena uporabniška vloga **Uporabnik časovnega vnosa** poleg obstoječih vlog. Ta vloga vključuje novo funkcionalnost in zagotavlja, da bo časovni vnos še naprej deloval.

Poleg tega velja tudi, da če imate module aplikacij po meri, ki vsebujejo vse obrazce za entiteto časovnega vnosa, boste morali iz modula odstraniti **Obrazec za hitro ustvarjanje časovnega vnosa za rešitev TESA**.

### <a name="currently-extended-time-entry-changes"></a>Trenutne razširjene spremembe časovnih vnosov
Za zmanjšanje vpliva na trenutne uporabnike časovnega vnosa je ta sprememba vloge edina bistvena zahteva, potrebna za nadaljevanje uporabe časovnega vnosa. Če ste ustvarili poglede po meri ali ločene izkušnje časovnega vnosa, morate nastaviti polja **Nastavitev časovnega vnosa** na pravilno vrednost PSA.


[!INCLUDE[footer-include](../includes/footer-banner.md)]