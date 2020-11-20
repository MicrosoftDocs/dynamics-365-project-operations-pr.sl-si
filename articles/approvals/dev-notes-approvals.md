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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483968"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="09e66-103">Opombe za razvijalce za odobritve</span><span class="sxs-lookup"><span data-stu-id="09e66-103">Developer notes for Approvals</span></span>

<span data-ttu-id="09e66-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="09e66-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="09e66-105">Dynamics 365 Project Operations vključuje logiko preverjanja veljavnosti, ki zagotavlja pravilen prehod zapisov po stopnjah odobritev.</span><span class="sxs-lookup"><span data-stu-id="09e66-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="09e66-106">Pravilni prehodi zapisov zagotavljajo:</span><span class="sxs-lookup"><span data-stu-id="09e66-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="09e66-107">Vse podporne vrstice so ustvarjene v povezanih tabelah, kot so dnevniki in dejanske vrednosti.</span><span class="sxs-lookup"><span data-stu-id="09e66-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="09e66-108">Odobritelj je označen kot **Odobritelj projekta** v projektu pred nadaljevanjem.</span><span class="sxs-lookup"><span data-stu-id="09e66-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
