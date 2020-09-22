---
title: Posodabljanje atributov vtičnikov za vključitev novih cenovnih razsežnosti
description: Ta tema vsebuje informacije o posodabljanju atributov vtičnika za cenovne razsežnosti.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755833"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="3ecc4-103">Posodabljanje atributov vtičnikov za vključitev novih cenovnih razsežnosti</span><span class="sxs-lookup"><span data-stu-id="3ecc4-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="3ecc4-104">Če ne uporabljate funkcij za oblikovanje ponudb in sklepanje pogodb v rešitvi Project Service Automation (PSA), lahko to temo preskočite.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="3ecc4-105">Predpostavljamo, da ste izvedli postopke v temah [Ustvarjanje polj in entitet po meri](create-custom-fields-entities.md), [Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete](field-references.md) in [Nastavitev polj po meri kot cenovnih razsežnosti](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="3ecc4-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="3ecc4-106">Če teh postopkov še niste izvedli, se vrnite nazaj in jih dokončajte, preden se vrnete na to temo.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="3ecc4-107">Ko ste ustvarili vrstico ponudbe na strani **Vrstica ponudbe** za vrstico ponudbe projekta, bo sistem v ozadju ustvaril dve vrstici ocen – eno za stroškovno stran ocene in eno za prodajno stran.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="3ecc4-108">Enako velja za podrobnosti projektne pogodbe.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="3ecc4-109">Ko spremenite količino ali polje na stroškovni strani, se ta sprememba razširi na prodajno stran.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="3ecc4-110">To omogočajo spodnji vtičniki, ki jih je treba ponovno registrirati po spremembi cenovnih razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="3ecc4-111">PreOperationContractLineDetailUpdate – Posodobitve **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="3ecc4-112">PreOperationQuoteLineDetailUpdate – Posodobitve **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="3ecc4-113">Naslednji koraki vam bodo pomagali pri postopku registracije vtičnikov.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="3ecc4-114">Odprite orodje **PluginRegistrationTool** in se povežite s spletnim primerkom.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="3ecc4-115">Kliknite **Iskanje** in poiščite vtičnik, ki ga želite posodobiti.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Posnetek zaslona drevesa za iskanje](media/PRT-1.png)

3. <span data-ttu-id="3ecc4-117">Ko najdete vtičnik, ga izberite in nato kliknite **Izberi v glavnem obrazcu**.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="3ecc4-118">Izberite korak vtičnika, ki ga želite posodobiti, ga kliknite z desno tipko miške in nato izberite **Posodobi**.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Posnetek zaslona vtičnika, ki ga želite posodobiti](media/PRT-2.png)
 
5. <span data-ttu-id="3ecc4-120">V oknu za posodobitev kliknite tri pike (**...**) v atributih za filtriranje.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Posnetek zaslona informacij o konfiguraciji za možnosti »Posodobi obstoječi korak«](media/PRT-3.png)
 
6. <span data-ttu-id="3ecc4-122">Izberite potrditvena polja z atributom za določanje cen.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-122">Select the pricing attribute check boxes.</span></span>

 ![Posnetek zaslona, ki prikazuje izbiro potrditvenega polja atributov za določanje cen](media/PRT-4.png)

7. <span data-ttu-id="3ecc4-124">Kliknite **V redu**, da zaprete stran, nato izberite možnost **Posodobi korak**.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Posnetek zaslona, ki prikazuje gumb »Posodobi korak«](media/PRT-5.png)
 
8. <span data-ttu-id="3ecc4-126">Ponovite ta postopek še za drugi vtičnik **PreOperationQuoteLineDetail – Posodobitev msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="3ecc4-127">Zaprite orodje za registracijo vtičnika.</span><span class="sxs-lookup"><span data-stu-id="3ecc4-127">Close the plug-in registration tool.</span></span>

