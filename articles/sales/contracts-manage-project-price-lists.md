---
title: Upravljanje projektnih cenikov v projektnih pogodbah
description: V tej temi so na voljo informacije o upravljanju projektnih cenikov v projektnih pogodbah.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278618"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="734ee-103">Upravljanje projektnih cenikov v projektnih pogodbah</span><span class="sxs-lookup"><span data-stu-id="734ee-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="734ee-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="734ee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="734ee-105">Projektne pogodbe v storitvi Dynamics 365 Project Operations so zasnovane za podporo več prodajnih cenikov, veljavnih na datum, v pogodbi.</span><span class="sxs-lookup"><span data-stu-id="734ee-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="734ee-106">V storitvi Project Operations obstaja nova povezana entiteta, imenovana **Projektni ceniki**.</span><span class="sxs-lookup"><span data-stu-id="734ee-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="734ee-107">Ta entiteta ima odnos »ena proti mnogo« s projektno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="734ee-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="734ee-108">Ceniki projektov se uporabljajo za določanje časovnih in stroškovnih transakcij projekta.</span><span class="sxs-lookup"><span data-stu-id="734ee-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="734ee-109">Ko ima pogodba enega ali več cenikov projektov, se ti ceniki uporabijo za nastavitev cene za ocene časa in stroška ter dejanskih vrednosti za projekte, ki so povezani s pogodbo prek podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="734ee-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="734ee-110">Ko ni projektnih cenikov v projektni pogodbi, boste videli opozorilo, da ni projektnih cenikov ter za vaše ocene, dejansko projektno delo in stroške cena ne bo nastavljena.</span><span class="sxs-lookup"><span data-stu-id="734ee-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="734ee-111">Ne bo cene za prodajne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="734ee-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="734ee-112">Povezava ali odstranjevanje povezave cenika projekta v projektni pogodbi</span><span class="sxs-lookup"><span data-stu-id="734ee-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="734ee-113">Ustvarjanje ali povezovanje specifičnih cenikov za ocenjevanje dela in stroškov, ki temeljijo na projektu</span><span class="sxs-lookup"><span data-stu-id="734ee-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="734ee-114">V projektni pogodbi izberite zavihek **Projektni ceniki**.</span><span class="sxs-lookup"><span data-stu-id="734ee-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="734ee-115">V podmreži izberite **+ Dodaj nov cenik projekta**.</span><span class="sxs-lookup"><span data-stu-id="734ee-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="734ee-116">Na drsniku **Hitro ustvarjanje** izberite cenik.</span><span class="sxs-lookup"><span data-stu-id="734ee-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="734ee-117">V spustnem seznamu so prikazani vsi ceniki, ki imajo kontekst nastavljen na **Prodaja**, kjer se valuta na ceniku ujema z valuto v pogodbi.</span><span class="sxs-lookup"><span data-stu-id="734ee-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="734ee-118">Vnesite opis za povezavo cenika projekta, izberite **Shrani**, nato pa zaprite drsnik **Hitro ustvarjanje**.</span><span class="sxs-lookup"><span data-stu-id="734ee-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="734ee-119">Ustvari se povezava s cenikom projekta.</span><span class="sxs-lookup"><span data-stu-id="734ee-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="734ee-120">Ponovite korake 1–4, da povežete več kot en cenik s projektno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="734ee-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="734ee-121">Več projektnih cenikov ustvarite samo, če imate drugačen datum veljavnosti na vsakem od povezanih projektnih cenikov.</span><span class="sxs-lookup"><span data-stu-id="734ee-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="734ee-122">Project Operations ne podpira prekrivanja datumske veljavnosti projektnih cenikov.</span><span class="sxs-lookup"><span data-stu-id="734ee-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="734ee-123">Če obstaja več projektnih cenikov za transakcijo z določenim datumom, bo cena za to transakcijo privzeto povrnjena na nič.</span><span class="sxs-lookup"><span data-stu-id="734ee-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="734ee-124">Odstranitev povezave projektnega cenika</span><span class="sxs-lookup"><span data-stu-id="734ee-124">Remove a project price list association</span></span>

