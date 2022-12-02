---
title: Preklic odobritve predhodno odobrenih vnosov
description: Ta članek pojasnjuje, kako lahko vodja projektov prekliče odobritev predhodno odobrenih vnosov časa, stroškov ali porabe materiala.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930476"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Preklic odobritve predhodno odobrenih vnosov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Vodja projektov ali odobritelj, ki je prej odobril vnose časa, stroškov ali porabe materiala, lahko prekliče svojo odobritev teh vnosov. 

Če želite preklicati odobritev prej odobrenih vnosov časa, stroškov ali porabe materiala, sledite spodnjim korakom.

1. Odprite **Projekti** \> **Moje delo** \> **Odobritve**.
2. Stran s seznamom **Odobritve** prikazuje vse časovne vnose, ki čakajo na odobritev. Spremeni pogled na **Moje pretekle odobritve**.
3. Izberite odobritve časa, stroškov ali materiala, ki jih želite preklicati. Nato v podoknu za dejanja izberite **Preklic odobritve**.
4. V polju za potrditveno sporočilo, ki se prikaže, izberite možnost **V redu**, da potrdite postopek.

> [!IMPORTANT]
> Ne morete preklicati odobritve predhodno odobrenega vnosa časa, stroškov in porabe materiala, ki je že bila zaračunan stranki. Če to poskusite, prejmete sporočilo, da odobritve ni mogoče preklicati, ker je že bila zaračunana. V tem primeru lahko odobritev prekličete le, če se za izdajo celotnega dobroimetja ali vračila stranki na prvotnem računu uporabi popravljeni račun.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Učinek preklica odobritve predhodno odobrenega vnosa

Preklic odobritve ima operativni in finančni učinek.

### <a name="operational-impact"></a>Operativni učinek

Če je odobritev vnosa preklicana, je zapis odobritve označen kot **Poslano**. Stanje vnosa se spremeni v **Poslano**. V tej fazi lahko član projektne ekipe odpokliče vnos, ne da bi predložil zahtevo za odpoklic.

Odobritelj lahko spremeni vrednosti **Količina za obračun** in **Vrsta obračunavanja** in nato še enkrat potrdi vnos.

### <a name="financial-impact"></a>Finančni učinek

Če je odobritev vnosa preklicana, se ustrezne dejanske vrednosti za stroške in prodajne cene posodobijo tako:

- Polje **Stanje prilagoditve** je posodobljeno na **Prilagojeno**.
- Polje **Stanje obračunavanja** je posodobljeno na **Preklicano**.

Nato se v tabeli »Dejanske vrednosti« ustvarijo postavke storniranja. Če želite ustvariti postavke storniranja, sistem prekopira vrednosti polj iz prvotnih dejanskih vrednosti. Edine vrednosti, ki niso prekopirane, so vrednosti količin. Te vrednosti se stornirajo. Stornirane dejanske vrednosti se ustvarijo za dejanske vrednosti **Stroški** in **Neobračunana prodaja**. Polje **Stanje prilagoditve** za stornirane dejanske vrednosti je nastavljeno na **Ni mogoče prilagoditi**, polje **Stanje obračunavanja** pa na **Preklicano**. Zaradi teh sprememb se zabeleženi stroški in zaostali prihodki v projektu ne bodo več upoštevali pri zneskih, ki jih predstavljajo te dejanske vrednosti.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
