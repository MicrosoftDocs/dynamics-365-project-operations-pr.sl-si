---
title: Zahtevani pogoji za začasne rezervacije
description: Ta tema vsebuje informacije o tem, kako začasno rezervirati zahtevane pogoje.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 861e484ea2fc251e0082b4cb0cd5409a45a74057
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084966"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="bcd22-103">Zahtevani pogoji za začasne rezervacije</span><span class="sxs-lookup"><span data-stu-id="bcd22-103">Soft-book requirements</span></span>

<span data-ttu-id="bcd22-104">Rezervacije zahtevanih pogojev za vir je mogoče potrditi.</span><span class="sxs-lookup"><span data-stu-id="bcd22-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="bcd22-105">S potrjeno rezervacijo ustvarite predlog, ki porabi del zmogljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="bcd22-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="bcd22-106">Predlog se nato pošlje nazaj prosilcu za odobritev.</span><span class="sxs-lookup"><span data-stu-id="bcd22-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="bcd22-107">Začasna rezervacija pogojno doda vir v projektno ekipo in ima drugačno stanje na plošči razporeda, vendar ne porabi zmogljivosti vira.</span><span class="sxs-lookup"><span data-stu-id="bcd22-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="bcd22-108">Če želite vir s plošče razporeda začasno rezervirati, nastavite polje **Stanje rezervacije** na **Začasno**.</span><span class="sxs-lookup"><span data-stu-id="bcd22-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Stanje rezervacije je nastavljeno na »Začasno«](media/Resource-Management-image77.png)

<span data-ttu-id="bcd22-110">Ko je zavihek **Ekipa** v pogledu **Poimenovani člani ekipe** , se tam prikaže tudi vir.</span><span class="sxs-lookup"><span data-stu-id="bcd22-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="bcd22-111">Začasno rezervirane ure so zabeležene v stolpcu **Začasno rezervirane ure**.</span><span class="sxs-lookup"><span data-stu-id="bcd22-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Začasno rezervirane ure v pogledu »Poimenovani člani ekipe«](media/Resource-Management-image78.png)

<span data-ttu-id="bcd22-113">Začasno rezervirane člane ekipe je mogoče dodeliti opravilom.</span><span class="sxs-lookup"><span data-stu-id="bcd22-113">Soft-booked team members can be assigned to tasks.</span></span>

![Začasno rezerviran član ekipe, ki je dodeljen opravilu](media/Resource-Management-image79.png)

<span data-ttu-id="bcd22-115">V zavihku **Usklajevanje** ni prikazana nobena začasna rezervacija vira, saj zavihek **Usklajevanje** upošteva samo potrjene rezervacije.</span><span class="sxs-lookup"><span data-stu-id="bcd22-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Začasno rezerviran vir brez rezervacij v zavihku »Usklajevanje«](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="bcd22-117">Vira ni mogoče začasno rezervirati na podlagi zahtevanega pogoja, ustvarjenega na podlagi splošnega člana ekipe.</span><span class="sxs-lookup"><span data-stu-id="bcd22-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="bcd22-118">Na plošči razporeda je za začasne rezervacije za vir uporabljena drugačna barva.</span><span class="sxs-lookup"><span data-stu-id="bcd22-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Začasne rezervacije na plošči razporeda](media/Resource-Management-image81.png)

<span data-ttu-id="bcd22-120">Če želite pretvoriti začasno rezervacijo v potrjeno rezervacijo, na plošči razporeda z desno tipko miške kliknite začasno rezervacijo in izberite možnost **Spremeni stanje** \> **Potrjena rezervacija** \> **Potrjeno**.</span><span class="sxs-lookup"><span data-stu-id="bcd22-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Spreminjanje stanja rezervacije na »Potrjeno«](media/Resource-Management-image82.png)

<span data-ttu-id="bcd22-122">Na plošči razporeda se spremeni tako rezervacija kot stanje.</span><span class="sxs-lookup"><span data-stu-id="bcd22-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="bcd22-123">Ker se je stanje rezervacije spremenilo na **Potrjeno** , se vir prikaže kot rezerviran, njegova zmogljivost in razpoložljivost pa sta prilagojeni.</span><span class="sxs-lookup"><span data-stu-id="bcd22-123">Because the booking status is now **Hard** , the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="bcd22-124">Na enak način lahko tudi prekličete potrjeno ali začasno rezervacijo na plošči razporeda.</span><span class="sxs-lookup"><span data-stu-id="bcd22-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="bcd22-125">Če želite pretvoriti vir z začasno rezervacijo na potrjeno rezervacijo v zavihku **Ekipa** , izberite vir in nato še možnost **Potrdi**.</span><span class="sxs-lookup"><span data-stu-id="bcd22-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Potrdi ukaz](media/Resource-Management-image83.png)
