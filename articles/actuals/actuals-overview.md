---
title: Dejanske vrednosti
description: Ta tema vsebuje informacije o delu z dejanskimi vrednostmi v aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996631"
---
# <a name="actuals"></a><span data-ttu-id="f8404-103">Dejanske vrednosti</span><span class="sxs-lookup"><span data-stu-id="f8404-103">Actuals</span></span> 

<span data-ttu-id="f8404-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="f8404-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f8404-105">Dejanske vrednosti predstavljajo pregledane in odobrene finančne in časovne napredke projekta.</span><span class="sxs-lookup"><span data-stu-id="f8404-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="f8404-106">Ustvarijo se kot rezultat odobritve časa, stroškov, vnosov porabe materiala ter vknjižb in računov.</span><span class="sxs-lookup"><span data-stu-id="f8404-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="f8404-107">Vrstice dnevnikov in vnos časa</span><span class="sxs-lookup"><span data-stu-id="f8404-107">Journal lines and time submission</span></span>

<span data-ttu-id="f8404-108">Za več informacij o vnosu časa glejte [Pregled vnosa časa](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f8404-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="f8404-109">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="f8404-109">Time and materials</span></span>

<span data-ttu-id="f8404-110">Ko je predloženi vnos časa, povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in material, sta v sistemu ustvarita dve vrstici dnevnika, ena za ceno in druga za neobračunano prodajo.</span><span class="sxs-lookup"><span data-stu-id="f8404-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="f8404-111">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="f8404-111">Fixed price</span></span>

<span data-ttu-id="f8404-112">Ko je poslan časovni vnos za projekt, ki je preslikan v podrobnosti pogodbe za fiksno ceno, se v sistemu ustvari samo vrstica dnevnika za ceno.</span><span class="sxs-lookup"><span data-stu-id="f8404-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="f8404-113">Privzete cene</span><span class="sxs-lookup"><span data-stu-id="f8404-113">Default pricing</span></span>

<span data-ttu-id="f8404-114">Logika za oblikovanje privzetih cen se nahaja v vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="f8404-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="f8404-115">Vrednosti polj iz časovnega vnosa se kopirajo v vrstico dnevnika.</span><span class="sxs-lookup"><span data-stu-id="f8404-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="f8404-116">Te vrednosti vključujejo datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in rezultat valute v skladu z ustreznim cenikom.</span><span class="sxs-lookup"><span data-stu-id="f8404-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="f8404-117">Polja, ki vplivajo na privzete cene, kot sta **Vloga** in **Enota vira**, se uporabljajo za določanje ustrezne cene v vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="f8404-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="f8404-118">Časovnemu vnosu lahko dodate polje po meri.</span><span class="sxs-lookup"><span data-stu-id="f8404-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="f8404-119">Če želite, da se vrednost polja razširi na dejanske vrednosti, ustvarite polje v tabelah **Dejanske vrednosti** in **Vrstica dnevnika**.</span><span class="sxs-lookup"><span data-stu-id="f8404-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="f8404-120">Uporabite kodo po meri, da z izvori transakcij prek vrstice dnevnika razširite izbrane vrednosti polja iz časovnega vnosa v dejanske podatke.</span><span class="sxs-lookup"><span data-stu-id="f8404-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="f8404-121">Za več informacij o izvoru in povezavah transakcij in glejte stran [Povezava dejanskih podatkov z izvirnimi zapisi](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="f8404-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="f8404-122">Oddaja vrstic dnevnika in osnovnih stroškov</span><span class="sxs-lookup"><span data-stu-id="f8404-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="f8404-123">Za več informacij o vnosu stroškov glejte [Pregled stroškov](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f8404-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="f8404-124">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="f8404-124">Time and materials</span></span>

<span data-ttu-id="f8404-125">Ko je vnos osnovnega stiška, povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in material, se v sistemu ustvarita dve vrstici dnevnika, ena za ceno in druga za neobračunano prodajo.</span><span class="sxs-lookup"><span data-stu-id="f8404-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="f8404-126">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="f8404-126">Fixed price</span></span>

<span data-ttu-id="f8404-127">Ko je poslan vnos osnovnega stroška povezan s projektom, ki je preslikan v podrobnosti pogodbe za fiksno ceno, sistem ustvari eno vrstico dnevnika za ceno.</span><span class="sxs-lookup"><span data-stu-id="f8404-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="f8404-128">Privzete cene</span><span class="sxs-lookup"><span data-stu-id="f8404-128">Default pricing</span></span>

<span data-ttu-id="f8404-129">Logika vnosa privzetih cen za stroške temelji na kategoriji stroškov.</span><span class="sxs-lookup"><span data-stu-id="f8404-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="f8404-130">Datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in valuta se uporabijo za ugotavljanje ustreznega cenika.</span><span class="sxs-lookup"><span data-stu-id="f8404-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="f8404-131">Polja, ki vplivajo na privzete cene, kot sta **Kategorija transakcija** in **Enota vira**, se uporabljajo za določanje ustrezne cene v vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="f8404-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="f8404-132">Vendar to deluje le, če je v ceniku navedena metoda določanja cen **cena na enoto**.</span><span class="sxs-lookup"><span data-stu-id="f8404-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="f8404-133">Če je metoda določanja cen **nabavna cena** ali **pribitek na ceno**, se za stroške uporabi cena, vnesena ob ustvarjanju vnosa stroškov, cena v vrstici dnevnika prodaje pa se izračuna na podlagi metode določanja cen.</span><span class="sxs-lookup"><span data-stu-id="f8404-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="f8404-134">Vnosu stroškov lahko dodate polje po meri.</span><span class="sxs-lookup"><span data-stu-id="f8404-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="f8404-135">Če želite, da se vrednost polja razširi na dejanske vrednosti, ustvarite polje v tabelah **Dejanske vrednosti** in **Vrstica dnevnika**.</span><span class="sxs-lookup"><span data-stu-id="f8404-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="f8404-136">Uporabite kodo po meri, da z izvori transakcij prek vrstice dnevnika razširite izbrane vrednosti polja iz časovnega vnosa v dejanske podatke.</span><span class="sxs-lookup"><span data-stu-id="f8404-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="f8404-137">Za več informacij o izvoru in povezavah transakcij in glejte stran [Povezava dejanskih podatkov z izvirnimi zapisi](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="f8404-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="f8404-138">Vrstice dnevnika in oddaja dnevnika uporabe materiala</span><span class="sxs-lookup"><span data-stu-id="f8404-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="f8404-139">Za več informacij o vnosu stroškov glejte stran [Dnevnik uporabe materiala](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="f8404-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="f8404-140">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="f8404-140">Time and materials</span></span>

<span data-ttu-id="f8404-141">Ko je poslan vnos v dnevnik uporabe materiala povezan s projektom, ki je preslikan v podrobnosti pogodbe za čas in materiale, sistem ustvari dve vrstici dnevnika, eno za stroške in drugo za neobračunano prodajo.</span><span class="sxs-lookup"><span data-stu-id="f8404-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="f8404-142">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="f8404-142">Fixed price</span></span>

<span data-ttu-id="f8404-143">Ko je poslan vnos v dnevnik uporabe materiala povezan s projektom, ki je preslikan v podrobnosti pogodbe za fiksno ceno, sistem ustvari eno vrstico dnevnika za ceno.</span><span class="sxs-lookup"><span data-stu-id="f8404-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="f8404-144">Privzete cene</span><span class="sxs-lookup"><span data-stu-id="f8404-144">Default pricing</span></span>

<span data-ttu-id="f8404-145">Logika za vnos privzetih cen materiala temelji na kombinaciji izdelka in enote.</span><span class="sxs-lookup"><span data-stu-id="f8404-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="f8404-146">Datum transakcije, podrobnosti pogodbe, v katero je projekt preslikan, in valuta se uporabijo za ugotavljanje ustreznega cenika.</span><span class="sxs-lookup"><span data-stu-id="f8404-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="f8404-147">Polja, ki vplivajo na privzete cene, kot sta **ID izdelka** in **Enota vira**, se uporabljajo za določanje ustrezne cene v vrstici dnevnika.</span><span class="sxs-lookup"><span data-stu-id="f8404-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="f8404-148">Vendar to deluje samo za izdelke iz kataloga.</span><span class="sxs-lookup"><span data-stu-id="f8404-148">However, this only works for catalog products.</span></span> <span data-ttu-id="f8404-149">Za izdelke, ki niso v katalogu, se za stroške in prodajno ceno v vrsticah dnevnika uporablja cena, vnesena ob ustvarjanju vnosa v dnevnik uporabe materiala.</span><span class="sxs-lookup"><span data-stu-id="f8404-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="f8404-150">Vnosu v **dnevnik uporabe materiala** lahko dodate polje po meri.</span><span class="sxs-lookup"><span data-stu-id="f8404-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="f8404-151">Če želite, da se vrednost polja razširi na dejanske vrednosti, ustvarite polje v tabelah **Dejanske vrednosti** in **Vrstica dnevnika**.</span><span class="sxs-lookup"><span data-stu-id="f8404-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="f8404-152">Uporabite kodo po meri, da z izvori transakcij prek vrstice dnevnika razširite izbrane vrednosti polja iz časovnega vnosa v dejanske podatke.</span><span class="sxs-lookup"><span data-stu-id="f8404-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="f8404-153">Za več informacij o izvoru in povezavah transakcij in glejte stran [Povezava dejanskih podatkov z izvirnimi zapisi](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="f8404-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="f8404-154">Uporaba dnevnikov vnosov za zapisovanje stroškov</span><span class="sxs-lookup"><span data-stu-id="f8404-154">Use entry journals to record costs</span></span>

<span data-ttu-id="f8404-155">V dnevnike lahko beležite stroške ali prihodke v razredih transakcij za material, dajatve, čas, stroške ali davke.</span><span class="sxs-lookup"><span data-stu-id="f8404-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="f8404-156">Dnevniki se lahko uporabljajo v naslednje namene:</span><span class="sxs-lookup"><span data-stu-id="f8404-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="f8404-157">Dejanske podatke o transakciji prenesite iz drugega sistema v aplikacijo Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f8404-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="f8404-158">Beleženje stroškov, ki so nastali v drugem sistemu.</span><span class="sxs-lookup"><span data-stu-id="f8404-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="f8404-159">Ti stroški lahko vključujejo stroške naročanja ali podizvajanja.</span><span class="sxs-lookup"><span data-stu-id="f8404-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f8404-160">Aplikacija ne preveri veljavnosti vrste vrstice dnevnika ali povezanih cen, ki so vnesene v vrstico dnevnika.</span><span class="sxs-lookup"><span data-stu-id="f8404-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="f8404-161">Zato mora dnevnike vnosov za ustvarjanje dejanskih vrednosti uporabljati oseba, ki se popolnoma zaveda računovodskega vpliva dejanskih vrednosti na projekt.</span><span class="sxs-lookup"><span data-stu-id="f8404-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="f8404-162">Zaradi vpliva te vrste dnevnika morate skrbno izbrati, kdo ima dostop do ustvarjanja dnevnikov vnosov.</span><span class="sxs-lookup"><span data-stu-id="f8404-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="f8404-163">Zapisovanje dejanskih vrednosti na podlagi projektnih dogodkov</span><span class="sxs-lookup"><span data-stu-id="f8404-163">Record actuals based on project events</span></span>

<span data-ttu-id="f8404-164">Aplikacija Project Operations beleži finančne transakcije, do katerih pride med projektom.</span><span class="sxs-lookup"><span data-stu-id="f8404-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="f8404-165">Te transakcije se zapišejo kot dejanske vrednosti.</span><span class="sxs-lookup"><span data-stu-id="f8404-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="f8404-166">V spodnjih tabelah so prikazane različne vrste dejanskih vrednosti, ki so ustvarjene, glede na to, ali gre za časovne in materialne transakcije ali transakcije s fiksno ceno ali gre za stopnjo pred prodajo oziroma interni projekt.</span><span class="sxs-lookup"><span data-stu-id="f8404-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="f8404-167">Vir pripada isti organizacijski enoti kot pogodbena enota projekta</span><span class="sxs-lookup"><span data-stu-id="f8404-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f8404-168">Dogodek</span><span class="sxs-lookup"><span data-stu-id="f8404-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f8404-169">Obračunan ali prodan projekt</span><span class="sxs-lookup"><span data-stu-id="f8404-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f8404-170">Projekt v fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="f8404-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f8404-171">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="f8404-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f8404-172">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="f8404-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f8404-173">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="f8404-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f8404-174">Opravljeno delo</span><span class="sxs-lookup"><span data-stu-id="f8404-174">Actuals</span></span></th>
<th><span data-ttu-id="f8404-175">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="f8404-175">Transaction currency</span></span></th>
<th><span data-ttu-id="f8404-176">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="f8404-176">Fixed price</span></span></th>
<th><span data-ttu-id="f8404-177">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="f8404-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8404-178">Ustvari se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="f8404-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f8404-179">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="f8404-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-180">Pošlje se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="f8404-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f8404-181">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="f8404-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f8404-182">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f8404-183">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-183">Cost actual</span></span></td>
<td><span data-ttu-id="f8404-184">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="f8404-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f8404-185">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f8404-186">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="f8404-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="f8404-187">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f8404-188">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-189">Dejanska neobračunana prodaja – za obračunavanje</span><span class="sxs-lookup"><span data-stu-id="f8404-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f8404-190">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f8404-191">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f8404-192">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-192">Cost actual</span></span></td>
<td><span data-ttu-id="f8404-193">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="f8404-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-194">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-195">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="f8404-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-196">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-197">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-198">Dejanska neobračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="f8404-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f8404-199">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-200">Dejanska neobračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="f8404-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f8404-201">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f8404-202">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f8404-203">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="f8404-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f8404-204">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f8404-205">Obračunana prodaja za mejnik</span><span class="sxs-lookup"><span data-stu-id="f8404-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f8404-206">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f8404-207">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f8404-208">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-209">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="f8404-209">Billed sales</span></span></td>
<td><span data-ttu-id="f8404-210">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f8404-211">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f8404-212">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="f8404-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f8404-213">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-214">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-215">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-216">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-217">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-218">Obračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="f8404-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f8404-219">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-220">Obračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="f8404-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f8404-221">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f8404-222">Račun je popravljen s povečano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f8404-223">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="f8404-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f8404-224">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f8404-225">Storniranje obračunane prodaje za mejnik</span><span class="sxs-lookup"><span data-stu-id="f8404-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f8404-226">Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></span><span class="sxs-lookup"><span data-stu-id="f8404-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f8404-227">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f8404-228">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f8404-229">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-230">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="f8404-230">Billed sales</span></span></td>
<td><span data-ttu-id="f8404-231">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f8404-232">Račun je popravljen z zmanjšano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f8404-233">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="f8404-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f8404-234">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-235">Obračunana prodaja za novo količino</span><span class="sxs-lookup"><span data-stu-id="f8404-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f8404-236">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-237">Neobračunana prodaja – obračuna se za razliko</span><span class="sxs-lookup"><span data-stu-id="f8404-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f8404-238">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="f8404-239">Vir pripada organizacijski enoti, ki se razlikuje od pogodbene enote projekta</span><span class="sxs-lookup"><span data-stu-id="f8404-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f8404-240">Dogodek</span><span class="sxs-lookup"><span data-stu-id="f8404-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f8404-241">Obračunan ali prodan projekt</span><span class="sxs-lookup"><span data-stu-id="f8404-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f8404-242">Projekt v fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="f8404-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f8404-243">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="f8404-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f8404-244">Čas in materiali</span><span class="sxs-lookup"><span data-stu-id="f8404-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f8404-245">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="f8404-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f8404-246">Opravljeno delo</span><span class="sxs-lookup"><span data-stu-id="f8404-246">Actuals</span></span></th>
<th><span data-ttu-id="f8404-247">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="f8404-247">Transaction currency</span></span></th>
<th><span data-ttu-id="f8404-248">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="f8404-248">Fixed price</span></span></th>
<th><span data-ttu-id="f8404-249">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="f8404-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f8404-250">Ustvari se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="f8404-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f8404-251">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="f8404-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-252">Pošlje se časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="f8404-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f8404-253">V entitetah dejanskih podatkov ni dejavnosti</span><span class="sxs-lookup"><span data-stu-id="f8404-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="f8404-254">Čas je odobren in med odobritvijo ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f8404-255">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-255">Cost actual</span></span></td>
<td><span data-ttu-id="f8404-256">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="f8404-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f8404-257">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f8404-258">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="f8404-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f8404-259">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f8404-260">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-261">Dejanska neobračunana prodaja – za obračunavanje</span><span class="sxs-lookup"><span data-stu-id="f8404-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f8404-262">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-263">Cena enote vira</span><span class="sxs-lookup"><span data-stu-id="f8404-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f8404-264">Valuta enote vira</span><span class="sxs-lookup"><span data-stu-id="f8404-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-265">Prodaja znotraj organizacije</span><span class="sxs-lookup"><span data-stu-id="f8404-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f8404-266">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="f8404-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="f8404-267">Čas je odobren in med odobritvijo je prišlo pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f8404-268">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-268">Cost actual</span></span></td>
<td><span data-ttu-id="f8404-269">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="f8404-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f8404-270">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f8404-271">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="f8404-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f8404-272">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f8404-273">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f8404-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-274">Cena enote vira</span><span class="sxs-lookup"><span data-stu-id="f8404-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f8404-275">Valuta enote vira</span><span class="sxs-lookup"><span data-stu-id="f8404-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-276">Prodaja znotraj organizacije</span><span class="sxs-lookup"><span data-stu-id="f8404-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f8404-277">Valuta pogodbene enote</span><span class="sxs-lookup"><span data-stu-id="f8404-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-278">Dejanska neobračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="f8404-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f8404-279">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-280">Dejanska neobračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="f8404-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f8404-281">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f8404-282">Račun je potrjen in ni prišlo do spremembe ali povečanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f8404-283">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="f8404-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f8404-284">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f8404-285">Obračunana prodaja za mejnik</span><span class="sxs-lookup"><span data-stu-id="f8404-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f8404-286">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f8404-287">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f8404-288">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-289">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="f8404-289">Billed sales</span></span></td>
<td><span data-ttu-id="f8404-290">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f8404-291">Račun je potrjen in prišlo je do pomanjšanja števila ur za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f8404-292">Storniranje neobračunane prodaje</span><span class="sxs-lookup"><span data-stu-id="f8404-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f8404-293">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-294">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-295">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-296">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f8404-297">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-298">Obračunana prodaja – obračuna se za novo količino</span><span class="sxs-lookup"><span data-stu-id="f8404-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f8404-299">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-300">Obračunana prodaja – za razliko se ne obračuna</span><span class="sxs-lookup"><span data-stu-id="f8404-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f8404-301">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f8404-302">Račun je popravljen s povečano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f8404-303">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="f8404-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f8404-304">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f8404-305">Storniranje obračunane prodaje za mejnik</span><span class="sxs-lookup"><span data-stu-id="f8404-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f8404-306">Sprememba stanja mejnika s stanja <strong>Fakturirano</strong> na stanje <strong>Pripravljeno za izdajo računa</strong></span><span class="sxs-lookup"><span data-stu-id="f8404-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f8404-307">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f8404-308">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f8404-309">Ni na voljo</span><span class="sxs-lookup"><span data-stu-id="f8404-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-310">Obračunana prodaja</span><span class="sxs-lookup"><span data-stu-id="f8404-310">Billed sales</span></span></td>
<td><span data-ttu-id="f8404-311">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f8404-312">Račun je popravljen z zmanjšano količino za obračunavanje.</span><span class="sxs-lookup"><span data-stu-id="f8404-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f8404-313">Obračunana prodaja – storniranje</span><span class="sxs-lookup"><span data-stu-id="f8404-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f8404-314">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-315">Obračunana prodaja za novo količino</span><span class="sxs-lookup"><span data-stu-id="f8404-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f8404-316">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f8404-317">Neobračunana prodaja – obračuna se za razliko</span><span class="sxs-lookup"><span data-stu-id="f8404-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f8404-318">Valuta projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="f8404-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
