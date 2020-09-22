---
title: Vključevanje polj po meri za mobilno aplikacijo Microsoft Dynamics 365 Project Timesheet v sistemih iOS in Android
description: Ta tema ponuja skupne vzorce za uporabo razširitev za vključevanje polj po meri.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: 4564bbda-34ea-4647-a9bc-f6ef17b1038b
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 16c3b79dcaaf8c5c491587618256694f82f44753
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755756"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="95514-103">Vključevanje polj po meri za mobilno aplikacijo Microsoft Dynamics 365 Project Timesheet v sistemih iOS in Android</span><span class="sxs-lookup"><span data-stu-id="95514-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95514-104">Ta tema ponuja skupne vzorce za uporabo razširitev za vključevanje polj po meri.</span><span class="sxs-lookup"><span data-stu-id="95514-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="95514-105">Zajete so naslednje teme:</span><span class="sxs-lookup"><span data-stu-id="95514-105">The following topics are covered:</span></span>

- <span data-ttu-id="95514-106">Različne vrste podatkov, ki jih podpira ogrodje polja po meri</span><span class="sxs-lookup"><span data-stu-id="95514-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="95514-107">Prikaz polj samo za branje ali polj, ki jih je mogoče urejati, v vnosih časovnega lista in shranjevanje vrednosti, ki jih vnese uporabnik, nazaj v zbirko podatkov</span><span class="sxs-lookup"><span data-stu-id="95514-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="95514-108">Prikaz polj samo za branje v glavi časovnega lista</span><span class="sxs-lookup"><span data-stu-id="95514-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="95514-109">Vključevanje druge poslovne logike po meri za vnos privzetih vrednosti v polja in dodatno preverjanje veljavnosti</span><span class="sxs-lookup"><span data-stu-id="95514-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="95514-110">Občinstvo</span><span class="sxs-lookup"><span data-stu-id="95514-110">Audience</span></span>

