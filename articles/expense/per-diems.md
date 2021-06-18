---
title: Dnevnice
description: Ta tema vsebuje informacije o pravilih za dnevnice, ki se uporabljajo pri upravljanju stroškov.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b1476bfc0386412762c30e5a00acaff65bfbe3c7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995281"
---
# <a name="per-diems"></a><span data-ttu-id="a682d-103">Dnevnice</span><span class="sxs-lookup"><span data-stu-id="a682d-103">Per diems</span></span>

<span data-ttu-id="a682d-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="a682d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="a682d-105">Dnevnica je dodatek, ki se izplača delavcu, ki dela na terenu.</span><span class="sxs-lookup"><span data-stu-id="a682d-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="a682d-106">V razdelku »Upravljanje stroškov« lahko ustvarite pravila za dnevnice za različne potovalne situacije.</span><span class="sxs-lookup"><span data-stu-id="a682d-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="a682d-107">Dnevnice lahko temeljijo na letnem času, kraju potovanja ali obojem.</span><span class="sxs-lookup"><span data-stu-id="a682d-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="a682d-108">Ko ustvarite pravilo za dnevnice, lahko določite, da se izbrani odstotek od dnevnice zadrži, če delavec prejme brezplačne obroke ali storitve.</span><span class="sxs-lookup"><span data-stu-id="a682d-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="a682d-109">Določite lahko tudi najmanjše in največje število ur, za katera lahko velja dnevnica za potovanje delavca.</span><span class="sxs-lookup"><span data-stu-id="a682d-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="a682d-110">Konfiguracija</span><span class="sxs-lookup"><span data-stu-id="a682d-110">Configuration</span></span> 

1. <span data-ttu-id="a682d-111">Če želite dodati lokacije dnevnic, odprite **Nastavi** > **Izračuni in kode** > **Dnevnice**.</span><span class="sxs-lookup"><span data-stu-id="a682d-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="a682d-112">Za vsako od zgoraj dodanih lokacij izberite vrednost dnevnice in valuto, ki velja med izbranim začetnim ter končnim datumom za hotel, prehrano in druge stroške.</span><span class="sxs-lookup"><span data-stu-id="a682d-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="a682d-113">Vrednosti dnevnic in valute konfigurirate tako, da odprete **Nastavi** > **Izračuni in kode** > **Dnevnice**.</span><span class="sxs-lookup"><span data-stu-id="a682d-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="a682d-114">Na strani **Dnevnice** konfigurirajte stopnje za vrednost dnevnic.</span><span class="sxs-lookup"><span data-stu-id="a682d-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="a682d-115">Stopnje vrednosti dnevnic vam omogočajo, da določite odstotek razdelitve dnevnic za stroške hotela, prehrane in druge stroške.</span><span class="sxs-lookup"><span data-stu-id="a682d-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="a682d-116">Če želite znižati odstotek za obrok za zajtrk, kosilo ali večerjo, posodobite polja na strani **Parametri upravljanja stroškov** na zavihku **Dnevnica**.</span><span class="sxs-lookup"><span data-stu-id="a682d-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="a682d-117">Pošiljanje stroškov z možnostjo dnevnic</span><span class="sxs-lookup"><span data-stu-id="a682d-117">Submit expenses using per diem</span></span>
<span data-ttu-id="a682d-118">Če želite poslati stroške z možnostjo dnevnic, uporabite kategorijo stroška **Dnevnica**, ko ustvarite poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="a682d-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="a682d-119">Vnesite **Začetni datum dnevnic**, **Končni datum dnevnic** in **Lokacija dnevnic**.</span><span class="sxs-lookup"><span data-stu-id="a682d-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="a682d-120">Znesek se izračuna na podlagi vrednosti dnevnic za izbrano lokacijo, znižanje za obrok pa na podlagi stopnje vrednosti dnevnic.</span><span class="sxs-lookup"><span data-stu-id="a682d-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]