---
title: Upravljanje virov
description: Ta tema vsebuje informacije o upravljanju virov.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: b067f900fa49bba04536b49600dbe80a2167f707
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997846"
---
# <a name="manage-resources"></a><span data-ttu-id="032f4-103">Upravljanje virov</span><span class="sxs-lookup"><span data-stu-id="032f4-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="032f4-104">Dynamics 365 Project Service Automation vključuje nadzorno ploščo za upravljanje virov, ki zagotavlja vizualni pregled povpraševanja po virih in njihove uporabe v organizaciji.</span><span class="sxs-lookup"><span data-stu-id="032f4-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="032f4-105">Grafikone na tej nadzorni plošči lahko uporabite za upodobitev teh informacij:</span><span class="sxs-lookup"><span data-stu-id="032f4-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="032f4-106">**Povpraševanje po virih** – grafikon **Zahteve za dejavne vire** prikaže vire, ki so bili poslani.</span><span class="sxs-lookup"><span data-stu-id="032f4-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="032f4-107">Viri so združeni po vlogi ali projektu.</span><span class="sxs-lookup"><span data-stu-id="032f4-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="032f4-108">**Neposlano povpraševanje po virih** – grafikon **Povpraševanje po nedodeljenih virih** prikazuje vse zahteve za vir, ki niso bile poslane.</span><span class="sxs-lookup"><span data-stu-id="032f4-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="032f4-109">Upraviteljem virov pomaga, da si ogledajo povpraševanje, ki ni potrjeno in ga je mogoče poslati prek zahteve za vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="032f4-110">**Zaračunana uporaba za pretekli teden** – grafikon **Uporaba po vlogi** prikazuje odstotek dejanske zaračunane uporabe po vlogi v primerjavi s ciljno zaračunano uporabo po vlogi v organizaciji.</span><span class="sxs-lookup"><span data-stu-id="032f4-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="032f4-111">Če želite, da je grafikon **Uporaba po vlogi** na voljo, ustvarite posel, ki zažene potek dela UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="032f4-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="032f4-112">Ta ponavljajoči se posel se zažene vsakih sedem dni, da izračuna zaračunano uporabo za preteklih sedem dni.</span><span class="sxs-lookup"><span data-stu-id="032f4-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="032f4-113">Rezultati se združijo po vlogi.</span><span class="sxs-lookup"><span data-stu-id="032f4-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="032f4-114">Upravljanje članov projektne ekipe</span><span class="sxs-lookup"><span data-stu-id="032f4-114">Manage project team members</span></span>

<span data-ttu-id="032f4-115">Vodje projektov lahko za upravljanje virov v projektih uporabijo nadzorno ploščo za upravljanje virov.</span><span class="sxs-lookup"><span data-stu-id="032f4-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="032f4-116">Lahko na primer dodajo člana ekipe neposredno v projekt in rezervirajo člana ekipe, da izpolnijo zahteve za vir, ki jih je zajel splošni vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="032f4-117">Dodajanje člana ekipe neposredno v projekt</span><span class="sxs-lookup"><span data-stu-id="032f4-117">Add a team member directly to a project</span></span>

<span data-ttu-id="032f4-118">Če želite člana ekipe dodati neposredno v projekt, na strani **Projekti** na zavihku **Ekipa** izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="032f4-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="032f4-119">Prikaže se pogovorno okno **Hitro ustvarjanje: član projektne ekipe**.</span><span class="sxs-lookup"><span data-stu-id="032f4-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="032f4-120">V tem pogovornem oknu lahko izvedete ta opravila:</span><span class="sxs-lookup"><span data-stu-id="032f4-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="032f4-121">**Rezervirajte poimenovani vir** – v polju **Vir, ki ga je mogoče rezervirati** izberite ime vira.</span><span class="sxs-lookup"><span data-stu-id="032f4-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="032f4-122">Nato izberite vlogo, nastavite obdobje in izberite način dodelitve.</span><span class="sxs-lookup"><span data-stu-id="032f4-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="032f4-123">Poimenovani vir, ki ste ga izbrali, se doda projektu z uporabo izbranega načina dodelitve in koledarja virov.</span><span class="sxs-lookup"><span data-stu-id="032f4-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="032f4-124">**Dodajte splošni vir** – pustite polje **Vir, ki ga je mogoče rezervirati** prazno, in nato izberite vlogo, nastavite obdobje ter izberite želeni način dodeljevanja.</span><span class="sxs-lookup"><span data-stu-id="032f4-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="032f4-125">Splošni vir se ekipi doda kot označba mesta za hranjenje vzorca povpraševanja, ki se uporablja za rezervacijo poimenovanih virov v ekipi.</span><span class="sxs-lookup"><span data-stu-id="032f4-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="032f4-126">Zahteva je ustvarjena v skladu s koledarjem projekta.</span><span class="sxs-lookup"><span data-stu-id="032f4-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="032f4-127">**Ekipi dodajte poimenovani vir, ne da bi porabili zmogljivost vira** – v polju **Vir, ki ga je mogoče rezervirati** izberite vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="032f4-128">Nato izberite obdobje in **Brez** kot način dodelitve.</span><span class="sxs-lookup"><span data-stu-id="032f4-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="032f4-129">Vir se doda ekipi, vendar rezervacija ne porabi zmogljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="032f4-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="032f4-130">Rezervacija člana ekipe za izpolnjevanje zahtev za vir pri splošnem viru</span><span class="sxs-lookup"><span data-stu-id="032f4-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="032f4-131">V PSA lahko v projektni ekipi rezervirate splošni vir in določite vlogo, zahtevano zmogljivost in način porazdelitve zmogljivosti.</span><span class="sxs-lookup"><span data-stu-id="032f4-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="032f4-132">V zahtevi za vir lahko določite atribute, ki so povezani s splošnim virom.</span><span class="sxs-lookup"><span data-stu-id="032f4-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="032f4-133">Ti atributi vključujejo zahtevana znanja, želeno organizacijsko enoto in želene vire.</span><span class="sxs-lookup"><span data-stu-id="032f4-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="032f4-134">Če želite določiti zahtevana znanja v splošnem viru za razvijalca, sledite spodnjim korakom.</span><span class="sxs-lookup"><span data-stu-id="032f4-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="032f4-135">Na strani **Projekti** na zavihku **Ekipa** izberite **Novo**, da rezervirate splošni vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Splošni vir je rezerviran v ekipi](media/Resource-Management-image9.png)

