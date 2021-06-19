---
title: Opredelitev pravilnikov o stroških
description: Opredelite lahko pravilnike o stroških, ki jih morajo vaši delavci upoštevati, ko vnašajo in predložijo poročila o stroških in zahteve za pot.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa108db9aa0d2a22c35d2d046917ddae1f3842c1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001896"
---
# <a name="define-expense-policies"></a><span data-ttu-id="dfadc-103">Opredelitev pravilnikov o stroških</span><span class="sxs-lookup"><span data-stu-id="dfadc-103">Define expense policies</span></span>

<span data-ttu-id="dfadc-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="dfadc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dfadc-105">Opredelite lahko pravilnike, ki jih morajo vaši delavci upoštevati, ko vnašajo in predložijo poročila o stroških in zahteve za pot.</span><span class="sxs-lookup"><span data-stu-id="dfadc-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="dfadc-106">Izvajanje pravilnikov o stroških vam lahko pomaga učinkovito upravljati stroške.</span><span class="sxs-lookup"><span data-stu-id="dfadc-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="dfadc-107">Tako lahko na primer nastavite pravilnik za hotelske stroške v New Yorku, ki določa, da strošek na nočitev ne sme presegati 250 USD.</span><span class="sxs-lookup"><span data-stu-id="dfadc-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="dfadc-108">Če delavec predloži poročilo o stroških ali zahtevo za pot, kjer cena sobe presega ta znesek, sistem obvesti</span><span class="sxs-lookup"><span data-stu-id="dfadc-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="dfadc-109">delavca, da je bil znesek pravilnika za strošek presežen.</span><span class="sxs-lookup"><span data-stu-id="dfadc-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="dfadc-110">Lahko konfigurirate sporočilo, ki ga bo delavec prejel, ko</span><span class="sxs-lookup"><span data-stu-id="dfadc-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="dfadc-111">opredelite pravilnik.</span><span class="sxs-lookup"><span data-stu-id="dfadc-111">define the policy.</span></span>      
        
<span data-ttu-id="dfadc-112">Opredelite lahko tri vrste pravilnikov:</span><span class="sxs-lookup"><span data-stu-id="dfadc-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="dfadc-113">**Opozorilo**: dovoli delavcu, da predloži poročilo o stroških ali zahtevo za pot, vendar bodo stroški označeni za vse odobritelje in</span><span class="sxs-lookup"><span data-stu-id="dfadc-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="dfadc-114">za poznejše poročanje.</span><span class="sxs-lookup"><span data-stu-id="dfadc-114">for later reporting.</span></span>        

- <span data-ttu-id="dfadc-115">**Napaka**: od delavca zahteva, da revidira strošek v skladu s pravilnikom, preden predloži poročilo o stroških ali zahtevo za pot.</span><span class="sxs-lookup"><span data-stu-id="dfadc-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="dfadc-116">**Utemeljitev**: zahteva, da delavec ali vodja pred predložitvijo poročila o stroških ali zahteve za pot vnese utemeljitev za preseganje zneska pravilnika.</span><span class="sxs-lookup"><span data-stu-id="dfadc-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="dfadc-117">Nasveti glede pravilnikov</span><span class="sxs-lookup"><span data-stu-id="dfadc-117">Policy tips</span></span>
<span data-ttu-id="dfadc-118">Tu je nekaj predlogov, ki vam lahko pomagajo pri ustvarjanju novih pravilnikov za upravljanje stroškov:</span><span class="sxs-lookup"><span data-stu-id="dfadc-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="dfadc-119">Pravilniki veljajo z datumom začetka veljavnosti, kar pomeni, da pravilnik ne bo začel veljati, če bo ustvarjen z datumom po datumu nastanka stroška.</span><span class="sxs-lookup"><span data-stu-id="dfadc-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="dfadc-120">Na primer, danes ustvarite nov pravilnik, s katerim uveljavite največji strošek obroka v višini 50 $.</span><span class="sxs-lookup"><span data-stu-id="dfadc-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="dfadc-121">Vsi obstoječi stroški, vneseni do včeraj, ne bodo preverjeni v skladu s tem pravilnikom.</span><span class="sxs-lookup"><span data-stu-id="dfadc-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="dfadc-122">Pri ustvarjanju pravilnika za kategorijo stroška, ki jo je mogoče razčleniti, razmislite o dodajanju pogoja za vrsto vrstice stroška.</span><span class="sxs-lookup"><span data-stu-id="dfadc-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="dfadc-123">Nekateri pravilniki, na primer zahtevanje potrdila, morda niso smiselni za razčlenjene vrstice.</span><span class="sxs-lookup"><span data-stu-id="dfadc-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="dfadc-124">V tem primeru se pravilnik uporablja samo za vrstico glave ali nerazčlenjeno vrstico.</span><span class="sxs-lookup"><span data-stu-id="dfadc-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="dfadc-125">Pravilniki upravljanja stroškov se privzeto ovrednotijo glede na izvorno entiteto.</span><span class="sxs-lookup"><span data-stu-id="dfadc-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="dfadc-126">Za medpodjetniške scenarije lahko nastavite, da se pravilnik namesto tega vrednoti glede na ciljno entiteto (entiteta izposojevalka).</span><span class="sxs-lookup"><span data-stu-id="dfadc-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="dfadc-127">Če želite izvajati pravilnike glede na ciljno entiteto, vklopite funkcijo **Ocena pravilnika o stroških glede na pravno osebo izposojevalko** v delovnem prostoru **Upravljanje funkcij**.</span><span class="sxs-lookup"><span data-stu-id="dfadc-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="dfadc-128">Kdaj oceniti pravilnike</span><span class="sxs-lookup"><span data-stu-id="dfadc-128">When to evaluate policies</span></span>

<span data-ttu-id="dfadc-129">V parametrih upravljanja stroškov lahko izberete, da ocenite pravilnike upravljanja stroškov, ko se vrstica shrani ali ko se predloži poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="dfadc-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="dfadc-130">Če se odločite, da boste ocenili, ko je vrstica shranjena, bodo uporabniki prej videli, kaj morajo storiti, da naenkrat izpolnijo poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="dfadc-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="dfadc-131">V nasprotnem primeru lahko odložite oceno pravilnika in prihranite čas s preverjanjem na koncu med predložitvijo v potek dela.</span><span class="sxs-lookup"><span data-stu-id="dfadc-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]