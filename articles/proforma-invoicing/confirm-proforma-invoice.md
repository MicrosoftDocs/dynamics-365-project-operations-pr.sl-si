---
title: Potrditev predračuna
description: Ta tema vsebuje informacije o potrditvi predračuna.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287888"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="8b72f-103">Potrditev predračuna</span><span class="sxs-lookup"><span data-stu-id="8b72f-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="8b72f-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="8b72f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8b72f-105">Po potrditvi predračuna se stanje računa projekta posodobi na **Potrjeno**.</span><span class="sxs-lookup"><span data-stu-id="8b72f-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="8b72f-106">Ko je račun potrjen, postane na voljo samo za branje.</span><span class="sxs-lookup"><span data-stu-id="8b72f-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="8b72f-107">V prihodnje je račun lahko popravljen le, če popravke ali dobropis zahteva stranka oz. če je račun označen kot plačan.</span><span class="sxs-lookup"><span data-stu-id="8b72f-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="8b72f-108">V spodnji tabeli so navedeni dejanski podatki, ki jih je ustvaril sistem.</span><span class="sxs-lookup"><span data-stu-id="8b72f-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="8b72f-109">Ti dejanski podatki so ustvarjeni, ko se pred potrditvijo osnutka računa za projekt izvedejo določene operacije.</span><span class="sxs-lookup"><span data-stu-id="8b72f-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="8b72f-110">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b72f-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="8b72f-111">
                    <strong>Dejanski podatki, ustvarjeni ob potrditvi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b72f-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b72f-112">Izdajanje računov za časovno transakcijo brez sprememb na osnutku računa</span><span class="sxs-lookup"><span data-stu-id="8b72f-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-113">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="8b72f-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-114">Dejanska vrednost obračunane prodaje za ure in znesek ob prvotni odobritvi časa</span><span class="sxs-lookup"><span data-stu-id="8b72f-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8b72f-115">Izdajanje računov za časovno transakcijo, ki je bila urejena za zmanjšanje količine</span><span class="sxs-lookup"><span data-stu-id="8b72f-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-116">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="8b72f-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-117">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za ure in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="8b72f-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-118">Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek ur in zneska na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje.</span><span class="sxs-lookup"><span data-stu-id="8b72f-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b72f-119">Izdajanje računov za časovno transakcijo, ki je bila urejena za povečanje količine</span><span class="sxs-lookup"><span data-stu-id="8b72f-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-120">Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.</span><span class="sxs-lookup"><span data-stu-id="8b72f-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-121">Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za ure in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="8b72f-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b72f-122">Izdajanje računov za transakcijo stroška brez sprememb na osnutku računa</span><span class="sxs-lookup"><span data-stu-id="8b72f-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-123">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="8b72f-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-124">Obračunana dejanska vrednost prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="8b72f-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8b72f-125">Izdajanje računov za transakcijo stroška, ki je bila urejena za zmanjšanje količine</span><span class="sxs-lookup"><span data-stu-id="8b72f-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-126">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="8b72f-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-127">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="8b72f-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-128">Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek količine in zneska na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="8b72f-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b72f-129">Izdajanje računov za transakcijo stroška, ki je bila urejena za povečanje količine</span><span class="sxs-lookup"><span data-stu-id="8b72f-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-130">Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov</span><span class="sxs-lookup"><span data-stu-id="8b72f-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-131">Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="8b72f-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b72f-132">Izdajanje računa za dajatev</span><span class="sxs-lookup"><span data-stu-id="8b72f-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-133">Storniranje neobračunane prodaje za znesek dajatev v prvotni vrstici dnevnika</span><span class="sxs-lookup"><span data-stu-id="8b72f-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-134">Obračunana dejanska vrednost prodaje za količino in znesek v prvotni vrstici dnevnika</span><span class="sxs-lookup"><span data-stu-id="8b72f-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="8b72f-135">Izdajanje računa za mejnik</span><span class="sxs-lookup"><span data-stu-id="8b72f-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8b72f-136">Obračunana dejanska vrednost prodaje za znesek mejnika iz prvotnega mejnika v podrobnosti projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="8b72f-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]