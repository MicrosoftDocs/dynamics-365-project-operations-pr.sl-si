---
title: Nastavitev pravilnikov o stroških
description: Nastavite lahko pravilnike o stroških, ki jih morajo vaši delavci upoštevati, ko vnašajo in predložijo poročila o stroških in zahteve za pot v aplikaciji Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005766"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="7cf8a-103">Nastavitev pravilnikov o stroških</span><span class="sxs-lookup"><span data-stu-id="7cf8a-103">Set up expense policies</span></span>

<span data-ttu-id="7cf8a-104">Opredelite lahko pravilnike, ki jih morajo vaši delavci upoštevati, ko vnašajo in predložijo poročila o stroških in zahteve za pot.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="7cf8a-105">Izvajanje pravilnikov o stroških vam lahko pomaga učinkovito upravljati stroške.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="7cf8a-106">Tako lahko na primer nastavite pravilnik za hotelske stroške v New Yorku, ki določa, da strošek na nočitev ne sme presegati 250 USD.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="7cf8a-107">Če delavec predloži poročilo o stroških ali zahtevo za pot, kjer cena sobe presega ta znesek, sistem obvesti</span><span class="sxs-lookup"><span data-stu-id="7cf8a-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="7cf8a-108">delavca, da je bil znesek pravilnika za strošek presežen.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="7cf8a-109">Lahko konfigurirate sporočilo, ki ga bo delavec prejel, ko</span><span class="sxs-lookup"><span data-stu-id="7cf8a-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="7cf8a-110">opredelite pravilnik.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-110">define the policy.</span></span>      
        
<span data-ttu-id="7cf8a-111">Opredelite lahko tri vrste pravilnikov:</span><span class="sxs-lookup"><span data-stu-id="7cf8a-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="7cf8a-112">Opozorilo – dovoli delavcu, da predloži poročilo o stroških ali zahtevo za pot, vendar bodo stroški označeni za vse odobritelje in</span><span class="sxs-lookup"><span data-stu-id="7cf8a-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="7cf8a-113">za poznejše poročanje.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-113">for later reporting.</span></span>        

- <span data-ttu-id="7cf8a-114">Napaka – od delavca zahteva, da revidira strošek v skladu s pravilnikom, preden predloži poročilo o stroških ali zahtevo za pot.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="7cf8a-115">Utemeljitev – zahteva, da delavec ali vodja pred predložitvijo poročila o stroških ali zahteve za pot vnese utemeljitev za preseganje zneska pravilnika.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="7cf8a-116">Nasveti glede pravilnikov</span><span class="sxs-lookup"><span data-stu-id="7cf8a-116">Policy tips</span></span>
<span data-ttu-id="7cf8a-117">Tu je nekaj predlogov, ki vam lahko pomagajo pri ustvarjanju novih pravilnikov za upravljanje stroškov.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="7cf8a-118">Pravilniki veljajo z datumom začetka veljavnosti in ne bodo začel veljati, če je pravilnik ustvarjen z datumom po datumu nastanka stroška.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="7cf8a-119">Če na primer danes ustvarite nov pravilnik, s katerim uveljavite največji strošek obroka v višini $50, vsi obstoječi stroški, vneseni do včeraj, ne bodo preverjeni v skladu s tem pravilnikom.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="7cf8a-120">Pri ustvarjanju pravilnika za kategorijo stroška, ki jo je mogoče razčleniti, razmislite o dodajanju pogoja za vrsto vrstice stroška.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="7cf8a-121">Nekateri pravilniki, na primer zahtevanje potrdila, morda niso smiselni za razčlenjene vrstice in se uporabljajo samo za vrstico glave ali nerazčlenjeno vrstico.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="7cf8a-122">Pravilniki upravljanja stroškov se privzeto ovrednotijo glede na izvorno entiteto.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="7cf8a-123">Za medpodjetniške scenarije lahko nastavite, da se pravilnik namesto tega vrednoti glede na ciljno entiteto (entiteta izposojevalka).</span><span class="sxs-lookup"><span data-stu-id="7cf8a-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="7cf8a-124">Če želite izvajati pravilnike glede na ciljno entiteto, vklopite funkcijo »Ocena pravilnika o stroških glede na pravno osebo izposojevalko« v delovnem prostoru **Upravljanje funkcij**.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="7cf8a-125">Kdaj oceniti pravilnike</span><span class="sxs-lookup"><span data-stu-id="7cf8a-125">When to evaluate policies</span></span>

<span data-ttu-id="7cf8a-126">V parametrih upravljanja stroškov imate možnost, da ocenite pravilnike upravljanja stroškov, ko se vrstica shrani ali ko se predloži poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="7cf8a-127">Če se odločite, da boste ocenili, ko je vrstica shranjena, s tem zagotovite, da bodo uporabniki prej videli, kaj morajo storiti, da naenkrat izpolnijo poročilo o stroških.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="7cf8a-128">V nasprotnem primeru lahko odložite oceno pravilnika in prihranite čas s preverjanjem na koncu med predložitvijo v potek dela.</span><span class="sxs-lookup"><span data-stu-id="7cf8a-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]