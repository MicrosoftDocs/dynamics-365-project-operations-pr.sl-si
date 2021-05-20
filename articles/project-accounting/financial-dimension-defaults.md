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
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950149"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="c222d-103">Privzete vrednosti finančnih razsežnosti</span><span class="sxs-lookup"><span data-stu-id="c222d-103">Financial dimension defaults</span></span>

<span data-ttu-id="c222d-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="c222d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c222d-105">Dynamics 365 Project Operations uporablja ogrodje [Finančne razsežnosti](/dynamics365/finance/general-ledger/financial-dimensions) v storitvi Dynamics 365 Finance za podajanje dodatnih vpogledov na transakcije podknjige in glavne knjige projekta.</span><span class="sxs-lookup"><span data-stu-id="c222d-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="c222d-106">Privzete finančne razsežnosti je mogoče nastaviti na stranko, vir financiranja projekta, mejnik, vrstico projektne pogodbe ali projekt.</span><span class="sxs-lookup"><span data-stu-id="c222d-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="c222d-107">Določanje privzetih finančnih razsežnosti za stranko</span><span class="sxs-lookup"><span data-stu-id="c222d-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="c222d-108">Privzete razsežnosti stranke so določene v storitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="c222d-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="c222d-109">Dokončajte naslednje korake za nastavitev privzetih vrednosti razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="c222d-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="c222d-110">Pojdite na **Terjatve** > **Stranke** > **Vse stranke**.</span><span class="sxs-lookup"><span data-stu-id="c222d-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="c222d-111">Na strani **Stranke** na zavihku **Finančne razsežnosti** nastavite vrednost finančne razsežnosti za določeno stranko.</span><span class="sxs-lookup"><span data-stu-id="c222d-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="c222d-112">Določanje privzetih finančnih razsežnosti za projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="c222d-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="c222d-113">Projektne pogodbe so ustvarjene in vzdrževane v storitvi Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="c222d-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="c222d-114">Računovodski atributi za projektne pogodbe so nastavljeni v modulu **Upravljanje projektov in računovodstvo** v storitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="c222d-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="c222d-115">Nastavitev finančnih razsežnosti za vir financiranja projekta</span><span class="sxs-lookup"><span data-stu-id="c222d-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="c222d-116">Odprite **Vodenje projektov in računovodstvo** > **Projekti** > **Projektne pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="c222d-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="c222d-117">Izberite zapis, ki ga želite posodobiti, in na zavihku **Projektna pogodba** izberite **Prikaži privzeto računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="c222d-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="c222d-118">Razširite **Povezane informacije** in izberite zavihek **Viri financiranja**.</span><span class="sxs-lookup"><span data-stu-id="c222d-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="c222d-119">Nastavite privzete vrednosti finančne razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="c222d-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="c222d-120">Upoštevajte, da so privzete vrednosti finančne razsežnosti iz računa stranke.</span><span class="sxs-lookup"><span data-stu-id="c222d-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="c222d-121">Nastavitev finančnih razsežnosti za podrobnosti pogodbe projekta</span><span class="sxs-lookup"><span data-stu-id="c222d-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="c222d-122">Odprite **Vodenje projektov in računovodstvo** > **Projekti** > **Projektne pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="c222d-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="c222d-123">Izberite zapis, ki ga želite posodobiti, in na zavihku **Projektna pogodba** izberite **Prikaži privzeto računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="c222d-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="c222d-124">Razširite **Povezane informacije** in izberite zavihek **Podrobnosti pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="c222d-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="c222d-125">Nastavite privzete vrednosti finančne razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="c222d-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="c222d-126">Privzete vrednosti finančne razsežnosti so veljavne in se lahko uporabljajo samo s podrobnostmi pogodbe fiksne cene (mejnik).</span><span class="sxs-lookup"><span data-stu-id="c222d-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="c222d-127">Te privzete vrednosti se uporabljajo na povezanih transakcijah za kupca in vrsticah računov projekta.</span><span class="sxs-lookup"><span data-stu-id="c222d-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="c222d-128">Določanje privzetih finančnih razsežnosti za projekte</span><span class="sxs-lookup"><span data-stu-id="c222d-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="c222d-129">Projekti so ustvarjeni in vzdrževani v storitvi CDS.</span><span class="sxs-lookup"><span data-stu-id="c222d-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="c222d-130">Računovodski atributi za projekte so nastavljeni v modulu **Upravljanje projektov in računovodstvo** v storitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="c222d-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="c222d-131">Odprite **Vodenje projekta in računovodstvo** > **Projekti** > **Vsi projekti**.</span><span class="sxs-lookup"><span data-stu-id="c222d-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="c222d-132">Izberite zapis, ki ga želite posodobiti, in na zavihku **Projekt** izberite **Prikaži privzeto računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="c222d-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="c222d-133">Razširite **Povezane informacije** in izberite zavihek **Nastavitev**.</span><span class="sxs-lookup"><span data-stu-id="c222d-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="c222d-134">Nastavite privzete vrednosti finančne razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="c222d-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="c222d-135">Upoštevajte, da so privzete vrednosti finančne razsežnosti iz računa stranke.</span><span class="sxs-lookup"><span data-stu-id="c222d-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="c222d-136">Če je projekt povezan s podrobnostmi pogodbe z več strankami za pogodbo projekta, se uporabi primarna stranka za nastavitev finančnih razsežnosti na privzete.</span><span class="sxs-lookup"><span data-stu-id="c222d-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="c222d-137">Privzete finančne razsežnosti projekta se uporabljajo za nastavitev privzetih vrednosti vrstice dnevnika za čas, stroške in brezplačne transakcije v možnosti **Dnevnik integracij za Project Operations** ter na povezanih projektnih vrsticah računa.</span><span class="sxs-lookup"><span data-stu-id="c222d-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]