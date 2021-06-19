---
title: Odstranjevanje projektne ocene
description: Ta tema vsebuje informacije o odstranjevanju projektne ocene, ko je ta končana.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a4ad06bef7ed66a626c6d2ad7ef01ba5b99d1c0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006936"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="6575c-103">Odstranjevanje projektne ocene</span><span class="sxs-lookup"><span data-stu-id="6575c-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6575c-104">Projektne ocene omogočajo finančni pregled za predvideno in načrtovano delo za projekt.</span><span class="sxs-lookup"><span data-stu-id="6575c-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="6575c-105">Če želite delati z ocenami za projekt, morate projekt priložiti projektni oceni.</span><span class="sxs-lookup"><span data-stu-id="6575c-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="6575c-106">Projektna ocena vedno temelji na obstoječem projektu, vendar se lahko več projektov nanaša na eno samo projektno oceno.</span><span class="sxs-lookup"><span data-stu-id="6575c-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="6575c-107">Projektnim ocenam je mogoče priložiti samo projekte s fiksno ceno in naložbene projekte, ki morajo pripadati isti projektni skupini kot projektna ocena.</span><span class="sxs-lookup"><span data-stu-id="6575c-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="6575c-108">Če želite odpraviti projektno ocena, mora biti ta popolna.</span><span class="sxs-lookup"><span data-stu-id="6575c-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="6575c-109">Spodnji koraki pojasnjujejo, kako odpraviti oceno.</span><span class="sxs-lookup"><span data-stu-id="6575c-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="6575c-110">Odprite **Vodenje projekta in računovodstvo** > **Vsi projekti** in odprite projekt.</span><span class="sxs-lookup"><span data-stu-id="6575c-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="6575c-111">V zavihku **Upravljanje** izberite **Ocene** in na strani **Oceni** izberite **Odpravi**.</span><span class="sxs-lookup"><span data-stu-id="6575c-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="6575c-112">Na strani **Odpravi oceno** v zavihku **Splošno** nastavite naslednje možnosti:</span><span class="sxs-lookup"><span data-stu-id="6575c-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="6575c-113">**Koda obdobja**: izberite kodo obdobja, da izberete ustrezne projektne ocene.</span><span class="sxs-lookup"><span data-stu-id="6575c-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="6575c-114">**Predvideni datum**: izberite ustrezen predvideni datum za odstranjevanje.</span><span class="sxs-lookup"><span data-stu-id="6575c-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="6575c-115">**Odstranjevanje z opozorili WIP**: izberite to možnost, da omogočite obveščanje, ko bo odstranjena ocena, ki je povezana z delom v teku (WIP).</span><span class="sxs-lookup"><span data-stu-id="6575c-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="6575c-116">Če ta možnost ni omogočena, se odpravljanje ne bo nadaljevalo, če obstajajo kakršne koli neocenjene transakcije.</span><span class="sxs-lookup"><span data-stu-id="6575c-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="6575c-117">Ta možnost je na voljo samo, če se odpravljanje uporabi za projektno oceno.</span><span class="sxs-lookup"><span data-stu-id="6575c-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="6575c-118">Funkcija ni na voljo, če uporabljate periodično knjiženje.</span><span class="sxs-lookup"><span data-stu-id="6575c-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="6575c-119">Ta nastavitev začne delovati, če jo nastavite v zavihku **Ocena** na strani **Projektni parametri** v skupini polj **Dovoli odpravljanje v primeru neocenjenih transakcij**.</span><span class="sxs-lookup"><span data-stu-id="6575c-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="6575c-120">**Nastavi stopnjo na končano**: omogočite to možnost, da nastavite stopnjo projektne ocene na **Končano** po izvedbi odstranjevanja.</span><span class="sxs-lookup"><span data-stu-id="6575c-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="6575c-121">**Natisni seznam ocen**: izberite informacije, ki jih želite vključiti pri tiskanju seznama ocen.</span><span class="sxs-lookup"><span data-stu-id="6575c-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="6575c-122">**Pokaži dnevnik podatkov**: omogočite to možnost za prikaz dnevnika podatkov.</span><span class="sxs-lookup"><span data-stu-id="6575c-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="6575c-123">**Datum knjiženja**: izberite datum knjiženja ocene v glavni knjigi.</span><span class="sxs-lookup"><span data-stu-id="6575c-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="6575c-124">Izberite **V redu**.</span><span class="sxs-lookup"><span data-stu-id="6575c-124">Select **OK**.</span></span>
5. <span data-ttu-id="6575c-125">Po zaključku postopka odstranjevanja se odstranjena projektna ocena prikaže z negativno vrednostjo.</span><span class="sxs-lookup"><span data-stu-id="6575c-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="6575c-126">Če ocene niste nameravali odstraniti, jo lahko izberete in kliknete **Povrni postopek odstranjevanja**.</span><span class="sxs-lookup"><span data-stu-id="6575c-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]