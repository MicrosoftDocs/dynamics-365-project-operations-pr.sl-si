---
title: Preslikava projektov in opravil v podrobnosti ponudbe, ki temelji na projektih
description: Ta tema ponuja informacije o tem, kako preslikati projekte in opravila v podrobnost opravila, ki temelji na projektih.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 871d323136cd982bd48ed9aa2b9c34017951d2d8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130733"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="61641-103">Preslikava projektov in opravil v podrobnosti ponudbe, ki temelji na projektih</span><span class="sxs-lookup"><span data-stu-id="61641-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="61641-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="61641-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="61641-105">V podrobnostih ponudbe, ki temeljijo na projektu, lahko preslikate določena opravila projekta, ki je že povezan s podrobnostjo ponudbe.</span><span class="sxs-lookup"><span data-stu-id="61641-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="61641-106">Ko preslikate opravila v podrobnost ponudbe, bodo naslednji elementi, ki ste jih določili v podrobnosti ponudbe, veljali samo za ta opravila:</span><span class="sxs-lookup"><span data-stu-id="61641-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="61641-107">Način obračunavanja</span><span class="sxs-lookup"><span data-stu-id="61641-107">Billing method</span></span>
- <span data-ttu-id="61641-108">Možnosti zaračunavanja</span><span class="sxs-lookup"><span data-stu-id="61641-108">Chargeability options</span></span>
- <span data-ttu-id="61641-109">Omejitve »Ni dovoljeno preseči«</span><span class="sxs-lookup"><span data-stu-id="61641-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="61641-110">Stranke</span><span class="sxs-lookup"><span data-stu-id="61641-110">Customers</span></span>

<span data-ttu-id="61641-111">Na primer, morda imate projekt, pri katerem je ena faza fiksna cena, vse druge faze pa so čas in materiali.</span><span class="sxs-lookup"><span data-stu-id="61641-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="61641-112">V tem primeru lahko prvo fazo in vsa njena podrejena opravila povežete s podrobnostjo ponudbe za to fazo z načinom obračunavanja po fiksni ceni.</span><span class="sxs-lookup"><span data-stu-id="61641-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="61641-113">Nato lahko vse ostale faze povežete s podrobnostjo ponudbe, ki temelji na ceni in materialih.</span><span class="sxs-lookup"><span data-stu-id="61641-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="61641-114">Povezava opravil s podrobnostmi ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="61641-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="61641-115">Opravila lahko povežete s podrobnostmi ponudb na naslednjih lokacijah:</span><span class="sxs-lookup"><span data-stu-id="61641-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="61641-116">Stran **Projekt** > zavihek **Obračunavanje opravil** (optimalno)</span><span class="sxs-lookup"><span data-stu-id="61641-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="61641-117">Stran **Podrobnost ponudbe** > zavihek **Opravila, ki se zaračunajo**</span><span class="sxs-lookup"><span data-stu-id="61641-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="61641-118">S strani Projekt</span><span class="sxs-lookup"><span data-stu-id="61641-118">From the Project page</span></span>

