---
title: Podrobnosti ponudb, ki temeljijo na stroškovnih izdelkih
description: Ta tema vsebuje informacije o uveljavljanju lastne cene v vrstici ponudbe, ki temelji na izdelku.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003471"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="902a4-103">Podrobnosti ponudb, ki temeljijo na stroškovnih izdelkih</span><span class="sxs-lookup"><span data-stu-id="902a4-103">Costing product-based quote lines</span></span>

<span data-ttu-id="902a4-104">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="902a4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="902a4-105">Podrobnosti ponudb, ki temeljijo na izdelkih, imajo v aplikaciji Dynamics 365 Project Operations tudi polje **Lastna cena**.</span><span class="sxs-lookup"><span data-stu-id="902a4-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="902a4-106">Polje se uporablja za sledenje lastni ceni izdelka v vrstici ponudbe in za izračune nadaljnje donosnosti.</span><span class="sxs-lookup"><span data-stu-id="902a4-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="902a4-107">Ko se za kataloški izdelek ustvari vrstica ponudbe, ki temelji na izdelku, je cena za vrstico samodejno privzeta iz polja **Standardna cena** v katalogu izdelkov.</span><span class="sxs-lookup"><span data-stu-id="902a4-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="902a4-108">Polje standardne cene v katalogu izdelkov je nastavljeno v osnovni valuti organizacije.</span><span class="sxs-lookup"><span data-stu-id="902a4-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="902a4-109">Privzeta cena na enoto v vrstici ponudbe, ki temelji na izdelku, se za ponudbo pretvori v valuto prodaje.</span><span class="sxs-lookup"><span data-stu-id="902a4-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="902a4-110">Cena na enoto v vrstici ponudbe, ki temelji na izdelku</span><span class="sxs-lookup"><span data-stu-id="902a4-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="902a4-111">Namen določitve cene na enoto v vrstici ponudbe, ki temelji na izdelku, je omogočiti različno ceno za izdelek za posamezno prodajo.</span><span class="sxs-lookup"><span data-stu-id="902a4-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="902a4-112">Tak scenarij sicer ni najbolj običajen, vendar pa včasih dobavitelj zniža ceno izdelka glede na končno stranko.</span><span class="sxs-lookup"><span data-stu-id="902a4-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="902a4-113">Na primer:</span><span class="sxs-lookup"><span data-stu-id="902a4-113">For example:</span></span>

<span data-ttu-id="902a4-114">Družba Fabrikam Robotics namešča robotske roke na montažne trakove korporacije A Datum.</span><span class="sxs-lookup"><span data-stu-id="902a4-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="902a4-115">Družba Fabrikam izvaja storitve namestitve, robotske roke pa dobavlja družba Trey robotics.</span><span class="sxs-lookup"><span data-stu-id="902a4-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="902a4-116">Če namestitev robotskih rok za korporacijo A Datum odpre novo navpičnico panoge za družbo Trey robotics, bi ta družba lahko družbi Fabrikam za ta posel priznala poseben popust.</span><span class="sxs-lookup"><span data-stu-id="902a4-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="902a4-117">V tem primeru družba Fabrikam za družbo Trey robotics ustvari vrstico ponudbe, ki temelji na izdelku, in za to ponudbo vnese posebno ceno na enoto.</span><span class="sxs-lookup"><span data-stu-id="902a4-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="902a4-118">Ta cena se razlikujejo od standardne cene družbe Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="902a4-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]