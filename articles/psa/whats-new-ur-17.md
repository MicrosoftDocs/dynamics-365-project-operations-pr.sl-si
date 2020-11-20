---
title: Novosti ali spremembe v izdaji posodobitve za Project Service Automation 17, V3
description: V tej temi so navedene funkcije in popravki, ki so na voljo za Project Service Automation V3, izdaja posodobitve 17.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: bb93208217972639f91b39b7b6705d9897373ef7
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126827"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="2fb60-103">Izdaja posodobitve 17 za Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="2fb60-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="2fb60-104">Z veseljem predstavljamo najnovejšo posodobitev za aplikacijo Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2fb60-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2fb60-105">Ta izdaja vključuje nekatere pomembne izboljšave kakovosti, delovanja in uporabnosti.</span><span class="sxs-lookup"><span data-stu-id="2fb60-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="2fb60-106">Ta izdaja je združljiva s storitvijo Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2fb60-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2fb60-107">Če želite posodobiti na to izdajo, obiščite skrbniško središče za Dynamics 365 online in odprite stran z rešitvami, da namestite posodobitev.</span><span class="sxs-lookup"><span data-stu-id="2fb60-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="2fb60-108">Za več informacij glejte [Namestitev, posodobitev ali odstranitev prednostne rešitve](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2fb60-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2fb60-109">V tej temi so navedene funkcije in popravki, ki so novi ali spremenjeni za PSA V3, izdaja posodobitve 17.</span><span class="sxs-lookup"><span data-stu-id="2fb60-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="2fb60-110">Ta različica ima številko graditve V3.10.6.34 in je splošno na voljo s samostojno posodobitvijo v marcu 2020.</span><span class="sxs-lookup"><span data-stu-id="2fb60-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="2fb60-111">Izdaja posodobitve 17</span><span class="sxs-lookup"><span data-stu-id="2fb60-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2fb60-112">Popravki napak</span><span class="sxs-lookup"><span data-stu-id="2fb60-112">Bug fixes</span></span>

<span data-ttu-id="2fb60-113">**Splošno**</span><span class="sxs-lookup"><span data-stu-id="2fb60-113">**General**</span></span>

- <span data-ttu-id="2fb60-114">Popravljeno: Posodobitev aplikacije Project Service Automation za uveljavitev licenc za člane ekipe (središče za projektne vire bo vsebovalo metapodatke 3.x paketa storitve za člane ekipe)</span><span class="sxs-lookup"><span data-stu-id="2fb60-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="2fb60-115">**Čas in strošek**</span><span class="sxs-lookup"><span data-stu-id="2fb60-115">**Time and Expense**</span></span>

- <span data-ttu-id="2fb60-116">Popravljeno: Ocene stroškov ni mogoče spremeniti iz ničelne cene v nič (0).</span><span class="sxs-lookup"><span data-stu-id="2fb60-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="2fb60-117">Ta sprememba se ne upošteva.</span><span class="sxs-lookup"><span data-stu-id="2fb60-117">The change is ignored.</span></span>

<span data-ttu-id="2fb60-118">**Vodenje projektov**</span><span class="sxs-lookup"><span data-stu-id="2fb60-118">**Project Management**</span></span>

- <span data-ttu-id="2fb60-119">Popravljeno: Kontrola za ničelne vrednosti je bila dodana imenu položaja člana ekipe.</span><span class="sxs-lookup"><span data-stu-id="2fb60-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="2fb60-120">Popravljeno: Polje **msdyn_userresourceid** v entiteti **msdyn_resourceassignment** je zastarelo.</span><span class="sxs-lookup"><span data-stu-id="2fb60-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="2fb60-121">Popravljeno: Posodobitev z 2.x na 3.x sedaj obravnava krivulje praznega obsega dela za dodelitev opravil.</span><span class="sxs-lookup"><span data-stu-id="2fb60-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="2fb60-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="2fb60-122">**Sales**</span></span>

- <span data-ttu-id="2fb60-123">Popravljeno: **Invoice.PreValidateInvoiceUpdate** sedaj obravnava scenarij ustreznega ponovnega dodeljevanja lastnikov zapisov.</span><span class="sxs-lookup"><span data-stu-id="2fb60-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="2fb60-124">Popravljeno: Če je razred transakcije **Čas**, **UnitGroup** ni mogoče urejati za vse entitete, vključno z: **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** in **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="2fb60-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="2fb60-125">Vendar pa polja **Enota** ni mogoče urejati za **JournalLine** in **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="2fb60-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


