---
title: Pregled podrobnosti ponudb, ki temeljijo na projektih
description: Ta tema vsebuje informacije o uporabi podrobnosti ponudb, ki temeljijo na projektih, za projektno delo.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369891"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="e1d7f-103">Pregled podrobnosti ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="e1d7f-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="e1d7f-104">_**Velja za:** poenostavljeno uvedbo – posel do izstavitve predračuna, Project Operations za primere, ki temeljijo na virih/nezalogi_</span><span class="sxs-lookup"><span data-stu-id="e1d7f-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e1d7f-105">Podrobnosti ponudb, ki temeljijo na projektu, so oblikovane tako, da pripomorejo k oceni projektnega dela v okviru interakcije.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="e1d7f-106">Struktura podrobnosti ponudb, ki temelji na projektu, je razširjena za ocene projektov z naslednjimi koncepti:</span><span class="sxs-lookup"><span data-stu-id="e1d7f-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="e1d7f-107">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="e1d7f-107">Billing Method</span></span>
- <span data-ttu-id="e1d7f-108">Preslikavanje projektov in opravil</span><span class="sxs-lookup"><span data-stu-id="e1d7f-108">Project and Task Mapping</span></span>
- <span data-ttu-id="e1d7f-109">Vključuje razrede transakcij</span><span class="sxs-lookup"><span data-stu-id="e1d7f-109">Included Transaction classes</span></span>
- <span data-ttu-id="e1d7f-110">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="e1d7f-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="e1d7f-111">Nastavitev možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="e1d7f-111">Chargeability setup</span></span>
- <span data-ttu-id="e1d7f-112">Ocena z uporabo podrobnosti ponudb</span><span class="sxs-lookup"><span data-stu-id="e1d7f-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="e1d7f-113">Stranke podrobnosti ponudbe</span><span class="sxs-lookup"><span data-stu-id="e1d7f-113">Quote line Customers</span></span>

