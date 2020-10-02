---
title: Konfiguracija avtomatiziranega ustvarjanja računov
description: Ta tema vsebuje informacije o tem, kako nastaviti sistem za samodejno ustvarjanje računov.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898146"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="d1aac-103">Konfiguracija avtomatiziranega ustvarjanja računov</span><span class="sxs-lookup"><span data-stu-id="d1aac-103">Configure automated invoice creation</span></span>

<span data-ttu-id="d1aac-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="d1aac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d1aac-105">Dokončajte naslednje korake, da konfigurirate samodejni zagon računa v storitvi Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d1aac-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="d1aac-106">Odprite **Nastavitve** \> **Paketna opravila**.</span><span class="sxs-lookup"><span data-stu-id="d1aac-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="d1aac-107">Ustvarite paketno opravilo in ga poimenujte **Ustvarjanje računov v storitvi Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="d1aac-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="d1aac-108">Ime paketnega opravila mora vključevati izraz »Ustvarjanje računov«.</span><span class="sxs-lookup"><span data-stu-id="d1aac-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="d1aac-109">V polju **Vrsta posla** izberite **Brez**.</span><span class="sxs-lookup"><span data-stu-id="d1aac-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="d1aac-110">Možnosti **Pogostost: dnevno** in **Je aktivno** sta nastavljeni na **Da**.</span><span class="sxs-lookup"><span data-stu-id="d1aac-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="d1aac-111">Izberite **Zaženi potek dela**.</span><span class="sxs-lookup"><span data-stu-id="d1aac-111">Select **Run Workflow**.</span></span> <span data-ttu-id="d1aac-112">V pogovornem oknu **Poišči zapis** vidite tri poteke dela:</span><span class="sxs-lookup"><span data-stu-id="d1aac-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="d1aac-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="d1aac-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="d1aac-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="d1aac-114">ProcessRunner</span></span>
    - <span data-ttu-id="d1aac-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="d1aac-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="d1aac-116">Izberite **ProcessRunCaller** in nato **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="d1aac-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="d1aac-117">V naslednjem pogovornem oknu izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="d1aac-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="d1aac-118">Poteku dela **Spanje** sledi potek dela **Proces**.</span><span class="sxs-lookup"><span data-stu-id="d1aac-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="d1aac-119">V 5. koraku lahko izberete tudi **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="d1aac-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="d1aac-120">Ko nato izberete **V redu**, poteku dela **Proces** sledi potek dela **Spanje**.</span><span class="sxs-lookup"><span data-stu-id="d1aac-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="d1aac-121">Poteka dela **ProcessRunCaller** in **ProcessRunner** ustvarita račune.</span><span class="sxs-lookup"><span data-stu-id="d1aac-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="d1aac-122">**ProcessRunCaller** prikliče **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="d1aac-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="d1aac-123">**ProcessRunner** je potek dela, ki dejansko ustvari račune.</span><span class="sxs-lookup"><span data-stu-id="d1aac-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="d1aac-124">Gre skozi vse vrstice pogodbe, za katere je treba ustvariti račune, in ustvari račune za te vrstice.</span><span class="sxs-lookup"><span data-stu-id="d1aac-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="d1aac-125">Opravilo preveri datume izdaje računa za vrstice pogodbe, da ugotovi, za katere vrstice pogodbe je treba ustvariti račune.</span><span class="sxs-lookup"><span data-stu-id="d1aac-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="d1aac-126">Če imajo vrstice pogodbe, ki pripadajo eni pogodbi, enak datum izdaje računa, se transakcije združijo v en račun, ki ima dve vrstici računa.</span><span class="sxs-lookup"><span data-stu-id="d1aac-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="d1aac-127">Če ni transakcij, za katere bi se lahko ustvarili računi, opravilo preskoči ustvarjanje računa.</span><span class="sxs-lookup"><span data-stu-id="d1aac-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="d1aac-128">Ko se potek dela **processrunner** preneha izvajati, prikliče potek dela **ProcessRunCaller**, navede končni čas in se zapre.</span><span class="sxs-lookup"><span data-stu-id="d1aac-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="d1aac-129">**ProcessRunCaller** nato zažene časovnik, ki se izvaja 24 ur od navedenega končnega časa.</span><span class="sxs-lookup"><span data-stu-id="d1aac-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="d1aac-130">Ko se časovnik preneha izvajati, se **ProcessRunCaller** zapre.</span><span class="sxs-lookup"><span data-stu-id="d1aac-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="d1aac-131">Paketna obdelava za ustvarjanje računov je ponavljajoče se opravilo.</span><span class="sxs-lookup"><span data-stu-id="d1aac-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="d1aac-132">Če se paketna obdelava zažene večkrat, se ustvari več primerkov opravila in pride do napak.</span><span class="sxs-lookup"><span data-stu-id="d1aac-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="d1aac-133">Zato paketno obdelavo zaženite samo enkrat in jo znova zaženite le, če se preneha izvajati.</span><span class="sxs-lookup"><span data-stu-id="d1aac-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="d1aac-134">Paketno izdajanje računov se izvaja samo za podrobnosti pogodbe, ki so konfigurirane z razporedi izdajanja računov.</span><span class="sxs-lookup"><span data-stu-id="d1aac-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="d1aac-135">V podrobnostih pogodbe z načinom obračunavanja s fiksno ceno morajo biti nastavljeni mejniki.</span><span class="sxs-lookup"><span data-stu-id="d1aac-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="d1aac-136">V podrobnostih pogodbe z načinom obračunavanja za časovne in materialne transakcije je treba nastaviti datumski urnik računov.</span><span class="sxs-lookup"><span data-stu-id="d1aac-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="d1aac-137">Enako velja v podrobnosti pogodbe za projekt.</span><span class="sxs-lookup"><span data-stu-id="d1aac-137">The same applies to a project-based contract line.</span></span>     
