---
title: Domača stran dejanskih vrednosti
description: Ta tema vsebuje informacije o delu z dejanskimi vrednostmi v storitvi Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907338"
---
# <a name="actuals"></a><span data-ttu-id="9fe43-103">Dejanske vrednosti</span><span class="sxs-lookup"><span data-stu-id="9fe43-103">Actuals</span></span>

<span data-ttu-id="9fe43-104">_**Velja za:** za scenarije v storitvi Project Operations, ki temeljijo na virih/brez zaloge_</span><span class="sxs-lookup"><span data-stu-id="9fe43-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9fe43-105">Dejanski podatki se nanašajo na količino dela, ki je bilo opravljeno za projekt.</span><span class="sxs-lookup"><span data-stu-id="9fe43-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="9fe43-106">Ustvarjeni so kot rezultat vnosov časa in stroškov ter dnevniških vnosov in računov.</span><span class="sxs-lookup"><span data-stu-id="9fe43-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="9fe43-107">Vrstice dnevnikov in vnos časa</span><span class="sxs-lookup"><span data-stu-id="9fe43-107">Journal lines and time submission</span></span>

<span data-ttu-id="9fe43-108">Za več informacij o vnosu časa glejte [Pregled vnosa časa](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9fe43-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="9fe43-109">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="9fe43-109">Time and materials</span></span>

<span data-ttu-id="9fe43-110">Ko je predloženi vnos časa, povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in material, sta v sistemu ustvarita dve vrstici dnevnika, ena za ceno in druga za neobračunano prodajo.</span><span class="sxs-lookup"><span data-stu-id="9fe43-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="9fe43-111">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-111">Fixed price</span></span>

<span data-ttu-id="9fe43-112">Ko je poslan časovni vnos za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se v sistemu ustvari samo vrstica dnevnika za ceno.</span><span class="sxs-lookup"><span data-stu-id="9fe43-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="9fe43-113">Privzete cene</span><span class="sxs-lookup"><span data-stu-id="9fe43-113">Default pricing</span></span>

<span data-ttu-id="9fe43-114">Logika za oblikovanje privzetih cen se nahaja v vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="9fe43-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="9fe43-115">Vrednosti polj iz časovnega vnosa se kopirajo v vrstico dnevnika.</span><span class="sxs-lookup"><span data-stu-id="9fe43-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="9fe43-116">Te vrednosti vključujejo datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in rezultat valute v skladu z ustreznim cenikom.</span><span class="sxs-lookup"><span data-stu-id="9fe43-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="9fe43-117">Polja, ki vplivajo na privzete cene, kot sta **Vloga** in **Organizacijska enota**, se uporabljajo za določanje ustrezne cene v vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="9fe43-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="9fe43-118">Časovnemu vnosu lahko dodate polje po meri.</span><span class="sxs-lookup"><span data-stu-id="9fe43-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="9fe43-119">Če za časovni vnos dodate polje po meri in želite, da se vrednost polja razširi na dejanske vrednosti, ustvarite polje v entiteti »Dejanske vrednosti« in za kopiranje polja iz časovnega vnosa v dejanske vrednosti uporabite preslikave polj.</span><span class="sxs-lookup"><span data-stu-id="9fe43-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="9fe43-120">Oddaja vrstic dnevnika in osnovnih stroškov</span><span class="sxs-lookup"><span data-stu-id="9fe43-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="9fe43-121">Za več informacij o vnosu stroškov glejte [Pregled stroškov](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9fe43-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="9fe43-122">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="9fe43-122">Time and materials</span></span>

<span data-ttu-id="9fe43-123">Ko je vnos osnovnega stiška, povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in material, se v sistemu ustvarita dve vrstici dnevnika, ena za ceno in druga za neobračunano prodajo.</span><span class="sxs-lookup"><span data-stu-id="9fe43-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="9fe43-124">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-124">Fixed price</span></span>

<span data-ttu-id="9fe43-125">Ko je poslan osnovni strošek za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se v sistemu ustvari samo vrstica dnevnika za ceno.</span><span class="sxs-lookup"><span data-stu-id="9fe43-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="9fe43-126">Privzete cene</span><span class="sxs-lookup"><span data-stu-id="9fe43-126">Default pricing</span></span>

<span data-ttu-id="9fe43-127">Logika vnosa privzetih cen za stroške temelji na kategoriji stroškov.</span><span class="sxs-lookup"><span data-stu-id="9fe43-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="9fe43-128">Datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in valuta se uporabijo za ugotavljanje ustreznega cenika.</span><span class="sxs-lookup"><span data-stu-id="9fe43-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="9fe43-129">Vendar pa je za ceno znesek, ki ga je uporabnik vnesel, privzeto nastavljen neposredno v povezani vrstici dnevnika stroškov za strošek in prodajo.</span><span class="sxs-lookup"><span data-stu-id="9fe43-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="9fe43-130">Vnos privzetih cen na enoto na podlagi kategorije za vnose stroška ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="9fe43-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="9fe43-131">Uporaba dnevnikov vnosov za zapisovanje stroškov</span><span class="sxs-lookup"><span data-stu-id="9fe43-131">Use entry journals to record costs</span></span>

<span data-ttu-id="9fe43-132">V dnevnike lahko beležite stroške ali prihodke v razredih transakcij za material, dajatve, čas, stroške ali davke.</span><span class="sxs-lookup"><span data-stu-id="9fe43-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="9fe43-133">Dnevniki se lahko uporabljajo v naslednje namene:</span><span class="sxs-lookup"><span data-stu-id="9fe43-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="9fe43-134">Beleženje dejanskih stroškov materiala in prodaje za posamezen projekt.</span><span class="sxs-lookup"><span data-stu-id="9fe43-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="9fe43-135">Prenos dejanskih vrednosti o transakcijah iz drugega sistema v storitev Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9fe43-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="9fe43-136">Beleženje stroškov, ki so nastali v drugem sistemu.</span><span class="sxs-lookup"><span data-stu-id="9fe43-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="9fe43-137">Ti stroški lahko vključujejo stroške naročanja ali podizvajanja.</span><span class="sxs-lookup"><span data-stu-id="9fe43-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fe43-138">Aplikacija ne preveri veljavnosti vrste vrstice dnevnika ali povezanih cen, ki so vnesene v vrstico dnevnika.</span><span class="sxs-lookup"><span data-stu-id="9fe43-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="9fe43-139">Zato mora dnevnike vnosov za ustvarjanje dejanskih vrednosti uporabljati oseba, ki se popolnoma zaveda računovodskega vpliva dejanskih vrednosti na projekt.</span><span class="sxs-lookup"><span data-stu-id="9fe43-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="9fe43-140">Zaradi vpliva te vrste dnevnika morate skrbno izbrati, kdo ima dostop do ustvarjanja dnevnikov vnosov.</span><span class="sxs-lookup"><span data-stu-id="9fe43-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="9fe43-141">Zapisovanje dejanskih vrednosti na podlagi projektnih dogodkov</span><span class="sxs-lookup"><span data-stu-id="9fe43-141">Record actuals based on project events</span></span>

<span data-ttu-id="9fe43-142">Aplikacija Project Operations beleži finančne transakcije, do katerih pride med projektom.</span><span class="sxs-lookup"><span data-stu-id="9fe43-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="9fe43-143">Te transakcije se zapišejo kot dejanske vrednosti.</span><span class="sxs-lookup"><span data-stu-id="9fe43-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="9fe43-144">V spodnjih tabelah so prikazane različne vrste dejanskih vrednosti, ki so ustvarjene, glede na to, ali gre za časovne in materialne transakcije ali transakcije s fiksno ceno ali gre za stopnjo pred prodajo oziroma interni projekt.</span><span class="sxs-lookup"><span data-stu-id="9fe43-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="9fe43-145">Vir pripada isti organizacijski enoti kot pogodbena enota projekta</span><span class="sxs-lookup"><span data-stu-id="9fe43-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="9fe43-146">Dogodek</span><span class="sxs-lookup"><span data-stu-id="9fe43-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="9fe43-147">Obračunan ali prodan projekt</span><span class="sxs-lookup"><span data-stu-id="9fe43-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="9fe43-148">Projekt v fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="9fe43-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="9fe43-149">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="9fe43-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="9fe43-150">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="9fe43-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="9fe43-151">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9fe43-152">Opravljeno delo</span><span class="sxs-lookup"><span data-stu-id="9fe43-152">Actuals</span></span></th>
<th><span data-ttu-id="9fe43-153">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="9fe43-153">Transaction currency</span></span></th>
<th><span data-ttu-id="9fe43-154">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-154">Fixed price</span></span></th>
<th><span data-ttu-id="9fe43-155">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="9fe43-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe43-156">Ustvari se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="9fe43-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="9fe43-157">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="9fe43-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-158">Pošlje se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="9fe43-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="9fe43-159">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="9fe43-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9fe43-160">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9fe43-161">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-161">Cost actual</span></span></td>
<td><span data-ttu-id="9fe43-162">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="9fe43-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9fe43-163">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="9fe43-164">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="9fe43-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="9fe43-165">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="9fe43-166">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-167">Dejanska neobračunana prodaja – za obračunavanje</span><span class="sxs-lookup"><span data-stu-id="9fe43-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="9fe43-168">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9fe43-169">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9fe43-170">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-170">Cost actual</span></span></td>
<td><span data-ttu-id="9fe43-171">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="9fe43-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-172">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-173">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="9fe43-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-174">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-175">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-176">Dejanska neobračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="9fe43-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9fe43-177">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-178">Dejanska neobračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="9fe43-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fe43-179">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9fe43-180">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9fe43-181">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="9fe43-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9fe43-182">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9fe43-183">Obračunana prodaja za mejnik</span><span class="sxs-lookup"><span data-stu-id="9fe43-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="9fe43-184">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9fe43-185">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="9fe43-186">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-187">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="9fe43-187">Billed sales</span></span></td>
<td><span data-ttu-id="9fe43-188">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9fe43-189">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9fe43-190">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="9fe43-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9fe43-191">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-192">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-193">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-194">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-195">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-196">Obračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="9fe43-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9fe43-197">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-198">Obračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="9fe43-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fe43-199">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9fe43-200">Račun je popravljen s povečano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9fe43-201">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="9fe43-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9fe43-202">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="9fe43-203">Storniranje obračunane prodaje za mejnik</span><span class="sxs-lookup"><span data-stu-id="9fe43-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="9fe43-204">Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></span><span class="sxs-lookup"><span data-stu-id="9fe43-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="9fe43-205">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9fe43-206">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="9fe43-207">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-208">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="9fe43-208">Billed sales</span></span></td>
<td><span data-ttu-id="9fe43-209">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9fe43-210">Račun je popravljen z zmanjšano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9fe43-211">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="9fe43-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9fe43-212">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-213">Obračunana prodaja za novo količino</span><span class="sxs-lookup"><span data-stu-id="9fe43-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="9fe43-214">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-215">Neobračunana prodaja – obračuna se za razliko</span><span class="sxs-lookup"><span data-stu-id="9fe43-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fe43-216">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="9fe43-217">Vir pripada organizacijski enoti, ki se razlikuje od pogodbene enote projekta</span><span class="sxs-lookup"><span data-stu-id="9fe43-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="9fe43-218">Dogodek</span><span class="sxs-lookup"><span data-stu-id="9fe43-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="9fe43-219">Obračunan ali prodan projekt</span><span class="sxs-lookup"><span data-stu-id="9fe43-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="9fe43-220">Projekt v fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="9fe43-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="9fe43-221">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="9fe43-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="9fe43-222">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="9fe43-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="9fe43-223">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9fe43-224">Opravljeno delo</span><span class="sxs-lookup"><span data-stu-id="9fe43-224">Actuals</span></span></th>
<th><span data-ttu-id="9fe43-225">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="9fe43-225">Transaction currency</span></span></th>
<th><span data-ttu-id="9fe43-226">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-226">Fixed price</span></span></th>
<th><span data-ttu-id="9fe43-227">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="9fe43-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe43-228">Ustvari se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="9fe43-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="9fe43-229">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="9fe43-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-230">Pošlje se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="9fe43-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="9fe43-231">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="9fe43-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="9fe43-232">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9fe43-233">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-233">Cost actual</span></span></td>
<td><span data-ttu-id="9fe43-234">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="9fe43-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="9fe43-235">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="9fe43-236">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="9fe43-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="9fe43-237">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="9fe43-238">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-239">Dejanska neobračunana prodaja – za obračunavanje</span><span class="sxs-lookup"><span data-stu-id="9fe43-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="9fe43-240">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-241">Cena enote vira</span><span class="sxs-lookup"><span data-stu-id="9fe43-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="9fe43-242">Valuta enote vira</span><span class="sxs-lookup"><span data-stu-id="9fe43-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-243">Prodaja znotraj organizacije</span><span class="sxs-lookup"><span data-stu-id="9fe43-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="9fe43-244">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="9fe43-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="9fe43-245">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9fe43-246">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-246">Cost actual</span></span></td>
<td><span data-ttu-id="9fe43-247">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="9fe43-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9fe43-248">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="9fe43-249">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="9fe43-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9fe43-250">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="9fe43-251">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="9fe43-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-252">Cena enote vira</span><span class="sxs-lookup"><span data-stu-id="9fe43-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="9fe43-253">Valuta enote vira</span><span class="sxs-lookup"><span data-stu-id="9fe43-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-254">Prodaja znotraj organizacije</span><span class="sxs-lookup"><span data-stu-id="9fe43-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="9fe43-255">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="9fe43-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-256">Dejanska neobračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="9fe43-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9fe43-257">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-258">Dejanska neobračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="9fe43-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fe43-259">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9fe43-260">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9fe43-261">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="9fe43-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9fe43-262">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9fe43-263">Obračunana prodaja za mejnik</span><span class="sxs-lookup"><span data-stu-id="9fe43-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="9fe43-264">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9fe43-265">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="9fe43-266">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-267">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="9fe43-267">Billed sales</span></span></td>
<td><span data-ttu-id="9fe43-268">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9fe43-269">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9fe43-270">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="9fe43-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9fe43-271">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-272">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-273">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-274">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fe43-275">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-276">Obračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="9fe43-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9fe43-277">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-278">Obračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="9fe43-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fe43-279">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9fe43-280">Račun je popravljen s povečano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9fe43-281">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="9fe43-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9fe43-282">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="9fe43-283">Storniranje obračunane prodaje za mejnik</span><span class="sxs-lookup"><span data-stu-id="9fe43-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="9fe43-284">Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></span><span class="sxs-lookup"><span data-stu-id="9fe43-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="9fe43-285">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9fe43-286">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="9fe43-287">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="9fe43-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-288">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="9fe43-288">Billed sales</span></span></td>
<td><span data-ttu-id="9fe43-289">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9fe43-290">Račun je popravljen z zmanjšano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="9fe43-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9fe43-291">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="9fe43-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9fe43-292">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-293">Obračunana prodaja za novo količino</span><span class="sxs-lookup"><span data-stu-id="9fe43-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="9fe43-294">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe43-295">Neobračunana prodaja – obračuna se za razliko</span><span class="sxs-lookup"><span data-stu-id="9fe43-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fe43-296">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="9fe43-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
