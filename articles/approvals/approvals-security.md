---
title: Varnost in odobritve
description: Ta članek vsebuje informacije o varnostni nastavitvi za delo z odobritvami v Microsoftu Dynamics 365 Project Operations.
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
- Administrator odobritve projekta

## <a name="project-approver"></a>Odobritelj projekta

Morate imeti **Odobritelj projekta** varnostna vloga za odobritev projektnega časa, stroškov in vnosov materiala. Imeti morate tudi dostop do ustreznih povezanih subjektov, kot je npr **Projekt**. Ta dostop lahko dodeli nekdo, ki ima **Vodja projekta** vlogo. Poleg tega morate biti član ekipe projekta in označeni kot odobritelj.

Če želite odobriti vnose, ki niso projekti, morate biti vodja prijavitelja.

## <a name="project-approver-admin"></a>Administrator odobritve projekta

> [!NOTE]
> The [Odobritveni nizi](approval-sets.md) mora biti omogočena, preden lahko uporabite skrbniško funkcijo odobritelja projekta.

The **Administrator odobritve projekta** varnostna vloga omogoča uporabnikom, da obidejo pravilnike in omogoča odobritev vnosov v vseh projektih. Dodelitev te vloge bo zaobšla logiko preverjanja, ki zahteva članstvo v skupini in oznako odobritelja. Imeti morate dostop do ustreznih povezanih tabel, kot npr **Projekt**, prek varnostnih vlog, ki so vam dodeljene.

Uporabniški kontekst SYSTEM obide preverjanja veljavnosti na enak način kot skrbnik odobritelja projekta varnostna vloga.
