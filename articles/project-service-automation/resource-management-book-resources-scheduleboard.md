---
title: Uporaba plošče razporeda za rezervacijo projektnih virov
description: Ta tema vsebuje informacije o postopku rezervacije virov.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 169f7b98-119b-4aa2-b121-c73c0396fcde
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: b377e0c80b2c4eb5028f131620213ea534a1a4dc
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755849"
---
# <a name="use-the-schedule-board-to-book-project-resources"></a><span data-ttu-id="d3eb1-103">Uporaba plošče razporeda za rezervacijo projektnih virov</span><span class="sxs-lookup"><span data-stu-id="d3eb1-103">Use the Schedule Board to book project resources</span></span>

<span data-ttu-id="d3eb1-104">Poleg tega, da lahko vire za projekt rezervirate v samem projektu, lahko začasne in potrjene rezervacije opravite tudi na plošči razporeda.</span><span class="sxs-lookup"><span data-stu-id="d3eb1-104">In addition to booking resources on a project from within a project, you can hard-book or soft-book resources from the Schedule Board.</span></span>

<span data-ttu-id="d3eb1-105">Preden lahko opravite rezervacijo na plošči razporeda, morate ustvariti ali generirati zahtevane pogoje za vir.</span><span class="sxs-lookup"><span data-stu-id="d3eb1-105">Before you can book from the Schedule Board, you must create or generate resource requirements.</span></span> <span data-ttu-id="d3eb1-106">Če želite ustvariti zahtevane pogoje za vir na plošči razporeda, upoštevajte te korake:</span><span class="sxs-lookup"><span data-stu-id="d3eb1-106">Follow these steps to create resource requirements from the Schedule Board.</span></span>

1. <span data-ttu-id="d3eb1-107">Če je podokno **Zahtevani pogoji za rezervacijo** na dnu strani strnjeno, izberite kontrolnik za razširitev, da ga razširite.</span><span class="sxs-lookup"><span data-stu-id="d3eb1-107">If the **Booking Requirements** pane at the bottom of the page is collapsed, select the expander control to expand it.</span></span>
2. <span data-ttu-id="d3eb1-108">Izberite zahtevo za rezervacijo v podoknu **Zahtevani pogoji za rezervacijo** na zavihku **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="d3eb1-108">In the **Booking Requirements** pane, on the **Project** tab, select the requirement to book.</span></span>

    ![Zahtevani pogoj, izbran na zavihku »Projekt«](media/Resource-Management-image73.png)

3. <span data-ttu-id="d3eb1-110">Izberite **Poišči razpoložljivost**, če želite filtrirati vire, ki jih je mogoče rezervirati, in si ogledati razpoložljive vire.</span><span class="sxs-lookup"><span data-stu-id="d3eb1-110">Select **Find Availability** to filter the bookable resources and view the available resources.</span></span> 
4. <span data-ttu-id="d3eb1-111">Izberite enega ali več virov s plošče razporeda.</span><span class="sxs-lookup"><span data-stu-id="d3eb1-111">Select one or more resources from the Schedule Board.</span></span> 
5. <span data-ttu-id="d3eb1-112">V podoknu **Ustvarjanje rezervacije vira** na desni strani strani vnesite informacije o rezervaciji in nato izberite možnost **Rezerviraj in zapri**.</span><span class="sxs-lookup"><span data-stu-id="d3eb1-112">In the **Create Resource Booking** pane on the right side of the page, enter the booking information, and then select **Book and exit**.</span></span>

    ![Podokno »Ustvarjanje rezervacije vira« za izbrani vir, ki ga je mogoče rezervirati](media/Resource-Management-image74.png)

6. <span data-ttu-id="d3eb1-114">Ko je v podoknu **Ustvarjanje rezervacije vira** izbrana zahteva, izberite eno ali več celic vira, da ustvarite rezervacijo.</span><span class="sxs-lookup"><span data-stu-id="d3eb1-114">While the requirement is selected in the **Create Resource Booking** pane, select one or more cells of a resource to create the booking.</span></span>

    ![Izbira več celic hkrati za posamezen vir](media/Resource-Management-image75.png)

7. <span data-ttu-id="d3eb1-116">Izberite možnost **Rezerviraj**</span><span class="sxs-lookup"><span data-stu-id="d3eb1-116">Select **Book**.</span></span>

<span data-ttu-id="d3eb1-117">Z uporabo izbranega vira je zahteva izpolnjena.</span><span class="sxs-lookup"><span data-stu-id="d3eb1-117">The requirement is fulfilled by using the selected resource.</span></span> <span data-ttu-id="d3eb1-118">V podoknu **Zahteve za rezervacijo** se bo pojavilo obvestilo, da je bila zahteva posodobljena, vir pa bo prikazan kot rezerviran za ta projekt.</span><span class="sxs-lookup"><span data-stu-id="d3eb1-118">In the **Booking Requirements** pane, notice that the requirement has been updated, and the resource is shown as booked on the project.</span></span>

![Vir, rezerviran za projekt](media/Resource-Management-image76.png)
