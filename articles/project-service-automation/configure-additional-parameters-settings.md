---
title: Konfiguracija nastavitev dodatnih parametrov
description: Navodila za konfiguracijo nastavitev dodatnih parametrov v rešitvi Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: de2fe830-4313-4711-b03b-76d56bf56cb6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: f3e110163088f8e3b78da9f273113d74775bf24c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755889"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="c9eca-103">Konfiguracija nastavitev dodatnih parametrov (rešitev Project Service)</span><span class="sxs-lookup"><span data-stu-id="c9eca-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c9eca-104">Ko ste konfigurirali elemente v prejšnjih temah, morate nastaviti še dodatne parametre projekta, ki jih boste uporabljali za svoje projekte.</span><span class="sxs-lookup"><span data-stu-id="c9eca-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="c9eca-105">Ob prvi namestitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ste ustvarili nastavitev parametrov, s katero ste najprej ustvarili vse zapise, ki so potrebni za delovanje [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="c9eca-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="c9eca-106">Zdaj je čas, da se vrnete nazaj in konfigurirate dodatna polja za te nastavitve.</span><span class="sxs-lookup"><span data-stu-id="c9eca-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="c9eca-107">Konfigurirati boste morali naslednje nastavitve:</span><span class="sxs-lookup"><span data-stu-id="c9eca-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="c9eca-108">Organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="c9eca-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="c9eca-109">Pogostost izdajanja računov</span><span class="sxs-lookup"><span data-stu-id="c9eca-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="c9eca-110">Predloga delovnih ur</span><span class="sxs-lookup"><span data-stu-id="c9eca-110">Work hours template</span></span>  
  
-   <span data-ttu-id="c9eca-111">Cenik</span><span class="sxs-lookup"><span data-stu-id="c9eca-111">Price list</span></span>  
 
<span data-ttu-id="c9eca-112">V tem koraku tudi navedite, katero vrsto dodeljevanja sredstev želite:</span><span class="sxs-lookup"><span data-stu-id="c9eca-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="c9eca-113">**Osrednji**.</span><span class="sxs-lookup"><span data-stu-id="c9eca-113">**Central**.</span></span> <span data-ttu-id="c9eca-114">Le upravitelji virov lahko projektom dodeljujejo vire.</span><span class="sxs-lookup"><span data-stu-id="c9eca-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="c9eca-115">**Hibridno**.</span><span class="sxs-lookup"><span data-stu-id="c9eca-115">**Hybrid**.</span></span> <span data-ttu-id="c9eca-116">Upravitelji virov, upravitelji projektov in upravitelji kupcev lahko projektom dodeljujejo vire.</span><span class="sxs-lookup"><span data-stu-id="c9eca-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="c9eca-117">Nastavitev parametra projekta:</span><span class="sxs-lookup"><span data-stu-id="c9eca-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="c9eca-118">Odprite **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="c9eca-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="c9eca-119">Kliknite nastavitev parametrov, ki jo želite konfigurirati (tisto, ki ste jo ustvarili, ko ste prvič namestili [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), ali pa kliknite **Novo**, če želite ustvariti novo nastavitev.</span><span class="sxs-lookup"><span data-stu-id="c9eca-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="c9eca-120">V območju **Splošno** nastavite vse možnosti za svoje parametre projekta.</span><span class="sxs-lookup"><span data-stu-id="c9eca-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="c9eca-121">Če želite dodati cenik, v območju **Cenik** kliknite **+**, da izberete cenik s spustnega seznama **Cenik parametra projekta**, in nato kliknite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="c9eca-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="c9eca-122">Kliknite gumb **Shrani** v spodnjem desnem kotu zaslona.</span><span class="sxs-lookup"><span data-stu-id="c9eca-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="c9eca-123">Zapis parametra projekta mora biti vzdrževan, da rešitev Project Service deluje pravilno.</span><span class="sxs-lookup"><span data-stu-id="c9eca-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="c9eca-124">Tega zapisa se ne sme izbrisati.</span><span class="sxs-lookup"><span data-stu-id="c9eca-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="c9eca-125">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="c9eca-125">See Also</span></span>  
 [<span data-ttu-id="c9eca-126">Nastavitev virov</span><span class="sxs-lookup"><span data-stu-id="c9eca-126">Set up resources</span></span>](../project-service/set-up-resources.md)
