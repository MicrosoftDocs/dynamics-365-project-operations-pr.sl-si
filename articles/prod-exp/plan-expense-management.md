---
title: Konfiguracija upravljanja stroškov
description: V tem članku so opisani dejavniki in odločitve, ki jih morate upoštevati med postopkom načrtovanja, preden konfigurirate upravljanje stroškov v storitvi Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271373"
---
# <a name="configure-expense-management"></a><span data-ttu-id="405d8-103">Konfiguracija upravljanja stroškov</span><span class="sxs-lookup"><span data-stu-id="405d8-103">Configure expense management</span></span>

<span data-ttu-id="405d8-104">V tej temi so opisani dejavniki in odločitve, ki jih morate upoštevati med postopkom načrtovanja, preden konfigurirate upravljanje stroškov.</span><span class="sxs-lookup"><span data-stu-id="405d8-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="405d8-105">V prostoru za upravljanje stroškov lahko shranite podatke o načinih plačila, zahtevah za pot, poročilih o stroških, pravilnikih itd.</span><span class="sxs-lookup"><span data-stu-id="405d8-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="405d8-106">Ker veliko odločitev, ki jih sprejmete, ko načrtujete konfiguracijo upravljanja odhodkov, temelji na hierarhiji in finančni strukturi vaše organizacije, se morate sklicevati na dokumente načrtovanja za ta področja.</span><span class="sxs-lookup"><span data-stu-id="405d8-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="405d8-107">Medpodjetniški stroški</span><span class="sxs-lookup"><span data-stu-id="405d8-107">Intercompany expenses</span></span>

<span data-ttu-id="405d8-108">Ko omogočite medpodjetniške stroške, pravnim osebam in zaposlenim omogočite, da ustvarijo stroške v imenu druge pravne osebe in poberejo plačilo od pravne osebe za zaposlitev v vaši organizaciji.</span><span class="sxs-lookup"><span data-stu-id="405d8-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="405d8-109">Na primer, zaposleni prek pravne osebe A zaključi projekt za pravno osebo B, v okviru projekta pa nastanejo stroški, povezani s potovanjem.</span><span class="sxs-lookup"><span data-stu-id="405d8-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="405d8-110">Če so medpodjetniški stroški omogočeni, lahko zaposleni nato vloži poročilo o stroških, ki bo stroške knjižilo pravni osebi B, strošek pa mora plačati pravna oseba A. Če vaša organizacija nima več kot ene pravne osebe, vam ni treba omogočiti medpodjetniške stroške.</span><span class="sxs-lookup"><span data-stu-id="405d8-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="405d8-111">**Odločitev:** Ali želite omogočiti medpodjetniške stroške?</span><span class="sxs-lookup"><span data-stu-id="405d8-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="405d8-112">Finančno upravljanje</span><span class="sxs-lookup"><span data-stu-id="405d8-112">Financial management</span></span>

<span data-ttu-id="405d8-113">Upravljanje stroškov je tesno povezano s finančnim upravljanjem vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="405d8-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="405d8-114">Veliko konfiguracije za upravljanje stroškov bo temeljilo na odločitvah, ki ste jih sprejeli glede financ vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="405d8-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="405d8-115">Naslednji razdelki opisujejo različna področja, ki zahtevajo načrtovanje in odločitve, ki temeljijo na finančnih odločitvah vaše organizacije in navodilih vodstvene ekipe.</span><span class="sxs-lookup"><span data-stu-id="405d8-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="405d8-116">Dnevnice</span><span class="sxs-lookup"><span data-stu-id="405d8-116">Per diems</span></span>

<span data-ttu-id="405d8-117">Določiti morate dnevnice za zaposlene, ki jih zagotavlja vaša organizacija.</span><span class="sxs-lookup"><span data-stu-id="405d8-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="405d8-118">Ker se dnevnice običajno uporabljajo za kritje stroškov, kot so prehrana, nastanitev in drugi nepredvideni stroški, lahko ustvarite pravila za dnevnice, ki jih ponuja vaša organizacija.</span><span class="sxs-lookup"><span data-stu-id="405d8-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="405d8-119">Dnevnice lahko temeljijo na letnem času, kraju potovanja ali obojem.</span><span class="sxs-lookup"><span data-stu-id="405d8-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="405d8-120">Ko ustvarite pravilo za dnevnice, lahko določite, da se izbrani odstotek od dnevnice zadrži, če delavec prejme brezplačne obroke ali storitve.</span><span class="sxs-lookup"><span data-stu-id="405d8-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="405d8-121">Določite lahko tudi stopnje za vrednost dnevnic, da nastavite najmanjše in največje število ur, za katera lahko velja dnevnica za potovanje delavca.</span><span class="sxs-lookup"><span data-stu-id="405d8-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="405d8-122">**Odločitve:**</span><span class="sxs-lookup"><span data-stu-id="405d8-122">**Decisions:**</span></span>

