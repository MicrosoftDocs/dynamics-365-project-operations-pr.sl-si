---
title: Upravljanje projektnih pogodb
description: V tej temi so na voljo informacije o ogledu pogodb, ki temeljijo na projektu.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a4357d5cf184a3c6ada3ae33631694c31bb5b00
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273232"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="c7d8a-103">Upravljanje projektnih pogodb</span><span class="sxs-lookup"><span data-stu-id="c7d8a-103">Manage project contracts</span></span>

<span data-ttu-id="c7d8a-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="c7d8a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c7d8a-105">Projektne pogodbe v storitvi Dynamics 365 Project Operations zajamejo in upravljajo pogodbeno dogovorjeno o obvezah in podrobnostih obračunavanja za projekt.</span><span class="sxs-lookup"><span data-stu-id="c7d8a-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="c7d8a-106">Struktura projektne pogodbe v storitvi Project Operations je prilagojena za delo, ki temelji na projektih, z naslednjimi komponentami:</span><span class="sxs-lookup"><span data-stu-id="c7d8a-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="c7d8a-107">Podrobnosti pogodbe, ki določajo posamezne komponente dela, ki bodo predstavljene kot komponente na visoki ravni na računu projekta.</span><span class="sxs-lookup"><span data-stu-id="c7d8a-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="c7d8a-108">Podrobnosti vrstice pogodbe, ki določajo in ocenjujejo delo za vsako komponento ali podrobnosti pogodbe na visoki ravni.</span><span class="sxs-lookup"><span data-stu-id="c7d8a-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="c7d8a-109">Ocena vključuje razpored in finančni vidiki dela so povezani s podrobnostmi pogodbe.</span><span class="sxs-lookup"><span data-stu-id="c7d8a-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="c7d8a-110">Pogodbeni modeli in plačljive komponente so nastavljeni za vsako od podrobnosti pogodbe, ki hrani dogovore za obračunavanje za vsako od podrobnosti pogodbe in splošno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="c7d8a-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="c7d8a-111">Ogled vseh pogodb, ki temeljijo na projektih</span><span class="sxs-lookup"><span data-stu-id="c7d8a-111">View all project-based contracts</span></span>

<span data-ttu-id="c7d8a-112">Seznam vseh pogodb za projekt si lahko ogledate na strani s seznamom **Pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="c7d8a-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="c7d8a-113">Odprite možnost **Prodaja** > **Pogodbe**.</span><span class="sxs-lookup"><span data-stu-id="c7d8a-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="c7d8a-114">Prikazan je seznam vseh pogodb za projekt v sistemu.</span><span class="sxs-lookup"><span data-stu-id="c7d8a-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="c7d8a-115">Izberite **Preklopnik med pogledi** (puščica spustnega seznama poleg imena pogleda) za izbiro drugih filtriranih pogledov.</span><span class="sxs-lookup"><span data-stu-id="c7d8a-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="c7d8a-116">Ustvarite lahko lastne poglede s pogoji filtra po meri.</span><span class="sxs-lookup"><span data-stu-id="c7d8a-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="c7d8a-117">Pogodbe lahko ustvarite ali izbrišete s strani s seznamom ali strani s podrobnostmi.</span><span class="sxs-lookup"><span data-stu-id="c7d8a-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]