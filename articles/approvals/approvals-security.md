---
title: Varnost in odobritve
description: Ta članek vsebuje informacije o varnostni nastavitvi za delo z odobritvami v Microsoftu Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525415"
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

The **Administrator odobritve projekta** varnostna vloga omogoča uporabnikom, da obidejo pravilnike in omogoča odobritev vnosov v vseh projektih. Dodelitev te vloge bo zaobšla logiko preverjanja, ki zahteva članstvo v skupini in oznako odobritelja. Imeti morate dostop do ustreznih povezanih subjektov, kot je npr **Projekt**. Ta dostop lahko dodeli nekdo, ki ima **Vodja projekta** vlogo.

Uporabniški kontekst SYSTEM obide preverjanja veljavnosti na enak način kot skrbnik odobritelja projekta varnostna vloga.
