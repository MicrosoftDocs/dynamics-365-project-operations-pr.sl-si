---
title: Nastavitev in uporabo konfiguracijskih podatkov v storitvi Common Data Service
description: Ta tema vsebuje informacije o nastavitvi in uporabi konfiguracijskih podatkov v storitvi Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642248"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="11374-103">Nastavitev in uporabo konfiguracijskih podatkov v storitvi Common Data Service</span><span class="sxs-lookup"><span data-stu-id="11374-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="11374-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="11374-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="11374-105">Zahteve</span><span class="sxs-lookup"><span data-stu-id="11374-105">Prerequisites</span></span>

<span data-ttu-id="11374-106">Preden začnete konfigurirati podatke v storitvi Common Data Service (CDS), morajo biti izpolnjeni naslednji predpogoji:</span><span class="sxs-lookup"><span data-stu-id="11374-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="11374-107">Omogočanje okolja CDS v okolju storitve Dynamics 365 Finance za Project Operations.</span><span class="sxs-lookup"><span data-stu-id="11374-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="11374-108">Podatki o pravni osebi iz storitve Dynamics 365 Finance so v skupni rabi z okoljem CDS.</span><span class="sxs-lookup"><span data-stu-id="11374-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="11374-109">To pomeni, da ima entiteta **Podjetje** v CDS-ju naslednje zapise podjetja:</span><span class="sxs-lookup"><span data-stu-id="11374-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="11374-110">THPM</span><span class="sxs-lookup"><span data-stu-id="11374-110">THPM</span></span>
  - <span data-ttu-id="11374-111">USPM</span><span class="sxs-lookup"><span data-stu-id="11374-111">USPM</span></span>
  - <span data-ttu-id="11374-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="11374-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="11374-113">Namestitev podatkov za nastavitev in konfiguracijo</span><span class="sxs-lookup"><span data-stu-id="11374-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="11374-114">Prenesite, odblokirajte in razširite datoteko [Paket podatkov za namestitev in konfiguracijo](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="11374-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="11374-115">Pomaknite se do mape z razširjenimi datotekami in zaženite izvedljivo datoteko *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="11374-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="11374-116">Na 1. strani čarovnika za selitev konfiguracije Common Data Service (CMT) izberite **Uvozi podatke** in nato izberite **Nadaljuj**.</span><span class="sxs-lookup"><span data-stu-id="11374-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Selitev konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="11374-118">Na 2. strani čarovnika CMT izberite **Microsoft 365** kot možnost **Vrsta uvajanja**.</span><span class="sxs-lookup"><span data-stu-id="11374-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="11374-119">Izberite potrditvena polja **Prikaži seznam organizacij, ki so na voljo** in **Pokaži napredno**.</span><span class="sxs-lookup"><span data-stu-id="11374-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="11374-120">Izberite regijo vašega najemnika, vnesite poverilnice in nato izberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="11374-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Prijava v konfiguracijo](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="11374-122">Na 3. strani s seznama organizacij pri najemniku izberite, v katero organizacijo želite uvoziti predstavitvene podatke, in kliknite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="11374-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="11374-123">Na 4. strani izberite datoteko ZIP *SampleSetupAndConfigData* iz razstavljene mape.</span><span class="sxs-lookup"><span data-stu-id="11374-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Izbira datoteke ZIP](./media/3ZipFile.png)

![Izberite datoteko](./media/4SelectAFile.png)

9. <span data-ttu-id="11374-126">Ko je izbrana datoteka ZIP, izberite **Uvozi podatke**.</span><span class="sxs-lookup"><span data-stu-id="11374-126">After the zip file is selected, select **Import Data**.</span></span>

![Uvozi podatke](./media/5ImportData.png)

10. <span data-ttu-id="11374-128">Uvoz bo trajal od približno dveh do deset minut, odvisno od hitrosti vašega omrežja.</span><span class="sxs-lookup"><span data-stu-id="11374-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="11374-129">Po dokončanem uvozu zapustite čarovnik CMT.</span><span class="sxs-lookup"><span data-stu-id="11374-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="11374-130">Preverite, ali ima vaša organizacija podatke o naslednjih 19 entitetah:</span><span class="sxs-lookup"><span data-stu-id="11374-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="11374-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="11374-131">Currency</span></span>
  - <span data-ttu-id="11374-132">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="11374-132">Organizational Unit</span></span>
  - <span data-ttu-id="11374-133">Stik</span><span class="sxs-lookup"><span data-stu-id="11374-133">Contact</span></span>
  - <span data-ttu-id="11374-134">Skupina davka</span><span class="sxs-lookup"><span data-stu-id="11374-134">Tax Group</span></span>
  - <span data-ttu-id="11374-135">Skupina strank</span><span class="sxs-lookup"><span data-stu-id="11374-135">Customer Group</span></span>
  - <span data-ttu-id="11374-136">Enota</span><span class="sxs-lookup"><span data-stu-id="11374-136">Unit</span></span>
  - <span data-ttu-id="11374-137">Skupina enot</span><span class="sxs-lookup"><span data-stu-id="11374-137">Unit Group</span></span>
  - <span data-ttu-id="11374-138">Cenik</span><span class="sxs-lookup"><span data-stu-id="11374-138">Price List</span></span>
  - <span data-ttu-id="11374-139">Cenik parametrov projekta</span><span class="sxs-lookup"><span data-stu-id="11374-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="11374-140">Pogostost izdajanja računov</span><span class="sxs-lookup"><span data-stu-id="11374-140">Invoice Frequency</span></span>
  - <span data-ttu-id="11374-141">Kategorija vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="11374-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="11374-142">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="11374-142">Transaction Category</span></span>
  - <span data-ttu-id="11374-143">Kategorija stroška</span><span class="sxs-lookup"><span data-stu-id="11374-143">Expense Category</span></span>
  - <span data-ttu-id="11374-144">Cena vloge</span><span class="sxs-lookup"><span data-stu-id="11374-144">Role Price</span></span>
  - <span data-ttu-id="11374-145">Cena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="11374-145">Transaction Category Price</span></span>
  - <span data-ttu-id="11374-146">Značilnost</span><span class="sxs-lookup"><span data-stu-id="11374-146">Characteristic</span></span>
  - <span data-ttu-id="11374-147">Vir, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="11374-147">Bookable Resource</span></span>
  - <span data-ttu-id="11374-148">Povezava kategorije vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="11374-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="11374-149">Lastnost vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="11374-149">Bookable Resource Characteristic</span></span>

