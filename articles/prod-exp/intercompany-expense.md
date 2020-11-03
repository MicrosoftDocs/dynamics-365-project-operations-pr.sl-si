---
title: Medpodjetni stroški
description: Delavec, ki je zaposlen pri eni pravni osebi v organizaciji, lahko opravlja delo pri drugi pravni osebi v isti organizaciji. V tem primeru lahko s funkcijo medpodjetnih stroškov dodelite stroške delavca tisti pravni osebi, za katero je bilo delo opravljeno.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084907"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="f1f84-104">Medpodjetni stroški</span><span class="sxs-lookup"><span data-stu-id="f1f84-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1f84-105">Delavec, ki je zaposlen pri eni pravni osebi v organizaciji, lahko opravlja delo pri drugi pravni osebi v isti organizaciji.</span><span class="sxs-lookup"><span data-stu-id="f1f84-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="f1f84-106">V tem primeru lahko s funkcijo medpodjetnih stroškov dodelite stroške delavca tisti pravni osebi, za katero je bilo delo opravljeno.</span><span class="sxs-lookup"><span data-stu-id="f1f84-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="f1f84-107">Pravna oseba, ki zaposli delavca, se imenuje posojilna pravna oseba.</span><span class="sxs-lookup"><span data-stu-id="f1f84-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="f1f84-108">Pravna oseba, na katero se pišejo stroški delavca, se imenuje izposojevalna pravna oseba.</span><span class="sxs-lookup"><span data-stu-id="f1f84-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="f1f84-109">Preden lahko delavec ustvari in predloži stroške dela, ki ga opravlja za drugo pravno osebo, na strani **Parametri upravljanja stroškov** za posojilno pravno osebo izberite možnost **Dovoli vrstice medpodjetnih stroškov**.</span><span class="sxs-lookup"><span data-stu-id="f1f84-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="f1f84-110">Davčna napoved za medpodjetne stroške</span><span class="sxs-lookup"><span data-stu-id="f1f84-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1f84-111">Če želite v poročilu o stroških uporabiti davčne skupine, ki so povezane s posojilno (izvorno) pravno osebo namesto z izposojilno (ciljno) pravno osebo, boste morali to nastaviti v možnosti za nastavitev prometnega davka v glavni knjigi.</span><span class="sxs-lookup"><span data-stu-id="f1f84-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="f1f84-112">Ko je parameter glavne knjige **Pravna oseba za medpodjetno davčno napoved** nastavljen na **Vir** in **Uporabi pravila o obdavčitvi za prometni davek** nastavljen na **Ne** , bo uporabljena kombinacija davkov za posojilno pravno osebo.</span><span class="sxs-lookup"><span data-stu-id="f1f84-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="f1f84-113">Ko je isti parameter nastavljen na **Cilj** , bo uporabljena kombinacija davka za izposojevalno pravno osebo.</span><span class="sxs-lookup"><span data-stu-id="f1f84-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="f1f84-114">Za pravne osebe v ZDA velja naslednje: če je parameter nastavljen na **Vir** , mora biti polje **Terjatve od prometnega davka** konfigurirano tudi na novi strani **Skupine za vnašanje v glavno knjigo**.</span><span class="sxs-lookup"><span data-stu-id="f1f84-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="f1f84-115">Računovodski mehanizem bo podatke iz tega polja uporabil za vnos računovodskih evidenc v zvezi z davki.</span><span class="sxs-lookup"><span data-stu-id="f1f84-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="f1f84-116">To vedenje je skladno za vrstice stroškov, objavljene s projektom ali brez.</span><span class="sxs-lookup"><span data-stu-id="f1f84-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