2. <span data-ttu-id="032f4-137">V pogledu **Vsi člani ekipe** v stolpcu **Zahtevani pogoj za vir** izberite povezavo, da dodate zahtevana znanja za splošni vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Povezava do zahteve](media/Resource-Management-image10.png)

3. <span data-ttu-id="032f4-139">Na strani **Zahtevani pogoj za vir**, ki se prikaže, v mreži **Znanja** izberite tri pike (**...**) in nato **Dodaj novo lastnost zahteve**, da dodate zahtevana znanja za razvijalca.</span><span class="sxs-lookup"><span data-stu-id="032f4-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Ukaz »Dodaj novo lastnost zahteve«](media/Resource-Management-image11.png)

4. <span data-ttu-id="032f4-141">V pogovornem oknu **Hitro ustvarjanje: lastnosti zahteve**, ki se prikaže, v polju **Lastnost** izberite zahtevano znanje.</span><span class="sxs-lookup"><span data-stu-id="032f4-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="032f4-142">Nato v polju **Vrednost ocene** izberite stopnjo usposobljenosti za to znanje.</span><span class="sxs-lookup"><span data-stu-id="032f4-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="032f4-143">Na koncu v polju **Zahtevani pogoj za vir** nastavite zahtevane pogoje za izvorne vire iz organizacijskih enot ali celo poimenovanih virov.</span><span class="sxs-lookup"><span data-stu-id="032f4-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="032f4-144">Ko končate, izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="032f4-144">When you've finished, select **Save**.</span></span>

    ![Pogovorno okno »Hitro ustvarjanje: značilnost zahteve«](media/Resource-Management-image12.png)

5. <span data-ttu-id="032f4-146">Na strani **Zahtevani pogoj za vir** izberite **Rezerviraj**, da izpolnite zahtevani pogoj za vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Gumb »Rezerviraj« na strani »Zahtevani pogoj za vir«](media/Resource-Management-image13.png)

    <span data-ttu-id="032f4-148">Izberete lahko tudi splošni vir v mreži **Vsi člani ekipe** in nato **Rezerviraj.**</span><span class="sxs-lookup"><span data-stu-id="032f4-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Gumb »Rezerviraj« nad mrežo »Vsi člani ekipe«](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="032f4-150">V tem primeru je 40 zahtevanih ur, vendar ni dejanskih rezerviranih ur, ker splošni viri nimajo rezervacij.</span><span class="sxs-lookup"><span data-stu-id="032f4-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="032f4-151">Poleg tega ni dodeljenih ur, ker je bil splošni vir dodan neposredno ekipi.</span><span class="sxs-lookup"><span data-stu-id="032f4-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="032f4-152">Ni bil dodan prek dodelitve opravila.</span><span class="sxs-lookup"><span data-stu-id="032f4-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="032f4-153">Na strani **Pomočnik za razporejanje** lahko filtrirate razpoložljive vire po zahtevah, ki so določene v zahtevanem pogoju za vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="032f4-154">Viri so razvrščeni glede na parametre razvrščanja, ki so določeni na plošči razporeda.</span><span class="sxs-lookup"><span data-stu-id="032f4-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Stran »Pomočnik za razporejanje«](media/Resource-Management-image15.png)

    <span data-ttu-id="032f4-156">Tukaj je nekaj filtrov, ki se pogosto uporabljajo:</span><span class="sxs-lookup"><span data-stu-id="032f4-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="032f4-157">**Lastnosti skupaj z oceno** – filtrirajte po znanjih, potrdilih in drugih kakovostih virov poleg ocen usposobljenosti.</span><span class="sxs-lookup"><span data-stu-id="032f4-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="032f4-158">**Vloge** – filtrirajte po privzetih vlogah, ki so dodeljene virom, ki jih je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="032f4-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="032f4-159">**Organizacijske enote** – filtrirajte vire, ki jih je mogoče rezervirati, po organizacijskih enotah, ki so jim dodeljeni.</span><span class="sxs-lookup"><span data-stu-id="032f4-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="032f4-160">Če niste zadovoljni z rezultati prvotnega iskanja zahteve, lahko spremenite kriterije filtra.</span><span class="sxs-lookup"><span data-stu-id="032f4-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="032f4-161">Razširite podokno **Pogled filtra** na levi in nato izberite **Iskanje**, da poiščete dodatne vire.</span><span class="sxs-lookup"><span data-stu-id="032f4-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Podokno »Pogled filtra«](media/Resource-Management-image16.png)

7. <span data-ttu-id="032f4-163">Če želite spremeniti način razvrščanja rezultatov, izberite **Razvrsti**.</span><span class="sxs-lookup"><span data-stu-id="032f4-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Ukaz »Razvrsti«](media/Resource-Management-image17.png)

