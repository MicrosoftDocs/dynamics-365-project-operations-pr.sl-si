---
title: Potrditev projektne pogodbe
description: Ta tema vsebuje informacije o tem, kako se v aplikaciji Project Operations potrdi pogodbo.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128304"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="ba1c5-103">Potrditev projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="ba1c5-103">Confirm a project contract</span></span>

<span data-ttu-id="ba1c5-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="ba1c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ba1c5-105">V aplikacij Dynamics 365 Project Operations je projektna pogodba lahko dejavna z razlogom stanja **Potrjeno** ali zaprta z razlogom stanja **Izgubljeno**.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="ba1c5-106">Če potrdite projektno pogodbo, se stanje **Osnutek** posodobi na **Aktivno** , razlog stanja pa je možnost **Potrjeno**.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="ba1c5-107">Dejavne ali zaprte pogodbe ni mogoče urejati ali znova odpirati.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="ba1c5-108">Finančni vpliv potrditve projektne pogodbe</span><span class="sxs-lookup"><span data-stu-id="ba1c5-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="ba1c5-109">Ko je projektna pogodba potrjena, bo aplikacija znova izračunala stroške tako, da bo stornirala starejše dejanske vrednosti stroškov in ustvarila nove.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="ba1c5-110">Nove dejanske vrednosti stroškov bodo nato obdelane na podlagi metode obračunavanja v povezani podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="ba1c5-111">Če se dejanske vrednosti stroškov sklicujejo na podrobnost pogodbe »Čas in material«, se v aplikaciji samodejno znova ustvarijo pripadajoče dejanske vrednosti neobračunane prodaje.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="ba1c5-112">Če se dejanske vrednosti stroškov sklicujejo na podrobnost pogodbe s fiksno ceno, se v aplikaciji njihova obdelava ustavi.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="ba1c5-113">Omejitve, ki se jih ne sme preseči, nastavitve zaračunljivosti ter cene in stroški dejanskih vrednosti so ocenjeni in nato posodobljeni kot del postopka potrditve.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="ba1c5-114">Zapiranje projektne pogodbe kot izgubljene</span><span class="sxs-lookup"><span data-stu-id="ba1c5-114">Close a project contract as lost</span></span>

<span data-ttu-id="ba1c5-115">Ko projektno pogodbo zaprete kot izgubljeno, se stanje pogodbe posodobi na **Zaprto**, razlog stanja pa je **Izgubljeno**.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="ba1c5-116">Projektna pogodba postane na voljo samo za branje.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-116">The project contract becomes read-only.</span></span> <span data-ttu-id="ba1c5-117">Pred dokončanjem sprememb se pojavi pogovorno okno za potrditev, saj zaprte projektne pogodbe ni mogoče znova odpreti.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="ba1c5-118">Če se projektna pogodba, ki je zaprta kot izgubljena, v svojih vrsticah sklicuje na projekt, je tudi ta projekt označen kot zaprt.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="ba1c5-119">Vse rezervacije virov od tega dne naprej so preklicane.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="ba1c5-120">Vse neobračunane dejanske vrednosti prodaje v projektni pogodbi, ki še niso na računu, bodo stornirane.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="ba1c5-121">Zapiranje projektne pogodbe v programu Dynamics 365 Project Operations kot izgubljene, ne bo vplivalo na stanje z njo povezane priložnosti.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="ba1c5-122">Priložnost ostane odprta in jo je treba ročno zapreti.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-122">The opportunity will remain open and must be manually closed.</span></span>
