---
title: Nastavitev cen in prodaje za izdelke iz kataloga – poenostavljeno
description: Ta tema vsebuje informacije o nastavitvi mer stroškov in prodajnih zneskov za elemente v katalogu izdelkov.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764582"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="5e65a-103">Nastavitev cen in prodaje za izdelke iz kataloga – poenostavljeno</span><span class="sxs-lookup"><span data-stu-id="5e65a-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="5e65a-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="5e65a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5e65a-105">Nastavitev cen za elemente kataloga izdelkov v storitvi Dynamics 365 Project Operations je enako kot v Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="5e65a-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="5e65a-106">V storitvi Project Operations izdelkov ni mogoče oceniti ali uporabiti na projektih, zato ni nujno, da so nastavljene cene kataloga izdelkov na projektnih cenikih za ponudbe in pogodbe.</span><span class="sxs-lookup"><span data-stu-id="5e65a-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="5e65a-107">Uporabite polja **Cena izdelka** za ponudbo, pogodbo ali kupca, da nastavite cene kataloga izdelkov.</span><span class="sxs-lookup"><span data-stu-id="5e65a-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="5e65a-108">Ne nastavljajte cen kataloga izdelkov v projektnih cenikih.</span><span class="sxs-lookup"><span data-stu-id="5e65a-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="5e65a-109">Ceniki za projekte so uporabljeni izključno v aplikaciji Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5e65a-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="5e65a-110">Poslovna logika, specifična za aplikacije, kopira cenike iz ponudbe v pogodbo.</span><span class="sxs-lookup"><span data-stu-id="5e65a-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="5e65a-111">Rezultat tega je poseben cenik za pogodbo.</span><span class="sxs-lookup"><span data-stu-id="5e65a-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="5e65a-112">Kopiranje lahko odloži postopek pridobivanja ponudbe, če cenik za projekte v ponudbi postane prevelik.</span><span class="sxs-lookup"><span data-stu-id="5e65a-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="5e65a-113">Ceniki za izdelke se ne kopirajo, da bi v pogodbah ustvarili cenike po meri.</span><span class="sxs-lookup"><span data-stu-id="5e65a-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="5e65a-114">Ker ni vključenega kopiranja, ni vplivov na delovanje postopka ponudbe.</span><span class="sxs-lookup"><span data-stu-id="5e65a-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
