---
title: Kopiranje projekta
description: Ta tema vsebuje informacije o kopiranju projektov v aplikaciji Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091274"
---
# <a name="copy-a-project"></a>Kopiranje projekta

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

V aplikaciji Dynamics 365 Project Operations lahko hitro gradite nove projekte tako, da na obrazcu **Projekti** izberete možnost **Kopiraj projekt**. Če želite kopirati projekt, odprite projekt, ki ga želite kopirati, in nato izberite možnost **Kopiraj projekt**. Dejanje bo kopiralo naslednje:

- Lastnosti projekta 
- Strukturirana členitev dela
- Člani projektne ekipe
- Projektne ocene
- Ocene stroškov projekta
- Ocene materiala za projekt

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
- Predvideni začetni datum: to je datum, ko je projekt ustvarjen iz kopije.
- Predvideni končni datum: ta datum se prilagodi glede na začetni datum novega projekta, ki je bil narejen iz kopije.
- Obseg dela (ure)
- Ocenjena cena dela
- Ocenjena cena stroškov
- Ocenjena vrednost »material – cena«

> [!NOTE]
> Kopiranje projekta je dolgotrajen postopek. Kopirajo se tudi projektni zapisi, njihovi ustrezni atributi in številne povezane entitete. Zaradi dolgotrajne narave postopka je po začetku kopiranja stran ciljnega projekta zaklenjena za urejanje, dokler postopek kopiranja ni končan.

## <a name="work-breakdown-structure"></a>Strukturirana členitev dela

Pri kopiranju projekta se kopira celotna struktura razčlenitve dela z naloženimi viri. Poimenovani vir je zamenjaj s splošnim. Če imenovani viri nimajo enakega delovnega časa kot splošni vir, se urnik preračuna in trajanje opravil se lahko spremeni.

## <a name="project-team-members"></a>Člani projektne ekipe

Če je iz izvornega projekta kopirana projektna skupina, so kopirani splošni viri. Iz izvornega projekta so ohranjene tudi dodelitve splošnega vira. Poimenovani viri bodo pretvorjeni v splošne člane skupine.

## <a name="estimates"></a>Ocene

Ko je projekt kopiran, se iz izvornega projekta kopirajo vrstice virov, stroškov in ocene materiala. 

Za informacije o programskem dostopu do programa Copy Project glejte razdelek [Razvijanje predlog projektov s programom Copy Project](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
