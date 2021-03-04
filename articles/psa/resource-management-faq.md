---
title: Pogosta vprašanja in odgovori o upravljanju virov
description: Ta tema vsebuje odgovore na pogosta vprašanja o upravljanju virov.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: d335a12a9b478bff63b6c93809c89dac9718a4be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144388"
---
# <a name="resource-management-faq"></a><span data-ttu-id="27a0b-103">Pogosta vprašanja in odgovori o upravljanju virov</span><span class="sxs-lookup"><span data-stu-id="27a0b-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="27a0b-104">Kakšna je razlika med članom ekipe in zahtevanim pogojem za vir?</span><span class="sxs-lookup"><span data-stu-id="27a0b-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="27a0b-105">Član projektne ekipe je lahko dodeljen k opravilom, rezerviran ali prevečkrat rezerviran ter nastavljen kot odobritelj.</span><span class="sxs-lookup"><span data-stu-id="27a0b-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="27a0b-106">Zahtevani pogoj za vir lahko obstaja tudi brez člana projektne ekipe v obliki osnutka o povpraševanju.</span><span class="sxs-lookup"><span data-stu-id="27a0b-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="27a0b-107">Kakšna je razlika med predlaganimi in začasno rezerviranimi urami?</span><span class="sxs-lookup"><span data-stu-id="27a0b-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="27a0b-108">Predlagane ure in začasno rezervirane ure se razlikujejo po vidljivosti.</span><span class="sxs-lookup"><span data-stu-id="27a0b-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="27a0b-109">Predlagane ure so vidne le upraviteljem virov in vodji projekta, ki je sprožil zahtevo prek zahteve za vir.</span><span class="sxs-lookup"><span data-stu-id="27a0b-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="27a0b-110">Začasno rezervirane ure so vidne vsem, ki imajo dostop do plošče razporeda.</span><span class="sxs-lookup"><span data-stu-id="27a0b-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="27a0b-111">Kako lahko vidim začasno rezervirane ure za vire znotraj ekipe?</span><span class="sxs-lookup"><span data-stu-id="27a0b-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="27a0b-112">Začasne rezervacije je mogoče opraviti ob rezervaciji zahtevanega pogoja za vir.</span><span class="sxs-lookup"><span data-stu-id="27a0b-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="27a0b-113">Viri, ki so začasno rezervirani v projektni ekipi, se nato prikažejo kot člani ekipe z začasno rezerviranimi urami.</span><span class="sxs-lookup"><span data-stu-id="27a0b-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="27a0b-114">Prikažejo se tudi na plošči razporeda.</span><span class="sxs-lookup"><span data-stu-id="27a0b-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="27a0b-115">Kako spremenim zahtevane ure ter začetne in končne datume za vir (splošen ali poimenovan), ki sem ga rezerviral/a?</span><span class="sxs-lookup"><span data-stu-id="27a0b-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="27a0b-116">Po opravljeni rezervaciji virov izberite **Upravljanje rezervacij**, če želite izvesti kakršne koli spremembe.</span><span class="sxs-lookup"><span data-stu-id="27a0b-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="27a0b-117">Katere vrste virov podpira Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="27a0b-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="27a0b-118">V aplikaciji Dynamics 365 Project Service Automation sta podprti le vrsti virov **Uporabnik** in **Stik**.</span><span class="sxs-lookup"><span data-stu-id="27a0b-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="27a0b-119">Druge vrste virov (na primer **Oprema** in **Skupina**) sicer lahko ustvarite, vendar zanje ni podprt noben celovit primer uporabe.</span><span class="sxs-lookup"><span data-stu-id="27a0b-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="27a0b-120">Kakšna je razlika med dodelitvijo in rezervacijo?</span><span class="sxs-lookup"><span data-stu-id="27a0b-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="27a0b-121">Dodelitve označujejo dodeljevanje virov k projektnim opravilom v projektnem razporedu.</span><span class="sxs-lookup"><span data-stu-id="27a0b-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="27a0b-122">Viri so lahko resnični ali splošni.</span><span class="sxs-lookup"><span data-stu-id="27a0b-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="27a0b-123">Rezervacije so potrjene ali začasne dodelitve virov določenemu projektu.</span><span class="sxs-lookup"><span data-stu-id="27a0b-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="27a0b-124">Potrjene rezervacije porabijo zmogljivost vira.</span><span class="sxs-lookup"><span data-stu-id="27a0b-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="27a0b-125">Načeloma bi se morale rezervacije in dodelitve za resnične vire skladati, saj se ne razlikujejo.</span><span class="sxs-lookup"><span data-stu-id="27a0b-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="27a0b-126">Vendar PSA ne vsiljuje tega pravila.</span><span class="sxs-lookup"><span data-stu-id="27a0b-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="27a0b-127">V pogledu »Usklajevanje« se vodji projekta prikažejo mesta, kjer se rezervacije in dodelitve vira ne skladajo.</span><span class="sxs-lookup"><span data-stu-id="27a0b-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
