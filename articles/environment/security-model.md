---
title: Varnostni model
description: Ta tema vsebuje informacije o varnostnem modelu v aplikaciji Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8acaa86dec8ebca8f9850877d345e30be3e3a919
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951229"
---
# <a name="security-model"></a><span data-ttu-id="5ac5e-103">Varnostni model</span><span class="sxs-lookup"><span data-stu-id="5ac5e-103">Security Model</span></span>

<span data-ttu-id="5ac5e-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="5ac5e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5ac5e-105">Microsoft Dynamics 365 Project Operations vsebuje edinstven varnostni model, ki omogoča delovanje poslovnega varnostnega modela, ki sodeluje s skupinami v Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="5ac5e-106">Varnostne vloge</span><span class="sxs-lookup"><span data-stu-id="5ac5e-106">Security roles</span></span>
<span data-ttu-id="5ac5e-107">Prednostne zmogljivosti Project Operations vključujejo naslednje vloge:</span><span class="sxs-lookup"><span data-stu-id="5ac5e-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="5ac5e-108">Vloga</span><span class="sxs-lookup"><span data-stu-id="5ac5e-108">Role</span></span>                          | <span data-ttu-id="5ac5e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5ac5e-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="5ac5e-110">Scope</span><span class="sxs-lookup"><span data-stu-id="5ac5e-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="5ac5e-111">Upravitelj prakse</span><span class="sxs-lookup"><span data-stu-id="5ac5e-111">Practice manager</span></span>              | <span data-ttu-id="5ac5e-112">Podpira poročanje med projekti.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="5ac5e-113">Poslovna enota</span><span class="sxs-lookup"><span data-stu-id="5ac5e-113">Business unit</span></span>              |
| <span data-ttu-id="5ac5e-114">Odobritelj projekta</span><span class="sxs-lookup"><span data-stu-id="5ac5e-114">Project approver</span></span>              | <span data-ttu-id="5ac5e-115">Odobri čas in stroške projekta.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="5ac5e-116">Poslovna enota</span><span class="sxs-lookup"><span data-stu-id="5ac5e-116">Business unit</span></span> |
| <span data-ttu-id="5ac5e-117">Skrbnik plačevanja pri projektu</span><span class="sxs-lookup"><span data-stu-id="5ac5e-117">Project billing administrator</span></span> | <span data-ttu-id="5ac5e-118">Ustvari predlog računa.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="5ac5e-119">Poslovna enota</span><span class="sxs-lookup"><span data-stu-id="5ac5e-119">Business unit</span></span> |
| <span data-ttu-id="5ac5e-120">Vodja projektov</span><span class="sxs-lookup"><span data-stu-id="5ac5e-120">Project manager</span></span>               | <span data-ttu-id="5ac5e-121">Ustvari projektni načrt in pošlje zahteve za vire.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="5ac5e-122">Poslovna enota</span><span class="sxs-lookup"><span data-stu-id="5ac5e-122">Business unit</span></span> |
| <span data-ttu-id="5ac5e-123">Projektni vir</span><span class="sxs-lookup"><span data-stu-id="5ac5e-123">Project resource</span></span>              | <span data-ttu-id="5ac5e-124">Člani ekipe, ki jih je mogoče rezervirati, in čas poročanja.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="5ac5e-125">Poslovna enota</span><span class="sxs-lookup"><span data-stu-id="5ac5e-125">Business unit</span></span>|
| <span data-ttu-id="5ac5e-126">Upravitelj virov</span><span class="sxs-lookup"><span data-stu-id="5ac5e-126">Resource manager</span></span>              | <span data-ttu-id="5ac5e-127">Vse funkcije za upravljanje virov, kot je izpolnjevanje zahtev za vire in rezervacije, so ločene v podporo hibridne konfiguracije za vodjo projektov + upravitelja virov in enotne, centralizirane vloge upravitelja virov.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="5ac5e-128">Poslovna enota</span><span class="sxs-lookup"><span data-stu-id="5ac5e-128">Business unit</span></span> |


