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
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="000e4-103">Pregled integracije za dvojno zapisovanje za Project Operations</span><span class="sxs-lookup"><span data-stu-id="000e4-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="000e4-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="000e4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="000e4-105">Project Operations uporablja [zmožnosti dvojnega zapisovanja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) za sinhronizacijo podatkov a aplikacijah Microsoft Dataverse in Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="000e4-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="000e4-106">Spodnja ilustracija prikazuje, kako se sinhronizirajo podatki kot del te integracije med storitvama Dataverse in Finance.</span><span class="sxs-lookup"><span data-stu-id="000e4-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Pregled pretoka podatkov za Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="000e4-108">Aplikacija Project Operations v storitvi Dataverse ponuja sodoben uporabniški vmesnik (UI) in preprosto razširitev brez kodiranja/z malo programske kode z uporabo zmogljivosti storitve Power Platform.</span><span class="sxs-lookup"><span data-stu-id="000e4-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="000e4-109">Vodje projektov, upravitelji virov, člani projektne ekipe in druge osebe osrednje pisarne, opravljajo svoje dejavnosti v aplikaciji Project Operations v storitvi Dataverse.</span><span class="sxs-lookup"><span data-stu-id="000e4-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="000e4-110">Aplikacija Project Operations v storitvi Finance zagotavlja podporo pri računovodstvu projekta in prepoznavanju prihodkov.</span><span class="sxs-lookup"><span data-stu-id="000e4-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="000e4-111">Aplikacija Project Operations se poveže s finančnim ogrodjem aplikacije Finance za pripravo izračunov prometnega davka, menjalnih tečajev valut, poročil o finančni razsežnosti in še več.</span><span class="sxs-lookup"><span data-stu-id="000e4-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="000e4-112">Izkušnje računovodje projekta večinoma temeljijo na aplikaciji Finance.</span><span class="sxs-lookup"><span data-stu-id="000e4-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="000e4-113">Integracija za Project Operations vključuje naslednjo integracijo komponent:</span><span class="sxs-lookup"><span data-stu-id="000e4-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="000e4-114">Nastavitev aplikacije Project Operations in integracija konfiguracijskih podatkov</span><span class="sxs-lookup"><span data-stu-id="000e4-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="000e4-115">Ocene projekta in dejanske vrednosti</span><span class="sxs-lookup"><span data-stu-id="000e4-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="000e4-116">Računi za projekt</span><span class="sxs-lookup"><span data-stu-id="000e4-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="000e4-117">Upravljanje stroškov</span><span class="sxs-lookup"><span data-stu-id="000e4-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="000e4-118">Račun dobavitelja</span><span class="sxs-lookup"><span data-stu-id="000e4-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
