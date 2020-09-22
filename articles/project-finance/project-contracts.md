---
title: Projektne pogodbe
description: Ta tema vsebuje primere projektnih pogodb, ki jih lahko ustvarite za različne vrste projektov in vire financiranja, in načine za upravljanje pogodb in izdajanje računov strankam projektov.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755826"
---
# <a name="project-contracts"></a><span data-ttu-id="df5e8-103">Projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="df5e8-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df5e8-104">Ta članek vsebuje primere projektnih pogodb, ki jih lahko ustvarite za različne vrste projektov in vire financiranja, in načine za upravljanje pogodb in izdajanje računov strankam projektov.</span><span class="sxs-lookup"><span data-stu-id="df5e8-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="df5e8-105">Vrsta projekta, ki ga ustvarite za projektno pogodbo, določa metodo za izdajo računov projektnim strankam.</span><span class="sxs-lookup"><span data-stu-id="df5e8-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="df5e8-106">Projektno pogodbo in z njo povezan projekt lahko spremenite, vendar ne morete spremeniti vrste projekta.</span><span class="sxs-lookup"><span data-stu-id="df5e8-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="df5e8-107">Z uporabo projektne pogodbe lahko izdate račun za en ali več projektov hkrati.</span><span class="sxs-lookup"><span data-stu-id="df5e8-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="df5e8-108">Projektna pogodba pomaga tudi pri doslednem izdajanju računov za vsak podprojekt v projektni strukturi.</span><span class="sxs-lookup"><span data-stu-id="df5e8-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="df5e8-109">Vsak projekt, za katerega bo izdan račun, mora biti povezan s projektno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="df5e8-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="df5e8-110">Nastavitve za projektno pogodbo veljajo za vse projekte in podprojekte, ki so povezani s to projektno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="df5e8-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="df5e8-111">Projektna pogodba lahko določa enega ali več virov financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="df5e8-112">Zato lahko obračun razdelite na več vlagateljev in nastavite omejitve financiranja, tako da viri financiranja ne bodo zaračunani nad določenim zneskom, in nastavite pravila financiranja za zaračunavanje izdatkov.</span><span class="sxs-lookup"><span data-stu-id="df5e8-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="df5e8-113">Financiranje za projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="df5e8-113">Funding for project contracts</span></span>
<span data-ttu-id="df5e8-114">Nekatere projektne pogodbe določajo, da je več strank odgovornih za financiranje stroškov projekta.</span><span class="sxs-lookup"><span data-stu-id="df5e8-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="df5e8-115">Tukaj je nekaj primerov:</span><span class="sxs-lookup"><span data-stu-id="df5e8-115">Here are some examples:</span></span>

