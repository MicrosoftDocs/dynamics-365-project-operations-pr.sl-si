---
title: Novosti ali spremembe v storitvi Project Service Automation različice 3.x, 1. faza za leto 2020
description: Ta članek vsebuje informacije o tem, kaj je novega in spremenjenega v Project Service Automation različici 3, val 1 2020.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c762f2e7931046d32464cfa8486ef8405aa7d836
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928636"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Novosti ali spremembe v storitvi Project Service Automation različice 3, 1. faza za leto 2020

[!include [banner](../includes/psa-now-project-operations.md)]

Članek izpostavlja ključne vidike nadgradnje pri prehodu na najnovejšo izdajo Project Service Automation (PSA) različice 3.x val 1 2020.

## <a name="time-entry"></a>Časovni vnos
Izkušnja časovnih vnosov je bila razširjena, da omogoča zmogljivosti za razširitev časovnega vnosa v več scenarijev stranke. To vključuje zmogljivost za dodajanje vrst vnosov, ki zdaj spodbujajo specifično vedenje na podlagi imena sheme polja **Nastavitve časovnega vnosa**, prikazanega kot **Časovni vir**. V podporo tej funkciji je bila dodana nova rešitev, imenovana TESA (angl. Time, Expense, Statusing, and Approvals – čas, stroški, stanje in odobritve).

### <a name="upgrade-consideration"></a>Vidik nadgradnje
Za podporo te funkcionalnosti so bile vloge znotraj storitve PSA posodobljene, da vključujejo nove pravice. Te pravice podeljujejo dostop za branje novi entiteti **Nastavitve časovnega vnosa**.

Uporabnikom, ki potrebujejo zmogljivost beleženja časa, bi morala biti dodeljena uporabniška vloga **Uporabnik časovnega vnosa** poleg obstoječih vlog. Ta vloga vključuje novo funkcionalnost in zagotavlja, da bo časovni vnos še naprej deloval.

Poleg tega velja tudi, da če imate module aplikacij po meri, ki vsebujejo vse obrazce za entiteto časovnega vnosa, boste morali iz modula odstraniti **Obrazec za hitro ustvarjanje časovnega vnosa za rešitev TESA**.

### <a name="currently-extended-time-entry-changes"></a>Trenutne razširjene spremembe časovnih vnosov
Za zmanjšanje vpliva na trenutne uporabnike časovnega vnosa je ta sprememba vloge edina bistvena zahteva, potrebna za nadaljevanje uporabe časovnega vnosa. Če ste ustvarili poglede po meri ali ločene izkušnje časovnega vnosa, morate nastaviti polja **Nastavitev časovnega vnosa** na pravilno vrednost PSA.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
