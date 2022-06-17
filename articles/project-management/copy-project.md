---
title: Kopiranje projekta
description: Ta članek vsebuje informacije o kopiranju projektov v Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925784"
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
- Kontrolni seznami projekta
- Projektna vedra

## <a name="project-properties"></a>Lastnosti projekta

Ko je projekt kopiran, se kopirajo vrednosti v naslednjih poljih.

| Polje | Projektne operacije Nezaloženi materiali | Project Operations Lite | Projekt za splet |
|-------|------------------------------------------|-------------------------|---------------------|
| Imenu | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| stranka | :heavy_check_mark: | :heavy_check_mark: | |
| Predloga koledarja | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Valuta | :heavy_check_mark: | :heavy_check_mark: | |
| Pogodbena enota | :heavy_check_mark: | :heavy_check_mark: | |
| Lastniško podjetje | :heavy_check_mark: | | |
| Vodja projektov | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Splošno stanje projekta | :heavy_check_mark: | :heavy_check_mark: | |
| Comments | :heavy_check_mark: | :heavy_check_mark: | |
| Ocene | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Predvideni začetni datum</p><p><strong>Opomba:</strong> To polje določa datum, ko je projekt ustvarjen iz kopije. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Predvideni datum zaključka</p><p><strong>Opomba:</strong> Datum v tem polju je prilagojen glede na datum začetka novega projekta, ki je bil izdelan iz kopije.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Obseg dela (ure) | :heavy_check_mark: | :heavy_check_mark: | |
| Ocenjena cena dela | :heavy_check_mark: | :heavy_check_mark: | |
| Ocenjena cena stroškov | :heavy_check_mark: | :heavy_check_mark: | |
| Ocenjena vrednost »material – cena« | | :heavy_check_mark: | |

> [!NOTE]
> Kopiranje projekta je dolgotrajen postopek. Kopirajo se tudi projektni zapisi, njihovi ustrezni atributi in številne povezane entitete. Zaradi dolgotrajne narave postopka je po začetku kopiranja stran ciljnega projekta zaklenjena za urejanje, dokler postopek kopiranja ni končan.

## <a name="work-breakdown-structure"></a>Strukturirana členitev dela

Pri kopiranju projekta se kopira celotna struktura razčlenitve dela z naloženimi viri. Poimenovani vir je zamenjaj s splošnim. Če imenovani viri nimajo enakega delovnega časa kot generični vir, bo urnik ponovno izračunan in trajanje opravil se lahko spremeni.

## <a name="project-team-members"></a>Člani projektne ekipe

Če je iz izvornega projekta kopirana projektna skupina, so kopirani splošni viri. Iz izvornega projekta so ohranjene tudi dodelitve splošnega vira. Poimenovani viri bodo pretvorjeni v splošne člane skupine.

> [!NOTE]
> Člani ekipe in naloge se ne kopirajo v Project za splet.

## <a name="estimates"></a>Ocene

Ko je projekt kopiran, se iz izvornega projekta kopirajo vrstice virov, stroškov in ocene materiala. 

Za informacije o programskem dostopu do programa Copy Project glejte razdelek [Razvijanje predlog projektov s programom Copy Project](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Ponudbe in pogodbe

Ponudbe in pogodbe niso povezane s ciljnim projektom.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
