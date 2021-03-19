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
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272993"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="a45a8-104">Pregled podrobnosti ponudb, ki temeljijo na projektih – poenostavljeno</span><span class="sxs-lookup"><span data-stu-id="a45a8-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="a45a8-105">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="a45a8-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a45a8-106">Podrobnosti ponudb, ki temeljijo na projektu, so oblikovane tako, da pripomorejo k oceni projektnega dela v okviru interakcije.</span><span class="sxs-lookup"><span data-stu-id="a45a8-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="a45a8-107">Struktura podrobnosti ponudb, ki temelji na projektu, je razširjena za ocene projektov z naslednjimi koncepti:</span><span class="sxs-lookup"><span data-stu-id="a45a8-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="a45a8-108">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="a45a8-108">Billing Method</span></span>
- <span data-ttu-id="a45a8-109">Preslikavanje projektov in opravil</span><span class="sxs-lookup"><span data-stu-id="a45a8-109">Project and Task Mapping</span></span>
- <span data-ttu-id="a45a8-110">Vključuje razrede transakcij</span><span class="sxs-lookup"><span data-stu-id="a45a8-110">Included Transaction classes</span></span>
- <span data-ttu-id="a45a8-111">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="a45a8-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="a45a8-112">Nastavitev možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="a45a8-112">Chargeability setup</span></span>
- <span data-ttu-id="a45a8-113">Ocena z uporabo podrobnosti ponudb</span><span class="sxs-lookup"><span data-stu-id="a45a8-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="a45a8-114">Stranke podrobnosti ponudbe</span><span class="sxs-lookup"><span data-stu-id="a45a8-114">Quote line Customers</span></span>