- <span data-ttu-id="405d8-123">Privzeta pravila za dnevnice za prvi in zadnji dan:</span><span class="sxs-lookup"><span data-stu-id="405d8-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="405d8-124">Kolikšno je najmanjše število ur, ki jih lahko zaposleni zahteva na dan in še vedno prejme dnevnico?</span><span class="sxs-lookup"><span data-stu-id="405d8-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="405d8-125">Ali je znesek, ki je na voljo za obroke, nižji za prvi in zadnji dan?</span><span class="sxs-lookup"><span data-stu-id="405d8-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="405d8-126">Če je nižji, kolikšen je odstotek znižanja?</span><span class="sxs-lookup"><span data-stu-id="405d8-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="405d8-127">Ali je znesek, ki je na voljo za hotel, nižji za prvi in zadnji dan?</span><span class="sxs-lookup"><span data-stu-id="405d8-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="405d8-128">Če je nižji, kolikšen je odstotek znižanja?</span><span class="sxs-lookup"><span data-stu-id="405d8-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="405d8-129">Ali je znesek, ki je na voljo za druge stroške, ki nastanejo na prvi in zadnji dan, nižji?</span><span class="sxs-lookup"><span data-stu-id="405d8-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="405d8-130">Če je nižji, kolikšen je odstotek znižanja?</span><span class="sxs-lookup"><span data-stu-id="405d8-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="405d8-131">Privzeta pravila za dnevnice:</span><span class="sxs-lookup"><span data-stu-id="405d8-131">Default per diem rules:</span></span>

    - <span data-ttu-id="405d8-132">Ali pride do znižanja odstotka pri dnevnici za vsak obrok, če je na primer obrok brezplačen?</span><span class="sxs-lookup"><span data-stu-id="405d8-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="405d8-133">Če je nižji, kolikšen je odstotek znižanja za vsak obrok?</span><span class="sxs-lookup"><span data-stu-id="405d8-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="405d8-134">Ali se znižanje za obrok izračuna na dan, na potovanje ali glede na število obrokov na dan?</span><span class="sxs-lookup"><span data-stu-id="405d8-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="405d8-135">Ali je treba zneske dnevnic zaokrožiti na običajen način ali zaokrožiti navzgor?</span><span class="sxs-lookup"><span data-stu-id="405d8-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="405d8-136">Ali se dnevnice izračunajo za 24-urno obdobje ali za koledarski dan?</span><span class="sxs-lookup"><span data-stu-id="405d8-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="405d8-137">Pravila za dnevnice, ki temeljijo na lokaciji:</span><span class="sxs-lookup"><span data-stu-id="405d8-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="405d8-138">Ali se stopnje dnevnic razlikujejo glede na lokacijo?</span><span class="sxs-lookup"><span data-stu-id="405d8-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="405d8-139">Katere lokacije so vključene?</span><span class="sxs-lookup"><span data-stu-id="405d8-139">What locations are included?</span></span>
    - <span data-ttu-id="405d8-140">Če se stopnje dnevnic razlikujejo glede na lokacijo, kolikšen odstotek zneska je pri vsaki lokaciji na voljo za naslednje vrste stroškov:</span><span class="sxs-lookup"><span data-stu-id="405d8-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="405d8-141">Obroki</span><span class="sxs-lookup"><span data-stu-id="405d8-141">Meals</span></span>
        - <span data-ttu-id="405d8-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="405d8-142">Hotel</span></span>
        - <span data-ttu-id="405d8-143">Drugi stroški</span><span class="sxs-lookup"><span data-stu-id="405d8-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="405d8-144">Dnevniki in računi za upravljanje stroškov</span><span class="sxs-lookup"><span data-stu-id="405d8-144">Expense management journals and accounts</span></span>

<span data-ttu-id="405d8-145">Upravljanje stroškov zahteva uporabo več dnevnikov in računov.</span><span class="sxs-lookup"><span data-stu-id="405d8-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="405d8-146">Odločiti se morate na primer, ali se isti račun uporablja za denarne predujme in spore v zvezi s kreditnimi karticami.</span><span class="sxs-lookup"><span data-stu-id="405d8-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="405d8-147">**Odločitve:**</span><span class="sxs-lookup"><span data-stu-id="405d8-147">**Decisions:**</span></span>

