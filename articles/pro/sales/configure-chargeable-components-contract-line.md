---
title: Konfiguriranje plačljivih komponent za podrobnosti pogodbe, ki temelji na projektu
description: Ta tema ponuja informacije o tem, kako v aplikaciji Project Operations v podrobnost pogodbe dodati komponente, ki se zaračunajo.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003741"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="34d70-103">Konfiguriranje plačljivih komponent za podrobnosti pogodbe, ki temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="34d70-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="34d70-104">_**Velja za:** poenostavljeno uvedbo – posel do izstavitve predračuna, Project Operations za primere, ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="34d70-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="34d70-105">Projektna podrobnost pogodbe je sestavljena iz *vključenih* komponent in komponent, *ki se zaračunajo*.</span><span class="sxs-lookup"><span data-stu-id="34d70-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="34d70-106">Vključene komponente so komponente, za katere velja:</span><span class="sxs-lookup"><span data-stu-id="34d70-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="34d70-107">Način zaračunavanja in razdelitve kupcev</span><span class="sxs-lookup"><span data-stu-id="34d70-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="34d70-108">Omejitve »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="34d70-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="34d70-109">Nastavitve pogostosti izdajanja računov, ki je določena v podrobnosti pogodbe, ki temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="34d70-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="34d70-110">Podmnožico vključenih komponent je v polju **Vrsta obračunavanja** mogoče označiti kot zaračunljive.</span><span class="sxs-lookup"><span data-stu-id="34d70-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="34d70-111">Polje **Vrsta obračunavanja** predstavlja nabor možnosti, ki v okviru podrobnosti pogodbe omogoča naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="34d70-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="34d70-112">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-112">Chargeable</span></span>
  - <span data-ttu-id="34d70-113">Se ne zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-113">Non-chargeable</span></span>

<span data-ttu-id="34d70-114">Komponente, ki se zaračunajo, je mogoče določiti za opravila, vloge in kategorije transakcij.</span><span class="sxs-lookup"><span data-stu-id="34d70-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="34d70-115">Zaračunavanje je določeno v opravilih za posamezno podrobnost pogodbe in velja za vse razrede transakcij, vključene v podrobnost.</span><span class="sxs-lookup"><span data-stu-id="34d70-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="34d70-116">Če je v podrobnosti pogodbe polje **Vključi opravila** prazno ali nastavljeno na možnost **Ves projekt**, zavihek **Opravila, ki se zaračunajo** ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="34d70-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="34d70-117">Zaračunavanje, določeno v vlogah za podrobnost projektne pogodbe, velja samo za razred transakcije **Čas**.</span><span class="sxs-lookup"><span data-stu-id="34d70-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="34d70-118">Če je v podrobnosti pogodbe polje **Vključi čas** prazno ali nastavljeno na možnost **Ne**, zavihek **Vloge, ki se zaračunajo** ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="34d70-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="34d70-119">Plačljivost, določena v kategorijah transakcije za podrobnost projektne pogodbe, velja samo za razred transakcije **Strošek**.</span><span class="sxs-lookup"><span data-stu-id="34d70-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="34d70-120">Če je polje **Vključi stroške** prazno ali nastavljeno na možnost **Ne**, zavihek **Kategorije, ki se zaračunajo** ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="34d70-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="34d70-121">Posodobite projektno opravilo kot zaračunljivo ali nezaračunljivo</span><span class="sxs-lookup"><span data-stu-id="34d70-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="34d70-122">Projektna naloga se lahko v posamezni podrobnosti pogodbe zaračuna ali ne zaračuna, kar omogoča naslednje nastavitve:</span><span class="sxs-lookup"><span data-stu-id="34d70-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="34d70-123">Če podrobnost pogodbe, ki temelji na projektu, vključuje možnost **Čas** in določeno opravilo, se možnost **T1** z njo poveže kot zaračunljiva.</span><span class="sxs-lookup"><span data-stu-id="34d70-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="34d70-124">Če obstaja druga podrobnost pogodbe, ki vključuje možnost **Stroški**, lahko opravilo T1 v podrobnosti pogodbe povežete kot nezaračunljivo.</span><span class="sxs-lookup"><span data-stu-id="34d70-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="34d70-125">Rezultat tega je, da se ves čas, zabeležen za opravilo, zaračuna, vsi stroški pa se ne zaračunajo.</span><span class="sxs-lookup"><span data-stu-id="34d70-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="34d70-126">Vrsta obračuna za opravilo je lahko konfigurirana na zavihku **Opravila, ki se zaračunajo** podrobnosti pogodbe s posodobitvijo polja **Vrsta obračunavanja** v podmreži opravil vrstice pogodbe.</span><span class="sxs-lookup"><span data-stu-id="34d70-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="34d70-127">Druga možnost je, da posodobite polje **Vrsta obračunavanja** v podmreži nastavitve obračunavanja opravil projekta, ki prikazuje podrobnosti pogodbe, povezane z opravilom.</span><span class="sxs-lookup"><span data-stu-id="34d70-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="34d70-128">Posodabljanje vloge kot zaračunljive ali nezaračunljive</span><span class="sxs-lookup"><span data-stu-id="34d70-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="34d70-129">V posamezni podrobnosti pogodbe je lahko vloga zaračunljiva ali nezaračunljiva.</span><span class="sxs-lookup"><span data-stu-id="34d70-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="34d70-130">Način obračunavanja vloge je mogoče nastaviti na zavihku **Vloge, ki se zaračunajo** v podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="34d70-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="34d70-131">To storite tako, da posodobite polje **Vrsta obračunavanja** v podmreži **Vloge, ki se zaračunajo**.</span><span class="sxs-lookup"><span data-stu-id="34d70-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="34d70-132">Posodabljanje kategorije transakcije kot zaračunljive ali nezaračunljive</span><span class="sxs-lookup"><span data-stu-id="34d70-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="34d70-133">V posamezni podrobnosti pogodbe je lahko kategorija transakcije zaračunljiva ali nezaračunljiva.</span><span class="sxs-lookup"><span data-stu-id="34d70-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="34d70-134">Način obračunavanja transakcije je mogoče nastaviti na zavihku **Kategorije, ki se zaračunajo** v podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="34d70-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="34d70-135">To storite tako, da posodobite polje **Vrsta obračunavanja** v podmreži **Kategorije, ki se zaračunajo**.</span><span class="sxs-lookup"><span data-stu-id="34d70-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="34d70-136">Razrešitev možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="34d70-136">Resolve chargeability</span></span>

