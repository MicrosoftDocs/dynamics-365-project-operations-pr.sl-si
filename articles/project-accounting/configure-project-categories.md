---
title: Konfiguracija kategorij projekta
description: Ta tema vsebuje informacije o nastavitvah kategorij projekta.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131948"
---
# <a name="configure-project-categories"></a><span data-ttu-id="54a7b-103">Konfiguracija kategorij projekta</span><span class="sxs-lookup"><span data-stu-id="54a7b-103">Configure project categories</span></span>

<span data-ttu-id="54a7b-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="54a7b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="54a7b-105">Aplikacija Project Operations ponuja zanesljive zmogljivosti za kategorizacijo prihodkov in odhodkov za posamezni projekt.</span><span class="sxs-lookup"><span data-stu-id="54a7b-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="54a7b-106">Kategorije omogočajo poročanje in analizo projektnih transakcij ter vodenje knjiženja v glavni knjigi.</span><span class="sxs-lookup"><span data-stu-id="54a7b-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="54a7b-107">Naslednji diagram prikazuje korelacijo med kategorijami transakcij, skupnimi kategorijami in kategorijami projektov.</span><span class="sxs-lookup"><span data-stu-id="54a7b-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="54a7b-108">Kategorije transakcij so osnovna skupina za projektne transakcije.</span><span class="sxs-lookup"><span data-stu-id="54a7b-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="54a7b-109">Znotraj te skupine obstaja nabor skupnih kategorij, ki jih je mogoče deliti med aplikacijami in moduli.</span><span class="sxs-lookup"><span data-stu-id="54a7b-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="54a7b-110">Še bolj podrobno, kategorije projekta so najbolj natančna raven kategorij.</span><span class="sxs-lookup"><span data-stu-id="54a7b-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="54a7b-111">Kategorije projektov so lastne posamezni pravni osebi, modulu in aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="54a7b-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korelacija med kategorijami transakcij, skupnimi kategorijami in kategorijami projektov](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="54a7b-113">Kategorije transakcij</span><span class="sxs-lookup"><span data-stu-id="54a7b-113">Transaction categories</span></span>

<span data-ttu-id="54a7b-114">Kategorije transakcij predstavljajo osnovno razvrščanje projektnih transakcij in niso določene glede na podjetje ali vrsto transakcije.</span><span class="sxs-lookup"><span data-stu-id="54a7b-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="54a7b-115">Družba Contoso Robotics na primer za razvrščanje projektnih transakcij uporablja kategorije načrtovanja, potovanja, namestitve in storitvenih transakcij.</span><span class="sxs-lookup"><span data-stu-id="54a7b-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="54a7b-116">Kategorije transakcij so definirane v modulu Project Operations.</span><span class="sxs-lookup"><span data-stu-id="54a7b-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="54a7b-117">Obrazec lahko odprete v razdelku **Nastavitve** \> **Kategorije transakcij**.</span><span class="sxs-lookup"><span data-stu-id="54a7b-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="54a7b-118">Ustvarite novo kategorijo transakcij bodisi z izbiro možnosti **Novo** ali pa z izbiro možnosti **Uvoz iz Excela**.</span><span class="sxs-lookup"><span data-stu-id="54a7b-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="54a7b-119">Kategorije v skupni rabi</span><span class="sxs-lookup"><span data-stu-id="54a7b-119">Shared categories</span></span>

<span data-ttu-id="54a7b-120">Rešitev Dynamics 365 uporablja skupno rabo kategorij za kategorizacijo stroškov v različnih aplikacijah, kot so npr. Dynamics 365 Finance, Dynamics 365 Supply Chain in Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="54a7b-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="54a7b-121">Za vsako ustvarjeno kategorijo transakcij aplikacija Project Operations samodejno ustvari štiri povezane kategorije v skupni rabi: ure, stroški, provizije in postavka.</span><span class="sxs-lookup"><span data-stu-id="54a7b-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="54a7b-122">Kategorije v skupni rabi lahko pregledate in prilagodite v razdelku **Vodenje projektov in računovodstvo** \> **Nastavitve** \> **Kategorije** \> **Kategorije v skupni rabi**.</span><span class="sxs-lookup"><span data-stu-id="54a7b-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="54a7b-123">Projektne kategorije</span><span class="sxs-lookup"><span data-stu-id="54a7b-123">Project categories</span></span>

<span data-ttu-id="54a7b-124">Projektne kategorije predstavljajo najpodrobnejšo raven konfiguracije kategorij. Projektni računovodja jih mora konfigurirati posebej in za vsako posamezno podjetje.</span><span class="sxs-lookup"><span data-stu-id="54a7b-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="54a7b-125">Odprite razdelek **Vodenje projektov in računovodstvo** \> **Nastavitve** \> **Kategorije** \> **Kategorije projektov**.</span><span class="sxs-lookup"><span data-stu-id="54a7b-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="54a7b-126">Izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="54a7b-126">Select **New**.</span></span>
3. <span data-ttu-id="54a7b-127">Izberite **ID kategorije** v skupni rabi, ki ste jo ustvarili v prejšnjem razdelku.</span><span class="sxs-lookup"><span data-stu-id="54a7b-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="54a7b-128">Aplikacija Project Operations omogoča uporabo samo tistih kategorij v skupni rabi, ki so povezane s kategorijami transakcij.</span><span class="sxs-lookup"><span data-stu-id="54a7b-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="54a7b-129">Izberite skupino kategorij.</span><span class="sxs-lookup"><span data-stu-id="54a7b-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="54a7b-130">Skupine kategorij</span><span class="sxs-lookup"><span data-stu-id="54a7b-130">Category groups</span></span>

<span data-ttu-id="54a7b-131">Skupine kategorij se uporabljajo za skupno rabo lastnosti, predvsem knjiženje profilov med sorodnimi kategorijami projekta.</span><span class="sxs-lookup"><span data-stu-id="54a7b-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="54a7b-132">Za vsako vrsto transakcije mora obstajati vsaj ena skupina kategorij, vsaki kategoriji projekta pa je dodeljena skupina.</span><span class="sxs-lookup"><span data-stu-id="54a7b-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="54a7b-133">Specifikacije knjiženja v aplikaciji Project Operations so opredeljene s pravili za profil stroškov in prihodkov, kategorijami projektov in skupinami kategorij.</span><span class="sxs-lookup"><span data-stu-id="54a7b-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="54a7b-134">Skupine kategorij lahko nastavite v razdelku **Vodenje projektov in računovodstvo** \> **Nastavitve** \> **Kategorije** \> **Skupine kategorij**.</span><span class="sxs-lookup"><span data-stu-id="54a7b-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
