---
title: Pregled podrobnosti ponudb, ki temeljijo na projektih
description: Ta tema vsebuje informacije o uporabi podrobnosti ponudb, ki temeljijo na projektih, za projektno delo.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e61a9fbf357123884397b930662d11f22bfdeaa0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277808"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="81cce-103">Pregled podrobnosti ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="81cce-103">Project-based quote lines overview</span></span>

<span data-ttu-id="81cce-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="81cce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="81cce-105">Podrobnosti ponudb, ki temeljijo na projektu, so oblikovane tako, da pripomorejo k oceni projektnega dela v okviru interakcije.</span><span class="sxs-lookup"><span data-stu-id="81cce-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="81cce-106">Struktura podrobnosti ponudb, ki temelji na projektu, je razširjena za ocene projektov z naslednjimi koncepti:</span><span class="sxs-lookup"><span data-stu-id="81cce-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="81cce-107">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="81cce-107">Billing Method</span></span>
- <span data-ttu-id="81cce-108">Preslikavanje projektov</span><span class="sxs-lookup"><span data-stu-id="81cce-108">Project Mapping</span></span>
- <span data-ttu-id="81cce-109">Vključuje razrede transakcij</span><span class="sxs-lookup"><span data-stu-id="81cce-109">Included Transaction classes</span></span>
- <span data-ttu-id="81cce-110">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="81cce-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="81cce-111">Nastavitev možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="81cce-111">Chargeability setup</span></span>
- <span data-ttu-id="81cce-112">Ocena z uporabo podrobnosti ponudb</span><span class="sxs-lookup"><span data-stu-id="81cce-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="81cce-113">Stranke podrobnosti ponudbe</span><span class="sxs-lookup"><span data-stu-id="81cce-113">Quote line Customers</span></span>

