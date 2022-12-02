---
title: Varnost in odobritve
description: Ta članek vsebuje informacije o varnostni nastavitvi za delo z odobritvami v programu Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709418"
---
# <a name="security-and-approvals"></a>Varnost in odobritve

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Microsoft Dynamics 365 Project Operations uporablja dve varnostni vlogi za odobritev vnosov časa, stroškov in materiala:

- Odobritelj projekta
- Skrbnik odobritelja projekta

## <a name="project-approver"></a>Odobritelj projekta

Za odobritev vnosov časa projekta, stroškov in materialov morate imeti varnostno vlogo **Odobritelj projekta**. Imeti morate tudi dostop do ustreznih povezanih entitet, kot je npr. **Projekt**. Ta dostop lahko dodeli nekdo, ki ima vlogo **Vodja projektov**. Poleg tega morate biti član projektne ekipe in označeni kot odobritelj.

Če želite odobriti vnose, ki niso povezani s projektom, morate biti vodja pošiljatelja.

## <a name="project-approver-admin"></a>Skrbnik odobritelja projekta

> [!NOTE]
> Funkcija [Nabori odobritev](approval-sets.md) mora biti omogočena, preden lahko uporabite funkcijo »Skrbnik odobritelja projekta«.

Varnostna vloga **Skrbnik odobritelja projekta** uporabnikom omogoča, da zaobidejo pravilnike in odobrijo vnose v vseh projektih. Dodelitev te vloge bo zaobšla logiko preverjanja veljavnosti, ki zahteva članstvo v ekipi in oznako odobritelja. Imeti morate dostop do ustreznih povezanih tabel, kot je npr. **Projekt**, prek varnostnih vlog, ki so vam dodeljene.

Uporabniški kontekst SYSTEM obide preverjanja veljavnosti na enak način kot varnostna vloga »Skrbnik odobritelja projekta«.
