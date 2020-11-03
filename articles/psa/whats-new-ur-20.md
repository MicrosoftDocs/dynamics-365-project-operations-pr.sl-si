---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 20, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za izdajo posodobitve 20 za Project Service Automation, V3
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084705"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="df777-103">Izdaja posodobitve 20 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="df777-103">Project Service Automation Update Release 20, V3</span></span>

<span data-ttu-id="df777-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="df777-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="df777-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="df777-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="df777-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="df777-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="df777-107">Če želite posodobiti na to izdajo, obiščite stran z rešitvami v skrbniškem središču za Dynamics 365 online, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="df777-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="df777-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="df777-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="df777-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za Project Service Automation V3, izdaja posodobitve 20.</span><span class="sxs-lookup"><span data-stu-id="df777-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="df777-110">Številka graditve te različice je V3.10.31.37 in je na splošno na voljo prek samostojne posodobitve junija 2020.</span><span class="sxs-lookup"><span data-stu-id="df777-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="df777-111">Izdaja posodobitve 20</span><span class="sxs-lookup"><span data-stu-id="df777-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="df777-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="df777-112">Bug fixes</span></span>

<span data-ttu-id="df777-113">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="df777-113">**Project Management**</span></span>

<span data-ttu-id="df777-114">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="df777-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="df777-115">Če uvažate člane projektne ekipe z načinom dodeljevanja, ki zahteva ure, se prikaže nejasno sporočilo o napaki, ko je določeno število ur enako nič.</span><span class="sxs-lookup"><span data-stu-id="df777-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="df777-116">Ko uporabnik doseže največje dovoljeno število znakov v polju **Opis** projektne naloge, se pojavi neustrezna napaka.</span><span class="sxs-lookup"><span data-stu-id="df777-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="df777-117">Ko je jezik uporabnika nastavljen na japonščino, stran **Prenos dodatka za Microsoft Dynamics 365 Project Service Automation** preusmeri na angleško stran za prenos.</span><span class="sxs-lookup"><span data-stu-id="df777-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="df777-118">Ko se pojavi napaka strežnika, se oznaka sinhronizacije na zavihku **Načrtovanje** obrazca **Projekti** včasih ohrani.</span><span class="sxs-lookup"><span data-stu-id="df777-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="df777-119">Ko je opravilo spremenjeno, so odvečne posodobitve opravil poslane strežniku.</span><span class="sxs-lookup"><span data-stu-id="df777-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="df777-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="df777-120">**Sales**</span></span>

<span data-ttu-id="df777-121">Odpravljene so naslednje težave:</span><span class="sxs-lookup"><span data-stu-id="df777-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="df777-122">Če na obrazcu **Pogodba** dvokliknete možnost **Ustvari račun** , se za en zapis dejanske vrednosti ustvarita dva računa.</span><span class="sxs-lookup"><span data-stu-id="df777-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="df777-123">V brskalniku Internet Explorer 11 uporabniki ne morejo ustvariti vnosov stroškov.</span><span class="sxs-lookup"><span data-stu-id="df777-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="df777-124">Razveljavitev stroškov in razveljavitev neplačanih dejanskih opravljenih prodajnih del niso povezani.</span><span class="sxs-lookup"><span data-stu-id="df777-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="df777-125">Z gumbom **Osvežitev opravljenih del** na obrazcu **Projekt** se ne osvežijo **Dejanske ure za opravilo**.</span><span class="sxs-lookup"><span data-stu-id="df777-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="df777-126">Z vtičnikom **PreValidateProjectTeamMemberCreate** lahko ustvarite podvojene splošne vire, ki jih je mogoče rezervirati, ko je atribut **msdyn_isgenericresourceprojectscoped** nastavljeno na **False**.</span><span class="sxs-lookup"><span data-stu-id="df777-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="df777-127">Z možnostjo **Znova izračunaj** počistite stroške, ki se zaračunajo za podrobnosti vrstice ponudb in podrobnosti vrstice pogodbe na podlagi izdelkov.</span><span class="sxs-lookup"><span data-stu-id="df777-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="df777-128">V določenih primerih vtičnik **PostEstimateLineUpdate** prikazuje napako izjeme sklica z vrednostjo »null«.</span><span class="sxs-lookup"><span data-stu-id="df777-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="df777-129">Trajanje časovne faze v razdelku **Tabela analize dobičkonosnosti** se ne ujema s trajanjem stroškov v podrobnostih vrstice ponudbe s fiksno ceno.</span><span class="sxs-lookup"><span data-stu-id="df777-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="df777-130">Vrednosti enot in skupin enot niso pravilno privzete za kategorije stroškov v obrazcih **Podrobnosti vrstice pogodbe** in **Podrobnosti vrstice ponudbe**.</span><span class="sxs-lookup"><span data-stu-id="df777-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="df777-131">Seznami **Lastna cena organizacijske enote** dovoljujejo prekrivanje datumske veljavnosti.</span><span class="sxs-lookup"><span data-stu-id="df777-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="df777-132">Uporabniki ne smejo spreminjati možnosti **OrgUnit** , ko vrsta naročila ne temelji na delu, ker bo prišlo do napake izjeme sklica z vrednostjo »null«.</span><span class="sxs-lookup"><span data-stu-id="df777-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="df777-133">Pri poskusu krmarjenja iz obrazca **Podrobnosti vrstice ponudbe** nazaj na zavihek **Ponudba** se obrazec osveži in prikaže se zavihek **Povzetek**.</span><span class="sxs-lookup"><span data-stu-id="df777-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
