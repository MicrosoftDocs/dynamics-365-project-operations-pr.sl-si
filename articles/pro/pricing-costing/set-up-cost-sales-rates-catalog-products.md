---
title: Nastavitev cen in prodaje za izdelke iz kataloga – poenostavljeno
description: Ta tema vsebuje informacije o nastavitvi mer stroškov in prodajnih zneskov za elemente v katalogu izdelkov.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176721"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="32623-103">Nastavitev cen in prodaje za izdelke iz kataloga – poenostavljeno</span><span class="sxs-lookup"><span data-stu-id="32623-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="32623-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="32623-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="32623-105">Nastavitev cen za elemente kataloga izdelkov v aplikaciji Dynamics 365 Project Operations je enaka kot v aplikaciji Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="32623-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="32623-106">Ker izdelkov ni mogoče oceniti ali uporabiti v projektih v aplikaciji Project Operations, za ponudbe in pogodbe ni treba nastaviti cen v katalogu izdelkov v cenikih za projekte.</span><span class="sxs-lookup"><span data-stu-id="32623-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="32623-107">Cene v katalogu izdelkov je treba nastaviti v polju **Cena izdelka** ponudbe, pogodbe ali stranke.</span><span class="sxs-lookup"><span data-stu-id="32623-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="32623-108">Za te entitete v cenikih za projekte ni treba nastaviti cen v katalogu izdelkov.</span><span class="sxs-lookup"><span data-stu-id="32623-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="32623-109">Ceniki za projekte so uporabljeni izključno v aplikaciji Project Operations.</span><span class="sxs-lookup"><span data-stu-id="32623-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="32623-110">Obstaja poslovna logika za aplikacije, ki kopira cenike iz ponudbe v pogodbo.</span><span class="sxs-lookup"><span data-stu-id="32623-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="32623-111">Rezultat tega je poseben cenik za pogodbo.</span><span class="sxs-lookup"><span data-stu-id="32623-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="32623-112">Kopiranje lahko odloži postopek pridobivanja ponudbe, če cenik za projekte v ponudbi postane prevelik.</span><span class="sxs-lookup"><span data-stu-id="32623-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="32623-113">Ceniki za izdelke se ne kopirajo, da bi v pogodbah ustvarili cenike po meri.</span><span class="sxs-lookup"><span data-stu-id="32623-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="32623-114">To pomeni, da ceniki za izdelke ne vplivajo na učinkovitost postopka pridobivanja ponudb.</span><span class="sxs-lookup"><span data-stu-id="32623-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