8. <span data-ttu-id="032f4-165">Izberite vire glede na zahtevo, ki je določena v pogoju, kot je navedeno na vrhu mreže.</span><span class="sxs-lookup"><span data-stu-id="032f4-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="032f4-166">Počistite lahko izbor celic v mreži in zmogljivost vira pustite odprto.</span><span class="sxs-lookup"><span data-stu-id="032f4-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="032f4-167">Samo en vir je lahko naenkrat izbran kot rezerviran.</span><span class="sxs-lookup"><span data-stu-id="032f4-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="032f4-168">Izberite **Rezerviraj**, da rezervirate izbrani vir in pustite ploščo razporeda odprto, tako da lahko izberete dodatne vire.</span><span class="sxs-lookup"><span data-stu-id="032f4-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="032f4-169">Lahko pa izberete tudi **Rezerviraj in zapri**, da rezervirate izbrani vir in zaprete ploščo razporeda.</span><span class="sxs-lookup"><span data-stu-id="032f4-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Vir za rezervacijo](media/Resource-Management-image19.png)

    <span data-ttu-id="032f4-171">Prejmete obvestilo o rezerviranih urah.</span><span class="sxs-lookup"><span data-stu-id="032f4-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="032f4-172">Kazalniki povpraševanja prikazujejo, v kolikšni meri je izpolnjena zahteva rezervacije in kakšen je preostanek.</span><span class="sxs-lookup"><span data-stu-id="032f4-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="032f4-173">Vidite lahko tudi, koliko zmogljivosti izbranega vira je porabljene.</span><span class="sxs-lookup"><span data-stu-id="032f4-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="032f4-174">Izberite **Razširi**, da prikažete več podrobnosti o rezervacijah virov.</span><span class="sxs-lookup"><span data-stu-id="032f4-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="032f4-175">Vrnite se v pogled **Vsi člani ekipe**.</span><span class="sxs-lookup"><span data-stu-id="032f4-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="032f4-176">V mreži lahko vidite, da je bil splošni vir zamenjan s poimenovanim virom in da je 40 ur navedenih kot rezerviranih za ta vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Posodobljena mreža v pogledu »Vsi člani skupine«](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="032f4-178">Dodeljene ure niso prikazane, ker so bile rezervirane neposredno v ekipi.</span><span class="sxs-lookup"><span data-stu-id="032f4-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="032f4-179">Niso bile rezervirane prek dodelitve opravila.</span><span class="sxs-lookup"><span data-stu-id="032f4-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="032f4-180">Dodeljevanje splošnih virov opravilom in ustvarjanje pogojev za vir</span><span class="sxs-lookup"><span data-stu-id="032f4-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="032f4-181">V PSA lahko ustvarite opravila in jim nato dodelite splošne vire.</span><span class="sxs-lookup"><span data-stu-id="032f4-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="032f4-182">Na ta način lahko povpraševanje po virih predstavljajo označbe mesta, medtem ko ocenjujete urnik in finančne številke.</span><span class="sxs-lookup"><span data-stu-id="032f4-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="032f4-183">Nato lahko ustvarite pogoje za vir za splošne vire in jih izpolnite.</span><span class="sxs-lookup"><span data-stu-id="032f4-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="032f4-184">Na strani **Projekti** na zavihku **Načrtovanje** izberite **Dodaj**, da ustvarite opravilo.</span><span class="sxs-lookup"><span data-stu-id="032f4-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Ustvarjeno je novo opravilo](media/Resource-Management-image21.png)

2. <span data-ttu-id="032f4-186">V polju **Viri** izberite simbol za **Izbirnik za vire**.</span><span class="sxs-lookup"><span data-stu-id="032f4-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="032f4-187">Prikaže se izbirnik za vire in prikaže obstoječe člane ekipe za projekt.</span><span class="sxs-lookup"><span data-stu-id="032f4-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Izbirnik za vire](media/Resource-Management-image22.png)

3. <span data-ttu-id="032f4-189">Vnesite ime novega splošnega vira in nato **Ustvari.**</span><span class="sxs-lookup"><span data-stu-id="032f4-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Vneseno je ime novega splošnega vira](media/Resource-Management-image23.png)

4. <span data-ttu-id="032f4-191">V pogovornem oknu **Hitro ustvarjanje: član projektne ekipe**, ki se prikaže, v polju **Vloga** izberite vlogo za splošni vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="032f4-192">V polju **Enota vira** izberite organizacijsko enoto za splošni vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="032f4-193">Nato izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="032f4-193">Then select **Save**.</span></span>

    ![Pogovorno okno »Hitro ustvarjanje: član projektne ekipe«](media/Resource-Management-image24.png)

    <span data-ttu-id="032f4-195">Generični član ekipe je zdaj dodeljen opravilu.</span><span class="sxs-lookup"><span data-stu-id="032f4-195">The generic team member is now assigned to the task.</span></span>

    ![Generični član ekipe je dodeljen opravilu](media/Resource-Management-image25.png)

    <span data-ttu-id="032f4-197">Na zavihku **Ekipa** boste videli novega generičnega člana ekipe.</span><span class="sxs-lookup"><span data-stu-id="032f4-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="032f4-198">Opazili boste, da ima samo dodeljene ure.</span><span class="sxs-lookup"><span data-stu-id="032f4-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="032f4-199">Te ure so vsota vseh opravil, ki so dodeljena generičnemu članu ekipe.</span><span class="sxs-lookup"><span data-stu-id="032f4-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="032f4-200">Generični član ekipe še nima zahtevanih ur ali pogoja za vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Generični član ekipe na zavihku »Ekipa«](media/Resource-Management-image26.png)

