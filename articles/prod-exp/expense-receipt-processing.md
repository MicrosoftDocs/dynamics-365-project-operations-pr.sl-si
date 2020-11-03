---
title: Obdelava potrdila o stroških
description: Ta tema vsebuje informacije o obdelavi z optičnim prepoznavanjem znakov (OCR) za potrdila. Ta funkcija je namenjena izboljšanju uporabniške izkušnje pri ustvarjanju poročil o stroških v storitvi Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084914"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="9e6d9-104">Obdelava potrdila o stroških</span><span class="sxs-lookup"><span data-stu-id="9e6d9-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e6d9-105">Vnos stroškov je bil izboljšan z uvedbo obdelave z optičnim prepoznavanjem znakov (OCR) za potrdila.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="9e6d9-106">Ta funkcija je namenjena izboljšanju uporabniške izkušnje pri ustvarjanju poročil o stroških.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="9e6d9-107">Najpomembnejše funkcije</span><span class="sxs-lookup"><span data-stu-id="9e6d9-107">Key features</span></span>

- <span data-ttu-id="9e6d9-108">Ime trgovca, datum in skupni znesek se izvlečejo iz potrdil.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="9e6d9-109">Funkcija poskuša izvesti ujemanje nepovezanih potrdil z nepovezanimi transakcijami stroškov.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="9e6d9-110">Uporabniki lahko ročno vnesejo transakcije stroškov iz potrdil.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="9e6d9-111">Primeri uporabe</span><span class="sxs-lookup"><span data-stu-id="9e6d9-111">Usage examples</span></span>

<span data-ttu-id="9e6d9-112">Za samodejno prilaganje potrdil, ki vključujejo transakcije s kreditnimi karticami, ko je ustvarjeno poročilo o stroških, storite naslednje:</span><span class="sxs-lookup"><span data-stu-id="9e6d9-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="9e6d9-113">Odprite delovni prostor **Upravljanje stroškov**.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="9e6d9-114">Na zavihku **Potrdila** preverite, ali obstajajo nepovezana potrdila.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="9e6d9-115">Potrdila lahko naložite tudi na zavihek **Potrdila**.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="9e6d9-116">Na zavihku **Stroški** preverite, ali obstajajo nepovezani stroški.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="9e6d9-117">Običajno skrbnik stroškov uvozi te stroške od ponudnika kreditne kartice.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="9e6d9-118">Izberite **Novo poročilo o stroških**.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-118">Select **New expense report**.</span></span> <span data-ttu-id="9e6d9-119">Opazite lahko, da lahko zdaj vključite stroške in potrdila, ko ustvarite poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="9e6d9-120">Če dodate stroške in potrdila, se sproži samodejno ujemanje potrdil s stroški.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="9e6d9-121">Če želite ustvariti strošek ali poiskati ujemanje stroška s potrdila, storite naslednje:</span><span class="sxs-lookup"><span data-stu-id="9e6d9-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="9e6d9-122">Na poročilu o stroških na zavihku **Potrdila** priložite potrdilo z izbiro možnosti **Dodaj potrdila**.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="9e6d9-123">Pod naloženo sliko potrdila opazite možnosti **Ustvari** in **Išči ujemanje**.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="9e6d9-124">Izberite **Ustvari** , da ustvarite ročno vneseno transakcijo stroška in izpolnite vrednosti, ki so izvlečene iz potrdila.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="9e6d9-125">Če izberete **Išči ujemanje** , sistem poskuša poiskati ujemanje obstoječega stroška s potrdilom.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-125">If you select **Match** , the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="9e6d9-126">Namestitev</span><span class="sxs-lookup"><span data-stu-id="9e6d9-126">Installation</span></span>

