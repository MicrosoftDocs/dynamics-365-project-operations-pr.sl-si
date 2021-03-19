---
title: Potrditev predračuna – poenostavljena različica
description: Ta tema vsebuje informacije o potrjevanju predračunov v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274298"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="14991-103">Potrditev predračuna – poenostavljena različica</span><span class="sxs-lookup"><span data-stu-id="14991-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="14991-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="14991-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="14991-105">Po potrditvi predračuna se stanje računa projekta posodobi na **Potrjeno**.</span><span class="sxs-lookup"><span data-stu-id="14991-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="14991-106">Ko je račun potrjen, postane na voljo samo za branje.</span><span class="sxs-lookup"><span data-stu-id="14991-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="14991-107">V prihodnje se račun lahko popravi le, če popravke ali dobropis zahteva stranka oz. če je račun označen kot plačan.</span><span class="sxs-lookup"><span data-stu-id="14991-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="14991-108">V spodnji tabeli so navedeni dejanski podatki, ki jih je ustvaril sistem.</span><span class="sxs-lookup"><span data-stu-id="14991-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="14991-109">Ti dejanski podatki so ustvarjeni, ko se pred potrditvijo osnutka računa za projekt izvedejo določene operacije.</span><span class="sxs-lookup"><span data-stu-id="14991-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="14991-110">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="14991-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="14991-111">
                    <strong>Dejanski podatki, ustvarjeni ob potrditvi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="14991-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="14991-112">Račun za predujem ali honorar</span><span class="sxs-lookup"><span data-stu-id="14991-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-113">Dejanska vrednost obračunane prodaje vrste <strong>Honorar</strong> je ustvarjena za znesek predplačila ali honorarja.</span><span class="sxs-lookup"><span data-stu-id="14991-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-114">Neobračunana dejanska vrednost prodaje negativnega zneska honorarja ali predplačila, ki se uporabi za uskladitev.</span><span class="sxs-lookup"><span data-stu-id="14991-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="14991-115">Po popolni uskladitvi honorarja ali predplačila na računu</span><span class="sxs-lookup"><span data-stu-id="14991-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-116">Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev</span><span class="sxs-lookup"><span data-stu-id="14991-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="14991-117">Ta znesek je pozitiven, saj naj bi odpravil negativno vrednost, ki je nastala ob izdaji računa za honorar ali predplačilo.</span><span class="sxs-lookup"><span data-stu-id="14991-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-118">Dejanska vrednost obračunane prodaje za znesek na tem računu</span><span class="sxs-lookup"><span data-stu-id="14991-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="14991-119">Po delni uskladitvi honorarja ali predplačila na računu</span><span class="sxs-lookup"><span data-stu-id="14991-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-120">Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev</span><span class="sxs-lookup"><span data-stu-id="14991-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="14991-121">Ta znesek je pozitiven, saj naj bi odpravil negativno vrednost, ki je nastala ob izdaji računa za honorar ali predplačilo.</span><span class="sxs-lookup"><span data-stu-id="14991-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-122">Dejanska vrednost obračunane prodaje za znesek na tem računu</span><span class="sxs-lookup"><span data-stu-id="14991-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-123">Neobračunana negativna dejanska vrednost prodaje preostanka zneska honorarja ali predplačila, ki se uporabi za usklajevanje prihodnjih računov.</span><span class="sxs-lookup"><span data-stu-id="14991-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="14991-124">Izdajanje računov za časovno transakcijo brez sprememb na osnutku računa</span><span class="sxs-lookup"><span data-stu-id="14991-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-125">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="14991-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-126">Dejanska vrednost obračunane prodaje za ure in znesek ob prvotni odobritvi časa</span><span class="sxs-lookup"><span data-stu-id="14991-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="14991-127">Izdajanje računov za časovno transakcijo, ki je bila urejena za zmanjšanje količine</span><span class="sxs-lookup"><span data-stu-id="14991-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-128">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="14991-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-129">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za ure in znesek na urejeni podrobnosti vrstice računa, storniranje dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="14991-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-130">Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek ur in zneska na urejeni podrobnosti vrstice računa, storniranje dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="14991-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="14991-131">Izdajanje računov za časovno transakcijo, ki je bila urejena za povečanje količine</span><span class="sxs-lookup"><span data-stu-id="14991-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-132">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="14991-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-133">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za ure in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="14991-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="14991-134">Izdajanje računov za transakcijo stroška brez sprememb na osnutku računa</span><span class="sxs-lookup"><span data-stu-id="14991-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-135">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="14991-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-136">Obračunana dejanska vrednost prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="14991-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="14991-137">Izdajanje računov za transakcijo stroška, ki je bila urejena za zmanjšanje količine</span><span class="sxs-lookup"><span data-stu-id="14991-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-138">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="14991-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-139">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="14991-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-140">Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek količine in zneska na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="14991-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="14991-141">Izdajanje računov za transakcijo stroška, ki je bila urejena za povečanje količine</span><span class="sxs-lookup"><span data-stu-id="14991-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-142">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="14991-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-143">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="14991-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="14991-144">Izdajanje računa za dajatev</span><span class="sxs-lookup"><span data-stu-id="14991-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-145">Storniranje neobračunane prodaje za znesek dajatev v prvotni vrstici dnevnika</span><span class="sxs-lookup"><span data-stu-id="14991-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-146">Obračunana dejanska vrednost prodaje za količino in znesek v prvotni vrstici dnevnika</span><span class="sxs-lookup"><span data-stu-id="14991-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="14991-147">Izdajanje računa za mejnik</span><span class="sxs-lookup"><span data-stu-id="14991-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-148">Obračunana dejanska vrednost prodaje za znesek mejnika iz prvotnega mejnika v podrobnosti projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="14991-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="14991-149">Izdajanje računa za podrobnost pogodbe, ki temelji na izdelku</span><span class="sxs-lookup"><span data-stu-id="14991-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="14991-150">Dejanska vrednost obračunane prodaje za linijo izdelkov s količino in zneskom iz podrobnosti pogodbe, ki temelji na izdelku</span><span class="sxs-lookup"><span data-stu-id="14991-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]