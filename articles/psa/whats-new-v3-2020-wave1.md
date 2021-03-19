---
title: Novosti ali spremembe v storitvi Project Service Automation različice 3.x, 1. faza za leto 2020
description: V tej temi so na voljo informacije o novostih in spremembah v storitvi Project Service Automation različice 3, 1. faza za leto 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fef9cb62e989c693c8b3d00cb15441c284f66554
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280193"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="87b6c-103">Novosti ali spremembe v storitvi Project Service Automation različice 3, 1. faza za leto 2020</span><span class="sxs-lookup"><span data-stu-id="87b6c-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="87b6c-104">V tej temi so izpostavljeni ključni vidiki nadgradnje pri posodobitvi na zadnjo izdajo storitve Project Service Automation (PSA) različice 3.x, 1. faza za leto 2020.</span><span class="sxs-lookup"><span data-stu-id="87b6c-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="87b6c-105">Časovni vnos</span><span class="sxs-lookup"><span data-stu-id="87b6c-105">Time entry</span></span>
<span data-ttu-id="87b6c-106">Izkušnja časovnih vnosov je bila razširjena, da omogoča zmogljivosti za razširitev časovnega vnosa v več scenarijev stranke.</span><span class="sxs-lookup"><span data-stu-id="87b6c-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="87b6c-107">To vključuje zmogljivost za dodajanje vrst vnosov, ki zdaj spodbujajo specifično vedenje na podlagi imena sheme polja **Nastavitve časovnega vnosa**, prikazanega kot **Časovni vir**.</span><span class="sxs-lookup"><span data-stu-id="87b6c-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="87b6c-108">V podporo tej funkciji je bila dodana nova rešitev, imenovana TESA (angl. Time, Expense, Statusing, and Approvals – čas, stroški, stanje in odobritve).</span><span class="sxs-lookup"><span data-stu-id="87b6c-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="87b6c-109">Vidik nadgradnje</span><span class="sxs-lookup"><span data-stu-id="87b6c-109">Upgrade consideration</span></span>
<span data-ttu-id="87b6c-110">Za podporo te funkcionalnosti so bile vloge znotraj storitve PSA posodobljene, da vključujejo nove pravice.</span><span class="sxs-lookup"><span data-stu-id="87b6c-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="87b6c-111">Te pravice podeljujejo dostop za branje novi entiteti **Nastavitve časovnega vnosa**.</span><span class="sxs-lookup"><span data-stu-id="87b6c-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="87b6c-112">Uporabnikom, ki potrebujejo zmogljivost beleženja časa, bi morala biti dodeljena uporabniška vloga **Uporabnik časovnega vnosa** poleg obstoječih vlog.</span><span class="sxs-lookup"><span data-stu-id="87b6c-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="87b6c-113">Ta vloga vključuje novo funkcionalnost in zagotavlja, da bo časovni vnos še naprej deloval.</span><span class="sxs-lookup"><span data-stu-id="87b6c-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="87b6c-114">Poleg tega velja tudi, da če imate module aplikacij po meri, ki vsebujejo vse obrazce za entiteto časovnega vnosa, boste morali iz modula odstraniti **Obrazec za hitro ustvarjanje časovnega vnosa za rešitev TESA**.</span><span class="sxs-lookup"><span data-stu-id="87b6c-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="87b6c-115">Trenutne razširjene spremembe časovnih vnosov</span><span class="sxs-lookup"><span data-stu-id="87b6c-115">Currently extended time entry changes</span></span>
<span data-ttu-id="87b6c-116">Za zmanjšanje vpliva na trenutne uporabnike časovnega vnosa je ta sprememba vloge edina bistvena zahteva, potrebna za nadaljevanje uporabe časovnega vnosa.</span><span class="sxs-lookup"><span data-stu-id="87b6c-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="87b6c-117">Če ste ustvarili poglede po meri ali ločene izkušnje časovnega vnosa, morate nastaviti polja **Nastavitev časovnega vnosa** na pravilno vrednost PSA.</span><span class="sxs-lookup"><span data-stu-id="87b6c-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]