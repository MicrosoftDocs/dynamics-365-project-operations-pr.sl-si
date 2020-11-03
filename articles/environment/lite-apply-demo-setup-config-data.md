---
title: Uporaba predstavitvenih podatkov za nastavitev in konfiguracijo
description: Ta tema vsebuje informacije o uporabi predstavitvenih podatkov za nastavitev in konfiguracijo za storitev Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084621"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="39132-103">Uporaba predstavitvenih podatkov za nastavitev in konfiguracijo za poenostavljeno uvedbo storitve Project Operations – od posla do izstavitve predračuna</span><span class="sxs-lookup"><span data-stu-id="39132-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="39132-104">_\*\*Poenostavljena uvedba – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="39132-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="39132-105">Prenesite [paket glavnih podatkov](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="39132-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="39132-106">Pomaknite se do mape *ProjOpsDemoDataSetupAndMaster – integrirani CMT* in zaženite izvedljivo datoteko *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="39132-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="39132-107">Na 1. strani čarovnika za selitev konfiguracije Common Data Service (CMT) izberite **Uvozi podatke** in nato izberite **Nadaljuj**.</span><span class="sxs-lookup"><span data-stu-id="39132-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Selitev konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="39132-109">Na 2. strani čarovnika CMT izberite **Microsoft 365** kot možnost **Vrsta uvajanja**.</span><span class="sxs-lookup"><span data-stu-id="39132-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="39132-110">Izberite potrditvena polja **Prikaži seznam organizacij, ki so na voljo** in **Pokaži napredno**.</span><span class="sxs-lookup"><span data-stu-id="39132-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="39132-111">Izberite regijo vašega najemnika, vnesite poverilnice in nato izberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="39132-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Prijava v konfiguracijo](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="39132-113">Na 3. strani s seznama organizacij pri najemniku izberite, v katero organizacijo želite uvoziti predstavitvene podatke, in nato izberite **Prijava**.</span><span class="sxs-lookup"><span data-stu-id="39132-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="39132-114">Na 4. strani izberite datoteko ZIP, *MasterAndSetupData* iz razstavljene mape, *ProjOpsDemoDataSetupAndMaster – integrirani CMT*.</span><span class="sxs-lookup"><span data-stu-id="39132-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Datoteka ZIP](./media/3ZipFile.png)

![Izberite datoteko](./media/4SelectAFile.png)

9. <span data-ttu-id="39132-117">Ko je izbrana datoteka ZIP, izberite **Uvozi podatke**.</span><span class="sxs-lookup"><span data-stu-id="39132-117">After the zip file is selected, select **Import Data**.</span></span>

![Uvozi podatke](./media/5ImportData.png)

10. <span data-ttu-id="39132-119">Uvoz bo trajal od približno dveh do deset minut, odvisno od hitrosti vašega omrežja.</span><span class="sxs-lookup"><span data-stu-id="39132-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="39132-120">Ko se konča, zapustite čarovnik CMT.</span><span class="sxs-lookup"><span data-stu-id="39132-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="39132-121">Preverite, ali ima vaša organizacija podatke o naslednjih 20 entitetah:</span><span class="sxs-lookup"><span data-stu-id="39132-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="39132-122">Valuta</span><span class="sxs-lookup"><span data-stu-id="39132-122">Currency</span></span>
- <span data-ttu-id="39132-123">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="39132-123">Organizational Unit</span></span>
- <span data-ttu-id="39132-124">Stik</span><span class="sxs-lookup"><span data-stu-id="39132-124">Contact</span></span>
- <span data-ttu-id="39132-125">Skupina davka</span><span class="sxs-lookup"><span data-stu-id="39132-125">Tax Group</span></span>
- <span data-ttu-id="39132-126">Skupina strank</span><span class="sxs-lookup"><span data-stu-id="39132-126">Customer Group</span></span>
- <span data-ttu-id="39132-127">Enota</span><span class="sxs-lookup"><span data-stu-id="39132-127">Unit</span></span>
- <span data-ttu-id="39132-128">Skupina enot</span><span class="sxs-lookup"><span data-stu-id="39132-128">Unit Group</span></span>
- <span data-ttu-id="39132-129">Cenik</span><span class="sxs-lookup"><span data-stu-id="39132-129">Price List</span></span>
- <span data-ttu-id="39132-130">Cenik parametrov projekta</span><span class="sxs-lookup"><span data-stu-id="39132-130">Project Parameter Price List</span></span>
- <span data-ttu-id="39132-131">Pogostost izdajanja računov</span><span class="sxs-lookup"><span data-stu-id="39132-131">Invoice Frequency</span></span>
- <span data-ttu-id="39132-132">Podrobnost o pogostosti izdajanja računov</span><span class="sxs-lookup"><span data-stu-id="39132-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="39132-133">Kategorija vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="39132-133">Bookable Resource Category</span></span>
- <span data-ttu-id="39132-134">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="39132-134">Transaction Category</span></span>
- <span data-ttu-id="39132-135">Kategorija stroška</span><span class="sxs-lookup"><span data-stu-id="39132-135">Expense Category</span></span>
- <span data-ttu-id="39132-136">Cena vloge</span><span class="sxs-lookup"><span data-stu-id="39132-136">Role Price</span></span>
- <span data-ttu-id="39132-137">Cena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="39132-137">Transaction Category Price</span></span>
- <span data-ttu-id="39132-138">Značilnost</span><span class="sxs-lookup"><span data-stu-id="39132-138">Characteristic</span></span>
- <span data-ttu-id="39132-139">Vir, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="39132-139">Bookable Resource</span></span>
- <span data-ttu-id="39132-140">Povezava kategorije vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="39132-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="39132-141">Lastnost vira, ki ga je mogoče rezervirati</span><span class="sxs-lookup"><span data-stu-id="39132-141">Bookable Resource Characteristic</span></span>

![Zaključek uvoza](./media/6CompleteImport.png)
