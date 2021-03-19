---
title: Opombe za razvijalce za odobritve
description: V tej temi so na voljo dodatne informacije o delu z odobritvami.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290289"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="387b8-103">Opombe za razvijalce za odobritve</span><span class="sxs-lookup"><span data-stu-id="387b8-103">Developer notes for Approvals</span></span>

<span data-ttu-id="387b8-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="387b8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="387b8-105">Aplikacija Dynamics 365 Project Operations vključuje logiko preverjanja veljavnosti, ki zagotavlja pravilen prehod zapisov po stopnjah odobritev.</span><span class="sxs-lookup"><span data-stu-id="387b8-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="387b8-106">Pravilni prehodi zapisov zagotavljajo:</span><span class="sxs-lookup"><span data-stu-id="387b8-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="387b8-107">Vse podporne vrstice so ustvarjene v povezanih tabelah, kot so dnevniki in dejanske vrednosti.</span><span class="sxs-lookup"><span data-stu-id="387b8-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="387b8-108">Odobritelj je označen kot **Odobritelj projekta** v projektu pred nadaljevanjem.</span><span class="sxs-lookup"><span data-stu-id="387b8-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]