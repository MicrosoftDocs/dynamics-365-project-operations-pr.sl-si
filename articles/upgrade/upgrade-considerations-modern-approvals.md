---
title: Premisleki o nadgradnji za sodobne odobritve
description: Tema zajema točke, ki bi jih morali skrbniki upoštevati, ko omogočijo funkcionalnost sodobnih odobritev.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578406"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Premisleki o nadgradnji za sodobne odobritve 

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Kot del izdaje Wave 1 iz aprila 2022 bo privzeto omogočena funkcionalnost Modern Approvals. Ta funkcionalnost izboljšuje zanesljivost logike odobritve in zagotavlja, da lahko ugotovite razlog, če logika odobritve ne uspe.

Kot del te spremembe se posodobijo spremembe statusa za odobritve projektov. Status gre zdaj neposredno od **Oddano** do **Odobreno**. **V teku** ni več status za odobritve. Če želite ugotoviti, ali je odobritev v teku, preverite, ali je odobritev del niza odobritev, in preglejte stanje priloženega kompleta odobritev.

## <a name="before-you-upgrade"></a>Pred nadgradnjo

Preden nadgradite na moderne odobritve, se prepričajte, da nimate čakajočih odobritev. Modern Approvals ne uporablja **V teku** stanje. Zato vse odobritve, ki so še vedno označene kot **V teku** po nadgradnji ne bo obdelan.

## <a name="after-you-upgrade"></a>Po nadgradnji

Ko nadgradite na moderne odobritve, mora skrbnik potrditi, da je bil tok v oblaku, ki obdeluje odobritve, omogočen.

1. Prijavite se v [flow.microsoft.com](https://flow.microsoft.com)
2. V zgornjem desnem kotu strani preklopite svoje okolje na okolje, ki ste ga nadgradili.
3. Izberite **Rešitve** navesti rešitve, ki so nameščene v okolju.
4. Na seznamu rešitev izberite **Projektne operacije** oz **Projektna služba**.
5. Zamenjajte filter iz **vse** do **Oblačni tokovi**.
6. Preverite, da je **Projektna storitev – periodično načrtujte komplete za odobritev projekta** možnost je nastavljena na **Vklopljeno**. Če ni, izberite tok in nato izberite **Vklopiti**.
7. Preverite, ali se obdelava izvaja vsakih pet minut, tako da pregledate **Sistemska delovna mesta** seznam v **Nastavitve** območje.

## <a name="short-term-rollback"></a>Kratkoročno vrnitev nazaj

Če ne morete sprejeti sprememb ali če naletite na resno težavo s to funkcijo, se lahko začasno vrnete na prvotni potek odobritve, tako da izvedete naslednje korake:
1. Prijavite se v svoje okolje in preverite, ali ni čakajočih odobritev.
2. Pojdi do **Nastavitve** > **Parametri projekta**.
3. Izberite **Nadzor funkcij** in nato izberite **Sodobne odobritve** za izklop funkcije.

## <a name="removing-the-feature-flag"></a>Odstranitev zastave funkcije

V posodobitvi Wave 2 iz oktobra 2022 bo možnost izklopa te funkcije odstranjena.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
