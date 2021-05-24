---
title: Načini razporejanja
description: Ta tema vsebuje informacije o načinih razporejanja.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981455"
---
# <a name="scheduling-modes"></a>Načini razporejanja

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_


Storitev Dynamics 365 Project Operations organizacijam omogoča, da opredelijo način upravljanja sprememb ključnih spremenljivk v opravilih znotraj strukture členitve dela. Na podlagi posebnih potreb organizacije lahko vodje projektov ob ustvaritvi projekta spremenijo način razporejanja.

V storitvi Project Operations so na voljo trije načini razporejanja:

  - Nespremenljivo trajanje (to je privzeti način)
  - Nespremenljivo delo
  - Nespremenljive enote

Vrednosti, na katere vpliva opredelitev posameznega načina razporejanja, se določijo z naslednjo formulo:

  Obseg dela (*Delo*) = Trajanje x Enote

Ko določite način razporejanja projekta, nastavite eno od teh vrednosti, ki je nato ni mogoče spremeniti. Če je ta vrednost konstanta, pridobi prednost, kar sistem obvesti, da je ne sme spremeniti, ko se spremenita drugi dve vrednosti. Naslednja tabela vsebuje informacije o vplivih izbire posameznega načina.

| **V tem opravilu**             | **Če popravite enote**   | **Če popravite trajanje** | **Če popravite obseg dela**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Opravilo z nespremenljivimi enotami     | Trajanje je znova izračunano. | Obseg dela je znova izračunan.    | Trajanje je znova izračunano. |
| Opravilo z nespremenljivim obsegom dela    | Trajanje je znova izračunano. | Enote so znova izračunane.    | Trajanje je znova izračunano. |
| Opravilo z nespremenljivim trajanjem  | Obseg dela je znova izračunan.   | Obseg dela je znova izračunan.    | Enote so znova izračunane.   |

Za več informacij o vplivih posameznega načina si preberite razdelek [Sprememba vrste opravila za natančnejše razporejanje](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). V temi se namesto izraza **Obseg dela** uporablja izraz **Delo**.

## <a name="change-the-organizations-scheduling-mode"></a>Sprememba načina razporejanja organizacije

Upoštevajte naslednja navodila, da določite način razporejanja organizacije.

1. Odprite razdelek **Nastavitve** \> **Splošno** \> **Parametri** in nato izberite parameter projekta. 
2. Na strani **Parametri projekta** izberite privzeti način razporejanja za organizacijo in nato upravitelju projekta omogočite preglasitev nastavitev pri ustvarjanju novega projekta.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Sprememba nastavitev načina razporejanja v projektu

Če organizacija upravitelju projektov dovoli, da preglasi privzeti način razporejanja, lahko vodja projekta to spremembo izvede ob ustvaritvi novega projekta. Ko je projekt shranjen, pa načina razporejanja ni več mogoče spremeniti.

## <a name="copied-projects"></a>Kopirani projekti

Ker je projekt ustvarjen ob izvedbi kopiranja projekta, upravitelj projekta ne more nastaviti načina razporejanja. Ciljni projekt bo vedno privzeto deloval v načinu, določenem na ravni organizacije.

## <a name="copied-tasks"></a>Kopirana opravila

Ko je opravilo kopirano iz enega projekta v drugega, opravilo podeduje način razporejanja ciljnega projekta.