---
title: Vrste uvajanja
description: Ta tema vsebuje informacije za pomoč pri izbiri prave vrste uvajanja za projektne postopke v vašem podjetju.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949078"
---
# <a name="deployment-types"></a><span data-ttu-id="fb5b9-103">Vrste uvajanja</span><span class="sxs-lookup"><span data-stu-id="fb5b9-103">Deployment types</span></span>

<span data-ttu-id="fb5b9-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="fb5b9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb5b9-105">Po nakupu licence določite najboljši model uvajanja v aplikaciji Dynamics 365 Project Operations z uporabo [vodenega postopka namestitve](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="fb5b9-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="fb5b9-106">Ko dokončate vodeni postopek namestitve, boste preusmerjeni na pravi portal za upravljanje, da dokončate namestitev.</span><span class="sxs-lookup"><span data-stu-id="fb5b9-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="fb5b9-107">Za dokončanje namestitve glejte spodnje podrobnosti o uvajanju.</span><span class="sxs-lookup"><span data-stu-id="fb5b9-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="fb5b9-108">Obstoječe stranke rešitve Dynamics, ki uporabljajo aplikacijo Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fb5b9-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="fb5b9-109">Aplikacija Project Operations vključuje zmogljivosti, ki so bile na voljo v aplikaciji Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fb5b9-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="fb5b9-110">Za te stranke bo v prihodnosti objavljena možnost nadgraditve.</span><span class="sxs-lookup"><span data-stu-id="fb5b9-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="fb5b9-111">Obstoječe stranke aplikacije Dynamics 365 Finance, ki uporabljajo Projektno vodenje in računovodstvo</span><span class="sxs-lookup"><span data-stu-id="fb5b9-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="fb5b9-112">Obstoječe stranke aplikacije Finance, ki uporabljajo projektno upravljanje in računovodske funkcije, lahko to še naprej uporabljajo v dozdajšnji obliki.</span><span class="sxs-lookup"><span data-stu-id="fb5b9-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="fb5b9-113">Glejte razdelek [Aplikacija Project Operations za scenarije z naročili na zalogi/v proizvodnji](#pma).</span><span class="sxs-lookup"><span data-stu-id="fb5b9-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="fb5b9-114">Aplikacija Project Operations podpira več možnosti uvajanja, ki ustrezajo vašim zahtevam.</span><span class="sxs-lookup"><span data-stu-id="fb5b9-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="fb5b9-115">Ne glede na to, ali ste nov ali obstoječ uporabnik rešitve Dynamics 365, lahko aplikacija Project Operations ustreza vašim zahtevam.</span><span class="sxs-lookup"><span data-stu-id="fb5b9-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="fb5b9-116">Naš [vprašalnik o uvajanju](https://aka.ms/provisionprojectoperations) vam bo pomagal določiti pravo vrsto uvajanja.</span><span class="sxs-lookup"><span data-stu-id="fb5b9-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="fb5b9-117">Rezultati vas bodo vodili do enega od naslednjih vrst uvajanja:</span><span class="sxs-lookup"><span data-stu-id="fb5b9-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="fb5b9-118">Poenostavljeno uvajanje – posel do izstavitve predračuna</span><span class="sxs-lookup"><span data-stu-id="fb5b9-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="fb5b9-119">Project Operations za primere uporabe z viri/brez zalog</span><span class="sxs-lookup"><span data-stu-id="fb5b9-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="fb5b9-120">Project Operations za primere uporabe z naročili na zalogi/v proizvodnji</span><span class="sxs-lookup"><span data-stu-id="fb5b9-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="fb5b9-121">Aplikacija Project Operations podpira primere naročil na zalogi/v proizvodnji in primere z viri/brez zalog v istem okolju prek konfiguracij na ravni pravne osebe.</span><span class="sxs-lookup"><span data-stu-id="fb5b9-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="fb5b9-122">Družba Contoso lahko na primer izkoristi zmogljivosti zalog/proizvodnih naročil v svojem ameriškem proizvodnem obratu (pravna oseba = Contoso Manufacturing United States) in zmogljivosti z viri/brez zalog v njihovem obratu za servisiranje Contoso Robotics Arms v Veliki Britaniji (pravna oseba = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="fb5b9-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="fb5b9-123"><a name="lite"><a/>Poenostavljeno uvajanje – posel do izstavitve predračuna</span><span class="sxs-lookup"><span data-stu-id="fb5b9-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="fb5b9-124">Poenostavljeno uvajanje vključuje naslednje zmožnosti:</span><span class="sxs-lookup"><span data-stu-id="fb5b9-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="fb5b9-125">Načrtovanje projektov z uporabo spletne aplikacije Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="fb5b9-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="fb5b9-126">Večrazsežnostno oblikovanje cen</span><span class="sxs-lookup"><span data-stu-id="fb5b9-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="fb5b9-127">Poenoteno upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="fb5b9-127">Unified Resource Management</span></span>
- <span data-ttu-id="fb5b9-128">Sledenje času</span><span class="sxs-lookup"><span data-stu-id="fb5b9-128">Time Tracking</span></span>
- <span data-ttu-id="fb5b9-129">Osnovne stroške</span><span class="sxs-lookup"><span data-stu-id="fb5b9-129">Basic Expense</span></span>
- <span data-ttu-id="fb5b9-130">Predloge računov</span><span class="sxs-lookup"><span data-stu-id="fb5b9-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="fb5b9-131">Koraki uvajanja:</span><span class="sxs-lookup"><span data-stu-id="fb5b9-131">Deployment steps:</span></span>
<span data-ttu-id="fb5b9-132">Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="fb5b9-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="fb5b9-133">Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](lite-preview-subscription-sign-up.md) in [Omogočanje novega okolja](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="fb5b9-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="fb5b9-134"><a name="integrated"><a/>Project Operations za primere uporabe z viri/brez zalog</span><span class="sxs-lookup"><span data-stu-id="fb5b9-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="fb5b9-135">Projektni postopki za primere z viri/brez zalog vključujejo naslednje zmožnosti:</span><span class="sxs-lookup"><span data-stu-id="fb5b9-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="fb5b9-136">Načrtovanje projektov z uporabo spletne aplikacije Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="fb5b9-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="fb5b9-137">Večrazsežnostno oblikovanje cen</span><span class="sxs-lookup"><span data-stu-id="fb5b9-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="fb5b9-138">Poenoteno upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="fb5b9-138">Unified Resource Management</span></span>
- <span data-ttu-id="fb5b9-139">Sledenje času</span><span class="sxs-lookup"><span data-stu-id="fb5b9-139">Time Tracking</span></span>
- <span data-ttu-id="fb5b9-140">Osnovne stroške</span><span class="sxs-lookup"><span data-stu-id="fb5b9-140">Basic Expense</span></span>
- <span data-ttu-id="fb5b9-141">Celotni stroški</span><span class="sxs-lookup"><span data-stu-id="fb5b9-141">Full Expense</span></span>
- <span data-ttu-id="fb5b9-142">Optično branje računov s tehnologijo OCR</span><span class="sxs-lookup"><span data-stu-id="fb5b9-142">Receipt OCR</span></span>
- <span data-ttu-id="fb5b9-143">Celoten postopek izdaje računa</span><span class="sxs-lookup"><span data-stu-id="fb5b9-143">Full Invoicing</span></span>
- <span data-ttu-id="fb5b9-144">Pripoznavanje prihodkov</span><span class="sxs-lookup"><span data-stu-id="fb5b9-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="fb5b9-145">Koraki uvajanja:</span><span class="sxs-lookup"><span data-stu-id="fb5b9-145">Deployment steps:</span></span>
<span data-ttu-id="fb5b9-146">Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="fb5b9-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="fb5b9-147">Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](resource-sign-up-preview-subscription.md) in [Omogočanje novega okolja](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fb5b9-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="fb5b9-148">Project Operations za primere uporabe z naročili na zalogi/v proizvodnji</span><span class="sxs-lookup"><span data-stu-id="fb5b9-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="fb5b9-149">Načrtovanje projekta z uporabo SČD</span><span class="sxs-lookup"><span data-stu-id="fb5b9-149">Project planning using WBS</span></span>
- <span data-ttu-id="fb5b9-150">Upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="fb5b9-150">Resource Management</span></span>
- <span data-ttu-id="fb5b9-151">Sledenje času</span><span class="sxs-lookup"><span data-stu-id="fb5b9-151">Time Tracking</span></span>
- <span data-ttu-id="fb5b9-152">Celotni stroški</span><span class="sxs-lookup"><span data-stu-id="fb5b9-152">Full Expense</span></span>
- <span data-ttu-id="fb5b9-153">Optično branje računov s tehnologijo OCR</span><span class="sxs-lookup"><span data-stu-id="fb5b9-153">Receipt OCR</span></span>
- <span data-ttu-id="fb5b9-154">Celoten postopek izdaje računa</span><span class="sxs-lookup"><span data-stu-id="fb5b9-154">Full Invoicing</span></span>
- <span data-ttu-id="fb5b9-155">Pripoznavanje prihodkov</span><span class="sxs-lookup"><span data-stu-id="fb5b9-155">Revenue Recognition</span></span>
- <span data-ttu-id="fb5b9-156">Proizvodna naročila</span><span class="sxs-lookup"><span data-stu-id="fb5b9-156">Production Orders</span></span>
- <span data-ttu-id="fb5b9-157">Podpora za materiale</span><span class="sxs-lookup"><span data-stu-id="fb5b9-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="fb5b9-158">Koraki uvajanja:</span><span class="sxs-lookup"><span data-stu-id="fb5b9-158">Deployment steps:</span></span>
<span data-ttu-id="fb5b9-159">Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="fb5b9-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="fb5b9-160">Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) in [Omogočanje novega okolja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="fb5b9-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