<span data-ttu-id="e1d7f-114">Naslednja tabela vsebuje informacije o poljih na zavihku **Splošno** pri podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="e1d7f-115">Ta polja pomagajo nastaviti osnovo za podrobno, temeljito oceno projektnega dela.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="e1d7f-116">**Polje**</span><span class="sxs-lookup"><span data-stu-id="e1d7f-116">**Field**</span></span> | <span data-ttu-id="e1d7f-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="e1d7f-117">**Description**</span></span> | <span data-ttu-id="e1d7f-118">**Nadaljnji vpliv**</span><span class="sxs-lookup"><span data-stu-id="e1d7f-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e1d7f-119">Imenu</span><span class="sxs-lookup"><span data-stu-id="e1d7f-119">Name</span></span> | <span data-ttu-id="e1d7f-120">Ime vrstice ponudbe, ki vam pomaga prepoznati posamezno komponento ponudbe, ki se ocenjuje.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="e1d7f-121">Kopirano v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1d7f-122">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="e1d7f-122">Billing Method</span></span> | <span data-ttu-id="e1d7f-123">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="e1d7f-124">To polje vključuje dva glavna pogodbena modela, ki sta podprta v aplikaciji Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="e1d7f-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="e1d7f-125">- fiksna cena</span><span class="sxs-lookup"><span data-stu-id="e1d7f-125">- Fixed price</span></span></br><span data-ttu-id="e1d7f-126">- čas in material</span><span class="sxs-lookup"><span data-stu-id="e1d7f-126">- Time and material.</span></span>| <span data-ttu-id="e1d7f-127">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1d7f-128">Project</span><span class="sxs-lookup"><span data-stu-id="e1d7f-128">Project</span></span> | <span data-ttu-id="e1d7f-129">S tem izbirnim poljem določite projekt, ki se bo uporabljal za izvedbo dela za to interakcijo.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="e1d7f-130">Ko je projekt preslikan v podrobnost ponudbe, pripomore k nastavitvi opravil, ki se zaračunajo, in tudi k pripravi ocene, ki temelji na projektu, pri vrstici ponudbe v obliki podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="e1d7f-131">Če projekt ni preslikan na vrstico ponudbe, ki temelji na projektu, morate oceno ustvariti ročno z izdelavo vsake podrobnosti vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="e1d7f-132">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="e1d7f-133">Vključena opravila</span><span class="sxs-lookup"><span data-stu-id="e1d7f-133">Included Tasks</span></span> | <span data-ttu-id="e1d7f-134">Označuje, ali se ta podrobnost ponudbe uporablja za vsa ali nekatera projektna opravila za izbrani projekt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="e1d7f-135">To polje ima lahko naslednje vrednosti:</span><span class="sxs-lookup"><span data-stu-id="e1d7f-135">This field has the following possible values:</span></span></br><span data-ttu-id="e1d7f-136">- vsa opravila projekta</span><span class="sxs-lookup"><span data-stu-id="e1d7f-136">- All project tasks</span></span></br><span data-ttu-id="e1d7f-137">- samo izbrana opravila projekta</span><span class="sxs-lookup"><span data-stu-id="e1d7f-137">- Selected project tasks only</span></span></br><span data-ttu-id="e1d7f-138">Prazna vrednost v tem polju je enaka možnosti **Vsa projektna opravila**.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="e1d7f-139">Ko je na strani projekta izbrana možnost **Samo izbrane projektne naloge**, zavihek **Nastavitev obračunavanja opravil** omogoča, da izberete določena opravila in jih povežete s to vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="e1d7f-140">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1d7f-141">Vključi čas</span><span class="sxs-lookup"><span data-stu-id="e1d7f-141">Include Time</span></span> | <span data-ttu-id="e1d7f-142">Vrednost **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1d7f-143">Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1d7f-144">Vrednost **Da** označuje, da bodo časovne transakcije ali stroški dela vključeni v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e1d7f-145">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1d7f-146">Vključi strošek</span><span class="sxs-lookup"><span data-stu-id="e1d7f-146">Include Expense</span></span> | <span data-ttu-id="e1d7f-147">Vrednost **Da**/**Ne** označuje, ali bodo stroški za izbrani projekt vključeni v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1d7f-148">Vrednost **Ne** označuje, da strošek ne bo vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1d7f-149">Vrednost **Ne** označuje, da bo strošek vključen v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e1d7f-150">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1d7f-151">Vključi material</span><span class="sxs-lookup"><span data-stu-id="e1d7f-151">Include Material</span></span> | <span data-ttu-id="e1d7f-152">Vrednost **Da**/**Ne** označuje, ali bodo stroški materiala za izbrani projekt vključeni v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1d7f-153">Vrednost **Ne** označuje, da stroški materiala ne bodo vključeni v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1d7f-154">Vrednost **Ja** označuje, da bodo stroški materiala vključeni v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e1d7f-155">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1d7f-156">Vključi dajatev</span><span class="sxs-lookup"><span data-stu-id="e1d7f-156">Include Fee</span></span> | <span data-ttu-id="e1d7f-157">Vrednost **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključene v oceno v tej vrstici ponudb.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1d7f-158">Vrednost **Ne** označuje, da dajatve ne bodo vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e1d7f-159">Vrednost **Da** označuje, da bodo dajatve vključene v oceno v tej vrstici ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e1d7f-160">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1d7f-161">Znesek ponudbe</span><span class="sxs-lookup"><span data-stu-id="e1d7f-161">Quoted Amount</span></span> | <span data-ttu-id="e1d7f-162">To je znesek, ki bo stranki naveden za vse napovedano delo v tej vrstici ponudb, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="e1d7f-163">V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz polja **Proračun stranke** v vrstici priložnosti.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="e1d7f-164">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="e1d7f-165">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1d7f-166">Predvideni davek</span><span class="sxs-lookup"><span data-stu-id="e1d7f-166">Estimated Tax</span></span> | <span data-ttu-id="e1d7f-167">To je polje, ki ga je mogoče urejati in v katerem lahko uporabnik doda predviden znesek davka v vrstico ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="e1d7f-168">Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska davka v podrobnostih vrstice ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="e1d7f-169">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1d7f-170">Znesek ponudbe po obdavčitvi</span><span class="sxs-lookup"><span data-stu-id="e1d7f-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="e1d7f-171">To polje je znesek v podrobnosti ponudbe po obdavčitvi in je samo za branje.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="e1d7f-172">Znesek v tem polju se izračuna kot *znesek ponudbe + davek*.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="e1d7f-173">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1d7f-174">Omejitev »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="e1d7f-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="e1d7f-175">To polje je mogoče urejati in je na voljo samo v podrobnostih ponudb, ki temeljijo na projektih in imajo način obračunavanja **Čas in material**.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="e1d7f-176">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e1d7f-177">Proračun stranke</span><span class="sxs-lookup"><span data-stu-id="e1d7f-177">Customer Budget</span></span> | <span data-ttu-id="e1d7f-178">To polje je mogoče urejati in se kopira iz ustreznega polja v vrstici priložnosti, če je bila ponudba ustvarjena iz priložnosti.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="e1d7f-179">Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="e1d7f-180">Pravila za preverjanje veljavnosti polj na zavihku Splošno v podrobnostih ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="e1d7f-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="e1d7f-181">**1. pravilo**: če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta**, je projekt vključen v podrobnost ponudbe.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="e1d7f-182">**2. pravilo**: če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta**, je projekt in izbran razred transakcije mogoče vključiti samo v eno podrobnost ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="e1d7f-183">**3. pravilo**: če je polje **Vključena opravila** nastavljeno na **Samo izbrana opravila projekta**, je projekt in izbran razred transakcije mogoče vključiti v več podrobnosti ponudbe, ki temeljijo na projektu.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="e1d7f-184">**4. pravilo** : če ima priložnost več ponudb, so lahko podrobnosti ponudbe za različne ponudbe, ki se vse sklicujejo na isti projekt in vključujejo isti razred transakcije.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="e1d7f-185">**5. pravilo**: če ponudbe ne pripadajo isti priložnosti, ne morejo vključevati istega projekta in razreda transakcije.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="e1d7f-186">
                    <strong>Priložnost</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="e1d7f-187">
                    <strong>Ponudba</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="e1d7f-188">
                    <strong>Podrobnost ponudbe</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="e1d7f-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="e1d7f-190">
                    <strong>Vključena opravila</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="e1d7f-191">
                    <strong>Vključi čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="e1d7f-192">
                    <strong>Vključi strošek</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="e1d7f-193">
                    <strong>Vključi material</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="e1d7f-194">
                    <strong>Vključi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="e1d7f-195">
                    <strong>Dajatev</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="e1d7f-196">
                    <strong>Veljavno/neveljavno</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="e1d7f-197">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e1d7f-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e1d7f-198">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-199">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-200">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-201">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-202">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-203">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-204">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-205">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-206">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-207">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-208">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-208">Violation of Rule #2.</span></span> <span data-ttu-id="e1d7f-209">Čas, stroški in dajatve za projekt P1 so vključeni v podrobnosti ponudbe QL1 in QL2</span><span class="sxs-lookup"><span data-stu-id="e1d7f-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e1d7f-210">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-211">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-212">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="e1d7f-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-213">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-214">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-215">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-216">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-217">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-218">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-218">Yes</span></span> </p>
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
<span data-ttu-id="e1d7f-219">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-220">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-221">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-222">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-223">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-224">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-225">No</span><span class="sxs-lookup"><span data-stu-id="e1d7f-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-226">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-227">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-228">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-229">Kršitev 2. pravila.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-229">Violation of Rule #2.</span></span> <span data-ttu-id="e1d7f-230">Čas, material in dajatve za projekt P1 so vključeni v podrobnosti ponudbe QL1 in QL2</span><span class="sxs-lookup"><span data-stu-id="e1d7f-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e1d7f-231">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-232">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-233">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="e1d7f-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-234">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-235">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-236">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-237">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-238">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-239">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-239">Yes</span></span> </p>
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
<span data-ttu-id="e1d7f-240">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-241">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-242">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-243">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-244">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-245">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-246">No</span><span class="sxs-lookup"><span data-stu-id="e1d7f-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-247">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-248">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-249">Veljavno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-250">Čas, material in dajatve za projekt P1 so vključeni v QL1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="e1d7f-251">Stroški za projekt P1 so vključeni v QL2</span><span class="sxs-lookup"><span data-stu-id="e1d7f-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="e1d7f-252">Ni prekrivanja tega, kar je vključeno v vsako vrstico ponudbe in je zato veljavno.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e1d7f-253">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-254">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-255">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="e1d7f-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-256">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-257">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-258">No</span><span class="sxs-lookup"><span data-stu-id="e1d7f-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-259">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-260">No</span><span class="sxs-lookup"><span data-stu-id="e1d7f-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-261">No</span><span class="sxs-lookup"><span data-stu-id="e1d7f-261">No</span></span> </p>
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
<span data-ttu-id="e1d7f-262">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-263">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-264">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-265">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-266">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="e1d7f-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-267">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-268">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-269">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-270">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-271">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-272">Kršitev 2. pravila</span><span class="sxs-lookup"><span data-stu-id="e1d7f-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="e1d7f-273">Q1 vključuje čas, material, stroške in nadomestila za podmnožico opravil v projektu P1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="e1d7f-274">QL2 vključuje čas, stroške in dajatve za celoten projekt P1 in se torej prekriva s tem, kar je vključeno v Q1.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e1d7f-275">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-276">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-277">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="e1d7f-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-278">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-279">Prazno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-280">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-281">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-282">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-283">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-283">Yes</span></span> </p>
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
<span data-ttu-id="e1d7f-284">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-285">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-286">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-287">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-288">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="e1d7f-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-289">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-290">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-291">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-292">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-293">Veljavno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-294">Po 3. pravilu,</span><span class="sxs-lookup"><span data-stu-id="e1d7f-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="e1d7f-295">Q1 vključuje čas, material, stroške in nadomestila za podmnožico opravil v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e1d7f-296">QL2 vključuje čas, material, stroške in nadomestila za podmnožico opravil v projektu P1.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e1d7f-297">Edino dodatno preverjanje se izvaja okoli podmnožice opravil za QL1, ki se razlikuje od podmnožice opravil za QL2, da se prepreči prekrivanje.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="e1d7f-298">To opravi sistem, ko so opravila povezana.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e1d7f-299">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-300">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-301">PodrPon2</span><span class="sxs-lookup"><span data-stu-id="e1d7f-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-302">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-303">Samo izbrana opravila</span><span class="sxs-lookup"><span data-stu-id="e1d7f-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-304">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-305">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-306">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-307">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-307">Yes</span></span> </p>
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
<span data-ttu-id="e1d7f-308">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-309">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-310">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-311">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-312">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-313">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-314">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-315">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-316">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-317">Veljavno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-318">Po 5. pravilu sta Q1 in Q2 dve ponudbi za isto priložnost, tako da lahko obe ocenjujeta enake komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e1d7f-319">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-320">2. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-321">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-322">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-323">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-324">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-325">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-326">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-327">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-327">Yes</span></span> </p>
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
<span data-ttu-id="e1d7f-328">Pril1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-329">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-330">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-331">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-332">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-333">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-334">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-335">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-336">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-337">Neveljavno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e1d7f-338">Po 4. pravilu sta Q1 in Q2 dve ponudbi za različni priložnosti, tako da ne moreta obe ocenjevati enakih komponente istega projekta.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e1d7f-339">Pril2</span><span class="sxs-lookup"><span data-stu-id="e1d7f-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e1d7f-340">1. četrt.</span><span class="sxs-lookup"><span data-stu-id="e1d7f-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e1d7f-341">PodrPon1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-342">O1</span><span class="sxs-lookup"><span data-stu-id="e1d7f-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e1d7f-343">Vsa opravila projekta ali prazno</span><span class="sxs-lookup"><span data-stu-id="e1d7f-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e1d7f-344">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e1d7f-345">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e1d7f-346">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e1d7f-347">Da</span><span class="sxs-lookup"><span data-stu-id="e1d7f-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