5. <span data-ttu-id="032f4-202">Generičnega člana skupine lahko zdaj z izbirnikom virov dodelite drugim opravilom.</span><span class="sxs-lookup"><span data-stu-id="032f4-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Generični član ekipe v izbirniku virov](media/Resource-Management-image27.png)

    <span data-ttu-id="032f4-204">Ko dokončate dodeljevanje splošnih virov opravilom, lahko ustvarite pogoj za vir za splošni vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="032f4-205">Na zavihku **Ekipa** izberite splošni vir in nato **Ustvari zahtevo**.</span><span class="sxs-lookup"><span data-stu-id="032f4-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Ukaz »Ustvari zahtevo«](media/Resource-Management-image28.png)

    <span data-ttu-id="032f4-207">Ko je zahteva ustvarjena, bo generični član ekipe imel zahtevane ure in povezavo za pogoj za vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Povezava za pogoj za vir](media/Resource-Management-image29.png)

    <span data-ttu-id="032f4-209">Ko rezervirate poimenovani vir, je splošni vir odstranjen iz ekipe zamenjan s poimenovanim virom.</span><span class="sxs-lookup"><span data-stu-id="032f4-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Splošni vir je zamenjan s poimenovanim virom](media/Resource-Management-image30.png)

    <span data-ttu-id="032f4-211">Na zavihku **Načrtovanje** so dodelitve splošnega vira odstranjene in zamenjane s poimenovanim virom.</span><span class="sxs-lookup"><span data-stu-id="032f4-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Dodelitve splošnega vira so zamenjane s poimenovanim virom na zavihku »Načrtovanje«](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="032f4-213">To se zgodi le, če je poimenovani vir v celoti rezerviran za zahtevo za splošni vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="032f4-214">Če poimenovani vir delno zamenja zahtevo za splošni vir ali več poimenovanih virov zamenja zahtevo za splošni vir, splošni vir ostane dodeljen opravilu.</span><span class="sxs-lookup"><span data-stu-id="032f4-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="032f4-215">Na spodnji sliki je bilo načrtovano 80-urno opravilo za pet dni (16 ur na dan v petih dneh) in dodeljeno splošnemu viru z imenom **Funkcionalno**.</span><span class="sxs-lookup"><span data-stu-id="032f4-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80-urno, petdnevno opravilo dodeljeno splošnemu viru »Funkcionalno«](media/Resource-Management-image32.png)

    <span data-ttu-id="032f4-217">Ko ustvarite zahtevo, je ustvarite za 80 ur v petih dneh.</span><span class="sxs-lookup"><span data-stu-id="032f4-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Zahteva, ustvarjena za 80 ur v petih dneh](media/Resource-Management-image33.png)

    <span data-ttu-id="032f4-219">Ker razpoložljivi viri delajo le osem ur na dan, sta izpolnitev zahteve potrebna dva vira.</span><span class="sxs-lookup"><span data-stu-id="032f4-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Drugi vir](media/Resource-Management-image35.png)

    <span data-ttu-id="032f4-221">Na zavihku **Ekipa** lahko zdaj vidite, da splošni vir nima zahtevanih ur, temveč so dodeljene ure še vedno prikazane skupaj z obema poimenovanima viroma, ki zagotavljata izpolnitev.</span><span class="sxs-lookup"><span data-stu-id="032f4-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dva poimenovana vira na zavihku »Ekipa«](media/Resource-Management-image36.png)

    <span data-ttu-id="032f4-223">Na zavihku **Načrtovanje** splošni vir ostane dodeljen opravilu.</span><span class="sxs-lookup"><span data-stu-id="032f4-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Splošni viri na zavihku »Načrtovanje«](media/Resource-Management-image37.png)

<span data-ttu-id="032f4-225">PSA ne dodeli obeh virov opravilu, saj bi bil zaradi tega urnik manj predvidljiv.</span><span class="sxs-lookup"><span data-stu-id="032f4-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="032f4-226">V tem enostavnem primeru je enostavno razdeliti ure enakomerno med dvema viroma.</span><span class="sxs-lookup"><span data-stu-id="032f4-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="032f4-227">Vendar pa bi morala PSA v bolj zapletenih scenarijih, ki vključujejo več opravil in več virov, predpostaviti, kako naj dodeli rezervacije, prejete za več virov v več opravilih.</span><span class="sxs-lookup"><span data-stu-id="032f4-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="032f4-228">Zato je v teh scenarijih vodja projekta odgovoren za razčlenjevanje več rezervacij in njihovo dodeljevanje, če je to potrebno.</span><span class="sxs-lookup"><span data-stu-id="032f4-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="032f4-229">Za dodeljevanje rezervacij vodja projekta dodeli opravila iz splošnih virov v poimenovane vire in nato uporabi pogled **Uskladitev**, da zagotovi, da dodelitev deluje z rezervacijami.</span><span class="sxs-lookup"><span data-stu-id="032f4-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="032f4-230">Urejanje pogoja za vir</span><span class="sxs-lookup"><span data-stu-id="032f4-230">Edit a resource requirement</span></span>