- <span data-ttu-id="734ee-125">Izberite projektni cenik in nato izberite **Brisanje pogodbenega projektnega cenika** v podmreži.</span><span class="sxs-lookup"><span data-stu-id="734ee-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="734ee-126">Cenik je odstranjen iz projektnih cenikov na pogodbi.</span><span class="sxs-lookup"><span data-stu-id="734ee-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="734ee-127">Cenik sam ne bo izbrisan.</span><span class="sxs-lookup"><span data-stu-id="734ee-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="734ee-128">Izbrisana bo samo povezava do cenika.</span><span class="sxs-lookup"><span data-stu-id="734ee-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="734ee-129">V pogodbi nastavite samodejno povrnitev projektnih cenikov na privzeto</span><span class="sxs-lookup"><span data-stu-id="734ee-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="734ee-130">Projektni cenik je mogoče nastaviti kot privzeti cenik na projektni pogodbi.</span><span class="sxs-lookup"><span data-stu-id="734ee-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="734ee-131">Ta nastavitev lahko pomaga zagotoviti, da vsi stiki v vaši organizaciji vedno začnejo s standardnim cenikom za to časovno obdobje.</span><span class="sxs-lookup"><span data-stu-id="734ee-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="734ee-132">Nastavitev organizacijske privzete nastavitve za projektne cenike</span><span class="sxs-lookup"><span data-stu-id="734ee-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="734ee-133">Odprite **Nastavitve** > **Splošno**, nato pa izberite **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="734ee-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="734ee-134">Na strani s seznamom **Aktivni parametri** izberite in dvokliknite zapis, da ga odprete.</span><span class="sxs-lookup"><span data-stu-id="734ee-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="734ee-135">Med dvoklikom se prepričajte, da ne klikate v vrednost polja, ki je hiperpovezava.</span><span class="sxs-lookup"><span data-stu-id="734ee-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="734ee-136">Na strani **Aktivni parametri** izberite zavihek **Cenik**. Podmreža prikaže seznam privzetih cenikov.</span><span class="sxs-lookup"><span data-stu-id="734ee-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="734ee-137">To je seznam standardnih cen in prodajnih cenikov.</span><span class="sxs-lookup"><span data-stu-id="734ee-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="734ee-138">Če je tukaj povezan cenik **Prodaja** za vsako valuto, v kateri prodajate, to zagotavlja, da je prodajni cenik privzet za vsako pogodbo, ki jo ustvarite za stranke, ki izvajajo transakcije v tej valuti.</span><span class="sxs-lookup"><span data-stu-id="734ee-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="734ee-139">Nastavitev projektnega cenika, specifičnega za stranko</span><span class="sxs-lookup"><span data-stu-id="734ee-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="734ee-140">Nastavite lahko tudi projektne cenike za specifično stranko, ko ste se dogovorili za glavni dogovor o cenah s strankami.</span><span class="sxs-lookup"><span data-stu-id="734ee-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="734ee-141">Odprite **Prodaja** > **Stranke**.</span><span class="sxs-lookup"><span data-stu-id="734ee-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="734ee-142">Na seznamu aktivnih računov izberite stranko, za katero imate poseben cenik.</span><span class="sxs-lookup"><span data-stu-id="734ee-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="734ee-143">Izberite zapis stranke, da ga odprete in nato izberite zavihek **Projektni ceniki**. Podmreža prikaže seznam projektnih cenikov, specifičnih za to stranko.</span><span class="sxs-lookup"><span data-stu-id="734ee-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="734ee-144">Tukaj ustvarite novo povezavo cenika za projektni cenik, specifičen za to stranko.</span><span class="sxs-lookup"><span data-stu-id="734ee-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="734ee-145">Cene po meri za projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="734ee-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="734ee-146">Ko imate organizacijske in privzete projekte cenike, specifične za stranko, bodo vaše projektne pogodbe samodejno ustvarjene s temi povezavami projektnih cenikov.</span><span class="sxs-lookup"><span data-stu-id="734ee-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="734ee-147">Projektni ceniki na projektni pogodbi pa so vedno kopirani s pripetim datumom in imenom pogodbe.</span><span class="sxs-lookup"><span data-stu-id="734ee-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="734ee-148">Upravitelji kupcev in projektni vodje lahko nato začnejo urejati cene za te kopije.</span><span class="sxs-lookup"><span data-stu-id="734ee-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="734ee-149">Te spremenjene cene bodo veljale samo za to projektno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="734ee-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]