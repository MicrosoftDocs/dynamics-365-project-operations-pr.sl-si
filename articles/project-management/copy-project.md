---
title: Kopiranje projekta
description: Ta tema vsebuje informacije o kopiranju projektov v aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479539"
---
# <a name="copy-a-project"></a>Kopiranje projekta

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V aplikaciji Dynamics 365 Project Operations lahko hitro gradite nove projekte tako, da na obrazcu **Projekti** izberete možnost **Kopiraj projekt**. Če želite kopirati projekt, odprite projekt, ki ga želite kopirati, in nato izberite možnost **Kopiraj projekt**. S tem dejanjem bodo kopirani naslednji elementi:

- Lastnosti projekta (predvideni datum začetka je kopiran iz izvornega projekta)
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
