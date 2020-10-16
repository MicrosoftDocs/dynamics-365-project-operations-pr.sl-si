---
title: Zapiranje ponudb
description: Ta tema vsebuje informacije o zapiranju ponudbe v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896211"
---
# <a name="close-quotes"></a><span data-ttu-id="1c476-103">Zapiranje ponudb</span><span class="sxs-lookup"><span data-stu-id="1c476-103">Close quotes</span></span> 

<span data-ttu-id="1c476-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="1c476-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1c476-105">Ponudbo projekta lahko zaprete kot »Pridobljena« ali »Izgubljena«.</span><span class="sxs-lookup"><span data-stu-id="1c476-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="1c476-106">Ker postopka za aktiviranje in pregledovanje nista na voljo v storitvi Microsoft Dynamics 365 Project Operations, lahko zaprete osnutek ponudbe.</span><span class="sxs-lookup"><span data-stu-id="1c476-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="1c476-107">Zapiranje ponudbe kot »Pridobljena«</span><span class="sxs-lookup"><span data-stu-id="1c476-107">Close a quote as Won</span></span>

<span data-ttu-id="1c476-108">Če zaprete ponudbo za projekt kot »Pridobljena«, bo stanje ponudbe nastavljeno na »Zaprto« in razlog stanja na »Pridobljena«.</span><span class="sxs-lookup"><span data-stu-id="1c476-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="1c476-109">Ko ponudbo zaprete, je ponudba projekta na voljo samo za branje, ustvari pa se osnutek pogodbe o projektu, ki vsebuje informacije o ponudbah.</span><span class="sxs-lookup"><span data-stu-id="1c476-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="1c476-110">Ker zaprte ponudbe ni mogoče znova odpreti, se pred potrditvijo sprememb pojavi potrditveno pogovorno okno, saj zaprte ponudbe ni mogoče znova odpreti in sprememb ni mogoče razveljaviti.</span><span class="sxs-lookup"><span data-stu-id="1c476-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="1c476-111">Če je ponudba priložena priložnosti, se vse druge ponudbe projekta za priložnost samodejno zaprejo kot izgubljene.</span><span class="sxs-lookup"><span data-stu-id="1c476-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="1c476-112">Finančni vpliv zapiranja ponudbe kot pridobljene</span><span class="sxs-lookup"><span data-stu-id="1c476-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="1c476-113">Če so bile zabeležene dejanske vrednosti za čas, ko je še bil projekt še vedno priložen osnutku ponudbe, se zabeleži le znesek časa ali stroška.</span><span class="sxs-lookup"><span data-stu-id="1c476-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="1c476-114">Ko je ponudba zaprta kot »Pridobljena«, bo aplikacija refaktorirala stroške tako, da bo razveljavila starejše dejanske stroške in ponovno ustvarila nove dejanske stroške.</span><span class="sxs-lookup"><span data-stu-id="1c476-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="1c476-115">Aplikacija bo te dejanske stroške obdelala na podlagi metode obračunavanja v povezani vrstici pogodbe o projektu.</span><span class="sxs-lookup"><span data-stu-id="1c476-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="1c476-116">Če se dejanski stroški sklicujejo na časovno in materialno vrstico pogodbe, bo sistem samodejno ustvaril ustrezne dejanske nezaračunane zneske prodaje, ko se ponudba zapre in se ustvari pogodba o projektu.</span><span class="sxs-lookup"><span data-stu-id="1c476-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="1c476-117">Če se dejanski stroški sklicujejo na podrobnost pogodbe s fiksno ceno, bo aplikacija zaustavila ponovno obdelavo dejanskih stroškov na podlagi pravil za izstavitev računa za delitev za stranke v pogodbi o projektu.</span><span class="sxs-lookup"><span data-stu-id="1c476-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="1c476-118">Zapiranje ponudbe kot izgubljene:</span><span class="sxs-lookup"><span data-stu-id="1c476-118">Closing a quote as lost:</span></span>

<span data-ttu-id="1c476-119">Če zaprete ponudbo za projekt kot »Izgubljena«, bo stanje nastavljeno na »Zaprto« in razlog stanja na »Izgubljena«.</span><span class="sxs-lookup"><span data-stu-id="1c476-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="1c476-120">Ko ponudbo zaprete, je ponudba projekta na voljo samo za branje.</span><span class="sxs-lookup"><span data-stu-id="1c476-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="1c476-121">Ker zaprte ponudbe ni mogoče znova odpreti, bo potrditveno okno potrdilo vaše spremembe, preden ponudbo zaprete.</span><span class="sxs-lookup"><span data-stu-id="1c476-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="1c476-122">Če se ponudba projekta, ki je zaprta kot »Izgubljena«, v kateri koli vrstici sklicuje na projekt, je tudi ta projekt označen kot zaprt in vse rezervacije virov od tistega dne dalje so preklicane.</span><span class="sxs-lookup"><span data-stu-id="1c476-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="1c476-123">V aplikaciji Project Operations zapiranje ponudbe kot pridobljene ali izgubljene ne bo vplivalo na to stanje priložnosti, ki bo ostalo odprto, dokler se ne zapre ročno.</span><span class="sxs-lookup"><span data-stu-id="1c476-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