-   <span data-ttu-id="df5e8-116">Velika stranka z več oddelki zahteva, da se financiranje projekta razdeli po oddelkih.</span><span class="sxs-lookup"><span data-stu-id="df5e8-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="df5e8-117">Vaše podjetje si stroške velikega projekta deli z zunanjo organizacijo.</span><span class="sxs-lookup"><span data-stu-id="df5e8-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="df5e8-118">Projekt za cesto sofinancirata dve občini.</span><span class="sxs-lookup"><span data-stu-id="df5e8-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="df5e8-119">Projekt za most financira javna uprava z nepovratnimi sredstvi in zasebna družba.</span><span class="sxs-lookup"><span data-stu-id="df5e8-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="df5e8-120">V rešitvi Dynamics 365 Finance lahko račun za eno transakcijo ali celoten projekt razdelite na več strank, nepovratnih sredstev ali organizacij.</span><span class="sxs-lookup"><span data-stu-id="df5e8-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="df5e8-121">V projektih z več vlagatelji se vse strani, ki prispevajo k financiranju projekta z naprednim financiranjem, imenujejo viri financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="df5e8-122">Ko so stranka, organizacija ali nepovratna sredstva opredeljena kot vir financiranja, se lahko dodelijo enemu ali več pravilom financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="df5e8-123">Pravila financiranja vsebujejo merila, ki določajo, kako se stroški razdelijo različnim virom financiranja za projekt.</span><span class="sxs-lookup"><span data-stu-id="df5e8-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="df5e8-124">Ker izdelkov na zalogi, na primer tistih, ki se pojavijo v zahtevah za nakup in naročilnicah, ni mogoče razdeliti, zneska stroškov v času distribucije ni mogoče razdeliti med več virov financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="df5e8-125">Zato vrednost vira financiranja ostane 0 (nič), dokler se ne vknjiži težava z zalogo.</span><span class="sxs-lookup"><span data-stu-id="df5e8-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="df5e8-126">Ko je težava z zalogo vknjižena, se znesek stroškov porazdeli v skladu s pravili o razdelitvi računov za projekt.</span><span class="sxs-lookup"><span data-stu-id="df5e8-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="df5e8-127">Tu je nekaj korakov, s katerimi boste lažje razdelili stroške med več virov financiranja:</span><span class="sxs-lookup"><span data-stu-id="df5e8-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="df5e8-128">Navedite, da vse transakcije, ki so vnesene za projekt, uporabljajo isto prodajno valuto kot projektna pogodba.</span><span class="sxs-lookup"><span data-stu-id="df5e8-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="df5e8-129">Določite omejitve financiranja, tako da se viru financiranja za projekt ne zaračuna več kot določen znesek.</span><span class="sxs-lookup"><span data-stu-id="df5e8-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="df5e8-130">Konfigurirajte pravila financiranja in omejitve financiranja za vsakega delavca, izdelek, kategorijo, skupino kategorij in vrsto transakcije (ali za vse vrste transakcij).</span><span class="sxs-lookup"><span data-stu-id="df5e8-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="df5e8-131">Izberite izbirni začetni in končni datum, da določite obdobje veljavnosti posameznega pravila financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="df5e8-132">Navedite delež, ki pripada posameznemu viru financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="df5e8-133">Navedite, kateri vir financiranja je odgovoren za zaokroževanje razlik, ki so posledica izračunov pri dodeljevanju sredstev.</span><span class="sxs-lookup"><span data-stu-id="df5e8-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="df5e8-134">Nastavite pravila, ki določajo, kako se stroški projekta zaračunavajo zunanjim strankam in internim organizacijam.</span><span class="sxs-lookup"><span data-stu-id="df5e8-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="df5e8-135">Transakcije beležite na začasnem računu financiranja, dokler ni mogoče pridobiti dodatnega financiranja ali dokler se ne odločite za interno kritje stroškov.</span><span class="sxs-lookup"><span data-stu-id="df5e8-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="df5e8-136">Če želite določiti, katero davčno skupino bi povezali s transakcijo, poiščite dodelitev davčne skupine v projektu.</span><span class="sxs-lookup"><span data-stu-id="df5e8-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="df5e8-137">Če na ravni projekta ni bila ustvarjena nobena davčna skupina, je treba poiskati projektno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="df5e8-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="df5e8-138">Primer: več virov financiranja (enostavno)</span><span class="sxs-lookup"><span data-stu-id="df5e8-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="df5e8-139">Spodnja tabela vsebuje scenarije za upravljanje dodeljevanja sredstev med več virov financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="df5e8-140">Ti scenariji temeljijo na naslednjih predpostavkah:</span><span class="sxs-lookup"><span data-stu-id="df5e8-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="df5e8-141">Prednostne nastavitve se upoštevajo pri dodeljevanju sredstev pred drugimi merili, ki določajo pravila financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="df5e8-142">Za določitev obdobja d, za katerega velja pravilo financiranja, ni določeno nobeno časovno obdobje.</span><span class="sxs-lookup"><span data-stu-id="df5e8-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df5e8-143"><strong>Scenarij</strong></span><span class="sxs-lookup"><span data-stu-id="df5e8-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="df5e8-144"><strong>Vir financiranja</strong></span><span class="sxs-lookup"><span data-stu-id="df5e8-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="df5e8-145"><strong>Delež dodelitve</strong></span><span class="sxs-lookup"><span data-stu-id="df5e8-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="df5e8-146"><strong>Prednost pri dodeljevanju</strong></span><span class="sxs-lookup"><span data-stu-id="df5e8-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5e8-147">Stroške dodelite enemu viru financiranja, dokler se njegova sredstva ne izčrpajo, nato drugemu viru financiranja, dokler se sredstva ne izčrpajo, preostale stroške pa tretjemu viru financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="df5e8-148">Vir　financiranja　1</span><span class="sxs-lookup"><span data-stu-id="df5e8-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="df5e8-149">Vir　financiranja　2</span><span class="sxs-lookup"><span data-stu-id="df5e8-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="df5e8-150">Vir　financiranja　3</span><span class="sxs-lookup"><span data-stu-id="df5e8-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="df5e8-151">100 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-151">100%</span></span></li>
<li><span data-ttu-id="df5e8-152">100 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-152">100%</span></span></li>
<li><span data-ttu-id="df5e8-153">100 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="df5e8-154">1</span><span class="sxs-lookup"><span data-stu-id="df5e8-154">1</span></span></li>
<li><span data-ttu-id="df5e8-155">2</span><span class="sxs-lookup"><span data-stu-id="df5e8-155">2</span></span></li>
<li><span data-ttu-id="df5e8-156">3</span><span class="sxs-lookup"><span data-stu-id="df5e8-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5e8-157">75 odstotkov stroškov želite dodeliti enemu viru financiranja, 25 odstotkov pa drugemu viru financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="df5e8-158">Ko je eden od teh virov financiranja izčrpan, plačajte preostale stroške iz tretjega vira financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="df5e8-159">Vir　financiranja　1</span><span class="sxs-lookup"><span data-stu-id="df5e8-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="df5e8-160">Vir　financiranja　2</span><span class="sxs-lookup"><span data-stu-id="df5e8-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="df5e8-161">Vir　financiranja　3</span><span class="sxs-lookup"><span data-stu-id="df5e8-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="df5e8-162">75 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-162">75%</span></span></li>
<li><span data-ttu-id="df5e8-163">25 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-163">25%</span></span></li>
<li><span data-ttu-id="df5e8-164">100 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="df5e8-165">1</span><span class="sxs-lookup"><span data-stu-id="df5e8-165">1</span></span></li>
<li><span data-ttu-id="df5e8-166">1</span><span class="sxs-lookup"><span data-stu-id="df5e8-166">1</span></span></li>
<li><span data-ttu-id="df5e8-167">2</span><span class="sxs-lookup"><span data-stu-id="df5e8-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5e8-168">75 odstotkov stroškov želite dodeliti enemu viru financiranja, 25 odstotkov pa drugemu viru financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="df5e8-169">Ko je eden od teh virov financiranja izčrpan, razdelite preostale stroške med tretji in četrti vir financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="df5e8-170">Vir　financiranja　1</span><span class="sxs-lookup"><span data-stu-id="df5e8-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="df5e8-171">Vir　financiranja　2</span><span class="sxs-lookup"><span data-stu-id="df5e8-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="df5e8-172">Vir　financiranja　3</span><span class="sxs-lookup"><span data-stu-id="df5e8-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="df5e8-173">Vir　financiranja　4</span><span class="sxs-lookup"><span data-stu-id="df5e8-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="df5e8-174">75 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-174">75%</span></span></li>
<li><span data-ttu-id="df5e8-175">25 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-175">25%</span></span></li>
<li><span data-ttu-id="df5e8-176">50 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-176">50%</span></span></li>
<li><span data-ttu-id="df5e8-177">50 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="df5e8-178">1</span><span class="sxs-lookup"><span data-stu-id="df5e8-178">1</span></span></li>
<li><span data-ttu-id="df5e8-179">1</span><span class="sxs-lookup"><span data-stu-id="df5e8-179">1</span></span></li>
<li><span data-ttu-id="df5e8-180">2</span><span class="sxs-lookup"><span data-stu-id="df5e8-180">2</span></span></li>
<li><span data-ttu-id="df5e8-181">2</span><span class="sxs-lookup"><span data-stu-id="df5e8-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5e8-182">Prvih 25 odstotkov stroškov želite dodeliti enemu viru financiranja, preostanek pa drugemu viru financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="df5e8-183">Vir　financiranja　1</span><span class="sxs-lookup"><span data-stu-id="df5e8-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="df5e8-184">Vir　financiranja　2</span><span class="sxs-lookup"><span data-stu-id="df5e8-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="df5e8-185">25 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-185">25%</span></span></li>
<li><span data-ttu-id="df5e8-186">100 %</span><span class="sxs-lookup"><span data-stu-id="df5e8-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="df5e8-187">1</span><span class="sxs-lookup"><span data-stu-id="df5e8-187">1</span></span></li>
<li><span data-ttu-id="df5e8-188">2</span><span class="sxs-lookup"><span data-stu-id="df5e8-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="df5e8-189">Primer: več virov financiranja (napredno)</span><span class="sxs-lookup"><span data-stu-id="df5e8-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="df5e8-190">Na voljo imate tri vire financiranja, ki jih želite uporabiti v naslednjem vrstnem redu:</span><span class="sxs-lookup"><span data-stu-id="df5e8-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="df5e8-191">Vir financiranja 2 in 3 uporabljajte enako, dokler se vir 2 ne izčrpa.</span><span class="sxs-lookup"><span data-stu-id="df5e8-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="df5e8-192">Še naprej uporabljajte vir financiranja 3, dokler ga ne izčrpate.</span><span class="sxs-lookup"><span data-stu-id="df5e8-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="df5e8-193">Ko izčrpate vir financiranja 3, uporabite vir financiranja 1.</span><span class="sxs-lookup"><span data-stu-id="df5e8-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="df5e8-194">Za dosego tega cilja morate najprej storiti naslednje:</span><span class="sxs-lookup"><span data-stu-id="df5e8-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="df5e8-195">Določite omejitve financiranja za vir financiranja 2 in 3 v skladu z njihovima zneskoma.</span><span class="sxs-lookup"><span data-stu-id="df5e8-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="df5e8-196">Ustvarite naslednja pravila financiranja:</span><span class="sxs-lookup"><span data-stu-id="df5e8-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="df5e8-197">1. pravilo (prednost 1): 50 odstotkov transakcij dodelite viru financiranja 2, 50 odstotkov pa viru financiranja 3.</span><span class="sxs-lookup"><span data-stu-id="df5e8-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="df5e8-198">2. pravilo (prednost 2): 100 odstotkov transakcij dodelite viru financiranja 3.</span><span class="sxs-lookup"><span data-stu-id="df5e8-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="df5e8-199">3. pravilo (prednost 3): 100 odstotkov transakcij dodelite viru financiranja 1.</span><span class="sxs-lookup"><span data-stu-id="df5e8-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="df5e8-200">Ta nastavitev deluje, ker se transakcije preverjajo glede na pravila in omejitve, da se ugotovi, ali katera od njih velja za transakcijo.</span><span class="sxs-lookup"><span data-stu-id="df5e8-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="df5e8-201">Če za transakcijo ne veljajo nobena posebna pravila ali omejitve, velja pravilo za vse transakcije.</span><span class="sxs-lookup"><span data-stu-id="df5e8-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="df5e8-202">Pravilo za vse transakcije se ujema z vsemi transakcijami.</span><span class="sxs-lookup"><span data-stu-id="df5e8-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="df5e8-203">Če najdemo pravilo, ki se ujema s transakcijo, je najprej uporabljen delež, ki je bil dodeljen v tem pravilu, vendar šele potem, ko se preverijo ujemanja glede na nastavljene omejitve.</span><span class="sxs-lookup"><span data-stu-id="df5e8-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="df5e8-204">Če je bila omejitev dosežena in so sredstva vira financiranja izčrpana, se pravilo financiranja, povezano z omejitvijo financiranja, ne upošteva in program preveri naslednje veljavno pravilo.</span><span class="sxs-lookup"><span data-stu-id="df5e8-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="df5e8-205">V nekaterih primerih je mogoče pravilu dodeliti le del transakcije.</span><span class="sxs-lookup"><span data-stu-id="df5e8-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="df5e8-206">To se lahko zgodi, ker je pri dodelitvi transakcije dosežena omejitev.</span><span class="sxs-lookup"><span data-stu-id="df5e8-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="df5e8-207">V tem primeru se v skladu s tem pravilom dodeli le določen znesek, na primer 50 odstotkov za vsak vir financiranja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="df5e8-208">To velja za 1. pravilo, ki je opisano v prejšnjih odstavkih tega razdelka.</span><span class="sxs-lookup"><span data-stu-id="df5e8-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="df5e8-209">Preostanek se dodeli v skladu z naslednjim pravilom v zaporedju.</span><span class="sxs-lookup"><span data-stu-id="df5e8-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="df5e8-210">Spodnja tabela vsebuje podroben pregled tega scenarija.</span><span class="sxs-lookup"><span data-stu-id="df5e8-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df5e8-211"><strong>Fokus</strong></span><span class="sxs-lookup"><span data-stu-id="df5e8-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="df5e8-212"><strong>Podrobnosti</strong></span><span class="sxs-lookup"><span data-stu-id="df5e8-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5e8-213">Pravila financiranja</span><span class="sxs-lookup"><span data-stu-id="df5e8-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="df5e8-214">1. pravilo (prednost 1): Vse transakcije.</span><span class="sxs-lookup"><span data-stu-id="df5e8-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="df5e8-215">50 % dodelite viru financiranja 2, 50 % pa viru financiranja 3.</span><span class="sxs-lookup"><span data-stu-id="df5e8-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="df5e8-216">2. pravilo (prednost 2): Vse transakcije.</span><span class="sxs-lookup"><span data-stu-id="df5e8-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="df5e8-217">Viru financiranja 3 dodelite 100 %.</span><span class="sxs-lookup"><span data-stu-id="df5e8-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="df5e8-218">3. pravilo (prednost 2): Vse transakcije.</span><span class="sxs-lookup"><span data-stu-id="df5e8-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="df5e8-219">Viru financiranja 1 dodelite 100 %.</span><span class="sxs-lookup"><span data-stu-id="df5e8-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5e8-220">Omejitve financiranja</span><span class="sxs-lookup"><span data-stu-id="df5e8-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="df5e8-221">Omejitev vira financiranja 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="df5e8-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="df5e8-222">Omejitev vira financiranja 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="df5e8-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="df5e8-223">Omejitev vira financiranja 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="df5e8-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5e8-224">Transakcija 1</span><span class="sxs-lookup"><span data-stu-id="df5e8-224">Transaction 1</span></span></td>
<td><span data-ttu-id="df5e8-225"><strong>Znesek transakcije:</strong> 100,00<strong>Financiranje:</strong> Transakcija se plača samo v skladu s 1. pravilom, ker se transakcija plača v celoti po uporabi 1. pravila.</span><span class="sxs-lookup"><span data-stu-id="df5e8-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="df5e8-226">Transakcija je financirana z viroma financiranja 2 in 3 v enakovrednih deležih.</span><span class="sxs-lookup"><span data-stu-id="df5e8-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="df5e8-227">Vir financiranja 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="df5e8-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="df5e8-228">Vir financiranja 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="df5e8-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="df5e8-229">Transakcija 2</span><span class="sxs-lookup"><span data-stu-id="df5e8-229">Transaction 2</span></span></td>
<td><span data-ttu-id="df5e8-230"><strong>Znesek transakcije:</strong> 5.000,00<strong>Financiranje:</strong> Transakcija se plača v skladu z vsemi tremi pravili.</span><span class="sxs-lookup"><span data-stu-id="df5e8-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="df5e8-231"><strong>1. pravilo</strong>
</span><span class="sxs-lookup"><span data-stu-id="df5e8-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="df5e8-232">Vir financiranja 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="df5e8-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="df5e8-233">Vir financiranja 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="df5e8-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="df5e8-234">
<strong>2. pravilo</strong>
</span><span class="sxs-lookup"><span data-stu-id="df5e8-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="df5e8-235">Vir financiranja 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="df5e8-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="df5e8-236">
<strong>3. pravilo</strong>
</span><span class="sxs-lookup"><span data-stu-id="df5e8-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="df5e8-237">Vir financiranja 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="df5e8-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df5e8-238">Skupna sredstva, ki se razdelijo za vsak vir financiranja</span><span class="sxs-lookup"><span data-stu-id="df5e8-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="df5e8-239">Vir financiranja 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="df5e8-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="df5e8-240">Vir financiranja 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="df5e8-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="df5e8-241">Vir financiranja 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="df5e8-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="df5e8-242">Pravila za obračunavanje</span><span class="sxs-lookup"><span data-stu-id="df5e8-242">Billing rules</span></span>
<span data-ttu-id="df5e8-243">Ko se s stranko dogovarjate za projektno pogodbo, določite, kako in kdaj lahko stranki zaračunate za delo na projektu.</span><span class="sxs-lookup"><span data-stu-id="df5e8-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="df5e8-244">Ko nastavite projektno pogodbo in projekt, lahko nastavite tudi obračunska pravila za projekt.</span><span class="sxs-lookup"><span data-stu-id="df5e8-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="df5e8-245">Obračunska pravila temeljijo na projektnih pogojih, ki so določeni v projektni pogodbi.</span><span class="sxs-lookup"><span data-stu-id="df5e8-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="df5e8-246">Obračunska pravila, ki jih lahko ustvarite, so odvisna od pogojev projektne pogodbe in vrste projekta, kot sta »Čas in material« ali »Fiksna cena«, ki ju povežete z obračunskim pravilom.</span><span class="sxs-lookup"><span data-stu-id="df5e8-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="df5e8-247">Za projektno pogodbo lahko ustvarite več obračunskih pravil.</span><span class="sxs-lookup"><span data-stu-id="df5e8-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="df5e8-248">Obračunsko pravilo lahko dodelite tudi več projektom, ki so povezani z isto projektno pogodbo in imajo podobne pogoje za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="df5e8-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="df5e8-249">Nastavite lahko naslednje vrste obračunskih pravil:</span><span class="sxs-lookup"><span data-stu-id="df5e8-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="df5e8-250">**Dostavna enota** – stranki izdajte račun, ko dokončate dostavno enoto.</span><span class="sxs-lookup"><span data-stu-id="df5e8-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="df5e8-251">Dostavne enote določite v pogodbi.</span><span class="sxs-lookup"><span data-stu-id="df5e8-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="df5e8-252">**Napredek** – stranki izdajte račun, ko dokončate določen delež projekta.</span><span class="sxs-lookup"><span data-stu-id="df5e8-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="df5e8-253">Obračunsko pravilo lahko nastavite tako, da bo samodejno izračunalo delež opravljenega dela, lahko pa ročno izračunate delež opravljenega dela in znesek, ki ga boste zaračunali stranki.</span><span class="sxs-lookup"><span data-stu-id="df5e8-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="df5e8-254">**Mejnik** – stranki izdajte račun za celoten znesek projektnega mejnika, ko je ta dosežen.</span><span class="sxs-lookup"><span data-stu-id="df5e8-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="df5e8-255">**Provizija** – stranki izdajte račun za vaše storitve plus provizijo za upravljanje, ki je običajno v obliki odstotka stroškov storitev.</span><span class="sxs-lookup"><span data-stu-id="df5e8-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="df5e8-256">**Čas in material** – stranki izdajte račun za vrednost časa in materialov, ki se uporabljajo pri projektu.</span><span class="sxs-lookup"><span data-stu-id="df5e8-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="df5e8-257">Za vse vrste obračunskih pravil lahko določite delež zadržanega plačila, ki se odšteje od računov za stranke, dokler projekt ne doseže dogovorjene stopnje.</span><span class="sxs-lookup"><span data-stu-id="df5e8-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="df5e8-258">Delež zadržanega plačila je določen v projektni pogodbi.</span><span class="sxs-lookup"><span data-stu-id="df5e8-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="df5e8-259">Znesek se izračuna na podlagi in odšteje od skupne vrednosti vrstic na računu za stranko.</span><span class="sxs-lookup"><span data-stu-id="df5e8-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="df5e8-260">Za obračunska pravila **Čas in material** in **Napredek** lahko dodelite plačljive kategorije.</span><span class="sxs-lookup"><span data-stu-id="df5e8-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="df5e8-261">Plačljive kategorije označujejo transakcije, ki naj bi bile vključene v račune za stranke.</span><span class="sxs-lookup"><span data-stu-id="df5e8-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="df5e8-262">Ko ste pripravljeni stranki izdati račun, se znesek, ki ga boste zaračunali za projekt, izračuna na podlagi obračunskih pravil, in ustvari predlog za račun projekta.</span><span class="sxs-lookup"><span data-stu-id="df5e8-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="df5e8-263">Naslednji razdelki vsebujejo primere, ki prikazujejo, kako nastaviti in upravljati obračunska pravila za projekt.</span><span class="sxs-lookup"><span data-stu-id="df5e8-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="df5e8-264">Primer: ustvarite obračunsko pravilo na podlagi števila izvedenih enot</span><span class="sxs-lookup"><span data-stu-id="df5e8-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="df5e8-265">Vaša organizacija sklene pogodbo, po kateri bo strankinim zaposlenim zagotovila pet usposabljanj po ceni 10.000 na usposabljanje.</span><span class="sxs-lookup"><span data-stu-id="df5e8-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="df5e8-266">Stranki izdate račun po vsakem usposabljanju.</span><span class="sxs-lookup"><span data-stu-id="df5e8-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="df5e8-267">Pri nastavljanju obračunskih pravil za pogodbo uporabite naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="df5e8-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="df5e8-268">Dostavna enota označuje eno usposabljanje.</span><span class="sxs-lookup"><span data-stu-id="df5e8-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="df5e8-269">Cena enote je 10.000 na usposabljanje.</span><span class="sxs-lookup"><span data-stu-id="df5e8-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="df5e8-270">Skupno število enot je pet usposabljanj.</span><span class="sxs-lookup"><span data-stu-id="df5e8-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="df5e8-271">Ko zaključite eno usposabljanje, ustvarite račun za 10.000 za prvo enoto, ki je bila izvedena, in pošljite račun stranki.</span><span class="sxs-lookup"><span data-stu-id="df5e8-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="df5e8-272">Primer: ustvarite obračunsko pravilo na podlagi določenega deleža dokončanosti projekta (ročni izračun)</span><span class="sxs-lookup"><span data-stu-id="df5e8-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="df5e8-273">Vaša organizacija, svetovalno podjetje za programsko opremo, s stranko sklene dogovor o razvoju dela izdelka, ki ga stranka razvija.</span><span class="sxs-lookup"><span data-stu-id="df5e8-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="df5e8-274">Vaša organizacija se strinja, da bo programsko kodo dostavila v šestih mesecih.</span><span class="sxs-lookup"><span data-stu-id="df5e8-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="df5e8-275">Stranka se strinja, da bo vaši organizaciji za delo plačala skupno 100.000.</span><span class="sxs-lookup"><span data-stu-id="df5e8-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="df5e8-276">Obračunsko pravilo ustvarite tako, da stranki izdate račun na podlagi deleža dokončanega dela na projektu, kot je navedeno v pogodbi.</span><span class="sxs-lookup"><span data-stu-id="df5e8-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="df5e8-277">Konec prvega meseca se sestanite s stranko, da določite delež dokončanega dela.</span><span class="sxs-lookup"><span data-stu-id="df5e8-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="df5e8-278">Ko s stranko pregledate projekt, ugotovite, da je projekt dokončan do 15 odstotkov.</span><span class="sxs-lookup"><span data-stu-id="df5e8-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="df5e8-279">Ustvarite račun za 15.000 (15 odstotkov od 100.000) in ga pošljite stranki.</span><span class="sxs-lookup"><span data-stu-id="df5e8-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="df5e8-280">Primer: ustvarite obračunsko pravilo na podlagi določenega deleža dokončanosti projekta (samodejni izračun)</span><span class="sxs-lookup"><span data-stu-id="df5e8-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="df5e8-281">Vaša organizacija, podjetje za razvoj programske opreme, se strinja, da bo za stranko razvila paket za obračun plač za 30.000.</span><span class="sxs-lookup"><span data-stu-id="df5e8-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="df5e8-282">Stranka se strinja, da bo vaši organizaciji za delo plačala za delež dokončanega dela.</span><span class="sxs-lookup"><span data-stu-id="df5e8-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="df5e8-283">Po vaši oceni znašajo stroški projekta 20.000.</span><span class="sxs-lookup"><span data-stu-id="df5e8-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="df5e8-284">Projektna pogodba določa kategorije del, ki jih uporabljate v postopku zaračunavanja.</span><span class="sxs-lookup"><span data-stu-id="df5e8-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="df5e8-285">Nastavite obračunska pravila, ki samodejno izračunajo zneske računov za delež opravljenega dela za posamezno kategorijo.</span><span class="sxs-lookup"><span data-stu-id="df5e8-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="df5e8-286">Za vsako kategorijo nastavite proračun:</span><span class="sxs-lookup"><span data-stu-id="df5e8-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="df5e8-287">**Razvoj** – stroški v višini 15.000 in prihodki v višini 20.000</span><span class="sxs-lookup"><span data-stu-id="df5e8-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="df5e8-288">**Namestitev** – stroški v višini 5.000 in prihodki v višini 10.000</span><span class="sxs-lookup"><span data-stu-id="df5e8-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="df5e8-289">Ko prvič ustvarite račun za stranko, se znesek računa samodejno izračuna na podlagi naslednjih informacij:</span><span class="sxs-lookup"><span data-stu-id="df5e8-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="df5e8-290">Po enem mesecu delavec na projektu predloži časovni list za projekt.</span><span class="sxs-lookup"><span data-stu-id="df5e8-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="df5e8-291">Strošek delovnega časa delavca je 5.000 za razvoj in 1.000 za namestitev.</span><span class="sxs-lookup"><span data-stu-id="df5e8-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="df5e8-292">Razvojna dela so končana v 33 odstotkih (5.000 dejanskih stroškov/15.000 proračunskih stroškov), namestitvena dela pa v 20 odstotkih (1.000 dejanskih stroškov/5.000 proračunskih stroškov).</span><span class="sxs-lookup"><span data-stu-id="df5e8-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="df5e8-293">Znesek računa v višini 8.667 se samodejno izračuna (33 odstotkov od 20.000 + 20 odstotkov od 10.000).</span><span class="sxs-lookup"><span data-stu-id="df5e8-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="df5e8-294">Ustvarite račun za 8.667 in ga pošljite stranki.</span><span class="sxs-lookup"><span data-stu-id="df5e8-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="df5e8-295">Primer: Ustvarite obračunsko pravilo na podlagi dogovorjenih mejnikov</span><span class="sxs-lookup"><span data-stu-id="df5e8-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="df5e8-296">Vaša organizacija, svetovalno podjetje za upravljanje, se zavezuje izvesti tržno raziskavo za potrošniški izdelek, ki ga stranka namerava prodati.</span><span class="sxs-lookup"><span data-stu-id="df5e8-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="df5e8-297">Stranka se strinja, da bo vaše storitve uporabljala tri mesece z začetkom marca in da plača vaši organizaciji 50.000.</span><span class="sxs-lookup"><span data-stu-id="df5e8-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="df5e8-298">Projekt ima tri mejnike:</span><span class="sxs-lookup"><span data-stu-id="df5e8-298">The project has three milestones:</span></span>