<span data-ttu-id="032f4-231">Ko je pogoj za vir ustvarjen, lahko vodja projekta ali upravitelj virov uredi podrobnosti, da natančneje določi merila iskanja, ko uporablja ploščo razporeda.</span><span class="sxs-lookup"><span data-stu-id="032f4-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="032f4-232">Če želite urediti pogoj za vir, sledite spodnjim korakom.</span><span class="sxs-lookup"><span data-stu-id="032f4-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="032f4-233">Na strani **Projekti** na zavihku **Ekipa** izberite povezavo do katerekoli zahteve v splošnem viru.</span><span class="sxs-lookup"><span data-stu-id="032f4-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="032f4-234">Na strani **Pogoj za vir**, ki se prikaže, lahko posodobite več atributov.</span><span class="sxs-lookup"><span data-stu-id="032f4-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="032f4-235">Tukaj je nekaj primerov:</span><span class="sxs-lookup"><span data-stu-id="032f4-235">Here are some examples:</span></span>

    - <span data-ttu-id="032f4-236">Ime</span><span class="sxs-lookup"><span data-stu-id="032f4-236">Name</span></span>
    - <span data-ttu-id="032f4-237">Od datuma</span><span class="sxs-lookup"><span data-stu-id="032f4-237">From Date</span></span>
    - <span data-ttu-id="032f4-238">Do datuma</span><span class="sxs-lookup"><span data-stu-id="032f4-238">To Date</span></span>
    - <span data-ttu-id="032f4-239">Trajanje</span><span class="sxs-lookup"><span data-stu-id="032f4-239">Duration</span></span>
    - <span data-ttu-id="032f4-240">Vrsta vira</span><span class="sxs-lookup"><span data-stu-id="032f4-240">Resource Type</span></span>

<span data-ttu-id="032f4-241">Na strani **Pogoj za vir** lahko vodja projekta ali upravitelj virov določi tudi te informacije:</span><span class="sxs-lookup"><span data-stu-id="032f4-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="032f4-242">Znanja</span><span class="sxs-lookup"><span data-stu-id="032f4-242">Skills</span></span>
- <span data-ttu-id="032f4-243">Vloge</span><span class="sxs-lookup"><span data-stu-id="032f4-243">Roles</span></span>
- <span data-ttu-id="032f4-244">Nastavitve virov</span><span class="sxs-lookup"><span data-stu-id="032f4-244">Resource preferences</span></span>
- <span data-ttu-id="032f4-245">Želena organizacijska enota</span><span class="sxs-lookup"><span data-stu-id="032f4-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="032f4-246">Posodabljanje rezervacij virov po tem, ko so rezervirani v projektu</span><span class="sxs-lookup"><span data-stu-id="032f4-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="032f4-247">Ko v projektno ekipo dodate splošni ali poimenovani vir, lahko spremenite rezervacije vira.</span><span class="sxs-lookup"><span data-stu-id="032f4-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="032f4-248">Na strani **Projekti** na zavihku **Ekipa** izberite člana ekipe in nato **Upravljaj rezervacije**.</span><span class="sxs-lookup"><span data-stu-id="032f4-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Odpre se plošča razporeda za izbranega člana ekipe](media/Resource-Management-image40.png)

    <span data-ttu-id="032f4-250">Prikaže se plošča razporeda, na kateri so prikazane rezervacije člana projektne ekipe.</span><span class="sxs-lookup"><span data-stu-id="032f4-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="032f4-251">Razširite zapis člana ekipe in si oglejte ure, ki so bile rezervirane za ta projekt in druge projekte, ki porabljajo zmogljivost člana ekipe.</span><span class="sxs-lookup"><span data-stu-id="032f4-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="032f4-252">Izberite in povlecite rezervacijo, da jo razširite ali skrajšate.</span><span class="sxs-lookup"><span data-stu-id="032f4-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="032f4-253">Prikaže se pogovorno okno **Ustvarjanje rezervacije vira**, ki vam omogoča prilagoditev rezervacije.</span><span class="sxs-lookup"><span data-stu-id="032f4-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Pogovorno okno »Ustvarjanje rezervacije vira«](media/Resource-Management-image41.png)

3. <span data-ttu-id="032f4-255">Z desno tipko miške kliknite rezervacijo.</span><span class="sxs-lookup"><span data-stu-id="032f4-255">Right-click the booking.</span></span> <span data-ttu-id="032f4-256">Nato lahko uporabite priročni meni in dokončate ta dejanja:</span><span class="sxs-lookup"><span data-stu-id="032f4-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="032f4-257">Spremenite stanje rezervacije.</span><span class="sxs-lookup"><span data-stu-id="032f4-257">Change the booking status.</span></span>
    - <span data-ttu-id="032f4-258">Uredite rezervacijo.</span><span class="sxs-lookup"><span data-stu-id="032f4-258">Edit the booking.</span></span>
    - <span data-ttu-id="032f4-259">Nadomestite vir v projektni ekipi.</span><span class="sxs-lookup"><span data-stu-id="032f4-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="032f4-260">Spreminjanje stanja rezervacije</span><span class="sxs-lookup"><span data-stu-id="032f4-260">Change the booking status</span></span>

<span data-ttu-id="032f4-261">Spremenite lahko katero koli privzeto stanje rezervacije ali stanje rezervacije po meri.</span><span class="sxs-lookup"><span data-stu-id="032f4-261">You can change any default or custom booking status.</span></span>

![Ukaz »Spremeni stanje«](media/Resource-Management-image42.png)

