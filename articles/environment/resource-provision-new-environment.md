---
title: Omogočanje novega okolja
description: Ta tema vsebuje informacije o omogočanju novega okolja v storitvi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643011"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="8f885-103">Omogočanje novega okolja</span><span class="sxs-lookup"><span data-stu-id="8f885-103">Provision a new environment</span></span>

<span data-ttu-id="8f885-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="8f885-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8f885-105">Ta tema vsebuje informacije o tem, kako zagotoviti novo okolje Dynamics 365 Project Operations za primere uporabe z viri/brez zalog.</span><span class="sxs-lookup"><span data-stu-id="8f885-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="8f885-106">Omogočite avtomatizirano omogočanje uporabe storitve Project Operations v projektu LCS</span><span class="sxs-lookup"><span data-stu-id="8f885-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="8f885-107">Uporabite naslednje korake, da omogočite avtomatizirano omogočanje uporabe storitve Project Operations za vaš projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="8f885-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="8f885-108">Odprite [LCS](https://lcs.dynamics.com/v2) in izberite ploščico **Upravljanje funkcije predogleda**.</span><span class="sxs-lookup"><span data-stu-id="8f885-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="8f885-109">V seznamu **Funkcija predogleda** izberite **Funkcija Project Operations** in izberite **Omogoči funkcijo predogleda**, da omogočite storitev Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8f885-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="8f885-110">Ta korak se izvede samo enkrat za posamezni projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="8f885-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="8f885-111">Omogočanje uporabe okolja Project Operations</span><span class="sxs-lookup"><span data-stu-id="8f885-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="8f885-112">Odprite novo [predstavitveno okolje](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance ali [preskusno/produkcijsko okolje](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) za uvedbo.</span><span class="sxs-lookup"><span data-stu-id="8f885-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="8f885-113">Sprehodite se skozi čarovnika **Omogočanje okolja**.</span><span class="sxs-lookup"><span data-stu-id="8f885-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8f885-114">Prepričajte se, da je izbrana različica aplikacije 10.0.13 ali novejša.</span><span class="sxs-lookup"><span data-stu-id="8f885-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="8f885-115">če želite omogočiti storitev Project Operations odprite možnost **Napredne nastavitve** in izberite **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="8f885-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="8f885-116">Omogočite **Nastavitev Common Data Service**, tako da izberete **Da** in vnesite podatke v zahtevana polja:</span><span class="sxs-lookup"><span data-stu-id="8f885-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="8f885-117">Imenu</span><span class="sxs-lookup"><span data-stu-id="8f885-117">Name</span></span>
  - <span data-ttu-id="8f885-118">Regija</span><span class="sxs-lookup"><span data-stu-id="8f885-118">Region</span></span>
  - <span data-ttu-id="8f885-119">Language</span><span class="sxs-lookup"><span data-stu-id="8f885-119">Language</span></span>
  - <span data-ttu-id="8f885-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="8f885-120">Currency</span></span>
 
5. <span data-ttu-id="8f885-121">V polju **Predloga Common Data Service** izberite **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="8f885-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="8f885-122">Izberite vrsto okolja za vašo uvedbo.</span><span class="sxs-lookup"><span data-stu-id="8f885-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="8f885-123">Preskus na podlagi naročnine vam bo omogočil uvedbo okolja CDS za 30 dni.</span><span class="sxs-lookup"><span data-stu-id="8f885-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Nastavitve uvedbe](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="8f885-125">Izberite možnost **Strinjam se**, da potrdite pogoje storitve, nato izberite **Končano**, da se vrnete v nastavitve uvajanja.</span><span class="sxs-lookup"><span data-stu-id="8f885-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Soglasje uvedbe](./media/2DeploymentConsent.png)

