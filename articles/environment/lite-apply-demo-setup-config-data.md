---
title: Uporaba nastavitve predstavitvenega načina in konfiguracijskih podatkov – poenostavljena različica
description: Ta tema vsebuje informacije o uporabi predstavitvenih podatkov za nastavitev in konfiguracijo za storitev Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 421c9d28088c92617687641d93b3ad5d6bfea73c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642113"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="9de07-103">Uporaba nastavitve predstavitvenega načina in konfiguracijskih podatkov za Project Operations – poenostavljena različica</span><span class="sxs-lookup"><span data-stu-id="9de07-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="9de07-104">_\*\*Poenostavljena uvedba – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="9de07-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="9de07-105">Zahteve</span><span class="sxs-lookup"><span data-stu-id="9de07-105">Prerequisites</span></span>

<span data-ttu-id="9de07-106">Preden začnete s konfiguracijo morate imeti omogočeno okolje Common Data Service (CDS) za Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9de07-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="9de07-107">Navodila</span><span class="sxs-lookup"><span data-stu-id="9de07-107">Instructions</span></span>

1. <span data-ttu-id="9de07-108">Prenesite [paket glavnih podatkov](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="9de07-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="9de07-109">Pomaknite se do mape *ProjOpsDemoDataSetupAndMaster – integrirani CMT* in zaženite izvedljivo datoteko *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="9de07-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="9de07-110">Na 1. strani čarovnika za selitev konfiguracije Common Data Service (CMT) izberite **Uvozi podatke** in nato izberite **Nadaljuj**.</span><span class="sxs-lookup"><span data-stu-id="9de07-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Selitev konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="9de07-112">Na 2. strani čarovnika CMT izberite **Microsoft 365** kot možnost **Vrsta uvajanja**.</span><span class="sxs-lookup"><span data-stu-id="9de07-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="9de07-113">Izberite potrditvena polja **Prikaži seznam organizacij, ki so na voljo** in **Pokaži napredno**.</span><span class="sxs-lookup"><span data-stu-id="9de07-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="9de07-114">Izberite regijo vašega najemnika, vnesite poverilnice in nato izberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="9de07-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Prijava v konfiguracijo](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="9de07-116">Na 3. strani s seznama organizacij pri najemniku izberite, v katero organizacijo želite uvoziti predstavitvene podatke, in nato izberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="9de07-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="9de07-117">Na 4. strani izberite datoteko ZIP, *MasterAndSetupData* iz razstavljene mape, *ProjOpsDemoDataSetupAndMaster – integrirani CMT*.</span><span class="sxs-lookup"><span data-stu-id="9de07-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Datoteka ZIP](./media/3ZipFile.png)

![Izberite datoteko](./media/4SelectAFile.png)

9. <span data-ttu-id="9de07-120">Ko je izbrana datoteka ZIP, izberite **Uvozi podatke**.</span><span class="sxs-lookup"><span data-stu-id="9de07-120">After the zip file is selected, select **Import Data**.</span></span>

![Uvozi podatke](./media/5ImportData.png)

10. <span data-ttu-id="9de07-122">Uvoz bo trajal od približno dveh do deset minut, odvisno od hitrosti vašega omrežja.</span><span class="sxs-lookup"><span data-stu-id="9de07-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="9de07-123">Ko se konča, zapustite čarovnik CMT.</span><span class="sxs-lookup"><span data-stu-id="9de07-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="9de07-124">Preverite, ali ima vaša organizacija podatke o naslednjih 20 entitetah:</span><span class="sxs-lookup"><span data-stu-id="9de07-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="9de07-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="9de07-125">Currency</span></span>
-   <span data-ttu-id="9de07-126">Račun</span><span class="sxs-lookup"><span data-stu-id="9de07-126">Account</span></span>
-   <span data-ttu-id="9de07-127">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="9de07-127">Organizational Unit</span></span>
-   <span data-ttu-id="9de07-128">Stik</span><span class="sxs-lookup"><span data-stu-id="9de07-128">Contact</span></span>
-   <span data-ttu-id="9de07-129">Skupina davka</span><span class="sxs-lookup"><span data-stu-id="9de07-129">Tax Group</span></span>
-   <span data-ttu-id="9de07-130">Skupina strank</span><span class="sxs-lookup"><span data-stu-id="9de07-130">Customer Group</span></span>
-   <span data-ttu-id="9de07-131">Enota</span><span class="sxs-lookup"><span data-stu-id="9de07-131">Unit</span></span>
-   <span data-ttu-id="9de07-132">Skupina enot</span><span class="sxs-lookup"><span data-stu-id="9de07-132">Unit Group</span></span>
-   <span data-ttu-id="9de07-133">Cenik</span><span class="sxs-lookup"><span data-stu-id="9de07-133">Price List</span></span>
-   <span data-ttu-id="9de07-134">Cenik parametrov projekta</span><span class="sxs-lookup"><span data-stu-id="9de07-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="9de07-135">Pogostost izdajanja računov</span><span class="sxs-lookup"><span data-stu-id="9de07-135">Invoice Frequency</span></span>
-   <span data-ttu-id="9de07-136">Kategorija vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="9de07-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="9de07-137">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="9de07-137">Transaction Category</span></span>
-   <span data-ttu-id="9de07-138">Kategorija stroška</span><span class="sxs-lookup"><span data-stu-id="9de07-138">Expense Category</span></span>
-   <span data-ttu-id="9de07-139">Cena vloge</span><span class="sxs-lookup"><span data-stu-id="9de07-139">Role Price</span></span>
-   <span data-ttu-id="9de07-140">Cena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="9de07-140">Transaction Category Price</span></span>
-   <span data-ttu-id="9de07-141">Značilnost</span><span class="sxs-lookup"><span data-stu-id="9de07-141">Characteristic</span></span>
-   <span data-ttu-id="9de07-142">Vir, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="9de07-142">Bookable Resource</span></span>
-   <span data-ttu-id="9de07-143">Povezava kategorije vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="9de07-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="9de07-144">Lastnost vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="9de07-144">Bookable Resource Characteristic</span></span>

![Zaključek uvoza](./media/6CompleteImport.png)
