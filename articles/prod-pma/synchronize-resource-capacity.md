---
title: Sinhronizacija zmogljivosti vira
description: Ta članek vsebuje informacije o sinhronizaciji zmogljivosti vira v koledarjih in projektih.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b684833ffae83b7cedfc73ee96a8aa8ddd4ec57
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920724"
---
# <a name="synchronize-resource-capacity"></a>Sinhronizacija zmogljivosti vira

[!include [banner](../includes/banner.md)]

Procesi za sinhronizacijo virov pomagajo zagotoviti, da se informacije za koledar in osnovni koledar stekajo navzdol v razporejanje virov projekta. Če je koledar spremenjen, procesi izvedejo zahtevane spremembe za razporejanje virov projekta. Procesi pripomorejo tudi k izboljšanju učinkovitosti, ker se informacije o virih koledarja vnaprej sinhronizirajo. Zato se posodobitve informacij o razporejanju virov pojavijo hitreje. Priporočamo, da procese razporedite kot paket, namesto enega po enega. V nasprotnem primeru obstaja nevarnost, da bo kdo pozabil vključujoče datume, ko so bile informacije nazadnje sinhronizirane. Če se ne uporabljajo vključujoči datumi, lahko med sinhronizacijo datumov pride do vrzeli.

![Sinhronizacija koledarja.](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sinhronizacija zbiranj zmogljivosti vira

Proces sinhronizacije je zasnovan za sinhronizacijo vseh informacij koledarja virov. Te informacije vključujejo informacije osnovnega koledarja o vseh spremembah tabele zmogljivosti koledarja virov projekta. Če so v projekt dodani novi viri, sinhronizacija pomaga zagotoviti, da so na voljo posodobljene informacije koledarja. To sinhronizacijo lahko izvedete kadar koli.

Priporočamo uporabo paketa. Možnosti so na voljo med sinhronizacijo rezervacij zmogljivosti.

1. Izberite **Vodenje projektov in računovodstvo** &gt; **Redno** &gt; **Sinhronizacija zmogljivosti** &gt; **Sinhronizacija zbiranj zmogljivosti vira**.
2. Nastavite možnosti v naslednji tabeli.

    | Možnost      | Opis |
    |-------------|-------------|
    | Koda obdobja | Izbirno izberite kodo intervala datuma glavne knjige, da nastavite začetni in končni datum za proces sinhronizacije za zbiranja zmogljivosti vira. |
    | Začetni datum  | Vnesite začetni datum za proces sinhronizacije za zbiranja zmogljivosti vira. |
    | Končni datum    | Vnesite končni datum za proces sinhronizacije za zbiranja zmogljivosti vira. |

[![Proces sinhronizacije.](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]