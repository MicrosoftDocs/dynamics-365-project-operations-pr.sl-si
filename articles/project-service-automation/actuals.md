---
title: Opravljeno delo
description: Ta tema vsebuje informacije o dejanskih podatkih za projekt.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755858"
---
# <a name="actuals"></a><span data-ttu-id="cff37-103">Opravljeno delo</span><span class="sxs-lookup"><span data-stu-id="cff37-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cff37-104">Dejanski podatki se nanašajo na količino dela, ki je bilo opravljeno za projekt.</span><span class="sxs-lookup"><span data-stu-id="cff37-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="cff37-105">Dejanske podatke za projekt je mogoče izslediti do njihovih izvornih dokumentov.</span><span class="sxs-lookup"><span data-stu-id="cff37-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="cff37-106">Ti izvorni dokumenti vključujejo čas, stroške, dnevniške vnose in tudi račune.</span><span class="sxs-lookup"><span data-stu-id="cff37-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kako se dejanske podatke za projekt izsledi v izvornih dokumentih](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="cff37-108">Pošiljanje časovnega vnosa</span><span class="sxs-lookup"><span data-stu-id="cff37-108">Submitting a time entry</span></span>

<span data-ttu-id="cff37-109">Ko je v PSA poslan časovni vnos za projekt, ki je preslikan v podrobnosti pogodbe za čas in materiale, se ustvarita dve vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="cff37-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="cff37-110">Ena vrstica je za ceno, druga za neobračunano prodajo.</span><span class="sxs-lookup"><span data-stu-id="cff37-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="cff37-111">Ko je poslan časovni vnos za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se ustvari samo vrstica dnevnika za ceno.</span><span class="sxs-lookup"><span data-stu-id="cff37-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="cff37-112">Logika za vnos privzetih cen uporablja vrstico dnevnika.</span><span class="sxs-lookup"><span data-stu-id="cff37-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="cff37-113">Vse vrednosti polj iz časovnega vnosa se kopirajo v vrstico dnevnika.</span><span class="sxs-lookup"><span data-stu-id="cff37-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="cff37-114">Ta polja vključujejo datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in rezultat valute v skladu z ustreznim cenikom.</span><span class="sxs-lookup"><span data-stu-id="cff37-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="cff37-115">Polja, ki vplivajo na privzete cene, kot sta **Vloga** in **Organizacijska enota**, povzročijo, da se v vrstico dnevnika privzeto vnese ustrezna cena.</span><span class="sxs-lookup"><span data-stu-id="cff37-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="cff37-116">Če za časovni vnos dodate polje po meri in želite, da se vrednost polja razširi na dejanske podatke, ustvarite polje v entiteti »Dejanski podatki« in za kopiranje polja iz časovnega vnosa v dejanske podatke uporabite preslikave polj.</span><span class="sxs-lookup"><span data-stu-id="cff37-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="cff37-117">Pošiljanje vnosa stroška</span><span class="sxs-lookup"><span data-stu-id="cff37-117">Submitting an expense entry</span></span>

<span data-ttu-id="cff37-118">Ko je v PSA poslan vnos stroška za projekt, ki je preslikan v podrobnosti pogodbe za čas in materiale, se ustvarita dve vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="cff37-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="cff37-119">Ena vrstica je za ceno, druga za neobračunano prodajo.</span><span class="sxs-lookup"><span data-stu-id="cff37-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="cff37-120">Ko je poslan vnos stroška za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se ustvari samo vrstica dnevnika za ceno.</span><span class="sxs-lookup"><span data-stu-id="cff37-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="cff37-121">Logika za vnašanje privzetih cen za stroške temelji na kategoriji stroška, ki je izbrana na strani **Vnos stroška**.</span><span class="sxs-lookup"><span data-stu-id="cff37-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="cff37-122">Datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in valuta se uporabijo za ugotavljanje ustreznega cenika.</span><span class="sxs-lookup"><span data-stu-id="cff37-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="cff37-123">Vendar pa je za ceno znesek, ki ga je uporabnik vnesel, privzeto nastavljen neposredno v povezani vrstici dnevnika stroškov za strošek in prodajo.</span><span class="sxs-lookup"><span data-stu-id="cff37-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="cff37-124">V trenutni različici aplikacije PSA vnos privzetih cen na enoto na podlagi kategorije za vnose stroška ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="cff37-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="cff37-125">Uporaba dnevnikov za zapisovanje stroškov</span><span class="sxs-lookup"><span data-stu-id="cff37-125">Using journals to record costs</span></span>

