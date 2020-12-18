---
title: Pregled izstavljanja računov med podjetji
description: Ta tema vsebuje informacije in primere o medpodjetnem izdajanju računov za projekte.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595555"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="c9f11-103">Pregled izstavljanja računov med podjetji</span><span class="sxs-lookup"><span data-stu-id="c9f11-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="c9f11-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="c9f11-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c9f11-105">Vaša organizacija ima lahko več oddelkov, podružnic in drugih pravnih subjektov, ki si za projekte izmenjujejo izdelke in storitve.</span><span class="sxs-lookup"><span data-stu-id="c9f11-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="c9f11-106">Pravna oseba, ki zagotavlja storitev ali izdelek, se imenuje *posojilna pravna oseba*.</span><span class="sxs-lookup"><span data-stu-id="c9f11-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="c9f11-107">Pravna oseba, ki sprejme storitev ali izdelek, se imenuje *izposojevalna pravna oseba*.</span><span class="sxs-lookup"><span data-stu-id="c9f11-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="c9f11-108">Naslednja slika prikazuje tipičen scenarij, kjer si dve pravni osebi, Contoso Robotics USA (izposojevalna pravna oseba) in Contoso Robotics UK (posojilna pravna oseba), delita sredstva za izvedbo projekta za stranko Adventure works.</span><span class="sxs-lookup"><span data-stu-id="c9f11-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="c9f11-109">V tem scenariju je podjetje Contoso Robotics USA po pogodbi dolžno opraviti storitev za Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="c9f11-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Izstavljanje računov med podjetji](./media/IntercompanyScenario.png) 

<span data-ttu-id="c9f11-111">Dynamics 365 Project Operations uporablja spodaj prikazani potek za obdelavo medpodjetnih transakcij:</span><span class="sxs-lookup"><span data-stu-id="c9f11-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="c9f11-112">Viri posojilne pravne entitete beležijo medpodjetne transakcije s časom ali stroški, tako da knjižijo čas in stroške za projekte v izposojevalni pravni entiteti.</span><span class="sxs-lookup"><span data-stu-id="c9f11-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="c9f11-113">Čas in stroški so zabeleženi v posojilnem podjetju po ceniku izposojevalnega podjetja.</span><span class="sxs-lookup"><span data-stu-id="c9f11-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="c9f11-114">Medpodjetne neobračunane prodajne transakcije so zabeležene v posojilnem podjetju po ceniku izposojevalnega podjetja.</span><span class="sxs-lookup"><span data-stu-id="c9f11-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="c9f11-115">Neobračunani prihodki so zabeleženi v izposojevalnem podjetju po prodajnem ceniku projektne pogodbe.</span><span class="sxs-lookup"><span data-stu-id="c9f11-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="c9f11-116">Stranki se lahko zaračuna, ko se zabeležijo neobračunani prihodki.</span><span class="sxs-lookup"><span data-stu-id="c9f11-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="c9f11-117">Stranki ni treba čakati, da se zaključi obdelava izdajanja računov med podjetji.</span><span class="sxs-lookup"><span data-stu-id="c9f11-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="c9f11-118">Medpodjetni računi za stranke se periodično ustvarjajo v posojilnem podjetju.</span><span class="sxs-lookup"><span data-stu-id="c9f11-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="c9f11-119">Računi se ustvarjajo ročno ali z uporabo periodičnega avtomatiziranega procesa.</span><span class="sxs-lookup"><span data-stu-id="c9f11-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="c9f11-120">Ustvariti je mogoče poseben račun za vsako izposojevalno pravno osebo ali ločene račune po projektih.</span><span class="sxs-lookup"><span data-stu-id="c9f11-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="c9f11-121">Ko je račun za medpodjetno stranko knjižen v posojilni pravni osebi, se v izposojevalni pravni osebi ustvari čakajoč račun za dobavitelja.</span><span class="sxs-lookup"><span data-stu-id="c9f11-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="c9f11-122">Stroški na čakajočem računu za dobavitelja bodo zabeleženi v podknjigi projekta ob knjiženju računa.</span><span class="sxs-lookup"><span data-stu-id="c9f11-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="c9f11-123">Naslednji diagram prikazuje medpodjetno izdajanje računov, saj se nanaša na računovodske dogodke in pričakovana knjiženja v glavno knjigo.</span><span class="sxs-lookup"><span data-stu-id="c9f11-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Medpodjetni potek](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="c9f11-125">Dodatni viri</span><span class="sxs-lookup"><span data-stu-id="c9f11-125">Additional resources</span></span>

- [<span data-ttu-id="c9f11-126">Konfiguriranje izstavljanja računov med podjetji</span><span class="sxs-lookup"><span data-stu-id="c9f11-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="c9f11-127">Beleženje medpodjetnih transakcij</span><span class="sxs-lookup"><span data-stu-id="c9f11-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="c9f11-128">Ustvarjanje računov medpodjetnih strank in prodajalcev</span><span class="sxs-lookup"><span data-stu-id="c9f11-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)
