---
title: Ujemanje potrdila s stroškom z uporabo OCR
description: Ta tema vsebuje informacije o obdelavi z optičnim prepoznavanjem znakov (OCR) za potrdila.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 62d6316c9602089518a94267d8ef2b7fb8d59cd0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084721"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="f8af4-103">Ujemanje potrdila s stroškom z uporabo OCR</span><span class="sxs-lookup"><span data-stu-id="f8af4-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="f8af4-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="f8af4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f8af4-105">Vnos stroškov je bil izboljšan z uvedbo obdelave z optičnim prepoznavanjem znakov (OCR) za potrdila.</span><span class="sxs-lookup"><span data-stu-id="f8af4-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="f8af4-106">Ta funkcionalnost je namenjena izboljšanju uporabniške izkušnje pri ustvarjanju poročil o stroških.</span><span class="sxs-lookup"><span data-stu-id="f8af4-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="f8af4-107">Najpomembnejše funkcije</span><span class="sxs-lookup"><span data-stu-id="f8af4-107">Key features</span></span>

- <span data-ttu-id="f8af4-108">Sistem izvleče ime trgovca, datum in skupni znesek iz potrdil.</span><span class="sxs-lookup"><span data-stu-id="f8af4-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="f8af4-109">Sistem bo poskušal izvesti ujemanje nepovezanih potrdil z nepovezanimi transakcijami stroškov.</span><span class="sxs-lookup"><span data-stu-id="f8af4-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="f8af4-110">Iz potrdil lahko ustvarite ročno vnesene transakcije stroškov.</span><span class="sxs-lookup"><span data-stu-id="f8af4-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="f8af4-111">Prilaganje potrdil poročilu o stroških</span><span class="sxs-lookup"><span data-stu-id="f8af4-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="f8af4-112">Za samodejno prilaganje potrdil, ki vključujejo transakcije s kreditnimi karticami, ko je ustvarjeno poročilo o stroških, izvedite naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="f8af4-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="f8af4-113">Odprite delovni prostor **Upravljanje stroškov**.</span><span class="sxs-lookup"><span data-stu-id="f8af4-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="f8af4-114">Na zavihku **Potrdila** preverite, ali obstajajo nepovezana potrdila.</span><span class="sxs-lookup"><span data-stu-id="f8af4-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="f8af4-115">Potrdila lahko naložite tudi na zavihek **Potrdila**.</span><span class="sxs-lookup"><span data-stu-id="f8af4-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="f8af4-116">Na zavihku **Stroški** preverite, ali obstajajo nepovezani stroški.</span><span class="sxs-lookup"><span data-stu-id="f8af4-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="f8af4-117">Običajno skrbnik stroškov uvozi te stroške od ponudnika kreditne kartice.</span><span class="sxs-lookup"><span data-stu-id="f8af4-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="f8af4-118">Izberite **Novo poročilo o stroških**.</span><span class="sxs-lookup"><span data-stu-id="f8af4-118">Select **New expense report**.</span></span> <span data-ttu-id="f8af4-119">Opazite lahko, da lahko zdaj vključite stroške in potrdila, ko ustvarite poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="f8af4-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="f8af4-120">Če dodate stroške in potrdila, se sproži samodejno ujemanje potrdil s stroški.</span><span class="sxs-lookup"><span data-stu-id="f8af4-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="f8af4-121">Ustvarjanje ali ujemanje potrdil za poročilo o stroških</span><span class="sxs-lookup"><span data-stu-id="f8af4-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="f8af4-122">Če želite ustvariti strošek ali poiskati ujemanje stroška s potrdila, izvedite naslednje korake.</span><span class="sxs-lookup"><span data-stu-id="f8af4-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="f8af4-123">Na poročilu o stroških na zavihku **Potrdila** priložite potrdilo z izbiro možnosti **Dodaj potrdila**.</span><span class="sxs-lookup"><span data-stu-id="f8af4-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="f8af4-124">Pod naloženo sliko potrdila opazite možnosti **Ustvari** in **Išči ujemanje**.</span><span class="sxs-lookup"><span data-stu-id="f8af4-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="f8af4-125">Izberite **Ustvari** , da ustvarite ročno vneseno transakcijo stroška in izpolnite vrednosti, ki so izvlečene iz potrdila.</span><span class="sxs-lookup"><span data-stu-id="f8af4-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="f8af4-126">Če izberete **Išči ujemanje** , sistem poskuša poiskati ujemanje obstoječega stroška s potrdilom.</span><span class="sxs-lookup"><span data-stu-id="f8af4-126">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="f8af4-127">Namestitev</span><span class="sxs-lookup"><span data-stu-id="f8af4-127">Installation</span></span>

