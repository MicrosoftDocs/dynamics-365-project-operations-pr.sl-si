---
title: Določanje vrste uvedbe
description: Ta tema vsebuje informacije za pomoč pri izbiri prave vrste uvajanja za projektne postopke v vašem podjetju.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084760"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="95a69-103">Določanje vrste uvedbe</span><span class="sxs-lookup"><span data-stu-id="95a69-103">Determine your deployment type</span></span>

<span data-ttu-id="95a69-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="95a69-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95a69-105">Po nakupu licence določite najboljši model uvajanja v aplikaciji Dynamics 365 Project Operations z uporabo [vodenega postopka namestitve](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="95a69-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="95a69-106">Ko dokončate vodeni postopek namestitve, boste preusmerjeni na pravi portal za upravljanje, da dokončate namestitev.</span><span class="sxs-lookup"><span data-stu-id="95a69-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="95a69-107">Za dokončanje namestitve glejte podrobnosti o uvajanju.</span><span class="sxs-lookup"><span data-stu-id="95a69-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="95a69-108">Obstoječe stranke rešitve Dynamics, ki uporabljajo aplikacijo Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="95a69-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="95a69-109">Aplikacija Project Operations vključuje zmogljivosti, ki so bile na voljo v aplikaciji Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="95a69-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="95a69-110">Za te stranke bo v prihodnosti objavljena možnost nadgraditve.</span><span class="sxs-lookup"><span data-stu-id="95a69-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="95a69-111">Obstoječe stranke aplikacije Dynamics 365 Finance, ki uporabljajo Projektno vodenje in računovodstvo</span><span class="sxs-lookup"><span data-stu-id="95a69-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="95a69-112">Obstoječe stranke aplikacije Finance, ki uporabljajo projektno upravljanje in računovodske funkcije, lahko to še naprej uporabljajo v dozdajšnji obliki.</span><span class="sxs-lookup"><span data-stu-id="95a69-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="95a69-113">Glejte razdelek [Aplikacija Project Operations za scenarije z naročili na zalogi/v proizvodnji](#pma).</span><span class="sxs-lookup"><span data-stu-id="95a69-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="95a69-114">Vrste uvajanja</span><span class="sxs-lookup"><span data-stu-id="95a69-114">Deployment types</span></span>
<span data-ttu-id="95a69-115">Aplikacija Project Operations podpira več možnosti uvajanja, ki ustrezajo vašim zahtevam.</span><span class="sxs-lookup"><span data-stu-id="95a69-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="95a69-116">Ne glede na to, ali ste nov ali obstoječ uporabnik rešitve Dynamics 365, lahko aplikacija Project Operations ustreza vašim zahtevam.</span><span class="sxs-lookup"><span data-stu-id="95a69-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="95a69-117">Naš [vprašalnik o uvajanju](https://aka.ms/provisionprojectoperations) vam bo pomagal določiti pravo vrsto uvajanja.</span><span class="sxs-lookup"><span data-stu-id="95a69-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="95a69-118">Rezultati vas bodo vodili do enega od naslednjih vrst uvajanja:</span><span class="sxs-lookup"><span data-stu-id="95a69-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="95a69-119">Poenostavljeno uvajanje – posel do izstavitve predračuna</span><span class="sxs-lookup"><span data-stu-id="95a69-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="95a69-120">Project Operations za primere uporabe z viri/brez zalog</span><span class="sxs-lookup"><span data-stu-id="95a69-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="95a69-121">Project Operations za primere uporabe z naročili na zalogi/v proizvodnji</span><span class="sxs-lookup"><span data-stu-id="95a69-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="95a69-122">Aplikacija Project Operations podpira primere naročil na zalogi/v proizvodnji in primere z viri/brez zalog v istem okolju prek konfiguracij na ravni pravne osebe.</span><span class="sxs-lookup"><span data-stu-id="95a69-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="95a69-123">Družba Contoso lahko na primer izkoristi zmogljivosti zalog/proizvodnih naročil v svojem ameriškem proizvodnem obratu (pravna oseba = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="95a69-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="95a69-124">Družba Contoso lahko na primer izkoristi zmogljivosti virov/brez zalog v njihovem obratu za servisiranje Contoso Robotics Arms v ZK (pravna oseba = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="95a69-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="95a69-125">Poenostavljeno uvajanje – posel do izstavitve predračuna</span><span class="sxs-lookup"><span data-stu-id="95a69-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="95a69-126">Poenostavljeno uvajanje vključuje naslednje zmožnosti:</span><span class="sxs-lookup"><span data-stu-id="95a69-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="95a69-127">Načrtovanje projektov z uporabo spletne aplikacije Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="95a69-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="95a69-128">Večrazsežnostno oblikovanje cen</span><span class="sxs-lookup"><span data-stu-id="95a69-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="95a69-129">Poenoteno upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="95a69-129">Unified Resource Management</span></span>
- <span data-ttu-id="95a69-130">Sledenje času</span><span class="sxs-lookup"><span data-stu-id="95a69-130">Time Tracking</span></span>
- <span data-ttu-id="95a69-131">Osnovne stroške</span><span class="sxs-lookup"><span data-stu-id="95a69-131">Basic Expense</span></span>
- <span data-ttu-id="95a69-132">Predloge računov</span><span class="sxs-lookup"><span data-stu-id="95a69-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="95a69-133">Koraki uvajanja</span><span class="sxs-lookup"><span data-stu-id="95a69-133">Deployment steps</span></span>
<span data-ttu-id="95a69-134">Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="95a69-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="95a69-135">Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](lite-preview-subscription-sign-up.md) in [Omogočanje novega okolja](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="95a69-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="95a69-136">Project Operations za primere uporabe z viri/brez zalog</span><span class="sxs-lookup"><span data-stu-id="95a69-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="95a69-137">Projektni postopki za primere z viri/brez zalog vključujejo naslednje zmožnosti:</span><span class="sxs-lookup"><span data-stu-id="95a69-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="95a69-138">Načrtovanje projektov z uporabo spletne aplikacije Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="95a69-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="95a69-139">Večrazsežnostno oblikovanje cen</span><span class="sxs-lookup"><span data-stu-id="95a69-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="95a69-140">Poenoteno upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="95a69-140">Unified Resource Management</span></span>
- <span data-ttu-id="95a69-141">Sledenje času</span><span class="sxs-lookup"><span data-stu-id="95a69-141">Time Tracking</span></span>
- <span data-ttu-id="95a69-142">Osnovne stroške</span><span class="sxs-lookup"><span data-stu-id="95a69-142">Basic Expense</span></span>
- <span data-ttu-id="95a69-143">Celotni stroški</span><span class="sxs-lookup"><span data-stu-id="95a69-143">Full Expense</span></span>
- <span data-ttu-id="95a69-144">Optično branje računov s tehnologijo OCR</span><span class="sxs-lookup"><span data-stu-id="95a69-144">Receipt OCR</span></span>
- <span data-ttu-id="95a69-145">Celoten postopek izdaje računa</span><span class="sxs-lookup"><span data-stu-id="95a69-145">Full Invoicing</span></span>
- <span data-ttu-id="95a69-146">Pripoznavanje prihodkov</span><span class="sxs-lookup"><span data-stu-id="95a69-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="95a69-147">Koraki uvajanja</span><span class="sxs-lookup"><span data-stu-id="95a69-147">Deployment steps</span></span>
<span data-ttu-id="95a69-148">Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="95a69-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="95a69-149">Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](resource-sign-up-preview-subscription.md) in [Omogočanje novega okolja](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="95a69-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="95a69-150">Project Operations za primere uporabe z naročili na zalogi/v proizvodnji</span><span class="sxs-lookup"><span data-stu-id="95a69-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="95a69-151">Načrtovanje projekta z uporabo SČD</span><span class="sxs-lookup"><span data-stu-id="95a69-151">Project planning using WBS</span></span>
- <span data-ttu-id="95a69-152">Upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="95a69-152">Resource Management</span></span>
- <span data-ttu-id="95a69-153">Sledenje času</span><span class="sxs-lookup"><span data-stu-id="95a69-153">Time Tracking</span></span>
- <span data-ttu-id="95a69-154">Celotni stroški</span><span class="sxs-lookup"><span data-stu-id="95a69-154">Full Expense</span></span>
- <span data-ttu-id="95a69-155">Optično branje računov s tehnologijo OCR</span><span class="sxs-lookup"><span data-stu-id="95a69-155">Receipt OCR</span></span>
- <span data-ttu-id="95a69-156">Celoten postopek izdaje računa</span><span class="sxs-lookup"><span data-stu-id="95a69-156">Full Invoicing</span></span>
- <span data-ttu-id="95a69-157">Pripoznavanje prihodkov</span><span class="sxs-lookup"><span data-stu-id="95a69-157">Revenue Recognition</span></span>
- <span data-ttu-id="95a69-158">Proizvodna naročila</span><span class="sxs-lookup"><span data-stu-id="95a69-158">Production Orders</span></span>
- <span data-ttu-id="95a69-159">Podpora za materiale</span><span class="sxs-lookup"><span data-stu-id="95a69-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="95a69-160">Koraki uvajanja</span><span class="sxs-lookup"><span data-stu-id="95a69-160">Deployment steps</span></span>
<span data-ttu-id="95a69-161">Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="95a69-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="95a69-162">Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) in [Omogočanje novega okolja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="95a69-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

