---
title: Poizvedba glede načrta porabe zveznih subvencij
description: Ta tema vsebuje informacije o poizvedbi glede načrta porabe zveznih subvencij.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 70dff12c106723dda801668412cfd084c462db4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288984"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="c4043-103">Poizvedba glede načrta porabe zveznih subvencij</span><span class="sxs-lookup"><span data-stu-id="c4043-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4043-104">V skladu z okrožnico Urada za upravljanje proračuna A-133 (OMB) za agencije, ki prejemajo zvezna sredstva, veljajo revizijske zahteve, ki so znane tudi kot enotne revizije.</span><span class="sxs-lookup"><span data-stu-id="c4043-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="c4043-105">Revizijski postopek se uporablja za redno poročanje o prihodkih in odhodkih glede zveznih subvencij.</span><span class="sxs-lookup"><span data-stu-id="c4043-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="c4043-106">Del poročila o enotni reviziji vključuje načrt porabe zveznih subvencij (SEFA).</span><span class="sxs-lookup"><span data-stu-id="c4043-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="c4043-107">Poizvedba glede načrta porabe subvencij zveznih držav vključuje naziv in številko kataloga za zvezno pomoč domačim entitetam (CFDA), številko subvencije, leto dodelitve, ime zvezne agencije, ki zagotavlja sredstva, in ime prehodne entitete.</span><span class="sxs-lookup"><span data-stu-id="c4043-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="c4043-108">Povpraševanje je za določeno obdobje.</span><span class="sxs-lookup"><span data-stu-id="c4043-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="c4043-109">To obdobje je običajno enako obdobju računovodskega izkaza, ki je proračunsko leto.</span><span class="sxs-lookup"><span data-stu-id="c4043-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="c4043-110">Poizvedba vključuje subvencije, ki imajo datume projekcije v izbranem časovnem obdobju.</span><span class="sxs-lookup"><span data-stu-id="c4043-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="c4043-111">Stolpec poizvedbe **Agencija, ki podeljuje subvencijo** prikazuje prejemnika subvencije oz. v primeru prehodne entitete za podelitev agencijo, ki podeljuje subvencijo.</span><span class="sxs-lookup"><span data-stu-id="c4043-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="c4043-112">V primeru prisotnosti prehodne entitete stolpec **Prehodna agencija** prikazuje prejemnika subvencije.</span><span class="sxs-lookup"><span data-stu-id="c4043-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="c4043-113">V primeru odsotnosti prehodne entitete je stolpec **Prehodna agencija** prazen.</span><span class="sxs-lookup"><span data-stu-id="c4043-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="c4043-114">Nastavitev gruč CFDA</span><span class="sxs-lookup"><span data-stu-id="c4043-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="c4043-115">Nastaviti morate gruče CFDA, ki jih je mogoče povezati s številkami CFDA pri poizvedbi glede načrta porabe zveznih subvencij.</span><span class="sxs-lookup"><span data-stu-id="c4043-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="c4043-116">Izberite **Vodenje projektov in računovodstvo \> Nastavitev \> Subvencije \> Gruče kataloga za zvezno pomoč domačim entitetam**.</span><span class="sxs-lookup"><span data-stu-id="c4043-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="c4043-117">Izberite **Novo**, da ustvarite gručo CFDA.</span><span class="sxs-lookup"><span data-stu-id="c4043-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="c4043-118">Vnesite ime gruče.</span><span class="sxs-lookup"><span data-stu-id="c4043-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="c4043-119">Izberite **Shrani**, da shranite spremembe.</span><span class="sxs-lookup"><span data-stu-id="c4043-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="c4043-120">Nastavitev številk CFDA</span><span class="sxs-lookup"><span data-stu-id="c4043-120">Set up CFDA numbers</span></span>

