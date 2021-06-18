---
title: Ustvarjanje popravljalnih računov, ki temeljijo na projektih
description: Ta tema vsebuje informacije o popravljalnih računih v aplikaciji Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001653"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="60130-103">Ustvarjanje popravljalnih računov, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="60130-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="60130-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="60130-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="60130-105">Potrjeni račun projekta je mogoče popraviti v skladu s spremembami ali dobroimetjem po dogovoru s stranko in vodjo projekta.</span><span class="sxs-lookup"><span data-stu-id="60130-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="60130-106">Če želite urediti potrjeni račun, odprite potrjeni račun in izberite **Popravi ta račun**.</span><span class="sxs-lookup"><span data-stu-id="60130-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="60130-107">Ta možnost je na voljo samo za potrjene račune projektov.</span><span class="sxs-lookup"><span data-stu-id="60130-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="60130-108">Iz potrjenega računa se ustvari nov osnutek računa.</span><span class="sxs-lookup"><span data-stu-id="60130-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="60130-109">Vse podrobnosti vrstice računa iz predhodno potrjenega računa so kopirane v novi osnutek.</span><span class="sxs-lookup"><span data-stu-id="60130-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="60130-110">Sledi nekaj ključnih točk, s katerimi boste lažje razumeli podrobnosti vrstice na novem popravljenem računu:</span><span class="sxs-lookup"><span data-stu-id="60130-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="60130-111">Vse količine se posodobijo na nič.</span><span class="sxs-lookup"><span data-stu-id="60130-111">All quantities are updated to zero.</span></span> <span data-ttu-id="60130-112">To predvideva, da so vsi zaračunani elementi v celoti knjiženi v dobro.</span><span class="sxs-lookup"><span data-stu-id="60130-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="60130-113">Po potrebi lahko te količine ročno posodobite, tako da odražajo količino, ki se zaračuna, in ne količine, ki se knjiži v dobro.</span><span class="sxs-lookup"><span data-stu-id="60130-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="60130-114">Na podlagi vnesene količine aplikacija izračuna količino dobroimetja.</span><span class="sxs-lookup"><span data-stu-id="60130-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="60130-115">Ta znesek se odraža v dejanskih vrednostih, ki se ustvarijo ob potrditvi popravljenega računa.</span><span class="sxs-lookup"><span data-stu-id="60130-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="60130-116">Če spreminjate znesek davka, morate vnesti pravilen znesek davka in ne zneska davka, ki se knjiži v dobro.</span><span class="sxs-lookup"><span data-stu-id="60130-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="60130-117">Popravki mejnika so vedno obdelani kot polno dobroimetje.</span><span class="sxs-lookup"><span data-stu-id="60130-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="60130-118">Zneske honorarja ali predujma je mogoče popraviti, če je bila stranki zaračunana napačna vrednost.</span><span class="sxs-lookup"><span data-stu-id="60130-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="60130-119">Uskladitve honorarjev in predujmov je mogoče popraviti, če je bil uporabljen nepravilen znesek za uskladitev stroškov na predhodno potrjenem računu.</span><span class="sxs-lookup"><span data-stu-id="60130-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60130-120">Podrobnosti vrstice računa, ki so popravki drugih že zaračunanih stroškov, imajo polje **Popravek** nastavljeno na vrednost **Da**.</span><span class="sxs-lookup"><span data-stu-id="60130-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="60130-121">Računi s popravljenimi podrobnostmi vrstice računa imajo polje **Vsebuje popravke**, ki je prav tako nastavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="60130-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="60130-122">Dejanske vrednosti, ustvarjene ob potrditvi popravljenega računa</span><span class="sxs-lookup"><span data-stu-id="60130-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="60130-123">V naslednji tabeli so navedene dejanske vrednosti, ki se ustvarijo, ko je popravljalni račun potrjen.</span><span class="sxs-lookup"><span data-stu-id="60130-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="60130-124">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="60130-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="60130-125">
                    <strong>Dejanski podatki, ustvarjeni ob potrditvi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="60130-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="60130-126">Potrdite popravek predračuna ali honorarja.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="60130-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-127">Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev</span><span class="sxs-lookup"><span data-stu-id="60130-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="60130-128">Ta znesek je pozitiven, saj naj bi odpravil negativno vrednost, ki je nastala ob izdaji računa za honorar ali predujem.</span><span class="sxs-lookup"><span data-stu-id="60130-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-129">Dejanska vrednost stornacije zaračunane prodaje se ustvari za znesek honorarja ali predujma za stornacijo prvotno zaračunane prodaje.</span><span class="sxs-lookup"><span data-stu-id="60130-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-130">Nova dejanska vrednost obračunane prodaje se ustvari za popravljeni znesek vrstice računa na podlagi honorarja ali predujma.</span><span class="sxs-lookup"><span data-stu-id="60130-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-131">Dejanska vrednost neobračunane prodaje negativnega zneska popravljene vrstice računa na podlagi honorarja ali predujma, ki se uporabi za uskladitev.</span><span class="sxs-lookup"><span data-stu-id="60130-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="60130-132">Potrditev popravka predhodno usklajenega honorarja ali predujma.</span><span class="sxs-lookup"><span data-stu-id="60130-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-133">Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev</span><span class="sxs-lookup"><span data-stu-id="60130-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="60130-134">Ta znesek je pozitiven in naj bi odpravil negativno vrednost, ki je nastala ob prejšnji uskladitvi.</span><span class="sxs-lookup"><span data-stu-id="60130-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-135">Dejanska vrednost stornirane obračunane prodaje za znesek na prejšnjem računu.</span><span class="sxs-lookup"><span data-stu-id="60130-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-136">Nova dejanska vrednost obračunane prodaje za popravljeni honorar, ki se uporabi pri popravljenem računu.</span><span class="sxs-lookup"><span data-stu-id="60130-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-137">Neobračunana dejanska vrednost prodaje z negativnim zneskom iz popravljenega preostanka honorarja ali predujma, ki se uporabi za uskladitev pri nadaljnjih računih.</span><span class="sxs-lookup"><span data-stu-id="60130-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="60130-138">Izdajanje računov za celotno dobroimetje predhodno zaračunane časovne transakcije.</span><span class="sxs-lookup"><span data-stu-id="60130-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-139">Stornacija obračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za čas.</span><span class="sxs-lookup"><span data-stu-id="60130-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-140">Nova dejanska vrednost neobračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za čas.</span><span class="sxs-lookup"><span data-stu-id="60130-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="60130-141">Izdajanje računov za delno dobroimetje pri časovni transakciji.</span><span class="sxs-lookup"><span data-stu-id="60130-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-142">Stornacija obračunane prodaje za ure in znesek, zaračunan na prvotni vrstici računa za čas.</span><span class="sxs-lookup"><span data-stu-id="60130-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-143">Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za ure in znesek na urejeni podrobnosti vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.</span><span class="sxs-lookup"><span data-stu-id="60130-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-144">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za preostale ure in zneske po odštetju popravljenih številk na podrobnostih vrstice računa.</span><span class="sxs-lookup"><span data-stu-id="60130-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="60130-145">Izdajanje računov za celotno dobroimetje predhodno zaračunane transakcije stroška.</span><span class="sxs-lookup"><span data-stu-id="60130-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-146">Stornacija obračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za strošek.</span><span class="sxs-lookup"><span data-stu-id="60130-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-147">Nova dejanska vrednost neobračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za strošek.</span><span class="sxs-lookup"><span data-stu-id="60130-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="60130-148">Izdajanje računov za delno dobroimetje predhodno zaračunane transakcije stroška.</span><span class="sxs-lookup"><span data-stu-id="60130-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-149">Stornacija obračunane prodaje za količino in znesek, zaračunan na prvotnih podrobnostih vrstice računa za strošek.</span><span class="sxs-lookup"><span data-stu-id="60130-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-150">Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za količino in znesek na popravljenih podrobnostih vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.</span><span class="sxs-lookup"><span data-stu-id="60130-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-151">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za preostalo količino in zneske po odštetju popravljenih številk na podrobnostih vrstice računa.</span><span class="sxs-lookup"><span data-stu-id="60130-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="60130-152">Izdajanje računov za celotno dobroimetje predhodno zaračunane transakcije dajatve.</span><span class="sxs-lookup"><span data-stu-id="60130-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-153">Stornacija obračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za dajatev.</span><span class="sxs-lookup"><span data-stu-id="60130-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-154">Nova dejanska vrednost neobračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za dajatev.</span><span class="sxs-lookup"><span data-stu-id="60130-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="60130-155">Izdajanje računov za delno dobroimetje predhodno zaračunane transakcije dajatve.</span><span class="sxs-lookup"><span data-stu-id="60130-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-156">Stornacija obračunane prodaje za količino in znesek, zaračunan na prvotnih podrobnostih vrstice računa za dajatev.</span><span class="sxs-lookup"><span data-stu-id="60130-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-157">Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za količino in znesek na urejenih in popravljenih podrobnostih vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.</span><span class="sxs-lookup"><span data-stu-id="60130-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="60130-158">Izdajanje računov za celotno dobroimetje predhodno zaračunanega mejnika.</span><span class="sxs-lookup"><span data-stu-id="60130-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-159">Stornacija obračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za mejnik.</span><span class="sxs-lookup"><span data-stu-id="60130-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="60130-160">Stanje računa na mejniku se posodablja od <b>Račun stranke je objavljen</b> do <b>Pripravljeno za račun</b>.</span><span class="sxs-lookup"><span data-stu-id="60130-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="60130-161">Izdajanje računov za delno dobroimetje predhodno zaračunanega mejnika.</span><span class="sxs-lookup"><span data-stu-id="60130-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="60130-162">Niso podprti</span><span class="sxs-lookup"><span data-stu-id="60130-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