<span data-ttu-id="032f4-263">V PSA so na voljo ta stanja:</span><span class="sxs-lookup"><span data-stu-id="032f4-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="032f4-264">**Preklicano** – to stanje prekliče rezervacijo vira in sprosti zmogljivost vira.</span><span class="sxs-lookup"><span data-stu-id="032f4-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="032f4-265">**Veljavna rezervacija** – to stanje porablja zmogljivost vira.</span><span class="sxs-lookup"><span data-stu-id="032f4-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="032f4-266">Rezervacija ima to stanje običajno takrat, ko na strani **Projekti** odprete **Upravljanje rezervacij** iz mreže **Vsi člani ekipe**.</span><span class="sxs-lookup"><span data-stu-id="032f4-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="032f4-267">**Začasna rezervacija** – to stanje doda vir ekipi, vendar ne porabi zmogljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="032f4-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="032f4-268">To pomeni, da je bil vir rezerviran za morebitno delo, vendar ima še vedno zmogljivost, če ga potrebujete pri drugih poslih.</span><span class="sxs-lookup"><span data-stu-id="032f4-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="032f4-269">Z vidika splošne razpoložljivosti virov imajo začasne rezervacije drugačno stanje kot veljavne rezervacije.</span><span class="sxs-lookup"><span data-stu-id="032f4-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="032f4-270">**Predlagano** – to stanje predstavlja predlog za vir upravitelja virov ali vodje projekta.</span><span class="sxs-lookup"><span data-stu-id="032f4-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="032f4-271">Predlogi ne porabijo zmogljivosti vira in vir ni dodan projektni ekipi.</span><span class="sxs-lookup"><span data-stu-id="032f4-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="032f4-272">Za veljavno rezervacijo vira v ekipi mora vodja projekta sprejeti predlog.</span><span class="sxs-lookup"><span data-stu-id="032f4-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="032f4-273">Pošiljanje zahtev za vire</span><span class="sxs-lookup"><span data-stu-id="032f4-273">Submit resource requests</span></span>

<span data-ttu-id="032f4-274">Zahteve za vir se uporabljajo za hranjenje zahteve (zahtevanega pogoja za vir), ki ga mora izpolniti upravitelj virov.</span><span class="sxs-lookup"><span data-stu-id="032f4-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="032f4-275">Za splošni vir, ki je že v ekipi, lahko zahtevo za vir pošljete neposredno.</span><span class="sxs-lookup"><span data-stu-id="032f4-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="032f4-276">Zahtevo za vir je mogoče izpolniti na dva načina:</span><span class="sxs-lookup"><span data-stu-id="032f4-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="032f4-277">Upravitelj virov neposredno izpolni zahtevo.</span><span class="sxs-lookup"><span data-stu-id="032f4-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="032f4-278">V tem primeru se splošni vir zamenja z veljavno rezervacijo s poimenovanim virom.</span><span class="sxs-lookup"><span data-stu-id="032f4-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="032f4-279">Upravitelj virov predlaga vir vodji projekta, vodja projekta pa odobri ali zavrne predlagani vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="032f4-280">Neposredna izpolnitev zahtev za vir</span><span class="sxs-lookup"><span data-stu-id="032f4-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="032f4-281">Ko je ustvarjen zahtevani pogoj za vir, lahko vodja projekta pošlje zahtevo za vir za splošni vir tako, da izbere vir in nato možnost **Pošlji zahtevo**.</span><span class="sxs-lookup"><span data-stu-id="032f4-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Gumb »Pošlji zahtevo«](media/Resource-Management-image45.png)

<span data-ttu-id="032f4-283">Komentarje o viru je mogoče posredovati upravitelju virov, ki izpolnjuje zahtevo.</span><span class="sxs-lookup"><span data-stu-id="032f4-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="032f4-284">Po predložitvi zahteve se polje **Stanje** za člana ekipe spremeni v **Poslano**.</span><span class="sxs-lookup"><span data-stu-id="032f4-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Vnos neobveznih komentarjev](media/Resource-Management-image46.png)

<span data-ttu-id="032f4-286">Ko upravitelj virov izpolni zahtevo, je generični član ekipe zamenjan s poimenovanim virom v mreži **Vsi člani ekipe**.</span><span class="sxs-lookup"><span data-stu-id="032f4-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Generični član skupine je zamenjan s poimenovanim virom v mreži »Vsi člani ekipe«](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="032f4-288">Uporaba predlaganega vira za zahteve za vir</span><span class="sxs-lookup"><span data-stu-id="032f4-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="032f4-289">Namesto neposredne rezervacije vira v zahtevi za vir lahko upravitelj virov predlaga vir vodji projekta.</span><span class="sxs-lookup"><span data-stu-id="032f4-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="032f4-290">Upravitelj virov lahko uporabi to možnost, ko natančno ujemanje za zahtevane pogoje ni na voljo.</span><span class="sxs-lookup"><span data-stu-id="032f4-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="032f4-291">Ko upravitelj virov predlaga vir, vodja projekta vidi, da je polje **Stanje** za generičnega člana ekipe spremenjeno v **Potreben pregled**.</span><span class="sxs-lookup"><span data-stu-id="032f4-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Stanje generičnega člana ekipe se je spremenilo v »Potrebuje pregled«](media/Resource-Management-image48.png)

<span data-ttu-id="032f4-293">Če si želite predlagani vir ogledati skupaj z upodobitvijo učinka rezervacije predloga, dvokliknite člana ekipe s stanjem **Potreben pregled**.</span><span class="sxs-lookup"><span data-stu-id="032f4-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="032f4-294">Nato izberite zavihek **Predlagani viri**.</span><span class="sxs-lookup"><span data-stu-id="032f4-294">Then select the **Proposed Resources** tab.</span></span>

![Zavihek »Predlagani viri«](media/Resource-Management-image49.png)

