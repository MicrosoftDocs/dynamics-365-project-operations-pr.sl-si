---
title: Zapiranje ponudbe – poenostavljeno
description: Ta tema vsebuje informacije o zapiranju ponudbe v aplikaciji Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994156"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="c60aa-103">Zapiranje ponudbe – poenostavljeno</span><span class="sxs-lookup"><span data-stu-id="c60aa-103">Close a quote - lite</span></span>

<span data-ttu-id="c60aa-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="c60aa-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c60aa-105">Ponudbo projekta lahko zaprete kot »Pridobljena« ali »Izgubljena«.</span><span class="sxs-lookup"><span data-stu-id="c60aa-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="c60aa-106">Osnutek ponudbe lahko zaprete, ker postopka za aktiviranje in pregled ponudb nista podprta v aplikaciji Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c60aa-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="c60aa-107">Zapiranje ponudbe kot »Pridobljena«</span><span class="sxs-lookup"><span data-stu-id="c60aa-107">Close a quote as Won</span></span>

<span data-ttu-id="c60aa-108">Ko projektno ponudbo zaprete kot »Pridobljena«, je stanje nastavljeno na »Zaprto«, razlog stanja pa je »Pridobljena«.</span><span class="sxs-lookup"><span data-stu-id="c60aa-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="c60aa-109">Ko ponudbo zaprete, je ponudba projekta na voljo samo za branje, ustvari pa se osnutek pogodbe o projektu, ki vsebuje informacije o ponudbah.</span><span class="sxs-lookup"><span data-stu-id="c60aa-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="c60aa-110">Ker zaprte ponudbe ni mogoče znova odpreti, bodo vaše spremembe potrjene s potrditvenim pogovornim oknom.</span><span class="sxs-lookup"><span data-stu-id="c60aa-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="c60aa-111">Če je ponudba priložena priložnosti, se vse druge ponudbe projekta za priložnost samodejno zaprejo kot izgubljene.</span><span class="sxs-lookup"><span data-stu-id="c60aa-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="c60aa-112">Finančni vpliv zapiranja ponudbe kot pridobljene</span><span class="sxs-lookup"><span data-stu-id="c60aa-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="c60aa-113">Če obstajajo dejanske vrednosti za čas za projekt, ko je ta še vedno povezan z osnutkom ponudbe, se beleži le strošek časa ali izdatek.</span><span class="sxs-lookup"><span data-stu-id="c60aa-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="c60aa-114">Ko je ponudba zaprta kot »Pridobljena«, bo aplikacija refaktorirala stroške tako, da bo razveljavila starejše dejanske stroške in ponovno ustvarila nove dejanske stroške.</span><span class="sxs-lookup"><span data-stu-id="c60aa-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="c60aa-115">Aplikacija bo te dejanske stroške obdelala na podlagi metode obračunavanja v povezani vrstici pogodbe o projektu.</span><span class="sxs-lookup"><span data-stu-id="c60aa-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="c60aa-116">Če se dejanske vrednosti stroškov sklicujejo na podrobnosti pogodbe za čas in material, so po zapiranju ponudbe in ustvarjanju projektne pogodbe ustvarjene ustrezne neobračunane dejanske vrednosti prodaje.</span><span class="sxs-lookup"><span data-stu-id="c60aa-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="c60aa-117">Če se dejanske vrednosti stroškov sklicujejo na podrobnosti pogodbe za fiksno ceno, bo aplikacija prenehala ponovno obdelovati dejanske vrednosti stroškov, ki temeljijo na pravilih za deljeno obračunavanje za stranke projektne pogodbe.</span><span class="sxs-lookup"><span data-stu-id="c60aa-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="c60aa-118">Zapiranje ponudbe kot izgubljene:</span><span class="sxs-lookup"><span data-stu-id="c60aa-118">Closing a quote as lost:</span></span>

<span data-ttu-id="c60aa-119">Ko projektno ponudbo zaprete kot »Izgubljena«, je stanje nastavljeno na »Zaprto«, razlog stanja pa je »Izgubljena«.</span><span class="sxs-lookup"><span data-stu-id="c60aa-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="c60aa-120">Ko ponudbo zaprete, je ponudba projekta na voljo samo za branje.</span><span class="sxs-lookup"><span data-stu-id="c60aa-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="c60aa-121">Ker zaprte ponudbe ni mogoče znova odpreti, bo potrditveno okno potrdilo vaše spremembe, preden ponudbo zaprete.</span><span class="sxs-lookup"><span data-stu-id="c60aa-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="c60aa-122">Če se projektna ponudba, ki je zaprta kot »Izgubljena«, v kateri koli podrobnosti sklicuje na projekt, bo tudi ta projekt označen kot »Zaprt«.</span><span class="sxs-lookup"><span data-stu-id="c60aa-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="c60aa-123">Vse rezervacije virov od tega dne naprej so preklicane.</span><span class="sxs-lookup"><span data-stu-id="c60aa-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="c60aa-124">V aplikaciji Project Operations zapiranje ponudbe kot pridobljene ali izgubljene ne bo vplivalo na to stanje priložnosti, ki bo ostalo odprto, dokler se ne zapre ročno.</span><span class="sxs-lookup"><span data-stu-id="c60aa-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]