---
title: Vnos stroškov (poenostavljen)
description: Ta tema vsebuje informacije o tem, kako delati z vnosom stroškov v poenostavljeni uvedbi.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d87094882751f0751a8d9d539fa4cdcfc6b7b0d7
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590966"
---
# <a name="expense-entry-lite"></a>Vnos stroškov (poenostavljen)

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Osnovno ali poenostavljeno upravljanje stroškov pomeni zmožnost beleženja enostavnih stroškov. Stroške lahko beležite za projekt, nato pa jih bo odobritelj projekta pregledal in odobril.

Za več informacij o stroškovnih zmožnostih v Dynamics 365 Project Operations glejte [Pregled stroškov](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Zajem posameznega osnovnega stroška

Podatke o stroških lahko zajamete in jih predložite odobritelju.

1. Odprite razdelek **Stroški** in izberite možnost **Novo**.
2. Na strani **Nov strošek** vnesite zahtevane podatke o stroških in nato izberite možnost **Shrani**.

## <a name="submit-a-basic-expense"></a>Pošiljanje posameznega osnovnega stroška

Ko končate z zajemanjem vseh stroškov in ste pripravljeni, da se jih odobri, jih morate najprej poslati v presojo.

1. Odprite razdelek **Stroški** in izberite posamezen strošek. Ali pa s potrditvenim poljem v glavi izberite vse stroške.
2. Izberite **Pošlji**. Sistem obdela izbrane vnose in nato ustvari zahteve za odobritev stroškov.

## <a name="add-an-attachment"></a>Dodaj prilogo

Morda boste morali odobritelju predložiti dodatno dokumentacijo o svojih stroških. Na časovnico z vnosom stroška lahko priložite potrdilo. Izberite **Uredi** in v razdelku **Časovnica** izberite ikono sponke, da priložite potrdilo.

## <a name="recall-a-basic-expense"></a>Preklic posameznega osnovnega stroška

Če v presojo pošljete strošek po pomoti, ga lahko prekličete. Čas, ki je potreben za preklic vnosa stroškov, je odvisen od stopnje odobritve.  Če odobritelj še ni odobril vnosa, se lahko preklic izvede takoj. Če pa je vnos že odobren, se od odobritelja zahteva odobritev preklica in razveljavitev transakcij.

1. V razdelku **Stroški** na seznamu stroškov izberite strošek, ki ga želite preklicati.
2. Izberite **Prekliči**. Če vnos stroška še ni odobren, ga sistem takoj prekliče. Če je bil vnos stroškov že odobren, se ustvari zahteva za preklic, s katero se odobritelja obvesti, da želite stornirati stroške. Odobritelj bo nato potrdil, ali je razveljavitev mogoča, in vnos bo vrnjen.

## <a name="delete-a-basic-expense"></a>Izbris posameznega osnovnega stroška

Stroške, ki še niso bili poslani, je mogoče izbrisati. Če želite izbrisati že oddani strošek, ga morate najprej preklicati.

## <a name="see-also"></a>Glejte tudi

- [Pregled odobritev](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]