<span data-ttu-id="032f4-296">Izberite **Sprejmi vse predloge**, da sprejmete vse predlagane vire, ali **Zavrni vse predloge**, da jih zavrnete.</span><span class="sxs-lookup"><span data-stu-id="032f4-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="032f4-297">Če sprejmete predlagane vire, so v projektu veljavno rezervirani kot člani ekipe in zamenjajo splošne vire.</span><span class="sxs-lookup"><span data-stu-id="032f4-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="032f4-298">Sprejeti ali zavrniti morate vse predlagane vire.</span><span class="sxs-lookup"><span data-stu-id="032f4-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="032f4-299">Ne morete jih delno sprejeti ali zavrniti.</span><span class="sxs-lookup"><span data-stu-id="032f4-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="032f4-300">Zamenjava vira v projektni ekipi</span><span class="sxs-lookup"><span data-stu-id="032f4-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="032f4-301">Včasih mora vodja projekta zamenjati rezerviranega člana ekipe v projektu.</span><span class="sxs-lookup"><span data-stu-id="032f4-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="032f4-302">Na strani **Projekti** na zavihku **Ekipa** izberite vir, ki potrebuje zamenjavo, in nato **Upravljaj rezervacije**.</span><span class="sxs-lookup"><span data-stu-id="032f4-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="032f4-303">Razširite vir, da prikažete projekte, ki jim je dodeljen.</span><span class="sxs-lookup"><span data-stu-id="032f4-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Razširjen vir prikazuje dodeljene projekte](media/Resource-Management-image50.png)

3. <span data-ttu-id="032f4-305">Z desno tipko miške kliknite projekt in nato izberite **Nadomeščanje vira**.</span><span class="sxs-lookup"><span data-stu-id="032f4-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="032f4-306">Če poznate vir, s katerim želite nadomestiti trenutni vir, izberite ali vnesite ime in nato izberite **Znova dodeli**.</span><span class="sxs-lookup"><span data-stu-id="032f4-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Določanje nadomestnega vira](media/Resource-Management-image51.png)

    <span data-ttu-id="032f4-308">Ali pa sledite spodnjim korakom, da poiščete vir:</span><span class="sxs-lookup"><span data-stu-id="032f4-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="032f4-309">Izberite **Najdi nadomestitev**.</span><span class="sxs-lookup"><span data-stu-id="032f4-309">Select **Find Substitution**.</span></span>

        ![Iskanje nadomestnega vira](media/Resource-Management-image52.png)

        <span data-ttu-id="032f4-311">Pomočnik za razporejanje vrne seznam nadomestkov, ki so na voljo.</span><span class="sxs-lookup"><span data-stu-id="032f4-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="032f4-312">V pomočniku za razporejanje lahko dodatno filtrirate razpoložljive vire, da poiščete ustrezen nadomestek.</span><span class="sxs-lookup"><span data-stu-id="032f4-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Seznam nadomestkov, ki so na voljo](media/Resource-Management-image53.png)

    2. <span data-ttu-id="032f4-314">Če želite nadomestiti vir, izberite želeni vir in nato izberite **Nadomestek**.</span><span class="sxs-lookup"><span data-stu-id="032f4-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Nadomestni vir je izbran](media/Resource-Management-image54.png)

    <span data-ttu-id="032f4-316">Rezervacije in dodelitve se nadomestijo z novim virom.</span><span class="sxs-lookup"><span data-stu-id="032f4-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Rezervacije in dodelitve so nadomeščene z novim virom](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="032f4-318">Usklajevanje rezervacij in dodelitev člana ekipe</span><span class="sxs-lookup"><span data-stu-id="032f4-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="032f4-319">Pri članih ekipe so rezervacije in dodelitve ohlapno povezane.</span><span class="sxs-lookup"><span data-stu-id="032f4-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="032f4-320">Z drugimi besedami, viri imajo lahko dodelitve brez rezervacij ali pa rezervacije brez dodelitev.</span><span class="sxs-lookup"><span data-stu-id="032f4-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="032f4-321">V idealnem primeru so rezervacije in dodelitve usklajene, tako da imajo viri določeno zmogljivost za izvajanje dodelitev opravila.</span><span class="sxs-lookup"><span data-stu-id="032f4-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="032f4-322">Vendar pa lahko rezervacije temeljijo na razpoložljivosti, časi opravil pa se lahko spremenijo, ko se projekt nadaljuje.</span><span class="sxs-lookup"><span data-stu-id="032f4-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="032f4-323">Zato ohlapno povezovanje rezervacij in dodelitev zagotavlja prilagodljivost.</span><span class="sxs-lookup"><span data-stu-id="032f4-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="032f4-324">PSA ima zavihek **Uskladitev**, ki omogoča vodjam projektov, da uskladijo rezervacije članov ekipe in njihove dodelitve za projektne ekipe.</span><span class="sxs-lookup"><span data-stu-id="032f4-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Zavihek »Uskladitev«](media/Resource-Management-image56.png)

