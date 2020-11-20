---
title: Rezervacije v primerjavi z dodelitvami
description: Ta tema ponuja informacije o razlikah med rezervacijami virov in dodeljevanjem virov.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130238"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="bc722-103">Rezervacije v primerjavi z dodelitvami</span><span class="sxs-lookup"><span data-stu-id="bc722-103">Bookings vs assignments</span></span>

<span data-ttu-id="bc722-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="bc722-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bc722-105">Rezervacije so potrjene ali začasne dodelitve virov določenemu projektu.</span><span class="sxs-lookup"><span data-stu-id="bc722-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="bc722-106">Potrjene rezervacije porabijo zmogljivost vira.</span><span class="sxs-lookup"><span data-stu-id="bc722-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="bc722-107">Rezervacije predstavljajo organizacijske pojme za ekipe, da lahko te razumejo, kako bodo viri vključeni po različnih projektih.</span><span class="sxs-lookup"><span data-stu-id="bc722-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="bc722-108">Dynamics 365 Project Operations ima rezervacije za pojem na ravni projekta.</span><span class="sxs-lookup"><span data-stu-id="bc722-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="bc722-109">Za razliko od rezervacij, so dodelitve zaveza virov k projektnih opravilom v razporedu projekta.</span><span class="sxs-lookup"><span data-stu-id="bc722-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="bc722-110">Viri so lahko imenovani ali splošni.</span><span class="sxs-lookup"><span data-stu-id="bc722-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="bc722-111">Običajno bo vsota rezervacij za vir enaka vsoti dodelitev vira po eni ali več opravilih.</span><span class="sxs-lookup"><span data-stu-id="bc722-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="bc722-112">Vendar pa aplikacija Project Operations ne vsiljuje tega pravila.</span><span class="sxs-lookup"><span data-stu-id="bc722-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="bc722-113">V pogledu **Usklajevanje** se vodji projekta prikažejo mesta, kjer se rezervacije in dodelitve vira ne skladajo.</span><span class="sxs-lookup"><span data-stu-id="bc722-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