<span data-ttu-id="c4043-121">Nastaviti morate številke CFDA, ki jih je mogoče dodati subvencijam in vključiti v poizvedbo glede načrta porabe zveznih subvencij.</span><span class="sxs-lookup"><span data-stu-id="c4043-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="c4043-122">Izberite **Vodenje projektov in računovodstvo \> Nastavitev \> Subvencije \> Številke kataloga za zvezno pomoč domačim entitetam**.</span><span class="sxs-lookup"><span data-stu-id="c4043-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="c4043-123">Izberite **Novo**, da ustvarite številko CFDA.</span><span class="sxs-lookup"><span data-stu-id="c4043-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="c4043-124">V stolpec **Številka** vnesite številko CFDA.</span><span class="sxs-lookup"><span data-stu-id="c4043-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="c4043-125">Pritisnite **tabulatorko**.</span><span class="sxs-lookup"><span data-stu-id="c4043-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="c4043-126">V stolpec **Opis** vnesite naziv CFDA.</span><span class="sxs-lookup"><span data-stu-id="c4043-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="c4043-127">Pritisnite **tabulatorko**.</span><span class="sxs-lookup"><span data-stu-id="c4043-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="c4043-128">Izbirno: v polje **Programska gruča** dodajte ustrezno gručo CFDA.</span><span class="sxs-lookup"><span data-stu-id="c4043-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="c4043-129">Izberite **Shrani**, da shranite spremembe.</span><span class="sxs-lookup"><span data-stu-id="c4043-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="c4043-130">Vzpostavitev subvencij za poročanje glede poizvedbe glede načrta porabe zveznih subvencij</span><span class="sxs-lookup"><span data-stu-id="c4043-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="c4043-131">Izberite **Vodenje projektov in računovodstvo \> Subvencije \> Subvencije** in izberite obstoječo subvencijo.</span><span class="sxs-lookup"><span data-stu-id="c4043-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="c4043-132">Na zavihku za hitri dostop **Nastavitev** v polju **Katalog za zvezno pomoč domačim entitetam** dodelite številko CFDA.</span><span class="sxs-lookup"><span data-stu-id="c4043-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="c4043-133">Številka CFDA pri subvenciji določa gručo CFDA za poročanje.</span><span class="sxs-lookup"><span data-stu-id="c4043-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="c4043-134">Na zavihku za hitri dostop **Podatki za stik** vnesite podatke o dajalcu subvencije tako, da upoštevate ta navodila:</span><span class="sxs-lookup"><span data-stu-id="c4043-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="c4043-135">V polju **Prejemnik subvencije** vnesite prejemnika, ki je odgovoren za subvencijo.</span><span class="sxs-lookup"><span data-stu-id="c4043-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="c4043-136">Za obstoječo subvencijo so ti podatki morda že vneseni.</span><span class="sxs-lookup"><span data-stu-id="c4043-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="c4043-137">Navedite, ali prejemnik subvencije zagotavlja tudi sredstva.</span><span class="sxs-lookup"><span data-stu-id="c4043-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="c4043-138">Če prejemnik subvencije zagotavlja tudi sredstva, pustite potrditveno polje **Prehodno** prazno.</span><span class="sxs-lookup"><span data-stu-id="c4043-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="c4043-139">Če sredstva zagotavlja druga stranka ter je prejemnik subvencije odgovoren za porabo in spremljanje denarja, izberite potrditveno polje **Prehodno**.</span><span class="sxs-lookup"><span data-stu-id="c4043-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="c4043-140">Če ste izbrali potrditveno polje **Prehodno** v prejšnjem koraku, v polje **Agencija, ki podeljuje subvencijo** vnesite stranko, ki je zagotovila subvencijo.</span><span class="sxs-lookup"><span data-stu-id="c4043-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="c4043-141">Agencija, ki podeljuje subvencijo, in prejemnik subvencije ne moreta biti ista stranka.</span><span class="sxs-lookup"><span data-stu-id="c4043-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="c4043-142">Tu je primer subvencije s prehodno entiteto:</span><span class="sxs-lookup"><span data-stu-id="c4043-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="c4043-143">Zvezna vlada je financirala infrastrukturni projekt za zvezno državo.</span><span class="sxs-lookup"><span data-stu-id="c4043-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="c4043-144">Zvezna vlada je zvezni državi dala denar, da bi ga slednja porabila.</span><span class="sxs-lookup"><span data-stu-id="c4043-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="c4043-145">V tem primeru je zvezna vlada agencija, ki podeljuje subvencijo, zvezna država pa prejemnik subvencije.</span><span class="sxs-lookup"><span data-stu-id="c4043-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="c4043-146">Ko prvič vklopite funkcijo, bodo začetne številke CFDA vnesene z uporabo obstoječih številk pri subvencijah.</span><span class="sxs-lookup"><span data-stu-id="c4043-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="c4043-147">Izključitev subvencij v zvezi s poročanjem SEFA glede na vrsto subvencije</span><span class="sxs-lookup"><span data-stu-id="c4043-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="c4043-148">Odprite razdelek **Vodenje projektov in računovodstvo \> Nastavitev \> Subvencije \> Vrste subvencij**.</span><span class="sxs-lookup"><span data-stu-id="c4043-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="c4043-149">Na zavihku za hitri dostop **Privzeti podatki** izberite potrditveno polje **Izključi iz načrta porabe zveznih subvencij**.</span><span class="sxs-lookup"><span data-stu-id="c4043-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="c4043-150">Izberite **Shrani**, da shranite spremembe.</span><span class="sxs-lookup"><span data-stu-id="c4043-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="c4043-151">Zagon poizvedbe glede načrta porabe zveznih subvencij</span><span class="sxs-lookup"><span data-stu-id="c4043-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="c4043-152">Izberite **Vodenje projektov in računovodstvo \> Poizvedbe in poročila \> Poizvedba glede subvencije \> Načrt porabe zveznih subvencij**.</span><span class="sxs-lookup"><span data-stu-id="c4043-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="c4043-153">V razdelku **Parametri** upoštevajte ta navodila:</span><span class="sxs-lookup"><span data-stu-id="c4043-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="c4043-154">V polju **Datumski interval** izberite kodo za datumski interval.</span><span class="sxs-lookup"><span data-stu-id="c4043-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="c4043-155">Lahko pa določite datumski interval tudi prek polj **Začetni datum** in **Končni datum**.</span><span class="sxs-lookup"><span data-stu-id="c4043-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="c4043-156">Izbirno: če želite v poizvedbo kot prihodek vključiti samo obračunane transakcije, nastavite možnost **Vključi samo obračunane prihodke** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="c4043-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="c4043-157">Št. stolpcev</span><span class="sxs-lookup"><span data-stu-id="c4043-157">Columns</span></span>

