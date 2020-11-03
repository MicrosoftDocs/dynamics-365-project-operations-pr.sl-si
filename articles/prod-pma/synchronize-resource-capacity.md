---
title: Sinhronizacija zmogljivosti vira
description: Ta tema vsebuje informacije o sinhronizaciji zmogljivosti vira v koledarjih in projektih.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084734"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="df49a-103">Sinhronizacija zmogljivosti vira</span><span class="sxs-lookup"><span data-stu-id="df49a-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df49a-104">Procesi za sinhronizacijo virov pomagajo zagotoviti, da se informacije za koledar in osnovni koledar stekajo navzdol v razporejanje virov projekta.</span><span class="sxs-lookup"><span data-stu-id="df49a-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="df49a-105">Če je koledar spremenjen, procesi izvedejo zahtevane spremembe za razporejanje virov projekta.</span><span class="sxs-lookup"><span data-stu-id="df49a-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="df49a-106">Procesi pripomorejo tudi k izboljšanju učinkovitosti, ker se informacije o virih koledarja vnaprej sinhronizirajo.</span><span class="sxs-lookup"><span data-stu-id="df49a-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="df49a-107">Zato se posodobitve informacij o razporejanju virov pojavijo hitreje.</span><span class="sxs-lookup"><span data-stu-id="df49a-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="df49a-108">Priporočamo, da procese razporedite kot paket, namesto enega po enega.</span><span class="sxs-lookup"><span data-stu-id="df49a-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="df49a-109">V nasprotnem primeru obstaja nevarnost, da bo kdo pozabil vključujoče datume, ko so bile informacije nazadnje sinhronizirane.</span><span class="sxs-lookup"><span data-stu-id="df49a-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="df49a-110">Če se ne uporabljajo vključujoči datumi, lahko med sinhronizacijo datumov pride do vrzeli.</span><span class="sxs-lookup"><span data-stu-id="df49a-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sinhronizacija koledarja](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="df49a-112">Sinhronizacija zbiranj zmogljivosti vira</span><span class="sxs-lookup"><span data-stu-id="df49a-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="df49a-113">Proces sinhronizacije je zasnovan za sinhronizacijo vseh informacij koledarja virov.</span><span class="sxs-lookup"><span data-stu-id="df49a-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="df49a-114">Te informacije vključujejo informacije osnovnega koledarja o vseh spremembah tabele zmogljivosti koledarja virov projekta.</span><span class="sxs-lookup"><span data-stu-id="df49a-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="df49a-115">Če so v projekt dodani novi viri, sinhronizacija pomaga zagotoviti, da so na voljo posodobljene informacije koledarja.</span><span class="sxs-lookup"><span data-stu-id="df49a-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="df49a-116">To sinhronizacijo lahko izvedete kadar koli.</span><span class="sxs-lookup"><span data-stu-id="df49a-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="df49a-117">Priporočamo uporabo paketa.</span><span class="sxs-lookup"><span data-stu-id="df49a-117">We recommend that you use a batch.</span></span> <span data-ttu-id="df49a-118">Možnosti so na voljo med sinhronizacijo rezervacij zmogljivosti.</span><span class="sxs-lookup"><span data-stu-id="df49a-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="df49a-119">Izberite **Vodenje projektov in računovodstvo** &gt; **Redno** &gt; **Sinhronizacija zmogljivosti** &gt; **Sinhronizacija zbiranj zmogljivosti vira**.</span><span class="sxs-lookup"><span data-stu-id="df49a-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="df49a-120">Nastavite možnosti v naslednji tabeli.</span><span class="sxs-lookup"><span data-stu-id="df49a-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="df49a-121">Možnost</span><span class="sxs-lookup"><span data-stu-id="df49a-121">Option</span></span>      | <span data-ttu-id="df49a-122">Opis</span><span class="sxs-lookup"><span data-stu-id="df49a-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="df49a-123">Koda obdobja</span><span class="sxs-lookup"><span data-stu-id="df49a-123">Period code</span></span> | <span data-ttu-id="df49a-124">Izbirno izberite kodo intervala datuma glavne knjige, da nastavite začetni in končni datum za proces sinhronizacije za zbiranja zmogljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="df49a-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="df49a-125">Začetni datum</span><span class="sxs-lookup"><span data-stu-id="df49a-125">Start date</span></span>  | <span data-ttu-id="df49a-126">Vnesite začetni datum za proces sinhronizacije za zbiranja zmogljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="df49a-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="df49a-127">Končni datum</span><span class="sxs-lookup"><span data-stu-id="df49a-127">End date</span></span>    | <span data-ttu-id="df49a-128">Vnesite končni datum za proces sinhronizacije za zbiranja zmogljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="df49a-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="df49a-129">[![Proces sinhronizacije](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="df49a-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
