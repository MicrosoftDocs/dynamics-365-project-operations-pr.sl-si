---
title: Ustvarjanje časovnih vnosov
description: Ta tema vsebuje informacije o ustvarjanju časovnih vnosov.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 878413a24baa340b745a045a6991a63a00851c8b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084847"
---
# <a name="create-time-entries"></a><span data-ttu-id="cb864-103">Ustvarjanje časovnih vnosov</span><span class="sxs-lookup"><span data-stu-id="cb864-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cb864-104">V prejšnjih različicah aplikacije Dynamics 365 Project Service Automation je bilo treba časovne vnose vnašati na tedenski ravni.</span><span class="sxs-lookup"><span data-stu-id="cb864-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="cb864-105">V različici 3 rešitve Project Service Automation se vnosi vnesejo vsakodnevno.</span><span class="sxs-lookup"><span data-stu-id="cb864-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="cb864-106">Po tem, ko ste ustvarili že nekaj časovnih vnosov, jih lahko množično ustvarite ali kopirate.</span><span class="sxs-lookup"><span data-stu-id="cb864-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="cb864-107">Ustvarjanje časovnega vnosa</span><span class="sxs-lookup"><span data-stu-id="cb864-107">Create a time entry</span></span>

<span data-ttu-id="cb864-108">Za ustvarjanje časovnega vnosa sledite tem korakom.</span><span class="sxs-lookup"><span data-stu-id="cb864-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="cb864-109">Na strani **Časovni vnosi** izberite možnost **Novo**.</span><span class="sxs-lookup"><span data-stu-id="cb864-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="cb864-110">V pogovorno okno **Hitro ustvarjanje: časovni vnos** vnesite trajanje časovnega vnosa v minutah, urah ali dnevih.</span><span class="sxs-lookup"><span data-stu-id="cb864-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="cb864-111">Trajanje morate vnesti v naslednji obliki: *x* minut, *x* ur ali *x* dni.</span><span class="sxs-lookup"><span data-stu-id="cb864-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="cb864-112">Ure in dneve lahko vnesete tudi kot decimalne vrednosti, na primer *x,x* ur ali *x,x* dni.</span><span class="sxs-lookup"><span data-stu-id="cb864-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="cb864-113">Izberite vrsto časovnega vnosa in projekt, za katerega vnašate časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="cb864-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="cb864-114">V polju **Projektno opravilo** poiščite opravilo za ta časovni vnos.</span><span class="sxs-lookup"><span data-stu-id="cb864-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cb864-115">Če ustvarjate časovni vnos za opravilo, ki ni dodeljeno uporabniku, v polju **Projektno opravilo** izberite gumb **Iskanje** , nato izberite **Spremeni pogled** in nato še **Vsa dejavna projektna opravila** , da se prikaže seznam vseh opravil.</span><span class="sxs-lookup"><span data-stu-id="cb864-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View** , and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="cb864-116">Vnesite opis, če je to potrebno, in nato izberite možnost **Shrani in zapri**.</span><span class="sxs-lookup"><span data-stu-id="cb864-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="cb864-117">Ko ste ustvarili in shranili časovni vnos, ga lahko uredite v mreži časovnega vnosa.</span><span class="sxs-lookup"><span data-stu-id="cb864-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="cb864-118">Mreža časovnega vnosa podpira dve obliki zapisa:</span><span class="sxs-lookup"><span data-stu-id="cb864-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="cb864-119">Časovne vnose lahko vnesete v obliki zapisa **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="cb864-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="cb864-120">Ta oblika zapisa se nato pretvori v ure in decimalne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="cb864-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="cb864-121">Ure in decimalne vrednosti lahko vnesete neposredno.</span><span class="sxs-lookup"><span data-stu-id="cb864-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="cb864-122">Upoštevajte, da decimalne vrednosti ene ure niso enake minutam.</span><span class="sxs-lookup"><span data-stu-id="cb864-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="cb864-123">To pomeni, da 1,5 ure predstavlja 1 uro in 30 minut.</span><span class="sxs-lookup"><span data-stu-id="cb864-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="cb864-124">Enako pravilo velja za decimalne vrednosti dneva.</span><span class="sxs-lookup"><span data-stu-id="cb864-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="cb864-125">En dan traja 24 ur, zato 0,5 dneva predstavlja 12 ur.</span><span class="sxs-lookup"><span data-stu-id="cb864-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="cb864-126">Množično ustvarjanje časovnih vnosov</span><span class="sxs-lookup"><span data-stu-id="cb864-126">Bulk create time entries</span></span>