<span data-ttu-id="95514-111">Ta tema je namenjena razvijalcem, ki vključujejo svoja polja po meri v mobilno aplikacijo Microsoft Dynamics 365 Project Timesheet, ki je na voljo za Apple iOS in Google Android.</span><span class="sxs-lookup"><span data-stu-id="95514-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="95514-112">Predpostavlja se, da bralci poznajo razvoj X++ in funkcije časovnega lista projekta.</span><span class="sxs-lookup"><span data-stu-id="95514-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="95514-113">Pogodba o podatkih – razred TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="95514-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="95514-114">Razred **TSTimesheetCustomField** je razred pogodbe o podatkih X++, ki predstavlja informacije o polju po meri za funkcije časovnega lista.</span><span class="sxs-lookup"><span data-stu-id="95514-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="95514-115">Seznami predmetov polja po meri se posredujejo v pogodbo o podatkih TSTimesheetDetails in TSTimesheetEntry za prikaz polj po meri v mobilni aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="95514-116">**TSTimesheetDetails** – pogodba o glavi časovnega lista.</span><span class="sxs-lookup"><span data-stu-id="95514-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="95514-117">**TSTimesheetEntry** – pogodba o transakciji časovnega lista.</span><span class="sxs-lookup"><span data-stu-id="95514-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="95514-118">Skupine teh predmetov, ki imajo enake informacije o projektu in vrednost **timesheetLineRecId**, predstavljajo vrstico.</span><span class="sxs-lookup"><span data-stu-id="95514-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="95514-119">fieldBaseType (vrste)</span><span class="sxs-lookup"><span data-stu-id="95514-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="95514-120">Lastnost **FieldBaseType** v predmetu **TsTimesheetCustom** določa vrsto polja, ki se prikaže v aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="95514-121">Podprte so spodnje vrednosti **Vrste**.</span><span class="sxs-lookup"><span data-stu-id="95514-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="95514-122">Vrednost »Vrste«</span><span class="sxs-lookup"><span data-stu-id="95514-122">Types value</span></span> | <span data-ttu-id="95514-123">Vrsta</span><span class="sxs-lookup"><span data-stu-id="95514-123">Type</span></span>              | <span data-ttu-id="95514-124">Opombe</span><span class="sxs-lookup"><span data-stu-id="95514-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="95514-125">0</span><span class="sxs-lookup"><span data-stu-id="95514-125">0</span></span>           | <span data-ttu-id="95514-126">Niz (in oštevilčenje)</span><span class="sxs-lookup"><span data-stu-id="95514-126">String (and Enum)</span></span> | <span data-ttu-id="95514-127">Polje se prikaže kot besedilno polje.</span><span class="sxs-lookup"><span data-stu-id="95514-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="95514-128">1</span><span class="sxs-lookup"><span data-stu-id="95514-128">1</span></span>           | <span data-ttu-id="95514-129">Celo število</span><span class="sxs-lookup"><span data-stu-id="95514-129">Integer</span></span>           | <span data-ttu-id="95514-130">Vrednost je prikazana kot število brez decimalnih mest.</span><span class="sxs-lookup"><span data-stu-id="95514-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="95514-131">2</span><span class="sxs-lookup"><span data-stu-id="95514-131">2</span></span>           | <span data-ttu-id="95514-132">Dejanska vrednost</span><span class="sxs-lookup"><span data-stu-id="95514-132">Real</span></span>              | <span data-ttu-id="95514-133">Vrednost je prikazana kot število z decimalnimi mesti.</span><span class="sxs-lookup"><span data-stu-id="95514-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="95514-134">Če želite v aplikaciji prikazati dejansko vrednost kot valuto, uporabite lastnost **fieldExtensedType**.</span><span class="sxs-lookup"><span data-stu-id="95514-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="95514-135">Uporabite lahko lastnost **numberOfDecimals** in nastavite število prikazanih decimalnih mest.</span><span class="sxs-lookup"><span data-stu-id="95514-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="95514-136">3</span><span class="sxs-lookup"><span data-stu-id="95514-136">3</span></span>           | <span data-ttu-id="95514-137">Datum</span><span class="sxs-lookup"><span data-stu-id="95514-137">Date</span></span>              | <span data-ttu-id="95514-138">Oblike zapisa datuma določa uporabnikova nastavitev **Oblika zapisa datuma, časa in številk**, ki je navedena pod možnostjo **Nastavitev jezika in države/regije** v razdelku **Uporabniške možnosti**.</span><span class="sxs-lookup"><span data-stu-id="95514-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="95514-139">4</span><span class="sxs-lookup"><span data-stu-id="95514-139">4</span></span>           | <span data-ttu-id="95514-140">Logična vrednost</span><span class="sxs-lookup"><span data-stu-id="95514-140">Boolean</span></span>           | |
| <span data-ttu-id="95514-141">15</span><span class="sxs-lookup"><span data-stu-id="95514-141">15</span></span>          | <span data-ttu-id="95514-142">GUID</span><span class="sxs-lookup"><span data-stu-id="95514-142">GUID</span></span>              | |
| <span data-ttu-id="95514-143">16</span><span class="sxs-lookup"><span data-stu-id="95514-143">16</span></span>          | <span data-ttu-id="95514-144">Int64</span><span class="sxs-lookup"><span data-stu-id="95514-144">Int64</span></span>             | |

