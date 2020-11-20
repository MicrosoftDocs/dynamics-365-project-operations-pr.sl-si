---
title: Zakaj se cena pri dejanski vrednosti »čas – cena« privzeto nastavi na nič?
description: 'Odpravljanje težav: cena pri dejanski vrednosti »čas – cena« se privzeto nastavi na 0.'
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 124719410f89dea506d43a1b64cb91c85d4f3968
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131403"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="75178-103">Zakaj se cena pri dejanski vrednosti »čas – cena« privzeto nastavi na nič?</span><span class="sxs-lookup"><span data-stu-id="75178-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="75178-104">To pogosto vprašanje se nanaša na dejansko vrednost, kjer je razred transakcije nastavljen na »Čas«, vrsta transakcije pa je »Cena«.</span><span class="sxs-lookup"><span data-stu-id="75178-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="75178-105">Naslednja tri preverjanja vam bodo v pomoč pri odpravljanju naslednje težave: cena pri dejanski vrednosti »čas – cena« se privzeto nastavi na 0.</span><span class="sxs-lookup"><span data-stu-id="75178-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="75178-106">1. preverjanje: opredelitev cenika z lastnimi cenami za projekt</span><span class="sxs-lookup"><span data-stu-id="75178-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="75178-107">V polju projekta z dejansko vrednostjo poiščite projekt in nato pojdite na stran projekta.</span><span class="sxs-lookup"><span data-stu-id="75178-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="75178-108">V polju kliknite povezavo do pogodbene enote.</span><span class="sxs-lookup"><span data-stu-id="75178-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="75178-109">Na strani pogodbene enote preverite, ali je v mreži cenikov z lastnimi cenami na voljo cenik za pogodbeno enoto.</span><span class="sxs-lookup"><span data-stu-id="75178-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="75178-110">Če obstaja več kot en cenik, ste osamili težavo.</span><span class="sxs-lookup"><span data-stu-id="75178-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="75178-111">Storitev Project Service podpira samo en cenik na organizacijsko enoto.</span><span class="sxs-lookup"><span data-stu-id="75178-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="75178-112">Odstranite vse cenike pri tej entiteti, dokler v mreži organizacijske enote s ceniki z lastnimi cenami ne bo priložen samo en cenik.</span><span class="sxs-lookup"><span data-stu-id="75178-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="75178-113">Če v organizacijski enoti ni priloženega cenika, si zabeležite valuto organizacijske enote.</span><span class="sxs-lookup"><span data-stu-id="75178-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="75178-114">Odprite Project Service in nato možnost »Parametri« ter odprite zavihek »Ceniki«. Preverite, ali so na voljo ceniki, pri katerih je kontekst nastavljen na »Cena« in kjer se valuta ujema z valuto organizacijske enote.</span><span class="sxs-lookup"><span data-stu-id="75178-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="75178-115">Če ni cenikov, ki bi ustrezali tem merilom, ste osamili težavo.</span><span class="sxs-lookup"><span data-stu-id="75178-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="75178-116">Prepričajte se, da imate vsaj en cenik, pri katerem je kontekst nastavljen na »Cena« in kjer se valuta ujema z valuto organizacijske enote.</span><span class="sxs-lookup"><span data-stu-id="75178-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="75178-117">Če obstaja več kot en cenik, ki ustreza tem merilom, dalje berite ta dokument, da izvedete več preverjanj.</span><span class="sxs-lookup"><span data-stu-id="75178-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="75178-118">2. preverjanje: ali je kateri od cenikov, opredeljenih zgoraj, veljaven za določeni datum dejanske vrednosti »čas – cena«?</span><span class="sxs-lookup"><span data-stu-id="75178-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="75178-119">Da bi storitev Project Service upoštevala cenik za nastavljanje privzete cene, bi moral ta cenik veljati za datum za dejansko vrednost »čas – cena«.</span><span class="sxs-lookup"><span data-stu-id="75178-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="75178-120">Preverite naslednje, da ugotovite, ali so ceniki, opredeljeni zgoraj, veljavni:</span><span class="sxs-lookup"><span data-stu-id="75178-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="75178-121">Prepričajte se, da sta začetni in končni datum na zavihku »Splošno« za priložene cenike izpolnjena.</span><span class="sxs-lookup"><span data-stu-id="75178-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="75178-122">Če začetni in končni datum na cenikih, opredeljenih zgoraj, nista izpolnjena, ste osamili težavo.</span><span class="sxs-lookup"><span data-stu-id="75178-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="75178-123">Zabeležite si polje z začetnim datumom za dejansko vrednost »čas – cena« in preverite, ali je kateri od opredeljenih cenikov veljaven za ta datum.</span><span class="sxs-lookup"><span data-stu-id="75178-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="75178-124">Datum dejanske vrednosti »čas – cena« bi moral biti na primer med začetnim datumom in končnim datumom na ceniku.</span><span class="sxs-lookup"><span data-stu-id="75178-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="75178-125">Če ni cenika, ki bi zajemal ta datum za dejansko vrednost »čas – cena«, ste osamili težavo.</span><span class="sxs-lookup"><span data-stu-id="75178-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="75178-126">Spremenite začetni in končni datum na ceniku in s tem zagotovite, da bo cenik zajemal datum za dejansko vrednost »čas – cena«.</span><span class="sxs-lookup"><span data-stu-id="75178-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="75178-127">Če obstaja več kot en cenik, ki zajema datum za dejansko vrednost »čas – cena«, ste osamili težavo.</span><span class="sxs-lookup"><span data-stu-id="75178-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="75178-128">To lahko popravite tako, da uredite začetni in končni datum na cenikih, da bo obstajal samo en cenik, ki bo zajemal datum dejanske vrednosti »čas – cena«.</span><span class="sxs-lookup"><span data-stu-id="75178-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="75178-129">Če obstaja samo en cenik, ki zajema ta datum dejanske vrednosti »čas – cena«, se premaknite na naslednje preverjanje v dokumentu.</span><span class="sxs-lookup"><span data-stu-id="75178-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="75178-130">Ko izvedete potrebne popravke, znova ustvarite vnos časa, ga odobrite in preverite, ali dejanska vrednost »čas – cena« prikazuje veljavno ceno.</span><span class="sxs-lookup"><span data-stu-id="75178-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="75178-131">3. preverjanje: ali obstaja cena v ceniku za cenovne razsežnosti pri dejanski vrednosti »čas – cena«?</span><span class="sxs-lookup"><span data-stu-id="75178-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="75178-132">Če ste uspešno zaključili 1. in 2. preverjanje, bi morali zdaj imeti samo en cenik, ki velja za datum dejanske vrednosti »čas – cena«.</span><span class="sxs-lookup"><span data-stu-id="75178-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="75178-133">Odprite ta cenik in pojdite na zavihek »Cene vlog«. Prepričajte se, da je v mreži vrstica za cenovne razsežnosti pri dejanski vrednosti »čas – cena«.</span><span class="sxs-lookup"><span data-stu-id="75178-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="75178-134">Če v mreži cen vlog za cenovne razsežnosti pri dejanski vrednosti »čas – cena« ni nobene vrstice, ste osamili težavo.</span><span class="sxs-lookup"><span data-stu-id="75178-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="75178-135">Ustvarite vrstico v mreži »Cene vlog« za cenovne razsežnosti pri dejanski vrednosti »čas – cena«.</span><span class="sxs-lookup"><span data-stu-id="75178-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="75178-136">Ko to naredite, znova ustvarite vnos časa, ga odobrite in preverite, ali dejanska vrednost »čas – cena« prikazuje veljavno ceno.</span><span class="sxs-lookup"><span data-stu-id="75178-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="75178-137">Če po treh opravljenih preverjanjih, opisanih zgoraj, še vedno ne vidite veljavne cene pri dejanski vrednosti »čas – cena«, vložite zahtevo za podporo.</span><span class="sxs-lookup"><span data-stu-id="75178-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



