---
title: Dejanske vrednosti
description: Ta tema vsebuje informacije o delu z dejanskimi vrednostmi v aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291819"
---
# <a name="actuals"></a><span data-ttu-id="126a9-103">Dejanske vrednosti</span><span class="sxs-lookup"><span data-stu-id="126a9-103">Actuals</span></span> 

<span data-ttu-id="126a9-104">_**Velja za:** za scenarije v storitvi Project Operations, ki temeljijo na virih/brez zaloge_</span><span class="sxs-lookup"><span data-stu-id="126a9-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="126a9-105">Dejanski podatki se nanašajo na količino dela, ki je bilo opravljeno za projekt.</span><span class="sxs-lookup"><span data-stu-id="126a9-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="126a9-106">Ustvarjeni so kot rezultat vnosov časa in stroškov ter dnevniških vnosov in računov.</span><span class="sxs-lookup"><span data-stu-id="126a9-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="126a9-107">Vrstice dnevnikov in vnos časa</span><span class="sxs-lookup"><span data-stu-id="126a9-107">Journal lines and time submission</span></span>

<span data-ttu-id="126a9-108">Za več informacij o vnosu časa glejte [Pregled vnosa časa](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="126a9-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="126a9-109">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="126a9-109">Time and materials</span></span>

<span data-ttu-id="126a9-110">Ko je predloženi vnos časa, povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in material, sta v sistemu ustvarita dve vrstici dnevnika, ena za ceno in druga za neobračunano prodajo.</span><span class="sxs-lookup"><span data-stu-id="126a9-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="126a9-111">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="126a9-111">Fixed price</span></span>

<span data-ttu-id="126a9-112">Ko je poslan časovni vnos za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se v sistemu ustvari samo vrstica dnevnika za ceno.</span><span class="sxs-lookup"><span data-stu-id="126a9-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="126a9-113">Privzete cene</span><span class="sxs-lookup"><span data-stu-id="126a9-113">Default pricing</span></span>

<span data-ttu-id="126a9-114">Logika za oblikovanje privzetih cen se nahaja v vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="126a9-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="126a9-115">Vrednosti polj iz časovnega vnosa se kopirajo v vrstico dnevnika.</span><span class="sxs-lookup"><span data-stu-id="126a9-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="126a9-116">Te vrednosti vključujejo datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in rezultat valute v skladu z ustreznim cenikom.</span><span class="sxs-lookup"><span data-stu-id="126a9-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="126a9-117">Polja, ki vplivajo na privzete cene, kot sta **Vloga** in **Organizacijska enota**, se uporabljajo za določanje ustrezne cene v vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="126a9-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="126a9-118">Časovnemu vnosu lahko dodate polje po meri.</span><span class="sxs-lookup"><span data-stu-id="126a9-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="126a9-119">Če za časovni vnos dodate polje po meri in želite, da se vrednost polja razširi na dejanske vrednosti, ustvarite polje v entiteti »Dejanske vrednosti« in za kopiranje polja iz časovnega vnosa v dejanske vrednosti uporabite preslikave polj.</span><span class="sxs-lookup"><span data-stu-id="126a9-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="126a9-120">Oddaja vrstic dnevnika in osnovnih stroškov</span><span class="sxs-lookup"><span data-stu-id="126a9-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="126a9-121">Za več informacij o vnosu stroškov glejte [Pregled stroškov](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="126a9-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="126a9-122">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="126a9-122">Time and materials</span></span>

<span data-ttu-id="126a9-123">Ko je vnos osnovnega stiška, povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in material, se v sistemu ustvarita dve vrstici dnevnika, ena za ceno in druga za neobračunano prodajo.</span><span class="sxs-lookup"><span data-stu-id="126a9-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="126a9-124">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="126a9-124">Fixed price</span></span>

<span data-ttu-id="126a9-125">Ko je poslan osnovni strošek za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se v sistemu ustvari samo vrstica dnevnika za ceno.</span><span class="sxs-lookup"><span data-stu-id="126a9-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="126a9-126">Privzete cene</span><span class="sxs-lookup"><span data-stu-id="126a9-126">Default pricing</span></span>

<span data-ttu-id="126a9-127">Logika vnosa privzetih cen za stroške temelji na kategoriji stroškov.</span><span class="sxs-lookup"><span data-stu-id="126a9-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="126a9-128">Datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in valuta se uporabijo za ugotavljanje ustreznega cenika.</span><span class="sxs-lookup"><span data-stu-id="126a9-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="126a9-129">Vendar pa je za ceno znesek, ki ga je uporabnik vnesel, privzeto nastavljen neposredno v povezani vrstici dnevnika stroškov za strošek in prodajo.</span><span class="sxs-lookup"><span data-stu-id="126a9-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="126a9-130">Vnos privzetih cen na enoto na podlagi kategorije za vnose stroška ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="126a9-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="126a9-131">Uporaba dnevnikov vnosov za zapisovanje stroškov</span><span class="sxs-lookup"><span data-stu-id="126a9-131">Use entry journals to record costs</span></span>

<span data-ttu-id="126a9-132">V dnevnike lahko beležite stroške ali prihodke v razredih transakcij za material, dajatve, čas, stroške ali davke.</span><span class="sxs-lookup"><span data-stu-id="126a9-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="126a9-133">Dnevniki se lahko uporabljajo v naslednje namene:</span><span class="sxs-lookup"><span data-stu-id="126a9-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="126a9-134">Beleženje dejanskih stroškov materiala in prodaje za posamezen projekt.</span><span class="sxs-lookup"><span data-stu-id="126a9-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="126a9-135">Dejanske podatke o transakciji prenesite iz drugega sistema v aplikacijo Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="126a9-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="126a9-136">Beleženje stroškov, ki so nastali v drugem sistemu.</span><span class="sxs-lookup"><span data-stu-id="126a9-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="126a9-137">Ti stroški lahko vključujejo stroške naročanja ali podizvajanja.</span><span class="sxs-lookup"><span data-stu-id="126a9-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="126a9-138">Aplikacija ne preveri veljavnosti vrste vrstice dnevnika ali povezanih cen, ki so vnesene v vrstico dnevnika.</span><span class="sxs-lookup"><span data-stu-id="126a9-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="126a9-139">Zato mora dnevnike vnosov za ustvarjanje dejanskih vrednosti uporabljati oseba, ki se popolnoma zaveda računovodskega vpliva dejanskih vrednosti na projekt.</span><span class="sxs-lookup"><span data-stu-id="126a9-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="126a9-140">Zaradi vpliva te vrste dnevnika morate skrbno izbrati, kdo ima dostop do ustvarjanja dnevnikov vnosov.</span><span class="sxs-lookup"><span data-stu-id="126a9-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="126a9-141">Zapisovanje dejanskih vrednosti na podlagi projektnih dogodkov</span><span class="sxs-lookup"><span data-stu-id="126a9-141">Record actuals based on project events</span></span>

<span data-ttu-id="126a9-142">Aplikacija Project Operations beleži finančne transakcije, do katerih pride med projektom.</span><span class="sxs-lookup"><span data-stu-id="126a9-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="126a9-143">Te transakcije se zapišejo kot dejanske vrednosti.</span><span class="sxs-lookup"><span data-stu-id="126a9-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="126a9-144">V spodnjih tabelah so prikazane različne vrste dejanskih vrednosti, ki so ustvarjene, glede na to, ali gre za časovne in materialne transakcije ali transakcije s fiksno ceno ali gre za stopnjo pred prodajo oziroma interni projekt.</span><span class="sxs-lookup"><span data-stu-id="126a9-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="126a9-145">Vir pripada isti organizacijski enoti kot pogodbena enota projekta</span><span class="sxs-lookup"><span data-stu-id="126a9-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="126a9-146">Dogodek</span><span class="sxs-lookup"><span data-stu-id="126a9-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="126a9-147">Obračunan ali prodan projekt</span><span class="sxs-lookup"><span data-stu-id="126a9-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="126a9-148">Projekt v fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="126a9-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="126a9-149">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="126a9-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="126a9-150">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="126a9-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="126a9-151">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="126a9-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="126a9-152">Opravljeno delo</span><span class="sxs-lookup"><span data-stu-id="126a9-152">Actuals</span></span></th>
<th><span data-ttu-id="126a9-153">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="126a9-153">Transaction currency</span></span></th>
<th><span data-ttu-id="126a9-154">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="126a9-154">Fixed price</span></span></th>
<th><span data-ttu-id="126a9-155">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="126a9-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="126a9-156">Ustvari se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="126a9-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="126a9-157">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="126a9-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-158">Pošlje se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="126a9-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="126a9-159">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="126a9-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="126a9-160">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="126a9-161">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-161">Cost actual</span></span></td>
<td><span data-ttu-id="126a9-162">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="126a9-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="126a9-163">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="126a9-164">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="126a9-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="126a9-165">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="126a9-166">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-167">Dejanska neobračunana prodaja – za obračunavanje</span><span class="sxs-lookup"><span data-stu-id="126a9-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="126a9-168">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="126a9-169">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="126a9-170">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-170">Cost actual</span></span></td>
<td><span data-ttu-id="126a9-171">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="126a9-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-172">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-173">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="126a9-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-174">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-175">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-176">Dejanska neobračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="126a9-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="126a9-177">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-178">Dejanska neobračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="126a9-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="126a9-179">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="126a9-180">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="126a9-181">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="126a9-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="126a9-182">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="126a9-183">Obračunana prodaja za mejnik</span><span class="sxs-lookup"><span data-stu-id="126a9-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="126a9-184">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="126a9-185">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="126a9-186">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-187">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="126a9-187">Billed sales</span></span></td>
<td><span data-ttu-id="126a9-188">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="126a9-189">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="126a9-190">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="126a9-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="126a9-191">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-192">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-193">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-194">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-195">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-196">Obračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="126a9-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="126a9-197">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-198">Obračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="126a9-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="126a9-199">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="126a9-200">Račun je popravljen s povečano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="126a9-201">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="126a9-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="126a9-202">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="126a9-203">Storniranje obračunane prodaje za mejnik</span><span class="sxs-lookup"><span data-stu-id="126a9-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="126a9-204">Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></span><span class="sxs-lookup"><span data-stu-id="126a9-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="126a9-205">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="126a9-206">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="126a9-207">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-208">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="126a9-208">Billed sales</span></span></td>
<td><span data-ttu-id="126a9-209">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="126a9-210">Račun je popravljen z zmanjšano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="126a9-211">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="126a9-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="126a9-212">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-213">Obračunana prodaja za novo količino</span><span class="sxs-lookup"><span data-stu-id="126a9-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="126a9-214">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-215">Neobračunana prodaja – obračuna se za razliko</span><span class="sxs-lookup"><span data-stu-id="126a9-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="126a9-216">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="126a9-217">Vir pripada organizacijski enoti, ki se razlikuje od pogodbene enote projekta</span><span class="sxs-lookup"><span data-stu-id="126a9-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="126a9-218">Dogodek</span><span class="sxs-lookup"><span data-stu-id="126a9-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="126a9-219">Obračunan ali prodan projekt</span><span class="sxs-lookup"><span data-stu-id="126a9-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="126a9-220">Projekt v fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="126a9-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="126a9-221">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="126a9-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="126a9-222">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="126a9-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="126a9-223">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="126a9-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="126a9-224">Opravljeno delo</span><span class="sxs-lookup"><span data-stu-id="126a9-224">Actuals</span></span></th>
<th><span data-ttu-id="126a9-225">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="126a9-225">Transaction currency</span></span></th>
<th><span data-ttu-id="126a9-226">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="126a9-226">Fixed price</span></span></th>
<th><span data-ttu-id="126a9-227">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="126a9-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="126a9-228">Ustvari se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="126a9-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="126a9-229">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="126a9-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-230">Pošlje se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="126a9-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="126a9-231">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="126a9-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="126a9-232">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="126a9-233">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-233">Cost actual</span></span></td>
<td><span data-ttu-id="126a9-234">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="126a9-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="126a9-235">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="126a9-236">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="126a9-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="126a9-237">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="126a9-238">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-239">Dejanska neobračunana prodaja – za obračunavanje</span><span class="sxs-lookup"><span data-stu-id="126a9-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="126a9-240">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-241">Cena enote vira</span><span class="sxs-lookup"><span data-stu-id="126a9-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="126a9-242">Valuta enote vira</span><span class="sxs-lookup"><span data-stu-id="126a9-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-243">Prodaja znotraj organizacije</span><span class="sxs-lookup"><span data-stu-id="126a9-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="126a9-244">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="126a9-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="126a9-245">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="126a9-246">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-246">Cost actual</span></span></td>
<td><span data-ttu-id="126a9-247">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="126a9-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="126a9-248">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="126a9-249">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="126a9-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="126a9-250">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="126a9-251">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="126a9-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-252">Cena enote vira</span><span class="sxs-lookup"><span data-stu-id="126a9-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="126a9-253">Valuta enote vira</span><span class="sxs-lookup"><span data-stu-id="126a9-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-254">Prodaja znotraj organizacije</span><span class="sxs-lookup"><span data-stu-id="126a9-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="126a9-255">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="126a9-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-256">Dejanska neobračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="126a9-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="126a9-257">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-258">Dejanska neobračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="126a9-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="126a9-259">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="126a9-260">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="126a9-261">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="126a9-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="126a9-262">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="126a9-263">Obračunana prodaja za mejnik</span><span class="sxs-lookup"><span data-stu-id="126a9-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="126a9-264">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="126a9-265">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="126a9-266">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-267">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="126a9-267">Billed sales</span></span></td>
<td><span data-ttu-id="126a9-268">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="126a9-269">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="126a9-270">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="126a9-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="126a9-271">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-272">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-273">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-274">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="126a9-275">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-276">Obračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="126a9-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="126a9-277">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-278">Obračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="126a9-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="126a9-279">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="126a9-280">Račun je popravljen s povečano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="126a9-281">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="126a9-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="126a9-282">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="126a9-283">Storniranje obračunane prodaje za mejnik</span><span class="sxs-lookup"><span data-stu-id="126a9-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="126a9-284">Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></span><span class="sxs-lookup"><span data-stu-id="126a9-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="126a9-285">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="126a9-286">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="126a9-287">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="126a9-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-288">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="126a9-288">Billed sales</span></span></td>
<td><span data-ttu-id="126a9-289">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="126a9-290">Račun je popravljen z zmanjšano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="126a9-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="126a9-291">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="126a9-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="126a9-292">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-293">Obračunana prodaja za novo količino</span><span class="sxs-lookup"><span data-stu-id="126a9-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="126a9-294">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="126a9-295">Neobračunana prodaja – obračuna se za razliko</span><span class="sxs-lookup"><span data-stu-id="126a9-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="126a9-296">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="126a9-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]