- <span data-ttu-id="405d8-148">V kateri glavni knjigi se beležijo odobrena poročila o stroških?</span><span class="sxs-lookup"><span data-stu-id="405d8-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="405d8-149">Kateri račun se uporablja za denarne predujme?</span><span class="sxs-lookup"><span data-stu-id="405d8-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="405d8-150">Ali je treba denarne predujme zabeležiti takoj?</span><span class="sxs-lookup"><span data-stu-id="405d8-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="405d8-151">Načini plačila</span><span class="sxs-lookup"><span data-stu-id="405d8-151">Payment methods</span></span>

<span data-ttu-id="405d8-152">Ko dovolite zaposlenim, da ustvarijo stroške v imenu vašega podjetja, morate določiti načine plačila, ki jih zaposleni smejo uporabljati.</span><span class="sxs-lookup"><span data-stu-id="405d8-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="405d8-153">Na primer, zaposlenim lahko dovolite uporabo gotovine ali kreditne kartice podjetja.</span><span class="sxs-lookup"><span data-stu-id="405d8-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="405d8-154">Prav tako lahko zaposlenim dovolite uporabo osebnih kreditnih kartic in nato zaposlenim povrnete stroške.</span><span class="sxs-lookup"><span data-stu-id="405d8-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="405d8-155">Za vsak dovoljen način plačila morate sprejeti naslednje odločitve.</span><span class="sxs-lookup"><span data-stu-id="405d8-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="405d8-156">**Odločitve:**</span><span class="sxs-lookup"><span data-stu-id="405d8-156">**Decisions:**</span></span>

- <span data-ttu-id="405d8-157">Kateri načini plačila so dovoljeni?</span><span class="sxs-lookup"><span data-stu-id="405d8-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="405d8-158">Kdo je lastnik stroškov za način plačila?</span><span class="sxs-lookup"><span data-stu-id="405d8-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="405d8-159">Ali je na voljo vrsta protikonta?</span><span class="sxs-lookup"><span data-stu-id="405d8-159">Is there an offset account type?</span></span> <span data-ttu-id="405d8-160">Če je na voljo vrsta protikonta, katera je na voljo?</span><span class="sxs-lookup"><span data-stu-id="405d8-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="405d8-161">Če je na voljo protikonto, kateri račun je na voljo?</span><span class="sxs-lookup"><span data-stu-id="405d8-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="405d8-162">Če je način plačila kreditna kartica, ali naj se način plačila uporablja samo pri uvoženih transakcijah?</span><span class="sxs-lookup"><span data-stu-id="405d8-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="405d8-163">Kategorije stroškov in skupne kategorije</span><span class="sxs-lookup"><span data-stu-id="405d8-163">Expense categories and shared categories</span></span>

<span data-ttu-id="405d8-164">Ko zaposleni ustvarijo poročilo o stroških, morajo biti vsi zabeleženi stroški povezani s kategorijo stroškov.</span><span class="sxs-lookup"><span data-stu-id="405d8-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="405d8-165">Kategorije stroškov izhajajo iz skupnih kategorij, ki si jih delijo vse pravne osebe v vaši organizaciji.</span><span class="sxs-lookup"><span data-stu-id="405d8-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="405d8-166">Te kategorije lahko delite tudi v razdelku za upravljanje projektov in računovodstvo, odvisno od načina, kako je opredeljena vaša organizacija.</span><span class="sxs-lookup"><span data-stu-id="405d8-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="405d8-167">Na podlagi strukture vaše organizacije in navodil ekipe za uvajanje določite, ali se bodo kategorije, ki se uporabljajo pri upravljanju stroškov, uporabljale samo pri upravljanju stroškov ali jih želite deliti med funkcijami za upravljanje projektov, računovodstvo in upravljanje stroškov.</span><span class="sxs-lookup"><span data-stu-id="405d8-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="405d8-168">Upoštevajte, da si te kategorije si lahko delita funkciji »Projekt« in »Strošek« ali »Projekt« in »Proizvodnja«, ne pa funkciji »Strošek« in »Proizvodnja«.</span><span class="sxs-lookup"><span data-stu-id="405d8-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="405d8-169">Za vsako kategorijo stroškov morate sprejeti naslednje odločitve.</span><span class="sxs-lookup"><span data-stu-id="405d8-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="405d8-170">**Odločitve:**</span><span class="sxs-lookup"><span data-stu-id="405d8-170">**Decisions:**</span></span>