<span data-ttu-id="9e6d9-127">Ta funkcija deluje v kombinaciji s funkcijo **Preoblikovana poročila o stroških** za poenostavljeno izkušnjo s stroški.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="9e6d9-128">Ta funkcija je na voljo samo za okolja Tier 2+, in sicer preskusna in produkcijska okolja.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="9e6d9-129">Če želite uporabiti te napredne zmožnosti stroškov, namestite dodatek za storitev upravljanja stroškov za Microsoft Dynamics 365 Finance in vklopite funkcije v svojem primerku.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="9e6d9-130">Do dodatka lahko dostopate iz svojega projekta v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9e6d9-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="9e6d9-131">Prijavite se v LCS in odprite želeno okolje.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="9e6d9-132">Odprite **Vse podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="9e6d9-133">Izberite **Vzdrževanje** ali se pomaknite navzdol do hitrega dostopa **Dodatki za okolje**.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-133">Select **Maintain** , or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="9e6d9-134">Izberite **Namestitev novega dodatka**.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="9e6d9-135">Izberite **Storitev za upravljanje stroškov**.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="9e6d9-136">Sledite navodilom za namestitev ter sprejmite pogoje in določila.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="9e6d9-137">Izberite **Namesti**.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-137">Select **Install**.</span></span>

<span data-ttu-id="9e6d9-138">V delovnem prostoru **Upravljanje funkcij** vklopite naslednje funkcije:</span><span class="sxs-lookup"><span data-stu-id="9e6d9-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="9e6d9-139">Prenovljena poročila o stroških</span><span class="sxs-lookup"><span data-stu-id="9e6d9-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="9e6d9-140">Samodejno iskanje ujemanja in ustvarjanje stroška s potrdila</span><span class="sxs-lookup"><span data-stu-id="9e6d9-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="9e6d9-141">Ko vklopite te funkcije, se zgodijo naslednja dejanja:</span><span class="sxs-lookup"><span data-stu-id="9e6d9-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="9e6d9-142">Obstoječi delovni prostor **Upravljanje stroškov** se nadomesti z novim delovnim prostorom.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="9e6d9-143">Dodana je nova postavka menija za vidljivost polja stroška.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="9e6d9-144">Še vedno lahko odprete prejšnjo stran **Poročila o stroških** , tako da obiščete **Upravljanje stroškov > Moji stroški > Poročila o stroških**.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="9e6d9-145">Poteki dela in morebitne odobritve vas še vedno vodijo na obstoječo stran s poročili o stroških.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="9e6d9-146">Potrdila bodo obdelana prek Microsoft Azure Cognitive Services ter metapodatki bodo izvlečeni in dodani.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="9e6d9-147">Dodana je možnost, ki omogoča ustvarjanje poročila o stroških, ki vključuje ujemajoča se nepovezana potrdila.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="9e6d9-148">Možnost, ki je dodana v poročila o stroških, vam omogoča, da iz potrdila ustvarite vrstico stroška ali poskušate poiskati ujemanje obstoječega potrdila z obstoječo vrstico stroška.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="9e6d9-149">Za več informacij o preoblikovani funkciji poročil o stroških glejte [Preoblikovana poročila o stroških](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="9e6d9-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="9e6d9-150">Pogosto zastavljena vprašanja</span><span class="sxs-lookup"><span data-stu-id="9e6d9-150">Frequently asked questions</span></span>

<span data-ttu-id="9e6d9-151">**Ali Microsoft za svoje modele uporablja moje podatke?**</span><span class="sxs-lookup"><span data-stu-id="9e6d9-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="9e6d9-152">Ne, Microsoft je za storitev obdelave potrdil zgradil splošni model strojnega učenja.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="9e6d9-153">Ta model ne temelji na potrdilih, ki jih naložite.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="9e6d9-154">**Kje je na voljo in obdelana ta funkcija?**</span><span class="sxs-lookup"><span data-stu-id="9e6d9-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="9e6d9-155">Trenutno so podprte Združene države Amerike.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="9e6d9-156">**Kam gredo moja potrdila?**</span><span class="sxs-lookup"><span data-stu-id="9e6d9-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="9e6d9-157">Storitev Finance pri Cognitive Services izvleče podatke polja.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="9e6d9-158">Cognitive Services ohrani kopijo potrdila do 24 ur med izvajanjem obdelave.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="9e6d9-159">Po končani obdelavi rešitev Cognitive Services potrdilo odstrani.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="9e6d9-160">Potrdila so še vedno shranjena v storitvi Finance.</span><span class="sxs-lookup"><span data-stu-id="9e6d9-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="9e6d9-161">Za več informacij glejte [Omogočanje razumevanja potrdil z novo zmožnostjo prepoznavalnika obrazcev](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="9e6d9-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
