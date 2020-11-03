---
title: Nastavitev in uporaba konfiguracijskih podatkov v storitvi Common Data Service za Project Operations
description: Ta tema vsebuje informacije o nastavitvi in uporabi konfiguracijskih podatkov v storitvi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084629"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="efbd7-103">Nastavitev in uporaba konfiguracijskih podatkov v storitvi Common Data Service za Project Operations</span><span class="sxs-lookup"><span data-stu-id="efbd7-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="efbd7-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="efbd7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="efbd7-105">Namestitev podatkov za nastavitev in konfiguracijo</span><span class="sxs-lookup"><span data-stu-id="efbd7-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="efbd7-106">Prenesite, odblokirajte in razširite datoteko [Paket podatkov za namestitev in konfiguracijo](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="efbd7-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="efbd7-107">Pomaknite se do mape z razširjenimi datotekami in zaženite izvedljivo datoteko *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="efbd7-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="efbd7-108">Na 1. strani čarovnika za selitev konfiguracije Common Data Service (CMT) izberite **Uvozi podatke** in nato izberite **Nadaljuj**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Selitev konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="efbd7-110">Na 2. strani čarovnika CMT izberite **Microsoft 365** kot možnost **Vrsta uvajanja**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="efbd7-111">Izberite potrditvena polja **Prikaži seznam organizacij, ki so na voljo** in **Pokaži napredno**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="efbd7-112">Izberite regijo vašega najemnika, vnesite poverilnice in nato izberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Prijava v konfiguracijo](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="efbd7-114">Na 3. strani s seznama organizacij pri najemniku izberite, v katero organizacijo želite uvoziti predstavitvene podatke, in kliknite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="efbd7-115">Na 4. strani izberite datoteko ZIP *SampleSetupAndConfigData* iz razstavljene mape.</span><span class="sxs-lookup"><span data-stu-id="efbd7-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Izbira datoteke ZIP](./media/3ZipFile.png)

![Izberite datoteko](./media/4SelectAFile.png)

9. <span data-ttu-id="efbd7-118">Ko je izbrana datoteka ZIP, izberite **Uvozi podatke**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-118">After the zip file is selected, select **Import Data**.</span></span>

![Uvozi podatke](./media/5ImportData.png)

10. <span data-ttu-id="efbd7-120">Uvoz bo trajal od približno dveh do deset minut, odvisno od hitrosti vašega omrežja.</span><span class="sxs-lookup"><span data-stu-id="efbd7-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="efbd7-121">Po dokončanem uvozu zapustite čarovnik CMT.</span><span class="sxs-lookup"><span data-stu-id="efbd7-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="efbd7-122">Preverite, ali ima vaša organizacija podatke o naslednjih 19 entitetah:</span><span class="sxs-lookup"><span data-stu-id="efbd7-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="efbd7-123">Valuta</span><span class="sxs-lookup"><span data-stu-id="efbd7-123">Currency</span></span>
  - <span data-ttu-id="efbd7-124">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="efbd7-124">Organizational Unit</span></span>
  - <span data-ttu-id="efbd7-125">Stik</span><span class="sxs-lookup"><span data-stu-id="efbd7-125">Contact</span></span>
  - <span data-ttu-id="efbd7-126">Skupina davka</span><span class="sxs-lookup"><span data-stu-id="efbd7-126">Tax Group</span></span>
  - <span data-ttu-id="efbd7-127">Skupina strank</span><span class="sxs-lookup"><span data-stu-id="efbd7-127">Customer Group</span></span>
  - <span data-ttu-id="efbd7-128">Enota</span><span class="sxs-lookup"><span data-stu-id="efbd7-128">Unit</span></span>
  - <span data-ttu-id="efbd7-129">Skupina enot</span><span class="sxs-lookup"><span data-stu-id="efbd7-129">Unit Group</span></span>
  - <span data-ttu-id="efbd7-130">Cenik</span><span class="sxs-lookup"><span data-stu-id="efbd7-130">Price List</span></span>
  - <span data-ttu-id="efbd7-131">Cenik parametrov projekta</span><span class="sxs-lookup"><span data-stu-id="efbd7-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="efbd7-132">Pogostost izdajanja računov</span><span class="sxs-lookup"><span data-stu-id="efbd7-132">Invoice Frequency</span></span>
  - <span data-ttu-id="efbd7-133">Kategorija vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="efbd7-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="efbd7-134">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="efbd7-134">Transaction Category</span></span>
  - <span data-ttu-id="efbd7-135">Kategorija stroška</span><span class="sxs-lookup"><span data-stu-id="efbd7-135">Expense Category</span></span>
  - <span data-ttu-id="efbd7-136">Cena vloge</span><span class="sxs-lookup"><span data-stu-id="efbd7-136">Role Price</span></span>
  - <span data-ttu-id="efbd7-137">Cena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="efbd7-137">Transaction Category Price</span></span>
  - <span data-ttu-id="efbd7-138">Značilnost</span><span class="sxs-lookup"><span data-stu-id="efbd7-138">Characteristic</span></span>
  - <span data-ttu-id="efbd7-139">Vir, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="efbd7-139">Bookable Resource</span></span>
  - <span data-ttu-id="efbd7-140">Povezava kategorije vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="efbd7-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="efbd7-141">Lastnost vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="efbd7-141">Bookable Resource Characteristic</span></span>

