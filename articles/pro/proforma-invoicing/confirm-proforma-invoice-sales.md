---
title: Potrditev predračuna projekta
description: Ta tema vsebuje informacije o potrditvi predračunov projekta v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 144c1b6a49951af8be0c619f41808e7617e59c92
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867107"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="aea2d-103">Potrditev predračuna projekta</span><span class="sxs-lookup"><span data-stu-id="aea2d-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="aea2d-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="aea2d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="aea2d-105">Po potrditvi predračuna se stanje računa projekta posodobi na **Potrjeno**.</span><span class="sxs-lookup"><span data-stu-id="aea2d-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="aea2d-106">Ko je račun potrjen, postane na voljo samo za branje.</span><span class="sxs-lookup"><span data-stu-id="aea2d-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="aea2d-107">V prihodnje je račun mogoče popraviti le, če obstajajo popravki ali dobroimetja, ki jih sproži stranka.</span><span class="sxs-lookup"><span data-stu-id="aea2d-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="aea2d-108">V spodnji tabeli so navedeni dejanski podatki, ki jih je ustvaril sistem.</span><span class="sxs-lookup"><span data-stu-id="aea2d-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="aea2d-109">Ti dejanski podatki so ustvarjeni, ko se pred potrditvijo osnutka računa za projekt izvedejo določene operacije.</span><span class="sxs-lookup"><span data-stu-id="aea2d-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="aea2d-110">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aea2d-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="aea2d-111">
                    <strong>Dejanski podatki, ustvarjeni ob potrditvi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="aea2d-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="aea2d-112">Račun za predujem ali honorar</span><span class="sxs-lookup"><span data-stu-id="aea2d-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-113">Dejanska vrednost obračunane prodaje vrste <strong>Honorar</strong> je ustvarjena za znesek predplačila ali honorarja.</span><span class="sxs-lookup"><span data-stu-id="aea2d-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-114">Neobračunana dejanska vrednost prodaje negativnega zneska honorarja ali predplačila, ki se uporabi za uskladitev.</span><span class="sxs-lookup"><span data-stu-id="aea2d-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="aea2d-115">Po popolni uskladitvi honorarja ali predplačila na računu</span><span class="sxs-lookup"><span data-stu-id="aea2d-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-116">Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev</span><span class="sxs-lookup"><span data-stu-id="aea2d-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="aea2d-117">Ta znesek je pozitiven, saj naj bi odpravil negativno vrednost, ki je nastala ob izdaji računa za honorar ali predplačilo.</span><span class="sxs-lookup"><span data-stu-id="aea2d-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-118">Dejanska vrednost obračunane prodaje za znesek na tem računu</span><span class="sxs-lookup"><span data-stu-id="aea2d-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="aea2d-119">Po delni uskladitvi honorarja ali predplačila na računu</span><span class="sxs-lookup"><span data-stu-id="aea2d-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-120">Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev</span><span class="sxs-lookup"><span data-stu-id="aea2d-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="aea2d-121">Ta znesek je pozitiven, saj naj bi odpravil negativno vrednost, ki je nastala ob izdaji računa za honorar ali predplačilo.</span><span class="sxs-lookup"><span data-stu-id="aea2d-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-122">Dejanska vrednost obračunane prodaje za znesek na tem računu</span><span class="sxs-lookup"><span data-stu-id="aea2d-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-123">Neobračunana negativna dejanska vrednost prodaje preostanka zneska honorarja ali predplačila, ki se uporabi za usklajevanje prihodnjih računov.</span><span class="sxs-lookup"><span data-stu-id="aea2d-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="aea2d-124">Izdajanje računov za časovno transakcijo brez sprememb na osnutku računa</span><span class="sxs-lookup"><span data-stu-id="aea2d-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-125">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="aea2d-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-126">Dejanska vrednost obračunane prodaje za ure in znesek ob prvotni odobritvi časa</span><span class="sxs-lookup"><span data-stu-id="aea2d-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="aea2d-127">Izdajanje računov za časovno transakcijo, ki je bila urejena za zmanjšanje količine</span><span class="sxs-lookup"><span data-stu-id="aea2d-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-128">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="aea2d-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-129">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za ure in znesek na urejeni podrobnosti vrstice računa, storniranje dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="aea2d-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-130">Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek ur in zneska na urejeni podrobnosti vrstice računa, storniranje dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="aea2d-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="aea2d-131">Izdajanje računov za časovno transakcijo, ki je bila urejena za povečanje količine</span><span class="sxs-lookup"><span data-stu-id="aea2d-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-132">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="aea2d-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-133">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za ure in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="aea2d-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="aea2d-134">Izdajanje računov za transakcijo stroška brez sprememb na osnutku računa</span><span class="sxs-lookup"><span data-stu-id="aea2d-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-135">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="aea2d-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-136">Obračunana dejanska vrednost prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="aea2d-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="aea2d-137">Izdajanje računov za transakcijo stroška, ki je bila urejena za zmanjšanje količine</span><span class="sxs-lookup"><span data-stu-id="aea2d-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-138">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="aea2d-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-139">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="aea2d-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-140">Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek količine in zneska na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="aea2d-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="aea2d-141">Izdajanje računov za transakcijo stroška, ki je bila urejena za povečanje količine</span><span class="sxs-lookup"><span data-stu-id="aea2d-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-142">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="aea2d-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-143">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="aea2d-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="aea2d-144">Izdajanje računov za materialno transakcijo brez sprememb na osnutku računa.</span><span class="sxs-lookup"><span data-stu-id="aea2d-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-145">Storniranje neobračunane prodaje za količino in znesek na prvotni odobritvi uporabe materiala.</span><span class="sxs-lookup"><span data-stu-id="aea2d-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-146">Obračunana dejanska prodajna vrednost za količino in znesek na prvotni odobritvi uporabe materiala.</span><span class="sxs-lookup"><span data-stu-id="aea2d-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="aea2d-147">Izdajanje računov za materialno transakcijo, ki je bila urejena za zmanjšanje količine.</span><span class="sxs-lookup"><span data-stu-id="aea2d-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-148">Storniranje neobračunane prodaje za količino in znesek na prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="aea2d-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-149">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="aea2d-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-150">Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek količine in zneska na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="aea2d-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="aea2d-151">Izdajanje računov za materialno transakcijo, ki je bila urejena za povečanje količine.</span><span class="sxs-lookup"><span data-stu-id="aea2d-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-152">Storniranje neobračunane prodaje za količino in znesek na prvotni odobritvi uporabe materiala.</span><span class="sxs-lookup"><span data-stu-id="aea2d-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-153">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="aea2d-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="aea2d-154">Izdajanje računa za dajatev</span><span class="sxs-lookup"><span data-stu-id="aea2d-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-155">Storniranje neobračunane prodaje za znesek dajatev v prvotni vrstici dnevnika</span><span class="sxs-lookup"><span data-stu-id="aea2d-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-156">Obračunana dejanska vrednost prodaje za količino in znesek v prvotni vrstici dnevnika</span><span class="sxs-lookup"><span data-stu-id="aea2d-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="aea2d-157">Izdajanje računa za mejnik</span><span class="sxs-lookup"><span data-stu-id="aea2d-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-158">Obračunana dejanska vrednost prodaje za znesek mejnika iz prvotnega mejnika v podrobnosti projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="aea2d-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="aea2d-159">Izdajanje računa za podrobnost pogodbe, ki temelji na izdelku</span><span class="sxs-lookup"><span data-stu-id="aea2d-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="aea2d-160">Dejanska vrednost obračunane prodaje za linijo izdelkov s količino in zneskom iz podrobnosti pogodbe, ki temelji na izdelku</span><span class="sxs-lookup"><span data-stu-id="aea2d-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
