---
title: Pregled podrobnosti ponudb, ki temeljijo na projektih – poenostavljeno
description: Ta tema vsebuje informacije o uporabi podrobnosti ponudb, ki temeljijo na projektih, za projektno delo. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181112"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="56381-104">Pregled podrobnosti ponudb, ki temeljijo na projektih – poenostavljeno</span><span class="sxs-lookup"><span data-stu-id="56381-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="56381-105">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="56381-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="56381-106">Podrobnosti ponudb, ki temeljijo na projektu, so oblikovane tako, da pripomorejo k oceni projektnega dela v okviru interakcije.</span><span class="sxs-lookup"><span data-stu-id="56381-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="56381-107">Struktura podrobnosti ponudb, ki temelji na projektu, je razširjena za ocene projektov z naslednjimi koncepti:</span><span class="sxs-lookup"><span data-stu-id="56381-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="56381-108">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="56381-108">Billing Method</span></span>
- <span data-ttu-id="56381-109">Preslikavanje projektov in opravil</span><span class="sxs-lookup"><span data-stu-id="56381-109">Project and Task Mapping</span></span>
- <span data-ttu-id="56381-110">Vključuje razrede transakcij</span><span class="sxs-lookup"><span data-stu-id="56381-110">Included Transaction classes</span></span>
- <span data-ttu-id="56381-111">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="56381-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="56381-112">Nastavitev možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="56381-112">Chargeability setup</span></span>
- <span data-ttu-id="56381-113">Ocena z uporabo podrobnosti ponudb</span><span class="sxs-lookup"><span data-stu-id="56381-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="56381-114">Stranke podrobnosti ponudbe</span><span class="sxs-lookup"><span data-stu-id="56381-114">Quote line Customers</span></span>