7. <span data-ttu-id="8f885-127">Izpolnite preostala zahtevana polja v čarovniku in potrdite uvajanje.</span><span class="sxs-lookup"><span data-stu-id="8f885-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="8f885-128">Čas omogočanja uporabe okolja se razlikuje glede na vrsto okolja.</span><span class="sxs-lookup"><span data-stu-id="8f885-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="8f885-129">Omogočanje uporabe lahko traja do šest ur.</span><span class="sxs-lookup"><span data-stu-id="8f885-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="8f885-130">Ko se uvajanje uspešno zaključi, bo okolje prikazano kot **Uvedeno**.</span><span class="sxs-lookup"><span data-stu-id="8f885-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="8f885-131">Če želite potrditi, da je bilo okolje uspešno uvedeno, izberite **Prijava** in se prijavite v okolje.</span><span class="sxs-lookup"><span data-stu-id="8f885-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Podrobnosti o okoljih v storitvi ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="8f885-133">Uporaba predstavitvenih podatkov storitve Project Operations Finance (izbirni korak)</span><span class="sxs-lookup"><span data-stu-id="8f885-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="8f885-134">Uporabite predstavitvene podatke storitve Project Operations Finance za izdajo v oblaku gostovane storitve 10.0.13, kot je opisano v [tem članku](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="8f885-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="8f885-135">Uporaba posodobitev za okolje Finance</span><span class="sxs-lookup"><span data-stu-id="8f885-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="8f885-136">Za storitev Project Operations je zahtevano okolje Finance z različico aplikacije **10.0.13 (10.0.569.20009)** ali novejšo.</span><span class="sxs-lookup"><span data-stu-id="8f885-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="8f885-137">Za prejem te različice boste morda morali zagnati posodobitev kakovosti svojega okolja Finance.</span><span class="sxs-lookup"><span data-stu-id="8f885-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="8f885-138">V LCS na strani **Podrobnosti o okolju** odprite razdelek **Razpoložljive posodobitve** in izberite **Prikaz posodobitev**.</span><span class="sxs-lookup"><span data-stu-id="8f885-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Prikaz posodobitev](./media/5ViewUpdates.png)

2. <span data-ttu-id="8f885-140">Na strani **Binarne posodobitve** izberite **Shrani paket**.</span><span class="sxs-lookup"><span data-stu-id="8f885-140">On the **Binary updates** page, select **Save package.**</span></span>

![Shrani paket](./media/6SavePackage.png)

3. <span data-ttu-id="8f885-142">Kliknite **Izberi vse** in nato **Shrani paket**.</span><span class="sxs-lookup"><span data-stu-id="8f885-142">Click **Select all** and then select **Save package**.</span></span>

![Pregled in shranjevanje posodobitev](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="8f885-144">Vnesite ime in opis paketa, nato pa izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="8f885-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="8f885-145">Ta postopek lahko traja nekaj časa, odvisno od internetne povezave.</span><span class="sxs-lookup"><span data-stu-id="8f885-145">Depending on the internet connection, this process might take some time.</span></span>

![Nalaganje paketa v knjižnico sredstev](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="8f885-147">Ko je paket shranjen, izberite možnost **Končano** in shranite ta paket v knjižnico sredstev v vašem projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="8f885-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="8f885-148">Shranjevanje in preverjanje veljavnosti paketa lahko traja približno 15 minut.</span><span class="sxs-lookup"><span data-stu-id="8f885-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="8f885-149">Če želite uporabiti posodobitev, pojdite na stran **Podrobnosti o okolju** v LCS in izberite **Vzdrževanje** > **Uporabi posodobitve**.</span><span class="sxs-lookup"><span data-stu-id="8f885-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Vzdrževanje okolij](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="8f885-151">Na seznamu posodobitev izberite paket, ki ste ga ustvarili, in izberite **Uporabi**.</span><span class="sxs-lookup"><span data-stu-id="8f885-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Uporabi posodobitve](./media/10ApplyUpdates.png)

<span data-ttu-id="8f885-153">Vzdrževanje okolja bo trajalo nekaj časa.</span><span class="sxs-lookup"><span data-stu-id="8f885-153">Environment servicing will take some time.</span></span> <span data-ttu-id="8f885-154">Ko bo končano, se bo okolje vrnilo v stanje ob uvedbi.</span><span class="sxs-lookup"><span data-stu-id="8f885-154">After it is complete, the environment will return to a deployed state.</span></span>

![Uvedeno okolje](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="8f885-156">Vzpostavite povezavo za dvojno zapisovanje</span><span class="sxs-lookup"><span data-stu-id="8f885-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="8f885-157">V projektu LCS odprite stran **Podrobnosti o okolju**.</span><span class="sxs-lookup"><span data-stu-id="8f885-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8f885-158">V možnosti **Informacije o okolju Common Data Service** izberite **Povezava do CDS-ja za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="8f885-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="8f885-159">Ko je povezava vzpostavljena, ponovno izberite **Povezava do CDS-ja za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="8f885-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="8f885-160">Preusmerjeni boste na funkcijo dvojnega zapisovanja v storitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="8f885-160">You will be redirected to Dual Write in Finance.</span></span>

![Povezava do CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="8f885-162">Izberite **Uporabi rešitev**, če želite dostopati do entitet, ki bodo preslikane v integraciji.</span><span class="sxs-lookup"><span data-stu-id="8f885-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Uporaba rešitev](./media/13ApplySolutions.png)

5. <span data-ttu-id="8f885-164">Izberite rešitvi **Preslikava entitete za dvojno pisanje Dynamics 365 Finance and Operations** in **Preslikava entitete za dvojno pisanje Dynamics 365 Project Operations** ter izberite **Uporabi**.</span><span class="sxs-lookup"><span data-stu-id="8f885-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Potrjevanje rešitev](./media/14ConfirmSolutions.png)

<span data-ttu-id="8f885-166">Po uporabi rešitev se entitete za dvojno zapisovanje uporabijo v samem okolju.</span><span class="sxs-lookup"><span data-stu-id="8f885-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Uporaba rešitev](./media/15ApplyingSolutions.png)

<span data-ttu-id="8f885-168">Po uporabi entitet se v okolju prikažejo vse razpoložljive preslikave.</span><span class="sxs-lookup"><span data-stu-id="8f885-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Zemljevidi entitet za dvojno zapisovanje](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="8f885-170">Po posodobitvi osvežite podatkovne vnose</span><span class="sxs-lookup"><span data-stu-id="8f885-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="8f885-171">V storitvi Finance odprite delovni prostor **Upravljanje podatkov**.</span><span class="sxs-lookup"><span data-stu-id="8f885-171">In Finance, go to the **Data management** workspace.</span></span>

![Delovni prostor »Upravljanje podatkov«](./media/16DataManagement.png)

2. <span data-ttu-id="8f885-173">Izberite ploščico **Parametri ogrodja**.</span><span class="sxs-lookup"><span data-stu-id="8f885-173">Select the **Framework parameters** tile.</span></span>

![Parametri ogrodja](./media/17FrameworkParameters.png)

3. <span data-ttu-id="8f885-175">Na strani **Nastavitve entitete** izberite **Osveži seznam entitet**.</span><span class="sxs-lookup"><span data-stu-id="8f885-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Osveži seznam entitet](./media/18RefreshEntityList.png)

<span data-ttu-id="8f885-177">Osveževanje bo trajalo približno 20 minut.</span><span class="sxs-lookup"><span data-stu-id="8f885-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="8f885-178">Ko bo končano, boste prejeli obvestilo.</span><span class="sxs-lookup"><span data-stu-id="8f885-178">You will receive an alert when it is complete.</span></span>

![Potrditev osveževanja](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="8f885-180">Zagon zemljevidov za dvojno zapisovanje v aplikaciji Project Operations</span><span class="sxs-lookup"><span data-stu-id="8f885-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="8f885-181">V projektu LCS odprite stran **Podrobnosti o okolju**.</span><span class="sxs-lookup"><span data-stu-id="8f885-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="8f885-182">V možnosti **Informacije o okolju Common Data Service** izberite **Povezava do CDS-ja za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="8f885-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="8f885-183">Ko izberete povezavo, boste preusmerjeni na seznam entitet v preslikavah.</span><span class="sxs-lookup"><span data-stu-id="8f885-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="8f885-184">Zaženite zemljevide, kot je opisano v naslednji tabeli.</span><span class="sxs-lookup"><span data-stu-id="8f885-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="8f885-185">Upoštevajte navedeno zaporedje.</span><span class="sxs-lookup"><span data-stu-id="8f885-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="8f885-186">**Preslikava entitete**</span><span class="sxs-lookup"><span data-stu-id="8f885-186">**Entity Map**</span></span> | <span data-ttu-id="8f885-187">**Osveži entiteto**</span><span class="sxs-lookup"><span data-stu-id="8f885-187">**Refresh entity**</span></span> | <span data-ttu-id="8f885-188">**Začetna sinhronizacija**</span><span class="sxs-lookup"><span data-stu-id="8f885-188">**Initial sync**</span></span> | <span data-ttu-id="8f885-189">**Glavni za začetno sinhronizacijo**</span><span class="sxs-lookup"><span data-stu-id="8f885-189">**Master for initial sync**</span></span> | <span data-ttu-id="8f885-190">**Zaženi predhodne zahteve**</span><span class="sxs-lookup"><span data-stu-id="8f885-190">**Run prerequisites**</span></span> | <span data-ttu-id="8f885-191">**Začetna sinhronizacija predhodnih zahtev**</span><span class="sxs-lookup"><span data-stu-id="8f885-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="8f885-192">**Vloge projektnih virov za vsa podjetja (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="8f885-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="8f885-193">No</span><span class="sxs-lookup"><span data-stu-id="8f885-193">No</span></span> | <span data-ttu-id="8f885-194">Da</span><span class="sxs-lookup"><span data-stu-id="8f885-194">Yes</span></span> | <span data-ttu-id="8f885-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8f885-195">Common Data Service</span></span> | <span data-ttu-id="8f885-196">No</span><span class="sxs-lookup"><span data-stu-id="8f885-196">No</span></span> | <span data-ttu-id="8f885-197">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-197">N\A</span></span> |
| <span data-ttu-id="8f885-198">**Pravne osebe (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="8f885-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="8f885-199">No</span><span class="sxs-lookup"><span data-stu-id="8f885-199">No</span></span> | <span data-ttu-id="8f885-200">Da</span><span class="sxs-lookup"><span data-stu-id="8f885-200">Yes</span></span> | <span data-ttu-id="8f885-201">Aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8f885-201">Finance and Operations apps</span></span> | <span data-ttu-id="8f885-202">No</span><span class="sxs-lookup"><span data-stu-id="8f885-202">No</span></span> | <span data-ttu-id="8f885-203">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-203">N\A</span></span> |
| <span data-ttu-id="8f885-204">**Knjiga (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="8f885-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="8f885-205">No</span><span class="sxs-lookup"><span data-stu-id="8f885-205">No</span></span> | <span data-ttu-id="8f885-206">Da</span><span class="sxs-lookup"><span data-stu-id="8f885-206">Yes</span></span> | <span data-ttu-id="8f885-207">Aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8f885-207">Finance and Operations apps</span></span> | <span data-ttu-id="8f885-208">Da</span><span class="sxs-lookup"><span data-stu-id="8f885-208">Yes</span></span> | <span data-ttu-id="8f885-209">Da, aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8f885-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="8f885-210">**Dejanske vrednosti integracije storitve Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="8f885-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="8f885-211">No</span><span class="sxs-lookup"><span data-stu-id="8f885-211">No</span></span> | <span data-ttu-id="8f885-212">No</span><span class="sxs-lookup"><span data-stu-id="8f885-212">No</span></span> | <span data-ttu-id="8f885-213">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-213">N\A</span></span> | <span data-ttu-id="8f885-214">Da</span><span class="sxs-lookup"><span data-stu-id="8f885-214">Yes</span></span> | <span data-ttu-id="8f885-215">No</span><span class="sxs-lookup"><span data-stu-id="8f885-215">No</span></span> |
| <span data-ttu-id="8f885-216">**Podrobnosti pogodbe (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="8f885-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="8f885-217">No</span><span class="sxs-lookup"><span data-stu-id="8f885-217">No</span></span> | <span data-ttu-id="8f885-218">No</span><span class="sxs-lookup"><span data-stu-id="8f885-218">No</span></span> | <span data-ttu-id="8f885-219">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-219">N\A</span></span> | <span data-ttu-id="8f885-220">No</span><span class="sxs-lookup"><span data-stu-id="8f885-220">No</span></span> | <span data-ttu-id="8f885-221">No</span><span class="sxs-lookup"><span data-stu-id="8f885-221">No</span></span> |
| <span data-ttu-id="8f885-222">**Integracijska entiteta za odnose projektne transakcije (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="8f885-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="8f885-223">No</span><span class="sxs-lookup"><span data-stu-id="8f885-223">No</span></span> | <span data-ttu-id="8f885-224">No</span><span class="sxs-lookup"><span data-stu-id="8f885-224">No</span></span> | <span data-ttu-id="8f885-225">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-225">N\A</span></span> | <span data-ttu-id="8f885-226">No</span><span class="sxs-lookup"><span data-stu-id="8f885-226">No</span></span> | <span data-ttu-id="8f885-227">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-227">N\A</span></span> |
| <span data-ttu-id="8f885-228">**Mejniki podrobnosti pogodbe o integraciji storitve Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="8f885-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="8f885-229">No</span><span class="sxs-lookup"><span data-stu-id="8f885-229">No</span></span> | <span data-ttu-id="8f885-230">No</span><span class="sxs-lookup"><span data-stu-id="8f885-230">No</span></span> | <span data-ttu-id="8f885-231">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-231">N\A</span></span> | <span data-ttu-id="8f885-232">No</span><span class="sxs-lookup"><span data-stu-id="8f885-232">No</span></span> | <span data-ttu-id="8f885-233">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-233">N\A</span></span> |
| <span data-ttu-id="8f885-234">**Integracijska entiteta za ocene stroškov v storitvi Project Operations (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="8f885-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="8f885-235">No</span><span class="sxs-lookup"><span data-stu-id="8f885-235">No</span></span> | <span data-ttu-id="8f885-236">No</span><span class="sxs-lookup"><span data-stu-id="8f885-236">No</span></span> | <span data-ttu-id="8f885-237">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-237">N\A</span></span> | <span data-ttu-id="8f885-238">No</span><span class="sxs-lookup"><span data-stu-id="8f885-238">No</span></span> | <span data-ttu-id="8f885-239">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-239">N\A</span></span> |
| <span data-ttu-id="8f885-240">**Entiteta za izvoz kategorije stroškov projekta pri integraciji storitve Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="8f885-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="8f885-241">No</span><span class="sxs-lookup"><span data-stu-id="8f885-241">No</span></span> | <span data-ttu-id="8f885-242">No</span><span class="sxs-lookup"><span data-stu-id="8f885-242">No</span></span> | <span data-ttu-id="8f885-243">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-243">N\A</span></span> | <span data-ttu-id="8f885-244">No</span><span class="sxs-lookup"><span data-stu-id="8f885-244">No</span></span> | <span data-ttu-id="8f885-245">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-245">N\A</span></span> |
| <span data-ttu-id="8f885-246">**Entiteta za izvoz stroškov projekta pri integraciji storitve Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="8f885-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="8f885-247">Da</span><span class="sxs-lookup"><span data-stu-id="8f885-247">Yes</span></span> | <span data-ttu-id="8f885-248">No</span><span class="sxs-lookup"><span data-stu-id="8f885-248">No</span></span> | <span data-ttu-id="8f885-249">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-249">N\A</span></span> | <span data-ttu-id="8f885-250">No</span><span class="sxs-lookup"><span data-stu-id="8f885-250">No</span></span> | <span data-ttu-id="8f885-251">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-251">N\A</span></span> |
| <span data-ttu-id="8f885-252">**Integracijska entiteta za oceno časa v storitvi Project Operations (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="8f885-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="8f885-253">Da</span><span class="sxs-lookup"><span data-stu-id="8f885-253">Yes</span></span> | <span data-ttu-id="8f885-254">No</span><span class="sxs-lookup"><span data-stu-id="8f885-254">No</span></span> | <span data-ttu-id="8f885-255">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-255">N\A</span></span> | <span data-ttu-id="8f885-256">No</span><span class="sxs-lookup"><span data-stu-id="8f885-256">No</span></span> | <span data-ttu-id="8f885-257">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="8f885-257">N\A</span></span> |


4. <span data-ttu-id="8f885-258">Če želite osvežiti entiteto, izberite ime zemljevida in nato **Osveži entitete**.</span><span class="sxs-lookup"><span data-stu-id="8f885-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Osveži zemljevid](./media/20RefreshMapping.png)

5. <span data-ttu-id="8f885-260">Po zaključenem osveževanju izvajajte zemljevid.</span><span class="sxs-lookup"><span data-stu-id="8f885-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="8f885-261">Preden omogočite naslednji zemljevid, preverite, ali je zemljevid v tabeli v stanju **Se izvaja**.</span><span class="sxs-lookup"><span data-stu-id="8f885-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="8f885-262">Izvajanje zemljevidov z večjim številom predhodnih zahtev lahko traja nekaj časa.</span><span class="sxs-lookup"><span data-stu-id="8f885-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="8f885-263">Za izvajanje zemljevida s predhodnimi zahtevami omogočite preklopno stikalo **Prikaz zemljevidov povezanih entitet**.</span><span class="sxs-lookup"><span data-stu-id="8f885-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="8f885-264">Če je v tabeli možnost **Predpogoj za začetno sinhronizacijo** nastavljena na **Ne**, preverite, ali je zastavica **Začetna sinhronizacija** nastavljena na **Izklopljeno** na vseh zahtevanih zemljevidih, preden jih zaženete.</span><span class="sxs-lookup"><span data-stu-id="8f885-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Zagon zemljevida](./media/21RunMap.png)

6. <span data-ttu-id="8f885-266">Preverite, ali se izvajajo vsi s projektom povezani zemljevidi.</span><span class="sxs-lookup"><span data-stu-id="8f885-266">Validate all project related maps are in the running state.</span></span>

![Vsi zemljevidi se izvajajo](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="8f885-268">Uporaba konfiguracijskih podatkov v storitvi CDS za Project Operations (izbirno)</span><span class="sxs-lookup"><span data-stu-id="8f885-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="8f885-269">Če ste predstavitvene podatke uporabili za okolje Finance in jih želite uporabiti v okolju CDS, glejte [Nastavitev in uporaba konfiguracijskih podatkov v storitvi Common Data Service za Project Operations](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="8f885-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="8f885-270">Vaše okolje Project Operations je zdaj omogočeno in konfigurirano.</span><span class="sxs-lookup"><span data-stu-id="8f885-270">Your Project Operations environment is now provisioned and configured.</span></span> 
