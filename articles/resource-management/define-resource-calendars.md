---
title: Določanje koledarjev virov
description: Ta tema vsebuje informacije o tem, kako v aplikaciji Project Operations določiti koledarje delovnega časa za vire.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961948"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="2ec24-103">Določanje koledarjev virov</span><span class="sxs-lookup"><span data-stu-id="2ec24-103">Define resource calendars</span></span>

<span data-ttu-id="2ec24-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="2ec24-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2ec24-105">Vsak projektni vir, ki ga je mogoče rezervirati, mora imeti koledar delovnega časa, ki določa njegovo razpoložljivost.</span><span class="sxs-lookup"><span data-stu-id="2ec24-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="2ec24-106">Delovni čas za vir lahko določimo na dva načina:</span><span class="sxs-lookup"><span data-stu-id="2ec24-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="2ec24-107">Določanje pravil posameznega koledarja za vir</span><span class="sxs-lookup"><span data-stu-id="2ec24-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="2ec24-108">Uporaba obstoječe predloge koledarja za vir</span><span class="sxs-lookup"><span data-stu-id="2ec24-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="2ec24-109">Določanje delovnega časa za vir</span><span class="sxs-lookup"><span data-stu-id="2ec24-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="2ec24-110">Na meniju **Viri** izberite možnost **Viri**.</span><span class="sxs-lookup"><span data-stu-id="2ec24-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="2ec24-111">V pogledu mreže izberite ustrezni **razpoložljivi vir**.</span><span class="sxs-lookup"><span data-stu-id="2ec24-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="2ec24-112">Nastrani **Podrobnosti vira** izberite zavihek **Delovni čas**. Privzeto koledar razpoložljivih virov privzame delovni čas privzete predloge delovnega časa, ki je določena za organizacijo.</span><span class="sxs-lookup"><span data-stu-id="2ec24-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="2ec24-113">Če želite posodobiti delovni čas, z desno miškino tipko kliknite začetni datum predlaganega pravila koledarja, ki ga želite določiti.</span><span class="sxs-lookup"><span data-stu-id="2ec24-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="2ec24-114">Z menijem pravila koledarja določite pravilo koledarja za posamezen dan, preostanek niza ali celoten koledar.</span><span class="sxs-lookup"><span data-stu-id="2ec24-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="2ec24-115">Po izbiri možnosti lahko določite:</span><span class="sxs-lookup"><span data-stu-id="2ec24-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="2ec24-116">Dan v tednu, za katerega velja delovni čas</span><span class="sxs-lookup"><span data-stu-id="2ec24-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="2ec24-117">Delovni čas znotraj posameznega dneva</span><span class="sxs-lookup"><span data-stu-id="2ec24-117">The working times within each day.</span></span>
    - <span data-ttu-id="2ec24-118">Časovni pas koledarskega pravila</span><span class="sxs-lookup"><span data-stu-id="2ec24-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="2ec24-119">Če je primerno, lahko za pravilo določite tudi čas neobratovanja.</span><span class="sxs-lookup"><span data-stu-id="2ec24-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="2ec24-120">Uporaba predloge koledarja za vir</span><span class="sxs-lookup"><span data-stu-id="2ec24-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="2ec24-121">Na meniju **Viri** izberite možnost **Viri**.</span><span class="sxs-lookup"><span data-stu-id="2ec24-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="2ec24-122">V pogledu mreže izberite do 25 **razpoložljivih virov**, ki jih želite posodobiti.</span><span class="sxs-lookup"><span data-stu-id="2ec24-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="2ec24-123">Izberite možnost **Nastavitve koledarja** za prikaz seznama razpoložljivih predlog delovnega časa v pogovornem oknu.</span><span class="sxs-lookup"><span data-stu-id="2ec24-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="2ec24-124">Izberite predlogo, ki jo želite uporabiti, in nato izberite možnost **Uporabi**.</span><span class="sxs-lookup"><span data-stu-id="2ec24-124">Select the template you want to use, and then select **Apply**.</span></span>
