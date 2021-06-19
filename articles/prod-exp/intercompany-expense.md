---
title: Medpodjetni stroški
description: V tej temi so na voljo informacije o tem, kako uporabite stroške med podjetji za dodelitev stroškov delavca pravni osebi, za katero je bilo delo opravljeno.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005091"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="c6702-103">Medpodjetni stroški</span><span class="sxs-lookup"><span data-stu-id="c6702-103">Intercompany expenses</span></span>

<span data-ttu-id="c6702-104">Delavec, ki je zaposlen pri eni pravni osebi v organizaciji, lahko opravlja delo pri drugi pravni osebi v isti organizaciji.</span><span class="sxs-lookup"><span data-stu-id="c6702-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="c6702-105">Stroške med podjetji lahko uporabite za dodelitev stroškov delavca pravni osebi, za katero je bilo delo opravljeno.</span><span class="sxs-lookup"><span data-stu-id="c6702-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="c6702-106">Pravna oseba, ki zaposli delavca, se imenuje posojilna pravna oseba.</span><span class="sxs-lookup"><span data-stu-id="c6702-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="c6702-107">Pravna oseba, na katero se pišejo stroški delavca, se imenuje izposojevalna pravna oseba.</span><span class="sxs-lookup"><span data-stu-id="c6702-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="c6702-108">Preden lahko delavec ustvari in predloži stroške med podjetji, morate omogočiti vrstice stroškov med podjetji.</span><span class="sxs-lookup"><span data-stu-id="c6702-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="c6702-109">V posojilni pravni osebi na strani **Parametri upravljanja stroškov** izberite **Omogoči vrstice stroškov med podjetji**.</span><span class="sxs-lookup"><span data-stu-id="c6702-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="c6702-110">Davčna napoved za medpodjetne stroške</span><span class="sxs-lookup"><span data-stu-id="c6702-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6702-111">Preden lahko v poročilu o stroških uporabite davčne skupine, ki so povezane s posojilno (izvorno) pravno osebo namesto z izposojevalno (ciljno) pravno osebo, morate omogočiti funkcijo v nastavitvi prometnega davka v glavni knjigi.</span><span class="sxs-lookup"><span data-stu-id="c6702-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="c6702-112">Ko je parameter **Pravna oseba za davčno napoved med podjetji** nastavljen na **Vir**, **Uporabi davčna pravila za prometni davek** pa na **Ne**, se uporabi davčna kombinacija za posojilno pravno osebo.</span><span class="sxs-lookup"><span data-stu-id="c6702-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="c6702-113">Ko je isti parameter nastavljen na **Cilj**, bo uporabljena kombinacija davka za izposojevalno pravno osebo.</span><span class="sxs-lookup"><span data-stu-id="c6702-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="c6702-114">Za pravne osebe v ZDA velja naslednje: če je parameter nastavljen na **Vir**, mora biti polje **Terjatve od prometnega davka** konfigurirano tudi na novi strani **Skupine za vnašanje v glavno knjigo**.</span><span class="sxs-lookup"><span data-stu-id="c6702-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="c6702-115">Računovodski mehanizem bo podatke iz tega polja uporabil za vnos računovodskih evidenc v zvezi z davki.</span><span class="sxs-lookup"><span data-stu-id="c6702-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="c6702-116">To vedenje je skladno za vrstice stroškov, objavljene s projektom ali brez.</span><span class="sxs-lookup"><span data-stu-id="c6702-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]