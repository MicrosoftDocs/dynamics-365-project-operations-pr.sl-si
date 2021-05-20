---
title: Integracija za dvojno zapisovanje za Project Operations
description: V tej temi najdete pregled integracije za dvojno zapisovanje za Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955678"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="de92a-103">Pregled integracije za dvojno zapisovanje za Project Operations</span><span class="sxs-lookup"><span data-stu-id="de92a-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="de92a-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="de92a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="de92a-105">Project Operations uporablja [zmožnosti dvojnega zapisovanja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) za sinhronizacijo podatkov a aplikacijah Microsoft Dataverse in Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="de92a-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="de92a-106">Spodnja ilustracija prikazuje, kako se sinhronizirajo podatki kot del te integracije med storitvama Dataverse in Finance.</span><span class="sxs-lookup"><span data-stu-id="de92a-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Pregled pretoka podatkov za Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="de92a-108">Aplikacija Project Operations v storitvi Dataverse ponuja sodoben uporabniški vmesnik (UI) in preprosto razširitev brez kodiranja/z malo programske kode z uporabo zmogljivosti storitve Power Platform.</span><span class="sxs-lookup"><span data-stu-id="de92a-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="de92a-109">Vodje projektov, upravitelji virov, člani projektne ekipe in druge osebe osrednje pisarne, opravljajo svoje dejavnosti v aplikaciji Project Operations v storitvi Dataverse.</span><span class="sxs-lookup"><span data-stu-id="de92a-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="de92a-110">Aplikacija Project Operations v storitvi Finance zagotavlja podporo pri računovodstvu projekta in prepoznavanju prihodkov.</span><span class="sxs-lookup"><span data-stu-id="de92a-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="de92a-111">Aplikacija Project Operations se poveže s finančnim ogrodjem aplikacije Finance za pripravo izračunov prometnega davka, menjalnih tečajev valut, poročil o finančni razsežnosti in še več.</span><span class="sxs-lookup"><span data-stu-id="de92a-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="de92a-112">Izkušnje računovodje projekta večinoma temeljijo na aplikaciji Finance.</span><span class="sxs-lookup"><span data-stu-id="de92a-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="de92a-113">Integracija za Project Operations vključuje naslednjo integracijo komponent:</span><span class="sxs-lookup"><span data-stu-id="de92a-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="de92a-114">Nastavitev aplikacije Project Operations in integracija konfiguracijskih podatkov</span><span class="sxs-lookup"><span data-stu-id="de92a-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="de92a-115">Ocene projekta in dejanske vrednosti</span><span class="sxs-lookup"><span data-stu-id="de92a-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="de92a-116">Računi za projekt</span><span class="sxs-lookup"><span data-stu-id="de92a-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="de92a-117">Upravljanje stroškov</span><span class="sxs-lookup"><span data-stu-id="de92a-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="de92a-118">Račun dobavitelja</span><span class="sxs-lookup"><span data-stu-id="de92a-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