<span data-ttu-id="032f4-326">Zavihek **Uskladitev** prikaže rezervacije in dodelitve vse do ravni dodelitve posameznega opravila za vsakega člana ekipe.</span><span class="sxs-lookup"><span data-stu-id="032f4-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="032f4-327">Ure so prikazane v celicah, ki predstavljajo časovna obdobja od mesecev do dni.</span><span class="sxs-lookup"><span data-stu-id="032f4-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="032f4-328">Zavihek prikazuje tudi skupno neto vsoto za projekt, skupaj s stolpcem s skupnim izračunom.</span><span class="sxs-lookup"><span data-stu-id="032f4-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="032f4-329">Zavihek za vsak vir izračuna razliko med rezervacijami člana ekipe in skupno vrednostjo dodelitev opravil člana ekipe.</span><span class="sxs-lookup"><span data-stu-id="032f4-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="032f4-330">V idealnem primeru je ta razlika 0 (nič).</span><span class="sxs-lookup"><span data-stu-id="032f4-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="032f4-331">Z drugimi besedami, med rezervacijami in dodelitvami ne bi smelo biti razlike.</span><span class="sxs-lookup"><span data-stu-id="032f4-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="032f4-332">Razlike so obarvane in osenčene, da opozorijo na dva pogoja:</span><span class="sxs-lookup"><span data-stu-id="032f4-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="032f4-333">**Primanjkljaj rezervacij** – do primanjkljaja rezervacij pride, ko ima vir več dodelitev kot rezervacij.</span><span class="sxs-lookup"><span data-stu-id="032f4-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="032f4-334">Ker ta zmogljivost ni bila rezervirana, lahko vodja projekta odpravi to stanje tako, da razširi rezervacije vira za kritje primanjkljaja.</span><span class="sxs-lookup"><span data-stu-id="032f4-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="032f4-335">**Odvečne rezervacije** – do odvečnih rezervacij pride, ko je vir rezerviran za projekt, vendar ni bil dodeljen opravilom.</span><span class="sxs-lookup"><span data-stu-id="032f4-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="032f4-336">Ta pogoj je morda sprejemljiv v primerih, ko je bil vir rezerviran za projekt, preden je prišlo do dodelitve opravila.</span><span class="sxs-lookup"><span data-stu-id="032f4-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="032f4-337">V drugih primerih pa vir morda ni načrtovan za dodelitev opravilom.</span><span class="sxs-lookup"><span data-stu-id="032f4-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="032f4-338">V takem primeru bi moral upravitelj projekta razmisliti o preklicu rezervacij vira, da se lahko zmogljivost uporabi za drug projekt.</span><span class="sxs-lookup"><span data-stu-id="032f4-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="032f4-339">Ko si ogledujete čas na višji ravni, kot je dnevna raven (npr. na ravni meseca), se v nekaterih primerih za vir lahko prikaže neto razlika nič (z drugimi besedami, rezervacije = dodelitve).</span><span class="sxs-lookup"><span data-stu-id="032f4-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="032f4-340">Če pa pogledate čas na tedenski ravni, boste morda videli, da obstajajo dodelitve z nič urami in rezervacije s 40 urami v prvem tednu ter dodelitve s 40 urami in rezervacije z nič urami v drugem tednu meseca.</span><span class="sxs-lookup"><span data-stu-id="032f4-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="032f4-341">Na splošno so rezervacije in dodelitve usklajene, vendar se razlikujejo od enega tedna do drugega.</span><span class="sxs-lookup"><span data-stu-id="032f4-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="032f4-342">Ko prikažete čas na višjih ravneh, imajo celice na zavihku **Usklajevanje** kazalnik, ki vas obvesti, da obstajajo razlike na nižjih ravneh.</span><span class="sxs-lookup"><span data-stu-id="032f4-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="032f4-343">Z dvojnim klikom v celici lahko povečate prikaz in si ogledate razliko.</span><span class="sxs-lookup"><span data-stu-id="032f4-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="032f4-344">Nato lahko kliknete z desno tipko miške, da pomanjšate prikaz. Če izberete vir in nato uporabite kontrolnik **Naslednja razlika** v orodni vrstici mreže, se lahko pomaknete na naslednjo razliko med rezervacijami in dodelitvami za ta vir.</span><span class="sxs-lookup"><span data-stu-id="032f4-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="032f4-345">Nato lahko za vrnitev uporabite kontrolnik **Prejšnja razlika**.</span><span class="sxs-lookup"><span data-stu-id="032f4-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="032f4-346">Prav tako lahko v meniju **Nastavitve** izklopite kazalnik razlike in delovanje krmarjenja.</span><span class="sxs-lookup"><span data-stu-id="032f4-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Kazalnik razlike](media/Resource-Management-image57.png)

<span data-ttu-id="032f4-348">Če imate dodelitve opravil za vir, a nimate rezervacij, na strani **Projekti** na zavihku **Usklajevanje** izberite primanjkljaj rezervacij in nato **Podaljšaj rezervacijo**.</span><span class="sxs-lookup"><span data-stu-id="032f4-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="032f4-349">Prikaže se pogovorno **Podaljšaj rezervacijo** in prikaže rezervacijo, ki je potrebna za odpravo primanjkljaja vira.</span><span class="sxs-lookup"><span data-stu-id="032f4-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="032f4-350">Prikazuje tudi obstoječe rezervacije vira za vse projekte ali druge entitete, ki jih je mogoče razporediti.</span><span class="sxs-lookup"><span data-stu-id="032f4-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="032f4-351">Če izberete **V redu**, da ustvarite rezervacijo za vir, lahko ne glede na razpoložljivost tega vira ustvarite prekomerno rezervacijo.</span><span class="sxs-lookup"><span data-stu-id="032f4-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Pogovorno okno »Podaljšaj rezervacijo«](media/Resource-Management-image58.png)

<span data-ttu-id="032f4-353">Vodja projekta ali upravitelj virov lahko nato s ploščo razporeda reši vse primere, kjer ima vir preveliko število rezervacij glede na svojo zmogljivost.</span><span class="sxs-lookup"><span data-stu-id="032f4-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]