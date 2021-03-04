---
title: Odpravljanje težav dela v mreži opravil
description: Ta tema zagotavlja informacije o odpravljanju težav, potrebne pri delu v mreži opravil.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031557"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="34824-103">Odpravljanje težav dela v mreži opravil</span><span class="sxs-lookup"><span data-stu-id="34824-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="34824-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="34824-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="34824-105">Ta tema opisuje, kako odpraviti težave, s katerimi se lahko srečate pri delu z upravljanjem stroškov.</span><span class="sxs-lookup"><span data-stu-id="34824-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="34824-106">Omogočanje piškotkov</span><span class="sxs-lookup"><span data-stu-id="34824-106">Enable cookies</span></span>

<span data-ttu-id="34824-107">Project Operations zahteva, da so omogočeni piškotki tretjih oseb, da se lahko upodobi strukturirana členitev dela.</span><span class="sxs-lookup"><span data-stu-id="34824-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="34824-108">Če piškotki tretjih oseb niso omogočeni, boste namesto, da bi videli opravila, videli prazno stran, ko izberete zavihek **Opravila** na strani **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="34824-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Prazen zavihek, ko piškotki tretjih oseb niso omogočeni](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="34824-110">Nadomestna rešitev</span><span class="sxs-lookup"><span data-stu-id="34824-110">Workaround</span></span>
<span data-ttu-id="34824-111">Za brskalnike Microsoft Edge ali Google Chrome naslednji postopki orisujejo, kako posodobiti nastavitve brskalnika, da se omogočijo piškotki tretjih oseb.</span><span class="sxs-lookup"><span data-stu-id="34824-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="34824-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="34824-112">Microsoft Edge</span></span>

1. <span data-ttu-id="34824-113">Odprite brskalnik Edge.</span><span class="sxs-lookup"><span data-stu-id="34824-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="34824-114">V desnem zgornjem kotu izberite **tri pike** (...) in nato izberite **Nastavitve**.</span><span class="sxs-lookup"><span data-stu-id="34824-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="34824-115">Pod možnostjo **Piškotki in dovoljenja za mesta** izberite **Piškotki in podatki o mestih**.</span><span class="sxs-lookup"><span data-stu-id="34824-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="34824-116">Izklopite **Blokiraj piškotke tretjih oseb**.</span><span class="sxs-lookup"><span data-stu-id="34824-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="34824-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="34824-117">Google Chrome</span></span>

1. <span data-ttu-id="34824-118">Odprite brskalnik Chrome.</span><span class="sxs-lookup"><span data-stu-id="34824-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="34824-119">V desnem zgornjem kotu izberite tri navpične pike in nato izberite **Nastavitve**.</span><span class="sxs-lookup"><span data-stu-id="34824-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="34824-120">Pod možnostjo **Zasebnost in varnost** izberite **Piškotki in drugi podatki mesta**.</span><span class="sxs-lookup"><span data-stu-id="34824-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="34824-121">Izberite možnost **Dovoli vse piškotke**.</span><span class="sxs-lookup"><span data-stu-id="34824-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="34824-122">Če blokirate piškotke tretjih oseb, bodo vsi piškotki in podatki mesta iz drugih mest blokirani, tudi če je mesto dovoljeno na seznamu izjem.</span><span class="sxs-lookup"><span data-stu-id="34824-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="34824-123">Končna točka PEX</span><span class="sxs-lookup"><span data-stu-id="34824-123">PEX Endpoint</span></span>

<span data-ttu-id="34824-124">Project Operations zahteva, da se parametri projekta sklicujejo na končno točko PEX.</span><span class="sxs-lookup"><span data-stu-id="34824-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="34824-125">Ta končna točka je potrebna za komunikacijo s storitvijo, uporabljeno za upodobitev strukturirane členitve dela.</span><span class="sxs-lookup"><span data-stu-id="34824-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="34824-126">Če parameter ni omogočen, se prikaže napaka »Parameter projekta ni veljaven«.</span><span class="sxs-lookup"><span data-stu-id="34824-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="34824-127">Nadomestna rešitev</span><span class="sxs-lookup"><span data-stu-id="34824-127">Workaround</span></span>
 ![Polje končne točke PEX na parametru projekta](media/projectparameter.png)

1. <span data-ttu-id="34824-129">Dodaj polje **Končna točka PEX** na stran **Projektni parametri**.</span><span class="sxs-lookup"><span data-stu-id="34824-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="34824-130">Posodobi polje z naslednjo vrednostjo: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="34824-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="34824-131">Odstranite polje s strani **Projektni parametri**.</span><span class="sxs-lookup"><span data-stu-id="34824-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="34824-132">Pravice za projekt za splet</span><span class="sxs-lookup"><span data-stu-id="34824-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="34824-133">Project Operations se zanaša na zunanjo storitev razporejanja.</span><span class="sxs-lookup"><span data-stu-id="34824-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="34824-134">Storitev zahteva, da ima uporabnik več vlog za branje in pisanje dodeljenih entitetam, povezanih s strukturirano členitvijo dela.</span><span class="sxs-lookup"><span data-stu-id="34824-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="34824-135">Te entitete vključujejo projektna opravila, dodelitve virov in odvisnosti opravil.</span><span class="sxs-lookup"><span data-stu-id="34824-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="34824-136">Če uporabnik ne more upodobiti strukturirane členitve dela, ko odpre zavihek **Opravila**, verjetno projekt za Project Operations ni bil omogočen.</span><span class="sxs-lookup"><span data-stu-id="34824-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="34824-137">Uporabnik lahko prejme bodisi napako varnostne vloge ali napako, povezano z zavrnitvijo dostopa.</span><span class="sxs-lookup"><span data-stu-id="34824-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="34824-138">Nadomestna rešitev</span><span class="sxs-lookup"><span data-stu-id="34824-138">Workaround</span></span>

1. <span data-ttu-id="34824-139">Pojdite na **Nastavitev > Varnost > Uporabniki > Uporabniki aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="34824-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Bralnik aplikacije](media/applicationuser.jpg)
   
2. <span data-ttu-id="34824-141">Dvokliknite zapis uporabnika aplikacije, da preverite naslednje:</span><span class="sxs-lookup"><span data-stu-id="34824-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="34824-142">Uporabnik ima dostop do projekta.</span><span class="sxs-lookup"><span data-stu-id="34824-142">The user has access to the project.</span></span> <span data-ttu-id="34824-143">To preverjanje se običajno opravi tako, da se zagotovi, da ima uporabnik varnostno vlogo **Vodja projektov**.</span><span class="sxs-lookup"><span data-stu-id="34824-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="34824-144">Uporabnik aplikacije Microsoft Project obstaja in je pravilno konfiguriran.</span><span class="sxs-lookup"><span data-stu-id="34824-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="34824-145">Če ta uporabnik ne obstaja, lahko ustvarite zapis novega uporabnika.</span><span class="sxs-lookup"><span data-stu-id="34824-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="34824-146">Izberite **Novi uporabniki**.</span><span class="sxs-lookup"><span data-stu-id="34824-146">Select **New Users**.</span></span> <span data-ttu-id="34824-147">Spremenite obrazec za vnos na **Uporabnik aplikacije**, nato pa dodajte **ID aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="34824-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Podrobnosti uporabnika aplikacije](media/applicationuserdetails.jpg)

4. <span data-ttu-id="34824-149">Prepričajte se, da je bila uporabniku dodeljena pravilna licenca in da je storitev omogočena v podrobnostih naročniških paketov licence.</span><span class="sxs-lookup"><span data-stu-id="34824-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="34824-150">Prepričajte se, da uporabnik lahko odpre project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="34824-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="34824-151">Prepričajte se, prek projektnih parametrov, da sistem kaže na pravilno projektno končno točko.</span><span class="sxs-lookup"><span data-stu-id="34824-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="34824-152">Prepričajte se, je ustvarjen uporabnik projektne aplikacije.</span><span class="sxs-lookup"><span data-stu-id="34824-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="34824-153">Uveljavite naslednje varnostne vloge za uporabnika:</span><span class="sxs-lookup"><span data-stu-id="34824-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="34824-154">Uporabnik storitve Dataverse</span><span class="sxs-lookup"><span data-stu-id="34824-154">Dataverse User</span></span>
  - <span data-ttu-id="34824-155">Sistem Project Operations</span><span class="sxs-lookup"><span data-stu-id="34824-155">Project Operations System</span></span>
  - <span data-ttu-id="34824-156">Sistem projekta</span><span class="sxs-lookup"><span data-stu-id="34824-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="34824-157">Napaka pri posodabljanju strukturirane členitve dela</span><span class="sxs-lookup"><span data-stu-id="34824-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="34824-158">Ko se izvede ena ali več posodobitev strukturirane členitve dela, spremembe nazadnje niso uspešne in se ne shranijo.</span><span class="sxs-lookup"><span data-stu-id="34824-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="34824-159">Pride do napake v mreži razporeda s sporočilom »Nedavnih sprememb, ki ste jih izvedli, ni bilo mogoče shraniti«.</span><span class="sxs-lookup"><span data-stu-id="34824-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="34824-160">Nadomestna rešitev</span><span class="sxs-lookup"><span data-stu-id="34824-160">Workaround</span></span>

1. <span data-ttu-id="34824-161">Prepričajte se, da je bila uporabniku dodeljena pravilna licenca in da je storitev omogočena v podrobnostih naročniških paketov licence.</span><span class="sxs-lookup"><span data-stu-id="34824-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="34824-162">Prepričajte se, da uporabnik lahko odpre project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="34824-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="34824-163">Prepričajte se, da sistem kaže na pravilno projektno končno točko.</span><span class="sxs-lookup"><span data-stu-id="34824-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="34824-164">Prepričajte se, je bil ustvarjen uporabnik projektne aplikacije.</span><span class="sxs-lookup"><span data-stu-id="34824-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="34824-165">Uveljavite naslednje varnostne vloge za uporabnika:</span><span class="sxs-lookup"><span data-stu-id="34824-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="34824-166">Uporabnik storitve Dataverse ali osnovni uporabnik</span><span class="sxs-lookup"><span data-stu-id="34824-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="34824-167">Sistem Project Operations</span><span class="sxs-lookup"><span data-stu-id="34824-167">Project Operations System</span></span>
  - <span data-ttu-id="34824-168">Sistem projekta</span><span class="sxs-lookup"><span data-stu-id="34824-168">Project System</span></span>
  - <span data-ttu-id="34824-169">Sistem dvojnega zapisovanja Project Operations (ta vloga je obvezna, če uvajate scenarije, ki temeljijo na virih/nezalogi v storitvi Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="34824-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
