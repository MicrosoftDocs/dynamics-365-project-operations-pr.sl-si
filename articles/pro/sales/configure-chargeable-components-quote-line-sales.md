---
title: Konfiguracija komponent v vrstici ponudbe, ki se zaračunajo
description: Ta tema ponuja informacije o nastavitvi zaračunljivih in nezaračunljivih komponent v vrstici projektne ponudbe.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003786"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="28f25-103">Konfiguriranje komponent podrobnosti ponudbe, ki se zaračunajo</span><span class="sxs-lookup"><span data-stu-id="28f25-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="28f25-104">_**Velja za:** poenostavljeno uvedbo – posel do izstavitve predračuna, Project Operations za primere, ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="28f25-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="28f25-105">Vrstica projektne pogodbe je sestavljena iz pojmov *vključenih* komponent in komponent, *ki se zaračunajo*.</span><span class="sxs-lookup"><span data-stu-id="28f25-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="28f25-106">Za vključene komponente veljajo naslednji elementi:</span><span class="sxs-lookup"><span data-stu-id="28f25-106">Included components are subject to:</span></span>

  - <span data-ttu-id="28f25-107">Način zaračunavanja in razdelitve kupcev</span><span class="sxs-lookup"><span data-stu-id="28f25-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="28f25-108">Omejitve »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="28f25-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="28f25-109">Nastavitve pogostosti izdajanja računov, ki so določene v vrstici ponudbe, ki temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="28f25-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="28f25-110">Podmnožico vključenih komponent je v polju **Vrsta obračunavanja** mogoče označiti kot zaračunljive.</span><span class="sxs-lookup"><span data-stu-id="28f25-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="28f25-111">Polje **Vrsta obračunavanja** predstavlja nabor možnosti, ki v okviru vrstice ponudbe omogoča naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="28f25-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="28f25-112">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-112">Chargeable</span></span>
  - <span data-ttu-id="28f25-113">Se ne zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-113">Non-chargeable</span></span>

