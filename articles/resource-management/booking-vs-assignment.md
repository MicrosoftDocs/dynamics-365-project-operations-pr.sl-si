---
title: Rezervacije v primerjavi z dodelitvami
description: Ta tema ponuja informacije o razlikah med rezervacijami virov in dodeljevanjem virov.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896031"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="9d970-103">Rezervacije v primerjavi z dodelitvami</span><span class="sxs-lookup"><span data-stu-id="9d970-103">Bookings vs assignments</span></span>

<span data-ttu-id="9d970-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="9d970-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9d970-105">Rezervacije so potrjene ali začasne dodelitve virov določenemu projektu.</span><span class="sxs-lookup"><span data-stu-id="9d970-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="9d970-106">Potrjene rezervacije porabijo zmogljivost vira.</span><span class="sxs-lookup"><span data-stu-id="9d970-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="9d970-107">Dodelitve označujejo dodeljevanje virov k projektnim opravilom v projektnem razporedu.</span><span class="sxs-lookup"><span data-stu-id="9d970-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="9d970-108">Viri so lahko resnični ali splošni.</span><span class="sxs-lookup"><span data-stu-id="9d970-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="9d970-109">Načeloma bi se morale rezervacije in dodelitve za resnične vire skladati, saj se ne razlikujejo.</span><span class="sxs-lookup"><span data-stu-id="9d970-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="9d970-110">Vendar pa aplikacija Microsoft Dynamics Project Operations ne vsiljuje tega pravila.</span><span class="sxs-lookup"><span data-stu-id="9d970-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="9d970-111">V pogledu **Usklajevanje** se vodji projekta prikažejo mesta, kjer se rezervacije in dodelitve vira ne skladajo.</span><span class="sxs-lookup"><span data-stu-id="9d970-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
