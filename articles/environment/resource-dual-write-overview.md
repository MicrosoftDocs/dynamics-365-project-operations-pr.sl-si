---
title: Integracija za dvojno zapisovanje za Project Operations
description: V tej temi najdete pregled integracije za dvojno zapisovanje za Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998701"
---
# <a name="project-operations-dual-write-integration-overview"></a>Pregled integracije za dvojno zapisovanje za Project Operations

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Project Operations uporablja [zmožnosti dvojnega zapisovanja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) za sinhronizacijo podatkov a aplikacijah Microsoft Dataverse in Dynamics 365 Finance.

Spodnja ilustracija prikazuje, kako se sinhronizirajo podatki kot del te integracije med storitvama Dataverse in Finance.

![Pregled pretoka podatkov za Project Operations](./media/ProjectOperationsFlows.jpg)

Aplikacija Project Operations v storitvi Dataverse ponuja sodoben uporabniški vmesnik (UI) in preprosto razširitev brez kodiranja/z malo programske kode z uporabo zmogljivosti storitve Power Platform. Vodje projektov, upravitelji virov, člani projektne ekipe in druge osebe osrednje pisarne, opravljajo svoje dejavnosti v aplikaciji Project Operations v storitvi Dataverse.

Aplikacija Project Operations v storitvi Finance zagotavlja podporo pri računovodstvu projekta in prepoznavanju prihodkov. Aplikacija Project Operations se poveže s finančnim ogrodjem aplikacije Finance za pripravo izračunov prometnega davka, menjalnih tečajev valut, poročil o finančni razsežnosti in še več. Izkušnje računovodje projekta večinoma temeljijo na aplikaciji Finance.

Integracija za Project Operations vključuje naslednjo integracijo komponent:


- [Nastavitev aplikacije Project Operations in integracija konfiguracijskih podatkov](resource-dual-write-setup-integration.md) 
- [Ocene projekta in dejanske vrednosti](resource-dual-write-estimates-actuals.md)
- [Računi za projekt](resource-dual-write-project-invoice.md)
- [Upravljanje stroškov](resource-dual-write-expense.md)
- [Račun dobavitelja](resource-dual-write-vendor-invoice.md)
