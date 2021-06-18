---
title: Omogočanje novega okolja
description: Ta tema vsebuje informacije o omogočanju novega okolja v storitvi Project Operations.
author: sigitac
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d0712d9d5dfc6c35ccd07142ff5948f50e6a254c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995506"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="71ede-103">Omogočanje novega okolja</span><span class="sxs-lookup"><span data-stu-id="71ede-103">Provision a new environment</span></span>

<span data-ttu-id="71ede-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="71ede-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="71ede-105">Ta tema vsebuje informacije o tem, kako zagotoviti novo okolje Dynamics 365 Project Operations za primere uporabe z viri/brez zalog.</span><span class="sxs-lookup"><span data-stu-id="71ede-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="71ede-106">Omogočite avtomatizirano omogočanje uporabe storitve Project Operations v projektu LCS</span><span class="sxs-lookup"><span data-stu-id="71ede-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="71ede-107">Uporabite naslednje korake, da omogočite avtomatizirano omogočanje uporabe storitve Project Operations za vaš projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="71ede-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="71ede-108">Odprite [LCS](https://lcs.dynamics.com/v2) in izberite ploščico **Upravljanje funkcije predogleda**.</span><span class="sxs-lookup"><span data-stu-id="71ede-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="71ede-109">V seznamu **Funkcija predogleda** izberite **Funkcija Project Operations** in izberite **Omogoči funkcijo predogleda**, da omogočite storitev Project Operations.</span><span class="sxs-lookup"><span data-stu-id="71ede-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="71ede-110">Ta korak se izvede samo enkrat za posamezni projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="71ede-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="71ede-111">Omogočanje uporabe okolja Project Operations</span><span class="sxs-lookup"><span data-stu-id="71ede-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="71ede-112">Odprite novo [predstavitveno okolje](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance ali [preskusno/produkcijsko okolje](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) za uvedbo.</span><span class="sxs-lookup"><span data-stu-id="71ede-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="71ede-113">Sprehodite se skozi čarovnika **Omogočanje okolja**.</span><span class="sxs-lookup"><span data-stu-id="71ede-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="71ede-114">Prepričajte se, da je izbrana različica aplikacije 10.0.13 ali novejša.</span><span class="sxs-lookup"><span data-stu-id="71ede-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="71ede-115">če želite omogočiti storitev Project Operations odprite možnost **Napredne nastavitve** in izberite **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="71ede-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="71ede-116">Omogočite **Nastavitev Common Data Service**, tako da izberete **Da** in vnesite podatke v zahtevana polja:</span><span class="sxs-lookup"><span data-stu-id="71ede-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="71ede-117">Imenu</span><span class="sxs-lookup"><span data-stu-id="71ede-117">Name</span></span>
  - <span data-ttu-id="71ede-118">Regija</span><span class="sxs-lookup"><span data-stu-id="71ede-118">Region</span></span>
  - <span data-ttu-id="71ede-119">Language</span><span class="sxs-lookup"><span data-stu-id="71ede-119">Language</span></span>
  - <span data-ttu-id="71ede-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="71ede-120">Currency</span></span>
 
5. <span data-ttu-id="71ede-121">V polju **Predloga Common Data Service** izberite **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="71ede-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="71ede-122">Izberite vrsto okolja za vašo uvedbo.</span><span class="sxs-lookup"><span data-stu-id="71ede-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="71ede-123">Preskus na podlagi naročnine vam bo omogočil uvedbo okolja CDS za 30 dni.</span><span class="sxs-lookup"><span data-stu-id="71ede-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Nastavitve uvedbe](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="71ede-125">Izberite možnost **Strinjam se**, da potrdite pogoje storitve, nato izberite **Končano**, da se vrnete v nastavitve uvajanja.</span><span class="sxs-lookup"><span data-stu-id="71ede-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Soglasje uvedbe](./media/2DeploymentConsent.png)

