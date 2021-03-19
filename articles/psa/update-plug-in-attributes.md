---
title: Posodabljanje atributov vtičnikov za vključitev novih cenovnih razsežnosti
description: Ta tema vsebuje informacije o posodabljanju atributov vtičnika za cenovne razsežnosti.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281813"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="b5dd5-103">Posodabljanje atributov vtičnikov za vključitev novih cenovnih razsežnosti</span><span class="sxs-lookup"><span data-stu-id="b5dd5-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="b5dd5-104">Če ne uporabljate funkcij za oblikovanje ponudb in sklepanje pogodb v rešitvi Project Service Automation (PSA), lahko to temo preskočite.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="b5dd5-105">Predpostavljamo, da ste izvedli postopke v temah [Ustvarjanje polj in entitet po meri](create-custom-fields-entities.md), [Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete](field-references.md) in [Nastavitev polj po meri kot cenovnih razsežnosti](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="b5dd5-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="b5dd5-106">Če teh postopkov še niste izvedli, se vrnite nazaj in jih dokončajte, preden se vrnete na to temo.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="b5dd5-107">Ko ste ustvarili vrstico ponudbe na strani **Vrstica ponudbe** za vrstico ponudbe projekta, bo sistem v ozadju ustvaril dve vrstici ocen – eno za stroškovno stran ocene in eno za prodajno stran.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="b5dd5-108">Enako velja za podrobnosti projektne pogodbe.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="b5dd5-109">Ko spremenite količino ali polje na stroškovni strani, se ta sprememba razširi na prodajno stran.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="b5dd5-110">To omogočajo spodnji vtičniki, ki jih je treba ponovno registrirati po spremembi cenovnih razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="b5dd5-111">PreOperationContractLineDetailUpdate – Posodobitve **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="b5dd5-112">PreOperationQuoteLineDetailUpdate – Posodobitve **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="b5dd5-113">Naslednji koraki vam bodo pomagali pri postopku registracije vtičnikov.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="b5dd5-114">Odprite orodje **PluginRegistrationTool** in se povežite s spletnim primerkom.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="b5dd5-115">Kliknite **Iskanje** in poiščite vtičnik, ki ga želite posodobiti.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Posnetek zaslona drevesa za iskanje](media/PRT-1.png)

3. <span data-ttu-id="b5dd5-117">Ko najdete vtičnik, ga izberite in nato kliknite **Izberi v glavnem obrazcu**.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="b5dd5-118">Izberite korak vtičnika, ki ga želite posodobiti, ga kliknite z desno tipko miške in nato izberite **Posodobi**.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Posnetek zaslona vtičnika, ki ga želite posodobiti](media/PRT-2.png)
 
5. <span data-ttu-id="b5dd5-120">V oknu za posodobitev kliknite tri pike (**...**) v atributih za filtriranje.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Posnetek zaslona informacij o konfiguraciji za možnosti »Posodobi obstoječi korak«](media/PRT-3.png)
 
6. <span data-ttu-id="b5dd5-122">Izberite potrditvena polja z atributom za določanje cen.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-122">Select the pricing attribute check boxes.</span></span>

 ![Posnetek zaslona, ki prikazuje izbiro potrditvenega polja atributov za določanje cen](media/PRT-4.png)

7. <span data-ttu-id="b5dd5-124">Kliknite **V redu**, da zaprete stran, nato izberite možnost **Posodobi korak**.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Posnetek zaslona, ki prikazuje gumb »Posodobi korak«](media/PRT-5.png)
 
8. <span data-ttu-id="b5dd5-126">Ponovite ta postopek še za drugi vtičnik **PreOperationQuoteLineDetail – Posodobitev msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="b5dd5-127">Zaprite orodje za registracijo vtičnika.</span><span class="sxs-lookup"><span data-stu-id="b5dd5-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]