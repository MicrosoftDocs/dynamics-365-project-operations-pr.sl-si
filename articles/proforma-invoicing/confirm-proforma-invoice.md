---
title: Potrditev predračuna, ki temelji na projektu
description: Ta tema vsebuje informacije o potrditvi predračuna, ki temelji na projektu.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012156"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="425be-103">Potrditev predračuna, ki temelji na projektu</span><span class="sxs-lookup"><span data-stu-id="425be-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="425be-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="425be-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="425be-105">Po potrditvi predračuna se stanje računa projekta posodobi na **Potrjeno**.</span><span class="sxs-lookup"><span data-stu-id="425be-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="425be-106">Ko je račun potrjen, postane na voljo samo za branje.</span><span class="sxs-lookup"><span data-stu-id="425be-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="425be-107">V prihodnje je račun mogoče popraviti le, če obstajajo popravki ali dobroimetja, ki jih sproži stranka.</span><span class="sxs-lookup"><span data-stu-id="425be-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="425be-108">V spodnji tabeli so navedeni dejanski podatki, ki jih je ustvaril sistem.</span><span class="sxs-lookup"><span data-stu-id="425be-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="425be-109">Ti dejanski podatki so ustvarjeni, ko se pred potrditvijo osnutka računa za projekt izvedejo določene operacije.</span><span class="sxs-lookup"><span data-stu-id="425be-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="425be-110">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="425be-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="425be-111">
                    <strong>Dejanski podatki, ustvarjeni ob potrditvi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="425be-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="425be-112">Račun za predujem ali honorar</span><span class="sxs-lookup"><span data-stu-id="425be-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-113">Dejanska vrednost obračunane prodaje vrste <strong>Honorar</strong> je ustvarjena za znesek predplačila ali honorarja.</span><span class="sxs-lookup"><span data-stu-id="425be-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-114">Za usklajevanje se uporabi dejanska neobračunana prodaja z negativnim zneskom honorarja ali predujma.</span><span class="sxs-lookup"><span data-stu-id="425be-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="425be-115">Po popolni uskladitvi honorarja ali predplačila na računu</span><span class="sxs-lookup"><span data-stu-id="425be-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-116">Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev</span><span class="sxs-lookup"><span data-stu-id="425be-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="425be-117">Ta znesek je pozitiven, saj naj bi odpravil negativno vrednost, ki je nastala ob izdaji računa za honorar ali predplačilo.</span><span class="sxs-lookup"><span data-stu-id="425be-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-118">Dejanska vrednost obračunane prodaje za znesek na tem računu</span><span class="sxs-lookup"><span data-stu-id="425be-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="425be-119">Po delni uskladitvi honorarja ali predplačila na računu</span><span class="sxs-lookup"><span data-stu-id="425be-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-120">Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev</span><span class="sxs-lookup"><span data-stu-id="425be-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="425be-121">Ta znesek je pozitiven, saj naj bi odpravil negativno vrednost, ki je nastala ob izdaji računa za honorar ali predplačilo.</span><span class="sxs-lookup"><span data-stu-id="425be-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-122">Dejanska vrednost obračunane prodaje za znesek na tem računu</span><span class="sxs-lookup"><span data-stu-id="425be-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-123">Neobračunana negativna dejanska vrednost prodaje preostanka zneska honorarja ali predplačila, ki se uporabi za usklajevanje prihodnjih računov.</span><span class="sxs-lookup"><span data-stu-id="425be-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="425be-124">Izdajanje računov za časovno transakcijo brez sprememb na osnutku računa</span><span class="sxs-lookup"><span data-stu-id="425be-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-125">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="425be-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-126">Dejanska vrednost obračunane prodaje za ure in znesek ob prvotni odobritvi časa</span><span class="sxs-lookup"><span data-stu-id="425be-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="425be-127">Izdajanje računov za časovno transakcijo, ki je bila urejena za zmanjšanje količine</span><span class="sxs-lookup"><span data-stu-id="425be-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-128">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="425be-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-129">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za ure in znesek na urejeni podrobnosti vrstice računa, storniranje dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="425be-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-130">Nova dejanska neobračunana prodaja, ki se ne zaračuna za preostanek ur in zneska po odštetju popravljenih številk za podrobnosti urejene vrstice računa, razveljavitev dejanske prodaje in enakovredna dejanska obračunana prodaja.</span><span class="sxs-lookup"><span data-stu-id="425be-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="425be-131">Izdajanje računov za časovno transakcijo, ki je bila urejena za povečanje količine</span><span class="sxs-lookup"><span data-stu-id="425be-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-132">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="425be-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-133">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za ure in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="425be-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="425be-134">Izdajanje računov za transakcijo stroška brez sprememb na osnutku računa</span><span class="sxs-lookup"><span data-stu-id="425be-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-135">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="425be-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-136">Obračunana dejanska vrednost prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="425be-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="425be-137">Izdajanje računov za transakcijo stroška, ki je bila urejena za zmanjšanje količine</span><span class="sxs-lookup"><span data-stu-id="425be-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-138">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="425be-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-139">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="425be-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-140">Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek količine in zneska na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="425be-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="425be-141">Izdajanje računov za transakcijo stroška, ki je bila urejena za povečanje količine</span><span class="sxs-lookup"><span data-stu-id="425be-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-142">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="425be-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-143">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="425be-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="425be-144">Izdajanje računov za materialno transakcijo brez sprememb na osnutku računa.</span><span class="sxs-lookup"><span data-stu-id="425be-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-145">Storniranje neobračunane prodaje za količino in znesek na prvotni odobritvi uporabe materiala.</span><span class="sxs-lookup"><span data-stu-id="425be-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-146">Obračunana dejanska prodajna vrednost za količino in znesek na prvotni odobritvi uporabe materiala.</span><span class="sxs-lookup"><span data-stu-id="425be-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="425be-147">Izdajanje računov za materialno transakcijo, ki je bila urejena za zmanjšanje količine.</span><span class="sxs-lookup"><span data-stu-id="425be-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-148">Storniranje neobračunane prodaje za količino in znesek na prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="425be-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-149">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="425be-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-150">Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek količine in zneska na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="425be-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="425be-151">Izdajanje računov za materialno transakcijo, ki je bila urejena za povečanje količine.</span><span class="sxs-lookup"><span data-stu-id="425be-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-152">Storniranje neobračunane prodaje za količino in znesek na prvotni odobritvi uporabe materiala.</span><span class="sxs-lookup"><span data-stu-id="425be-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-153">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="425be-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="425be-154">Izdajanje računa za dajatev</span><span class="sxs-lookup"><span data-stu-id="425be-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-155">Storniranje neobračunane prodaje za znesek dajatev v prvotni vrstici dnevnika</span><span class="sxs-lookup"><span data-stu-id="425be-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-156">Obračunana dejanska vrednost prodaje za količino in znesek v prvotni vrstici dnevnika</span><span class="sxs-lookup"><span data-stu-id="425be-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="425be-157">Izdajanje računa za mejnik</span><span class="sxs-lookup"><span data-stu-id="425be-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="425be-158">Obračunana dejanska vrednost prodaje za znesek mejnika iz prvotnega mejnika v podrobnosti projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="425be-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