<span data-ttu-id="c4043-158">Poizvedba glede načrta porabe zveznih subvencij vključuje naslednje stolpce:</span><span class="sxs-lookup"><span data-stu-id="c4043-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="c4043-159">Ime gruče kataloga za zvezno pomoč domačim entitetam</span><span class="sxs-lookup"><span data-stu-id="c4043-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="c4043-160">Agencija, ki podeljuje subvencijo</span><span class="sxs-lookup"><span data-stu-id="c4043-160">Grantor agency</span></span>
- <span data-ttu-id="c4043-161">Prehodna agencija</span><span class="sxs-lookup"><span data-stu-id="c4043-161">Pass-through agency</span></span>
- <span data-ttu-id="c4043-162">Ime subvencije</span><span class="sxs-lookup"><span data-stu-id="c4043-162">Grant name</span></span>
- <span data-ttu-id="c4043-163">ID subvencije</span><span class="sxs-lookup"><span data-stu-id="c4043-163">Grant ID</span></span>
- <span data-ttu-id="c4043-164">ID vloge za subvencijo</span><span class="sxs-lookup"><span data-stu-id="c4043-164">Grant application ID</span></span>
- <span data-ttu-id="c4043-165">Katalog za zvezno pomoč domačim entitetam</span><span class="sxs-lookup"><span data-stu-id="c4043-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="c4043-166">Potrdila</span><span class="sxs-lookup"><span data-stu-id="c4043-166">Receipts</span></span>
- <span data-ttu-id="c4043-167">Izdatki</span><span class="sxs-lookup"><span data-stu-id="c4043-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]