- <span data-ttu-id="95514-145">Če lastnost **stringOptions** ni na voljo v predmetu **TSTimesheetCustomField**, je uporabniku na voljo polje s prostim besedilom.</span><span class="sxs-lookup"><span data-stu-id="95514-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="95514-146">Lastnost **stringLength** lahko uporabite za nastavitev največje dolžine niza, ki jo lahko vnesejo uporabniki.</span><span class="sxs-lookup"><span data-stu-id="95514-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="95514-147">Če je lastnost **stringOptions** na voljo v predmetu **TSTimesheetCustomField**, so ti elementi seznama edine vrednosti, ki jih lahko uporabniki izberejo z uporabo izbirnih gumbov.</span><span class="sxs-lookup"><span data-stu-id="95514-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="95514-148">V tem primeru lahko polje niza deluje kot vrednost oštevilčenja za vnos uporabnika.</span><span class="sxs-lookup"><span data-stu-id="95514-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="95514-149">Če želite shraniti vrednost v zbirko podatkov kot oštevilčenje, ročno preslikajte vrednost niza nazaj na vrednost oštevilčenja, preden jo shranite v zbirko podatkov z uporabo niza ukazov (za primer glejte razdelek »Uporaba niza ukazov v razredu TSTimesheetEntryService za shranjevanje vnosa v časovnem listu iz aplikacije nazaj v zbirko podatkov« v nadaljevanju te teme).</span><span class="sxs-lookup"><span data-stu-id="95514-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="95514-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="95514-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="95514-151">To lastnost lahko uporabite za oblikovanje dejanskih vrednosti kot valute.</span><span class="sxs-lookup"><span data-stu-id="95514-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="95514-152">Ta pristop se uporablja le, če je vrednost **fieldBaseType** vrste **Dejanska vrednost**.</span><span class="sxs-lookup"><span data-stu-id="95514-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="95514-153">**TSCustomFieldExtendedType:None** – oblikovanje ni uporabljeno.</span><span class="sxs-lookup"><span data-stu-id="95514-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="95514-154">**TSCustomFieldExtendedType::Currency** – vrednost je oblikovana kot valuta.</span><span class="sxs-lookup"><span data-stu-id="95514-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="95514-155">Ko je oblikovanje valute dejavno, lahko uporabite polje **stringValue** za posredovanje kode valute, ki jo želite prikazati v aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="95514-156">Vrednost je vrednost samo za branje.</span><span class="sxs-lookup"><span data-stu-id="95514-156">The value is a read-only value.</span></span>

    <span data-ttu-id="95514-157">Polje **realValue** vsebuje denarni znesek, ki ga je treba shraniti v zbirko podatkov.</span><span class="sxs-lookup"><span data-stu-id="95514-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="95514-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="95514-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="95514-159">S to lastnostjo lahko določite, kje v aplikaciji naj se prikaže polje po meri.</span><span class="sxs-lookup"><span data-stu-id="95514-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="95514-160">**TSCustomFieldSection::Header** – polje bo prikazano v razdelku **Prikaži več podrobnosti** v aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="95514-161">Ta polja so vedno samo za branje.</span><span class="sxs-lookup"><span data-stu-id="95514-161">These fields are always read-only.</span></span>
- <span data-ttu-id="95514-162">**TSCustomFieldSection::Line** – polje se bo prikazalo za vsemi vnaprej pripravljenimi polji vrstice v vnosih časovnega lista.</span><span class="sxs-lookup"><span data-stu-id="95514-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="95514-163">Ta polja so lahko polja, ki jih je mogoče urejati, ali polja samo za branje.</span><span class="sxs-lookup"><span data-stu-id="95514-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="95514-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="95514-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="95514-165">Ta lastnost prepozna polje, ko se vrednosti, navedene v aplikaciji, shranijo nazaj v zbirko podatkov.</span><span class="sxs-lookup"><span data-stu-id="95514-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="95514-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="95514-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="95514-167">Ta lastnost prepozna polje, ko se vrednosti, navedene v aplikaciji, shranijo nazaj v zbirko podatkov.</span><span class="sxs-lookup"><span data-stu-id="95514-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="95514-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="95514-168">isEditable (NoYes)</span></span>

<span data-ttu-id="95514-169">Nastavite to lastnost na **Da**, če želite, da uporabniki lahko urejajo polje v razdelku za vnos v časovni list.</span><span class="sxs-lookup"><span data-stu-id="95514-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="95514-170">Nastavite lastnost na **Ne**, če želite, da je polje samo za branje.</span><span class="sxs-lookup"><span data-stu-id="95514-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="95514-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="95514-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="95514-172">Nastavite to lastnost na **Da**, če želite, da je polje v razdelku za vnos v časovni list obvezno.</span><span class="sxs-lookup"><span data-stu-id="95514-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="95514-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="95514-173">label (str)</span></span>