7. <span data-ttu-id="71ede-127">Izbirno – uporabi predstavitvene podatke v okolju.</span><span class="sxs-lookup"><span data-stu-id="71ede-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="71ede-128">Pojdite na **Napredne nastavitve**, izberite **Prilagajanje konfiguracije zbirke podatkov SQL** in nastavite **Določi nabor podatkov za zbirko podatkov aplikacije** na **Predstavitev**.</span><span class="sxs-lookup"><span data-stu-id="71ede-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="71ede-129">Izpolnite preostala zahtevana polja v čarovniku in potrdite uvajanje.</span><span class="sxs-lookup"><span data-stu-id="71ede-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="71ede-130">Čas za omogočanje okolja za uporabo se razlikuje na podlagi vrste okolja.</span><span class="sxs-lookup"><span data-stu-id="71ede-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="71ede-131">Omogočanje uporabe lahko traja do šest ur.</span><span class="sxs-lookup"><span data-stu-id="71ede-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="71ede-132">Ko se uvajanje uspešno zaključi, bo okolje prikazano kot **Uvedeno**.</span><span class="sxs-lookup"><span data-stu-id="71ede-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="71ede-133">Za potrditev, da je bilo okolje uspešno omogočeno za uporabo, izberite **Prijava** in se prijavite v okolje za potrditev.</span><span class="sxs-lookup"><span data-stu-id="71ede-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Podrobnosti o okoljih v storitvi ](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="71ede-135">Uporaba posodobitev za okolje Finance</span><span class="sxs-lookup"><span data-stu-id="71ede-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="71ede-136">Za storitev Project Operations je zahtevano okolje Finance z različico aplikacije **10.0.13 (10.0.569.20009)** ali novejšo.</span><span class="sxs-lookup"><span data-stu-id="71ede-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="71ede-137">Za prejem te različice boste morda morali zagnati posodobitev kakovosti svojega okolja Finance.</span><span class="sxs-lookup"><span data-stu-id="71ede-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="71ede-138">V LCS na strani **Podrobnosti o okolju** odprite razdelek **Razpoložljive posodobitve** in izberite **Prikaz posodobitev**.</span><span class="sxs-lookup"><span data-stu-id="71ede-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Prikaz posodobitev](./media/5ViewUpdates.png)

2. <span data-ttu-id="71ede-140">Na strani **Binarne posodobitve** izberite **Shrani paket**.</span><span class="sxs-lookup"><span data-stu-id="71ede-140">On the **Binary updates** page, select **Save package.**</span></span>

![Shrani paket](./media/6SavePackage.png)

3. <span data-ttu-id="71ede-142">Kliknite **Izberi vse** in nato **Shrani paket**.</span><span class="sxs-lookup"><span data-stu-id="71ede-142">Click **Select all** and then select **Save package**.</span></span>

