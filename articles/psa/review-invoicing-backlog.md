---
title: Pregled nedokončanih opravil za izdajo računov pri projektih in projektnih pogodbah
description: Ta tema vsebuje informacije o tem, kako pregledati nedokončana opravila za čas, stroške in izdelke in kako jih označiti kot pripravljene za izdajo računa.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084965"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="f5f04-103">Pregled nedokončanih opravil za izdajo računov pri projektih in projektnih pogodbah</span><span class="sxs-lookup"><span data-stu-id="f5f04-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f5f04-104">Ko je za transakcijo mogoče ustvariti in obdelati račun, mora biti označena z možnostjo **Pripravljeno za izdajanje računov**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="f5f04-105">Ta tema opisuje vrste transakcij, ki jih je mogoče ustvariti.</span><span class="sxs-lookup"><span data-stu-id="f5f04-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="f5f04-106">Pregled nedokončanih opravil obračunavanja časa in materiala</span><span class="sxs-lookup"><span data-stu-id="f5f04-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="f5f04-107">Ko je časovni ali stroškovni vnos predložen in odobren za določen projekt, PSA ustvari dejanske vrednosti projekta.</span><span class="sxs-lookup"><span data-stu-id="f5f04-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="f5f04-108">Če se projekt in razred transakcije skupaj preslikata v podrobnosti pogodbe za projekt, za katerega je potreben tako čas kot material, se ob odobritvi vnosa ustvarita dve dejanski vrednosti:</span><span class="sxs-lookup"><span data-stu-id="f5f04-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="f5f04-109">Dejanska cena</span><span class="sxs-lookup"><span data-stu-id="f5f04-109">Cost actual</span></span> 
- <span data-ttu-id="f5f04-110">Dejanski nezaračunani znesek prodaje</span><span class="sxs-lookup"><span data-stu-id="f5f04-110">Unbilled sales actual</span></span>

<span data-ttu-id="f5f04-111">Dejanski nezaračunani zneski prodaje predstavljajo nedokončana opravila obračunavanja, zato je treba njihovo stanje obračunavanja nastaviti na **Pripravljeno na izdajanje računov**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="f5f04-112">Ko ustvarite račun za projekt, se dejanski nezaračunani zneski prodaje, označeni kot **Pripravljeno za izdajanje računov** , prekopirajo kot podrobnosti vrstice računa.</span><span class="sxs-lookup"><span data-stu-id="f5f04-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="f5f04-113">Če želite pregledati nezaračunana opravila obračunavanja za čas in materiale, odprite možnost **Prodaja** \> **Obračunavanje** \> **Nedokončana opravila obračunavanja časa in materiala**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="f5f04-114">Izberite vse dejanske nezaračunane zneske prodaje, ki so pripravljeni za izdajo računa, in nato izberite možnost **Pripravljeno za izdajanje računov**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="f5f04-115">Stanje obračunavanja teh dejanskih zneskov se bo spremenilo v **Pripravljeno na izdajanje računov**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Nedokončana opravila obračunavanja časa in materiala](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="f5f04-117">Pregled nedokončanih opravil obračunavanja izdelkov</span><span class="sxs-lookup"><span data-stu-id="f5f04-117">Review the product billing backlog</span></span>

<span data-ttu-id="f5f04-118">Če ima projektna pogodba v PSA podrobnosti pogodbe na podlagi izdelkov, se te podrobnosti upoštevajo pri izdaji računov ob vsakokratnem ustvarjanju računa za projektno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="f5f04-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="f5f04-119">Vsi izdelki, katerih podrobnosti pogodbe so označene kot **Pripravljeno na izdajanje računov** , se prekopirajo v račun projekta v obliki projektnih vrstic računa.</span><span class="sxs-lookup"><span data-stu-id="f5f04-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="f5f04-120">Če želite pregledati nedokončana opravila obračunavanja izdelkov, pojdite v **Prodaja** \> **Obračunavanje** \> **Nedokončana opravila obračunavanja izdelkov**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="f5f04-121">Izberite vse podrobnosti pogodbe na podlagi izdelka, ki so pripravljene za izdajo računa, in nato izberite možnost **Pripravljeno za izdajanje računov**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="f5f04-122">Stanje obračunavanja teh podrobnosti se bo spremenilo v **Pripravljeno na izdajanje računov**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Nedokončana opravila obračunavanja izdelkov](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="f5f04-124">Pregled mejnikov obračunavanja za pogodbe s fiksno ceno</span><span class="sxs-lookup"><span data-stu-id="f5f04-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="f5f04-125">Vsaka podrobnost projektne pogodbe, ki uporablja način obračunavanja s fiksno ceno, mora določiti mejnike pogodbe.</span><span class="sxs-lookup"><span data-stu-id="f5f04-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="f5f04-126">Za te mejnike pogodbe je mogoče izdati račun le, če so označeni kot **Pripravljeno za izdajanje računov**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="f5f04-127">Če želite pregledati mejnike obračunavanja, odprite možnost **Prodaja** \> **Obračunavanje** \> **Mejniki s fiksno ceno**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="f5f04-128">Izberite mejnike, ki so pripravljeni za izdajo računa, in nato izberite možnost **Pripravljeno za izdajanje računov**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="f5f04-129">Stanje obračunavanja teh mejnikov se bo spremenilo v **Pripravljeno na izdajanje računov**.</span><span class="sxs-lookup"><span data-stu-id="f5f04-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Mejniki s fiksno ceno](media/FPBacklog.png)
