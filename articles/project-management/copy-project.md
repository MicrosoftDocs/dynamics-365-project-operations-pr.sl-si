---
title: Kopiranje projekta
description: Ta tema vsebuje informacije o kopiranju projektov v aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908605"
---
# <a name="copy-a-project"></a>Kopiranje projekta

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Z aplikacijo Dynamics 365 Project Operations lahko hitro gradite nove projekte z uporabo funkcije **Kopiraj projekt** na obrazcu **Projekti**. Če želite kopirati projekt, izberite projekt in nato izberite možnost **Kopiranje**. S tem dejanjem bodo kopirani naslednji elementi:

- Lastnosti projekta
- Strukturirana členitev dela
- Člani projektne ekipe
- Projektne ocene
- Ocene stroškov projekta

## <a name="project-properties"></a>Lastnosti projekta

Pri kopiranju projekta se kopirajo vrednosti v naslednjih poljih:

- Imenu
- Opis
- Stranki
- Predloga koledarja
- Valuta
- Pogodbena enota
- Vodja projektov
- Stanje
- Splošno stanje projekta
- Pripombe
- Ocene
- Predvideni začetni datum
- Datum zaključka
- Obseg dela (ure)
- Predvideni stroški dela
- Predvideni stroški

## <a name="work-breakdown-structure"></a>Strukturirana členitev dela

Pri kopiranju projekta se kopira celotna struktura razčlenitve dela z naloženimi viri. Poimenovani vir je zamenjaj s splošnim. Če imenovani viri nimajo enakega delovnega časa kot splošni vir, se urnik preračuna in trajanje opravil se lahko spremeni.

## <a name="project-team-members"></a>Člani projektne ekipe

Če je iz izvornega projekta kopirana projektna skupina, so kopirani splošni viri. Iz izvornega projekta so ohranjene tudi dodelitve splošnega vira. Poimenovani viri bodo pretvorjeni v splošne člane skupine.

## <a name="estimates"></a>Ocene

Pri kopiranju projekta so iz izvornega projekta kopirane vrstice za oceno virov in stroškov.