<span data-ttu-id="cb864-127">Ko ustvarite nekaj časovnih vnosov, jih lahko kopirate in s tem množično ustvarite dodatne časovne vnose.</span><span class="sxs-lookup"><span data-stu-id="cb864-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="cb864-128">Na strani **Časovni vnosi** izberite možnost **Kopiraj teden**.</span><span class="sxs-lookup"><span data-stu-id="cb864-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="cb864-129">Določite datumski obseg za kopiranje časovnih vnosov v poljih **Začetni datum** in **Končni datum** v skupini polj **Od obdobja**.</span><span class="sxs-lookup"><span data-stu-id="cb864-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="cb864-130">Določite datum, za katerega želite ustvariti časovne vnose, v polju **Začetni datum** v skupini polj **Do obdobja**.</span><span class="sxs-lookup"><span data-stu-id="cb864-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="cb864-131">Izberite **Kopiraj** , če želite ustvariti kopijo časovnih vnosov, ki ustrezajo dnevu v tednu, ki je določen v skupini polj **Do obdobja**.</span><span class="sxs-lookup"><span data-stu-id="cb864-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="cb864-132">Časovni vnos za prejšnji ponedeljek bo na primer kopiran v ponedeljek za teden, ki je označen v skupini polj **Do obdobja**.</span><span class="sxs-lookup"><span data-stu-id="cb864-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="cb864-133">Uvažanje podatkov za časovne vnose</span><span class="sxs-lookup"><span data-stu-id="cb864-133">Import data for time entries</span></span>

<span data-ttu-id="cb864-134">Podatke lahko uvozite iz projektnih rezervacij in dodelitev.</span><span class="sxs-lookup"><span data-stu-id="cb864-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="cb864-135">Ko uvažate podatke, lahko določite datumski obseg rezervacij za uvoz in nato izberite točno tiste rezervacije, ki jih je treba ustvariti kot **Osnutke** časovnih vnosov.</span><span class="sxs-lookup"><span data-stu-id="cb864-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="cb864-136">Združevanje po, razvrščanje, iskanje in zmogljivosti filtriranja</span><span class="sxs-lookup"><span data-stu-id="cb864-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="cb864-137">Časovne vnose lahko združite in filtrirate po razsežnostih, ki so določene v stolpcih.</span><span class="sxs-lookup"><span data-stu-id="cb864-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="cb864-138">V polju **Združi po** izberite razsežnost, ki jo želite uporabiti za filtriranje časovnih vnosov.</span><span class="sxs-lookup"><span data-stu-id="cb864-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="cb864-139">Zapise časovnih vnosov lahko razvrstite v naraščajočem ali padajočem vrstnem redu, tako da kliknete puščico za razvrščanje v glavi stolpca.</span><span class="sxs-lookup"><span data-stu-id="cb864-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="cb864-140">Poleg tega lahko tudi prikažete ali skrijete vnose, tako da izberete gumb **Filter** v glavi stolpca, nato pa v polje **Iskanje** vnesete besedilo, ki ga je treba uporabiti za iskanje časovnih vnosov glede na ime projekta, projektno opravilo, časovni vnos ali vir.</span><span class="sxs-lookup"><span data-stu-id="cb864-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
