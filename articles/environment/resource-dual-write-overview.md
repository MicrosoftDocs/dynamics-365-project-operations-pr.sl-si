---
title: Integracija za dvojno zapisovanje za Project Operations
description: V tej temi najdete pregled integracije za dvojno zapisovanje za Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582776"
---
# <a name="project-operations-dual-write-integration-overview"></a>Pregled integracije za dvojno zapisovanje za Project Operations

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Projektne operacije uporabljajo [zmožnosti dvojnega pisanja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) za sinhronizacijo podatkov med Microsoft Dataverse in Dynamics 365 Finance.

Spodnja ilustracija prikazuje, kako se sinhronizirajo podatki kot del te integracije med storitvama Dataverse in Finance.

![Pregled pretoka podatkov za storitve Project Operations.](./media/ProjectOperationsFlows.jpg)

Aplikacija Project Operations v storitvi Dataverse ponuja sodoben uporabniški vmesnik (UI) in preprosto razširitev brez kodiranja/z malo programske kode z uporabo zmogljivosti storitve Power Platform. Vodje projektov, upravitelji virov, člani projektne ekipe in druge osebe osrednje pisarne, opravljajo svoje dejavnosti v aplikaciji Project Operations v storitvi Dataverse.

Aplikacija Project Operations v storitvi Finance zagotavlja podporo pri računovodstvu projekta in prepoznavanju prihodkov. Aplikacija Project Operations se poveže s finančnim ogrodjem aplikacije Finance za pripravo izračunov prometnega davka, menjalnih tečajev valut, poročil o finančni razsežnosti in še več. Izkušnje računovodje projekta večinoma temeljijo na aplikaciji Finance.

Integracija za Project Operations vključuje naslednjo integracijo komponent:


- [Nastavitev aplikacije Project Operations in integracija konfiguracijskih podatkov](resource-dual-write-setup-integration.md) 
- [Ocene projekta in dejanske vrednosti](resource-dual-write-estimates-actuals.md)
- [Računi za projekt](resource-dual-write-project-invoice.md)
- [Upravljanje stroškov](resource-dual-write-expense.md)
- [Račun dobavitelja](resource-dual-write-vendor-invoice.md)
