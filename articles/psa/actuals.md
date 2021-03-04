---
title: Pregled dejanskih vrednosti
description: Ta tema vsebuje informacije o dejanskih podatkih za projekt.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146143"
---
# <a name="actuals-overview"></a><span data-ttu-id="027cd-103">Pregled dejanskih vrednosti</span><span class="sxs-lookup"><span data-stu-id="027cd-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="027cd-104">Dejanski podatki se nanašajo na količino dela, ki je bilo opravljeno za projekt.</span><span class="sxs-lookup"><span data-stu-id="027cd-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="027cd-105">Dejanske podatke za projekt je mogoče izslediti do njihovih izvornih dokumentov.</span><span class="sxs-lookup"><span data-stu-id="027cd-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="027cd-106">Ti izvorni dokumenti vključujejo čas, stroške, dnevniške vnose in tudi račune.</span><span class="sxs-lookup"><span data-stu-id="027cd-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kako se dejanske podatke za projekt izsledi v izvornih dokumentih](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="027cd-108">Pošiljanje časovnega vnosa</span><span class="sxs-lookup"><span data-stu-id="027cd-108">Submitting a time entry</span></span>

<span data-ttu-id="027cd-109">Ko je v PSA poslan časovni vnos za projekt, ki je preslikan v podrobnosti pogodbe za čas in materiale, se ustvarita dve vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="027cd-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="027cd-110">Ena vrstica je za ceno, druga za neobračunano prodajo.</span><span class="sxs-lookup"><span data-stu-id="027cd-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="027cd-111">Ko je poslan časovni vnos za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se ustvari samo vrstica dnevnika za ceno.</span><span class="sxs-lookup"><span data-stu-id="027cd-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="027cd-112">Logika za vnos privzetih cen uporablja vrstico dnevnika.</span><span class="sxs-lookup"><span data-stu-id="027cd-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="027cd-113">Vse vrednosti polj iz časovnega vnosa se kopirajo v vrstico dnevnika.</span><span class="sxs-lookup"><span data-stu-id="027cd-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="027cd-114">Ta polja vključujejo datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in rezultat valute v skladu z ustreznim cenikom.</span><span class="sxs-lookup"><span data-stu-id="027cd-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="027cd-115">Polja, ki vplivajo na privzete cene, kot sta **Vloga** in **Organizacijska enota**, povzročijo, da se v vrstico dnevnika privzeto vnese ustrezna cena.</span><span class="sxs-lookup"><span data-stu-id="027cd-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="027cd-116">Če za časovni vnos dodate polje po meri in želite, da se vrednost polja razširi na dejanske podatke, ustvarite polje v entiteti »Dejanski podatki« in za kopiranje polja iz časovnega vnosa v dejanske podatke uporabite preslikave polj.</span><span class="sxs-lookup"><span data-stu-id="027cd-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="027cd-117">Pošiljanje vnosa stroška</span><span class="sxs-lookup"><span data-stu-id="027cd-117">Submitting an expense entry</span></span>

<span data-ttu-id="027cd-118">Ko je v PSA poslan vnos stroška za projekt, ki je preslikan v podrobnosti pogodbe za čas in materiale, se ustvarita dve vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="027cd-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="027cd-119">Ena vrstica je za ceno, druga za neobračunano prodajo.</span><span class="sxs-lookup"><span data-stu-id="027cd-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="027cd-120">Ko je poslan vnos stroška za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se ustvari samo vrstica dnevnika za ceno.</span><span class="sxs-lookup"><span data-stu-id="027cd-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="027cd-121">Logika za vnašanje privzetih cen za stroške temelji na kategoriji stroška, ki je izbrana na strani **Vnos stroška**.</span><span class="sxs-lookup"><span data-stu-id="027cd-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="027cd-122">Datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in valuta se uporabijo za ugotavljanje ustreznega cenika.</span><span class="sxs-lookup"><span data-stu-id="027cd-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="027cd-123">Vendar pa je za ceno znesek, ki ga je uporabnik vnesel, privzeto nastavljen neposredno v povezani vrstici dnevnika stroškov za strošek in prodajo.</span><span class="sxs-lookup"><span data-stu-id="027cd-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="027cd-124">V trenutni različici aplikacije PSA vnos privzetih cen na enoto na podlagi kategorije za vnose stroška ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="027cd-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="027cd-125">Uporaba dnevnikov za zapisovanje stroškov</span><span class="sxs-lookup"><span data-stu-id="027cd-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="027cd-126">V aplikaciji PSA lahko v dnevnike beležimo stroške ali prihodke v razredih transakcij za material, provizijo, čas, stroške ali davke.</span><span class="sxs-lookup"><span data-stu-id="027cd-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="027cd-127">Dnevnik vsebuje glavo, vrstice in ukaz za **potrditev**.</span><span class="sxs-lookup"><span data-stu-id="027cd-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="027cd-128">Tukaj je nekaj scenarijev, v katerih lahko uporabite dnevnik:</span><span class="sxs-lookup"><span data-stu-id="027cd-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="027cd-129">Za projekt morate zabeležiti dejanske stroške materiala in prodaje.</span><span class="sxs-lookup"><span data-stu-id="027cd-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="027cd-130">V PSA morate prenesti dejanske podatke o transakcijah iz drugega sistema.</span><span class="sxs-lookup"><span data-stu-id="027cd-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="027cd-131">Zabeležiti morate stroške, ki so nastali v drugem sistemu, npr. za stroške nabave ali podizvajalcev.</span><span class="sxs-lookup"><span data-stu-id="027cd-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="027cd-132">Dnevnike za ustvarjanje dejanskih podatkov naj uporablja samo en uporabnik, ki je v celoti seznanjen z računovodskim vplivom, ki ga imajo dejanski podatki na projekt.</span><span class="sxs-lookup"><span data-stu-id="027cd-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="027cd-133">Razlog je v tem, da aplikacija ne potrdi vrstice dnevnika ali s tem povezane cene, ki je vnesena v vrstico dnevnika.</span><span class="sxs-lookup"><span data-stu-id="027cd-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="027cd-134">Zaradi vpliva teh vrst dnevnikov bodite previdni, komu omogočite dostop do ustvarjanja vknjižb.</span><span class="sxs-lookup"><span data-stu-id="027cd-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="027cd-135">Zapisovanje dejanskih podatkov na podlagi projektnih dogodkov</span><span class="sxs-lookup"><span data-stu-id="027cd-135">Recording actuals based on project events</span></span>