![Pregled in shranjevanje posodobitev](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="71ede-144">Vnesite ime in opis paketa, nato pa izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="71ede-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="71ede-145">Ta postopek lahko traja nekaj časa, odvisno od internetne povezave.</span><span class="sxs-lookup"><span data-stu-id="71ede-145">Depending on the internet connection, this process might take some time.</span></span>

![Nalaganje paketa v knjižnico sredstev](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="71ede-147">Ko je paket shranjen, izberite možnost **Končano** in shranite ta paket v knjižnico sredstev v vašem projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="71ede-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="71ede-148">Shranjevanje in preverjanje veljavnosti paketa lahko traja približno 15 minut.</span><span class="sxs-lookup"><span data-stu-id="71ede-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="71ede-149">Če želite uporabiti posodobitev, pojdite na stran **Podrobnosti o okolju** v LCS in izberite **Vzdrževanje** > **Uporabi posodobitve**.</span><span class="sxs-lookup"><span data-stu-id="71ede-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Vzdrževanje okolij](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="71ede-151">Na seznamu posodobitev izberite paket, ki ste ga ustvarili, in izberite **Uporabi**.</span><span class="sxs-lookup"><span data-stu-id="71ede-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Uporabi posodobitve](./media/10ApplyUpdates.png)

<span data-ttu-id="71ede-153">Vzdrževanje okolja bo trajalo nekaj časa.</span><span class="sxs-lookup"><span data-stu-id="71ede-153">Environment servicing will take some time.</span></span> <span data-ttu-id="71ede-154">Ko bo končano, se bo okolje vrnilo v stanje ob uvedbi.</span><span class="sxs-lookup"><span data-stu-id="71ede-154">After it is complete, the environment will return to a deployed state.</span></span>

![Uvedeno okolje](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="71ede-156">Vzpostavite povezavo za dvojno zapisovanje</span><span class="sxs-lookup"><span data-stu-id="71ede-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="71ede-157">V projektu LCS odprite stran **Podrobnosti o okolju**.</span><span class="sxs-lookup"><span data-stu-id="71ede-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="71ede-158">V možnosti **Informacije o okolju Common Data Service** izberite **Povezava do CDS-ja za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="71ede-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="71ede-159">Ko je povezava vzpostavljena, ponovno izberite **Povezava do CDS-ja za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="71ede-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="71ede-160">Preusmerjeni boste na funkcijo dvojnega zapisovanja v storitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="71ede-160">You will be redirected to Dual Write in Finance.</span></span>

![Povezava do CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="71ede-162">Izberite **Uporabi rešitev**, če želite dostopati do entitet, ki bodo preslikane v integraciji.</span><span class="sxs-lookup"><span data-stu-id="71ede-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Uporaba rešitev](./media/13ApplySolutions.png)

5. <span data-ttu-id="71ede-164">Izberite rešitvi **Preslikava entitete za dvojno pisanje Dynamics 365 Finance and Operations** in **Preslikava entitete za dvojno pisanje Dynamics 365 Project Operations** ter izberite **Uporabi**.</span><span class="sxs-lookup"><span data-stu-id="71ede-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Potrjevanje rešitev](./media/14ConfirmSolutions.png)

<span data-ttu-id="71ede-166">Po uporabi rešitev se entitete za dvojno zapisovanje uporabijo v samem okolju.</span><span class="sxs-lookup"><span data-stu-id="71ede-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Uporaba rešitev](./media/15ApplyingSolutions.png)

<span data-ttu-id="71ede-168">Po uporabi entitet se v okolju prikažejo vse razpoložljive preslikave.</span><span class="sxs-lookup"><span data-stu-id="71ede-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Zemljevidi entitet za dvojno zapisovanje](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="71ede-170">Po posodobitvi osvežite podatkovne vnose</span><span class="sxs-lookup"><span data-stu-id="71ede-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="71ede-171">V storitvi Finance odprite delovni prostor **Upravljanje podatkov**.</span><span class="sxs-lookup"><span data-stu-id="71ede-171">In Finance, go to the **Data management** workspace.</span></span>

![Delovni prostor »Upravljanje podatkov«](./media/16DataManagement.png)

2. <span data-ttu-id="71ede-173">Izberite ploščico **Parametri ogrodja**.</span><span class="sxs-lookup"><span data-stu-id="71ede-173">Select the **Framework parameters** tile.</span></span>

![Parametri ogrodja](./media/17FrameworkParameters.png)

3. <span data-ttu-id="71ede-175">Na strani **Nastavitve entitete** izberite **Osveži seznam entitet**.</span><span class="sxs-lookup"><span data-stu-id="71ede-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Osveži seznam entitet](./media/18RefreshEntityList.png)

<span data-ttu-id="71ede-177">Osveževanje bo trajalo približno 20 minut.</span><span class="sxs-lookup"><span data-stu-id="71ede-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="71ede-178">Ko bo končano, boste prejeli obvestilo.</span><span class="sxs-lookup"><span data-stu-id="71ede-178">You will receive an alert when it is complete.</span></span>

![Potrditev osveževanja](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="71ede-180">Posodobitev varnostnih nastavitev v storitvi Project Operations na Dataverse</span><span class="sxs-lookup"><span data-stu-id="71ede-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="71ede-181">Pojdite na Project Operations v svojem okolju Dataverse.</span><span class="sxs-lookup"><span data-stu-id="71ede-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="71ede-182">Pojdite na **Nastavitve** > **Varnost** > **Varnostne vloge**.</span><span class="sxs-lookup"><span data-stu-id="71ede-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="71ede-183">Na strani **Varnostne vloge** na seznamu vlog izberite **uporabnik aplikacije dvojnega zapisovanja** in izberite zavihek **Entitete po meri**.</span><span class="sxs-lookup"><span data-stu-id="71ede-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="71ede-184">Prepričajte se, da ima vloga dovoljenji **Branje** in **Prilaganje k** za:</span><span class="sxs-lookup"><span data-stu-id="71ede-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="71ede-185">**Vrsta menjalnega tečaja valute**</span><span class="sxs-lookup"><span data-stu-id="71ede-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="71ede-186">**Kontni načrt**</span><span class="sxs-lookup"><span data-stu-id="71ede-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="71ede-187">**Poslovni koledar**</span><span class="sxs-lookup"><span data-stu-id="71ede-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="71ede-188">**Knjiga**</span><span class="sxs-lookup"><span data-stu-id="71ede-188">**Ledger**</span></span>

5. <span data-ttu-id="71ede-189">Ko je varnostna vloga posodobljena, pojdite na **Nastavitve** > **Varnost** > **Ekipe** in izberite privzeto ekipo v pogledu ekipe **Lastnik lokalnega podjetja**.</span><span class="sxs-lookup"><span data-stu-id="71ede-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="71ede-190">Izberite **Upravljanje vlog** in se prepričajte, da je varnostna pravica **uporabnik aplikacije dvojnega zapisovanja** uveljavljena za to ekipo.</span><span class="sxs-lookup"><span data-stu-id="71ede-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="71ede-191">Zagon zemljevidov za dvojno zapisovanje v aplikaciji Project Operations</span><span class="sxs-lookup"><span data-stu-id="71ede-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="71ede-192">V projektu LCS odprite stran **Podrobnosti o okolju**.</span><span class="sxs-lookup"><span data-stu-id="71ede-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="71ede-193">V možnosti **Informacije o okolju Common Data Service** izberite **Povezava do CDS-ja za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="71ede-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="71ede-194">Ko izberete povezavo, boste preusmerjeni na seznam entitet v preslikavah.</span><span class="sxs-lookup"><span data-stu-id="71ede-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="71ede-195">Zaženite zemljevide, kot je opisano v naslednji tabeli.</span><span class="sxs-lookup"><span data-stu-id="71ede-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="71ede-196">Upoštevajte navedeno zaporedje.</span><span class="sxs-lookup"><span data-stu-id="71ede-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="71ede-197">**Preslikava entitete**</span><span class="sxs-lookup"><span data-stu-id="71ede-197">**Entity Map**</span></span> | <span data-ttu-id="71ede-198">**Osveži entiteto**</span><span class="sxs-lookup"><span data-stu-id="71ede-198">**Refresh entity**</span></span> | <span data-ttu-id="71ede-199">**Začetna sinhronizacija**</span><span class="sxs-lookup"><span data-stu-id="71ede-199">**Initial sync**</span></span> | <span data-ttu-id="71ede-200">**Glavni za začetno sinhronizacijo**</span><span class="sxs-lookup"><span data-stu-id="71ede-200">**Master for initial sync**</span></span> | <span data-ttu-id="71ede-201">**Zaženi predhodne zahteve**</span><span class="sxs-lookup"><span data-stu-id="71ede-201">**Run prerequisites**</span></span> | <span data-ttu-id="71ede-202">**Začetna sinhronizacija predhodnih zahtev**</span><span class="sxs-lookup"><span data-stu-id="71ede-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="71ede-203">**Vloge projektnih virov za vsa podjetja (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="71ede-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="71ede-204">No</span><span class="sxs-lookup"><span data-stu-id="71ede-204">No</span></span> | <span data-ttu-id="71ede-205">Da</span><span class="sxs-lookup"><span data-stu-id="71ede-205">Yes</span></span> | <span data-ttu-id="71ede-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="71ede-206">Common Data Service</span></span> | <span data-ttu-id="71ede-207">No</span><span class="sxs-lookup"><span data-stu-id="71ede-207">No</span></span> | <span data-ttu-id="71ede-208">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-208">N\A</span></span> |
| <span data-ttu-id="71ede-209">**Pravne osebe (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="71ede-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="71ede-210">No</span><span class="sxs-lookup"><span data-stu-id="71ede-210">No</span></span> | <span data-ttu-id="71ede-211">Da</span><span class="sxs-lookup"><span data-stu-id="71ede-211">Yes</span></span> | <span data-ttu-id="71ede-212">Aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="71ede-212">Finance and Operations apps</span></span> | <span data-ttu-id="71ede-213">No</span><span class="sxs-lookup"><span data-stu-id="71ede-213">No</span></span> | <span data-ttu-id="71ede-214">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-214">N\A</span></span> |
| <span data-ttu-id="71ede-215">**Knjiga (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="71ede-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="71ede-216">No</span><span class="sxs-lookup"><span data-stu-id="71ede-216">No</span></span> | <span data-ttu-id="71ede-217">Da</span><span class="sxs-lookup"><span data-stu-id="71ede-217">Yes</span></span> | <span data-ttu-id="71ede-218">Aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="71ede-218">Finance and Operations apps</span></span> | <span data-ttu-id="71ede-219">Da</span><span class="sxs-lookup"><span data-stu-id="71ede-219">Yes</span></span> | <span data-ttu-id="71ede-220">Da, aplikacije Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="71ede-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="71ede-221">**Dejanske vrednosti integracije storitve Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="71ede-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="71ede-222">No</span><span class="sxs-lookup"><span data-stu-id="71ede-222">No</span></span> | <span data-ttu-id="71ede-223">No</span><span class="sxs-lookup"><span data-stu-id="71ede-223">No</span></span> | <span data-ttu-id="71ede-224">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-224">N\A</span></span> | <span data-ttu-id="71ede-225">Da</span><span class="sxs-lookup"><span data-stu-id="71ede-225">Yes</span></span> | <span data-ttu-id="71ede-226">No</span><span class="sxs-lookup"><span data-stu-id="71ede-226">No</span></span> |
| <span data-ttu-id="71ede-227">**Podrobnosti pogodbe (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="71ede-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="71ede-228">No</span><span class="sxs-lookup"><span data-stu-id="71ede-228">No</span></span> | <span data-ttu-id="71ede-229">No</span><span class="sxs-lookup"><span data-stu-id="71ede-229">No</span></span> | <span data-ttu-id="71ede-230">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-230">N\A</span></span> | <span data-ttu-id="71ede-231">No</span><span class="sxs-lookup"><span data-stu-id="71ede-231">No</span></span> | <span data-ttu-id="71ede-232">No</span><span class="sxs-lookup"><span data-stu-id="71ede-232">No</span></span> |
| <span data-ttu-id="71ede-233">**Integracijska entiteta za odnose projektne transakcije (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="71ede-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="71ede-234">No</span><span class="sxs-lookup"><span data-stu-id="71ede-234">No</span></span> | <span data-ttu-id="71ede-235">No</span><span class="sxs-lookup"><span data-stu-id="71ede-235">No</span></span> | <span data-ttu-id="71ede-236">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-236">N\A</span></span> | <span data-ttu-id="71ede-237">No</span><span class="sxs-lookup"><span data-stu-id="71ede-237">No</span></span> | <span data-ttu-id="71ede-238">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-238">N\A</span></span> |
| <span data-ttu-id="71ede-239">**Mejniki podrobnosti pogodbe o integraciji storitve Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="71ede-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="71ede-240">No</span><span class="sxs-lookup"><span data-stu-id="71ede-240">No</span></span> | <span data-ttu-id="71ede-241">No</span><span class="sxs-lookup"><span data-stu-id="71ede-241">No</span></span> | <span data-ttu-id="71ede-242">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-242">N\A</span></span> | <span data-ttu-id="71ede-243">No</span><span class="sxs-lookup"><span data-stu-id="71ede-243">No</span></span> | <span data-ttu-id="71ede-244">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-244">N\A</span></span> |
| <span data-ttu-id="71ede-245">**Integracijska entiteta za ocene stroškov v storitvi Project Operations (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="71ede-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="71ede-246">No</span><span class="sxs-lookup"><span data-stu-id="71ede-246">No</span></span> | <span data-ttu-id="71ede-247">No</span><span class="sxs-lookup"><span data-stu-id="71ede-247">No</span></span> | <span data-ttu-id="71ede-248">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-248">N\A</span></span> | <span data-ttu-id="71ede-249">No</span><span class="sxs-lookup"><span data-stu-id="71ede-249">No</span></span> | <span data-ttu-id="71ede-250">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-250">N\A</span></span> |
| <span data-ttu-id="71ede-251">**Entiteta za izvoz kategorije stroškov projekta pri integraciji storitve Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="71ede-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="71ede-252">No</span><span class="sxs-lookup"><span data-stu-id="71ede-252">No</span></span> | <span data-ttu-id="71ede-253">No</span><span class="sxs-lookup"><span data-stu-id="71ede-253">No</span></span> | <span data-ttu-id="71ede-254">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-254">N\A</span></span> | <span data-ttu-id="71ede-255">No</span><span class="sxs-lookup"><span data-stu-id="71ede-255">No</span></span> | <span data-ttu-id="71ede-256">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-256">N\A</span></span> |
| <span data-ttu-id="71ede-257">**Entiteta za izvoz stroškov projekta pri integraciji storitve Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="71ede-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="71ede-258">Da</span><span class="sxs-lookup"><span data-stu-id="71ede-258">Yes</span></span> | <span data-ttu-id="71ede-259">No</span><span class="sxs-lookup"><span data-stu-id="71ede-259">No</span></span> | <span data-ttu-id="71ede-260">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-260">N\A</span></span> | <span data-ttu-id="71ede-261">No</span><span class="sxs-lookup"><span data-stu-id="71ede-261">No</span></span> | <span data-ttu-id="71ede-262">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-262">N\A</span></span> |
| <span data-ttu-id="71ede-263">**Integracijska entiteta za oceno časa v storitvi Project Operations (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="71ede-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="71ede-264">Da</span><span class="sxs-lookup"><span data-stu-id="71ede-264">Yes</span></span> | <span data-ttu-id="71ede-265">No</span><span class="sxs-lookup"><span data-stu-id="71ede-265">No</span></span> | <span data-ttu-id="71ede-266">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-266">N\A</span></span> | <span data-ttu-id="71ede-267">No</span><span class="sxs-lookup"><span data-stu-id="71ede-267">No</span></span> | <span data-ttu-id="71ede-268">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="71ede-268">N\A</span></span> |


4. <span data-ttu-id="71ede-269">Če želite osvežiti entiteto, izberite ime zemljevida in nato **Osveži entitete**.</span><span class="sxs-lookup"><span data-stu-id="71ede-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Osveži zemljevid](./media/20RefreshMapping.png)

5. <span data-ttu-id="71ede-271">Po zaključenem osveževanju izvajajte zemljevid.</span><span class="sxs-lookup"><span data-stu-id="71ede-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="71ede-272">Preden omogočite naslednji zemljevid, preverite, ali je zemljevid v tabeli v stanju **Se izvaja**.</span><span class="sxs-lookup"><span data-stu-id="71ede-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="71ede-273">Izvajanje zemljevidov z večjim številom predhodnih zahtev lahko traja nekaj časa.</span><span class="sxs-lookup"><span data-stu-id="71ede-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="71ede-274">Za izvajanje zemljevida s predhodnimi zahtevami omogočite preklopno stikalo **Prikaz zemljevidov povezanih entitet**.</span><span class="sxs-lookup"><span data-stu-id="71ede-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="71ede-275">Če je v tabeli možnost **Predpogoj za začetno sinhronizacijo** nastavljena na **Ne**, preverite, ali je zastavica **Začetna sinhronizacija** nastavljena na **Izklopljeno** na vseh zahtevanih zemljevidih, preden jih zaženete.</span><span class="sxs-lookup"><span data-stu-id="71ede-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Zagon zemljevida](./media/21RunMap.png)

6. <span data-ttu-id="71ede-277">Preverite, ali se izvajajo vsi s projektom povezani zemljevidi.</span><span class="sxs-lookup"><span data-stu-id="71ede-277">Validate all project related maps are in the running state.</span></span>

![Vsi zemljevidi se izvajajo](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="71ede-279">Uporaba konfiguracijskih podatkov v storitvi CDS za Project Operations (izbirno)</span><span class="sxs-lookup"><span data-stu-id="71ede-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="71ede-280">Če ste predstavitvene podatke uporabili za okolje Finance in jih želite uporabiti v okolju CDS, glejte [Nastavitev in uporaba konfiguracijskih podatkov v storitvi Common Data Service za Project Operations](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="71ede-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="71ede-281">Vaše okolje Project Operations je zdaj omogočeno in konfigurirano.</span><span class="sxs-lookup"><span data-stu-id="71ede-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]