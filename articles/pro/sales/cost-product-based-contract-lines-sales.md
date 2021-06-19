---
title: Podrobnosti pogodbe, ki temeljijo na stroškovnih izdelkih – poenostavljena različica
description: Ta tema vsebuje informacije o ustvarjanju
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003561"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="b0e39-103">Podrobnosti pogodbe, ki temeljijo na stroškovnih izdelkih – poenostavljena različica</span><span class="sxs-lookup"><span data-stu-id="b0e39-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="b0e39-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="b0e39-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b0e39-105">Podrobnosti pogodbe, ki temeljijo na izdelkih, v aplikaciji Dynamics 365 Project Operations vključujejo polje **Lastna cena**, ki shranjuje lastno ceno izdelka za nadaljnje izračune donosnosti.</span><span class="sxs-lookup"><span data-stu-id="b0e39-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="b0e39-106">Ko se za izdelek v katalogu ustvarijo podrobnosti pogodbe, ki temeljijo na izdelkih, se cena v vrstici v katalogu izdelkov ponastavi iz polja **Standardni stroški**.</span><span class="sxs-lookup"><span data-stu-id="b0e39-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="b0e39-107">Polje **Standardna cena** v katalogu izdelkov je nastavljeno v osnovni valuti organizacije.</span><span class="sxs-lookup"><span data-stu-id="b0e39-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="b0e39-108">Ko se stroški na enoto privzamejo iz podrobnosti pogodbe, se pretvorijo v prodajno valuto v pogodbi.</span><span class="sxs-lookup"><span data-stu-id="b0e39-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="b0e39-109">Cena na enoto v podrobnostih pogodbe na podlagi izdelka</span><span class="sxs-lookup"><span data-stu-id="b0e39-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="b0e39-110">Določitev cene na enoto v podrobnostih pogodbe na podlagi izdelka omogoča različno ceno za izdelek za posamezno prodajo enote.</span><span class="sxs-lookup"><span data-stu-id="b0e39-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="b0e39-111">Čeprav to ni vedno potrebno, obstajajo določeni scenariji, ko dobavitelj stranki lahko zniža stroške izdelka.</span><span class="sxs-lookup"><span data-stu-id="b0e39-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="b0e39-112">Oglejte si ta primer:</span><span class="sxs-lookup"><span data-stu-id="b0e39-112">Consider the following scenario:</span></span>

<span data-ttu-id="b0e39-113">Družba Fabrikam Robotics namešča robotske roke na montažne trakove korporacije Adatum.</span><span class="sxs-lookup"><span data-stu-id="b0e39-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="b0e39-114">Fabrikam ponuja storitve namestitve, toda robotske roke izdeluje podjetje Trey Research.</span><span class="sxs-lookup"><span data-stu-id="b0e39-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="b0e39-115">Če namestitev robotskih rok za družbo Adatum Corporation odpre novo navpičnico panoge za družbo Trey Research, bi lahko družbi Fabrikam za ta posel priznala poseben popust.</span><span class="sxs-lookup"><span data-stu-id="b0e39-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="b0e39-116">V tem primeru Fabrikam za Robotics Arms ustvari podrobnosti pogodbe, ki temeljijo na izdelku.</span><span class="sxs-lookup"><span data-stu-id="b0e39-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="b0e39-117">Za to pogodbo se vnese cena na enoto.</span><span class="sxs-lookup"><span data-stu-id="b0e39-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="b0e39-118">Cena se razlikuje od cene robotskih rok podjetja Trey Research.</span><span class="sxs-lookup"><span data-stu-id="b0e39-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]