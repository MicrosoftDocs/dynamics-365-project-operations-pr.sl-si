---
title: Učinkovitost razporejanja projektnih virov
description: Ta tema vsebuje informacije o tem, kako izboljšati učinkovitost razporejanja virov za veliko število projektov.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084739"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="2ea70-103">Učinkovitost razporejanja projektnih virov</span><span class="sxs-lookup"><span data-stu-id="2ea70-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="2ea70-104">Težave z učinkovitostjo, povezane z razporejanjem virov, se lahko pojavijo, ko število projektov postane večje od tisoč.</span><span class="sxs-lookup"><span data-stu-id="2ea70-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="2ea70-105">Za izboljšanje učinkovitosti razporejanja virov je na voljo funkcija, ki uporabnikom omogoča, da skrajšajo čas, potreben za zagon obrazca o razpoložljivosti virov.</span><span class="sxs-lookup"><span data-stu-id="2ea70-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="2ea70-106">Odpravlja namreč postopek sinhronizacije za zbiranje zmogljivosti vira in uporablja tabelo **ResProjectResource** za hitrejše iskanje virov.</span><span class="sxs-lookup"><span data-stu-id="2ea70-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="2ea70-107">Upoštevajte, da se tabela **ResRollup** ne bo več uporabljala.</span><span class="sxs-lookup"><span data-stu-id="2ea70-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ea70-108">Če obstaja odvisnost bodisi od postopka sinhronizacije za zbiranje zmogljivosti vira bodisi od tabele **ResProjectResource** , ne uporabljajte te funkcije.</span><span class="sxs-lookup"><span data-stu-id="2ea70-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="2ea70-109">Omogočanje funkcije za izboljšanje učinkovitosti razporejanja virov</span><span class="sxs-lookup"><span data-stu-id="2ea70-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="2ea70-110">Če želite omogočiti funkcijo za izboljšanje učinkovitosti razporejanja virov, upoštevajte ta navodila.</span><span class="sxs-lookup"><span data-stu-id="2ea70-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="2ea70-111">Izberite **Upravljanje funkcij** > **Vse** in na seznamu funkcij poiščite **Omogoči funkcijo za izboljšanje učinkovitosti razporejanja projektnih virov**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="2ea70-112">Izberite **Omogoči zdaj**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="2ea70-113">Če funkcije ne najdete na seznamu, izberite **Preveri, ali so na voljo posodobitve** , da osvežite seznam.</span><span class="sxs-lookup"><span data-stu-id="2ea70-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="2ea70-114">Osvežite brskalnik in izberite **Vodenje projektov in računovodstvo** > **Redno** > **Projektni viri** > **Sinhroniziraj zmogljivosti vira v koledarjih v vseh podjetjih**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="2ea70-115">Nastavite **Odstrani obstoječe zapise o zmogljivosti** na **Da** , da odstranite prejšnje podatke.</span><span class="sxs-lookup"><span data-stu-id="2ea70-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="2ea70-116">Če želite ustvariti postopne podatke, možnost nastavite na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="2ea70-117">V polju **Koda obdobij** izberite obdobje, v katerem naj se ustvarijo podatki.</span><span class="sxs-lookup"><span data-stu-id="2ea70-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="2ea70-118">Če izberete kodo obdobij, začetnega in končnega datuma ni treba določiti.</span><span class="sxs-lookup"><span data-stu-id="2ea70-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="2ea70-119">Če pustite polje **Koda obdobij** prazno, izberite določene začetne in končne datume za ustvarjanje podatkov.</span><span class="sxs-lookup"><span data-stu-id="2ea70-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="2ea70-120">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="2ea70-121">S tem se bo tabela **ResCalendarCapacity** izpolnila s splošnimi podatki za vsa podjetja v vašem okolju, zato je treba paketno opravilo izvesti samo pri eni pravni osebi.</span><span class="sxs-lookup"><span data-stu-id="2ea70-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="2ea70-122">Podatki pri tem paketnem opravilu so potrebni za izračun zmogljivosti vira prek povezanega koledarja.</span><span class="sxs-lookup"><span data-stu-id="2ea70-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="2ea70-123">Izberite **Vodenje projektov in računovodstvo** > **Redno** > **Projektni viri** > **Izpolni projektne vire za vsa podjetja** in nato izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="2ea70-124">To je skript za nadgradnjo podatkov, in sicer za splošne podatke v tabelah **ResProjectResource** , **ResCalendarDateTimeRange** in **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="2ea70-125">Vrednosti za polje **PSAPRojSchedRole.RootActivity** se tudi posodobijo.</span><span class="sxs-lookup"><span data-stu-id="2ea70-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="2ea70-126">Če se to ne zažene, boste prejeli opozorilo, ko boste poskušali izvesti postopke razporejanja virov.</span><span class="sxs-lookup"><span data-stu-id="2ea70-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="2ea70-127">Izklop funkcije za izboljšanje učinkovitosti razporejanja virov</span><span class="sxs-lookup"><span data-stu-id="2ea70-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="2ea70-128">Izberite **Upravljanje funkcij** > **Vse** in poiščite **Omogoči funkcijo za izboljšanje učinkovitosti razporejanja projektnih virov**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="2ea70-129">Izberite funkcijo in nato izberite **Onemogoči**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="2ea70-130">Osvežite brskalnik.</span><span class="sxs-lookup"><span data-stu-id="2ea70-130">Refresh your browser.</span></span>
4. <span data-ttu-id="2ea70-131">Izberite **Vodenje projektov in računovodstvo** > **Redno** > **Sinhronizacija zmogljivosti** > **Sinhronizacija zbiranj zmogljivosti vira**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="2ea70-132">Na strani **Sinhronizacija zbiranj zmogljivosti vira** nastavite **Odstrani obstoječe zapise o zmogljivosti** na **Da** , da odstranite prejšnje podatke.</span><span class="sxs-lookup"><span data-stu-id="2ea70-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="2ea70-133">Če želite ustvariti postopne podatke, možnost nastavite na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="2ea70-134">V polju **Koda obdobij** izberite obdobje, v katerem naj se ustvarijo podatki.</span><span class="sxs-lookup"><span data-stu-id="2ea70-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="2ea70-135">Če izberete kodo obdobij, začetnega in končnega datuma ni treba določiti.</span><span class="sxs-lookup"><span data-stu-id="2ea70-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="2ea70-136">Če pustite polje **Koda obdobij** prazno, izberite določene začetne in končne datume za ustvarjanje podatkov.</span><span class="sxs-lookup"><span data-stu-id="2ea70-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="2ea70-137">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="2ea70-138">S tem se bo tabela **ResRollup** izpolnila s splošnimi podatki za vsa podjetja v vašem okolju, zato je treba paketno opravilo izvesti samo pri eni pravni osebi.</span><span class="sxs-lookup"><span data-stu-id="2ea70-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="2ea70-139">To paketno opravilo je potrebno za vse poglede za **razpoložljivost virov**.</span><span class="sxs-lookup"><span data-stu-id="2ea70-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="2ea70-140">Če se to paketno opravilo ne zažene, bodo podatki **ResRollup** bodo ustvarjeni sproti, kar lahko traja nekaj časa.</span><span class="sxs-lookup"><span data-stu-id="2ea70-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
