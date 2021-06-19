---
title: Vrste obdobij
description: Ta tema vsebuje informacije o tem, kako nastaviti vrste obdobij za oceno prihodkov.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013506"
---
# <a name="period-types"></a><span data-ttu-id="b3960-103">Vrste obdobij</span><span class="sxs-lookup"><span data-stu-id="b3960-103">Period types</span></span>

<span data-ttu-id="b3960-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="b3960-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b3960-105">Vrsta obdobja določa, kako pogosto bodo izdelane ocene prihodkov od projekta.</span><span class="sxs-lookup"><span data-stu-id="b3960-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="b3960-106">Ta tema vsebuje informacije o tem, kako nastaviti vrste obdobij za oceno prihodkov.</span><span class="sxs-lookup"><span data-stu-id="b3960-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="b3960-107">Ustvarjanje vrst obdobij in delo z njimi</span><span class="sxs-lookup"><span data-stu-id="b3960-107">Create and work with period types</span></span>
<span data-ttu-id="b3960-108">Če želite ustvariti vrste obdobij in delati z njimi, izvedite naslednje korake:</span><span class="sxs-lookup"><span data-stu-id="b3960-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="b3960-109">V vašem okolju Dynamics 365 Finance odprite **Upravljanje projektov in računovodstvo** > **Nastavitev** > **Ocene** > **Vrste obdobij**.</span><span class="sxs-lookup"><span data-stu-id="b3960-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="b3960-110">Če želite ustvariti novo vrsto obdobja, izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="b3960-110">Select **New** to create new period type.</span></span> <span data-ttu-id="b3960-111">Vnesite Ime in opis.</span><span class="sxs-lookup"><span data-stu-id="b3960-111">Enter a name and description.</span></span>
3. <span data-ttu-id="b3960-112">V polje **Pogostost** vnesite vrednost:</span><span class="sxs-lookup"><span data-stu-id="b3960-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="b3960-113">Če izberete **Tedensko**, **Dvotedensko**, **Polmesečno**, **Mesečno**, **Dnevno**, **Četrtletno** ali **Letno**, bo koledar uporabljen za generiranje obdobij.</span><span class="sxs-lookup"><span data-stu-id="b3960-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="b3960-114">Če izberete **Knjigovodsko obdobje**, bodo za generiranje obdobij uporabljena knjigovodska obdobja iz glavne knjige.</span><span class="sxs-lookup"><span data-stu-id="b3960-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="b3960-115">Če izberete **Neomejeno**, lahko določite obdobja po meri.</span><span class="sxs-lookup"><span data-stu-id="b3960-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="b3960-116">Izberite zapis vrste obdobja in nato **Ustvari obdobja**, da ustvarite obdobja za izbrano vrsto obdobja.</span><span class="sxs-lookup"><span data-stu-id="b3960-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="b3960-117">Glede na izbrano pogostost obdobja boste morda imeli možnost določiti začetni datum ali število obdobij, ki jih želite ustvariti.</span><span class="sxs-lookup"><span data-stu-id="b3960-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="b3960-118">Izberite **Obdobja** za pregled ustvarjenih obdobij.</span><span class="sxs-lookup"><span data-stu-id="b3960-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]