- <span data-ttu-id="405d8-171">Katera kategorija stroška je izbrana?</span><span class="sxs-lookup"><span data-stu-id="405d8-171">What is the expense category?</span></span> <span data-ttu-id="405d8-172">Primeri vključujejo kategorije za lete, hotele ali kilometrino.</span><span class="sxs-lookup"><span data-stu-id="405d8-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="405d8-173">Ali lahko kategorijo stroškov uporabljajo tudi na oddelku »Vodenje projektov in računovodstvo«?</span><span class="sxs-lookup"><span data-stu-id="405d8-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="405d8-174">Katera vrsta stroška je izbrana?</span><span class="sxs-lookup"><span data-stu-id="405d8-174">What is the expense type?</span></span>
- <span data-ttu-id="405d8-175">Kateri je privzeti način plačila za kategorijo stroškov?</span><span class="sxs-lookup"><span data-stu-id="405d8-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="405d8-176">Ali je treba razčleniti stroške v kategoriji stroškov?</span><span class="sxs-lookup"><span data-stu-id="405d8-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="405d8-177">Kateri je glavni privzeti račun za kategorijo stroškov?</span><span class="sxs-lookup"><span data-stu-id="405d8-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="405d8-178">Katera je privzeta davčna skupina za prodajo izdelka za kategorijo stroškov?</span><span class="sxs-lookup"><span data-stu-id="405d8-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="405d8-179">Ali so za kategorijo stroškov dovoljeni dodatni načini plačila?</span><span class="sxs-lookup"><span data-stu-id="405d8-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="405d8-180">Če so dovoljeni dodatni načini plačila, kateri so na voljo?</span><span class="sxs-lookup"><span data-stu-id="405d8-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="405d8-181">Ali obstajajo podkategorije v tej kategoriji stroškov?</span><span class="sxs-lookup"><span data-stu-id="405d8-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="405d8-182">Če obstajajo podkategorije, morate določiti tudi naslednje:</span><span class="sxs-lookup"><span data-stu-id="405d8-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="405d8-183">Ali je katera od podkategorij izključena iz davčne olajšave?</span><span class="sxs-lookup"><span data-stu-id="405d8-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="405d8-184">Katera davčna skupina za prodajo izdelka velja za podkategorije?</span><span class="sxs-lookup"><span data-stu-id="405d8-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="405d8-185">Če se kategorija stroškov uporablja tudi pri upravljanju projektov in računovodstvu, odgovorite na preostala vprašanja.</span><span class="sxs-lookup"><span data-stu-id="405d8-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="405d8-186">V nasprotnem primeru pojdite na naslednji razdelek.</span><span class="sxs-lookup"><span data-stu-id="405d8-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="405d8-187">Kateri računi stroškov bodo uporabljeni za naslednje stroške?</span><span class="sxs-lookup"><span data-stu-id="405d8-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="405d8-188">Cena</span><span class="sxs-lookup"><span data-stu-id="405d8-188">Cost</span></span>
    - <span data-ttu-id="405d8-189">Dodelitev plače</span><span class="sxs-lookup"><span data-stu-id="405d8-189">Payroll allocation</span></span>
    - <span data-ttu-id="405d8-190">Vrednost cene WIP</span><span class="sxs-lookup"><span data-stu-id="405d8-190">WIP-cost value</span></span>
    - <span data-ttu-id="405d8-191">Element stroška</span><span class="sxs-lookup"><span data-stu-id="405d8-191">Cost-item</span></span>
    - <span data-ttu-id="405d8-192">Element vrednosti cene WIP</span><span class="sxs-lookup"><span data-stu-id="405d8-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="405d8-193">Vračunana izguba</span><span class="sxs-lookup"><span data-stu-id="405d8-193">Accrued loss</span></span>
    - <span data-ttu-id="405d8-194">Vračunana izguba WIP</span><span class="sxs-lookup"><span data-stu-id="405d8-194">WIP-accrued loss</span></span>