<span data-ttu-id="cff37-126">V aplikaciji PSA lahko v dnevnike beležimo stroške ali prihodke v razredih transakcij za material, dajatve, čas, stroške ali davke.</span><span class="sxs-lookup"><span data-stu-id="cff37-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="cff37-127">Dnevnik vsebuje glavo, vrstice in ukaz za **potrditev**.</span><span class="sxs-lookup"><span data-stu-id="cff37-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="cff37-128">Tukaj je nekaj scenarijev, v katerih lahko uporabite dnevnik:</span><span class="sxs-lookup"><span data-stu-id="cff37-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="cff37-129">Za projekt morate zabeležiti dejanske stroške materiala in prodaje.</span><span class="sxs-lookup"><span data-stu-id="cff37-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="cff37-130">V PSA morate prenesti dejanske podatke o transakcijah iz drugega sistema.</span><span class="sxs-lookup"><span data-stu-id="cff37-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="cff37-131">Zabeležiti morate stroške, ki so nastali v drugem sistemu, npr. za stroške nabave ali podizvajalcev.</span><span class="sxs-lookup"><span data-stu-id="cff37-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="cff37-132">Zapisovanje dejanskih podatkov na podlagi projektnih dogodkov</span><span class="sxs-lookup"><span data-stu-id="cff37-132">Recording actuals based on project events</span></span>

