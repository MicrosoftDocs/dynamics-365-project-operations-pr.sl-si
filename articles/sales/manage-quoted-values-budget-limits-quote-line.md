---
title: Pregled podrobnosti projektne ponudbe
description: Ta tema vsebuje informacije o uporabi podrobnosti projektne ponudbe za projektno delo.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa48a90c275eae1b0c0dbce685ae718dd9674c88
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858052"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="ae8f0-103">Pregled podrobnosti projektne ponudbe</span><span class="sxs-lookup"><span data-stu-id="ae8f0-103">Project quote lines overview</span></span>

<span data-ttu-id="ae8f0-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="ae8f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ae8f0-105">Podrobnosti ponudb, ki temeljijo na projektu, so oblikovane tako, da pripomorejo k oceni projektnega dela v okviru interakcije.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="ae8f0-106">Struktura podrobnosti ponudb, ki temelji na projektu, je razširjena za ocene projektov z naslednjimi koncepti:</span><span class="sxs-lookup"><span data-stu-id="ae8f0-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="ae8f0-107">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="ae8f0-107">Billing Method</span></span>
- <span data-ttu-id="ae8f0-108">Preslikavanje projektov</span><span class="sxs-lookup"><span data-stu-id="ae8f0-108">Project Mapping</span></span>
- <span data-ttu-id="ae8f0-109">Vključuje razrede transakcij</span><span class="sxs-lookup"><span data-stu-id="ae8f0-109">Included Transaction classes</span></span>
- <span data-ttu-id="ae8f0-110">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="ae8f0-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="ae8f0-111">Nastavitev možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="ae8f0-111">Chargeability setup</span></span>
- <span data-ttu-id="ae8f0-112">Ocena z uporabo podrobnosti ponudb</span><span class="sxs-lookup"><span data-stu-id="ae8f0-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="ae8f0-113">Stranke podrobnosti ponudbe</span><span class="sxs-lookup"><span data-stu-id="ae8f0-113">Quote line Customers</span></span>

