---
title: Podrobnosti ponudb, ki temeljijo na projektih (Pro)
description: Ta tema vsebuje informacije o uporabi podrobnosti ponudb, ki temeljijo na projektih, za projektno delo. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084686"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="e1842-104">Podrobnosti ponudb, ki temeljijo na projektih (Pro)</span><span class="sxs-lookup"><span data-stu-id="e1842-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="e1842-105">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="e1842-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e1842-106">Podrobnosti ponudb, ki temeljijo na projektu, so oblikovane tako, da pripomorejo k oceni projektnega dela v okviru interakcije.</span><span class="sxs-lookup"><span data-stu-id="e1842-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="e1842-107">Struktura podrobnosti ponudb, ki temelji na projektu, je razširjena za ocene projektov z naslednjimi koncepti:</span><span class="sxs-lookup"><span data-stu-id="e1842-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="e1842-108">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="e1842-108">Billing Method</span></span>
- <span data-ttu-id="e1842-109">Preslikavanje projektov in opravil</span><span class="sxs-lookup"><span data-stu-id="e1842-109">Project and Task Mapping</span></span>
- <span data-ttu-id="e1842-110">Vključuje razrede transakcij</span><span class="sxs-lookup"><span data-stu-id="e1842-110">Included Transaction classes</span></span>
- <span data-ttu-id="e1842-111">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="e1842-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="e1842-112">Nastavitev možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="e1842-112">Chargeability setup</span></span>
- <span data-ttu-id="e1842-113">Ocena z uporabo podrobnosti ponudb</span><span class="sxs-lookup"><span data-stu-id="e1842-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="e1842-114">Stranke podrobnosti ponudbe</span><span class="sxs-lookup"><span data-stu-id="e1842-114">Quote line Customers</span></span>

