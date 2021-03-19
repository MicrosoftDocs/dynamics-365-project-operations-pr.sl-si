---
title: Preglasitev prodajnih cenikov za projekte
description: Ta tema vsebuje informacije o ustvarjanju prodajnih cenikov po meri.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275558"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="3a0b6-103">Preglasitev prodajnih cenikov za projekte</span><span class="sxs-lookup"><span data-stu-id="3a0b6-103">Override project sales price lists</span></span>

<span data-ttu-id="3a0b6-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="3a0b6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="3a0b6-105">Ceniki za projekte za določeno stranko</span><span class="sxs-lookup"><span data-stu-id="3a0b6-105">Customer-specific project price lists</span></span>

<span data-ttu-id="3a0b6-106">Dogovore o cenah za posamezno stranko lahko nastavite kot cenike za projekt na zapisu kupca v aplikaciji Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="3a0b6-107">Če želite nastaviti cenik za projekt za posamezno stranko, se v območju **Prodaja** pomaknite do zapisa kupca.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="3a0b6-108">Odprite stran s seznamom **Kupci**.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="3a0b6-109">Poiščite in dvokliknite zapis stranke, da odprete stran s podrobnostmi **Kupec**.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="3a0b6-110">Na zavihku **Ceniki za projekte** izberite možnost **+ Nov cenik za projekt**.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="3a0b6-111">Na strani **Nov cenik za projekt** s spustnega menija izberite cenik.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="3a0b6-112">Samo ceniki, ki imajo kontekst nastavljen na **Prodaja** in ki imajo ujemajočo se valuto z valuto kupca.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="3a0b6-113">Poimenujte povezavo in nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="3a0b6-114">Ustvarjen je cenik za projekt za posamezno stranko.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="3a0b6-115">Ta cenik se uporablja za nastavljanje privzetih cen projekta za projektne ponudbe ali pogodbe, ustvarjene za to stranko, ko se datum izdelave ponudbe ali projektne pogodbe prekriva z datumom veljavnosti cenika.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="3a0b6-116">Cene po meri za projektne ponudbe</span><span class="sxs-lookup"><span data-stu-id="3a0b6-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="3a0b6-117">Na projektnih ponudbah lahko določite cene za projekte, ki se začnejo s privzetim standardnim cenikom, ki sledi privzetim nastavitvam stranke ali projektnih parametrov.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="3a0b6-118">Če na določeni ponudbi potrebujete cene po meri za delo, povezano s projektom, jih lahko dobite v povezani entiteti s ceniki projekta.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="3a0b6-119">Upoštevajte spodnje korake, če želite nastaviti cene za projekte za posamezne ponudbe.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="3a0b6-120">V projektni ponudbi odprite zavihek **Ceniki projektov**.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="3a0b6-121">V podmreži izberite **Ustvarjanje cen po meri**.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="3a0b6-122">Vsi ceniki projekta, ki so priloženi ponudbi, se kopirajo v nove cenike.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="3a0b6-123">Imena novih cenikov odražajo ime ponudbe z žigom datuma in časa, ko so bili ceniki ustvarjeni.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="3a0b6-124">Vsakega od teh cenikov lahko uporabite in posodobite cene dela (cena vloge) in cene stroškov (cena kategorije).</span><span class="sxs-lookup"><span data-stu-id="3a0b6-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="3a0b6-125">Te cene bodo veljale samo za to ponudbo za projekt.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="3a0b6-126">Ceniki v projektni pogodbi</span><span class="sxs-lookup"><span data-stu-id="3a0b6-126">Price lists on a project contract</span></span>

<span data-ttu-id="3a0b6-127">Pri projektni pogodbi so cene vedno privzete kot cenik po meri z imenom pogodbe in ustvarjenim žigom datuma in časa, ki je priložen imenu.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="3a0b6-128">To velja, ne glede na to, ali je bila pogodba ustvarjena, ko je bila ponudba pridobljena, ali če je bila pogodba ustvarjena povsem od začetka.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="3a0b6-129">Po potrebi lahko to povezavo s cenikom po meri odstranite in namesto tega s projektno pogodbo povežete standardni cenik.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="3a0b6-130">Ko standardni cenik povežete s ceniki za projekte na ponudbi ali pogodbi, bodo vse spremembe cen v ceniku vplivale na vse ponudbe in pogodbe, ki uporabljajo cenik.</span><span class="sxs-lookup"><span data-stu-id="3a0b6-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]