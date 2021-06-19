---
title: Popravljalni računi za projekt
description: Ta tema vsebuje informacije o tem, kako ustvariti in potrditi popravljalne račune v aplikaciji Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004101"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="897a3-103">Popravljalni računi za projekt</span><span class="sxs-lookup"><span data-stu-id="897a3-103">Corrective project invoices</span></span>

<span data-ttu-id="897a3-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="897a3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="897a3-105">Potrjeni račun projekta je mogoče popraviti v skladu s spremembami ali dobroimetjem po dogovoru s stranko in vodjo projekta.</span><span class="sxs-lookup"><span data-stu-id="897a3-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="897a3-106">Če želite urediti potrjeni račun, odprite potrjeni račun in izberite **Popravi ta račun**.</span><span class="sxs-lookup"><span data-stu-id="897a3-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="897a3-107">Ta možnost je na voljo samo za potrjene račune projektov.</span><span class="sxs-lookup"><span data-stu-id="897a3-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="897a3-108">Iz potrjenega računa se ustvari nov osnutek računa.</span><span class="sxs-lookup"><span data-stu-id="897a3-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="897a3-109">Vse podrobnosti vrstice računa iz predhodno potrjenega računa so kopirane v novi osnutek.</span><span class="sxs-lookup"><span data-stu-id="897a3-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="897a3-110">Spodaj so naštete nekatere ključne točke, ki jih je treba razumeti glede podrobnosti vrstice na novem popravljenem računu:</span><span class="sxs-lookup"><span data-stu-id="897a3-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="897a3-111">Vse količine se posodobijo na nič.</span><span class="sxs-lookup"><span data-stu-id="897a3-111">All quantities are updated to zero.</span></span> <span data-ttu-id="897a3-112">Aplikacija predpostavlja, da so vsi zaračunani elementi v celoti knjiženi v dobro.</span><span class="sxs-lookup"><span data-stu-id="897a3-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="897a3-113">Po potrebi lahko te količine ročno posodobite, tako da odražajo količino, ki se zaračuna, in ne količine, ki se knjiži v dobro.</span><span class="sxs-lookup"><span data-stu-id="897a3-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="897a3-114">Na podlagi vnesene količine aplikacija izračuna količino dobroimetja.</span><span class="sxs-lookup"><span data-stu-id="897a3-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="897a3-115">Ta znesek se odraža v dejanskih vrednostih, ki se ustvarijo ob potrditvi popravljenega računa.</span><span class="sxs-lookup"><span data-stu-id="897a3-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="897a3-116">Če spreminjate znesek davka, morate vnesti pravilen znesek davka in ne zneska davka, ki se knjiži v dobro.</span><span class="sxs-lookup"><span data-stu-id="897a3-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="897a3-117">Predhodno potrjene podrobnosti pogodbe na podlagi izdelka niso kopirane.</span><span class="sxs-lookup"><span data-stu-id="897a3-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="897a3-118">Obdelava popravkov na projektnem računu na podlagi izdelka ni podprta.</span><span class="sxs-lookup"><span data-stu-id="897a3-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="897a3-119">Popravki mejnika so vedno obdelani kot polno dobroimetje.</span><span class="sxs-lookup"><span data-stu-id="897a3-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="897a3-120">Zneske honorarja ali predujma je mogoče popraviti, če je bila stranki zaračunana napačna vrednost.</span><span class="sxs-lookup"><span data-stu-id="897a3-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="897a3-121">Uskladitve honorarjev in predujmov je mogoče popraviti, če je bil uporabljen nepravilen znesek za uskladitev stroškov na predhodno potrjenem računu.</span><span class="sxs-lookup"><span data-stu-id="897a3-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="897a3-122">Podrobnosti vrstice računa oz. popravki drugih že zaračunanih stroškov imajo polje **Popravek** nastavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="897a3-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="897a3-123">Računi s popravljenimi podrobnostmi vrstice računa imajo polje **Vsebuje popravke**, ki je prav tako nastavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="897a3-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="897a3-124">Dejanske vrednosti, ustvarjene ob potrditvi popravljenega računa</span><span class="sxs-lookup"><span data-stu-id="897a3-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="897a3-125">V naslednji tabeli so navedene dejanske vrednosti, ki se ustvarijo, ko je popravljalni račun potrjen.</span><span class="sxs-lookup"><span data-stu-id="897a3-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="897a3-126">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="897a3-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="897a3-127">
                    <strong>Dejanski podatki, ustvarjeni ob potrditvi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="897a3-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="897a3-128">Potrdite popravek predračuna ali honorarja.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="897a3-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-129">Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev</span><span class="sxs-lookup"><span data-stu-id="897a3-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="897a3-130">Ta znesek je pozitiven, saj naj bi odpravil negativno vrednost, ki je nastala ob izdaji računa za honorar ali predujem.</span><span class="sxs-lookup"><span data-stu-id="897a3-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-131">Dejanska vrednost stornacije zaračunane prodaje se ustvari za znesek honorarja ali predujma za stornacijo prvotno zaračunane prodaje.</span><span class="sxs-lookup"><span data-stu-id="897a3-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-132">Nova dejanska vrednost obračunane prodaje se ustvari za popravljeni znesek vrstice računa na podlagi honorarja ali predujma.</span><span class="sxs-lookup"><span data-stu-id="897a3-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-133">Dejanska vrednost neobračunane prodaje negativnega zneska popravljene vrstice računa na podlagi honorarja ali predujma, ki se uporabi za uskladitev.</span><span class="sxs-lookup"><span data-stu-id="897a3-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="897a3-134">Potrditev popravka predhodno usklajenega honorarja ali predujma.</span><span class="sxs-lookup"><span data-stu-id="897a3-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-135">Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev</span><span class="sxs-lookup"><span data-stu-id="897a3-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="897a3-136">Ta znesek je pozitiven in naj bi odpravil negativno vrednost, ki je nastala ob prejšnji uskladitvi.</span><span class="sxs-lookup"><span data-stu-id="897a3-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-137">Dejanska vrednost stornirane obračunane prodaje za znesek na prejšnjem računu.</span><span class="sxs-lookup"><span data-stu-id="897a3-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-138">Nova dejanska vrednost obračunane prodaje za popravljeni honorar, ki se uporabi pri popravljenem računu.</span><span class="sxs-lookup"><span data-stu-id="897a3-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-139">Neobračunana dejanska vrednost prodaje z negativnim zneskom iz popravljenega preostanka honorarja ali predujma, ki se uporabi za uskladitev pri nadaljnjih računih.</span><span class="sxs-lookup"><span data-stu-id="897a3-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="897a3-140">Izdajanje računov za celotno dobroimetje predhodno zaračunane časovne transakcije.</span><span class="sxs-lookup"><span data-stu-id="897a3-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-141">Stornacija obračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za čas.</span><span class="sxs-lookup"><span data-stu-id="897a3-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-142">Nova dejanska vrednost neobračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za čas.</span><span class="sxs-lookup"><span data-stu-id="897a3-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="897a3-143">Izdajanje računov za delno dobroimetje pri časovni transakciji.</span><span class="sxs-lookup"><span data-stu-id="897a3-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-144">Stornacija obračunane prodaje za ure in znesek, zaračunan na prvotni vrstici računa za čas.</span><span class="sxs-lookup"><span data-stu-id="897a3-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-145">Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za ure in znesek na urejeni podrobnosti vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.</span><span class="sxs-lookup"><span data-stu-id="897a3-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-146">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za preostale ure in zneske po odštetju popravljenih številk na podrobnostih vrstice računa.</span><span class="sxs-lookup"><span data-stu-id="897a3-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="897a3-147">Izdajanje računov za celotno dobroimetje predhodno zaračunane transakcije stroška.</span><span class="sxs-lookup"><span data-stu-id="897a3-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-148">Stornacija obračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za strošek.</span><span class="sxs-lookup"><span data-stu-id="897a3-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-149">Nova dejanska vrednost neobračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za strošek.</span><span class="sxs-lookup"><span data-stu-id="897a3-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="897a3-150">Izdajanje računov za delno dobroimetje predhodno zaračunane transakcije stroška.</span><span class="sxs-lookup"><span data-stu-id="897a3-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-151">Stornacija obračunane prodaje za količino in znesek, zaračunan na prvotnih podrobnostih vrstice računa za strošek.</span><span class="sxs-lookup"><span data-stu-id="897a3-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-152">Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za količino in znesek na popravljenih podrobnostih vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.</span><span class="sxs-lookup"><span data-stu-id="897a3-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-153">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za preostalo količino in zneske po odštetju popravljenih številk na podrobnostih vrstice računa.</span><span class="sxs-lookup"><span data-stu-id="897a3-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="897a3-154">Izdajanje računov predhodno zaračunanih materialnih transakcij v celoti v dobro.</span><span class="sxs-lookup"><span data-stu-id="897a3-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-155">Storniranje obračunane prodaje za količino in znesek v izvirnih podrobnostih vrstice računa za material.</span><span class="sxs-lookup"><span data-stu-id="897a3-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-156">Nova neobračunana dejanska prodaja za količino in znesek v izvirnih podrobnostih vrstice računa za material.</span><span class="sxs-lookup"><span data-stu-id="897a3-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="897a3-157">Račun za delno dobroimetje pri materialni transakciji.</span><span class="sxs-lookup"><span data-stu-id="897a3-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-158">Storniranje obračunane prodaje za količino in znesek, zaračunan v izvirnih podrobnostih vrstice računa za material.</span><span class="sxs-lookup"><span data-stu-id="897a3-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-159">Nova neobračunana dejanska prodaja, ki se zaračuna za količino in znesek v podrobnostih vrstice računa, storno in vrednost obračuna dejanske prodaje.</span><span class="sxs-lookup"><span data-stu-id="897a3-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-160">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za preostalo količino in zneske po odštetju popravljenih številk na podrobnostih vrstice računa.</span><span class="sxs-lookup"><span data-stu-id="897a3-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="897a3-161">Izdajanje računov za celotno dobroimetje predhodno zaračunane transakcije dajatve.</span><span class="sxs-lookup"><span data-stu-id="897a3-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-162">Stornacija obračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za dajatev.</span><span class="sxs-lookup"><span data-stu-id="897a3-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-163">Nova dejanska vrednost neobračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za dajatev.</span><span class="sxs-lookup"><span data-stu-id="897a3-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="897a3-164">Izdajanje računov za delno dobroimetje predhodno zaračunane transakcije dajatve.</span><span class="sxs-lookup"><span data-stu-id="897a3-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-165">Stornacija obračunane prodaje za količino in znesek, zaračunan na prvotnih podrobnostih vrstice računa za dajatev.</span><span class="sxs-lookup"><span data-stu-id="897a3-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-166">Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za količino in znesek na urejenih in popravljenih podrobnostih vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.</span><span class="sxs-lookup"><span data-stu-id="897a3-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="897a3-167">Izdajanje računov za celotno dobroimetje predhodno zaračunanega mejnika.</span><span class="sxs-lookup"><span data-stu-id="897a3-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-168">Stornacija obračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za mejnik.</span><span class="sxs-lookup"><span data-stu-id="897a3-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="897a3-169">Stanje računa na mejniku se posodablja od <b>Račun stranke je objavljen</b> do <b>Pripravljeno za račun</b>.</span><span class="sxs-lookup"><span data-stu-id="897a3-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="897a3-170">Izdajanje računov za delno dobroimetje predhodno zaračunanega mejnika.</span><span class="sxs-lookup"><span data-stu-id="897a3-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-171">Niso podprti</span><span class="sxs-lookup"><span data-stu-id="897a3-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="897a3-172">Dobroimetje in popravki predhodno zaračunanih podrobnosti pogodbe na podlagi izdelka.</span><span class="sxs-lookup"><span data-stu-id="897a3-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="897a3-173">Niso podprti</span><span class="sxs-lookup"><span data-stu-id="897a3-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
