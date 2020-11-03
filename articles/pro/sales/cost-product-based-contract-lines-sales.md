---
title: Podrobnosti pogodb, ki temeljijo na stroškovnih izdelkih
description: Ta tema vsebuje informacije o ustvarjanju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/20/2020
ms.locfileid: "4084987"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="65f5d-103">Podrobnosti pogodb, ki temeljijo na stroškovnih izdelkih</span><span class="sxs-lookup"><span data-stu-id="65f5d-103">Costing product-based contract lines</span></span>

<span data-ttu-id="65f5d-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="65f5d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="65f5d-105">Podrobnosti pogodbe na podlagi izdelkov v storitvi Dynamics 365 Project Operations vključujejo polje **Lastna cena** , ki označuje lastno ceno izdelka za izračune nadaljnje donosnosti.</span><span class="sxs-lookup"><span data-stu-id="65f5d-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="65f5d-106">Ko se za kataloški izdelek ustvarijo podrobnosti pogodbe na podlagi izdelka, je cena za podrobnosti pogodbe samodejno privzeta iz polja **Standardna cena** v katalogu izdelkov.</span><span class="sxs-lookup"><span data-stu-id="65f5d-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="65f5d-107">Polje **Standardna cena** v katalogu izdelkov je nastavljeno v osnovni valuti organizacije.</span><span class="sxs-lookup"><span data-stu-id="65f5d-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="65f5d-108">Ko se stroški na enoto privzamejo iz podrobnosti pogodbe, se pretvorijo v prodajno valuto v pogodbi.</span><span class="sxs-lookup"><span data-stu-id="65f5d-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="65f5d-109">Cena na enoto v podrobnostih pogodbe na podlagi izdelka</span><span class="sxs-lookup"><span data-stu-id="65f5d-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="65f5d-110">Določitev cene na enoto v podrobnostih pogodbe na podlagi izdelka omogoča različno ceno za izdelek za posamezno prodajo enote.</span><span class="sxs-lookup"><span data-stu-id="65f5d-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="65f5d-111">Čeprav to ni vedno potrebno, obstajajo določeni scenariji, ko dobavitelj stranki lahko zniža stroške izdelka.</span><span class="sxs-lookup"><span data-stu-id="65f5d-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="65f5d-112">Oglejte si ta primer:</span><span class="sxs-lookup"><span data-stu-id="65f5d-112">Consider the following scenario:</span></span>

<span data-ttu-id="65f5d-113">Družba Fabrikam Robotics namešča robotske roke na montažne trakove korporacije Adatum.</span><span class="sxs-lookup"><span data-stu-id="65f5d-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="65f5d-114">Družba Fabrikam izvaja storitve namestitve, robotske roke pa dobavlja družba Trey Research.</span><span class="sxs-lookup"><span data-stu-id="65f5d-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="65f5d-115">Če namestitev robotskih rok za družbo Adatum Corporation odpre novo navpičnico panoge za družbo Trey Research, bi lahko družbi Fabrikam za ta posel priznala poseben popust.</span><span class="sxs-lookup"><span data-stu-id="65f5d-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="65f5d-116">V tem primeru Fabrikam ustvari podrobnosti pogodbe na podlagi izdelka za Robotic Arms in vnese stroške na enoto za to pogodbo, ki se razlikujejo od standardnih stroškov robotskih rok družbe Trey Research.</span><span class="sxs-lookup"><span data-stu-id="65f5d-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
