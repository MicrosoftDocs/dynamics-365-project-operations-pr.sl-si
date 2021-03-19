---
title: Razumevanje stanja projekta
description: Ta tema vsebuje informacije o stanju, ki je dodeljen projektom v aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286493"
---
# <a name="understand-project-status"></a><span data-ttu-id="576a2-103">Razumevanje stanja projekta</span><span class="sxs-lookup"><span data-stu-id="576a2-103">Understand project status</span></span>

<span data-ttu-id="576a2-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="576a2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="576a2-105">Razdelek **Stanje** na strani **Entiteta projekta** vsebuje povzetek stanja projekta na podlagi stroškov in obsega dela.</span><span class="sxs-lookup"><span data-stu-id="576a2-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="576a2-106">Polja s povzetkom stanja</span><span class="sxs-lookup"><span data-stu-id="576a2-106">Status summary fields</span></span>

- <span data-ttu-id="576a2-107">Polje **Splošno stanje projekta** je polje, ki ga je mogoče urejati in ki prikazuje splošno stanje projekta.</span><span class="sxs-lookup"><span data-stu-id="576a2-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="576a2-108">To polje uporablja barvno kodiranje, na primer zeleno, rumeno in rdečo barvo, za označevanje naraščajočega tveganja.</span><span class="sxs-lookup"><span data-stu-id="576a2-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="576a2-109">Polje **Komentarji** omogoča vodji projekta, da vnese določene komentarje o stanju.</span><span class="sxs-lookup"><span data-stu-id="576a2-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="576a2-110">Polja **Stanje posodobljeno dne** ni mogoče urejati.</span><span class="sxs-lookup"><span data-stu-id="576a2-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="576a2-111">Vrednost v tem polju je časovni žig, ki označuje, kdaj je bilo stanje nazadnje posodobljeno.</span><span class="sxs-lookup"><span data-stu-id="576a2-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="576a2-112">Polji **Učinkovitost razporeda** in **Stroškovna učinkovitost** sta nastavljeni iz mreže za sledenje.</span><span class="sxs-lookup"><span data-stu-id="576a2-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="576a2-113">Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče v pogledu **Sledenje obsegu dela** pozitivni, sta polji posodobljeni na **Pred**.</span><span class="sxs-lookup"><span data-stu-id="576a2-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="576a2-114">Če sta vrednosti odmika od razporeda in stroškov za korensko vozlišče negativni, sta ti polji nastavljeni na **Za**.</span><span class="sxs-lookup"><span data-stu-id="576a2-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]