<span data-ttu-id="34d70-137">Ocena ali dejansko ustvarjena vrednost za čas šteje za plačljivo le v naslednjih primerih:</span><span class="sxs-lookup"><span data-stu-id="34d70-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="34d70-138">**Čas** je vključen v podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="34d70-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="34d70-139">**Vloga** je v podrobnosti pogodbe nastavljena kot plačljiva.</span><span class="sxs-lookup"><span data-stu-id="34d70-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="34d70-140">**Vključena opravila** so v podrobnostih pogodbe nastavljena na **Izbrana opravila**.</span><span class="sxs-lookup"><span data-stu-id="34d70-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="34d70-141">Če so te tri stvari resnične, je tudi opravilo konfigurirano tudi kot plačljivo.</span><span class="sxs-lookup"><span data-stu-id="34d70-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="34d70-142">Ocena ali dejansko ustvarjena vrednost za stroške šteje za plačljivo le v naslednjih primerih:</span><span class="sxs-lookup"><span data-stu-id="34d70-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="34d70-143">**Stroški** so vključeni v podrobnosti pogodbe</span><span class="sxs-lookup"><span data-stu-id="34d70-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="34d70-144">**Kategorija transakcije** je v podrobnostih pogodbe nastavljena kot plačljiva</span><span class="sxs-lookup"><span data-stu-id="34d70-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="34d70-145">**Vključena opravila** so v podrobnostih pogodbe nastavljena na **Izbrano opravilo**</span><span class="sxs-lookup"><span data-stu-id="34d70-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="34d70-146">Če so te tri stvari resnične, je tudi **Opravilo** konfigurirano tudi kot plačljivo.</span><span class="sxs-lookup"><span data-stu-id="34d70-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="34d70-147">Ocena ali dejansko ustvarjena vrednost za material šteje za plačljivo le v naslednjih primerih:</span><span class="sxs-lookup"><span data-stu-id="34d70-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="34d70-148">**Materiali** so vključeni v podrobnosti pogodbe</span><span class="sxs-lookup"><span data-stu-id="34d70-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="34d70-149">**Vključena opravila** so v podrobnostih pogodbe nastavljena na **Izbrana opravila**</span><span class="sxs-lookup"><span data-stu-id="34d70-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="34d70-150">Če sta ti dve stvari resnični, je tudi **Opravilo** konfigurirano tudi kot plačljivo.</span><span class="sxs-lookup"><span data-stu-id="34d70-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="34d70-151">
                    <strong>Čas je vključen</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="34d70-152">
                    <strong>Strošek je vključen</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="34d70-153">
                    <strong>Vključuje materiale</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="34d70-154">
                    <strong>Vključena opravila</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="34d70-155">
                    <strong>Vloga</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="34d70-156">
                    <strong>Kategoriji</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="34d70-157">
                    <strong>Opravilo</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="34d70-158">
                    <strong>Vpliv plačljivosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-159">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="34d70-160">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="34d70-161">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-162">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="34d70-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-163">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-164">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-165">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="34d70-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-166">Obračun po dejanskem času: <strong>Se zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-167">Vrsta obračuna za dejanske stroške: <strong>Se zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-168">Vrsta obračuna za dejanski material: <strong>plačljivo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-169">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="34d70-170">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="34d70-171">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-172">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="34d70-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-173">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-174">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-175">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-176">Obračun po dejanskem času: <strong>Se zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-177">Vrsta obračuna za dejanske stroške: <strong>Se zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-178">Vrsta obračuna za dejanski material: <strong>plačljivo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-179">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="34d70-180">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="34d70-181">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-182">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="34d70-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="34d70-183">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-184">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-185">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-186">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-187">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="34d70-188">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="34d70-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-189">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="34d70-190">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="34d70-191">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-192">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="34d70-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-193">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-194">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="34d70-195">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-196">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-197">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-198">Vrsta obračuna za dejanski material: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-199">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="34d70-200">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="34d70-201">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-202">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="34d70-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="34d70-203">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-204">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="34d70-205">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-206">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-207">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-208">Vrsta obračuna za dejanski material: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-209">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="34d70-210">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="34d70-211">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-212">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="34d70-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="34d70-213">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="34d70-214">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-215">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-216">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-217">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-218">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="34d70-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="34d70-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="34d70-220">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="34d70-221">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-222">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="34d70-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-223">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="34d70-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="34d70-224">
                    <strong>Se zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-225">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="34d70-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-226">Obračun po dejanskem času: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-227">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="34d70-228">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="34d70-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="34d70-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="34d70-230">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="34d70-231">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-232">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="34d70-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-233">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="34d70-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="34d70-234">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-235">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="34d70-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-236">Obračun po dejanskem času: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-237">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-238">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="34d70-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-239">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="34d70-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="34d70-241">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-242">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="34d70-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-243">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-244">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="34d70-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-245">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="34d70-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-246">Obračun po dejanskem času: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="34d70-247">Vrsta obračuna za dejanske stroške:<strong> Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-248">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="34d70-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-249">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="34d70-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="34d70-251">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-252">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="34d70-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="34d70-253">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-254">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="34d70-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-255">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="34d70-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-256">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-257">Vrsta obračuna za dejanske stroške:<strong> Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-258">Vrsta obračuna za dejanski material: plačljivo</span><span class="sxs-lookup"><span data-stu-id="34d70-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-259">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="34d70-260">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="34d70-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-262">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="34d70-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-263">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-264">Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-265">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="34d70-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-266">Obračun po dejanskem času: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="34d70-267">Vrsta obračuna za dejansko vrednost stroška: Se zaračuna</span><span class="sxs-lookup"><span data-stu-id="34d70-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="34d70-268">Vrsta obračuna za dejanski material: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="34d70-269">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="34d70-270">Da</span><span class="sxs-lookup"><span data-stu-id="34d70-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="34d70-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="34d70-272">Celoten projekt</span><span class="sxs-lookup"><span data-stu-id="34d70-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="34d70-273">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="34d70-274">
                    <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="34d70-275">Ni mogoče nastaviti</span><span class="sxs-lookup"><span data-stu-id="34d70-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="34d70-276">Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-277">Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="34d70-278">Vrsta obračuna za dejanski material: <strong>Ni na voljo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="34d70-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