<span data-ttu-id="cff37-133">PDA zapiše finančne transakcije v okviru projekta.</span><span class="sxs-lookup"><span data-stu-id="cff37-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="cff37-134">Te transakcije se zapišejo kot **dejanske vrednosti**.</span><span class="sxs-lookup"><span data-stu-id="cff37-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="cff37-135">V spodnjih tabelah so prikazane različne vrste dejanskih vrednosti, ki so ustvarjene, glede na to, ali gre za časovne in materialne transakcije ali transakcije s fiksno ceno ali gre za stopnjo pred prodajo oziroma interni projekt.</span><span class="sxs-lookup"><span data-stu-id="cff37-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="cff37-136">**Vir pripada isti organizacijski enoti kot pogodbena enota projekta**</span><span class="sxs-lookup"><span data-stu-id="cff37-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cff37-137">Dogodek</span><span class="sxs-lookup"><span data-stu-id="cff37-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cff37-138">Obračunan ali prodan projekt</span><span class="sxs-lookup"><span data-stu-id="cff37-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cff37-139">Projekt v fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="cff37-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cff37-140">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="cff37-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cff37-141">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="cff37-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cff37-142">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="cff37-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cff37-143">Opravljeno delo</span><span class="sxs-lookup"><span data-stu-id="cff37-143">Actuals</span></span></th>
<th><span data-ttu-id="cff37-144">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="cff37-144">Transaction currency</span></span></th>
<th><span data-ttu-id="cff37-145">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="cff37-145">Fixed price</span></span></th>
<th><span data-ttu-id="cff37-146">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="cff37-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cff37-147">Ustvari se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="cff37-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cff37-148">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="cff37-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-149">Pošlje se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="cff37-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cff37-150">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="cff37-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cff37-151">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cff37-152">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-152">Cost actual</span></span></td>
<td><span data-ttu-id="cff37-153">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="cff37-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cff37-154">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cff37-155">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="cff37-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="cff37-156">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="cff37-157">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-158">Dejanska neobračunana prodaja – za obračunavanje</span><span class="sxs-lookup"><span data-stu-id="cff37-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cff37-159">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cff37-160">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cff37-161">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-161">Cost actual</span></span></td>
<td><span data-ttu-id="cff37-162">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="cff37-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-163">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-164">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="cff37-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-165">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-166">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-167">Dejanska neobračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="cff37-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cff37-168">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-169">Dejanska neobračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="cff37-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cff37-170">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cff37-171">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cff37-172">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="cff37-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cff37-173">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cff37-174">Obračunana prodaja za mejnik</span><span class="sxs-lookup"><span data-stu-id="cff37-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cff37-175">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cff37-176">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cff37-177">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-178">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="cff37-178">Billed sales</span></span></td>
<td><span data-ttu-id="cff37-179">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cff37-180">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cff37-181">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="cff37-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cff37-182">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-183">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-184">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-185">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-186">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-187">Obračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="cff37-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cff37-188">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-189">Obračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="cff37-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cff37-190">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cff37-191">Račun je popravljen s povečano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cff37-192">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="cff37-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cff37-193">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cff37-194">Storniranje obračunane prodaje za mejnik</span><span class="sxs-lookup"><span data-stu-id="cff37-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cff37-195">Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></span><span class="sxs-lookup"><span data-stu-id="cff37-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cff37-196">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cff37-197">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cff37-198">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-199">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="cff37-199">Billed sales</span></span></td>
<td><span data-ttu-id="cff37-200">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cff37-201">Račun je popravljen z zmanjšano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cff37-202">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="cff37-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cff37-203">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-204">Obračunana prodaja za novo količino</span><span class="sxs-lookup"><span data-stu-id="cff37-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cff37-205">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-206">Neobračunana prodaja – obračuna se za razliko</span><span class="sxs-lookup"><span data-stu-id="cff37-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cff37-207">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cff37-208">**Vir pripada organizacijski enoti, ki se razlikuje od pogodbene enote projekta**</span><span class="sxs-lookup"><span data-stu-id="cff37-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="cff37-209">Dogodek</span><span class="sxs-lookup"><span data-stu-id="cff37-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="cff37-210">Obračunan ali prodan projekt</span><span class="sxs-lookup"><span data-stu-id="cff37-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="cff37-211">Projekt v fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="cff37-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="cff37-212">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="cff37-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="cff37-213">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="cff37-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="cff37-214">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="cff37-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cff37-215">Opravljeno delo</span><span class="sxs-lookup"><span data-stu-id="cff37-215">Actuals</span></span></th>
<th><span data-ttu-id="cff37-216">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="cff37-216">Transaction currency</span></span></th>
<th><span data-ttu-id="cff37-217">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="cff37-217">Fixed price</span></span></th>
<th><span data-ttu-id="cff37-218">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="cff37-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cff37-219">Ustvari se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="cff37-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="cff37-220">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="cff37-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-221">Pošlje se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="cff37-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="cff37-222">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="cff37-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="cff37-223">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cff37-224">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-224">Cost actual</span></span></td>
<td><span data-ttu-id="cff37-225">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="cff37-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cff37-226">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cff37-227">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="cff37-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="cff37-228">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="cff37-229">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-230">Dejanska neobračunana prodaja – za obračunavanje</span><span class="sxs-lookup"><span data-stu-id="cff37-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="cff37-231">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-232">Cena enote vira</span><span class="sxs-lookup"><span data-stu-id="cff37-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cff37-233">Valuta enote vira</span><span class="sxs-lookup"><span data-stu-id="cff37-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-234">Prodaja znotraj organizacije</span><span class="sxs-lookup"><span data-stu-id="cff37-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cff37-235">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="cff37-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="cff37-236">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="cff37-237">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-237">Cost actual</span></span></td>
<td><span data-ttu-id="cff37-238">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="cff37-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cff37-239">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cff37-240">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="cff37-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cff37-241">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="cff37-242">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="cff37-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-243">Cena enote vira</span><span class="sxs-lookup"><span data-stu-id="cff37-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="cff37-244">Valuta enote vira</span><span class="sxs-lookup"><span data-stu-id="cff37-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-245">Prodaja znotraj organizacije</span><span class="sxs-lookup"><span data-stu-id="cff37-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="cff37-246">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="cff37-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-247">Dejanska neobračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="cff37-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cff37-248">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-249">Dejanska neobračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="cff37-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cff37-250">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cff37-251">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cff37-252">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="cff37-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cff37-253">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cff37-254">Obračunana prodaja za mejnik</span><span class="sxs-lookup"><span data-stu-id="cff37-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="cff37-255">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="cff37-256">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="cff37-257">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-258">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="cff37-258">Billed sales</span></span></td>
<td><span data-ttu-id="cff37-259">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cff37-260">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="cff37-261">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="cff37-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="cff37-262">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-263">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-264">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-265">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="cff37-266">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-267">Obračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="cff37-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="cff37-268">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-269">Obračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="cff37-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="cff37-270">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="cff37-271">Račun je popravljen s povečano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cff37-272">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="cff37-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cff37-273">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="cff37-274">Storniranje obračunane prodaje za mejnik</span><span class="sxs-lookup"><span data-stu-id="cff37-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="cff37-275">Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></span><span class="sxs-lookup"><span data-stu-id="cff37-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="cff37-276">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="cff37-277">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="cff37-278">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="cff37-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-279">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="cff37-279">Billed sales</span></span></td>
<td><span data-ttu-id="cff37-280">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="cff37-281">Račun je popravljen z zmanjšano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="cff37-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="cff37-282">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="cff37-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="cff37-283">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-284">Obračunana prodaja za novo količino</span><span class="sxs-lookup"><span data-stu-id="cff37-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="cff37-285">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cff37-286">Neobračunana prodaja – obračuna se za razliko</span><span class="sxs-lookup"><span data-stu-id="cff37-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="cff37-287">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="cff37-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
