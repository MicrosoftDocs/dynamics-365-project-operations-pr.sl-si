---
title: Uporaba predstavitvenih podatkov v okolju, gostovanem v oblaku Finance
description: Ta tema vsebuje razlago, kako uporabiti predstavitvene podatke iz storitve Project Operations v okolju Dynamics 365 Finance v oblaku.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365258"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="b75ae-103">Uporaba predstavitvenih podatkov v okolju, gostovanem v oblaku Finance</span><span class="sxs-lookup"><span data-stu-id="b75ae-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="b75ae-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="b75ae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b75ae-105">Ta tema se nanaša samo na Microsoft Dynamics 365 Finance različice 10.0.13 in jo je mogoče izvajati samo v okolju, ki je gostovano v oblaku.</span><span class="sxs-lookup"><span data-stu-id="b75ae-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="b75ae-106">Dokončajte korake v tej temi, **PREDEN** izvedete posodobitev kakovosti v okolju.</span><span class="sxs-lookup"><span data-stu-id="b75ae-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="b75ae-107">V projektu LCS odprite stran **Podrobnosti o okolju**.</span><span class="sxs-lookup"><span data-stu-id="b75ae-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="b75ae-108">Upoštevajte, da vključuje podrobnosti, ki so potrebne za povezavo z okoljem prek protokola RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="b75ae-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Podrobnosti o okoljih v storitvi ](./media/1EnvironmentDetails.png)

<span data-ttu-id="b75ae-110">Prvi nabor označenih poverilnic so poverilnice lokalnih računov, ki vsebujejo hiperpovezavo do povezave z oddaljenim namizjem.</span><span class="sxs-lookup"><span data-stu-id="b75ae-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="b75ae-111">Poverilnice vključujejo uporabniško ime in geslo skrbnika okolja.</span><span class="sxs-lookup"><span data-stu-id="b75ae-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="b75ae-112">Drugi nabor poverilnic se uporablja za prijavo v strežnik SQL Server v tem okolju.</span><span class="sxs-lookup"><span data-stu-id="b75ae-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="b75ae-113">Povežite se z oddaljenim okoljem prek hiperpovezave v možnosti **Lokalni računi** in uporabite **Poverilnice lokalnega računa** za preverjanje pristnosti.</span><span class="sxs-lookup"><span data-stu-id="b75ae-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="b75ae-114">Odprite **Internet Information Services** > **Skupine programov** > **AOSService** in zaustavite storitev.</span><span class="sxs-lookup"><span data-stu-id="b75ae-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="b75ae-115">S tem boste zaustavili storitev, da boste lahko nadaljevali z menjavo zbirke podatkov SQL.</span><span class="sxs-lookup"><span data-stu-id="b75ae-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Zaustavitev AOS](./media/2StopAOS.png)

4. <span data-ttu-id="b75ae-117">Odprite možnost **Storitve** in zaustavite naslednja dva elementa:</span><span class="sxs-lookup"><span data-stu-id="b75ae-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="b75ae-118">Microsoft Dynamics 365 Unified Operations: storitev za paketno upravljanje</span><span class="sxs-lookup"><span data-stu-id="b75ae-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="b75ae-119">Microsoft Dynamics 365 Unified Operations: ogrodje za uvoz in izvoz podatkov</span><span class="sxs-lookup"><span data-stu-id="b75ae-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Zaustavitev storitev](./media/3StopServices.png)

5. <span data-ttu-id="b75ae-121">Odprite Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="b75ae-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="b75ae-122">Prijavite se s poverilnicami strežnika SQL in uporabite uporabniško ime in geslo za axdbadmin na strani **Podrobnosti o okoljih LCS**.</span><span class="sxs-lookup"><span data-stu-id="b75ae-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="b75ae-124">V raziskovalcu predmetov odprite **Zbirke podatkov** in poiščite **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="b75ae-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="b75ae-125">Zbirko podatkov boste zamenjali z novo, ki se nahaja v [Središču za prenose](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="b75ae-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="b75ae-126">Kopirajte datoteko ZIP v VM, v katerega ste prijavljeni na daljavo, in razširite vsebino datoteke ZIP.</span><span class="sxs-lookup"><span data-stu-id="b75ae-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="b75ae-127">V programu SQL Server Management Studio z desno tipko miške kliknite **AxDB** in nato izberite **Opravila** > **Obnovitev** > **Zbirka podatkov**.</span><span class="sxs-lookup"><span data-stu-id="b75ae-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Obnovitev zbirke podatkov](./media/5RestoreDatabase.png)

9. <span data-ttu-id="b75ae-129">Izberite **Izvorna naprava** in se pomaknite do datoteke, ki ste jo razširili iz kopirane datoteke ZIP.</span><span class="sxs-lookup"><span data-stu-id="b75ae-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Izvorne naprave](./media/6SourceDevice.png)

10. <span data-ttu-id="b75ae-131">Izberite **Možnosti** in nato **Prepiši obstoječo zbirko podatkov** in **Zapri obstoječe povezave do ciljne zbirke podatkov**.</span><span class="sxs-lookup"><span data-stu-id="b75ae-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="b75ae-132">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="b75ae-132">Select **OK**.</span></span>

![Obnovitev nastavitev](./media/7RestoreSetting.png)

<span data-ttu-id="b75ae-134">Prejeli boste potrditev, da je bila obnovitev AXDB uspešna.</span><span class="sxs-lookup"><span data-stu-id="b75ae-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="b75ae-135">Ko prejmete to potrditev, lahko zaprete SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="b75ae-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="b75ae-136">Vrnite se do **Internet Information Services** > **Skupine programov** > **AOSService** in zaženite storitev AOSService.</span><span class="sxs-lookup"><span data-stu-id="b75ae-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="b75ae-137">Odprite **Storitve** in zaženite obe storitvi, ki ste ju predhodno zaustavili.</span><span class="sxs-lookup"><span data-stu-id="b75ae-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="b75ae-138">Poiščite orodje AdminUserProvisioning na tej VM.</span><span class="sxs-lookup"><span data-stu-id="b75ae-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="b75ae-139">Poglejte v K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="b75ae-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="b75ae-140">Zaženite datoteko .ext, tako da vpišete svoj uporabniški naslov v polje **E-poštni naslov**.</span><span class="sxs-lookup"><span data-stu-id="b75ae-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="b75ae-141">Izberite **Pošlji**.</span><span class="sxs-lookup"><span data-stu-id="b75ae-141">Select **Submit**.</span></span>

![Omogočanje uporabe skrbnikom](./media/8AdminUserProvisioning.png)

<span data-ttu-id="b75ae-143">To traja nekaj minut.</span><span class="sxs-lookup"><span data-stu-id="b75ae-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="b75ae-144">Prejeti bi morali potrditveno sporočilo, da je bil skrbnik uspešno posodobljen.</span><span class="sxs-lookup"><span data-stu-id="b75ae-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="b75ae-145">Na koncu zaženite ukazni poziv kot skrbnik in izvedite ukaz iisreset</span><span class="sxs-lookup"><span data-stu-id="b75ae-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Ponastavitev IIS](./media/9IISReset.png)

18. <span data-ttu-id="b75ae-147">Zaprite sejo oddaljenega namizja in uporabite stran **Podrobnosti o okolju** LCS, da se prijavite v okolje in potrdite, da deluje po pričakovanjih.</span><span class="sxs-lookup"><span data-stu-id="b75ae-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