<span data-ttu-id="e1842-115">Naslednja tabela vsebuje informacije o poljih na zavihku **Splošno** pri podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="e1842-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="e1842-116">Ta polja pomagajo nastaviti osnovo za podrobno, temeljito oceno projektnega dela.</span><span class="sxs-lookup"><span data-stu-id="e1842-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="e1842-117">**Polje**</span><span class="sxs-lookup"><span data-stu-id="e1842-117">**Field**</span></span> | <span data-ttu-id="e1842-118">**Ustreznost, namen in smernice**</span><span class="sxs-lookup"><span data-stu-id="e1842-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="e1842-119">**Nadaljnji vpliv**</span><span class="sxs-lookup"><span data-stu-id="e1842-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e1842-120">Imenu</span><span class="sxs-lookup"><span data-stu-id="e1842-120">Name</span></span> | <span data-ttu-id="e1842-121">Ime podrobnosti ponudbe, ki bi vam pomagala prepoznati ločeno komponento ponudbe, ki jo ocenjujete.</span><span class="sxs-lookup"><span data-stu-id="e1842-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="e1842-122">Kopirano v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1842-123">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="e1842-123">Billing Method</span></span> | <span data-ttu-id="e1842-124">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="e1842-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="e1842-125">To polje vključuje dva glavna pogodbena modela, ki ju podpira Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="e1842-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="e1842-126">- fiksna cena</span><span class="sxs-lookup"><span data-stu-id="e1842-126">- Fixed price</span></span></br><span data-ttu-id="e1842-127">- čas in material</span><span class="sxs-lookup"><span data-stu-id="e1842-127">- Time and material.</span></span>| <span data-ttu-id="e1842-128">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1842-129">Project</span><span class="sxs-lookup"><span data-stu-id="e1842-129">Project</span></span> | <span data-ttu-id="e1842-130">S tem izbirnim poljem določite projekt, ki se bo uporabljal za izvedbo dela za to interakcijo.</span><span class="sxs-lookup"><span data-stu-id="e1842-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="e1842-131">Ko je projekt preslikan v podrobnost ponudbe, pripomore k nastavitvi opravil, ki se zaračunajo, in tudi k pripravi ocene, ki temelji na projektu, pri vrstici ponudbe v obliki podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="e1842-132">Če projekt ni preslikan na vrstico ponudbe, ki temelji na projektu, morate oceno ustvariti ročno z izdelavo vsake podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="e1842-133">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="e1842-134">Vključena opravila</span><span class="sxs-lookup"><span data-stu-id="e1842-134">Included Tasks</span></span> | <span data-ttu-id="e1842-135">Označuje, ali se ta podrobnost ponudbe uporablja za vsa ali nekatera projektna opravila za izbrani projekt.</span><span class="sxs-lookup"><span data-stu-id="e1842-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="e1842-136">To polje ima lahko naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="e1842-136">This field has the following possible values:</span></span></br><span data-ttu-id="e1842-137">- vsa opravila projekta</span><span class="sxs-lookup"><span data-stu-id="e1842-137">- All project tasks</span></span></br><span data-ttu-id="e1842-138">- samo izbrana opravila projekta</span><span class="sxs-lookup"><span data-stu-id="e1842-138">- Selected project tasks only</span></span></br><span data-ttu-id="e1842-139">Prazna vrednost v tem polju je enaka možnosti **Vsa projektna opravila**.</span><span class="sxs-lookup"><span data-stu-id="e1842-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="e1842-140">Ko je izbrana možnost **Samo izbrana opravila projekta** , lahko na strani projekta na zavihku **Nastavitev obračunavanja opravil** izberete povezavo posameznih opravil s to podrobnostjo ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="e1842-141">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1842-142">Vključi čas</span><span class="sxs-lookup"><span data-stu-id="e1842-142">Include Time</span></span> | <span data-ttu-id="e1842-143">Zastava **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1842-144">Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1842-145">Vrednost **Da** označuje, da bodo časovne transakcije ali stroški dela vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e1842-146">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1842-147">Vključi strošek</span><span class="sxs-lookup"><span data-stu-id="e1842-147">Include Expense</span></span> | <span data-ttu-id="e1842-148">Zastava **Da**/**Ne** označuje, ali bodo stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1842-149">Vrednost **Ne** označuje, da strošek ne bo vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1842-150">Vrednost **Ne** označuje, da bo strošek vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e1842-151">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1842-152">Vključi dajatev</span><span class="sxs-lookup"><span data-stu-id="e1842-152">Include Fee</span></span> | <span data-ttu-id="e1842-153">Zastava **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1842-154">Vrednost **Ne** označuje, da dajatve ne bodo vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1842-155">Vrednost **Da** označuje, da bodo dajatve vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e1842-156">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1842-157">Znesek ponudbe</span><span class="sxs-lookup"><span data-stu-id="e1842-157">Quoted Amount</span></span> | <span data-ttu-id="e1842-158">To je znesek, ki bo stranki podan v ponudbi za vso delo, napovedano v tej podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="e1842-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="e1842-159">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz polja **Proračun stranke** v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="e1842-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="e1842-160">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="e1842-161">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1842-162">Predvideni davek</span><span class="sxs-lookup"><span data-stu-id="e1842-162">Estimated Tax</span></span> | <span data-ttu-id="e1842-163">To je polje, ki ga je mogoče urejati in v katerem lahko uporabnik doda predviden znesek davka v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="e1842-164">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska davka v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="e1842-165">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1842-166">Znesek ponudbe po obdavčitvi</span><span class="sxs-lookup"><span data-stu-id="e1842-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="e1842-167">To polje je znesek v podrobnosti ponudbe po obdavčitvi in je samo za branje.</span><span class="sxs-lookup"><span data-stu-id="e1842-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="e1842-168">Znesek v tem polju se izračuna kot *znesek ponudbe + davek*.</span><span class="sxs-lookup"><span data-stu-id="e1842-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="e1842-169">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1842-170">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="e1842-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="e1842-171">To polje je mogoče urejati in je na voljo samo v podrobnostih ponudb, ki temeljijo na projektih in imajo način obračunavanja **Čas in material**.</span><span class="sxs-lookup"><span data-stu-id="e1842-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="e1842-172">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1842-173">Proračun stranke</span><span class="sxs-lookup"><span data-stu-id="e1842-173">Customer Budget</span></span> | <span data-ttu-id="e1842-174">To polje je mogoče urejati in se kopira iz ustreznega polja v vrstici priložnosti, če je bila ponudba ustvarjena iz priložnosti.</span><span class="sxs-lookup"><span data-stu-id="e1842-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="e1842-175">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1842-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="e1842-176">Pravila za preverjanje veljavnosti polj na zavihku Splošno v podrobnostih ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="e1842-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="e1842-177">**1. pravilo** : če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta** , je projekt vključen v podrobnost ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1842-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="e1842-178">**2. pravilo** : če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta** , je projekt in izbran razred transakcije mogoče vključiti samo v eno podrobnost ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="e1842-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="e1842-179">**3. pravilo** : če je polje **Vključena opravila** nastavljeno na **Samo izbrana opravila projekta** , je projekt in izbran razred transakcije mogoče vključiti v več podrobnosti ponudbe, ki temeljijo na projektu.</span><span class="sxs-lookup"><span data-stu-id="e1842-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="e1842-180">**4. pravilo** : če ima priložnost več ponudb, so lahko podrobnosti ponudbe za različne ponudbe, ki se vse sklicujejo na isti projekt in vključujejo isti razred transakcije.</span><span class="sxs-lookup"><span data-stu-id="e1842-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="e1842-181">**5. pravilo** : če ponudbe ne pripadajo isti priložnosti, ne morejo vključevati istega projekta in razreda transakcije.</span><span class="sxs-lookup"><span data-stu-id="e1842-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="e1842-182">
                    <strong>Priložnost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1842-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="e1842-183">
                    <strong>Ponudba</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1842-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e1842-184">
                    <strong>Podrobnost ponudbe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1842-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e1842-185">
                    <strong>Projekt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1842-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="e1842-186">
                    <strong>Vključena opravila</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1842-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="e1842-187">
                    <strong>Vključi čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1842-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="e1842-188">
                    <strong>Vključi strošek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1842-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e1842-189">
                    <strong>Vključi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1842-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="e1842-190">
                    <strong>Dajatev</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1842-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="e1842-191">
                    <strong>Veljavno/neveljavno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1842-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="e1842-192">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1842-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e1842-193">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-194">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-195">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1842-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-196">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-197">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1842-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-198">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-199">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-200">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1842-201">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="e1842-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1842-202">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="e1842-202">Violation of Rule #2.</span></span> <span data-ttu-id="e1842-203">Čas, stroški in dajatve za projekt Proj1 so vključeni v podrobnosti ponudbe PodrPon1 in PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="e1842-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e1842-204">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-205">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-206">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="e1842-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-207">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-208">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1842-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-209">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-210">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-211">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-211">Yes</span></span> </p>
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
<span data-ttu-id="e1842-212">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-213">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-214">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1842-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-215">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-216">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1842-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-217">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-218">No</span><span class="sxs-lookup"><span data-stu-id="e1842-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-219">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1842-220">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="e1842-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1842-221">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="e1842-221">Violation of Rule #2.</span></span> <span data-ttu-id="e1842-222">Čas in dajatve za projekt Proj1 so vključeni v podrobnosti ponudbe PodrPon1 in PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="e1842-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e1842-223">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-224">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-225">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="e1842-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-226">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-227">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1842-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-228">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-229">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-230">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-230">Yes</span></span> </p>
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
<span data-ttu-id="e1842-231">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-232">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-233">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1842-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-234">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-235">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1842-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-236">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-237">No</span><span class="sxs-lookup"><span data-stu-id="e1842-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-238">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1842-239">Veljavno</span><span class="sxs-lookup"><span data-stu-id="e1842-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="e1842-240">Čas in dajatve za projekt Proj1 so vključeni v PodrPon1.</span><span class="sxs-lookup"><span data-stu-id="e1842-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="e1842-241">Stroški za projekt P1 so vključeni v PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="e1842-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="e1842-242">Ni prekrivanja glede tega, kar je vključeno v vsako podrobnost ponudbe in je veljavno.</span><span class="sxs-lookup"><span data-stu-id="e1842-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e1842-243">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-244">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-245">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="e1842-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-246">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-247">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1842-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-248">No</span><span class="sxs-lookup"><span data-stu-id="e1842-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-249">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-250">No</span><span class="sxs-lookup"><span data-stu-id="e1842-250">No</span></span> </p>
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
<span data-ttu-id="e1842-251">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-252">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-253">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1842-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-254">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-255">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="e1842-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-256">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-257">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-258">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1842-259">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="e1842-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1842-260">Kršitev zgornjega 2. pravila</span><span class="sxs-lookup"><span data-stu-id="e1842-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="e1842-261">Pon1 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.</span><span class="sxs-lookup"><span data-stu-id="e1842-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e1842-262">PodrPon2 vključuje čas, stroške in dajatve za celoten projekt P1 ter se prekriva s tistim, kar je vključeno v Pon1.</span><span class="sxs-lookup"><span data-stu-id="e1842-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e1842-263">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-264">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-265">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="e1842-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-266">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-267">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1842-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-268">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-269">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-270">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-270">Yes</span></span> </p>
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
<span data-ttu-id="e1842-271">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-272">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-273">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1842-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-274">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-275">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="e1842-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-276">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-277">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-278">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1842-279">Veljavno</span><span class="sxs-lookup"><span data-stu-id="e1842-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1842-280">V skladu z zgornjim 3. pravilom</span><span class="sxs-lookup"><span data-stu-id="e1842-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="e1842-281">Pon1 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.</span><span class="sxs-lookup"><span data-stu-id="e1842-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e1842-282">Pon2 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.</span><span class="sxs-lookup"><span data-stu-id="e1842-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e1842-283">Edino dodatno preverjanje velja okoli podmnožice opravil v PodrPon1, ki se razlikujejo od podmnožice nalog v PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="e1842-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="e1842-284">To zagotavlja, da ne bo prekrivanja.</span><span class="sxs-lookup"><span data-stu-id="e1842-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="e1842-285">To opravi sistem, ko so opravila povezana.</span><span class="sxs-lookup"><span data-stu-id="e1842-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e1842-286">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-287">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-288">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="e1842-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-289">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-290">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="e1842-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-291">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-292">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-293">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-293">Yes</span></span> </p>
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
<span data-ttu-id="e1842-294">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-295">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-296">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1842-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-297">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-298">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="e1842-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-299">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-300">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-301">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e1842-302">Veljavno</span><span class="sxs-lookup"><span data-stu-id="e1842-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1842-303">Glede na 5. pravilo sta Pon1 in Pon2 dve ponudbi za isto priložnost, tako da lahko oba ocenjujeta enake komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="e1842-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e1842-304">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-305">Pon2</span><span class="sxs-lookup"><span data-stu-id="e1842-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-306">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1842-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-307">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-308">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="e1842-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-309">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-310">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-311">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-311">Yes</span></span> </p>
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
<span data-ttu-id="e1842-312">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1842-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-313">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-314">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1842-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-315">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-316">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="e1842-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-317">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-318">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-319">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e1842-320">Veljavno</span><span class="sxs-lookup"><span data-stu-id="e1842-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1842-321">Glede na 4. pravilo sta Pon1 in Pon2 dve ponudbi za različni priložnosti, tako da ne moreta obe ocenjevati enakih komponent istega projekta.</span><span class="sxs-lookup"><span data-stu-id="e1842-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e1842-322">Pril2</span><span class="sxs-lookup"><span data-stu-id="e1842-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1842-323">Pon1</span><span class="sxs-lookup"><span data-stu-id="e1842-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-324">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1842-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-325">Proj1</span><span class="sxs-lookup"><span data-stu-id="e1842-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="e1842-326">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="e1842-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-327">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e1842-328">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e1842-329">Da</span><span class="sxs-lookup"><span data-stu-id="e1842-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e1842-330">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="e1842-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