<span data-ttu-id="28f25-114">Komponente, ki se zaračunajo, je mogoče določiti za opravila, vloge in kategorije transakcij.</span><span class="sxs-lookup"><span data-stu-id="28f25-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="28f25-115">Možnost zaračunavanja je določena v opravilih za posamezno vrstico ponudbe in velja za vse razrede transakcij, vključene v to vrstico.</span><span class="sxs-lookup"><span data-stu-id="28f25-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="28f25-116">Če je polje **Vključi opravila** prazno ali nastavljeno na možnost **Ves projekt**, zavihek **Opravila, ki se zaračunajo** ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="28f25-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="28f25-117">Možnost zaračunavanja je določena v vlogah za podrobnost projektne pogodbe in velja samo za razred transakcije **Čas**.</span><span class="sxs-lookup"><span data-stu-id="28f25-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="28f25-118">Če je v vrstici ponudbe polje **Vključi čas** prazno ali nastavljeno na možnost **Ne**, zavihek **Vloge, ki se zaračunajo** ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="28f25-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="28f25-119">Plačljivost je določena v kategorijah transakcije za podrobnost projektne pogodbe in velja samo za razred transakcije **Strošek**.</span><span class="sxs-lookup"><span data-stu-id="28f25-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="28f25-120">Če je v vrstici ponudbe polje **Vključi čas** prazno ali nastavljeno na možnost **Ne**, zavihek **Kategorije, ki se zaračunajo** ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="28f25-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="28f25-121">Posodabljanje projektnega opravila kot zaračunljivega ali nezaračunljivega</span><span class="sxs-lookup"><span data-stu-id="28f25-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="28f25-122">Projektna naloga je lahko v posamezni vrstici ponudbe, ki temelji na projektu, zaračunljiva ali nezaračunljiva, kar omogoča naslednje nastavitve.</span><span class="sxs-lookup"><span data-stu-id="28f25-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="28f25-123">Če vrstica ponudbe, ki temelji na projektu, vključuje možnost **Čas** in opravilo **T1**, je opravilo povezano s ponudbo kot zaračunljivo.</span><span class="sxs-lookup"><span data-stu-id="28f25-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="28f25-124">Če obstaja druga vrstica ponudbe, ki vključuje možnost **Stroški**, lahko opravilo **T1** v vrstici ponudbe povežete kot nezaračunljivo.</span><span class="sxs-lookup"><span data-stu-id="28f25-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="28f25-125">Rezultat tega je, da se ves čas, zabeležen za opravilo, zaračuna, vsi zabeleženi stroški pa se ne zaračunajo.</span><span class="sxs-lookup"><span data-stu-id="28f25-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="28f25-126">Vrsta obračuna za opravilo je lahko konfigurirana na zavihku **Opravila, ki se zaračunajo** podrobnosti ponudbe, ki temelji na projektih, s posodobitvijo polja **Vrsta obračunavanja** v podmreži **Opravila vrstice pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="28f25-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="28f25-127">Druga možnost je, da posodobite vrsto obračunavanja za opravilo projekta v polju **Vrsta obračunavanja** v podmreži v nastavitvah obračunavanja opravil projekta, ki prikazuje podrobnosti ponudb, povezane z opravilom.</span><span class="sxs-lookup"><span data-stu-id="28f25-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="28f25-128">Posodabljanje vloge kot zaračunljive ali nezaračunljive</span><span class="sxs-lookup"><span data-stu-id="28f25-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="28f25-129">Vloga je lahko v okviru določene vrstice ponudbe, ki temelji na projektu, zaračunljiva ali nezaračunljiva.</span><span class="sxs-lookup"><span data-stu-id="28f25-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="28f25-130">Vrsta obračuna za vlogo je lahko konfigurirana na zavihku **Vloge, ki se zaračunajo** podrobnosti ponudbe s posodobitvijo polja **Vrsta obračunavanja** v podmreži **Vloge, ki se zaračunajo**.</span><span class="sxs-lookup"><span data-stu-id="28f25-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="28f25-131">Posodabljanje kategorije transakcije kot zaračunljive ali nezaračunljive</span><span class="sxs-lookup"><span data-stu-id="28f25-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="28f25-132">V posamezni vrstici ponudbe se lahko kategorija transakcije zaračuna ali ne zaračuna.</span><span class="sxs-lookup"><span data-stu-id="28f25-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="28f25-133">Vrsta obračuna za transakcijo je lahko konfigurirana na zavihku **Kategorije, ki se zaračunajo** podrobnosti ponudbe s posodobitvijo polja **Vrsta obračunavanja** v podmreži **Kategorije, ki se zaračunajo**.</span><span class="sxs-lookup"><span data-stu-id="28f25-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="28f25-134">Razrešitev možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="28f25-134">Resolve chargeability</span></span>
<span data-ttu-id="28f25-135">Ocena ali dejansko ustvarjena vrednost za čas šteje za plačljivo le v naslednjih primerih:</span><span class="sxs-lookup"><span data-stu-id="28f25-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="28f25-136">**Čas** je vključen v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="28f25-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="28f25-137">**Vloga** je v vrstici ponudbe nastavljena kot plačljiva.</span><span class="sxs-lookup"><span data-stu-id="28f25-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="28f25-138">**Vključena opravila** so v vrstici ponudbe nastavljena na **Izbrana opravila**.</span><span class="sxs-lookup"><span data-stu-id="28f25-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="28f25-139">Če so te tri stvari resnične, je tudi **Opravilo** konfigurirano kot plačljivo.</span><span class="sxs-lookup"><span data-stu-id="28f25-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="28f25-140">Ocena ali dejansko ustvarjena vrednost za stroške šteje za plačljivo le v naslednjih primerih:</span><span class="sxs-lookup"><span data-stu-id="28f25-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="28f25-141">**Strošek** je vključen v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="28f25-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="28f25-142">**Kategorija transakcije** je v vrstici ponudbe nastavljena kot plačljiva.</span><span class="sxs-lookup"><span data-stu-id="28f25-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="28f25-143">**Vključena opravila** so v vrstici ponudbe nastavljena na **Izbrana opravila**.</span><span class="sxs-lookup"><span data-stu-id="28f25-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="28f25-144">Če so te tri stvari resnične, je tudi **Opravilo** konfigurirano kot plačljivo.</span><span class="sxs-lookup"><span data-stu-id="28f25-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="28f25-145">Ocena ali dejansko ustvarjena vrednost za material šteje za plačljivo le v naslednjih primerih:</span><span class="sxs-lookup"><span data-stu-id="28f25-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="28f25-146">**Materiali** so vključeni v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="28f25-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="28f25-147">**Vključena opravila** so v vrstici ponudbe nastavljena na **Izbrana opravila**.</span><span class="sxs-lookup"><span data-stu-id="28f25-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="28f25-148">Če sta ti dve stvari resnični, mora biti tudi **Opravilo** konfigurirano kot plačljivo.</span><span class="sxs-lookup"><span data-stu-id="28f25-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="28f25-149">
                    <strong>Čas je vključen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="28f25-150">
                    <strong>Strošek je vključen</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="28f25-151">
                    <strong>Vključuje materiale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="28f25-152">
                    <strong>Vključena opravila</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="28f25-153">
                    <strong>Vloga</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="28f25-154">
                    <strong>Kategoriji</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="28f25-155">
                    <strong>Opravilo</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="28f25-156">
                    <strong>Vpliv plačljivosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-157">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="28f25-158">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="28f25-159">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-160">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="28f25-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-161">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-162">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-163">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="28f25-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-164">Obračun po dejanskem času: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="28f25-165">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="28f25-166">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="28f25-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-167">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="28f25-168">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="28f25-169">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-170">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="28f25-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-171">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-172">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-173">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-174">Obračun po dejanskem času: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="28f25-175">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="28f25-176">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="28f25-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-177">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="28f25-178">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="28f25-179">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-180">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="28f25-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="28f25-181">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-182">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-183">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-184">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-185">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="28f25-186">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="28f25-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-187">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="28f25-188">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="28f25-189">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-190">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="28f25-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-191">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-192">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="28f25-193">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-194">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-195">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-196">Vrsta obračuna za dejanski material: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-197">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="28f25-198">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="28f25-199">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-200">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="28f25-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="28f25-201">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-202">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="28f25-203">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-204">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-205">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-206">Vrsta obračuna za dejanski material: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-207">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="28f25-208">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="28f25-209">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-210">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="28f25-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="28f25-211">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="28f25-212">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-213">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-214">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-215">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-216">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="28f25-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="28f25-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="28f25-218">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="28f25-219">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-220">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="28f25-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-221">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="28f25-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="28f25-222">
                    <strong>Se zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-223">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="28f25-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-224">Obračun po dejanskem času: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-225">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="28f25-226">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="28f25-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="28f25-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="28f25-228">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="28f25-229">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-230">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="28f25-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-231">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="28f25-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="28f25-232">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-233">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="28f25-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-234">Obračun po dejanskem času: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-235">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-236">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="28f25-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-237">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="28f25-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="28f25-239">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-240">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="28f25-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-241">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-242">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="28f25-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-243">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="28f25-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-244">Obračun po dejanskem času: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="28f25-245">Vrsta obračuna za dejanske stroške:<strong> Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-246">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="28f25-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-247">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="28f25-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="28f25-249">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-250">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="28f25-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="28f25-251">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-252">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="28f25-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-253">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="28f25-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-254">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-255">Vrsta obračuna za dejanske stroške:<strong> Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-256">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="28f25-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-257">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="28f25-258">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="28f25-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-260">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="28f25-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-261">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-262">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-263">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="28f25-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-264">Obračun po dejanskem času: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="28f25-265">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="28f25-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="28f25-266">Vrsta obračuna za dejanski material: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="28f25-267">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="28f25-268">Da</span><span class="sxs-lookup"><span data-stu-id="28f25-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="28f25-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="28f25-270">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="28f25-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="28f25-271">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="28f25-272">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="28f25-273">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="28f25-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="28f25-274">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-275">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="28f25-276">Vrsta obračuna za dejanski material: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="28f25-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