<span data-ttu-id="61641-119">Stran **Projekt** ponuja optimalno izkušnjo za povezovanje opravil s podrobnostmi ponudbe.</span><span class="sxs-lookup"><span data-stu-id="61641-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="61641-120">Na tej strani lahko izberete več opravil in vse skupaj z njihovimi podrejenimi opravili povežete z izbrano podrobnostjo ponudbe.</span><span class="sxs-lookup"><span data-stu-id="61641-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="61641-121">Na zavihku **Splošno** podrobnosti ponudbe, ki temelji na projektu, preverite, ali je izpolnjeno polje **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="61641-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="61641-122">V polju **Vključena opravila** izberite **Samo izbrana opravila**.</span><span class="sxs-lookup"><span data-stu-id="61641-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="61641-123">Shranite podrobnost ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="61641-123">Save the project-based quote line.</span></span> <span data-ttu-id="61641-124">Ko se obrazec osveži, se prikaže zavihek **Opravila, ki se zaračunajo**.</span><span class="sxs-lookup"><span data-stu-id="61641-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="61641-125">Na zavihku **Splošno** izberite povezavo do projekta v polju **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="61641-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="61641-126">Na strani **Projekt** izberite zavihek **Obračunavanje opravil**.</span><span class="sxs-lookup"><span data-stu-id="61641-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="61641-127">V drugi mreži, ki velja za nastavitev obračunavanja za posamezna opravila, izberite eno ali več opravil ter nato izberite **Povezava podrobnosti ponudb**.</span><span class="sxs-lookup"><span data-stu-id="61641-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="61641-128">V pogovornem oknu, ki se prikaže, izberite podrobnost ponudbe, ki v ponudbi prikazuje podrobnosti ponudbe, ki temeljijo na projektu.</span><span class="sxs-lookup"><span data-stu-id="61641-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="61641-129">V polju **Vrsta obračunavanja** navedite, ali so ta opravila plačljiva ali ne.</span><span class="sxs-lookup"><span data-stu-id="61641-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="61641-130">Izberite potrditveno polje, da označite, ali naj povezava vključuje podrejena opravila izbranih opravil.</span><span class="sxs-lookup"><span data-stu-id="61641-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="61641-131">Če potrdite polje, bodo podrejena opravila izbranih opravil povezana v podrobnost ponudbe.</span><span class="sxs-lookup"><span data-stu-id="61641-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="61641-132">Izberite **V redu**, da zaprete pogovorno okno.</span><span class="sxs-lookup"><span data-stu-id="61641-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="61641-133">Na strani »Podrobnost ponudbe«</span><span class="sxs-lookup"><span data-stu-id="61641-133">From the Quote line page</span></span>

<span data-ttu-id="61641-134">Projektna opravila lahko povežete s podrobnostmi ponudbe z zavihka **Opravila, ki se zaračunajo** na strani **Podrobnost ponudbe**.</span><span class="sxs-lookup"><span data-stu-id="61641-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="61641-135">Optimalno mesto za povezovanje projektnih opravil s podrobnostmi ponudbe je na zavihku **Obračunavanje opravil** na strani **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="61641-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="61641-136">Če opravila povežete z zavihka **Opravila, ki se zaračunajo** na strani **Podrobnost ponudbe**, morate ročno povezati vsak projekt.</span><span class="sxs-lookup"><span data-stu-id="61641-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="61641-137">Na zavihku **Splošno** podrobnosti ponudbe, ki temelji na projektu, preverite, ali je v polju **Projekt** izbran projekt.</span><span class="sxs-lookup"><span data-stu-id="61641-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="61641-138">V polju **Vključena opravila** izberite **Samo izbrana opravila**.</span><span class="sxs-lookup"><span data-stu-id="61641-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="61641-139">Shranite podrobnost ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="61641-139">Save the project-based quote line.</span></span> <span data-ttu-id="61641-140">Ko se obrazec osveži, se prikaže zavihek **Opravila, ki se zaračunajo**.</span><span class="sxs-lookup"><span data-stu-id="61641-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="61641-141">Na zavihku **Opravila, ki se zaračunajo** izberite **Dodaj opravilo za podrobnost ponudbe**.</span><span class="sxs-lookup"><span data-stu-id="61641-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="61641-142">Na strani **Opravilo za podrobnost ponudbe** v polju **Opravila** izberite opravilo in v polju **Vrsta obračunavanja** izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="61641-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="61641-143">Zaprite stran.</span><span class="sxs-lookup"><span data-stu-id="61641-143">Close the page.</span></span> <span data-ttu-id="61641-144">Izbrano opravilo je zdaj povezano s podrobnostjo ponudbe.</span><span class="sxs-lookup"><span data-stu-id="61641-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="61641-145">Prekinite povezavo opravil s podrobnostmi ponudb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="61641-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="61641-146">S strani Projekt</span><span class="sxs-lookup"><span data-stu-id="61641-146">From the Project page</span></span>

