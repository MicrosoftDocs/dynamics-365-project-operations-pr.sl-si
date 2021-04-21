---
title: Konfiguracija komponent v vrstici ponudbe, ki se zaračunajo
description: Ta tema ponuja informacije o nastavitvi zaračunljivih in nezaračunljivih komponent v vrstici projektne ponudbe.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858313"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="1af97-103">Konfiguriranje komponent podrobnosti ponudbe, ki se zaračunajo</span><span class="sxs-lookup"><span data-stu-id="1af97-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="1af97-104">_**Velja za:** poenostavljeno uvedbo – posel do izstavitve predračuna, Project Operations za primere, ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="1af97-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1af97-105">Vrstica projektne pogodbe je sestavljena iz pojmov *vključenih* komponent in komponent, *ki se zaračunajo*.</span><span class="sxs-lookup"><span data-stu-id="1af97-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="1af97-106">Za vključene komponente veljajo naslednji elementi:</span><span class="sxs-lookup"><span data-stu-id="1af97-106">Included components are subject to:</span></span>

  - <span data-ttu-id="1af97-107">Način zaračunavanja in razdelitve kupcev</span><span class="sxs-lookup"><span data-stu-id="1af97-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="1af97-108">Omejitve »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="1af97-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="1af97-109">Nastavitve pogostosti izdajanja računov, ki so določene v vrstici ponudbe, ki temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="1af97-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="1af97-110">Podmnožico vključenih komponent je v polju **Vrsta obračunavanja** mogoče označiti kot zaračunljive.</span><span class="sxs-lookup"><span data-stu-id="1af97-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="1af97-111">Polje **Vrsta obračunavanja** predstavlja nabor možnosti, ki v okviru vrstice ponudbe omogoča naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="1af97-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="1af97-112">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-112">Chargeable</span></span>
  - <span data-ttu-id="1af97-113">Se ne zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-113">Non-chargeable</span></span>

