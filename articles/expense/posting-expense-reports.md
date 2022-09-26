---
title: Objavljanje poročil o stroških
description: V tem članku je razloženo, kako objaviti poročila o stroških.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524890"
---
# <a name="post-expense-reports"></a>Objavljanje poročil o stroških

Ko je poročilo o stroških odobreno in preneseno v splošno temeljnico, ga lahko objavite. Ko objavite poročilo o stroških, se ugotovijo stroški, ki so upravičeni do izterjave davka na dodano vrednost (DDV). Opravilo preverjanja in izterjave davka na dodano vrednost je dodeljeno zaposlenemu, ki je odgovoren za preverjanje poročila o stroških.

Če se stroški v poročilu o stroških zaračunajo podjetju, ki ni podjetje, ki zaposluje zaposlenega, morate preveriti tako podjetje, kateremu se dolgujejo ti stroški, kot podjetje, ki mora povrniti ta znesek. Na primer, zaposleni, ki je predložil poročilo o stroških, dela za podjetje DAT, vendar je strošek zaračunal podjetju DIR. V tem primeru je DAT podjetje, ki mu je treba povrniti strošek, DIR pa podjetje, ki mora povrniti strošek. Ko preverite te vrstice dnevnika, lahko vrstice stroškov knjižite v glavno knjigo.

Če želite objaviti poročilo o stroških, na strani **Odobrena poročila o stroških** izberite poročilo o stroških in nato v podoknu za dejanja izberite **Objavi**.

Na seznamu lahko hkrati objavite tudi vsa poročila o stroških. Izberite vsa poročila o stroških in nato izberite **Objavi**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Omogočite možnost knjiženja obveznosti za stroške v valuti prodajalca za funkcijo načina gotovinskega plačila

The **Možnost knjiženja obveznosti za stroške v valuti prodajalca za gotovinsko plačilno metodo** funkcija omogoča objavo poročil o stroških v valuti prodajalca za način gotovinskega plačila.

Trenutno se ob oddaji blagajniških stroškov poročila o stroških knjižijo v obračunski valuti. Zaradi pretvorbe zneska med valuto transakcije, obračunsko valuto in valuto dobavitelja je prodajalcem plačan napačen znesek, če imata transakcijski datum stroška in dejanski datum plačila različna menjalna tečaja.

Ta funkcija bo zagotovila, da se stanje dobavitelja zabeleži v valuti prodajalca, ko je poročilo o stroških objavljeno.

1. Odprite zavihek **Delovni prostori** \> **Upravljanje funkcije**.
2. Na seznamu poiščite in izberite **Možnost knjiženja obveznosti za stroške v valuti prodajalca za gotovinsko plačilno metodo** in nato izberite **Omogoči zdaj**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
