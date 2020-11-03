---
title: Ustvarjanje cenika
description: Navodila za ustvarjanje cenika v rešitvi Project Service
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: bf75286fd1837e27a9b6053ccb21b60771ee197d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084792"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="0f1ed-103">Ustvarjanje cenika (rešitev Project Service)</span><span class="sxs-lookup"><span data-stu-id="0f1ed-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0f1ed-104">Ceniki zagotavljajo predlogo, ki jo upravitelji kupcev lahko uporabijo za ustvarjanje ponudb in projektov ter določanje stroškov projekta.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="0f1ed-105">Zagotavljajo vrstični seznam vlog in stroškov s pripadajočimi cenami, ki jih boste zaračunali.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="0f1ed-106">Ustvarite lahko več cenikov, da lahko tako vzdržujete ločene cenovne strukture za različne regije, v katerih prodajate izdelke, ali različne prodajne kanale.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="0f1ed-107">Priporočamo, da ustvarite vsaj en cenik za vsako valuto, v kateri nameravate strankam izdajati račune.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="0f1ed-108">Če želite ustvariti finančne ocene za delo, ki bo opravljeno, poskrbite, da ima vsak projekt osnovni cenik stroškov in prodajnih cen.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="0f1ed-109">Nastavite privzeti cenik stroškov in prodaje, ki se uporablja za vse projekte, ustvarjene v organizaciji.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="0f1ed-110">Ceniki temeljijo na vlogah in kategorijah stroškov, zato poskrbite, da že pred ustvarjanjem cenika konfigurirate vloge in kategorije stroškov, ki jih želite uporabiti pri ustvarjanju cenika.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="0f1ed-111">Odprite **Project Service > Ceniki**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="0f1ed-112">Kliknite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="0f1ed-113">V polju **Kontekst** izberite kategorijo cenika: **Stroški** , **Nakup** ali **Prodaja**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-113">In **Context** , select whether this price list is for **Cost** , **Purchase** , or **Sales**.</span></span>  
  
4.  <span data-ttu-id="0f1ed-114">V polje **Ime** vnesite ime cenika.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-114">In **Name** , enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="0f1ed-115">V polju **Valuta** izberite valuto, ki jo boste uporabljali za obračunavanje ali razčlenitev stroškov.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-115">In **Currency** , select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="0f1ed-116">V polju **Časovna enota** določite časovno obdobje, za katerega velja cena, npr. dan ali ura.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-116">In **Time Unit** , specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="0f1ed-117">Vnesite **Začetni datum** , **Končni datum** in **Opis**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-117">Fill in the **Start Date** , **End Date** , and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="0f1ed-118">Kliknite **Shrani** , da ustvarite zapis, ki ga nato lahko urejate.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="0f1ed-119">Če želite na cenik dodati ceno vloge, kliknite **+** v razdelku **Cene vlog**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="0f1ed-120">V podoknu **Cena vloge** vnesite podrobnosti in nato kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0f1ed-121">Po potrebi dodajate druge cene vlog.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="0f1ed-122">Ko končate, v spodnjem desnem kotu zaslona kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="0f1ed-123">Če želite na cenik dodati ceno kategorije stroška, kliknite **+** v razdelku **Cene kategorij**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="0f1ed-124">V podoknu **Cena kategorije transakcije** vnesite podrobnosti in nato kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0f1ed-125">Po potrebi dodajajte druge cene kategorij.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="0f1ed-126">Ko končate, v spodnjem desnem kotu zaslona kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="0f1ed-127">Če želite ceniku dodati elemente cenika, kliknite **+** v razdelku **Elementi cenika**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="0f1ed-128">V podoknu **Elementi cenika** vnesite podrobnosti in nato kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0f1ed-129">Po potrebi dodajate druge elemente cenika.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="0f1ed-130">Ko končate, v spodnjem desnem kotu zaslona kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="0f1ed-131">Če želite ceniku dodati odnose področja, kliknite **+** v razdelku **Odnosi področja**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="0f1ed-132">V oknu **Nova povezava** vnesite podrobnosti in nato kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0f1ed-133">Po potrebi dodajate druge odnose področja.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="0f1ed-134">Ko končate, v spodnjem desnem kotu zaslona kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="0f1ed-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0f1ed-135">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="0f1ed-135">See Also</span></span>  
 [<span data-ttu-id="0f1ed-136">Konfiguracija storitve Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0f1ed-136">Configure Project Service Automation</span></span>](../psa/configure.md)
