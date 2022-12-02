---
title: Integracija za dvojno zapisovanje za Project Operations
description: V tem članku najdete pregled integracije za dvojno zapisovanje za Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927992"
---
# <a name="project-operations-dual-write-integration-overview"></a>Pregled integracije za dvojno zapisovanje za Project Operations

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Project Operations uporablja [zmožnosti dvojnega zapisovanja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) za sinhronizacijo podatkov v aplikacijah Microsoft Dataverse in Dynamics 365 Finance.

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
