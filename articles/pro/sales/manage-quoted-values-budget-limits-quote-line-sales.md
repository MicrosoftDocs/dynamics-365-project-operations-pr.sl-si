---
title: Pregled podrobnosti ponudb, ki temeljijo na projektih
description: Ta tema vsebuje informacije o uporabi podrobnosti ponudb, ki temeljijo na projektih, za projektno delo.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858718"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="47b14-103">Pregled podrobnosti ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="47b14-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="47b14-104">_**Velja za:** poenostavljeno uvedbo – posel do izstavitve predračuna, Project Operations za primere, ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="47b14-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="47b14-105">Podrobnosti ponudb, ki temeljijo na projektu, so oblikovane tako, da pripomorejo k oceni projektnega dela v okviru interakcije.</span><span class="sxs-lookup"><span data-stu-id="47b14-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="47b14-106">Struktura podrobnosti ponudb, ki temelji na projektu, je razširjena za ocene projektov z naslednjimi koncepti:</span><span class="sxs-lookup"><span data-stu-id="47b14-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="47b14-107">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="47b14-107">Billing Method</span></span>
- <span data-ttu-id="47b14-108">Preslikavanje projektov in opravil</span><span class="sxs-lookup"><span data-stu-id="47b14-108">Project and Task Mapping</span></span>
- <span data-ttu-id="47b14-109">Vključuje razrede transakcij</span><span class="sxs-lookup"><span data-stu-id="47b14-109">Included Transaction classes</span></span>
- <span data-ttu-id="47b14-110">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="47b14-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="47b14-111">Nastavitev možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="47b14-111">Chargeability setup</span></span>
- <span data-ttu-id="47b14-112">Ocena z uporabo podrobnosti ponudb</span><span class="sxs-lookup"><span data-stu-id="47b14-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="47b14-113">Stranke podrobnosti ponudbe</span><span class="sxs-lookup"><span data-stu-id="47b14-113">Quote line Customers</span></span>