<span data-ttu-id="95514-174">Ta lastnost določa oznako, ki je prikazana poleg polja v aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="95514-175">stringOptions (List of Strings)</span><span class="sxs-lookup"><span data-stu-id="95514-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="95514-176">Ta lastnost se uporablja samo, če je lastnost **fieldBaseType** nastavljena na vrsto **Niz**.</span><span class="sxs-lookup"><span data-stu-id="95514-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="95514-177">Če je nastavljena lastnost **stringOptions**, so vrednosti nizov, ki so na voljo za izbiro z izbirnimi gumbi, določene z nizi na seznamu.</span><span class="sxs-lookup"><span data-stu-id="95514-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="95514-178">Če ni nizov, je dovoljen vnos prostega besedila v polje niza (za primer glejte razdelek »Uporaba niza ukazov v razredu TSTimesheetEntryService za shranjevanje vnosa v časovnem listu iz aplikacije nazaj v zbirko podatkov« v nadaljevanju te teme).</span><span class="sxs-lookup"><span data-stu-id="95514-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="95514-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="95514-179">stringLength (int)</span></span>

<span data-ttu-id="95514-180">Ta lastnost določa največjo dolžino polja niza.</span><span class="sxs-lookup"><span data-stu-id="95514-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="95514-181">Uporablja se samo, če je lastnost **fieldBaseType** nastavljena na vrsto **Niz**.</span><span class="sxs-lookup"><span data-stu-id="95514-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="95514-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="95514-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="95514-183">Ta lastnost določa število decimalnih mest, ki so prikazana za dejansko polje.</span><span class="sxs-lookup"><span data-stu-id="95514-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="95514-184">Uporablja se samo, če je lastnost **fieldBaseType** nastavljena na vrsto **Dejanska vrednost**.</span><span class="sxs-lookup"><span data-stu-id="95514-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="95514-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="95514-185">orderSequence (int)</span></span>

<span data-ttu-id="95514-186">Ta lastnost upravlja vrstni red prikaza polj po meri v aplikaciji, če je določeno več kot eno polje po meri.</span><span class="sxs-lookup"><span data-stu-id="95514-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="95514-187">Najprej so prikazana polja z nižjimi številkami.</span><span class="sxs-lookup"><span data-stu-id="95514-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="95514-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="95514-188">booleanValue (boolean)</span></span>

<span data-ttu-id="95514-189">Pri poljih vrste **Logična vrednost** ta lastnost posreduje logično vrednost polja med strežnikom in aplikacijo.</span><span class="sxs-lookup"><span data-stu-id="95514-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="95514-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="95514-190">guidValue (guid)</span></span>

<span data-ttu-id="95514-191">Pri poljih vrste **GUID** ta lastnost posreduje vrednost globalnega enoličnega identifikatorja (GUID) za polje med strežnikom in aplikacijo.</span><span class="sxs-lookup"><span data-stu-id="95514-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="95514-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="95514-192">int64Value (int64)</span></span>

<span data-ttu-id="95514-193">Pri poljih vrste **Int64** ta lastnost posreduje vrednost »int64« polja med strežnikom in aplikacijo.</span><span class="sxs-lookup"><span data-stu-id="95514-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="95514-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="95514-194">intValue (int)</span></span>

<span data-ttu-id="95514-195">Pri poljih vrste **Int** ta lastnost posreduje vrednost »int« polja med strežnikom in aplikacijo.</span><span class="sxs-lookup"><span data-stu-id="95514-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="95514-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="95514-196">realValue (real)</span></span>

<span data-ttu-id="95514-197">Pri poljih vrste **Dejanska vrednost** ta lastnost posreduje dejansko vrednost polja med strežnikom in aplikacijo.</span><span class="sxs-lookup"><span data-stu-id="95514-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="95514-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="95514-198">stringValue (str)</span></span>

<span data-ttu-id="95514-199">Pri poljih vrste **Niz** ta lastnost posreduje vrednost niza za polje med strežnikom in aplikacijo.</span><span class="sxs-lookup"><span data-stu-id="95514-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="95514-200">Uporablja se tudi za polja vrste **Dejanska vrednost**, ki so oblikovana kot valuta.</span><span class="sxs-lookup"><span data-stu-id="95514-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="95514-201">Pri teh poljih se lastnost uporablja za posredovanje kode valute v aplikacijo.</span><span class="sxs-lookup"><span data-stu-id="95514-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="95514-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="95514-202">dateValue (date)</span></span>

