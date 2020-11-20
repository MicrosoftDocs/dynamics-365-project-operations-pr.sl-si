---
title: Privzete vrednosti finančnih razsežnosti
description: V tej temi so na voljo informacije o tem, kako nastaviti privzete vrednosti finančne razsežnosti.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131903"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="0e3b9-103">Privzete vrednosti finančnih razsežnosti</span><span class="sxs-lookup"><span data-stu-id="0e3b9-103">Financial dimension defaults</span></span>

<span data-ttu-id="0e3b9-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="0e3b9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0e3b9-105">Dynamics 365 Project Operations uporablja ogrodje [Finančne razsežnosti](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) v storitvi Dynamics 365 Finance za podajanje dodatnih vpogledov na transakcije podknjige in glavne knjige projekta.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="0e3b9-106">Privzete finančne razsežnosti je mogoče nastaviti na stranko, vir financiranja projekta, mejnik, vrstico projektne pogodbe ali projekt.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="0e3b9-107">Določanje privzetih finančnih razsežnosti za stranko</span><span class="sxs-lookup"><span data-stu-id="0e3b9-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="0e3b9-108">Privzete razsežnosti stranke so določene v storitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="0e3b9-109">Dokončajte naslednje korake za nastavitev privzetih vrednosti razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="0e3b9-110">Pojdite na **Terjatve** > **Stranke** > **Vse stranke**.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="0e3b9-111">Na strani **Stranke** na zavihku **Finančne razsežnosti** nastavite vrednost finančne razsežnosti za določeno stranko.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="0e3b9-112">Določanje privzetih finančnih razsežnosti za projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="0e3b9-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="0e3b9-113">Projektne pogodbe so ustvarjene in vzdrževane v storitvi Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="0e3b9-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="0e3b9-114">Računovodski atributi za projektne pogodbe so nastavljeni v modulu **Upravljanje projektov in računovodstvo** v storitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="0e3b9-115">Nastavitev finančnih razsežnosti za vir financiranja projekta</span><span class="sxs-lookup"><span data-stu-id="0e3b9-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="0e3b9-116">Odprite **Vodenje projektov in računovodstvo** > **Projekti** > **Projektne pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="0e3b9-117">Izberite zapis, ki ga želite posodobiti, in na zavihku **Projektna pogodba** izberite **Prikaži privzeto računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="0e3b9-118">Razširite **Povezane informacije** in izberite zavihek **Viri financiranja**.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="0e3b9-119">Nastavite privzete vrednosti finančne razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="0e3b9-120">Upoštevajte, da so privzete vrednosti finančne razsežnosti iz računa stranke.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="0e3b9-121">Nastavitev finančnih razsežnosti za podrobnosti pogodbe projekta</span><span class="sxs-lookup"><span data-stu-id="0e3b9-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="0e3b9-122">Odprite **Vodenje projektov in računovodstvo** > **Projekti** > **Projektne pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="0e3b9-123">Izberite zapis, ki ga želite posodobiti, in na zavihku **Projektna pogodba** izberite **Prikaži privzeto računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="0e3b9-124">Razširite **Povezane informacije** in izberite zavihek **Podrobnosti pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="0e3b9-125">Nastavite privzete vrednosti finančne razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="0e3b9-126">Privzete vrednosti finančne razsežnosti so veljavne in se lahko uporabljajo samo s podrobnostmi pogodbe fiksne cene (mejnik).</span><span class="sxs-lookup"><span data-stu-id="0e3b9-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="0e3b9-127">Te privzete vrednosti se uporabljajo na povezanih transakcijah za kupca in vrsticah računov projekta.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="0e3b9-128">Določanje privzetih finančnih razsežnosti za projekte</span><span class="sxs-lookup"><span data-stu-id="0e3b9-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="0e3b9-129">Projekti so ustvarjeni in vzdrževani v storitvi CDS.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="0e3b9-130">Računovodski atributi za projekte so nastavljeni v modulu **Upravljanje projektov in računovodstvo** v storitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="0e3b9-131">Odprite **Vodenje projekta in računovodstvo** > **Projekti** > **Vsi projekti**.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="0e3b9-132">Izberite zapis, ki ga želite posodobiti, in na zavihku **Projekt** izberite **Prikaži privzeto računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="0e3b9-133">Razširite **Povezane informacije** in izberite zavihek **Nastavitev**.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="0e3b9-134">Nastavite privzete vrednosti finančne razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="0e3b9-135">Upoštevajte, da so privzete vrednosti finančne razsežnosti iz računa stranke.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="0e3b9-136">Če je projekt povezan s podrobnostmi pogodbe z več strankami za pogodbo projekta, se uporabi primarna stranka za nastavitev finančnih razsežnosti na privzete.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="0e3b9-137">Privzete finančne razsežnosti projekta se uporabljajo za nastavitev privzetih vrednosti vrstice dnevnika za čas, stroške in brezplačne transakcije v možnosti **Dnevnik integracij za Project Operations** ter na povezanih projektnih vrsticah računa.</span><span class="sxs-lookup"><span data-stu-id="0e3b9-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
