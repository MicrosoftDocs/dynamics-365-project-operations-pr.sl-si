---
title: Popravljalni računi, ki temeljijo na projektih
description: Ta tema vsebuje informacije o tem, kako v aplikaciji Project Operations ustvariti in potrditi popravljalne račune, ki temeljijo na projektu.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867061"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="4bac4-103">Popravljalni računi, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="4bac4-103">Corrective project-based invoices</span></span>

<span data-ttu-id="4bac4-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="4bac4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4bac4-105">Potrjeni račun projekta je mogoče popraviti v skladu s spremembami ali dobroimetjem po dogovoru s stranko in vodjo projekta.</span><span class="sxs-lookup"><span data-stu-id="4bac4-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="4bac4-106">Če želite urediti potrjeni račun, odprite potrjeni račun in izberite **Popravi ta račun**.</span><span class="sxs-lookup"><span data-stu-id="4bac4-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="4bac4-107">Ta izbira ni na voljo, razen če je račun za projekt potrjen ali če račun, ki temelji na projektu, vsebuje predujme, honorarje ali usklajevanja predujmov ali honorarjev.</span><span class="sxs-lookup"><span data-stu-id="4bac4-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="4bac4-108">Iz potrjenega računa se ustvari nov osnutek računa.</span><span class="sxs-lookup"><span data-stu-id="4bac4-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="4bac4-109">Vse podrobnosti vrstice računa iz predhodno potrjenega računa so kopirane v novi osnutek.</span><span class="sxs-lookup"><span data-stu-id="4bac4-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="4bac4-110">Spodaj so naštete nekatere ključne točke, ki jih je treba razumeti glede podrobnosti vrstice na novem popravljenem računu:</span><span class="sxs-lookup"><span data-stu-id="4bac4-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="4bac4-111">Vse količine se posodobijo na nič.</span><span class="sxs-lookup"><span data-stu-id="4bac4-111">All quantities are updated to zero.</span></span> <span data-ttu-id="4bac4-112">Dynamics 365 Project Operations predvideva, da so vsi zaračunani elementi v celoti knjiženi v dobro.</span><span class="sxs-lookup"><span data-stu-id="4bac4-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="4bac4-113">Po potrebi lahko te količine ročno posodobite, tako da odražajo količino, ki se zaračuna, in ne količine, ki se knjiži v dobro.</span><span class="sxs-lookup"><span data-stu-id="4bac4-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="4bac4-114">Na podlagi vnesene količine aplikacija izračuna količino dobroimetja.</span><span class="sxs-lookup"><span data-stu-id="4bac4-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="4bac4-115">Ta znesek se odraža v dejanskih vrednostih, ki se ustvarijo ob potrditvi popravljenega računa.</span><span class="sxs-lookup"><span data-stu-id="4bac4-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="4bac4-116">Če spreminjate znesek davka, morate vnesti pravilen znesek davka in ne zneska davka, ki se knjiži v dobro.</span><span class="sxs-lookup"><span data-stu-id="4bac4-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="4bac4-117">Popravki mejnika so vedno obdelani kot polno dobroimetje.</span><span class="sxs-lookup"><span data-stu-id="4bac4-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="4bac4-118">Podrobnosti vrstice računa, ki so popravki drugih že zaračunanih stroškov, imajo polje **Popravek** nastavljeno na vrednost **Da**.</span><span class="sxs-lookup"><span data-stu-id="4bac4-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="4bac4-119">Računi s popravljenimi podrobnostmi vrstice računa imajo polje **Vsebuje popravke** nastavljeno na vrednost **Da**.</span><span class="sxs-lookup"><span data-stu-id="4bac4-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="4bac4-120">Dejanske vrednosti, ustvarjene ob potrditvi popravljenega računa</span><span class="sxs-lookup"><span data-stu-id="4bac4-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="4bac4-121">V naslednji tabeli so navedene dejanske vrednosti, ki se ustvarijo, ko je popravljalni račun potrjen.</span><span class="sxs-lookup"><span data-stu-id="4bac4-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="4bac4-122">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4bac4-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="4bac4-123">
                    <strong>Dejanski podatki, ustvarjeni ob potrditvi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4bac4-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4bac4-124">Izdajanje računov za celotno dobroimetje predhodno zaračunane časovne transakcije.</span><span class="sxs-lookup"><span data-stu-id="4bac4-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-125">Stornacija obračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za čas.</span><span class="sxs-lookup"><span data-stu-id="4bac4-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-126">Nova dejanska vrednost neobračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za čas.</span><span class="sxs-lookup"><span data-stu-id="4bac4-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4bac4-127">Izdajanje računov za delno dobroimetje pri časovni transakciji.</span><span class="sxs-lookup"><span data-stu-id="4bac4-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-128">Stornacija obračunane prodaje za ure in znesek, zaračunan na prvotni vrstici računa za čas.</span><span class="sxs-lookup"><span data-stu-id="4bac4-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-129">Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za ure in znesek na urejeni podrobnosti vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.</span><span class="sxs-lookup"><span data-stu-id="4bac4-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-130">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za preostale ure in zneske po odštetju popravljenih številk na podrobnostih vrstice računa.</span><span class="sxs-lookup"><span data-stu-id="4bac4-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4bac4-131">Izdajanje računov za celotno dobroimetje predhodno zaračunane transakcije stroška.</span><span class="sxs-lookup"><span data-stu-id="4bac4-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-132">Stornacija obračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za strošek.</span><span class="sxs-lookup"><span data-stu-id="4bac4-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-133">Nova dejanska vrednost neobračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za strošek.</span><span class="sxs-lookup"><span data-stu-id="4bac4-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4bac4-134">Izdajanje računov za delno dobroimetje predhodno zaračunane transakcije stroška.</span><span class="sxs-lookup"><span data-stu-id="4bac4-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-135">Stornacija obračunane prodaje za količino in znesek, zaračunan na prvotnih podrobnostih vrstice računa za strošek.</span><span class="sxs-lookup"><span data-stu-id="4bac4-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-136">Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za količino in znesek na popravljenih podrobnostih vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.</span><span class="sxs-lookup"><span data-stu-id="4bac4-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-137">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za preostalo količino in zneske po odštetju popravljenih številk na podrobnostih vrstice računa.</span><span class="sxs-lookup"><span data-stu-id="4bac4-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4bac4-138">Izdajanje računov predhodno zaračunanih materialnih transakcij v celoti v dobro.</span><span class="sxs-lookup"><span data-stu-id="4bac4-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-139">Storniranje obračunane prodaje za količino in znesek v izvirnih podrobnostih vrstice računa za material.</span><span class="sxs-lookup"><span data-stu-id="4bac4-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-140">Nova neobračunana dejanska prodaja za količino in znesek v izvirnih podrobnostih vrstice računa za material.</span><span class="sxs-lookup"><span data-stu-id="4bac4-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4bac4-141">Račun za delno dobroimetje pri materialni transakciji.</span><span class="sxs-lookup"><span data-stu-id="4bac4-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-142">Storniranje obračunane prodaje za količino in znesek, zaračunan v izvirnih podrobnostih vrstice računa za material.</span><span class="sxs-lookup"><span data-stu-id="4bac4-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-143">Nova neobračunana dejanska prodaja, ki se zaračuna za količino in znesek v podrobnostih vrstice računa, storno in vrednost obračuna dejanske prodaje.</span><span class="sxs-lookup"><span data-stu-id="4bac4-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-144">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za preostalo količino in zneske po odštetju popravljenih številk na podrobnostih vrstice računa.</span><span class="sxs-lookup"><span data-stu-id="4bac4-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4bac4-145">Izdajanje računov za celotno dobroimetje predhodno zaračunane transakcije dajatve.</span><span class="sxs-lookup"><span data-stu-id="4bac4-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-146">Stornacija obračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za dajatev.</span><span class="sxs-lookup"><span data-stu-id="4bac4-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-147">Nova dejanska vrednost neobračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za dajatev.</span><span class="sxs-lookup"><span data-stu-id="4bac4-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4bac4-148">Izdajanje računov za delno dobroimetje predhodno zaračunane transakcije dajatve.</span><span class="sxs-lookup"><span data-stu-id="4bac4-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-149">Stornacija obračunane prodaje za količino in znesek, zaračunan na prvotnih podrobnostih vrstice računa za dajatev.</span><span class="sxs-lookup"><span data-stu-id="4bac4-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-150">Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za količino in znesek na urejenih in popravljenih podrobnostih vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.</span><span class="sxs-lookup"><span data-stu-id="4bac4-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4bac4-151">Izdajanje računov za celotno dobroimetje predhodno zaračunanega mejnika.</span><span class="sxs-lookup"><span data-stu-id="4bac4-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-152">Stornacija obračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za mejnik.</span><span class="sxs-lookup"><span data-stu-id="4bac4-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="4bac4-153">Stanje računa na mejniku se posodablja od <b>Račun stranke je objavljen</b> do <b>Pripravljeno za račun</b>.</span><span class="sxs-lookup"><span data-stu-id="4bac4-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4bac4-154">Izdajanje računov za delno dobroimetje predhodno zaračunanega mejnika.</span><span class="sxs-lookup"><span data-stu-id="4bac4-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4bac4-155">Ta scenarij ni podprt.</span><span class="sxs-lookup"><span data-stu-id="4bac4-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