<span data-ttu-id="95514-203">Pri poljih vrste **Datum** ta lastnost posreduje vrednost datuma za polje med strežnikom in aplikacijo.</span><span class="sxs-lookup"><span data-stu-id="95514-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="95514-204">Prikaz in shranjevanje polja po meri v razdelku za vnos v časovni list</span><span class="sxs-lookup"><span data-stu-id="95514-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="95514-205">Spodaj je posnetek zaslona iz mobilne aplikacije, ki prikazuje ustvarjanje vnosa v časovni list.</span><span class="sxs-lookup"><span data-stu-id="95514-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="95514-206">Prikazuje vnaprej pripravljena polja in polje po meri v razdelku »Časovni vnos«, imenovano »Preizkusni niz«, z že nastavljeno vrednostjo oštevilčenja »Druga možnost«.</span><span class="sxs-lookup"><span data-stu-id="95514-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Polje po meri »Preizkusni niz« v aplikaciji](media/timesheet-entry.jpg)



<span data-ttu-id="95514-208">Spodaj je posnetek zaslona iz mobilne aplikacije uporabnika, ki izbere eno od možnosti oštevilčevanja, ki je na voljo za polje po meri »Preizkusni niz«.</span><span class="sxs-lookup"><span data-stu-id="95514-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="95514-209">Možnosti, prikazani kot izbirna gumba, sta »Prva možnost« in »Druga možnost«.</span><span class="sxs-lookup"><span data-stu-id="95514-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="95514-210">Trenutno je izbrana druga možnost.</span><span class="sxs-lookup"><span data-stu-id="95514-210">The second option is currently selected.</span></span>

