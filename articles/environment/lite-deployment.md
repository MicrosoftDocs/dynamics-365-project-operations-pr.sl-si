---
title: Poenostavljena uvedba storitve Project Operations – od posla do izstavitve predračuna
description: Ta tema vsebuje informacije o tem, kako lahko namestite poenostavljeno uvedbo storitve Project Operations – od posla do izstavitve predračuna.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084620"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="b758a-103">Poenostavljena uvedba storitve Project Operations – od posla do izstavitve predračuna</span><span class="sxs-lookup"><span data-stu-id="b758a-103">Deploy Project Operations Lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="b758a-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="b758a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b758a-105">Storitev Project Operations podpira več modelov uvedbe.</span><span class="sxs-lookup"><span data-stu-id="b758a-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="b758a-106">Če želite določiti najboljši model uvedbe, glejte [Vrste uvajanja](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="b758a-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="b758a-107">Ta uvedba, poenostavljena uvedba – od posla do izstavitve predračuna, vodi v **uvedbo zgolj možnosti Common Data Service za storitev Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="b758a-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="b758a-108">Namestitev storitve Project Operations v novo okolje CDS</span><span class="sxs-lookup"><span data-stu-id="b758a-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="b758a-109">Namestitev v obstoječe okolje CDS</span><span class="sxs-lookup"><span data-stu-id="b758a-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="b758a-110">Namestitev storitve Project Operations v novo okolje CDS</span><span class="sxs-lookup"><span data-stu-id="b758a-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="b758a-111">Kot [globalni skrbnik ali skrbnik za Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) z licenco Project Operations ustvarite novo okolje CDS v [skrbniškem središču PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="b758a-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="b758a-112">Poskrbite, da so omogočene **Zbirka podatkov CDS** in **Aplikacije Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="b758a-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="b758a-113">Za več informacij glejte [Ustvarjanje in upravljanje okolij v skrbniškem središču Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="b758a-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="b758a-114">S seznama za uvajanje aplikacij Dynamics 365 izberite **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="b758a-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="b758a-115">Namestitev storitve Project Operations v obstoječe okolje CDS</span><span class="sxs-lookup"><span data-stu-id="b758a-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="b758a-116">Kot [globalni skrbnik ali skrbnik Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) z licenco Project Operations poiščite okolje v [skrbniškem centru PowerPlatform](https://admin.powerplatform.com), kamor želite namestiti Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b758a-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="b758a-117">S seznama za uvajanje aplikacij Dynamics 365 namestite **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="b758a-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="b758a-118">Če želite več informacij, glejte [Upravljanje aplikacij Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="b758a-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


