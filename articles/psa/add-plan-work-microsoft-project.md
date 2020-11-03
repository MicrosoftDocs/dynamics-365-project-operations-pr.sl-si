---
title: Uporaba dodatka za rešitev Project Service za načrtovanje dela v programu Microsoft Project | MicrosoftDocs
description: V tej temi najdete informacije o dodajanju, konfiguriranju in uporabi dodatka Microsoft Project za Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084886"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="6ee94-103">Uporaba dodatka za rešitev Project Service Automation za načrtovanje dela v Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="6ee94-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="6ee94-104">omogoča lažje načrtovanje projektov, vključno z ocenami.</span><span class="sxs-lookup"><span data-stu-id="6ee94-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="6ee94-105">Delo lahko določite tako, da so stroški, zmogljivost in prodajna vrednost jasni, ko je predložen končni predlog.</span><span class="sxs-lookup"><span data-stu-id="6ee94-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="6ee94-106">Zdaj lahko namestite program [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] in začnete načrtovati v znanem okolju [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="6ee94-107">Uporabite zanesljive zmogljivosti načrtovanja in upravljanja programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in nato posodobite svoj načrt projekta v rešitvi Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6ee94-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="6ee94-108">Če želite uporabljati funkcijo upravljanja dokumentov SharePoint za shranjevanje datotek [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] za projekte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], mora vaš skrbnik za [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vklopiti funkcijo upravljanja dokumentov.</span><span class="sxs-lookup"><span data-stu-id="6ee94-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="6ee94-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] je združljiv le s programom [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="6ee94-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="6ee94-110">Prenos in namestitev dodatka</span><span class="sxs-lookup"><span data-stu-id="6ee94-110">Download and install the add-in</span></span>  
 <span data-ttu-id="6ee94-111">Pripravite svoje vpisne podatke za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="6ee94-112">Te podatke potrebujete, da se s programom [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] lahko povežete v rešitev [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="6ee94-113">Iz središča za prenose prenesite dodatek za podprto različico aplikacije Project Service, [V2. X](https://go.microsoft.com/fwlink/?linkid=828268) ali [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="6ee94-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="6ee94-114">Kliknite povezavo za prenos.</span><span class="sxs-lookup"><span data-stu-id="6ee94-114">Click the download link.</span></span>  

3.  <span data-ttu-id="6ee94-115">Ko je prenos končan, kliknite **Da** , da namestite dodatek.</span><span class="sxs-lookup"><span data-stu-id="6ee94-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="6ee94-116">Konfiguracija dodatka</span><span class="sxs-lookup"><span data-stu-id="6ee94-116">Configure the add-in</span></span>  

1. <span data-ttu-id="6ee94-117">Odprite [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in kliknite zavihek **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="6ee94-118">Kliknite **Poveži**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="6ee94-119">Vnesite podatke za vpis in nato kliknite **Vpis**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="6ee94-120">Zdaj lahko začnete uporabljati dodatek.</span><span class="sxs-lookup"><span data-stu-id="6ee94-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="6ee94-121">Branje iz predloge</span><span class="sxs-lookup"><span data-stu-id="6ee94-121">Read from a template</span></span>  
 <span data-ttu-id="6ee94-122">Berite iz predloge, ki ste jo ustvarili v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] in kopirali v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], ter začnite načrtovanje projektov.</span><span class="sxs-lookup"><span data-stu-id="6ee94-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="6ee94-123">[Ustvarjanje projektne predloge (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="6ee94-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="6ee94-124">Na zavihku **Project Service** kliknite **Branje** > **Projektna predloga rešitve Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="6ee94-125">Na seznamu izberite projektno predlogo in nato kliknite **Odpri**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="6ee94-126">Opravila, ki ste jih iz predloge kopirali v Projekt, so privzeto nastavljena kot ročno razporejena.</span><span class="sxs-lookup"><span data-stu-id="6ee94-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="6ee94-127">Dodeljevanje vlog rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] virom projekta</span><span class="sxs-lookup"><span data-stu-id="6ee94-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="6ee94-128">Odprite projekt in kliknite trak **Opravilo**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="6ee94-129">Kliknite meni **Ganttov grafikon** in nato izberite **List z viri**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="6ee94-130">Na listu z viri kliknite spustni meni **Vloga vira rešitve Project Service** in izberite vlogo rešitve Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6ee94-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="6ee94-131">Dodajanje virov za projekt</span><span class="sxs-lookup"><span data-stu-id="6ee94-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="6ee94-132">Na zavihku rešitve Project Service izberite vrstico in kliknite **Poišči vire**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="6ee94-133">Na zaslonu **Rezerviraj vir** izberite vir, ki ga želite uporabiti za projekt.</span><span class="sxs-lookup"><span data-stu-id="6ee94-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="6ee94-134">Kliknite **Rezerviraj** in nato **V redu**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="6ee94-135">Objava projekta</span><span class="sxs-lookup"><span data-stu-id="6ee94-135">Publish your project</span></span>  
<span data-ttu-id="6ee94-136">Ko končate z načrtovanjem projekta, sledi uvoz in objava projekta v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="6ee94-137">Projekt se bo uvozil v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="6ee94-138">Oblikovati je treba ceno in ustvariti ekipo.</span><span class="sxs-lookup"><span data-stu-id="6ee94-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="6ee94-139">Odprite projekt v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], da preverite, ali so ekipa, ocene za projekte in strukturirana členitev dela ustvarjene.</span><span class="sxs-lookup"><span data-stu-id="6ee94-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="6ee94-140">Spodnja tabela prikazuje, kje lahko najdete rezultate:</span><span class="sxs-lookup"><span data-stu-id="6ee94-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="6ee94-141">**Ganttov grafikon**</span><span class="sxs-lookup"><span data-stu-id="6ee94-141">**Gantt Chart**</span></span>   | <span data-ttu-id="6ee94-142">Uvoze na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zaslon **Strukturirane členitve dela**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="6ee94-143">**List z viri**</span><span class="sxs-lookup"><span data-stu-id="6ee94-143">**Resource Sheet**</span></span> |   <span data-ttu-id="6ee94-144">Uvozi na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zaslon **Člani projektne ekipe**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="6ee94-145">**Uporaba uporabe**</span><span class="sxs-lookup"><span data-stu-id="6ee94-145">**Use Usage**</span></span>    |    <span data-ttu-id="6ee94-146">Uvoze na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] zaslon **Ocene projekta**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="6ee94-147">**Uvoz in objava projekta**</span><span class="sxs-lookup"><span data-stu-id="6ee94-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="6ee94-148">Na zavihku **Project Service** kliknite **Objavi** > **Nov projekt rešitve Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="6ee94-149">V pogovornem oknu **Objavi v nov projekt rešitve Project Service** vnesite **Ime projekta** in izberite možnost **Stranka**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="6ee94-150">Po želji potrdite možnost **Poveži načrt projekta z rešitvijo Project Service Automation** , da datoteko za načrtovanje projekta povežete z rešitvijo Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6ee94-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="6ee94-151">Kliknite **Objavi**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-151">Click **Publish**.</span></span>  

   <span data-ttu-id="6ee94-152">Če povežete projektno datoteko z rešitvijo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], projektna datoteka postane glavna datoteka in strukturirano členitev dela v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nastavi samo za branje.</span><span class="sxs-lookup"><span data-stu-id="6ee94-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="6ee94-153">Če želite spremeniti načrt projekta, morate to storiti v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in spremembe objaviti kot posodobitve za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="6ee94-154">Urejanje projekta, ki je bil uvožen</span><span class="sxs-lookup"><span data-stu-id="6ee94-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="6ee94-155">Če želite spremeniti načrt projekta, ki je bil uvožen v rešitev [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], imate dve možnosti:</span><span class="sxs-lookup"><span data-stu-id="6ee94-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="6ee94-156">Odprite glavno datoteko in jo uredite v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="6ee94-157">Odstranite povezavo do datoteke in jo uredite neposredno v rešitvi Project Service.</span><span class="sxs-lookup"><span data-stu-id="6ee94-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="6ee94-158">Projekt, ki je bil prenesen iz programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], je privzeto zaklenjen in ga je mogoče urejati le v projektu.</span><span class="sxs-lookup"><span data-stu-id="6ee94-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="6ee94-159">Če želite urediti datoteko v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], mora biti povezava do datoteke odstranjena.</span><span class="sxs-lookup"><span data-stu-id="6ee94-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="6ee94-160">Urejanje v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="6ee94-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="6ee94-161">V glavnem meniju kliknite **Project Service** > **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="6ee94-162">Na seznamu projektov odprite tisti projekt, ki ste ga ustvarili v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="6ee94-163">Na traku kliknite **Odpri v programu MS Project**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="6ee94-164">V programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] se bo odprla glavna povezana datoteka.</span><span class="sxs-lookup"><span data-stu-id="6ee94-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="6ee94-165">Odstranjevanje povezave do datoteke in urejanje datoteke v storitvi [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="6ee94-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="6ee94-166">V glavnem meniju kliknite **Project Service** > **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="6ee94-167">Na seznamu projektov odprite tisti projekt, ki ste ga ustvarili v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="6ee94-168">Na traku kliknite **Odstrani povezavo s programom MS Project**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="6ee94-169">Nalaganje projektne datoteke v skupine storitve SharePoint ali Office</span><span class="sxs-lookup"><span data-stu-id="6ee94-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="6ee94-170">Projektno datoteko lahko naložite v SharePoint, kjer jo v možnosti »Povezani dokumenti« najdete za svoj projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="6ee94-171">Skrbnik mora nastaviti funkcijo upravljanja dokumentov SharePoint in jo vklopiti za entiteto »Projekt«.</span><span class="sxs-lookup"><span data-stu-id="6ee94-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="6ee94-172">Prav tako lahko svojo projektno datoteko naložite v [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], če imate nastavljene skupine storitve Office.</span><span class="sxs-lookup"><span data-stu-id="6ee94-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="6ee94-173">Nalaganje datoteke za SharePoint</span><span class="sxs-lookup"><span data-stu-id="6ee94-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="6ee94-174">V glavnem meniju kliknite **Project Service** > **Naloži**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="6ee94-175">Izberite **V projektne dokumente rešitve Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="6ee94-176">V pogovornem oknu **Omogoči odpiranje v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izberite **Da** ali **Ne**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="6ee94-177">Če kliknete **Da** , boste lahko izbrali gumb **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v rešitvi Project Service Automation ter tako zagnali [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in naložili projektno datoteko iz knjižnice dokumentov SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6ee94-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="6ee94-178">Če kliknete **Ne** , povezava za gumb **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ne bo delovala.</span><span class="sxs-lookup"><span data-stu-id="6ee94-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="6ee94-179">Datoteko [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] je mogoče najti v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v možnosti **Dokumenti** za določen projekt rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="6ee94-180">Nalaganje datoteke za skupine storitve Office</span><span class="sxs-lookup"><span data-stu-id="6ee94-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="6ee94-181">V glavnem meniju kliknite **Project Service** > **Naloži**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="6ee94-182">Izberite **V projektne dokumente rešitve Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="6ee94-183">V pogovornem oknu **Omogoči odpiranje v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izberite **Da** ali **Ne**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="6ee94-184">Če kliknete **Da** , boste lahko izbrali gumb **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v rešitvi Project Service Automation ter tako zagnali [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in naložili projektno datoteko iz knjižnice dokumentov SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6ee94-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="6ee94-185">Če kliknete **Ne** , povezava za gumb **Odpri v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** ne bo delovala.</span><span class="sxs-lookup"><span data-stu-id="6ee94-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="6ee94-186">Datoteko [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] je mogoče najti v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v možnosti **Dokumenti** za določen projekt rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="6ee94-187">Objava projekta kot predloge</span><span class="sxs-lookup"><span data-stu-id="6ee94-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="6ee94-188">Svoj projekt lahko shranite in ga znova uporabite tako, da ga shranite kot projektno predlogo v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="6ee94-189">Projektne predloge so načrti projektov, ki jih je mogoče znova uporabiti v rešitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="6ee94-190">[Ustvarjanje projektne predloge (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="6ee94-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="6ee94-191">Na zavihku **Project Service** kliknite **Objavi** > **Nova projektna predloga rešitve Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="6ee94-192">V pogovornem oknu **Objavi v nov projekt predloge rešitve Project Service** vnesite **Ime projektne predloge**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="6ee94-193">Po želji potrdite možnost **Poveži načrt projekta z rešitvijo Project Service Automation** , da datoteko projekta povežete z rešitvijo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="6ee94-194">Kliknite **Objavi**.</span><span class="sxs-lookup"><span data-stu-id="6ee94-194">Click **Publish**.</span></span>  

<span data-ttu-id="6ee94-195">Če povežete projektno datoteko z rešitvijo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], projektna datoteka postane glavna datoteka in strukturirano členitev dela v predlogi rešitve [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nastavi samo za branje.</span><span class="sxs-lookup"><span data-stu-id="6ee94-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="6ee94-196">Če želite spremeniti načrt projekta, morate to storiti v programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] in spremembe objaviti kot posodobitve za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6ee94-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="6ee94-197">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="6ee94-197">See Also</span></span>  
 [<span data-ttu-id="6ee94-198">Priročnik za vodje projektov</span><span class="sxs-lookup"><span data-stu-id="6ee94-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
