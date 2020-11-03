---
title: Zapiranje ponudbe
description: Ta tema vsebuje informacije o zapiranju ponudb v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c429fa14b4b95420c67a91a6a59af7db2660f68
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084654"
---
# <a name="close-a-quote"></a><span data-ttu-id="1c962-103">Zapiranje ponudbe</span><span class="sxs-lookup"><span data-stu-id="1c962-103">Close a quote</span></span>

<span data-ttu-id="1c962-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="1c962-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1c962-105">Ponudbo projekta lahko zaprete kot »Pridobljena« ali »Izgubljena«.</span><span class="sxs-lookup"><span data-stu-id="1c962-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="1c962-106">Ker funkciji za aktiviranje in pregledovanje nista na voljo za ponudbe v storitvi Microsoft Dynamics 365 Project Operations, lahko zaprete osnutek ponudbe.</span><span class="sxs-lookup"><span data-stu-id="1c962-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="1c962-107">Zapiranje ponudbe kot »Pridobljena«</span><span class="sxs-lookup"><span data-stu-id="1c962-107">Close a quote as Won</span></span>

<span data-ttu-id="1c962-108">Če zaprete ponudbo za projekt kot »Pridobljena«, bo stanje ponudbe nastavljeno na **Zaprto** in razlog stanja na **Pridobljena**.</span><span class="sxs-lookup"><span data-stu-id="1c962-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="1c962-109">Ko ponudbo zaprete, je na voljo samo za branje, ustvari pa se osnutek pogodbe o projektu z vsemi informacijami o ponudbah.</span><span class="sxs-lookup"><span data-stu-id="1c962-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="1c962-110">Ker zaprte ponudbe ni mogoče znova odpreti, bo potrditveno okno potrdilo vaše spremembe, preden ponudbo zaprete.</span><span class="sxs-lookup"><span data-stu-id="1c962-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="1c962-111">Pogodba o projektu, izdelana na podlagi ponudbe za projekt, je na voljo tudi v modulu za vodenje projektov in računovodstvo aplikacije Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1c962-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="1c962-112">Če pogodba o projektu ni preslikana v projekt v nobeni od njegovih vrstic, je ta pogodba o projektu na voljo kot nedejavna pogodba o projektu in začne veljati takoj, ko se projekt preslika v vsaj eno od njegovih podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="1c962-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="1c962-113">Če je ponudba priložena priložnosti, se vse druge ponudbe projekta za priložnost samodejno zaprejo kot izgubljene.</span><span class="sxs-lookup"><span data-stu-id="1c962-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="1c962-114">Finančni vpliv zapiranja ponudbe kot pridobljene</span><span class="sxs-lookup"><span data-stu-id="1c962-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="1c962-115">Če so bile zabeležene dejanske vrednosti za čas, ko je še bil projekt še vedno priložen osnutku ponudbe, se zabeleži le znesek časa ali stroška.</span><span class="sxs-lookup"><span data-stu-id="1c962-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="1c962-116">Ko je ponudba zaprta kot »Pridobljena«, bo aplikacija refaktorirala stroške tako, da bo razveljavila starejše dejanske stroške in ponovno ustvarila nove dejanske stroške.</span><span class="sxs-lookup"><span data-stu-id="1c962-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="1c962-117">Aplikacija bo te dejanske stroške obdelala na podlagi metode obračunavanja v povezani vrstici pogodbe o projektu.</span><span class="sxs-lookup"><span data-stu-id="1c962-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="1c962-118">Če se dejanski stroški sklicujejo na časovno in materialno vrstico pogodbe, bo sistem samodejno ustvaril ustrezne dejanske nezaračunane zneske prodaje, ko se ponudba zapre in se ustvari pogodba o projektu.</span><span class="sxs-lookup"><span data-stu-id="1c962-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="1c962-119">Če se dejanski stroški sklicujejo na podrobnost pogodbe s fiksno ceno, bo aplikacija zaustavila ponovno obdelavo dejanskih stroškov na podlagi pravil za izstavitev računa za delitev za stranke v pogodbi o projektu.</span><span class="sxs-lookup"><span data-stu-id="1c962-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="1c962-120">Vsi predelani dejanski podatki so na voljo v modulu za vodenje projektov in računovodstvo, ki ga lahko računovodja projekta pregleda, posodobi in objavi v glavni knjigi.</span><span class="sxs-lookup"><span data-stu-id="1c962-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="1c962-121">Zapiranje ponudbe kot »Izgubljena«</span><span class="sxs-lookup"><span data-stu-id="1c962-121">Close a quote as Lost</span></span>

<span data-ttu-id="1c962-122">Če zaprete ponudbo za projekt kot »Izgubljena«, bo stanje nastavljeno na **Zaprto** in razlog stanja na **Izgubljena**.</span><span class="sxs-lookup"><span data-stu-id="1c962-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="1c962-123">Ko ponudbo zaprete, je na voljo samo za branje.</span><span class="sxs-lookup"><span data-stu-id="1c962-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="1c962-124">Ker zaprte ponudbe ni mogoče znova odpreti, bo potrditveno okno potrdilo vaše spremembe, preden ponudbo zaprete.</span><span class="sxs-lookup"><span data-stu-id="1c962-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="1c962-125">Če se ponudba projekta, ki je zaprta kot »Izgubljena«, v kateri koli vrstici sklicuje na projekt, je tudi ta projekt označen kot zaprt in vse rezervacije virov od tistega dne dalje so preklicane.</span><span class="sxs-lookup"><span data-stu-id="1c962-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="1c962-126">V aplikaciji Project Operations zapiranje ponudbe kot pridobljene ali izgubljene ne bo vplivalo na to stanje priložnosti, ki bo ostalo odprto, dokler se ne zapre ročno.</span><span class="sxs-lookup"><span data-stu-id="1c962-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