![Zaključek uvoza](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="efbd7-143">Posodobitev konfiguracij storitve Project Operations</span><span class="sxs-lookup"><span data-stu-id="efbd7-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="efbd7-144">Pomaknite se v okolje CE.</span><span class="sxs-lookup"><span data-stu-id="efbd7-144">Navigate to the CE environment.</span></span> <span data-ttu-id="efbd7-145">Najdete ga tako, da odprete [skrbniško središče Power Platform](https://admin.powerplatform.microsoft.com/environments), izberete okolje in kliknete **Odpri okolje**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Odpri okolje](./media/7OpenEnvironment.png)

2. <span data-ttu-id="efbd7-147">Odprite **Projekti** > **Viri** in nato izberite **Novo** , da za svojega uporabnika ustvarite vir, ki ga je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="efbd7-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Viri, ki jih je mogoče rezervirati](./media/8BookableResources.png)

3. <span data-ttu-id="efbd7-149">Na zavihku **Splošno** izberite skrbniškega uporabnika.</span><span class="sxs-lookup"><span data-stu-id="efbd7-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="efbd7-150">Preverite, ali se časovni pas ujema s tistim, v katerem ste.</span><span class="sxs-lookup"><span data-stu-id="efbd7-150">Verify that the time zone matches the one you are in.</span></span> 

![Novi vir, ki ga je mogoče rezervirati](./media/9NewBookableResource.png)

4. <span data-ttu-id="efbd7-152">Na zavihku **Načrtovanje** v polju **Podjetje** izberite podjetje **USPM** in nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Zavihek »Načrtovanje«](./media/10SchedulingTab.png)

5. <span data-ttu-id="efbd7-154">Izberite zavihek **Delovni čas**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-154">Select the **Work hours** tab.</span></span>  

![Delovni čas](./media/11WorkHours.png)

6. <span data-ttu-id="efbd7-156">Dvokliknite katero koli vrednost v koledarju in izberite **Uredi** > **Vsi dogodki v seriji**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Delovni koledar](./media/12WorkCalendar.png)

7. <span data-ttu-id="efbd7-158">Spremenite delovni čas v osemurni (8) delovnik, vikende označite kot dela proste dni in se prepričajte, da se časovni pas ujema z vašim.</span><span class="sxs-lookup"><span data-stu-id="efbd7-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="efbd7-159">Izberite **Shrani in zapri**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-159">Select **Save and close**.</span></span>

![Posodobitev koledarja](./media/13UpdateCalendar.png)

9. <span data-ttu-id="efbd7-161">Odprite **Nastavitve** > **Predloge koledarja** in izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Predloge koledarja](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="efbd7-163">Vnesite ime, izberite vir predloge, ki ste ga ustvarili, in nato **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Shranite predlogo koledarja](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="efbd7-165">Odprite možnost **Parametri** in dvokliknite zapis.</span><span class="sxs-lookup"><span data-stu-id="efbd7-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projektni parametri](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="efbd7-167">Posodobite naslednja polja:</span><span class="sxs-lookup"><span data-stu-id="efbd7-167">Update the following fields:</span></span>

 - <span data-ttu-id="efbd7-168">**Privzeto podjetje** : USPM</span><span class="sxs-lookup"><span data-stu-id="efbd7-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="efbd7-169">**Privzeta organizacijska enota** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="efbd7-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="efbd7-170">**Pogostost izdajanja računov** : sedmi in zadnji dan</span><span class="sxs-lookup"><span data-stu-id="efbd7-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="efbd7-171">**Predloga delovnega časa** : preklopite na predlogo, ki ste jo ustvarili.</span><span class="sxs-lookup"><span data-stu-id="efbd7-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="efbd7-172">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="efbd7-172">Select **Save**.</span></span> 

![Posodobljeni projektni parametri](./media/17UpdatedProjectParameters.png)
