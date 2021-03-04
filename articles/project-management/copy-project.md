---
title: Kopiranje projekta
description: Ta tema vsebuje informacije o kopiranju projektov v aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131813"
---
# <a name="copy-a-project"></a>Kopiranje projekta

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Z aplikacijo Dynamics 365 Project Operations lahko hitro gradite nove projekte z izbiro funkcije **Kopiraj projekt** na obrazcu **Projekti**. Če želite kopirati projekt, odprite projekt, ki ga želite kopirati, in nato izberite možnost **Kopiraj projekt**. S tem dejanjem bodo kopirani naslednji elementi:

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

Za informacije o programskem dostopu do programa Copy Project glejte razdelek [Razvijanje predlog projektov s programom Copy Project](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]