![Izbirna gumba za polje po meri »Preizkusni niz«](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="95514-212">Razširitev tabele TSTimesheetLine, tako da ima polje po meri</span><span class="sxs-lookup"><span data-stu-id="95514-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="95514-213">Običajno so podatki za polje po meri v razdelku za vnos v časovni list shranjeni v tabelo TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="95514-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="95514-214">Vendar lahko uporabite druge tabele, če je podatke mogoče pridobiti na podlagi zapisa TSTimesheetTrans, ki je na voljo, ali če ni določenega konteksta zapisa (če je na primer polje v parametrih projekta nastavljeno kot samo za branje).</span><span class="sxs-lookup"><span data-stu-id="95514-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="95514-215">Upoštevajte, da polja po meri ne potrebujejo rezervnih zapisov zbirke podatkov.</span><span class="sxs-lookup"><span data-stu-id="95514-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="95514-216">Lahko so dinamično ustvarjeni na podlagi logike X++.</span><span class="sxs-lookup"><span data-stu-id="95514-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="95514-217">Ta pristop je lahko uporaben v primerih samo za branje (za primer dinamično ustvarjenih vrednosti polja po meri glejte razdelek »Uporaba niza ukazov v razredu TSTimesheetDetails, metodi buildCustomFieldListForHeader za vnašanje podrobnosti časovnega lista«).</span><span class="sxs-lookup"><span data-stu-id="95514-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="95514-218">Spodaj je posnetek zaslona drevesa predmetov aplikacije iz aplikacije Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="95514-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="95514-219">Prikazuje razširitev tabele TSTimesheetLine s poljem TestLineString, ki je dodano kot polje po meri.</span><span class="sxs-lookup"><span data-stu-id="95514-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Niz vrstice](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="95514-221">Uporaba niza ukazov v metodi buildCustomFieldList razreda TSTimesheetSettings za prikaz polja v razdelku za vnos v časovni list</span><span class="sxs-lookup"><span data-stu-id="95514-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="95514-222">Ta koda upravlja nastavitve prikaza za polje v aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="95514-223">Upravlja na primer vrsto polja, oznako, ali je polje obvezno in v katerem razdelku se polje prikaže.</span><span class="sxs-lookup"><span data-stu-id="95514-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="95514-224">Spodnji primer prikazuje polje niza v časovnem vnosu.</span><span class="sxs-lookup"><span data-stu-id="95514-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="95514-225">To polje ima dve možnosti, **Prva možnost** in **Druga možnost**, ki sta na voljo prek izbirnih gumbov.</span><span class="sxs-lookup"><span data-stu-id="95514-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="95514-226">Polje v aplikaciji je povezano s poljem **TestLineString**, ki je dodano v tabelo TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="95514-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="95514-227">Oglejte si uporabo metode **TSTimesheetCustomField::newFromMetatdata()** za enostavnejšo inicializacijo lastnosti polja po meri: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** in **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="95514-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="95514-228">Te parametre lahko nastavite tudi ročno, če želite.</span><span class="sxs-lookup"><span data-stu-id="95514-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="95514-229">Uporaba niza ukazov v metodi buildCustomFieldListForEntry razreda TSTimesheetEntry za vnos vrednosti v vnosu v časovni list</span><span class="sxs-lookup"><span data-stu-id="95514-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="95514-230">Metoda **buildCustomFieldListForEntry** se uporablja za vnos vrednosti v vrsticah shranjenega časovnega lista v mobilni aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="95514-231">Kot parameter je potreben zapis TSTimesheetTrans.</span><span class="sxs-lookup"><span data-stu-id="95514-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="95514-232">Polja iz tega zapisa lahko uporabite za vnos vrednosti polja po meri v aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="95514-233">Uporaba niza ukazov v razredu TSTimesheetEntryService za shranjevanje vnosa v časovni list iz aplikacije nazaj v zbirko podatkov</span><span class="sxs-lookup"><span data-stu-id="95514-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="95514-234">Če želite polje po meri shraniti nazaj v zbirko podatkov pri običajni uporabi, morate razširiti več metod:</span><span class="sxs-lookup"><span data-stu-id="95514-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="95514-235">Metoda **timesheetLineNeedsUpdating** se uporablja za ugotavljanje, ali je uporabnik v aplikaciji spremenil zapis vrstice in ga je treba shraniti v zbirko podatkov.</span><span class="sxs-lookup"><span data-stu-id="95514-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="95514-236">Če učinkovitost delovanja ni zaskrbljujoča, lahko to metodo poenostavite, tako da vedno vrne vrednost **true**.</span><span class="sxs-lookup"><span data-stu-id="95514-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="95514-237">Metodi **populateTimesheetLineFromEntryDuringCreate** in **populateTimesheetLineFromEntryDuringUpdate** lahko razširite tako, da vnesejo vrednosti v zapis zbirke podatkov TSTimesheetLine iz zapisa pogodbe o podatkih TSTimesheetEntry, ki je na voljo.</span><span class="sxs-lookup"><span data-stu-id="95514-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="95514-238">V spodnjem primeru si oglejte, kako se preslikava med poljem zbirke podatkov in poljem za vnos ročno izvede prek kode X++.</span><span class="sxs-lookup"><span data-stu-id="95514-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="95514-239">Metoda **populateTimesheetWeekFromEntry** se lahko razširi tudi, če je za polje po meri, ki je preslikano v predmet **TSTimesheetEntry**, potrebno povratno zapisovanje v tabelo zbirke podatkov TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="95514-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="95514-240">V spodnjem primeru je vrednost **firstOption** ali **secondOption**, ki jo izbere uporabnik, shranjena v zbirko podatkov kot neobdelana vrednost niza.</span><span class="sxs-lookup"><span data-stu-id="95514-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="95514-241">Če je polje zbirke podatkov polje vrste **Oštevilčevanje**, lahko te vrednosti ročno preslikate v vrednost oštevilčevanja in nato shranite v polje oštevilčevanja v tabeli zbirke podatkov.</span><span class="sxs-lookup"><span data-stu-id="95514-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="95514-242">Prikaz polja po meri v razdelku glave časovnega lista</span><span class="sxs-lookup"><span data-stu-id="95514-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="95514-243">Spodaj je posnetek zaslona iz mobilne aplikacije, ki prikazuje časovni list.</span><span class="sxs-lookup"><span data-stu-id="95514-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="95514-244">V zgornjem desnem kotu je bil izbran gumb »Več informacij« za prikaz možnosti »Prikaži več podrobnosti«.</span><span class="sxs-lookup"><span data-stu-id="95514-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Ukaz »Prikaži več podrobnosti«](media/show-more.png)

<span data-ttu-id="95514-246">Spodaj je posnetek zaslona iz mobilne aplikacije, ki prikazuje razdelek »Več« na časovnem listu.</span><span class="sxs-lookup"><span data-stu-id="95514-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="95514-247">Polje po meri, imenovano »Stopnja izkoristka tega časovnega lista (izračunano polje po meri)«, je bilo dodano v odsek glave časovnega lista.</span><span class="sxs-lookup"><span data-stu-id="95514-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="95514-248">V polju po meri je nastavljena vrednost samo za branje »0,667«.</span><span class="sxs-lookup"><span data-stu-id="95514-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Razdelek »Več«](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="95514-250">Razširitev tabele TSTimesheetTable, tako da ima polje po meri</span><span class="sxs-lookup"><span data-stu-id="95514-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="95514-251">Običajno so podatki za polje po meri v odseku glave pridobljeni iz tabele TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="95514-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="95514-252">Vendar lahko uporabite druge tabele, če je podatke mogoče pridobiti na podlagi zapisa TSTimesheetTable, ki je na voljo, ali če ni določenega konteksta zapisa (če je na primer polje v parametrih projekta nastavljeno kot samo za branje).</span><span class="sxs-lookup"><span data-stu-id="95514-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="95514-253">Upoštevajte, da polja po meri ne potrebujejo rezervnih zapisov zbirke podatkov.</span><span class="sxs-lookup"><span data-stu-id="95514-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="95514-254">Lahko so dinamično ustvarjeni na podlagi logike X++.</span><span class="sxs-lookup"><span data-stu-id="95514-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="95514-255">Naslednji primer prikazuje ta pristop.</span><span class="sxs-lookup"><span data-stu-id="95514-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="95514-256">Polja v odseku glave so v aplikaciji vedno samo za branje.</span><span class="sxs-lookup"><span data-stu-id="95514-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="95514-257">Uporaba niza ukazov v metodi buildCustomFieldList razreda TSTimesheetSettings za prikaz polja v odseku glave</span><span class="sxs-lookup"><span data-stu-id="95514-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="95514-258">Ta koda upravlja nastavitve prikaza za polje v aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="95514-259">Upravlja na primer vrsto polja, oznako, ali je polje obvezno in v katerem razdelku se polje prikaže.</span><span class="sxs-lookup"><span data-stu-id="95514-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="95514-260">Naslednji primer prikazuje izračunano vrednost v odseku glave v aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="95514-261">Uporaba niza ukazov v metodi buildCustomFieldListForHeader razreda TSTimesheetDetails za vnos podrobnosti časovnega lista</span><span class="sxs-lookup"><span data-stu-id="95514-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="95514-262">Metoda **buildCustomFieldListForHeader** se uporablja za vnos podrobnosti glave časovnega lista v mobilni aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="95514-263">Kot parameter je potreben zapis TSTimesheetTable.</span><span class="sxs-lookup"><span data-stu-id="95514-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="95514-264">Polja iz tega zapisa lahko uporabite za vnos vrednosti polja po meri v aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="95514-265">Naslednji primer ne prebere nobene vrednosti iz zbirke podatkov.</span><span class="sxs-lookup"><span data-stu-id="95514-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="95514-266">Namesto tega uporablja logiko X++ za ustvarjanje izračunane vrednosti, ki je nato prikazana v aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="95514-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="95514-267">Druge možnosti konfiguracije/razširljivosti</span><span class="sxs-lookup"><span data-stu-id="95514-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="95514-268">Dodajanje dodatnega preverjanja veljavnosti za aplikacijo</span><span class="sxs-lookup"><span data-stu-id="95514-268">Adding additional validation for the app</span></span>

<span data-ttu-id="95514-269">Obstoječa logika za funkcije časovnega lista na ravni zbirke podatkov bo še vedno delovala po pričakovanjih.</span><span class="sxs-lookup"><span data-stu-id="95514-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="95514-270">Če želite prekiniti dokončanje operacij shranjevanja ali pošiljanja in prikazati določeno sporočilo o napaki, lahko prek razširitve z nizom ukazov v kodo dodate **throw error("message to user")**.</span><span class="sxs-lookup"><span data-stu-id="95514-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="95514-271">Tukaj so trije primeri uporabnih razširljivih metod:</span><span class="sxs-lookup"><span data-stu-id="95514-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="95514-272">Če metoda **validateWrite** v tabeli TSTimesheetLine vrne vrednost **false** med operacijo shranjevanja za vrstico časovnega lista, se v mobilni aplikaciji prikaže sporočilo o napaki.</span><span class="sxs-lookup"><span data-stu-id="95514-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="95514-273">Če metoda **validateSubmit** v tabeli TSTimesheetTable vrne vrednost **false** med pošiljanjem časovnega lista v aplikaciji, se uporabniku prikaže sporočilo o napaki.</span><span class="sxs-lookup"><span data-stu-id="95514-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="95514-274">Logika, ki izpolni polja (na primer **Lastnost vrstice**) med metodo **insert** v tabeli TSTimesheetLine, se bo še vedno izvajala.</span><span class="sxs-lookup"><span data-stu-id="95514-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="95514-275">Skrivanje in označevanje vnaprej pripravljenih polj kot samo za branje prek konfiguracije</span><span class="sxs-lookup"><span data-stu-id="95514-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="95514-276">Iz parametrov projekta lahko v mobilni aplikaciji označite vnaprej pripravljena polja samo za branje ali jih skrijete.</span><span class="sxs-lookup"><span data-stu-id="95514-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="95514-277">Nastavite možnosti v razdelku **Mobilni časovni listi** na zavihku **Časovni list** na strani **Vodenje projektov in računovodski parametri**.</span><span class="sxs-lookup"><span data-stu-id="95514-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projektni parametri](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="95514-279">Spreminjanje dejavnosti, ki so na voljo za izbiro prek razširitev</span><span class="sxs-lookup"><span data-stu-id="95514-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="95514-280">Dejavnosti, ki so na voljo za izbiro projekta, so vnesene prek metod **getActivitiesForProject()** in **getActivityQuery()** v razredu **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="95514-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="95514-281">Z nizom ukazov lahko to delovanje spremenite tako, da se ujema z vašim poslovnim scenarijem za dejavnosti, ki so na voljo za izbiro za določen projekt.</span><span class="sxs-lookup"><span data-stu-id="95514-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="95514-282">Vnos privzete kategorije projekta v vnosih v časovni list</span><span class="sxs-lookup"><span data-stu-id="95514-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="95514-283">Vnos privzete kategorije projekta v vnosih v časovni list poteka na treh ravneh.</span><span class="sxs-lookup"><span data-stu-id="95514-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="95514-284">Z nizom ukazov lahko razširite delovanje na posamezni ravni ali na vseh ravneh, da dosežete želeno delovanje.</span><span class="sxs-lookup"><span data-stu-id="95514-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="95514-285">Uporablja se naslednja hierarhija:</span><span class="sxs-lookup"><span data-stu-id="95514-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="95514-286">Aplikacija poskuša pridobiti privzeto kategorijo iz vira projekta.</span><span class="sxs-lookup"><span data-stu-id="95514-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="95514-287">Ta privzeta kategorija je nastavljena v metodah **getCurrentUserResource** in **getDelegatedResourcesForCurrentUser** v razredu **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="95514-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="95514-288">Če privzeta kategorija ni na voljo na ravni vira projekta, jo aplikacija poskuša pridobiti iz dejavnosti projekta.</span><span class="sxs-lookup"><span data-stu-id="95514-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="95514-289">Ta privzeta kategorija je nastavljena v metodi **getActivitiesForProject** v razredu **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="95514-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="95514-290">Če privzeta kategorija ni na voljo na ravni dejavnosti projekta, se pridobi iz parametrov projekta.</span><span class="sxs-lookup"><span data-stu-id="95514-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="95514-291">Ta privzeta kategorija je nastavljena v metodi **getProjectDetailsbyRule** v razredu **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="95514-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