<span data-ttu-id="f8af4-128">Če želite uporabiti te napredne zmožnosti stroškov, namestite dodatek za storitev upravljanja stroškov za Microsoft Dynamics 365 Finance in vklopite funkcije v svojem primerku.</span><span class="sxs-lookup"><span data-stu-id="f8af4-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="f8af4-129">Do dodatka lahko dostopate iz svojega projekta v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f8af4-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="f8af4-130">Prijavite se v LCS in odprite želeno okolje.</span><span class="sxs-lookup"><span data-stu-id="f8af4-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="f8af4-131">Odprite **Vse podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="f8af4-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="f8af4-132">Izberite **Vzdrževanje** ali se pomaknite navzdol do hitrega dostopa **Dodatki za okolje**.</span><span class="sxs-lookup"><span data-stu-id="f8af4-132">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="f8af4-133">Izberite **Namestitev novega dodatka**.</span><span class="sxs-lookup"><span data-stu-id="f8af4-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="f8af4-134">Izberite **Storitev za upravljanje stroškov**.</span><span class="sxs-lookup"><span data-stu-id="f8af4-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="f8af4-135">Sledite navodilom za namestitev ter sprejmite pogoje in določila.</span><span class="sxs-lookup"><span data-stu-id="f8af4-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="f8af4-136">Izberite **Namesti**.</span><span class="sxs-lookup"><span data-stu-id="f8af4-136">Select **Install**.</span></span>

<span data-ttu-id="f8af4-137">V delovnem prostoru **Upravljanje funkcij** vklopite naslednje funkcije:</span><span class="sxs-lookup"><span data-stu-id="f8af4-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="f8af4-138">Prenovljena poročila o stroških</span><span class="sxs-lookup"><span data-stu-id="f8af4-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="f8af4-139">Samodejno iskanje ujemanja in ustvarjanje stroška s potrdila</span><span class="sxs-lookup"><span data-stu-id="f8af4-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="f8af4-140">Ko vklopite te funkcije, se zgodijo naslednja dejanja:</span><span class="sxs-lookup"><span data-stu-id="f8af4-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="f8af4-141">Obstoječi delovni prostor **Upravljanje stroškov** se nadomesti z novim delovnim prostorom.</span><span class="sxs-lookup"><span data-stu-id="f8af4-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="f8af4-142">Dodana je nova postavka menija za vidljivost polja stroška.</span><span class="sxs-lookup"><span data-stu-id="f8af4-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="f8af4-143">Še vedno lahko odprete prejšnjo stran **Poročila o stroških** , tako da obiščete **Upravljanje stroškov > Moji stroški > Poročila o stroških**.</span><span class="sxs-lookup"><span data-stu-id="f8af4-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="f8af4-144">Poteki dela in morebitne odobritve vas še vedno vodijo na obstoječo stran s poročili o stroških.</span><span class="sxs-lookup"><span data-stu-id="f8af4-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="f8af4-145">Potrdila bodo obdelana prek Microsoft Azure Cognitive Services ter metapodatki bodo izvlečeni in dodani.</span><span class="sxs-lookup"><span data-stu-id="f8af4-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="f8af4-146">Dodana je možnost, ki omogoča ustvarjanje poročila o stroških, ki vključuje ujemajoča se nepovezana potrdila.</span><span class="sxs-lookup"><span data-stu-id="f8af4-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="f8af4-147">Možnost, ki je dodana v poročila o stroških, vam omogoča, da iz potrdila ustvarite vrstico stroška ali poskušate poiskati ujemanje obstoječega potrdila z obstoječo vrstico stroška.</span><span class="sxs-lookup"><span data-stu-id="f8af4-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="f8af4-148">Pogosto zastavljena vprašanja</span><span class="sxs-lookup"><span data-stu-id="f8af4-148">Frequently asked questions</span></span>

<span data-ttu-id="f8af4-149">**Ali Microsoft za svoje modele uporablja moje podatke?**</span><span class="sxs-lookup"><span data-stu-id="f8af4-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="f8af4-150">Ne, Microsoft je za storitev obdelave potrdil zgradil splošni model strojnega učenja.</span><span class="sxs-lookup"><span data-stu-id="f8af4-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="f8af4-151">Ta model ne temelji na potrdilih, ki jih naložite.</span><span class="sxs-lookup"><span data-stu-id="f8af4-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="f8af4-152">**Kje je na voljo in obdelana ta funkcija?**</span><span class="sxs-lookup"><span data-stu-id="f8af4-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="f8af4-153">Trenutno so podprte Združene države Amerike.</span><span class="sxs-lookup"><span data-stu-id="f8af4-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="f8af4-154">**Kam gredo moja potrdila?**</span><span class="sxs-lookup"><span data-stu-id="f8af4-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="f8af4-155">Storitev Finance pri Cognitive Services izvleče podatke polja.</span><span class="sxs-lookup"><span data-stu-id="f8af4-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="f8af4-156">Cognitive Services ohrani kopijo potrdila do 24 ur med izvajanjem obdelave.</span><span class="sxs-lookup"><span data-stu-id="f8af4-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="f8af4-157">Po končani obdelavi rešitev Cognitive Services potrdilo odstrani.</span><span class="sxs-lookup"><span data-stu-id="f8af4-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="f8af4-158">Potrdila so še vedno shranjena v storitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="f8af4-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="f8af4-159">Za več informacij glejte [Omogočanje razumevanja potrdil z novo zmožnostjo prepoznavalnika obrazcev](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="f8af4-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
