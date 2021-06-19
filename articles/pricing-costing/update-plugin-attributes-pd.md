---
title: Posodabljanje atributov vtičnikov z novimi cenovnimi razsežnostmi
description: Ta tema vsebuje informacije o posodabljanju atributov vtičnika za cenovne razsežnosti.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 54b87a993929edbf89ef48741ba0a06c6c42ec4e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004641"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="97b64-103">Posodabljanje atributov vtičnikov z novimi cenovnimi razsežnostmi</span><span class="sxs-lookup"><span data-stu-id="97b64-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="97b64-104">Ta tema vsebuje informacije o posodabljanju atributov vtičnika za cenovne razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="97b64-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="97b64-105">Ta tema se uporablja samo za funkcije ponudbe in pogodbe v storitvi Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="97b64-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="97b64-106">Zahteve</span><span class="sxs-lookup"><span data-stu-id="97b64-106">Prerequisites</span></span>
<span data-ttu-id="97b64-107">Preden dokončate korake v tej temi, morate izvesti postopke v naslednjih temah:</span><span class="sxs-lookup"><span data-stu-id="97b64-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="97b64-108">Ustvarjanje polj in entitet po meri</span><span class="sxs-lookup"><span data-stu-id="97b64-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="97b64-109">Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete </span><span class="sxs-lookup"><span data-stu-id="97b64-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="97b64-110">[Nastavitev polj po meri kot cenovnih razsežnosti](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="97b64-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="97b64-111">Če teh postopkov še niste izvedli, jih dokončajte in se vrnite na to temo.</span><span class="sxs-lookup"><span data-stu-id="97b64-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="97b64-112">Registracija vtičnika</span><span class="sxs-lookup"><span data-stu-id="97b64-112">Register a plug-in</span></span>
<span data-ttu-id="97b64-113">Ko se na strani **Vrstica ponudbe** ustvarijo podrobnosti vrstice ponudbe za projektno vrstico ponudbe, sistem ustvari dve vrstici ocene.</span><span class="sxs-lookup"><span data-stu-id="97b64-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="97b64-114">Ena vrstica je na strani stroškov ocene, druga vrstica pa na strani prodaje.</span><span class="sxs-lookup"><span data-stu-id="97b64-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="97b64-115">Enako velja za podrobnosti projektne pogodbe.</span><span class="sxs-lookup"><span data-stu-id="97b64-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="97b64-116">Ko spremenite količino ali polje na stroškovni strani, se ta sprememba razširi tudi na prodajno stran.</span><span class="sxs-lookup"><span data-stu-id="97b64-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="97b64-117">To je mogoče, ker vtičniki PreOperation na entitetah s podrobnostmi QuoteLineDetail in ContractLine povežejo določene atribute na strani stroškov s prodajno stranjo transakcije.</span><span class="sxs-lookup"><span data-stu-id="97b64-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="97b64-118">Če bi radi, da se spremembe vrednosti cenovnih razsežnosti na prodajni strani izvedejo tudi na strani stroškov, je treba po spremembi cenovnih razsežnosti naslednje vtičnike ponovno registrirati.</span><span class="sxs-lookup"><span data-stu-id="97b64-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="97b64-119">Spodaj so našteti vtičniki za posodobitev in ponovno registracijo:</span><span class="sxs-lookup"><span data-stu-id="97b64-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="97b64-120">PreOperationContractLineDetailUpdate – **Posodobitev msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="97b64-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="97b64-121">PreOperationQuoteLineDetailUpdate – **Posodobitev msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="97b64-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="97b64-122">Dokončajte naslednje korake za posodobitev in ponovno registracijo vtičnikov.</span><span class="sxs-lookup"><span data-stu-id="97b64-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="97b64-123">Odprite **PluginRegistrationTool** in se povežite s svojim okoljem Dataverse v storitvi Project Operations.</span><span class="sxs-lookup"><span data-stu-id="97b64-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="97b64-124">Izberite **Iskanje** in vnesite prvih nekaj črk vtičnika, ki ga želite posodobiti.</span><span class="sxs-lookup"><span data-stu-id="97b64-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="97b64-125">Ko najdete vtičnik, ga izberite in nato kliknite **Izberi v glavnem obrazcu**.</span><span class="sxs-lookup"><span data-stu-id="97b64-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="97b64-126">Izberite korak **Posodobitev msdyn_orderlinetransaction**, ga kliknite z desno tipko miške in izberite **Posodobi**.</span><span class="sxs-lookup"><span data-stu-id="97b64-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="97b64-127">V pogovornem oknu **Posodobitev** kliknite tri pike (**...**) v atributih za filtriranje.</span><span class="sxs-lookup"><span data-stu-id="97b64-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="97b64-128">Odprlo se bo okno atributov za filtriranje skupaj s seznamom vseh atributov v entiteti in cenovnih razsežnostih.</span><span class="sxs-lookup"><span data-stu-id="97b64-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="97b64-129">Izberite potrditvena polja za atribute cenovnih razsežnosti.</span><span class="sxs-lookup"><span data-stu-id="97b64-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="97b64-130">Kliknite **V redu**, da zaprete stran, nato izberite možnost **Posodobi korak**.</span><span class="sxs-lookup"><span data-stu-id="97b64-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="97b64-131">Ponovite korake od 2 do 7 za drugi vtičnik **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="97b64-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="97b64-132">Za ta vtičnik morate posodobiti korak **Posodobitev msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="97b64-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="97b64-133">Zaprite **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="97b64-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]