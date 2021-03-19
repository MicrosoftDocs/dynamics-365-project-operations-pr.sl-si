---
title: Sinhronizacija opravil projekta neposredno iz rešitve Project Service Automation v Finance and Operations
description: Ta tema opisuje predlogo in temeljno opravilo, ki se uporabljata za sinhronizacijo opravil projekta neposredno iz rešitve Microsoft Dynamics 365 Project Service Automation v Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288939"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="16e99-103">Sinhronizacija opravil projekta neposredno iz rešitve Project Service Automation v Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="16e99-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="16e99-104">Ta tema opisuje predlogo in temeljno opravilo, ki se uporabljata za sinhronizacijo opravil projekta neposredno iz rešitve Dynamics 365 Project Service Automation v Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="16e99-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="16e99-105">V različici 8.0 so na voljo integracija projektnih opravil, kategorije transakcije stroškov, ocene delovnih ur, ocene stroškov in zaklepanje funkcionalnosti.</span><span class="sxs-lookup"><span data-stu-id="16e99-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="16e99-106">Če uporabljate različico Enterprise 7.3.0, boste po namestitvi KB 4132657 in KB 4132660 lahko predloge uporabili za integracijo projektnih opravil, kategorij stroškov transakcij, ocen delovnih ur, ocen stroškov in dejanskih vrednosti ter konfiguriranje zaklepanja funkcionalnosti.</span><span class="sxs-lookup"><span data-stu-id="16e99-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="16e99-107">Če morate ponastaviti računovodsko porazdeljevanje, priporočamo, da namestite tudi KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="16e99-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="16e99-108">Integracija dejanskih vrednosti je na voljo v različici 8.0.1 ali novejši.</span><span class="sxs-lookup"><span data-stu-id="16e99-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="16e99-109">Pretok podatkov za Project Service Automation v Finance</span><span class="sxs-lookup"><span data-stu-id="16e99-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="16e99-110">Rešitev za integracijo rešitve Project Service Automation v rešitev Finance uporablja funkcijo za integracijo podatkov za sinhronizacijo podatkov med primerki rešitev Project Service Automation in Finance.</span><span class="sxs-lookup"><span data-stu-id="16e99-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="16e99-111">Predloga za integracijo, ki je na voljo s funkcijo za integracijo podatkov, omogoča pretok podatkov o opravilih projekta iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="16e99-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="16e99-112">Naslednja slika prikazuje, kako se podatki sinhronizirajo med rešitvama Project Service Automation in Finance.</span><span class="sxs-lookup"><span data-stu-id="16e99-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="16e99-113">[![Pretok podatkov za integracijo rešitve Project Service Automation v Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="16e99-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="16e99-114">Predloga in opravilo</span><span class="sxs-lookup"><span data-stu-id="16e99-114">Template and task</span></span>

<span data-ttu-id="16e99-115">Za dostop do predloge v skrbniškem središču Microsoft Power Apps izberite **Projekti** in nato v zgornjem desnem kotu izberite **Nov projekt**, da izberete javne predloge.</span><span class="sxs-lookup"><span data-stu-id="16e99-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="16e99-116">Naslednja predloga in temeljno opravilo se uporabljata za sinhronizacijo opravil projekta iz rešitve Project Service Automation v Finance:</span><span class="sxs-lookup"><span data-stu-id="16e99-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="16e99-117">**Ime predloge v integraciji podatkov:** opravila projekta (PSA v Fin in Ops)</span><span class="sxs-lookup"><span data-stu-id="16e99-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="16e99-118">**Ime opravila v projektu:** opravila projekta</span><span class="sxs-lookup"><span data-stu-id="16e99-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="16e99-119">Preden lahko pride do sinhronizacije opravil projekta, morate sinhronizirati projektne pogodbe in projekte.</span><span class="sxs-lookup"><span data-stu-id="16e99-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="16e99-120">Nabor entitet</span><span class="sxs-lookup"><span data-stu-id="16e99-120">Entity set</span></span>

| <span data-ttu-id="16e99-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="16e99-121">Project Service Automation</span></span> | <span data-ttu-id="16e99-122">Finance</span><span class="sxs-lookup"><span data-stu-id="16e99-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="16e99-123">Opravila projekta</span><span class="sxs-lookup"><span data-stu-id="16e99-123">Project Tasks</span></span>              | <span data-ttu-id="16e99-124">Integracijska entiteta za opravilo projekta</span><span class="sxs-lookup"><span data-stu-id="16e99-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="16e99-125">Potek entitete</span><span class="sxs-lookup"><span data-stu-id="16e99-125">Entity flow</span></span>

<span data-ttu-id="16e99-126">Ocene opravil projekta se upravljajo v rešitvi Project Service Automation in sinhronizirajo v Finance kot napovedi dejavnosti projekta.</span><span class="sxs-lookup"><span data-stu-id="16e99-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="16e99-127">Predpogoji in nastavitev preslikave</span><span class="sxs-lookup"><span data-stu-id="16e99-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="16e99-128">Preden lahko pride do sinhronizacije opravil projekta, morate sinhronizirati projektne pogodbe in projekte.</span><span class="sxs-lookup"><span data-stu-id="16e99-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="16e99-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="16e99-129">Power Query</span></span>

<span data-ttu-id="16e99-130">Če je ta pogoj izpolnjen, morate za filtriranje podatkov uporabiti rešitev Microsoft Power Query for Excel:</span><span class="sxs-lookup"><span data-stu-id="16e99-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="16e99-131">V opravilu projekta imate zapise, povezane z viri.</span><span class="sxs-lookup"><span data-stu-id="16e99-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="16e99-132">Če morate uporabiti rešitev Power Query, upoštevajte navodila:</span><span class="sxs-lookup"><span data-stu-id="16e99-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="16e99-133">Predloga opravil projekta (PSA v Fin in Ops) ima privzeti filter, ki iz opravila projekta izključi zapise, povezane z viri, tako, da filter v možnosti **IsLineTask** nastavi na **Napačno**.</span><span class="sxs-lookup"><span data-stu-id="16e99-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="16e99-134">Če ustvarite svojo predlogo, morate dodati ta filter.</span><span class="sxs-lookup"><span data-stu-id="16e99-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="16e99-135">Preslikava predlog v Integraciji podatkov</span><span class="sxs-lookup"><span data-stu-id="16e99-135">Template mapping in Data integration</span></span>

<span data-ttu-id="16e99-136">Naslednja ilustracija prikazuje primer preslikave predloge opravila v integracijo podatkov.</span><span class="sxs-lookup"><span data-stu-id="16e99-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="16e99-137">Preslikava prikazuje informacije o polju, ki bodo sinhronizirane iz rešitve Project Service Automation v Finance.</span><span class="sxs-lookup"><span data-stu-id="16e99-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="16e99-138">[![Preslikava predloge](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="16e99-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]