-   <span data-ttu-id="df5e8-299">1. mejnik: zbiranje podatkov o potrošnikih – 31. marec</span><span class="sxs-lookup"><span data-stu-id="df5e8-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="df5e8-300">2. mejnik: analiza podatkov o potrošnikih – 30. april</span><span class="sxs-lookup"><span data-stu-id="df5e8-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="df5e8-301">3. mejnik: predstavitev predloga za preživetje izdelka – 31. maj</span><span class="sxs-lookup"><span data-stu-id="df5e8-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="df5e8-302">Stranka se strinja, da bo vaši organizaciji plačala 10.000 za prvi mejnik, 20.000 za drugi mejnik in 20.000 za tretji mejnik.</span><span class="sxs-lookup"><span data-stu-id="df5e8-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="df5e8-303">Ko določite projektno pogodbo, se strinjate, da boste stranki izdali račun na podlagi opravljenega mejnika.</span><span class="sxs-lookup"><span data-stu-id="df5e8-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="df5e8-304">Nastavitev obračunskega pravila vključuje naslednje korake:</span><span class="sxs-lookup"><span data-stu-id="df5e8-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="df5e8-305">Določitev mejnikov projekta.</span><span class="sxs-lookup"><span data-stu-id="df5e8-305">Define the project milestones.</span></span>
-   <span data-ttu-id="df5e8-306">Določitev zneska, ki bo stranki zaračunan ob izpolnitvi posameznega mejnika.</span><span class="sxs-lookup"><span data-stu-id="df5e8-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="df5e8-307">Ko dosežete prvi mejnik 31. marca, ga označite kot izpolnjenega, nato pa ustvarite račun za 10.000 in ga pošljite stranki.</span><span class="sxs-lookup"><span data-stu-id="df5e8-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="df5e8-308">Računa za mejnik ne morete ustvariti, dokler mejnika ne označite kot zaključenega.</span><span class="sxs-lookup"><span data-stu-id="df5e8-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="df5e8-309">Primer: Ustvarite pravilo za obračunavanje na podlagi storitev in provizije za upravljanje</span><span class="sxs-lookup"><span data-stu-id="df5e8-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="df5e8-310">Vaša organizacija, svetovalno podjetje za upravljanje, se zavezuje, da bo izvedla tržne raziskave, da bi ocenila sposobnost preživetja izdelka, ki ga razvija stranka – maloprodajno podjetje.</span><span class="sxs-lookup"><span data-stu-id="df5e8-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="df5e8-311">Pogoji sporazuma določajo, da boste zagotovili storitve svojih treh vodilnih svetovalcev, ki bodo raziskave izvajali v časovnem in materialnem sorazmerju.</span><span class="sxs-lookup"><span data-stu-id="df5e8-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="df5e8-312">Stranka se strinja, da bo plačala 100 na uro plus 10-odstotno provizijo za upravljanje za svetovalne ure, ki se zaračunajo projektu.</span><span class="sxs-lookup"><span data-stu-id="df5e8-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="df5e8-313">Ko določate projektno pogodbo, ustvarite obračunsko pravilo, s katerim se svetovalnim uram, ki se zaračunajo projektu, doda 10-odstotno provizijo za upravljanje.</span><span class="sxs-lookup"><span data-stu-id="df5e8-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="df5e8-314">Ko ustvarite račun za stranko, ji zaračunajte 10-odstotno provizijo za upravljanje plus stroške svetovalnih ur.</span><span class="sxs-lookup"><span data-stu-id="df5e8-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="df5e8-315">Primer: če so omenjeni trije svetovalci na projektu delali skupno 200 ur, je treba na podlagi spodnjega izračuna ustvariti račun za 22.000:</span><span class="sxs-lookup"><span data-stu-id="df5e8-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="df5e8-316">200 ur po 100 na uro = 20.000</span><span class="sxs-lookup"><span data-stu-id="df5e8-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="df5e8-317">10-odstotna provizija za upravljanje = 2.000</span><span class="sxs-lookup"><span data-stu-id="df5e8-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="df5e8-318">Skupni znesek računa = 22.000</span><span class="sxs-lookup"><span data-stu-id="df5e8-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="df5e8-319">Če so provizije za stranko obdavčene in v projektni pogodbi izberete skupino prometnega davka, se skupina prometnega davka samodejno vnese v obračunsko pravilo za provizije.</span><span class="sxs-lookup"><span data-stu-id="df5e8-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="df5e8-320">Primer: Ustvarite obračunsko pravilo za vrednost časa in materialov</span><span class="sxs-lookup"><span data-stu-id="df5e8-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="df5e8-321">Vaša organizacija, svetovalno podjetje za programsko opremo, se zavezuje, da bo v naslednjih šestih mesecih zagotovila pet tehničnih svetovalcev, ki bodo delali na projektu za razvoj programske opreme za stranko.</span><span class="sxs-lookup"><span data-stu-id="df5e8-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="df5e8-322">Stranka se strinja, da bo plačala 150 za vsako svetovalno uro plus stroške pisarniškega materiala.</span><span class="sxs-lookup"><span data-stu-id="df5e8-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="df5e8-323">Vaša organizacija stranki konec vsakega meseca pošlje račun.</span><span class="sxs-lookup"><span data-stu-id="df5e8-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="df5e8-324">Ob zasnovi projektne pogodbe se zavežete, da boste kupcu vsak mesec zaračunali trajanje in pisarniški material za projekt.</span><span class="sxs-lookup"><span data-stu-id="df5e8-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="df5e8-325">Ustvarite obračunsko pravilo, ki vključuje naslednje informacije:</span><span class="sxs-lookup"><span data-stu-id="df5e8-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="df5e8-326">Pogodbeno obdobje traja šest mesecev.</span><span class="sxs-lookup"><span data-stu-id="df5e8-326">The contract period is six months.</span></span>
-   <span data-ttu-id="df5e8-327">Svetovalni čas se izračuna po postavki 150 na uro.</span><span class="sxs-lookup"><span data-stu-id="df5e8-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="df5e8-328">Pisarniški material se zaračuna po nabavni vrednosti, skupni stroški projekta pa ne smejo presegati 10.000.</span><span class="sxs-lookup"><span data-stu-id="df5e8-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="df5e8-329">Med trajanjem projekta morate ustvariti račun za stranko na koncu vsakega koledarskega meseca.</span><span class="sxs-lookup"><span data-stu-id="df5e8-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="df5e8-330">V prvem mesecu so svetovalci na projektu zabeležili skupno 800 ur.</span><span class="sxs-lookup"><span data-stu-id="df5e8-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="df5e8-331">Strošek pisarniškega materiala, ki je zaračunan projektu, znaša 2.000.</span><span class="sxs-lookup"><span data-stu-id="df5e8-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="df5e8-332">Konec meseca torej ustvarite račun za 122.000, tj. 800 delovnih ur po 150 na uro plus 2.000 za pisarniški material.</span><span class="sxs-lookup"><span data-stu-id="df5e8-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



