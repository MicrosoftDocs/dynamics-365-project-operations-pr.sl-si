---
title: Posodobitev storitve Project Operations v okolju Finance
description: Ta tema vsebuje informacije o tem, kako posodobite Project Operations v okolju Dynamics 365 Finance.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291999"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="9dc36-103">Posodobitev storitve Project Operations v okolju Finance</span><span class="sxs-lookup"><span data-stu-id="9dc36-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="9dc36-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="9dc36-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="9dc36-105">Ta tema vsebuje informacije o tem, kako posodobite Dynamics 365 Project Operations v okolju Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="9dc36-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="9dc36-106">Trije postopki so obvezni za posodobitev storitve Project Operations na posodobitev 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="9dc36-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="9dc36-107">Uvoz paketa v projekt predogledne različice</span><span class="sxs-lookup"><span data-stu-id="9dc36-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="9dc36-108">Uveljavitev posodobitve</span><span class="sxs-lookup"><span data-stu-id="9dc36-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="9dc36-109">Posodobitev okolja Dataverse</span><span class="sxs-lookup"><span data-stu-id="9dc36-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="9dc36-110">Uvoz paketa v projekt LCS</span><span class="sxs-lookup"><span data-stu-id="9dc36-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="9dc36-111">Prijavite se v storitve [Lifecycle Services (LCS)](https://lcs.dynamics.com/) kot lastnik projekta ali kot upravitelj okolja.</span><span class="sxs-lookup"><span data-stu-id="9dc36-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="9dc36-112">Na seznamu projektov izberite svoj projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="9dc36-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="9dc36-113">Na strani **Projekt** v skupini **Okolja** odprite okolje, ki ga želite posodobiti.</span><span class="sxs-lookup"><span data-stu-id="9dc36-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="9dc36-114">Prepričajte se, da se okolje izvaja.</span><span class="sxs-lookup"><span data-stu-id="9dc36-114">Verify that the environment is running.</span></span> <span data-ttu-id="9dc36-115">Če ni zagnano, zaženite okolje.</span><span class="sxs-lookup"><span data-stu-id="9dc36-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="9dc36-116">V razdelku **Nova izdaja** pod možnostjo **Razpoložljive posodobitve** izberite **Ogled posodobitev** za 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="9dc36-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Ogled gumba za posodobitev](media/view-update.png)

6. <span data-ttu-id="9dc36-118">Na strani **Binarne posodobitve** izberite **Shrani paket**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="9dc36-119">Na strani **Preglej in shrani posodobitve** izberite **Shrani paket**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="9dc36-120">V podoknu **Shrani paket v knjižnico sredstev**, ki se odpre, vnesite ime paketa in nato izberite **Shrani paket**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="9dc36-121">Ko LCS konča shranjevanje paketa, je gumb **Končano** omogočen.</span><span class="sxs-lookup"><span data-stu-id="9dc36-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="9dc36-122">Izberite **Dokončano**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-122">Select **Done**.</span></span> <span data-ttu-id="9dc36-123">Storitev LCS bo preverila paket.</span><span class="sxs-lookup"><span data-stu-id="9dc36-123">LCS will verify the package.</span></span> <span data-ttu-id="9dc36-124">Preverjanje lahko traja nekaj minut ali do ene ure.</span><span class="sxs-lookup"><span data-stu-id="9dc36-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="9dc36-125">Uporabite posodobitev paketa</span><span class="sxs-lookup"><span data-stu-id="9dc36-125">Apply the package update</span></span>

1. <span data-ttu-id="9dc36-126">V LCS na strani **Podrobnosti o okolju** izberite **Ohranjaj** > **Uporabi posodobitve**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="9dc36-127">Na seznamu izberite paket, ki ste ga prej shranili, in nato izberite **Uporabi**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="9dc36-128">Izberite **Da**, da potrdite, da želite uvesti paket.</span><span class="sxs-lookup"><span data-stu-id="9dc36-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Potrdite pogovorno okno za uvajanje paketa](media/confirm-package-deployment.png)

4. <span data-ttu-id="9dc36-130">Izberite **Da**, da potrdite, da želite posodobiti aplikacijo.</span><span class="sxs-lookup"><span data-stu-id="9dc36-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Potrdite pogovorno okno za posodobitev aplikacije](media/confirm-application-update.png)

<span data-ttu-id="9dc36-132">Uvajanje in posodobitev aplikacije se začne.</span><span class="sxs-lookup"><span data-stu-id="9dc36-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="9dc36-133">Na strani **Podrobnosti o okolju** v zgornjem desnem kotu se stanje okolja posodobi na **Vzdrževanje**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="9dc36-134">V približno dveh urah se posodobitev konča.</span><span class="sxs-lookup"><span data-stu-id="9dc36-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="9dc36-135">Informacije o izdaji aplikacije se posodobijo na **Microsoft Dynamics 365 for Finance and Operations 10.0.15** in stanje okolja se posodobi na **Uvedeno**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="9dc36-136">Posodobitev okolja Dataverse</span><span class="sxs-lookup"><span data-stu-id="9dc36-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="9dc36-137">Vpišite se v [skrbniško središče za Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="9dc36-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="9dc36-138">Na seznamu poiščite in odprite okolje, ki ste ga uporabili za namestitev storitve Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9dc36-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="9dc36-139">Na strani **Okolja** izberite **Vir** > **Aplikacije Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="9dc36-140">Na seznamu poiščite **Microsoft Dynamics 365 Project Operations** in v stolpcu **Stanje** izberite **Na voljo je posodobitev**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="9dc36-141">Izberite potrditveno polje **Strinjam se s pogoji storitve** in nato izberite **Posodobi**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="9dc36-142">Nameščena bo najnovejša različica rešitve.</span><span class="sxs-lookup"><span data-stu-id="9dc36-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="9dc36-143">Po končani namestitvi boste imeli nameščeno različico 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="9dc36-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="9dc36-144">Konfiguracija novih funkcij</span><span class="sxs-lookup"><span data-stu-id="9dc36-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="9dc36-145">Omogočanje preslikave dvojnega zapisovanja</span><span class="sxs-lookup"><span data-stu-id="9dc36-145">Enable dual-write mapping</span></span>

<span data-ttu-id="9dc36-146">Ko končate posodobitev v okoljih Finance in Dataverse, lahko omogočite zahtevane preslikave dvojnega zapisovanja.</span><span class="sxs-lookup"><span data-stu-id="9dc36-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="9dc36-147">Dokončajte naslednje postopke, da omogočite preslikave dvojnega zapisovanja.</span><span class="sxs-lookup"><span data-stu-id="9dc36-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="9dc36-148">Posodobitev varnostnih nastavitev v okolju Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="9dc36-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="9dc36-149">Osvežitev entitet podatkov</span><span class="sxs-lookup"><span data-stu-id="9dc36-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="9dc36-150">Posodobitev in zagon preslikav dvojnega zapisovanja</span><span class="sxs-lookup"><span data-stu-id="9dc36-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="9dc36-151">Posodobitev varnostnih nastavitev v okolju Dataverse</span><span class="sxs-lookup"><span data-stu-id="9dc36-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="9dc36-152">Naslednje posodobitve varnostnih pravic za entitete so zahtevane kot del posodobitve na UR5.</span><span class="sxs-lookup"><span data-stu-id="9dc36-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="9dc36-153">V svojem okolju Dataverse pojdite na **Nastavitve** in v skupini **Sistem** izberite **Varnost**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Nastavitve okolja Dataverse](media/Picture21.png)

2. <span data-ttu-id="9dc36-155">Izberite **Varnostne vloge**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="9dc36-156">Na seznamu vlog izberite **uporabnik aplikacije dvojnega zapisovanja** in izberite zavihek **Entitete po meri**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="9dc36-157">Prepričajte se, da ima vloga dovoljenji **Branje** in **Prilaganje k** za:</span><span class="sxs-lookup"><span data-stu-id="9dc36-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="9dc36-158">**Vrsta menjalnega tečaja valute**</span><span class="sxs-lookup"><span data-stu-id="9dc36-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="9dc36-159">**Kontni načrt**</span><span class="sxs-lookup"><span data-stu-id="9dc36-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="9dc36-160">**Poslovni koledar**</span><span class="sxs-lookup"><span data-stu-id="9dc36-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="9dc36-161">**Knjiga**</span><span class="sxs-lookup"><span data-stu-id="9dc36-161">**Ledger**</span></span>

5. <span data-ttu-id="9dc36-162">Ko je varnostna vloga posodobljena, pojdite na **Nastavitve** > **Varnost** > **Ekipe**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="9dc36-163">Prepričajte se, da je bila vloga **uporabnik aplikacije dvojnega zapisovanja** uporabljena za ekipo.</span><span class="sxs-lookup"><span data-stu-id="9dc36-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="9dc36-164">Osvežitev entitet podatkov iz posodobitve</span><span class="sxs-lookup"><span data-stu-id="9dc36-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="9dc36-165">V svojem okolju Finance odprite delovni prostor **Upravljanje podatkov** in nato odprite stran **Parametri ogrodja**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="9dc36-166">Na zavihku **Nastavitve entitete** izberite **Osvežitev seznama entitet**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="9dc36-167">Izberite **Zapri**, da potrdite osvežitev entitet.</span><span class="sxs-lookup"><span data-stu-id="9dc36-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="9dc36-168">Ta postopek do konca traja približno 20 minut.</span><span class="sxs-lookup"><span data-stu-id="9dc36-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="9dc36-169">Ko je osvežitev končana, boste obveščeni.</span><span class="sxs-lookup"><span data-stu-id="9dc36-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="9dc36-170">Posodobitev preslikav dvojnega zapisovanja</span><span class="sxs-lookup"><span data-stu-id="9dc36-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="9dc36-171">V delovnem prostoru **Upravljanje podatkov** izberite **Dvojno zapisovanje**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="9dc36-172">Izberite **Uporabi rešitvi**, izberite obe rešitvi na seznamu in nato izberite **Uporabi**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="9dc36-173">Na strani **Dvojno zapisovanje** izberite naslednje preslikave tabel in nato izberite **Ustavi**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="9dc36-174">**Dejanske vrednosti integracije storitve Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="9dc36-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="9dc36-175">**Kategorije stroškov projekta za integracijo storitve Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="9dc36-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="9dc36-176">**Entiteta za izvoz stroškov projekta dejanskih vrednosti integracije storitve Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="9dc36-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="9dc36-177">Na strani **Različica preslikave tabele** uporabite novo različico preslikave za vsako od treh entitet.</span><span class="sxs-lookup"><span data-stu-id="9dc36-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="9dc36-178">Na strani **Dvojno zapisovanje** izberite izvajanje za ponovni zagon preslikav.</span><span class="sxs-lookup"><span data-stu-id="9dc36-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="9dc36-179">Na seznamu preslikav izberite preslikavo **Knjiga (msdyn_ledgers)** z vsemi zahtevami in izberite potrditveno polje **Začetna sinhronizacija**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="9dc36-180">V polju **Glavni za začetno sinhronizacijo** izberite **Aplikacije Finance and Operations** in nato izberite **Zagon**.</span><span class="sxs-lookup"><span data-stu-id="9dc36-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Sinhronizacija preslikave knjige](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]