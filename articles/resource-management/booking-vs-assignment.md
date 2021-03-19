---
title: Rezervacije v primerjavi z dodelitvami
description: Ta tema ponuja informacije o razlikah med rezervacijami virov in dodeljevanjem virov.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279923"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="4ff7f-103">Rezervacije v primerjavi z dodelitvami</span><span class="sxs-lookup"><span data-stu-id="4ff7f-103">Bookings vs assignments</span></span>

<span data-ttu-id="4ff7f-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="4ff7f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4ff7f-105">Rezervacije so potrjene ali začasne dodelitve virov določenemu projektu.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="4ff7f-106">Potrjene rezervacije porabijo zmogljivost vira.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="4ff7f-107">Rezervacije predstavljajo organizacijske pojme za ekipe, da lahko te razumejo, kako bodo viri vključeni po različnih projektih.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="4ff7f-108">Dynamics 365 Project Operations obravnava rezervacije kot koncept na ravni projekta.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="4ff7f-109">Za razliko od rezervacij, so dodelitve zaveza virov k projektnih opravilom v razporedu projekta.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="4ff7f-110">Viri so lahko imenovani ali splošni.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-110">The resources can be named or generic.</span></span>  <span data-ttu-id="4ff7f-111">Ko zahteva za vir izhaja iz dodelitev projektnih opravil, Project Operations uporabi krivulje obsega dela delitve virov za oblikovanje krivulje podrobnosti zahtevanega pogoja za vir.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="4ff7f-112">Vendar se sklic na dodelitve virov ne ohrani.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="4ff7f-113">Posodobitve rezervacij, ki izhajajo iz zahtevanega pogoja za vir, ne posodobijo dodelitev virov.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="4ff7f-114">Običajno bo vsota rezervacij za vir enaka vsoti dodelitev vira po eni ali več opravilih.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="4ff7f-115">Vendar pa aplikacija Project Operations ne vsiljuje tega pravila.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="4ff7f-116">V pogledu **Usklajevanje** se vodji projekta prikažejo mesta, kjer se rezervacije in dodelitve vira ne skladajo.</span><span class="sxs-lookup"><span data-stu-id="4ff7f-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]