![Zaključek uvoza](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="11374-151">Posodobitev konfiguracij storitve Project Operations</span><span class="sxs-lookup"><span data-stu-id="11374-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="11374-152">Pomaknite se v okolje CE.</span><span class="sxs-lookup"><span data-stu-id="11374-152">Navigate to the CE environment.</span></span> <span data-ttu-id="11374-153">Najdete ga tako, da odprete [skrbniško središče Power Platform](https://admin.powerplatform.microsoft.com/environments), izberete okolje in kliknete **Odpri okolje**.</span><span class="sxs-lookup"><span data-stu-id="11374-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Odpri okolje](./media/7OpenEnvironment.png)

2. <span data-ttu-id="11374-155">Odprite **Projekti** > **Viri** in nato izberite **Novo**, da za svojega uporabnika ustvarite vir, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="11374-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Viri, ki jih je mogoče rezervirati](./media/8BookableResources.png)

3. <span data-ttu-id="11374-157">Na zavihku **Splošno** izberite skrbniškega uporabnika.</span><span class="sxs-lookup"><span data-stu-id="11374-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="11374-158">Preverite, ali se časovni pas ujema s tistim, v katerem ste.</span><span class="sxs-lookup"><span data-stu-id="11374-158">Verify that the time zone matches the one you are in.</span></span> 

![Novi vir, ki ga je mogoče rezervirati](./media/9NewBookableResource.png)

4. <span data-ttu-id="11374-160">Na zavihku **Načrtovanje** v polju **Podjetje** izberite podjetje **USPM** in nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="11374-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Zavihek »Načrtovanje«](./media/10SchedulingTab.png)

5. <span data-ttu-id="11374-162">Izberite zavihek **Delovni čas**.</span><span class="sxs-lookup"><span data-stu-id="11374-162">Select the **Work hours** tab.</span></span>  

![Delovni čas](./media/11WorkHours.png)

6. <span data-ttu-id="11374-164">Dvokliknite katero koli vrednost v koledarju in izberite **Uredi** > **Vsi dogodki v seriji**.</span><span class="sxs-lookup"><span data-stu-id="11374-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Delovni koledar](./media/12WorkCalendar.png)

7. <span data-ttu-id="11374-166">Spremenite delovni čas v osemurni (8) delovnik, vikende označite kot dela proste dni in se prepričajte, da se časovni pas ujema z vašim.</span><span class="sxs-lookup"><span data-stu-id="11374-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="11374-167">Izberite **Shrani in zapri**.</span><span class="sxs-lookup"><span data-stu-id="11374-167">Select **Save and close**.</span></span>

![Posodobitev koledarja](./media/13UpdateCalendar.png)

9. <span data-ttu-id="11374-169">Odprite **Nastavitve** > **Predloge koledarja** in izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="11374-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Predloge koledarja](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="11374-171">Vnesite ime, izberite vir predloge, ki ste ga ustvarili, in nato **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="11374-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Shranite predlogo koledarja](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="11374-173">Odprite možnost **Parametri** in dvokliknite zapis.</span><span class="sxs-lookup"><span data-stu-id="11374-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektni parametri](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="11374-175">Posodobite naslednja polja:</span><span class="sxs-lookup"><span data-stu-id="11374-175">Update the following fields:</span></span>

 - <span data-ttu-id="11374-176">**Privzeto podjetje**: USPM</span><span class="sxs-lookup"><span data-stu-id="11374-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="11374-177">**Privzeta organizacijska enota**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="11374-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="11374-178">**Pogostost izdajanja računov**: sedmi in zadnji dan</span><span class="sxs-lookup"><span data-stu-id="11374-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="11374-179">**Predloga delovnega časa**: preklopite na predlogo, ki ste jo ustvarili.</span><span class="sxs-lookup"><span data-stu-id="11374-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="11374-180">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="11374-180">Select **Save**.</span></span> 

![Posodobljeni projektni parametri](./media/17UpdatedProjectParameters.png)