<span data-ttu-id="81cce-114">Naslednja tabela vsebuje informacije o poljih na zavihku **Splošno** pri podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="81cce-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="81cce-115">Ta polja pomagajo nastaviti osnovo za podrobno, temeljito oceno projektnega dela.</span><span class="sxs-lookup"><span data-stu-id="81cce-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="81cce-116">**Polje**</span><span class="sxs-lookup"><span data-stu-id="81cce-116">**Field**</span></span> | <span data-ttu-id="81cce-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="81cce-117">**Description**</span></span> | <span data-ttu-id="81cce-118">**Nadaljnji vpliv**</span><span class="sxs-lookup"><span data-stu-id="81cce-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="81cce-119">Imenu</span><span class="sxs-lookup"><span data-stu-id="81cce-119">Name</span></span> | <span data-ttu-id="81cce-120">Ime podrobnosti ponudbe, ki bi vam pomagala prepoznati ločeno komponento ponudbe, ki jo ocenjujete.</span><span class="sxs-lookup"><span data-stu-id="81cce-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="81cce-121">Kopirano v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="81cce-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="81cce-122">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="81cce-122">Billing Method</span></span> | <span data-ttu-id="81cce-123">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="81cce-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="81cce-124">To polje vključuje dva glavna pogodbena modela, ki sta podprta v aplikaciji Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="81cce-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="81cce-125">- fiksna cena</span><span class="sxs-lookup"><span data-stu-id="81cce-125">- Fixed price</span></span></br><span data-ttu-id="81cce-126">- čas in material</span><span class="sxs-lookup"><span data-stu-id="81cce-126">- Time and material.</span></span>| <span data-ttu-id="81cce-127">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="81cce-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="81cce-128">Project</span><span class="sxs-lookup"><span data-stu-id="81cce-128">Project</span></span> | <span data-ttu-id="81cce-129">S tem izbirnim poljem določite projekt, ki se bo uporabljal za izvedbo dela za to interakcijo.</span><span class="sxs-lookup"><span data-stu-id="81cce-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="81cce-130">Ko je projekt preslikan v podrobnost ponudbe, pripomore k nastavitvi opravil, ki se zaračunajo, in tudi k pripravi ocene, ki temelji na projektu, pri vrstici ponudbe v obliki podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="81cce-131">Če projekt ni preslikan na vrstico ponudbe, ki temelji na projektu, morate oceno ustvariti ročno z izdelavo vsake podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="81cce-132">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="81cce-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="81cce-133">Vključi čas</span><span class="sxs-lookup"><span data-stu-id="81cce-133">Include Time</span></span> | <span data-ttu-id="81cce-134">Zastava **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="81cce-135">Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="81cce-136">Vrednost **Da** označuje, da bodo časovne transakcije ali stroški dela vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="81cce-137">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="81cce-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="81cce-138">Vključi strošek</span><span class="sxs-lookup"><span data-stu-id="81cce-138">Include Expense</span></span> | <span data-ttu-id="81cce-139">Zastava **Da**/**Ne** označuje, ali bodo stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="81cce-140">Vrednost **Ne** označuje, da strošek ne bo vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="81cce-141">Vrednost **Ne** označuje, da bo strošek vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="81cce-142">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="81cce-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="81cce-143">Vključi dajatev</span><span class="sxs-lookup"><span data-stu-id="81cce-143">Include Fee</span></span> | <span data-ttu-id="81cce-144">Zastava **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="81cce-145">Vrednost **Ne** označuje, da dajatve ne bodo vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="81cce-146">Vrednost **Da** označuje, da bodo dajatve vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="81cce-147">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="81cce-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="81cce-148">Znesek ponudbe</span><span class="sxs-lookup"><span data-stu-id="81cce-148">Quoted Amount</span></span> | <span data-ttu-id="81cce-149">To je znesek, ki bo stranki podan v ponudbi za vso delo, napovedano v tej podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="81cce-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="81cce-150">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz polja **Proračun stranke** v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="81cce-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="81cce-151">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="81cce-152">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="81cce-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="81cce-153">Predvideni davek</span><span class="sxs-lookup"><span data-stu-id="81cce-153">Estimated Tax</span></span> | <span data-ttu-id="81cce-154">To je polje, ki ga je mogoče urejati in v katerem lahko uporabnik doda predviden znesek davka v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="81cce-155">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska davka v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="81cce-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="81cce-156">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="81cce-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="81cce-157">Znesek ponudbe po obdavčitvi</span><span class="sxs-lookup"><span data-stu-id="81cce-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="81cce-158">To polje je znesek v podrobnosti ponudbe po obdavčitvi in je samo za branje.</span><span class="sxs-lookup"><span data-stu-id="81cce-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="81cce-159">Znesek v tem polju se izračuna kot *znesek ponudbe + davek*.</span><span class="sxs-lookup"><span data-stu-id="81cce-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="81cce-160">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="81cce-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="81cce-161">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="81cce-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="81cce-162">To polje je mogoče urejati in je na voljo samo v podrobnostih ponudb, ki temeljijo na projektih in imajo način obračunavanja **Čas in material**.</span><span class="sxs-lookup"><span data-stu-id="81cce-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="81cce-163">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="81cce-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="81cce-164">Proračun stranke</span><span class="sxs-lookup"><span data-stu-id="81cce-164">Customer Budget</span></span> | <span data-ttu-id="81cce-165">To polje je mogoče urejati in se kopira iz ustreznega polja v vrstici priložnosti, če je bila ponudba ustvarjena iz priložnosti.</span><span class="sxs-lookup"><span data-stu-id="81cce-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="81cce-166">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="81cce-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="81cce-167">Pravila za preverjanje veljavnosti polj na zavihku Splošno v podrobnostih ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="81cce-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="81cce-168">**1. pravilo**: določen razred transakcije v izbranem projektu je mogoče vključiti samo v eno podrobnost ponudbe, ki temelji na projektih.</span><span class="sxs-lookup"><span data-stu-id="81cce-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="81cce-169">**2. pravilo** : če ima priložnost več ponudb, so lahko podrobnosti ponudbe za različne ponudbe, ki se vse sklicujejo na isti projekt in vključujejo isti razred transakcije.</span><span class="sxs-lookup"><span data-stu-id="81cce-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="81cce-170">**3. pravilo**: če ponudbe ne pripadajo isti priložnosti, ne morejo vključevati istega projekta in razreda transakcije.</span><span class="sxs-lookup"><span data-stu-id="81cce-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="81cce-171">
                    <strong>Priložnost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81cce-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="81cce-172">
                    <strong>Ponudba</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81cce-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="81cce-173">
                    <strong>Podrobnost ponudbe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81cce-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="81cce-174">
                    <strong>Projekt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81cce-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="81cce-175">
                    <strong>Vključi čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81cce-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="81cce-176">
                    <strong>Vključi strošek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81cce-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="81cce-177">
                    <strong>Vključi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81cce-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="81cce-178">
                    <strong>dajatev</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81cce-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="81cce-179">
                    <strong>Veljavno/neveljavno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81cce-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="81cce-180">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="81cce-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-181">Pril1</span><span class="sxs-lookup"><span data-stu-id="81cce-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-182">Pon1</span><span class="sxs-lookup"><span data-stu-id="81cce-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-183">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="81cce-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-184">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-185">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-186">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-187">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81cce-188">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="81cce-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81cce-189">Kršitev 1. pravila.</span><span class="sxs-lookup"><span data-stu-id="81cce-189">Violation of Rule #1.</span></span> <span data-ttu-id="81cce-190">Čas, stroški in dajatve za projekt Proj1 so vključeni v obe podrobnosti ponudbe: PodrPon1 in PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="81cce-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-191">Pril1</span><span class="sxs-lookup"><span data-stu-id="81cce-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-192">Pon1</span><span class="sxs-lookup"><span data-stu-id="81cce-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-193">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="81cce-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-194">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-195">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-196">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-197">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-198">Pril1</span><span class="sxs-lookup"><span data-stu-id="81cce-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-199">Pon1</span><span class="sxs-lookup"><span data-stu-id="81cce-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-200">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="81cce-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-201">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-202">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-203">No</span><span class="sxs-lookup"><span data-stu-id="81cce-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-204">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81cce-205">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="81cce-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81cce-206">Kršitev 1. pravila.</span><span class="sxs-lookup"><span data-stu-id="81cce-206">Violation of Rule #1.</span></span> <span data-ttu-id="81cce-207">Čas in dajatve za projekt Proj1 so vključeni v obe podrobnosti ponudbe: PodrPon1 in PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="81cce-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-208">Pril1</span><span class="sxs-lookup"><span data-stu-id="81cce-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-209">Pon1</span><span class="sxs-lookup"><span data-stu-id="81cce-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-210">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="81cce-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-211">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-212">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-213">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-214">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-215">Pril1</span><span class="sxs-lookup"><span data-stu-id="81cce-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-216">Pon1</span><span class="sxs-lookup"><span data-stu-id="81cce-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-217">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="81cce-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-218">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-219">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-220">No</span><span class="sxs-lookup"><span data-stu-id="81cce-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-221">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81cce-222">Veljavno</span><span class="sxs-lookup"><span data-stu-id="81cce-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="81cce-223">Čas in dajatve za projekt Proj1 so vključeni v PodrPon1.</span><span class="sxs-lookup"><span data-stu-id="81cce-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="81cce-224">Stroški za projekt P1 so vključeni v PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="81cce-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="81cce-225">Ni prekrivanja glede tega, kar je vključeno v vsako podrobnost ponudbe, tako da je veljavno.</span><span class="sxs-lookup"><span data-stu-id="81cce-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-226">Pril1</span><span class="sxs-lookup"><span data-stu-id="81cce-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-227">Pon1</span><span class="sxs-lookup"><span data-stu-id="81cce-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-228">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="81cce-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-229">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-230">No</span><span class="sxs-lookup"><span data-stu-id="81cce-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-231">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-232">No</span><span class="sxs-lookup"><span data-stu-id="81cce-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-233">Pril1</span><span class="sxs-lookup"><span data-stu-id="81cce-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-234">Pon1</span><span class="sxs-lookup"><span data-stu-id="81cce-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-235">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="81cce-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-236">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-237">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-238">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-239">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81cce-240">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="81cce-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81cce-241">Kršitev zgornjega 1. pravila</span><span class="sxs-lookup"><span data-stu-id="81cce-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="81cce-242">Pon1 vključuje čas, stroške in dajatve za celoten projekt P1.</span><span class="sxs-lookup"><span data-stu-id="81cce-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="81cce-243">PodrPon2 vključuje čas, stroške in dajatve za celoten projekt P1 ter se prekriva s tistim, kar je vključeno v Pon1.</span><span class="sxs-lookup"><span data-stu-id="81cce-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-244">Pril1</span><span class="sxs-lookup"><span data-stu-id="81cce-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-245">Pon1</span><span class="sxs-lookup"><span data-stu-id="81cce-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-246">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="81cce-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-247">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-248">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-249">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-250">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-251">Pril1</span><span class="sxs-lookup"><span data-stu-id="81cce-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-252">Pon1</span><span class="sxs-lookup"><span data-stu-id="81cce-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-253">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="81cce-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-254">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-255">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-256">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-257">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="81cce-258">Veljavno</span><span class="sxs-lookup"><span data-stu-id="81cce-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81cce-259">Glede na 2. pravilo sta Pon1 in Pon2 dve ponudbi za isto priložnost, tako da lahko oba ocenjujeta enake komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="81cce-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-260">Pril1</span><span class="sxs-lookup"><span data-stu-id="81cce-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-261">Pon2</span><span class="sxs-lookup"><span data-stu-id="81cce-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-262">PodrPon1 pri Pon2</span><span class="sxs-lookup"><span data-stu-id="81cce-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-263">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-264">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-265">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-266">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-267">Pril1</span><span class="sxs-lookup"><span data-stu-id="81cce-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-268">Pon1</span><span class="sxs-lookup"><span data-stu-id="81cce-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-269">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="81cce-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-270">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-271">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-272">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-273">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="81cce-274">Veljavno</span><span class="sxs-lookup"><span data-stu-id="81cce-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="81cce-275">Glede na 3. pravilo sta Pon1 in Pon2 dve ponudbi za različni priložnosti, tako da ne moreta obe ocenjevati enakih komponent istega projekta.</span><span class="sxs-lookup"><span data-stu-id="81cce-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="81cce-276">Pril2</span><span class="sxs-lookup"><span data-stu-id="81cce-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="81cce-277">Pon1</span><span class="sxs-lookup"><span data-stu-id="81cce-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-278">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="81cce-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-279">Proj1</span><span class="sxs-lookup"><span data-stu-id="81cce-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-280">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="81cce-281">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="81cce-282">Da</span><span class="sxs-lookup"><span data-stu-id="81cce-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="81cce-283">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="81cce-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]