<span data-ttu-id="1af97-114">Komponente, ki se zaračunajo, je mogoče določiti za opravila, vloge in kategorije transakcij.</span><span class="sxs-lookup"><span data-stu-id="1af97-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="1af97-115">Možnost zaračunavanja je določena v opravilih za posamezno vrstico ponudbe in velja za vse razrede transakcij, vključene v to vrstico.</span><span class="sxs-lookup"><span data-stu-id="1af97-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="1af97-116">Če je polje **Vključi opravila** prazno ali nastavljeno na možnost **Ves projekt**, zavihek **Opravila, ki se zaračunajo** ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="1af97-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="1af97-117">Možnost zaračunavanja je določena v vlogah za podrobnost projektne pogodbe in velja samo za razred transakcije **Čas**.</span><span class="sxs-lookup"><span data-stu-id="1af97-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="1af97-118">Če je v vrstici ponudbe polje **Vključi čas** prazno ali nastavljeno na možnost **Ne**, zavihek **Vloge, ki se zaračunajo** ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="1af97-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="1af97-119">Plačljivost je določena v kategorijah transakcije za podrobnost projektne pogodbe in velja samo za razred transakcije **Strošek**.</span><span class="sxs-lookup"><span data-stu-id="1af97-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="1af97-120">Če je v vrstici ponudbe polje **Vključi čas** prazno ali nastavljeno na možnost **Ne**, zavihek **Kategorije, ki se zaračunajo** ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="1af97-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="1af97-121">Posodabljanje projektnega opravila kot zaračunljivega ali nezaračunljivega</span><span class="sxs-lookup"><span data-stu-id="1af97-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="1af97-122">Projektna naloga je lahko v posamezni vrstici ponudbe, ki temelji na projektu, zaračunljiva ali nezaračunljiva, kar omogoča naslednje nastavitve.</span><span class="sxs-lookup"><span data-stu-id="1af97-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="1af97-123">Če vrstica ponudbe, ki temelji na projektu, vključuje možnost **Čas** in opravilo **T1**, je opravilo povezano s ponudbo kot zaračunljivo.</span><span class="sxs-lookup"><span data-stu-id="1af97-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="1af97-124">Če obstaja druga vrstica ponudbe, ki vključuje možnost **Stroški**, lahko opravilo **T1** v vrstici ponudbe povežete kot nezaračunljivo.</span><span class="sxs-lookup"><span data-stu-id="1af97-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="1af97-125">Rezultat tega je, da se ves čas, zabeležen za opravilo, zaračuna, vsi zabeleženi stroški pa se ne zaračunajo.</span><span class="sxs-lookup"><span data-stu-id="1af97-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="1af97-126">Vrsta obračuna za opravilo je lahko konfigurirana na zavihku **Opravila, ki se zaračunajo** podrobnosti ponudbe, ki temelji na projektih, s posodobitvijo polja **Vrsta obračunavanja** v podmreži **Opravila vrstice pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="1af97-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="1af97-127">Druga možnost je, da posodobite vrsto obračunavanja za opravilo projekta v polju **Vrsta obračunavanja** v podmreži v nastavitvah obračunavanja opravil projekta, ki prikazuje podrobnosti ponudb, povezane z opravilom.</span><span class="sxs-lookup"><span data-stu-id="1af97-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="1af97-128">Posodabljanje vloge kot zaračunljive ali nezaračunljive</span><span class="sxs-lookup"><span data-stu-id="1af97-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="1af97-129">Vloga je lahko v okviru določene vrstice ponudbe, ki temelji na projektu, zaračunljiva ali nezaračunljiva.</span><span class="sxs-lookup"><span data-stu-id="1af97-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="1af97-130">Vrsta obračuna za vlogo je lahko konfigurirana na zavihku **Vloge, ki se zaračunajo** podrobnosti ponudbe s posodobitvijo polja **Vrsta obračunavanja** v podmreži **Vloge, ki se zaračunajo**.</span><span class="sxs-lookup"><span data-stu-id="1af97-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="1af97-131">Posodabljanje kategorije transakcije kot zaračunljive ali nezaračunljive</span><span class="sxs-lookup"><span data-stu-id="1af97-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="1af97-132">V posamezni vrstici ponudbe se lahko kategorija transakcije zaračuna ali ne zaračuna.</span><span class="sxs-lookup"><span data-stu-id="1af97-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="1af97-133">Vrsta obračuna za transakcijo je lahko konfigurirana na zavihku **Kategorije, ki se zaračunajo** podrobnosti ponudbe s posodobitvijo polja **Vrsta obračunavanja** v podmreži **Kategorije, ki se zaračunajo**.</span><span class="sxs-lookup"><span data-stu-id="1af97-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="1af97-134">Razrešitev možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="1af97-134">Resolve chargeability</span></span>
<span data-ttu-id="1af97-135">Ocena ali dejansko ustvarjena vrednost za čas šteje za plačljivo le v naslednjih primerih:</span><span class="sxs-lookup"><span data-stu-id="1af97-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="1af97-136">**Čas** je vključen v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="1af97-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="1af97-137">**Vloga** je v vrstici ponudbe nastavljena kot plačljiva.</span><span class="sxs-lookup"><span data-stu-id="1af97-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="1af97-138">**Vključena opravila** so v vrstici ponudbe nastavljena na **Izbrana opravila**.</span><span class="sxs-lookup"><span data-stu-id="1af97-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="1af97-139">Če so te tri stvari resnične, je tudi **Opravilo** konfigurirano kot plačljivo.</span><span class="sxs-lookup"><span data-stu-id="1af97-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="1af97-140">Ocena ali dejansko ustvarjena vrednost za stroške šteje za plačljivo le v naslednjih primerih:</span><span class="sxs-lookup"><span data-stu-id="1af97-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="1af97-141">**Strošek** je vključen v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="1af97-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="1af97-142">**Kategorija transakcije** je v vrstici ponudbe nastavljena kot plačljiva.</span><span class="sxs-lookup"><span data-stu-id="1af97-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="1af97-143">**Vključena opravila** so v vrstici ponudbe nastavljena na **Izbrana opravila**.</span><span class="sxs-lookup"><span data-stu-id="1af97-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="1af97-144">Če so te tri stvari resnične, je tudi **Opravilo** konfigurirano kot plačljivo.</span><span class="sxs-lookup"><span data-stu-id="1af97-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="1af97-145">Ocena ali dejansko ustvarjena vrednost za material šteje za plačljivo le v naslednjih primerih:</span><span class="sxs-lookup"><span data-stu-id="1af97-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="1af97-146">**Materiali** so vključeni v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="1af97-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="1af97-147">**Vključena opravila** so v vrstici ponudbe nastavljena na **Izbrana opravila**.</span><span class="sxs-lookup"><span data-stu-id="1af97-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="1af97-148">Če sta ti dve stvari resnični, mora biti tudi **Opravilo** konfigurirano kot plačljivo.</span><span class="sxs-lookup"><span data-stu-id="1af97-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1af97-149">
                    <strong>Čas je vključen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1af97-150">
                    <strong>Strošek je vključen</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1af97-151">
                    <strong>Vključuje materiale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="1af97-152">
                    <strong>Vključena opravila</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1af97-153">
                    <strong>Vloga</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1af97-154">
                    <strong>Kategoriji</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1af97-155">
                    <strong>Opravilo</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="1af97-156">
                    <strong>Vpliv plačljivosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-157">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1af97-158">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1af97-159">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-160">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="1af97-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-161">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-162">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-163">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="1af97-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-164">Obračun po dejanskem času: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1af97-165">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1af97-166">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="1af97-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-167">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1af97-168">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1af97-169">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-170">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="1af97-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-171">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-172">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-173">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-174">Obračun po dejanskem času: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1af97-175">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1af97-176">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="1af97-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-177">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1af97-178">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1af97-179">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-180">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="1af97-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1af97-181">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-182">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-183">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-184">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-185">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1af97-186">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="1af97-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-187">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1af97-188">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1af97-189">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-190">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="1af97-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-191">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-192">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1af97-193">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-194">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-195">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-196">Vrsta obračuna za dejanski material: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-197">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1af97-198">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1af97-199">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-200">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="1af97-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1af97-201">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-202">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1af97-203">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-204">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-205">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-206">Vrsta obračuna za dejanski material: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-207">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1af97-208">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1af97-209">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-210">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="1af97-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1af97-211">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1af97-212">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-213">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-214">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-215">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-216">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="1af97-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1af97-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1af97-218">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1af97-219">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-220">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="1af97-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-221">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="1af97-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1af97-222">
                    <strong>Se zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-223">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="1af97-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-224">Obračun po dejanskem času: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-225">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1af97-226">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="1af97-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="1af97-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1af97-228">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1af97-229">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-230">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="1af97-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-231">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="1af97-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1af97-232">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-233">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="1af97-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-234">Obračun po dejanskem času: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-235">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-236">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="1af97-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-237">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1af97-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1af97-239">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-240">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="1af97-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-241">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-242">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="1af97-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-243">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="1af97-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-244">Obračun po dejanskem času: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1af97-245">Vrsta obračuna za dejanske stroške:<strong> Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-246">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="1af97-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-247">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="1af97-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="1af97-249">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-250">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="1af97-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1af97-251">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-252">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="1af97-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-253">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="1af97-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-254">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-255">Vrsta obračuna za dejanske stroške:<strong> Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-256">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="1af97-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-257">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1af97-258">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1af97-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-260">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="1af97-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-261">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-262">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-263">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="1af97-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-264">Obračun po dejanskem času: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1af97-265">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="1af97-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="1af97-266">Vrsta obračuna za dejanski material: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="1af97-267">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="1af97-268">Da</span><span class="sxs-lookup"><span data-stu-id="1af97-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="1af97-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="1af97-270">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="1af97-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="1af97-271">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="1af97-272">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="1af97-273">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="1af97-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="1af97-274">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-275">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="1af97-276">Vrsta obračuna za dejanski material: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1af97-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