<span data-ttu-id="ae8f0-114">Naslednja tabela vsebuje informacije o poljih na zavihku **Splošno** pri podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="ae8f0-115">Ta polja pomagajo nastaviti osnovo za podrobno, temeljito oceno projektnega dela.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="ae8f0-116">**Polje**</span><span class="sxs-lookup"><span data-stu-id="ae8f0-116">**Field**</span></span> | <span data-ttu-id="ae8f0-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="ae8f0-117">**Description**</span></span> | <span data-ttu-id="ae8f0-118">**Nadaljnji vpliv**</span><span class="sxs-lookup"><span data-stu-id="ae8f0-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ae8f0-119">Imenu</span><span class="sxs-lookup"><span data-stu-id="ae8f0-119">Name</span></span> | <span data-ttu-id="ae8f0-120">Ime podrobnosti ponudbe, ki bi vam pomagala prepoznati ločeno komponento ponudbe, ki jo ocenjujete.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="ae8f0-121">Kopirano v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ae8f0-122">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="ae8f0-122">Billing Method</span></span> | <span data-ttu-id="ae8f0-123">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="ae8f0-124">To polje vključuje dva glavna pogodbena modela, ki sta podprta v aplikaciji Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="ae8f0-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="ae8f0-125">- fiksna cena</span><span class="sxs-lookup"><span data-stu-id="ae8f0-125">- Fixed price</span></span></br><span data-ttu-id="ae8f0-126">- čas in material</span><span class="sxs-lookup"><span data-stu-id="ae8f0-126">- Time and material.</span></span>| <span data-ttu-id="ae8f0-127">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ae8f0-128">Project</span><span class="sxs-lookup"><span data-stu-id="ae8f0-128">Project</span></span> | <span data-ttu-id="ae8f0-129">S tem izbirnim poljem določite projekt, ki se bo uporabljal za izvedbo dela za to interakcijo.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="ae8f0-130">Ko je projekt preslikan v podrobnost ponudbe, pripomore k nastavitvi opravil, ki se zaračunajo, in tudi k pripravi ocene, ki temelji na projektu, pri vrstici ponudbe v obliki podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="ae8f0-131">Če projekt ni preslikan na vrstico ponudbe, ki temelji na projektu, morate oceno ustvariti ročno z izdelavo vsake podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="ae8f0-132">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ae8f0-133">Vključi čas</span><span class="sxs-lookup"><span data-stu-id="ae8f0-133">Include Time</span></span> | <span data-ttu-id="ae8f0-134">Zastava **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ae8f0-135">Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ae8f0-136">Vrednost **Da** označuje, da bodo časovne transakcije ali stroški dela vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ae8f0-137">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ae8f0-138">Vključi strošek</span><span class="sxs-lookup"><span data-stu-id="ae8f0-138">Include Expense</span></span> | <span data-ttu-id="ae8f0-139">Zastava **Da**/**Ne** označuje, ali bodo stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ae8f0-140">Vrednost **Ne** označuje, da strošek ne bo vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ae8f0-141">Vrednost **Ne** označuje, da bo strošek vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ae8f0-142">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ae8f0-143">Vključi dajatev</span><span class="sxs-lookup"><span data-stu-id="ae8f0-143">Include Fee</span></span> | <span data-ttu-id="ae8f0-144">Zastava **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="ae8f0-145">Vrednost **Ne** označuje, da dajatve ne bodo vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="ae8f0-146">Vrednost **Da** označuje, da bodo dajatve vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="ae8f0-147">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ae8f0-148">Znesek ponudbe</span><span class="sxs-lookup"><span data-stu-id="ae8f0-148">Quoted Amount</span></span> | <span data-ttu-id="ae8f0-149">To je znesek, ki bo stranki podan v ponudbi za vso delo, napovedano v tej podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="ae8f0-150">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz polja **Proračun stranke** v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="ae8f0-151">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="ae8f0-152">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ae8f0-153">Predvideni davek</span><span class="sxs-lookup"><span data-stu-id="ae8f0-153">Estimated Tax</span></span> | <span data-ttu-id="ae8f0-154">To je polje, ki ga je mogoče urejati in v katerem lahko uporabnik doda predviden znesek davka v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="ae8f0-155">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska davka v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="ae8f0-156">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ae8f0-157">Znesek ponudbe po obdavčitvi</span><span class="sxs-lookup"><span data-stu-id="ae8f0-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="ae8f0-158">To polje je znesek v podrobnosti ponudbe po obdavčitvi in je samo za branje.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="ae8f0-159">Znesek v tem polju se izračuna kot *znesek ponudbe + davek*.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="ae8f0-160">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ae8f0-161">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="ae8f0-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="ae8f0-162">To polje je mogoče urejati in je na voljo samo v podrobnostih ponudb, ki temeljijo na projektih in imajo način obračunavanja **Čas in material**.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="ae8f0-163">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="ae8f0-164">Proračun stranke</span><span class="sxs-lookup"><span data-stu-id="ae8f0-164">Customer Budget</span></span> | <span data-ttu-id="ae8f0-165">To polje je mogoče urejati in se kopira iz ustreznega polja v vrstici priložnosti, če je bila ponudba ustvarjena iz priložnosti.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="ae8f0-166">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="ae8f0-167">Pravila za preverjanje veljavnosti polj na zavihku Splošno v podrobnostih ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="ae8f0-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="ae8f0-168">**1. pravilo**: določen razred transakcije v izbranem projektu je mogoče vključiti samo v eno podrobnost ponudbe, ki temelji na projektih.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="ae8f0-169">**2. pravilo** : če ima priložnost več ponudb, so lahko podrobnosti ponudbe za različne ponudbe, ki se vse sklicujejo na isti projekt in vključujejo isti razred transakcije.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="ae8f0-170">**3. pravilo**: če ponudbe ne pripadajo isti priložnosti, ne morejo vključevati istega projekta in razreda transakcije.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="ae8f0-171">
                    <strong>Priložnost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ae8f0-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="ae8f0-172">
                    <strong>Ponudba</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ae8f0-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ae8f0-173">
                    <strong>Podrobnost ponudbe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ae8f0-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ae8f0-174">
                    <strong>Projekt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ae8f0-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ae8f0-175">
                    <strong>Vključi čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ae8f0-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="ae8f0-176">
                    <strong>Vključi strošek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ae8f0-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="ae8f0-177">
                    <strong>Vključi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ae8f0-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="ae8f0-178">
                    <strong>dajatev</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ae8f0-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="ae8f0-179">
                    <strong>Veljavno/neveljavno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ae8f0-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="ae8f0-180">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ae8f0-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ae8f0-181">Pril1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-182">Pon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-183">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-184">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-185">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-186">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-187">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ae8f0-188">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="ae8f0-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ae8f0-189">Kršitev 1. pravila.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-189">Violation of Rule #1.</span></span> <span data-ttu-id="ae8f0-190">Čas, stroški in dajatve za projekt Proj1 so vključeni v obe podrobnosti ponudbe: PodrPon1 in PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ae8f0-191">Pril1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-192">Pon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-193">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="ae8f0-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-194">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-195">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-196">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-197">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-197">Yes</span></span> </p>
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
<span data-ttu-id="ae8f0-198">Pril1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-199">Pon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-200">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-201">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-202">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-203">No</span><span class="sxs-lookup"><span data-stu-id="ae8f0-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-204">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ae8f0-205">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="ae8f0-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ae8f0-206">Kršitev 1. pravila.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-206">Violation of Rule #1.</span></span> <span data-ttu-id="ae8f0-207">Čas in dajatve za projekt Proj1 so vključeni v obe podrobnosti ponudbe: PodrPon1 in PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ae8f0-208">Pril1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-209">Pon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-210">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="ae8f0-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-211">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-212">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-213">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-214">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-214">Yes</span></span> </p>
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
<span data-ttu-id="ae8f0-215">Pril1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-216">Pon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-217">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-218">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-219">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-220">No</span><span class="sxs-lookup"><span data-stu-id="ae8f0-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-221">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ae8f0-222">Veljavno</span><span class="sxs-lookup"><span data-stu-id="ae8f0-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="ae8f0-223">Čas in dajatve za projekt Proj1 so vključeni v PodrPon1.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="ae8f0-224">Stroški za projekt P1 so vključeni v PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="ae8f0-225">Ni prekrivanja glede tega, kar je vključeno v vsako podrobnost ponudbe, tako da je veljavno.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ae8f0-226">Pril1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-227">Pon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-228">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="ae8f0-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-229">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-230">No</span><span class="sxs-lookup"><span data-stu-id="ae8f0-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-231">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-232">No</span><span class="sxs-lookup"><span data-stu-id="ae8f0-232">No</span></span> </p>
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
<span data-ttu-id="ae8f0-233">Pril1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-234">Pon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-235">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-236">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-237">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-238">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-239">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ae8f0-240">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="ae8f0-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ae8f0-241">Kršitev zgornjega 1. pravila</span><span class="sxs-lookup"><span data-stu-id="ae8f0-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="ae8f0-242">Pon1 vključuje čas, stroške in dajatve za celoten projekt P1.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="ae8f0-243">PodrPon2 vključuje čas, stroške in dajatve za celoten projekt P1 ter se prekriva s tistim, kar je vključeno v Pon1.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ae8f0-244">Pril1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-245">Pon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-246">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="ae8f0-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-247">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-248">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-249">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-250">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-250">Yes</span></span> </p>
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
<span data-ttu-id="ae8f0-251">Pril1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-252">Pon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-253">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-254">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-255">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-256">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-257">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ae8f0-258">Veljavno</span><span class="sxs-lookup"><span data-stu-id="ae8f0-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ae8f0-259">Glede na 2. pravilo sta Pon1 in Pon2 dve ponudbi za isto priložnost, tako da lahko oba ocenjujeta enake komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ae8f0-260">Pril1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-261">Pon2</span><span class="sxs-lookup"><span data-stu-id="ae8f0-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-262">PodrPon1 pri Pon2</span><span class="sxs-lookup"><span data-stu-id="ae8f0-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-263">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-264">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-265">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-266">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-266">Yes</span></span> </p>
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
<span data-ttu-id="ae8f0-267">Pril1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-268">Pon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-269">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-270">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-271">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-272">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-273">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ae8f0-274">Veljavno</span><span class="sxs-lookup"><span data-stu-id="ae8f0-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ae8f0-275">Glede na 3. pravilo sta Pon1 in Pon2 dve ponudbi za različni priložnosti, tako da ne moreta obe ocenjevati enakih komponent istega projekta.</span><span class="sxs-lookup"><span data-stu-id="ae8f0-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="ae8f0-276">Pril2</span><span class="sxs-lookup"><span data-stu-id="ae8f0-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="ae8f0-277">Pon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-278">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-279">Proj1</span><span class="sxs-lookup"><span data-stu-id="ae8f0-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-280">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="ae8f0-281">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="ae8f0-282">Da</span><span class="sxs-lookup"><span data-stu-id="ae8f0-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="ae8f0-283">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="ae8f0-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