<span data-ttu-id="47b14-114">Naslednja tabela vsebuje informacije o poljih na zavihku **Splošno** pri podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="47b14-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="47b14-115">Ta polja pomagajo nastaviti osnovo za podrobno, temeljito oceno projektnega dela.</span><span class="sxs-lookup"><span data-stu-id="47b14-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="47b14-116">**Polje**</span><span class="sxs-lookup"><span data-stu-id="47b14-116">**Field**</span></span> | <span data-ttu-id="47b14-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="47b14-117">**Description**</span></span> | <span data-ttu-id="47b14-118">**Nadaljnji vpliv**</span><span class="sxs-lookup"><span data-stu-id="47b14-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="47b14-119">Imenu</span><span class="sxs-lookup"><span data-stu-id="47b14-119">Name</span></span> | <span data-ttu-id="47b14-120">Ime vrstice ponudbe, ki vam pomaga prepoznati posamezno komponento ponudbe, ki se ocenjuje.</span><span class="sxs-lookup"><span data-stu-id="47b14-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="47b14-121">Kopirano v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="47b14-122">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="47b14-122">Billing Method</span></span> | <span data-ttu-id="47b14-123">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="47b14-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="47b14-124">To polje vključuje dva glavna pogodbena modela, ki sta podprta v aplikaciji Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="47b14-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="47b14-125">- fiksna cena</span><span class="sxs-lookup"><span data-stu-id="47b14-125">- Fixed price</span></span></br><span data-ttu-id="47b14-126">- čas in material</span><span class="sxs-lookup"><span data-stu-id="47b14-126">- Time and material.</span></span>| <span data-ttu-id="47b14-127">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="47b14-128">Project</span><span class="sxs-lookup"><span data-stu-id="47b14-128">Project</span></span> | <span data-ttu-id="47b14-129">S tem izbirnim poljem določite projekt, ki se bo uporabljal za izvedbo dela za to interakcijo.</span><span class="sxs-lookup"><span data-stu-id="47b14-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="47b14-130">Ko je projekt preslikan v podrobnost ponudbe, pripomore k nastavitvi opravil, ki se zaračunajo, in tudi k pripravi ocene, ki temelji na projektu, pri vrstici ponudbe v obliki podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="47b14-131">Če projekt ni preslikan na vrstico ponudbe, ki temelji na projektu, morate oceno ustvariti ročno z izdelavo vsake podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="47b14-132">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="47b14-133">Vključena opravila</span><span class="sxs-lookup"><span data-stu-id="47b14-133">Included Tasks</span></span> | <span data-ttu-id="47b14-134">Označuje, ali se ta podrobnost ponudbe uporablja za vsa ali nekatera projektna opravila za izbrani projekt.</span><span class="sxs-lookup"><span data-stu-id="47b14-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="47b14-135">To polje ima lahko naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="47b14-135">This field has the following possible values:</span></span></br><span data-ttu-id="47b14-136">- vsa opravila projekta</span><span class="sxs-lookup"><span data-stu-id="47b14-136">- All project tasks</span></span></br><span data-ttu-id="47b14-137">- samo izbrana opravila projekta</span><span class="sxs-lookup"><span data-stu-id="47b14-137">- Selected project tasks only</span></span></br><span data-ttu-id="47b14-138">Prazna vrednost v tem polju je enaka možnosti **Vsa projektna opravila**.</span><span class="sxs-lookup"><span data-stu-id="47b14-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="47b14-139">Ko je na strani projekta izbrana možnost **Samo izbrane projektne naloge**, zavihek **Nastavitev obračunavanja opravil** omogoča, da izberete določena opravila in jih povežete s to vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="47b14-140">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="47b14-141">Vključi čas</span><span class="sxs-lookup"><span data-stu-id="47b14-141">Include Time</span></span> | <span data-ttu-id="47b14-142">Vrednost **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="47b14-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="47b14-143">Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="47b14-144">Vrednost **Da** označuje, da bodo časovne transakcije ali stroški dela vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="47b14-145">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="47b14-146">Vključi strošek</span><span class="sxs-lookup"><span data-stu-id="47b14-146">Include Expense</span></span> | <span data-ttu-id="47b14-147">Vrednost **Da**/**Ne** označuje, ali bodo stroški za izbrani projekt vključeni v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="47b14-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="47b14-148">Vrednost **Ne** označuje, da strošek ne bo vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="47b14-149">Vrednost **Ne** označuje, da bo strošek vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="47b14-150">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="47b14-151">Vključi material</span><span class="sxs-lookup"><span data-stu-id="47b14-151">Include Material</span></span> | <span data-ttu-id="47b14-152">Vrednost **Da**/**Ne** označuje, ali bodo stroški materiala za izbrani projekt vključeni v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="47b14-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="47b14-153">Vrednost **Ne** označuje, da stroški materiala ne bodo vključeni v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="47b14-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="47b14-154">Vrednost **Ja** označuje, da bodo stroški materiala vključeni v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="47b14-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="47b14-155">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="47b14-156">Vključi dajatev</span><span class="sxs-lookup"><span data-stu-id="47b14-156">Include Fee</span></span> | <span data-ttu-id="47b14-157">Vrednost **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključene v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="47b14-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="47b14-158">Vrednost **Ne** označuje, da dajatve ne bodo vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="47b14-159">Vrednost **Da** označuje, da bodo dajatve vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="47b14-160">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="47b14-161">Znesek ponudbe</span><span class="sxs-lookup"><span data-stu-id="47b14-161">Quoted Amount</span></span> | <span data-ttu-id="47b14-162">To je znesek, ki bo stranki naveden za vse napovedano delo v tej vrstici ponudb, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="47b14-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="47b14-163">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz polja **Proračun stranke** v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="47b14-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="47b14-164">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="47b14-165">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="47b14-166">Predvideni davek</span><span class="sxs-lookup"><span data-stu-id="47b14-166">Estimated Tax</span></span> | <span data-ttu-id="47b14-167">To je polje, ki ga je mogoče urejati in v katerem lahko uporabnik doda predviden znesek davka v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="47b14-168">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska davka v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="47b14-169">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="47b14-170">Znesek ponudbe po obdavčitvi</span><span class="sxs-lookup"><span data-stu-id="47b14-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="47b14-171">To polje je znesek v podrobnosti ponudbe po obdavčitvi in je samo za branje.</span><span class="sxs-lookup"><span data-stu-id="47b14-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="47b14-172">Znesek v tem polju se izračuna kot *znesek ponudbe + davek*.</span><span class="sxs-lookup"><span data-stu-id="47b14-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="47b14-173">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="47b14-174">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="47b14-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="47b14-175">To polje je mogoče urejati in je na voljo samo v podrobnostih ponudb, ki temeljijo na projektih in imajo način obračunavanja **Čas in material**.</span><span class="sxs-lookup"><span data-stu-id="47b14-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="47b14-176">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="47b14-177">Proračun stranke</span><span class="sxs-lookup"><span data-stu-id="47b14-177">Customer Budget</span></span> | <span data-ttu-id="47b14-178">To polje je mogoče urejati in se kopira iz ustreznega polja v vrstici priložnosti, če je bila ponudba ustvarjena iz priložnosti.</span><span class="sxs-lookup"><span data-stu-id="47b14-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="47b14-179">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="47b14-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="47b14-180">Pravila za preverjanje veljavnosti polj na zavihku Splošno v podrobnostih ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="47b14-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="47b14-181">**1. pravilo**: če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta**, je projekt vključen v podrobnost ponudbe.</span><span class="sxs-lookup"><span data-stu-id="47b14-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="47b14-182">**2. pravilo**: če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta**, je projekt in izbran razred transakcije mogoče vključiti samo v eno podrobnost ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="47b14-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="47b14-183">**3. pravilo**: če je polje **Vključena opravila** nastavljeno na **Samo izbrana opravila projekta**, je projekt in izbran razred transakcije mogoče vključiti v več podrobnosti ponudbe, ki temeljijo na projektu.</span><span class="sxs-lookup"><span data-stu-id="47b14-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="47b14-184">**4. pravilo** : če ima priložnost več ponudb, so lahko podrobnosti ponudbe za različne ponudbe, ki se vse sklicujejo na isti projekt in vključujejo isti razred transakcije.</span><span class="sxs-lookup"><span data-stu-id="47b14-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="47b14-185">**5. pravilo**: če ponudbe ne pripadajo isti priložnosti, ne morejo vključevati istega projekta in razreda transakcije.</span><span class="sxs-lookup"><span data-stu-id="47b14-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="47b14-186">
                    <strong>Priložnost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="47b14-187">
                    <strong>Ponudba</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="47b14-188">
                    <strong>Podrobnost ponudbe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="47b14-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="47b14-190">
                    <strong>Vključena opravila</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="47b14-191">
                    <strong>Vključi čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="47b14-192">
                    <strong>Vključi strošek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="47b14-193">
                    <strong>Vključi material</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="47b14-194">
                    <strong>Vključi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="47b14-195">
                    <strong>Dajatev</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="47b14-196">
                    <strong>Veljavno/neveljavno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="47b14-197">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="47b14-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-198">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-199">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-200">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="47b14-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-201">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-202">Prazno</span><span class="sxs-lookup"><span data-stu-id="47b14-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-203">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-204">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-205">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-206">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-207">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="47b14-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-208">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="47b14-208">Violation of Rule #2.</span></span> <span data-ttu-id="47b14-209">Čas, stroški in dajatve za projekt P1 so vključeni v podrobnosti ponudbe QL1 in QL2</span><span class="sxs-lookup"><span data-stu-id="47b14-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-210">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-211">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-212">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="47b14-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-213">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-214">Prazno</span><span class="sxs-lookup"><span data-stu-id="47b14-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-215">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-216">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-217">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-218">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-219">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-220">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-221">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="47b14-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-222">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-223">Prazno</span><span class="sxs-lookup"><span data-stu-id="47b14-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-224">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-225">No</span><span class="sxs-lookup"><span data-stu-id="47b14-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-226">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-227">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-228">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="47b14-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-229">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="47b14-229">Violation of Rule #2.</span></span> <span data-ttu-id="47b14-230">Čas, material in dajatve za projekt P1 so vključeni v podrobnosti ponudbe QL1 in QL2</span><span class="sxs-lookup"><span data-stu-id="47b14-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-231">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-232">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-233">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="47b14-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-234">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-235">Prazno</span><span class="sxs-lookup"><span data-stu-id="47b14-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-236">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-237">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-238">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-239">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-240">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-241">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-242">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="47b14-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-243">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-244">Prazno</span><span class="sxs-lookup"><span data-stu-id="47b14-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-245">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-246">No</span><span class="sxs-lookup"><span data-stu-id="47b14-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-247">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-248">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-249">Veljavno</span><span class="sxs-lookup"><span data-stu-id="47b14-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-250">Čas, material in dajatve za projekt P1 so vključeni v QL1</span><span class="sxs-lookup"><span data-stu-id="47b14-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="47b14-251">Stroški za projekt P1 so vključeni v QL2</span><span class="sxs-lookup"><span data-stu-id="47b14-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="47b14-252">Ni prekrivanja tega, kar je vključeno v vsako vrstico ponudbe in je zato veljavno.</span><span class="sxs-lookup"><span data-stu-id="47b14-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-253">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-254">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-255">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="47b14-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-256">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-257">Prazno</span><span class="sxs-lookup"><span data-stu-id="47b14-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-258">No</span><span class="sxs-lookup"><span data-stu-id="47b14-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-259">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-260">No</span><span class="sxs-lookup"><span data-stu-id="47b14-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-261">No</span><span class="sxs-lookup"><span data-stu-id="47b14-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-262">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-263">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-264">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="47b14-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-265">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-266">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="47b14-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-267">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-268">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-269">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-270">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-271">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="47b14-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-272">Kršitev 2. pravila</span><span class="sxs-lookup"><span data-stu-id="47b14-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="47b14-273">Q1 vključuje čas, material, stroške in nadomestila za podmnožico opravil v projektu P1</span><span class="sxs-lookup"><span data-stu-id="47b14-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="47b14-274">QL2 vključuje čas, stroške in dajatve za celoten projekt P1 in se torej prekriva s tem, kar je vključeno v Q1.</span><span class="sxs-lookup"><span data-stu-id="47b14-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-275">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-276">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-277">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="47b14-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-278">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-279">Prazno</span><span class="sxs-lookup"><span data-stu-id="47b14-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-280">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-281">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-282">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-283">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-284">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-285">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-286">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="47b14-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-287">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-288">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="47b14-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-289">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-290">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-291">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-292">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-293">Veljavno</span><span class="sxs-lookup"><span data-stu-id="47b14-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-294">Po 3. pravilu,</span><span class="sxs-lookup"><span data-stu-id="47b14-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="47b14-295">Q1 vključuje čas, material, stroške in nadomestila za podmnožico opravil v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="47b14-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="47b14-296">QL2 vključuje čas, material, stroške in nadomestila za podmnožico opravil v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="47b14-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="47b14-297">Edino dodatno preverjanje se izvaja okoli podmnožice opravil za QL1, ki se razlikuje od podmnožice opravil za QL2, da se prepreči prekrivanje.</span><span class="sxs-lookup"><span data-stu-id="47b14-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="47b14-298">To opravi sistem, ko so opravila povezana.</span><span class="sxs-lookup"><span data-stu-id="47b14-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-299">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-300">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-301">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="47b14-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-302">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-303">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="47b14-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-304">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-305">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-306">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-307">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-308">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-309">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-310">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="47b14-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-311">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-312">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="47b14-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-313">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-314">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-315">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-316">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-317">Veljavno</span><span class="sxs-lookup"><span data-stu-id="47b14-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-318">Po 5. pravilu sta Q1 in Q2 dve ponudbi za isto priložnost, tako da lahko obe ocenjujeta enake komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="47b14-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-319">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-320">2. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-321">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="47b14-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-322">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-323">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="47b14-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-324">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-325">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-326">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-327">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-328">Pril1</span><span class="sxs-lookup"><span data-stu-id="47b14-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-329">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-330">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="47b14-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-331">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-332">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="47b14-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-333">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-334">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-335">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-336">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-337">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="47b14-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="47b14-338">Po 4. pravilu sta Q1 in Q2 dve ponudbi za različni priložnosti, tako da ne moreta obe ocenjevati enakih komponente istega projekta.</span><span class="sxs-lookup"><span data-stu-id="47b14-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="47b14-339">Pril2</span><span class="sxs-lookup"><span data-stu-id="47b14-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="47b14-340">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="47b14-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="47b14-341">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="47b14-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-342">O1</span><span class="sxs-lookup"><span data-stu-id="47b14-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="47b14-343">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="47b14-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="47b14-344">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="47b14-345">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="47b14-346">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="47b14-347">Da</span><span class="sxs-lookup"><span data-stu-id="47b14-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
