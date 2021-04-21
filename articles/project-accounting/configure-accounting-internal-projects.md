---
title: Konfiguracija vodenja računov za interne projekte
description: Ta tema vsebuje informacije o nastavitvah računovodskih postopkov za interne projekte v aplikaciji Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857998"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="8a9e6-103">Konfiguracija vodenja računov za interne projekte</span><span class="sxs-lookup"><span data-stu-id="8a9e6-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="8a9e6-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="8a9e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8a9e6-105">Interni projekti podjetjem omogočajo sledenje stroškom, povezanih z dejavnostmi, ki niso obračunane za stranko.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="8a9e6-106">Primeri internih projektov so:</span><span class="sxs-lookup"><span data-stu-id="8a9e6-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="8a9e6-107">Razvijanje izdelka, kot je mobilna aplikacija, in sledenje stroškom, ki so povezani z razvojem.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="8a9e6-108">Upravljanje časa in stroškov pred prodajo</span><span class="sxs-lookup"><span data-stu-id="8a9e6-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="8a9e6-109">Ta interni predprodajni projekt je v primeru pridobljene ponudbe mogoče pozneje pretvoriti v projekt, ki ga je mogoče obračunati.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="8a9e6-110">Vsak projekt, ki ni povezan s pogodbo v aplikaciji Dynamics 365 Project Operations, se obravnava kot notranji.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="8a9e6-111">Profili stroškov in prihodkov podjetja se ne uporabljajo za določanje računovodskih pravil za projekt.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="8a9e6-112">Stroški internega projekta se vedno knjižijo po načelih dobička in izgube.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="8a9e6-113">Računi glavne knjige za vknjižbe so opredeljeni na strani **z nastavitvami vnašanja v glavno knjigo**.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="8a9e6-114">Časovne transakcije so knjižene v breme na računu **Stroški** in v dobro na računu **Dodelitev plače**.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="8a9e6-115">Stroškovne transakcije so knjižene v breme na računu **Stroški** in v dobro na računu **Protikonto za stroške**.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="8a9e6-116">Transakcije postavk se knjižijo z obremenitvijo računa **Stroški** in kreditiranjem računa **Stroški – postavka**.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="8a9e6-117">Potem ko so transakcije vknjižene za projekt in če je projekt povezan s projektno pogodbo, sistem stornira vse zbrane transakcije in ustvari nove transakcije, ki jih je mogoče obračunati.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="8a9e6-118">Transakcije, ki jih je mogoče obračunati, sledijo računovodskim pravilom, opredeljenim v ustreznem profilu stroškov in prihodkov projekta.</span><span class="sxs-lookup"><span data-stu-id="8a9e6-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