<span data-ttu-id="a45a8-115">Naslednja tabela vsebuje informacije o poljih na zavihku **Splošno** pri podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="a45a8-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="a45a8-116">Ta polja pomagajo nastaviti osnovo za podrobno, temeljito oceno projektnega dela.</span><span class="sxs-lookup"><span data-stu-id="a45a8-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="a45a8-117">**Polje**</span><span class="sxs-lookup"><span data-stu-id="a45a8-117">**Field**</span></span> | <span data-ttu-id="a45a8-118">**Opis**</span><span class="sxs-lookup"><span data-stu-id="a45a8-118">**Description**</span></span> | <span data-ttu-id="a45a8-119">**Nadaljnji vpliv**</span><span class="sxs-lookup"><span data-stu-id="a45a8-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a45a8-120">Imenu</span><span class="sxs-lookup"><span data-stu-id="a45a8-120">Name</span></span> | <span data-ttu-id="a45a8-121">Ime podrobnosti ponudbe, ki bi vam pomagala prepoznati ločeno komponento ponudbe, ki jo ocenjujete.</span><span class="sxs-lookup"><span data-stu-id="a45a8-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="a45a8-122">Kopirano v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a45a8-123">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="a45a8-123">Billing Method</span></span> | <span data-ttu-id="a45a8-124">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="a45a8-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="a45a8-125">To polje vključuje dva glavna pogodbena modela, ki sta podprta v aplikaciji Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="a45a8-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="a45a8-126">- fiksna cena</span><span class="sxs-lookup"><span data-stu-id="a45a8-126">- Fixed price</span></span></br><span data-ttu-id="a45a8-127">- čas in material</span><span class="sxs-lookup"><span data-stu-id="a45a8-127">- Time and material.</span></span>| <span data-ttu-id="a45a8-128">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a45a8-129">Project</span><span class="sxs-lookup"><span data-stu-id="a45a8-129">Project</span></span> | <span data-ttu-id="a45a8-130">S tem izbirnim poljem določite projekt, ki se bo uporabljal za izvedbo dela za to interakcijo.</span><span class="sxs-lookup"><span data-stu-id="a45a8-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="a45a8-131">Ko je projekt preslikan v podrobnost ponudbe, pripomore k nastavitvi opravil, ki se zaračunajo, in tudi k pripravi ocene, ki temelji na projektu, pri vrstici ponudbe v obliki podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="a45a8-132">Če projekt ni preslikan na vrstico ponudbe, ki temelji na projektu, morate oceno ustvariti ročno z izdelavo vsake podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="a45a8-133">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="a45a8-134">Vključena opravila</span><span class="sxs-lookup"><span data-stu-id="a45a8-134">Included Tasks</span></span> | <span data-ttu-id="a45a8-135">Označuje, ali se ta podrobnost ponudbe uporablja za vsa ali nekatera projektna opravila za izbrani projekt.</span><span class="sxs-lookup"><span data-stu-id="a45a8-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="a45a8-136">To polje ima lahko naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="a45a8-136">This field has the following possible values:</span></span></br><span data-ttu-id="a45a8-137">- vsa opravila projekta</span><span class="sxs-lookup"><span data-stu-id="a45a8-137">- All project tasks</span></span></br><span data-ttu-id="a45a8-138">- samo izbrana opravila projekta</span><span class="sxs-lookup"><span data-stu-id="a45a8-138">- Selected project tasks only</span></span></br><span data-ttu-id="a45a8-139">Prazna vrednost v tem polju je enaka možnosti **Vsa projektna opravila**.</span><span class="sxs-lookup"><span data-stu-id="a45a8-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="a45a8-140">Ko je izbrana možnost **Samo izbrana opravila projekta**, lahko na strani projekta na zavihku **Nastavitev obračunavanja opravil** izberete povezavo posameznih opravil s to podrobnostjo ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="a45a8-141">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a45a8-142">Vključi čas</span><span class="sxs-lookup"><span data-stu-id="a45a8-142">Include Time</span></span> | <span data-ttu-id="a45a8-143">Zastava **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="a45a8-144">Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="a45a8-145">Vrednost **Da** označuje, da bodo časovne transakcije ali stroški dela vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="a45a8-146">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a45a8-147">Vključi strošek</span><span class="sxs-lookup"><span data-stu-id="a45a8-147">Include Expense</span></span> | <span data-ttu-id="a45a8-148">Zastava **Da**/**Ne** označuje, ali bodo stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="a45a8-149">Vrednost **Ne** označuje, da strošek ne bo vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="a45a8-150">Vrednost **Ne** označuje, da bo strošek vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="a45a8-151">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a45a8-152">Vključi dajatev</span><span class="sxs-lookup"><span data-stu-id="a45a8-152">Include Fee</span></span> | <span data-ttu-id="a45a8-153">Zastava **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="a45a8-154">Vrednost **Ne** označuje, da dajatve ne bodo vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="a45a8-155">Vrednost **Da** označuje, da bodo dajatve vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="a45a8-156">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a45a8-157">Znesek ponudbe</span><span class="sxs-lookup"><span data-stu-id="a45a8-157">Quoted Amount</span></span> | <span data-ttu-id="a45a8-158">To je znesek, ki bo stranki podan v ponudbi za vso delo, napovedano v tej podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="a45a8-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="a45a8-159">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz polja **Proračun stranke** v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="a45a8-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="a45a8-160">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="a45a8-161">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a45a8-162">Predvideni davek</span><span class="sxs-lookup"><span data-stu-id="a45a8-162">Estimated Tax</span></span> | <span data-ttu-id="a45a8-163">To je polje, ki ga je mogoče urejati in v katerem lahko uporabnik doda predviden znesek davka v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="a45a8-164">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska davka v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="a45a8-165">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a45a8-166">Znesek ponudbe po obdavčitvi</span><span class="sxs-lookup"><span data-stu-id="a45a8-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="a45a8-167">To polje je znesek v podrobnosti ponudbe po obdavčitvi in je samo za branje.</span><span class="sxs-lookup"><span data-stu-id="a45a8-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="a45a8-168">Znesek v tem polju se izračuna kot *znesek ponudbe + davek*.</span><span class="sxs-lookup"><span data-stu-id="a45a8-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="a45a8-169">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a45a8-170">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="a45a8-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="a45a8-171">To polje je mogoče urejati in je na voljo samo v podrobnostih ponudb, ki temeljijo na projektih in imajo način obračunavanja **Čas in material**.</span><span class="sxs-lookup"><span data-stu-id="a45a8-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="a45a8-172">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="a45a8-173">Proračun stranke</span><span class="sxs-lookup"><span data-stu-id="a45a8-173">Customer Budget</span></span> | <span data-ttu-id="a45a8-174">To polje je mogoče urejati in se kopira iz ustreznega polja v vrstici priložnosti, če je bila ponudba ustvarjena iz priložnosti.</span><span class="sxs-lookup"><span data-stu-id="a45a8-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="a45a8-175">Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="a45a8-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="a45a8-176">Pravila za preverjanje veljavnosti polj na zavihku Splošno v podrobnostih ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="a45a8-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="a45a8-177">**1. pravilo**: če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta**, je projekt vključen v podrobnost ponudbe.</span><span class="sxs-lookup"><span data-stu-id="a45a8-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="a45a8-178">**2. pravilo**: če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta**, je projekt in izbran razred transakcije mogoče vključiti samo v eno podrobnost ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="a45a8-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="a45a8-179">**3. pravilo**: če je polje **Vključena opravila** nastavljeno na **Samo izbrana opravila projekta**, je projekt in izbran razred transakcije mogoče vključiti v več podrobnosti ponudbe, ki temeljijo na projektu.</span><span class="sxs-lookup"><span data-stu-id="a45a8-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="a45a8-180">**4. pravilo** : če ima priložnost več ponudb, so lahko podrobnosti ponudbe za različne ponudbe, ki se vse sklicujejo na isti projekt in vključujejo isti razred transakcije.</span><span class="sxs-lookup"><span data-stu-id="a45a8-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="a45a8-181">**5. pravilo**: če ponudbe ne pripadajo isti priložnosti, ne morejo vključevati istega projekta in razreda transakcije.</span><span class="sxs-lookup"><span data-stu-id="a45a8-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="a45a8-182">
                    <strong>Priložnost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a45a8-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="a45a8-183">
                    <strong>Ponudba</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a45a8-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a45a8-184">
                    <strong>Podrobnost ponudbe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a45a8-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a45a8-185">
                    <strong>Projekt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a45a8-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="a45a8-186">
                    <strong>Vključena opravila</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a45a8-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="a45a8-187">
                    <strong>Vključi čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a45a8-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="a45a8-188">
                    <strong>Vključi strošek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a45a8-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="a45a8-189">
                    <strong>Vključi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a45a8-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="a45a8-190">
                    <strong>Dajatev</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a45a8-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="a45a8-191">
                    <strong>Veljavno/neveljavno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a45a8-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="a45a8-192">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a45a8-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a45a8-193">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-194">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-195">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-196">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-197">Prazno</span><span class="sxs-lookup"><span data-stu-id="a45a8-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-198">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-199">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-200">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a45a8-201">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="a45a8-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a45a8-202">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="a45a8-202">Violation of Rule #2.</span></span> <span data-ttu-id="a45a8-203">Čas, stroški in dajatve za projekt Proj1 so vključeni v podrobnosti ponudbe PodrPon1 in PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="a45a8-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a45a8-204">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-205">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-206">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="a45a8-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-207">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-208">Prazno</span><span class="sxs-lookup"><span data-stu-id="a45a8-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-209">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-210">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-211">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-211">Yes</span></span> </p>
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
<span data-ttu-id="a45a8-212">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-213">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-214">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-215">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-216">Prazno</span><span class="sxs-lookup"><span data-stu-id="a45a8-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-217">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-218">No</span><span class="sxs-lookup"><span data-stu-id="a45a8-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-219">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a45a8-220">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="a45a8-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a45a8-221">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="a45a8-221">Violation of Rule #2.</span></span> <span data-ttu-id="a45a8-222">Čas in dajatve za projekt Proj1 so vključeni v podrobnosti ponudbe PodrPon1 in PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="a45a8-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a45a8-223">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-224">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-225">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="a45a8-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-226">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-227">Prazno</span><span class="sxs-lookup"><span data-stu-id="a45a8-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-228">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-229">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-230">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-230">Yes</span></span> </p>
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
<span data-ttu-id="a45a8-231">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-232">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-233">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-234">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-235">Prazno</span><span class="sxs-lookup"><span data-stu-id="a45a8-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-236">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-237">No</span><span class="sxs-lookup"><span data-stu-id="a45a8-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-238">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a45a8-239">Veljavno</span><span class="sxs-lookup"><span data-stu-id="a45a8-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="a45a8-240">Čas in dajatve za projekt Proj1 so vključeni v PodrPon1.</span><span class="sxs-lookup"><span data-stu-id="a45a8-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="a45a8-241">Stroški za projekt P1 so vključeni v PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="a45a8-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="a45a8-242">Ni prekrivanja glede tega, kar je vključeno v vsako podrobnost ponudbe in je veljavno.</span><span class="sxs-lookup"><span data-stu-id="a45a8-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a45a8-243">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-244">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-245">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="a45a8-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-246">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-247">Prazno</span><span class="sxs-lookup"><span data-stu-id="a45a8-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-248">No</span><span class="sxs-lookup"><span data-stu-id="a45a8-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-249">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-250">No</span><span class="sxs-lookup"><span data-stu-id="a45a8-250">No</span></span> </p>
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
<span data-ttu-id="a45a8-251">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-252">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-253">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-254">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-255">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="a45a8-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-256">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-257">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-258">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a45a8-259">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="a45a8-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a45a8-260">Kršitev zgornjega 2. pravila</span><span class="sxs-lookup"><span data-stu-id="a45a8-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="a45a8-261">Pon1 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.</span><span class="sxs-lookup"><span data-stu-id="a45a8-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a45a8-262">PodrPon2 vključuje čas, stroške in dajatve za celoten projekt P1 ter se prekriva s tistim, kar je vključeno v Pon1.</span><span class="sxs-lookup"><span data-stu-id="a45a8-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a45a8-263">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-264">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-265">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="a45a8-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-266">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-267">Prazno</span><span class="sxs-lookup"><span data-stu-id="a45a8-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-268">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-269">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-270">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-270">Yes</span></span> </p>
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
<span data-ttu-id="a45a8-271">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-272">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-273">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-274">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-275">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="a45a8-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-276">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-277">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-278">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a45a8-279">Veljavno</span><span class="sxs-lookup"><span data-stu-id="a45a8-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a45a8-280">V skladu z zgornjim 3. pravilom</span><span class="sxs-lookup"><span data-stu-id="a45a8-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="a45a8-281">Pon1 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.</span><span class="sxs-lookup"><span data-stu-id="a45a8-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a45a8-282">Pon2 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.</span><span class="sxs-lookup"><span data-stu-id="a45a8-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="a45a8-283">Edino dodatno preverjanje velja okoli podmnožice opravil v PodrPon1, ki se razlikujejo od podmnožice nalog v PodrPon2.</span><span class="sxs-lookup"><span data-stu-id="a45a8-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="a45a8-284">To zagotavlja, da ne bo prekrivanja.</span><span class="sxs-lookup"><span data-stu-id="a45a8-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="a45a8-285">To opravi sistem, ko so opravila povezana.</span><span class="sxs-lookup"><span data-stu-id="a45a8-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a45a8-286">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-287">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-288">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="a45a8-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-289">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-290">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="a45a8-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-291">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-292">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-293">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-293">Yes</span></span> </p>
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
<span data-ttu-id="a45a8-294">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-295">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-296">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-297">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-298">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="a45a8-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-299">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-300">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-301">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="a45a8-302">Veljavno</span><span class="sxs-lookup"><span data-stu-id="a45a8-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a45a8-303">Glede na 5. pravilo sta Pon1 in Pon2 dve ponudbi za isto priložnost, tako da lahko oba ocenjujeta enake komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="a45a8-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a45a8-304">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-305">Pon2</span><span class="sxs-lookup"><span data-stu-id="a45a8-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-306">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-307">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-308">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="a45a8-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-309">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-310">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-311">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-311">Yes</span></span> </p>
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
<span data-ttu-id="a45a8-312">Pril1</span><span class="sxs-lookup"><span data-stu-id="a45a8-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-313">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-314">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-315">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-316">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="a45a8-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-317">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-318">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-319">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="a45a8-320">Veljavno</span><span class="sxs-lookup"><span data-stu-id="a45a8-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a45a8-321">Glede na 4. pravilo sta Pon1 in Pon2 dve ponudbi za različni priložnosti, tako da ne moreta obe ocenjevati enakih komponent istega projekta.</span><span class="sxs-lookup"><span data-stu-id="a45a8-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="a45a8-322">Pril2</span><span class="sxs-lookup"><span data-stu-id="a45a8-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="a45a8-323">Pon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-324">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="a45a8-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-325">Proj1</span><span class="sxs-lookup"><span data-stu-id="a45a8-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="a45a8-326">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="a45a8-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-327">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="a45a8-328">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="a45a8-329">Da</span><span class="sxs-lookup"><span data-stu-id="a45a8-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="a45a8-330">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="a45a8-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]