<span data-ttu-id="5ac5e-129">Microsoft Project za splet vključuje naslednje vloge:</span><span class="sxs-lookup"><span data-stu-id="5ac5e-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="5ac5e-130">Vloga</span><span class="sxs-lookup"><span data-stu-id="5ac5e-130">Role</span></span>           | <span data-ttu-id="5ac5e-131">Opis</span><span class="sxs-lookup"><span data-stu-id="5ac5e-131">Description</span></span>                                                                                                        | <span data-ttu-id="5ac5e-132">Scope</span><span class="sxs-lookup"><span data-stu-id="5ac5e-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="5ac5e-133">Uporabnik projekta</span><span class="sxs-lookup"><span data-stu-id="5ac5e-133">Project user</span></span>   | <span data-ttu-id="5ac5e-134">Sodelujoči uporabnik projekta, ki lahko ustvari lastne projekte in si ogleda vse projekte, ki so v skupni rabi z njimi.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="5ac5e-135">Uporabnik</span><span class="sxs-lookup"><span data-stu-id="5ac5e-135">User</span></span>   |
| <span data-ttu-id="5ac5e-136">Sistem projekta</span><span class="sxs-lookup"><span data-stu-id="5ac5e-136">Project system</span></span> | <span data-ttu-id="5ac5e-137">Vloga, uporabljena za kontekst aplikacije.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-137">Role used for application   context.</span></span> <span data-ttu-id="5ac5e-138">Stranke ne bi smele uporabljati te sistemske vloge.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="5ac5e-139">Globalno</span><span class="sxs-lookup"><span data-stu-id="5ac5e-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="5ac5e-140">Izvajanje varnosti</span><span class="sxs-lookup"><span data-stu-id="5ac5e-140">Security enforcement</span></span>
<span data-ttu-id="5ac5e-141">Dejanja, ki se izvajajo na ravni projekta, se izvajajo v kontekstu prijavljenega uporabnika.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="5ac5e-142">To pomeni, da mora uporabnik za ustvarjanje, odpiranje ali brisanje projekta imeti na voljo dostop do CDS.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="5ac5e-143">Dostop do CDS je mogoče odobriti prek katerega koli razpoložljivega mehanizma v platformi.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="5ac5e-144">Uporabnik z večjim obsegom lahko na primer dostopa do projekta, če je bilo izvedeno izrecno dejanje za skupno rabo projekta, ki uporabniku omogoča dostop.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="5ac5e-145">Pomembno je, da se to upošteva pri ustvarjanju projektov v Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="5ac5e-146">Sodelovanje sodobnih skupin s Project Operations</span><span class="sxs-lookup"><span data-stu-id="5ac5e-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="5ac5e-147">Project for the Web in Project Operations podpirata sodobne skupine za sodelovanje.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="5ac5e-148">Uporabniki, ki so dodani v projekt prek skupine, lahko urejajo projektni načrt.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="5ac5e-149">Project for the Web samodejno doda uporabnike v skupino po njihovi dodelitvi.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="5ac5e-150">Skupine omogočajo skupno uporabo dovoljenj za projekt in podporne artefakte.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="5ac5e-151">Naslednji diagram prikazuje dogodke in spremembe stanja, do katerih pride med postopkom dodelitve skupine.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="5ac5e-152">Project Operations ne ustvari skupine z implicitnim dejanjem, ampak samo z dejanskim pritiskom na Skupine.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="5ac5e-153">Iskanje članov skupine v pogovornem oknu **Upravljanje skupine** je omejeno na tiste, ki so nastavljeni kot del varnostne skupine okolja.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="5ac5e-154">Za več informacij glejte [Nadzor uporabniškega dostopa do okolij: varnostne skupine in licence](/power-platform/admin/control-user-access).</span><span class="sxs-lookup"><span data-stu-id="5ac5e-154">For more information, see [Control user access to environments: security groups and licenses](/power-platform/admin/control-user-access).</span></span>

![Skupinski način](./media/groupsmode.png)

1. <span data-ttu-id="5ac5e-156">Projekt je plod in last uporabnika, ki ga je ustvaril.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="5ac5e-157">Lastnik projekta je posodobljen v skladu z ekipo.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="5ac5e-158">Ekipa lastnika se preslika v navedeno ali ustvarjeno Skupino Office.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="5ac5e-159">Prvotni lastnik projekta je dodan v Skupino Office.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="5ac5e-160">Priporočilo za uvajanje</span><span class="sxs-lookup"><span data-stu-id="5ac5e-160">Deployment recommendation</span></span>
<span data-ttu-id="5ac5e-161">Z razvojem modela za sodelovanje v skupini Office bo dodana funkcionalnost, ki bo sčasoma zagotavljala podrobnejši nadzor.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="5ac5e-162">Stranke, ki danes uvajajo storitev Project Operations, spodbujamo, da se osredotočijo na tradicionalni varnostni model Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5ac5e-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="5ac5e-163">Za več informacij glejte [Varnost v Common Data Service](/power-platform/admin/wp-security).</span><span class="sxs-lookup"><span data-stu-id="5ac5e-163">For more information, see [Security in Common Data Service](/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="5ac5e-164">Varnost v storitvah Project Operations in Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="5ac5e-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="5ac5e-165">Storitev Project Operations vključuje naslednje vloge:</span><span class="sxs-lookup"><span data-stu-id="5ac5e-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="5ac5e-166">Vodja projektov</span><span class="sxs-lookup"><span data-stu-id="5ac5e-166">Project manager</span></span>
- <span data-ttu-id="5ac5e-167">Projektni računovodja</span><span class="sxs-lookup"><span data-stu-id="5ac5e-167">Project accountant</span></span>

<span data-ttu-id="5ac5e-168">Za več informacij o varnosti v storitvi Finance glejte [Varnost na podlagi vlog](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span><span class="sxs-lookup"><span data-stu-id="5ac5e-168">For more information about security in Finance, see [Role-based security](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]