<span data-ttu-id="027cd-136">PDA zapiše finančne transakcije v okviru projekta.</span><span class="sxs-lookup"><span data-stu-id="027cd-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="027cd-137">Te transakcije se zapišejo kot **dejanske vrednosti**.</span><span class="sxs-lookup"><span data-stu-id="027cd-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="027cd-138">V spodnjih tabelah so prikazane različne vrste dejanskih vrednosti, ki so ustvarjene, glede na to, ali gre za časovne in materialne transakcije ali transakcije s fiksno ceno ali gre za stopnjo pred prodajo oziroma interni projekt.</span><span class="sxs-lookup"><span data-stu-id="027cd-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="027cd-139">**Vir pripada isti organizacijski enoti kot pogodbena enota projekta**</span><span class="sxs-lookup"><span data-stu-id="027cd-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="027cd-140">Dogodek</span><span class="sxs-lookup"><span data-stu-id="027cd-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="027cd-141">Obračunan ali prodan projekt</span><span class="sxs-lookup"><span data-stu-id="027cd-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="027cd-142">Projekt v fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="027cd-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="027cd-143">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="027cd-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="027cd-144">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="027cd-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="027cd-145">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="027cd-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="027cd-146">Opravljeno delo</span><span class="sxs-lookup"><span data-stu-id="027cd-146">Actuals</span></span></th>
<th><span data-ttu-id="027cd-147">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="027cd-147">Transaction currency</span></span></th>
<th><span data-ttu-id="027cd-148">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="027cd-148">Fixed price</span></span></th>
<th><span data-ttu-id="027cd-149">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="027cd-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="027cd-150">Ustvari se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="027cd-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="027cd-151">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="027cd-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-152">Pošlje se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="027cd-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="027cd-153">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="027cd-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="027cd-154">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="027cd-155">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-155">Cost actual</span></span></td>
<td><span data-ttu-id="027cd-156">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="027cd-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="027cd-157">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="027cd-158">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="027cd-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="027cd-159">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="027cd-160">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-161">Dejanska neobračunana prodaja – za obračunavanje</span><span class="sxs-lookup"><span data-stu-id="027cd-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="027cd-162">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="027cd-163">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="027cd-164">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-164">Cost actual</span></span></td>
<td><span data-ttu-id="027cd-165">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="027cd-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-166">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-167">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="027cd-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-168">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-169">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-170">Dejanska neobračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="027cd-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="027cd-171">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-172">Dejanska neobračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="027cd-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="027cd-173">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="027cd-174">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="027cd-175">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="027cd-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="027cd-176">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="027cd-177">Obračunana prodaja za mejnik</span><span class="sxs-lookup"><span data-stu-id="027cd-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="027cd-178">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="027cd-179">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="027cd-180">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-181">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="027cd-181">Billed sales</span></span></td>
<td><span data-ttu-id="027cd-182">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="027cd-183">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="027cd-184">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="027cd-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="027cd-185">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-186">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-187">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-188">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-189">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-190">Obračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="027cd-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="027cd-191">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-192">Obračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="027cd-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="027cd-193">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="027cd-194">Račun je popravljen s povečano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="027cd-195">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="027cd-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="027cd-196">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="027cd-197">Storniranje obračunane prodaje za mejnik</span><span class="sxs-lookup"><span data-stu-id="027cd-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="027cd-198">Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></span><span class="sxs-lookup"><span data-stu-id="027cd-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="027cd-199">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="027cd-200">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="027cd-201">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-202">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="027cd-202">Billed sales</span></span></td>
<td><span data-ttu-id="027cd-203">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="027cd-204">Račun je popravljen z zmanjšano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="027cd-205">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="027cd-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="027cd-206">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-207">Obračunana prodaja za novo količino</span><span class="sxs-lookup"><span data-stu-id="027cd-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="027cd-208">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-209">Neobračunana prodaja – obračuna se za razliko</span><span class="sxs-lookup"><span data-stu-id="027cd-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="027cd-210">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="027cd-211">**Vir pripada organizacijski enoti, ki se razlikuje od pogodbene enote projekta**</span><span class="sxs-lookup"><span data-stu-id="027cd-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="027cd-212">Dogodek</span><span class="sxs-lookup"><span data-stu-id="027cd-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="027cd-213">Obračunan ali prodan projekt</span><span class="sxs-lookup"><span data-stu-id="027cd-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="027cd-214">Projekt v fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="027cd-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="027cd-215">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="027cd-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="027cd-216">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="027cd-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="027cd-217">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="027cd-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="027cd-218">Opravljeno delo</span><span class="sxs-lookup"><span data-stu-id="027cd-218">Actuals</span></span></th>
<th><span data-ttu-id="027cd-219">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="027cd-219">Transaction currency</span></span></th>
<th><span data-ttu-id="027cd-220">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="027cd-220">Fixed price</span></span></th>
<th><span data-ttu-id="027cd-221">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="027cd-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="027cd-222">Ustvari se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="027cd-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="027cd-223">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="027cd-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-224">Pošlje se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="027cd-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="027cd-225">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="027cd-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="027cd-226">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="027cd-227">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-227">Cost actual</span></span></td>
<td><span data-ttu-id="027cd-228">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="027cd-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="027cd-229">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="027cd-230">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="027cd-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="027cd-231">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="027cd-232">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-233">Dejanska neobračunana prodaja – za obračunavanje</span><span class="sxs-lookup"><span data-stu-id="027cd-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="027cd-234">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-235">Cena enote vira</span><span class="sxs-lookup"><span data-stu-id="027cd-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="027cd-236">Valuta enote vira</span><span class="sxs-lookup"><span data-stu-id="027cd-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-237">Prodaja znotraj organizacije</span><span class="sxs-lookup"><span data-stu-id="027cd-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="027cd-238">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="027cd-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="027cd-239">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="027cd-240">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-240">Cost actual</span></span></td>
<td><span data-ttu-id="027cd-241">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="027cd-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="027cd-242">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="027cd-243">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="027cd-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="027cd-244">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="027cd-245">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="027cd-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-246">Cena enote vira</span><span class="sxs-lookup"><span data-stu-id="027cd-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="027cd-247">Valuta enote vira</span><span class="sxs-lookup"><span data-stu-id="027cd-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-248">Prodaja znotraj organizacije</span><span class="sxs-lookup"><span data-stu-id="027cd-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="027cd-249">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="027cd-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-250">Dejanska neobračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="027cd-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="027cd-251">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-252">Dejanska neobračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="027cd-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="027cd-253">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="027cd-254">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="027cd-255">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="027cd-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="027cd-256">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="027cd-257">Obračunana prodaja za mejnik</span><span class="sxs-lookup"><span data-stu-id="027cd-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="027cd-258">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="027cd-259">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="027cd-260">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-261">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="027cd-261">Billed sales</span></span></td>
<td><span data-ttu-id="027cd-262">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="027cd-263">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="027cd-264">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="027cd-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="027cd-265">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-266">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-267">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-268">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="027cd-269">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-270">Obračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="027cd-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="027cd-271">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-272">Obračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="027cd-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="027cd-273">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="027cd-274">Račun je popravljen s povečano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="027cd-275">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="027cd-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="027cd-276">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="027cd-277">Storniranje obračunane prodaje za mejnik</span><span class="sxs-lookup"><span data-stu-id="027cd-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="027cd-278">Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></span><span class="sxs-lookup"><span data-stu-id="027cd-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="027cd-279">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="027cd-280">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="027cd-281">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="027cd-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-282">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="027cd-282">Billed sales</span></span></td>
<td><span data-ttu-id="027cd-283">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="027cd-284">Račun je popravljen z zmanjšano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="027cd-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="027cd-285">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="027cd-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="027cd-286">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-287">Obračunana prodaja za novo količino</span><span class="sxs-lookup"><span data-stu-id="027cd-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="027cd-288">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="027cd-289">Neobračunana prodaja – obračuna se za razliko</span><span class="sxs-lookup"><span data-stu-id="027cd-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="027cd-290">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="027cd-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