- <span data-ttu-id="405d8-195">Kateri računi prihodkov bodo uporabljeni za naslednje?</span><span class="sxs-lookup"><span data-stu-id="405d8-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="405d8-196">Fakturirani prihodek</span><span class="sxs-lookup"><span data-stu-id="405d8-196">Invoiced revenue</span></span>
    - <span data-ttu-id="405d8-197">Vračunana vrednost prihodkov od prodaje</span><span class="sxs-lookup"><span data-stu-id="405d8-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="405d8-198">Vrednost prodaje WIP</span><span class="sxs-lookup"><span data-stu-id="405d8-198">WIP-sales value</span></span>
    - <span data-ttu-id="405d8-199">Vračunano razmerje med prihodkom in proizvodnjo</span><span class="sxs-lookup"><span data-stu-id="405d8-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="405d8-200">Proizvodnja WIP</span><span class="sxs-lookup"><span data-stu-id="405d8-200">WIP-production</span></span>
    - <span data-ttu-id="405d8-201">Vračunano razmerje med prihodkom in dobičkom</span><span class="sxs-lookup"><span data-stu-id="405d8-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="405d8-202">Dobiček WIP</span><span class="sxs-lookup"><span data-stu-id="405d8-202">WIP-profit</span></span>
    - <span data-ttu-id="405d8-203">Vračunano razmerje med prihodkom in naročnino</span><span class="sxs-lookup"><span data-stu-id="405d8-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="405d8-204">Naročnina WIP</span><span class="sxs-lookup"><span data-stu-id="405d8-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="405d8-205">Davki</span><span class="sxs-lookup"><span data-stu-id="405d8-205">Taxes</span></span>

<span data-ttu-id="405d8-206">Za davke, povezane s stroški, morate določiti, kaj je vključeno ali omogočeno v poročilih o stroških.</span><span class="sxs-lookup"><span data-stu-id="405d8-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="405d8-207">**Odločitve:**</span><span class="sxs-lookup"><span data-stu-id="405d8-207">**Decisions:**</span></span>

- <span data-ttu-id="405d8-208">Ali je prometni davek vključen v zneske stroškov?</span><span class="sxs-lookup"><span data-stu-id="405d8-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="405d8-209">Ali je treba omogočiti izterjavo davkov na stroške?</span><span class="sxs-lookup"><span data-stu-id="405d8-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="405d8-210">Če ste se odločili za uporabo ameriškega prometnega davka in uporabo davčnih pravil, ko ste načrtovali glavno knjigo, ne morete omogočiti izterjave davka na stroške.</span><span class="sxs-lookup"><span data-stu-id="405d8-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="405d8-211">(Če želite uporabljati ameriški prometni davek in davčna pravila, nastavite možnost **Uporabi pravila za prometni davek** na **Da**.)</span><span class="sxs-lookup"><span data-stu-id="405d8-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="405d8-212">Pravilniki</span><span class="sxs-lookup"><span data-stu-id="405d8-212">Policies</span></span>

<span data-ttu-id="405d8-213">Z ustvarjanjem pravilnikov za poročanje o stroških lahko svoji organizaciji pomagate prihraniti čas in denar, ko zaposleni ustvarijo stroške v njenem imenu.</span><span class="sxs-lookup"><span data-stu-id="405d8-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="405d8-214">Pravilniki zagotavljajo, da zaposleni ne presežejo proračunu, zagotavljajo vse zahtevane informacije in denar porabijo le, ko ga potrebujejo.</span><span class="sxs-lookup"><span data-stu-id="405d8-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="405d8-215">Za vsak pravilnik poročanja o stroških in vsak pravilnik odobritve poročila o stroških, ki jih ustvarite, morate sprejeti naslednje odločitve.</span><span class="sxs-lookup"><span data-stu-id="405d8-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="405d8-216">**Odločitve:**</span><span class="sxs-lookup"><span data-stu-id="405d8-216">**Decisions:**</span></span>

- <span data-ttu-id="405d8-217">Kako se imenuje pravilnik?</span><span class="sxs-lookup"><span data-stu-id="405d8-217">What is the name of the policy?</span></span>
- <span data-ttu-id="405d8-218">Kakšen je namen pravilnika o stroških?</span><span class="sxs-lookup"><span data-stu-id="405d8-218">What is the expense policy for?</span></span>
- <span data-ttu-id="405d8-219">Če ste se prej odločili, da boste omogočili medpodjetniške stroške, za katera podjetja v vaši organizaciji bo veljal ta pravilnik?</span><span class="sxs-lookup"><span data-stu-id="405d8-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="405d8-220">Kdaj začne pravilnik veljati?</span><span class="sxs-lookup"><span data-stu-id="405d8-220">When does the policy become effective?</span></span>
- <span data-ttu-id="405d8-221">Kdaj pravilnik poteče?</span><span class="sxs-lookup"><span data-stu-id="405d8-221">When does the policy expire?</span></span>
- <span data-ttu-id="405d8-222">Kakšno je pravilo pravilnika?</span><span class="sxs-lookup"><span data-stu-id="405d8-222">What is the policy rule?</span></span>
- <span data-ttu-id="405d8-223">Kakšen je rezultat pravila pravilnika?</span><span class="sxs-lookup"><span data-stu-id="405d8-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]