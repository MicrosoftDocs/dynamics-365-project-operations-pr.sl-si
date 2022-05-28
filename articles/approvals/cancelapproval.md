---
title: Prekliči odobritev predhodno odobrenih vnosov
description: Ta tema pojasnjuje, kako lahko vodja projekta prekliče odobritev predhodno odobrenih vnosov časa, stroškov ali porabe materiala.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584800"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Prekliči odobritev predhodno odobrenih vnosov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Vodja projekta ali odobritelj, ki je predhodno odobril vnose za čas, stroške ali porabo materiala, lahko prekliče odobritev teh vnosov. 

Sledite tem korakom, da prekličete odobritev predhodno odobrenega vnosa časa, stroškov ali porabe materiala.

1. Odprite **Projekti** \> **Moje delo** \> **Odobritve**.
2. The **Odobritve** stran s seznamom prikazuje vse časovne vnose, ki čakajo na odobritev. Spremenite pogled v **Moje pretekle odobritve**.
3. Izberite odobritve časa, stroškov ali materiala za preklic. Nato v podoknu za dejanja izberite **Prekliči odobritev**.
4. V potrditvenem polju, ki se prikaže, izberite **v redu** za potrditev operacije.

> [!IMPORTANT]
> Ne morete preklicati odobritve predhodno odobrenega vnosa časa, stroškov in porabe materiala, ki je že bil zaračunan stranki. Če poskusite, prejmete sporočilo, da odobritve ni mogoče preklicati, ker je bila že zaračunana. V tem primeru lahko prekličete odobritev le, če se za izdajo celotnega dobropisa ali vračila kupcu na izvirnem računu uporabi popravni račun.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Vpliv preklica odobritve predhodno odobrenega vnosa

Preklic odobritve ima operativni in finančni učinek.

### <a name="operational-impact"></a>Operativni učinek

Če je odobritev vpisa preklicana, se zapisnik o odobritvi označi kot **Oddano**. Status vnosa se spremeni v **Oddano**. V tej fazi lahko član projektne skupine odpokliče vnos, ne da bi predložil zahtevo za odpoklic.

Odobrnik lahko spremeni **Obračunska količina** in **Vrsta obračunavanja** vrednosti in nato še enkrat odobrite vnos.

### <a name="financial-impact"></a>Finančni učinek

Če je odobritev vpisa preklicana, se ustrezni dejanski podatki za stroške in prodajo posodobijo na naslednji način:

- Polje **Stanje prilagoditve** je posodobljeno na **Prilagojeno**.
- Polje **Stanje obračunavanja** je posodobljeno na **Preklicano**.

Nato se v tabeli »Dejanske vrednosti« ustvarijo postavke storniranja. Če želite ustvariti postavke storniranja, sistem prekopira vrednosti polj iz prvotnih dejanskih vrednosti. Edine vrednosti, ki niso prekopirane, so vrednosti količin. Te vrednosti se stornirajo. Stornirane dejanske vrednosti se ustvarijo za dejanske vrednosti **Stroški** in **Neobračunana prodaja**. Polje **Stanje prilagoditve** za stornirane dejanske vrednosti je nastavljeno na **Ni mogoče prilagoditi**, polje **Stanje obračunavanja** pa na **Preklicano**. Zaradi teh sprememb se zabeleženi stroški in zaostali prihodki v projektu ne bodo več upoštevali pri zneskih, ki jih predstavljajo te dejanske vrednosti.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