<span data-ttu-id="61641-147">Ta način ponuja optimalno izkušnjo za prekinitev povezave opravil s podrobnostmi ponudbe.</span><span class="sxs-lookup"><span data-stu-id="61641-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="61641-148">Izberete lahko več opravil in prekinete povezavo vseh, tudi njihovih podrejenih opravil, z izbrano podrobnostjo ponudbe.</span><span class="sxs-lookup"><span data-stu-id="61641-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="61641-149">Na zavihku **Splošno** podrobnosti ponudbe, ki temelji na projektu, v polju **Projekt** izberite povezavo projekta.</span><span class="sxs-lookup"><span data-stu-id="61641-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="61641-150">Na strani **Projekt** izberite zavihek **Obračunavanje opravil**.</span><span class="sxs-lookup"><span data-stu-id="61641-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="61641-151">V drugi mreži, ki velja za nastavitev obračunavanja za posamezna opravila, izberite eno ali več opravil ter nato izberite **Prekini povezavo podrobnosti ponudb**.</span><span class="sxs-lookup"><span data-stu-id="61641-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="61641-152">Na pogovornem oknu, ki se odpre, izberite podrobnost ponudbe.</span><span class="sxs-lookup"><span data-stu-id="61641-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="61641-153">Izberite potrditveno polje, da označite, ali naj se povezava odstrani tudi od podrejenih opravil izbranih opravil.</span><span class="sxs-lookup"><span data-stu-id="61641-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="61641-154">Če potrdite polje, bo prekinjena povezava podrejenih opravil izbranih opravil s podrobnostjo ponudbe.</span><span class="sxs-lookup"><span data-stu-id="61641-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="61641-155">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="61641-155">Select **OK**.</span></span> <span data-ttu-id="61641-156">Opozorilno sporočilo vas obvešča, da če odstranite to povezavo, se lahko vse dejanske vrednosti, ki so bili predhodno zabeleženi pri opravilu, razveljavijo.</span><span class="sxs-lookup"><span data-stu-id="61641-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="61641-157">Izberite **V redu** za potrditev in odstranjevanje povezave med opravilom in podrobnostjo ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="61641-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="61641-158">Na strani »Podrobnost ponudbe«</span><span class="sxs-lookup"><span data-stu-id="61641-158">From the Quote line page</span></span>

<span data-ttu-id="61641-159">Povezavo projektnih opravil s podrobnostmi ponudbe lahko tudi prekinete z zavihka **Opravila, ki se zaračunajo** na strani **Podrobnost ponudbe**.</span><span class="sxs-lookup"><span data-stu-id="61641-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="61641-160">Na zavihku **Opravila, ki se zaračunajo** izberite **Izbriši opravilo za podrobnost ponudbe**.</span><span class="sxs-lookup"><span data-stu-id="61641-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="61641-161">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="61641-161">Select **OK**.</span></span> <span data-ttu-id="61641-162">Opozorilno sporočilo vas obvešča, da če odstranite to povezavo, se lahko vse dejanske vrednosti, ki so bili predhodno zabeleženi pri opravilu, razveljavijo.</span><span class="sxs-lookup"><span data-stu-id="61641-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="61641-163">Izberite **V redu** za potrditev in odstranjevanje povezave med opravilom in podrobnostjo ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="61641-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="61641-164">Ta postopek ne izbriše opravila iz projekta.</span><span class="sxs-lookup"><span data-stu-id="61641-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="61641-165">Zgolj odstrani povezavo opravila od podrobnosti ponudbe, ki temelji na projektu.</span><span class="sxs-lookup"><span data-stu-id="61641-165">It only removes the task association from the project-based quote line.</span></span>