<span data-ttu-id="56381-115">Naslednja tabela vsebuje informacije o poljih na zavihku **Splošno** pri podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="56381-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="56381-116">Ta polja pomagajo nastaviti osnovo za podrobno, temeljito oceno projektnega dela.</span><span class="sxs-lookup"><span data-stu-id="56381-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="56381-117">**Polje**</span><span class="sxs-lookup"><span data-stu-id="56381-117">**Field**</span></span> | <span data-ttu-id="56381-118">**Opis**</span><span class="sxs-lookup"><span data-stu-id="56381-118">**Description**</span></span> | <span data-ttu-id="56381-119">**Nadaljnji vpliv**</span><span class="sxs-lookup"><span data-stu-id="56381-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="56381-120">Imenu</span><span class="sxs-lookup"><span data-stu-id="56381-120">Name</span></span> | <span data-ttu-id="56381-121">Ime podrobnosti ponudbe, ki bi vam pomagala prepoznati ločeno komponento ponudbe, ki jo ocenjujete.</span><span class="sxs-lookup"><span data-stu-id="56381-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="56381-122">Kopirano v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="56381-123">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="56381-123">Billing Method</span></span> | <span data-ttu-id="56381-124">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="56381-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="56381-125">To polje vključuje dva glavna pogodbena modela, ki ju podpira Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="56381-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="56381-126">- fiksna cena</span><span class="sxs-lookup"><span data-stu-id="56381-126">- Fixed price</span></span></br><span data-ttu-id="56381-127">- čas in material</span><span class="sxs-lookup"><span data-stu-id="56381-127">- Time and material.</span></span>| <span data-ttu-id="56381-128">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="56381-129">Project</span><span class="sxs-lookup"><span data-stu-id="56381-129">Project</span></span> | <span data-ttu-id="56381-130">S tem izbirnim poljem določite projekt, ki se bo uporabljal za izvedbo dela za to interakcijo.</span><span class="sxs-lookup"><span data-stu-id="56381-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="56381-131">Ko je projekt preslikan v podrobnost ponudbe, pripomore k nastavitvi opravil, ki se zaračunajo, in tudi k pripravi ocene, ki temelji na projektu, pri vrstici ponudbe v obliki podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="56381-132">Če projekt ni preslikan na vrstico ponudbe, ki temelji na projektu, morate oceno ustvariti ročno z izdelavo vsake podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="56381-133">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="56381-134">Vključena opravila</span><span class="sxs-lookup"><span data-stu-id="56381-134">Included Tasks</span></span> | <span data-ttu-id="56381-135">Označuje, ali se ta podrobnost ponudbe uporablja za vsa ali nekatera projektna opravila za izbrani projekt.</span><span class="sxs-lookup"><span data-stu-id="56381-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="56381-136">To polje ima lahko naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="56381-136">This field has the following possible values:</span></span></br><span data-ttu-id="56381-137">- vsa opravila projekta</span><span class="sxs-lookup"><span data-stu-id="56381-137">- All project tasks</span></span></br><span data-ttu-id="56381-138">- samo izbrana opravila projekta</span><span class="sxs-lookup"><span data-stu-id="56381-138">- Selected project tasks only</span></span></br><span data-ttu-id="56381-139">Prazna vrednost v tem polju je enaka možnosti **Vsa projektna opravila**.</span><span class="sxs-lookup"><span data-stu-id="56381-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="56381-140">Ko je izbrana možnost **Samo izbrana opravila projekta**, lahko na strani projekta na zavihku **Nastavitev obračunavanja opravil** izberete povezavo posameznih opravil s to podrobnostjo ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="56381-141">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="56381-142">Vključi čas</span><span class="sxs-lookup"><span data-stu-id="56381-142">Include Time</span></span> | <span data-ttu-id="56381-143">Zastava **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="56381-144">Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="56381-145">Vrednost **Da** označuje, da bodo časovne transakcije ali stroški dela vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="56381-146">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="56381-147">Vključi strošek</span><span class="sxs-lookup"><span data-stu-id="56381-147">Include Expense</span></span> | <span data-ttu-id="56381-148">Zastava **Da**/**Ne** označuje, ali bodo stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="56381-149">Vrednost **Ne** označuje, da strošek ne bo vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="56381-150">Vrednost **Ne** označuje, da bo strošek vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="56381-151">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="56381-152">Vključi dajatev</span><span class="sxs-lookup"><span data-stu-id="56381-152">Include Fee</span></span> | <span data-ttu-id="56381-153">Zastava **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="56381-154">Vrednost **Ne** označuje, da dajatve ne bodo vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="56381-155">Vrednost **Da** označuje, da bodo dajatve vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="56381-156">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="56381-157">Znesek ponudbe</span><span class="sxs-lookup"><span data-stu-id="56381-157">Quoted Amount</span></span> | <span data-ttu-id="56381-158">To je znesek, ki bo stranki podan v ponudbi za vso delo, napovedano v tej podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="56381-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="56381-159">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz polja **Proračun stranke** v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="56381-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="56381-160">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="56381-161">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="56381-162">Predvideni davek</span><span class="sxs-lookup"><span data-stu-id="56381-162">Estimated Tax</span></span> | <span data-ttu-id="56381-163">To je polje, ki ga je mogoče urejati in v katerem lahko uporabnik doda predviden znesek davka v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="56381-164">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska davka v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="56381-165">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="56381-166">Znesek ponudbe po obdavčitvi</span><span class="sxs-lookup"><span data-stu-id="56381-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="56381-167">To polje je znesek v podrobnosti ponudbe po obdavčitvi in je samo za branje.</span><span class="sxs-lookup"><span data-stu-id="56381-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="56381-168">Znesek v tem polju se izračuna kot *znesek ponudbe + davek*.</span><span class="sxs-lookup"><span data-stu-id="56381-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="56381-169">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="56381-170">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="56381-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="56381-171">To polje je mogoče urejati in je na voljo samo v podrobnostih ponudb, ki temeljijo na projektih in imajo način obračunavanja **Čas in material**.</span><span class="sxs-lookup"><span data-stu-id="56381-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="56381-172">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="56381-173">Proračun stranke</span><span class="sxs-lookup"><span data-stu-id="56381-173">Customer Budget</span></span> | <span data-ttu-id="56381-174">To polje je mogoče urejati in se kopira iz ustreznega polja v vrstici priložnosti, če je bila ponudba ustvarjena iz priložnosti.</span><span class="sxs-lookup"><span data-stu-id="56381-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="56381-175">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="56381-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="56381-176">Pravila za preverjanje veljavnosti polj na zavihku Splošno v podrobnostih ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="56381-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="56381-177">**1. pravilo**: če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta**, je projekt vključen v podrobnost ponudbe.</span><span class="sxs-lookup"><span data-stu-id="56381-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="56381-178">**2. pravilo**: če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta**, je projekt in izbran razred transakcije mogoče vključiti samo v eno podrobnost ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="56381-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="56381-179">**3. pravilo**: če je polje **Vključena opravila** nastavljeno na **Samo izbrana opravila projekta**, je projekt in izbran razred transakcije mogoče vključiti v več podrobnosti ponudbe, ki temeljijo na projektu.</span><span class="sxs-lookup"><span data-stu-id="56381-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="56381-180">**4. pravilo** : če ima priložnost več ponudb, so lahko podrobnosti ponudbe za različne ponudbe, ki se vse sklicujejo na isti projekt in vključujejo isti razred transakcije.</span><span class="sxs-lookup"><span data-stu-id="56381-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="56381-181">**5. pravilo**: če ponudbe ne pripadajo isti priložnosti, ne morejo vključevati istega projekta in razreda transakcije.</span><span class="sxs-lookup"><span data-stu-id="56381-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="56381-182">
                    <strong>Priložnost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56381-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="56381-183">
                    <strong>Ponudba</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56381-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="56381-184">
                    <strong>Podrobnost ponudbe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56381-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="56381-185">
                    <strong>Projekt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56381-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="56381-186">
                    <strong>Vključena opravila</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56381-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="56381-187">
                    <strong>Vključi čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56381-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="56381-188">
                    <strong>Vključi strošek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56381-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="56381-189">
                    <strong>Vključi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56381-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="56381-190">
                    <strong>Dajatev</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56381-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="56381-191">
                    <strong>Veljavno/neveljavno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56381-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="56381-192">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="56381-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="56381-193">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-194">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-195">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="56381-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-196">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-197">Prazno</span><span class="sxs-lookup"><span data-stu-id="56381-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-198">Da</span><span class="sxs-lookup"><span data-stu-id="56381-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-199">Da</span><span class="sxs-lookup"><span data-stu-id="56381-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-200">Da</span><span class="sxs-lookup"><span data-stu-id="56381-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56381-201">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="56381-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56381-202">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="56381-202">Violation of Rule #2.</span></span> <span data-ttu-id="56381-203">Čas, stroški in dajatve za projekt Proj1 so vključeni v podrobnosti ponudbe PodrPon1 in PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="56381-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="56381-204">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-205">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-206">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="56381-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-207">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-208">Prazno</span><span class="sxs-lookup"><span data-stu-id="56381-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-209">Da</span><span class="sxs-lookup"><span data-stu-id="56381-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-210">Da</span><span class="sxs-lookup"><span data-stu-id="56381-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-211">Da</span><span class="sxs-lookup"><span data-stu-id="56381-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="56381-212">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-213">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-214">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="56381-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-215">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-216">Prazno</span><span class="sxs-lookup"><span data-stu-id="56381-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-217">Da</span><span class="sxs-lookup"><span data-stu-id="56381-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-218">No</span><span class="sxs-lookup"><span data-stu-id="56381-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-219">Da</span><span class="sxs-lookup"><span data-stu-id="56381-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56381-220">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="56381-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56381-221">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="56381-221">Violation of Rule #2.</span></span> <span data-ttu-id="56381-222">Čas in dajatve za projekt Proj1 so vključeni v podrobnosti ponudbe PodrPon1 in PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="56381-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="56381-223">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-224">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-225">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="56381-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-226">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-227">Prazno</span><span class="sxs-lookup"><span data-stu-id="56381-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-228">Da</span><span class="sxs-lookup"><span data-stu-id="56381-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-229">Da</span><span class="sxs-lookup"><span data-stu-id="56381-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-230">Da</span><span class="sxs-lookup"><span data-stu-id="56381-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="56381-231">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-232">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-233">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="56381-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-234">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-235">Prazno</span><span class="sxs-lookup"><span data-stu-id="56381-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-236">Da</span><span class="sxs-lookup"><span data-stu-id="56381-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-237">No</span><span class="sxs-lookup"><span data-stu-id="56381-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-238">Da</span><span class="sxs-lookup"><span data-stu-id="56381-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56381-239">Veljavno</span><span class="sxs-lookup"><span data-stu-id="56381-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="56381-240">Čas in dajatve za projekt Proj1 so vključeni v PodrPon1.</span><span class="sxs-lookup"><span data-stu-id="56381-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="56381-241">Stroški za projekt P1 so vključeni v PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="56381-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="56381-242">Ni prekrivanja glede tega, kar je vključeno v vsako podrobnost ponudbe in je veljavno.</span><span class="sxs-lookup"><span data-stu-id="56381-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="56381-243">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-244">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-245">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="56381-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-246">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-247">Prazno</span><span class="sxs-lookup"><span data-stu-id="56381-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-248">No</span><span class="sxs-lookup"><span data-stu-id="56381-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-249">Da</span><span class="sxs-lookup"><span data-stu-id="56381-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-250">No</span><span class="sxs-lookup"><span data-stu-id="56381-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="56381-251">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-252">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-253">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="56381-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-254">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-255">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="56381-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-256">Da</span><span class="sxs-lookup"><span data-stu-id="56381-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-257">Da</span><span class="sxs-lookup"><span data-stu-id="56381-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-258">Da</span><span class="sxs-lookup"><span data-stu-id="56381-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56381-259">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="56381-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56381-260">Kršitev zgornjega 2. pravila</span><span class="sxs-lookup"><span data-stu-id="56381-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="56381-261">Pon1 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.</span><span class="sxs-lookup"><span data-stu-id="56381-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="56381-262">PodrPon2 vključuje čas, stroške in dajatve za celoten projekt P1 ter se prekriva s tistim, kar je vključeno v Pon1.</span><span class="sxs-lookup"><span data-stu-id="56381-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="56381-263">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-264">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-265">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="56381-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-266">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-267">Prazno</span><span class="sxs-lookup"><span data-stu-id="56381-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-268">Da</span><span class="sxs-lookup"><span data-stu-id="56381-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-269">Da</span><span class="sxs-lookup"><span data-stu-id="56381-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-270">Da</span><span class="sxs-lookup"><span data-stu-id="56381-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="56381-271">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-272">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-273">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="56381-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-274">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-275">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="56381-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-276">Da</span><span class="sxs-lookup"><span data-stu-id="56381-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-277">Da</span><span class="sxs-lookup"><span data-stu-id="56381-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-278">Da</span><span class="sxs-lookup"><span data-stu-id="56381-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56381-279">Veljavno</span><span class="sxs-lookup"><span data-stu-id="56381-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56381-280">V skladu z zgornjim 3. pravilom</span><span class="sxs-lookup"><span data-stu-id="56381-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="56381-281">Pon1 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.</span><span class="sxs-lookup"><span data-stu-id="56381-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="56381-282">Pon2 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.</span><span class="sxs-lookup"><span data-stu-id="56381-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="56381-283">Edino dodatno preverjanje velja okoli podmnožice opravil v PodrPon1, ki se razlikujejo od podmnožice nalog v PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="56381-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="56381-284">To zagotavlja, da ne bo prekrivanja.</span><span class="sxs-lookup"><span data-stu-id="56381-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="56381-285">To opravi sistem, ko so opravila povezana.</span><span class="sxs-lookup"><span data-stu-id="56381-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="56381-286">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-287">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-288">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="56381-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-289">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-290">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="56381-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-291">Da</span><span class="sxs-lookup"><span data-stu-id="56381-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-292">Da</span><span class="sxs-lookup"><span data-stu-id="56381-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-293">Da</span><span class="sxs-lookup"><span data-stu-id="56381-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="56381-294">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-295">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-296">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="56381-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-297">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-298">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="56381-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-299">Da</span><span class="sxs-lookup"><span data-stu-id="56381-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-300">Da</span><span class="sxs-lookup"><span data-stu-id="56381-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-301">Da</span><span class="sxs-lookup"><span data-stu-id="56381-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="56381-302">Veljavno</span><span class="sxs-lookup"><span data-stu-id="56381-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56381-303">Glede na 5. pravilo sta Pon1 in Pon2 dve ponudbi za isto priložnost, tako da lahko oba ocenjujeta enake komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="56381-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="56381-304">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-305">Pon2</span><span class="sxs-lookup"><span data-stu-id="56381-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-306">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="56381-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-307">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-308">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="56381-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-309">Da</span><span class="sxs-lookup"><span data-stu-id="56381-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-310">Da</span><span class="sxs-lookup"><span data-stu-id="56381-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-311">Da</span><span class="sxs-lookup"><span data-stu-id="56381-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="56381-312">Pril1</span><span class="sxs-lookup"><span data-stu-id="56381-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-313">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-314">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="56381-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-315">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-316">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="56381-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-317">Da</span><span class="sxs-lookup"><span data-stu-id="56381-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-318">Da</span><span class="sxs-lookup"><span data-stu-id="56381-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-319">Da</span><span class="sxs-lookup"><span data-stu-id="56381-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="56381-320">Veljavno</span><span class="sxs-lookup"><span data-stu-id="56381-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="56381-321">Glede na 4. pravilo sta Pon1 in Pon2 dve ponudbi za različni priložnosti, tako da ne moreta obe ocenjevati enakih komponent istega projekta.</span><span class="sxs-lookup"><span data-stu-id="56381-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="56381-322">Pril2</span><span class="sxs-lookup"><span data-stu-id="56381-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="56381-323">Pon1</span><span class="sxs-lookup"><span data-stu-id="56381-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-324">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="56381-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-325">Proj1</span><span class="sxs-lookup"><span data-stu-id="56381-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="56381-326">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="56381-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-327">Da</span><span class="sxs-lookup"><span data-stu-id="56381-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="56381-328">Da</span><span class="sxs-lookup"><span data-stu-id="56381-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="56381-329">Da</span><span class="sxs-lookup"><span data-stu-id="56381-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="56381-330">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="56381-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

