---
title: Določanje vrste uvedbe
description: Ta tema vsebuje informacije za pomoč pri izbiri prave vrste uvajanja za projektne postopke v vašem podjetju.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401238"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="7270c-103">Določanje vrste uvedbe</span><span class="sxs-lookup"><span data-stu-id="7270c-103">Determine your deployment type</span></span>

<span data-ttu-id="7270c-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="7270c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7270c-105">Po nakupu licence določite najboljši model uvajanja v aplikaciji Dynamics 365 Project Operations z uporabo [vodenega postopka namestitve](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7270c-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="7270c-106">Ko dokončate vodeni postopek namestitve, boste preusmerjeni na pravi portal za upravljanje, da dokončate namestitev.</span><span class="sxs-lookup"><span data-stu-id="7270c-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="7270c-107">Za dokončanje namestitve glejte podrobnosti o uvajanju.</span><span class="sxs-lookup"><span data-stu-id="7270c-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="7270c-108">Obstoječe stranke rešitve Dynamics, ki uporabljajo aplikacijo Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7270c-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="7270c-109">Aplikacija Project Operations vključuje zmogljivosti, ki so bile na voljo v aplikaciji Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="7270c-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="7270c-110">Pot nadgradnje bo tem strankam izdana v 1. valu izdaj za leto 2021.</span><span class="sxs-lookup"><span data-stu-id="7270c-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="7270c-111">Obstoječe stranke aplikacije Dynamics 365 Finance, ki uporabljajo Projektno vodenje in računovodstvo</span><span class="sxs-lookup"><span data-stu-id="7270c-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="7270c-112">Obstoječe stranke rešitve Finance, ki uporabljajo funkcionalnost upravljanja projektov in računovodstva lahko nadaljujejo z uporabo rešitve, kakršna je.</span><span class="sxs-lookup"><span data-stu-id="7270c-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="7270c-113">Glejte razdelek [Aplikacija Project Operations za scenarije z naročili na zalogi/v proizvodnji](#pma).</span><span class="sxs-lookup"><span data-stu-id="7270c-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="7270c-114">Vrste uvajanja</span><span class="sxs-lookup"><span data-stu-id="7270c-114">Deployment types</span></span>
<span data-ttu-id="7270c-115">Aplikacija Project Operations podpira več možnosti uvajanja, ki ustrezajo vašim zahtevam.</span><span class="sxs-lookup"><span data-stu-id="7270c-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="7270c-116">Ne glede na to, ali ste nov ali obstoječ uporabnik rešitve Dynamics 365, lahko aplikacija Project Operations ustreza vašim zahtevam.</span><span class="sxs-lookup"><span data-stu-id="7270c-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="7270c-117">Naš [vprašalnik o uvajanju](https://aka.ms/provisionprojectoperations) vam bo pomagal določiti pravo vrsto uvajanja.</span><span class="sxs-lookup"><span data-stu-id="7270c-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="7270c-118">Rezultati vas bodo vodili do enega od naslednjih vrst uvajanja:</span><span class="sxs-lookup"><span data-stu-id="7270c-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="7270c-119">Poenostavljeno uvajanje – posel do izstavitve predračuna</span><span class="sxs-lookup"><span data-stu-id="7270c-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="7270c-120">Project Operations za primere uporabe z viri/brez zalog</span><span class="sxs-lookup"><span data-stu-id="7270c-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="7270c-121">Project Operations za primere uporabe z naročili na zalogi/v proizvodnji</span><span class="sxs-lookup"><span data-stu-id="7270c-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="7270c-122">Aplikacija Project Operations podpira primere naročil na zalogi/v proizvodnji in primere z viri/brez zalog v istem okolju prek konfiguracij na ravni pravne osebe.</span><span class="sxs-lookup"><span data-stu-id="7270c-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="7270c-123">Družba Contoso lahko na primer izkoristi zmogljivosti zalog/proizvodnih naročil v svojem ameriškem proizvodnem obratu (pravna oseba = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="7270c-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="7270c-124">Družba Contoso lahko na primer izkoristi zmogljivosti virov/brez zalog v njihovem obratu za servisiranje Contoso Robotics Arms v ZK (pravna oseba = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="7270c-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="7270c-125">Poenostavljeno uvajanje – posel do izstavitve predračuna</span><span class="sxs-lookup"><span data-stu-id="7270c-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="7270c-126">Poenostavljeno uvajanje vključuje naslednje zmožnosti:</span><span class="sxs-lookup"><span data-stu-id="7270c-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="7270c-127">Prodajni proces za projekte, ki razširja izkušnje aplikacije Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="7270c-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="7270c-128">Načrtovanje projektov z uporabo spletne aplikacije Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="7270c-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="7270c-129">Večrazsežnostno oblikovanje cen</span><span class="sxs-lookup"><span data-stu-id="7270c-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="7270c-130">Poenoteno upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="7270c-130">Unified resource management</span></span>
- <span data-ttu-id="7270c-131">Sledenje času</span><span class="sxs-lookup"><span data-stu-id="7270c-131">Time tracking</span></span>
- <span data-ttu-id="7270c-132">Osnovni stroški</span><span class="sxs-lookup"><span data-stu-id="7270c-132">Basic expense</span></span>
- <span data-ttu-id="7270c-133">Predračun in izstavljanje računov za stranke</span><span class="sxs-lookup"><span data-stu-id="7270c-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="7270c-134">Koraki uvajanja</span><span class="sxs-lookup"><span data-stu-id="7270c-134">Deployment steps</span></span>
<span data-ttu-id="7270c-135">Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7270c-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7270c-136">Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](lite-preview-subscription-sign-up.md) in [Omogočanje novega okolja](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="7270c-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="7270c-137">Project Operations za primere uporabe z viri/brez zalog</span><span class="sxs-lookup"><span data-stu-id="7270c-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="7270c-138">Projektni postopki za primere z viri/brez zalog vključujejo naslednje zmožnosti:</span><span class="sxs-lookup"><span data-stu-id="7270c-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="7270c-139">Prodajni proces za projekte, ki razširja aplikacijo Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="7270c-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="7270c-140">Načrtovanje projektov z uporabo spletne aplikacije Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="7270c-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="7270c-141">Večrazsežnostno oblikovanje cen</span><span class="sxs-lookup"><span data-stu-id="7270c-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="7270c-142">Poenoteno upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="7270c-142">Unified resource management</span></span>
- <span data-ttu-id="7270c-143">Sledenje času</span><span class="sxs-lookup"><span data-stu-id="7270c-143">Time tracking</span></span>
- <span data-ttu-id="7270c-144">Osnovni stroški</span><span class="sxs-lookup"><span data-stu-id="7270c-144">Basic expense</span></span>
- <span data-ttu-id="7270c-145">Celoten strošek</span><span class="sxs-lookup"><span data-stu-id="7270c-145">Full expense</span></span>
- <span data-ttu-id="7270c-146">Optično branje računov s tehnologijo OCR</span><span class="sxs-lookup"><span data-stu-id="7270c-146">Receipt OCR</span></span>
- <span data-ttu-id="7270c-147">Predračun in izstavljanje računov za stranke</span><span class="sxs-lookup"><span data-stu-id="7270c-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="7270c-148">Pripoznavanje prihodkov za projekte</span><span class="sxs-lookup"><span data-stu-id="7270c-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7270c-149">Koraki uvajanja</span><span class="sxs-lookup"><span data-stu-id="7270c-149">Deployment steps</span></span>
<span data-ttu-id="7270c-150">Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7270c-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7270c-151">Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](resource-sign-up-preview-subscription.md) in [Omogočanje novega okolja](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7270c-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="7270c-152">Project Operations za primere uporabe z naročili na zalogi/v proizvodnji</span><span class="sxs-lookup"><span data-stu-id="7270c-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="7270c-153">Načrtovanje projekta z uporabo SČD</span><span class="sxs-lookup"><span data-stu-id="7270c-153">Project planning using WBS</span></span>
- <span data-ttu-id="7270c-154">Upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="7270c-154">Resource Management</span></span>
- <span data-ttu-id="7270c-155">Sledenje času</span><span class="sxs-lookup"><span data-stu-id="7270c-155">Time Tracking</span></span>
- <span data-ttu-id="7270c-156">Celotni stroški</span><span class="sxs-lookup"><span data-stu-id="7270c-156">Full Expense</span></span>
- <span data-ttu-id="7270c-157">Optično branje računov s tehnologijo OCR</span><span class="sxs-lookup"><span data-stu-id="7270c-157">Receipt OCR</span></span>
- <span data-ttu-id="7270c-158">Celoten postopek izdaje računa</span><span class="sxs-lookup"><span data-stu-id="7270c-158">Full Invoicing</span></span>
- <span data-ttu-id="7270c-159">Pripoznavanje prihodkov</span><span class="sxs-lookup"><span data-stu-id="7270c-159">Revenue Recognition</span></span>
- <span data-ttu-id="7270c-160">Proizvodna naročila</span><span class="sxs-lookup"><span data-stu-id="7270c-160">Production Orders</span></span>
- <span data-ttu-id="7270c-161">Podpora za materiale</span><span class="sxs-lookup"><span data-stu-id="7270c-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="7270c-162">Koraki uvajanja</span><span class="sxs-lookup"><span data-stu-id="7270c-162">Deployment steps</span></span>
<span data-ttu-id="7270c-163">Določite najboljši model uvajanja v aplikaciji Project Operations z [vprašalnikom o uvajanju](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="7270c-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="7270c-164">Za to uvajanje glejte razdelka [Prijava za naročnino na predogledno različico](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) in [Omogočanje novega okolja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7270c-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

