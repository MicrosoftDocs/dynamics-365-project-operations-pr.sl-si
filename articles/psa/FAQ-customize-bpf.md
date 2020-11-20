---
title: Kako prilagodim potek poslovnega procesa stopenj projekta?
description: Pregled prilagajanja poteka poslovnega procesa stopenj projekta.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: a999bbffff848db7a6349df380d9ed5e73c143ab
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125063"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="ca144-103">Kako prilagodim potek poslovnega procesa stopenj projekta?</span><span class="sxs-lookup"><span data-stu-id="ca144-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="ca144-104">V starejših različicah aplikacije Project Service obstaja znana omejitev, da se morajo imena stopenj v poteku poslovnega procesa stopenj projekta natančno ujemati s pričakovanimi angleškimi imeni (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="ca144-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="ca144-105">Sicer poslovna logika, ki temelji na angleških imenih stopenj, ne deluje po pričakovanjih.</span><span class="sxs-lookup"><span data-stu-id="ca144-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="ca144-106">Zato v obrazcu projekta niso na voljo znana dejanja, kot je **Preklopi proces** ali **Uredi proces**, prav tako pa se ne spodbuja prilagajanje poteka poslovnega procesa.</span><span class="sxs-lookup"><span data-stu-id="ca144-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="ca144-107">Ta omejitev je bila obravnavana v različici 2.4.5.48 in novejših različicah.</span><span class="sxs-lookup"><span data-stu-id="ca144-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="ca144-108">Ta članek ponuja predlagane rešitve, če morate prilagoditi privzeti potek poslovnega procesa za starejše različice.</span><span class="sxs-lookup"><span data-stu-id="ca144-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="ca144-109">Poslovna logika zahteva natančno ujemanje z angleškimi imeni stopenj</span><span class="sxs-lookup"><span data-stu-id="ca144-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="ca144-110">Potek poslovnega procesa stopenj projekta vključuje poslovno logiko, ki spodbuja naslednje načine delovanja v aplikaciji:</span><span class="sxs-lookup"><span data-stu-id="ca144-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="ca144-111">Ko je projekt povezan s ponudbo, koda nastavi potek poslovnega procesa na stopnjo **Quote**.</span><span class="sxs-lookup"><span data-stu-id="ca144-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="ca144-112">Ko je projekt povezan s pogodbo, koda nastavi potek poslovnega procesa na stopnjo **Plan**.</span><span class="sxs-lookup"><span data-stu-id="ca144-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="ca144-113">Ko se potek poslovnega procesa pomakne na stopnjo **Close**, je zapis projekta deaktiviran.</span><span class="sxs-lookup"><span data-stu-id="ca144-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="ca144-114">Ko je projekt deaktiviran, sta obrazec projekta in strukturirana členitev dela (SČD) nastavljena samo za branje, rezervacije poimenovanih virov so izdane in vsi povezani ceniki so deaktivirani.</span><span class="sxs-lookup"><span data-stu-id="ca144-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="ca144-115">Ta poslovna logika temelji na angleških imenih za stopnje projekta.</span><span class="sxs-lookup"><span data-stu-id="ca144-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="ca144-116">Ta odvisnost od angleških imen stopenj je glavni razlog, zakaj se ne spodbuja prilagajanje poteka poslovnega procesa stopenj projekta in zakaj v entiteti projekta ne vidite skupnih dejanj poteka poslovnega procesa, kot je **Preklopi proces** ali **Uredi proces**.</span><span class="sxs-lookup"><span data-stu-id="ca144-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="ca144-117">Kaj se zgodi, če se imena stopenj ne ujemajo z angleškimi imeni?</span><span class="sxs-lookup"><span data-stu-id="ca144-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="ca144-118">V aplikaciji Project Service, različica 1.x na platformi 8.2, poslovna logika, ki nastavi pravo stopnjo za ponudbe ali pogodbe oziroma zapre projekt, preskoči, če se imena stopenj v poteku poslovnega procesa ne ujemajo natančno z angleškimi imeni stopenj.</span><span class="sxs-lookup"><span data-stu-id="ca144-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="ca144-119">Sporočila o napakah niso prikazana.</span><span class="sxs-lookup"><span data-stu-id="ca144-119">No error messages are displayed.</span></span> <span data-ttu-id="ca144-120">Zato se zdi, da lahko prilagodite potek poslovnega procesa stopenj projekta.</span><span class="sxs-lookup"><span data-stu-id="ca144-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="ca144-121">Vendar ne boste videli nobenega samodejnega procesa, ki deluje za ponudbe, pogodbe in zapiranje projekta.</span><span class="sxs-lookup"><span data-stu-id="ca144-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="ca144-122">V aplikaciji Project Service, različica 2.4.4.30 ali starejša različica na platformi 9.0, je prišlo do pomembne arhitekturne spremembe potekov poslovnih procesov, zaradi česar je bilo treba ponovno napisati poslovno logiko poteka poslovnega procesa.</span><span class="sxs-lookup"><span data-stu-id="ca144-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="ca144-123">Če se imena stopenj procesa ne ujemajo s pričakovanimi angleškimi imeni, posledično prejmete sporočilo o napaki.</span><span class="sxs-lookup"><span data-stu-id="ca144-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="ca144-124">Če torej želite prilagoditi potek poslovnega procesa stopenj projekta za entiteto projekta, lahko privzetemu poteku poslovnega procesa za entiteto projekta dodate le povsem nove stopnje, pri tem pa ohranite stopnje **Quote**, **Plan** in **Close** v takšni obliki, kot so.</span><span class="sxs-lookup"><span data-stu-id="ca144-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="ca144-125">Ta omejitev zagotavlja, da ne prejemate napak iz poslovne logike, ki pričakuje angleška imena stopenj v poteku poslovnega procesa.</span><span class="sxs-lookup"><span data-stu-id="ca144-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="ca144-126">V različici 2.4.5.48 ali novejših različicah je bila poslovna logika, ki je opisana v tem članku, odstranjena iz privzetega poteka poslovnega procesa za entiteto projekta.</span><span class="sxs-lookup"><span data-stu-id="ca144-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="ca144-127">Če aplikacijo nadgradite na to različico ali novejšo različico, boste lahko prilagodili privzeti potek poslovnega procesa ali ga zamenjali s svojim.</span><span class="sxs-lookup"><span data-stu-id="ca144-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="ca144-128">Rešitve za starejše različice</span><span class="sxs-lookup"><span data-stu-id="ca144-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="ca144-129">Če nadgradnja ne pride v poštev, lahko prilagodite potek poslovnega procesa stopenj projekta za entiteto projekta na enega od teh dveh načinov:</span><span class="sxs-lookup"><span data-stu-id="ca144-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="ca144-130">Privzeti konfiguraciji dodajte dodatne stopnje, pri tem pa ohranite angleška imena stopenj za **Quote**, **Plan** in **Close**.</span><span class="sxs-lookup"><span data-stu-id="ca144-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Posnetek zaslona dodajanja stopenj privzeti konfiguraciji](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="ca144-132">Ustvarite svoj potek poslovnega procesa in ga spremenite v primarni potek poslovnega procesa za entiteto projekta, ki omogoča poimenovanje stopenj s poljubnimi imeni.</span><span class="sxs-lookup"><span data-stu-id="ca144-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="ca144-133">Če želite uporabiti iste standardne stopnje projekta **Quote**, **Plan** in **Close**, pa morate izvesti nekatere prilagoditve, ki omogočajo uporabo imen stopenj po meri.</span><span class="sxs-lookup"><span data-stu-id="ca144-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="ca144-134">Bolj zapletena logika obstaja pri zapiranju projekta, ki ga lahko še vedno sprožite z deaktiviranjem zapisa projekta.</span><span class="sxs-lookup"><span data-stu-id="ca144-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Prilagajanje BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="ca144-136">Dodatni vidiki za aplikacijo Project Service, različica 2.4.4.30 ali starejša različica na platformi 9.0</span><span class="sxs-lookup"><span data-stu-id="ca144-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="ca144-137">V aplikaciji Project Service, različica 2.4.4.30 ali starejša različica na platformi 9.0, se polje **Ime stopnje** s potekom poslovnega procesa po meri v entiteti projekta, ki se uporablja v grafikonu **Projekt po stopnjah** in pogledih seznamov projektov, ne bo posodobilo, saj je povezano s privzetim potekom poslovnega procesa stopenj projekta.</span><span class="sxs-lookup"><span data-stu-id="ca144-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="ca144-138">To težavo lahko odpravite na naslednji način:</span><span class="sxs-lookup"><span data-stu-id="ca144-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="ca144-139">Dodajte polje po meri, da zajamete trenutno stopnjo poteka poslovnega procesa, ki se posodobi, ko se uporabnik pomika po poteku poslovnega procesa po meri.</span><span class="sxs-lookup"><span data-stu-id="ca144-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="ca144-140">Spremenite grafikon **Projekt po stopnjah**, da boste lahko uporabljali polje po meri, namesto privzete konfiguracije.</span><span class="sxs-lookup"><span data-stu-id="ca144-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="ca144-141">Koraki za ustvarjanje lastnega poteka poslovnega procesa za entiteto projekta</span><span class="sxs-lookup"><span data-stu-id="ca144-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="ca144-142">Če želite ustvariti lastni potek poslovnega procesa za entiteto projekta, naredite naslednje:</span><span class="sxs-lookup"><span data-stu-id="ca144-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="ca144-143">Odprite **Nastavitve** > **Središče procesov**.</span><span class="sxs-lookup"><span data-stu-id="ca144-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="ca144-144">Ne kopirajte poteka poslovnega procesa stopenj projekta, saj boste s tem kopirali tudi poslovno logiko za Project Service.</span><span class="sxs-lookup"><span data-stu-id="ca144-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Ustvari proces](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="ca144-146">Z oblikovalnikom procesov ustvarite poljubna imena stopenj.</span><span class="sxs-lookup"><span data-stu-id="ca144-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="ca144-147">Če želite enake funkcije, kot so funkcije privzetih stopenj za **Quote**, **Plan** in **Close**, jih boste morali ustvariti na podlagi vaših imen stopenj poteka poslovnega procesa po meri.</span><span class="sxs-lookup"><span data-stu-id="ca144-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Posnetek zaslona oblikovalnika procesov za prilagajanje BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="ca144-149">V oblikovalniku procesov kliknite **Potek procesa naročila**, da potek poslovnega procesa po meri spremenite v primarni potek poslovnega procesa za entiteto projekta tako, da ga premaknete na vrh seznama nad potek poslovnega procesa stopenj projekta.</span><span class="sxs-lookup"><span data-stu-id="ca144-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="ca144-150">Posnetek zaslona uporabe poteka procesa naročila</span><span class="sxs-lookup"><span data-stu-id="ca144-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="ca144-151">Naslednji koraki veljajo za aplikacijo Project Service, različica 2.4.4.30 ali starejša različica na platformi 9.0</span><span class="sxs-lookup"><span data-stu-id="ca144-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="ca144-152">Entiteti projekta dodajte novo polje po meri, da v svojem poteku poslovnega procesa po meri zajamete stopnje po meri.</span><span class="sxs-lookup"><span data-stu-id="ca144-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="ca144-153">Za posodobitev tega polja boste morali dodati poslovno logiko (vtičnik/potek dela), če je stopnja poteka poslovnega procesa po meri posodobljena.</span><span class="sxs-lookup"><span data-stu-id="ca144-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Posnetek zaslona prilagajanja entitete projekta](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="ca144-155">Spremenite grafikon **Projekt po stopnjah**, da boste lahko za stopnje uporabili novo polje po meri.</span><span class="sxs-lookup"><span data-stu-id="ca144-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Posnetek zaslona uporabe grafikona »Projekt po stopnjah«](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="ca144-157">Spremenite vse poglede za entiteto projekta, da boste za stopnje lahko vključili novo polje po meri.</span><span class="sxs-lookup"><span data-stu-id="ca144-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Posnetek zaslona spreminjanja pogledov v entiteti projekta](media/FAQ-Customize-BPF-8-720.png)

