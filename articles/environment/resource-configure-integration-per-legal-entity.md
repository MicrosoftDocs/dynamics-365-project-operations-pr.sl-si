---
title: Konfiguracija integracije storitve Project Operations po pravnih osebah
description: Ta tema vsebuje informacije o nastavitvi integracije po pravnih osebah v storitvi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ccdbdce6b7d006adc9be2b5f3573dd8e79dd2b8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276998"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="4f7f5-103">Konfiguracija integracije storitve Project Operations po pravnih osebah</span><span class="sxs-lookup"><span data-stu-id="4f7f5-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="4f7f5-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="4f7f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4f7f5-105">Ta tema vsebuje postopna navodila za konfiguracijo aplikacije Dynamics 365 Project Operations za pravno osebo.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="4f7f5-106">Omogočanje ključev funkcij v storitvi Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="4f7f5-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="4f7f5-107">Izvedite naslednje korake, da omogočite zahtevane funkcije.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="4f7f5-108">V storitvi Dynamics 365 Finance izberite delovni prostor **Upravljanje funkcij**.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="4f7f5-109">Pri možnosti **Seznam funkcij** poiščite in omogočite naslednje funkcije:</span><span class="sxs-lookup"><span data-stu-id="4f7f5-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="4f7f5-110">**Omogočanje več podrobnosti pogodbe za projekt**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="4f7f5-111">**Omogočanje storitve Project Operations za Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="4f7f5-112">Če **ključi funkcij** niso navedeni, preverite, ali vaša različica storitve za finance izpolnjuje najmanjše zahteve glede različice (različica aplikacije 10.0.13 z vsemi posodobitvami kakovosti ali novejša različica).</span><span class="sxs-lookup"><span data-stu-id="4f7f5-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="4f7f5-113">Izberite **Preveri, ali so na voljo posodobitve**, da osvežite seznam funkcij.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="4f7f5-114">Opredelitev scenarija za uvajanje storitve Project Operations za pravno osebo</span><span class="sxs-lookup"><span data-stu-id="4f7f5-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="4f7f5-115">Project Operations lahko omogočite v storitvi Dynamics 365 Customer Engagement na ravni pravne osebe.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="4f7f5-116">V storitvi Project Operations lahko uporabljate eno pravno osebo v okviru storitve Dynamics 365 Customer Engagement za scenarije, ki temeljijo na viru/nezalogi.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="4f7f5-117">V istem okolju imate lahko še eno pravno osebo, ki uporablja Project Operations za scenarije z naročili na zalogi/v proizvodnji.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="4f7f5-118">V storitvi Dynamics 365 Finance odprite **Vodenje projektov in računovodstvo** > **Nastavitev** > **Globalno vodenje projektov in računovodski parametri**.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="4f7f5-119">Na seznamu razpoložljivih pravnih oseb izberite entitete, v katerih je vključenih več podrobnosti pogodbe in bodo omogočene funkcije Dynamics 365 Customer Engagement za Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="4f7f5-120">Ne izberite pravnih oseb, ki bodo uporabljale Project Operations za scenarije z naročili na zalogi/v proizvodnji.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="4f7f5-121">Pravno osebo je mogoče izbrati le, če nima obstoječih projektov.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="4f7f5-122">Konfiguracija parametrov za vodenje projektov in računovodstvo</span><span class="sxs-lookup"><span data-stu-id="4f7f5-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="4f7f5-123">Vsaka pravna oseba, ki uporablja Project Operations v okviru storitve Dynamics 365 Customer Engagement, potrebuje nabor privzetih parametrov.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="4f7f5-124">Ti parametri so nastavljeni na zavihku **Project Operations** na strani **Vodenje projektov in računovodski parametri**.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="4f7f5-125">Parametri so naslednji:</span><span class="sxs-lookup"><span data-stu-id="4f7f5-125">The parameters are:</span></span>

  - <span data-ttu-id="4f7f5-126">**Privzete vrednosti vrste obračunavanja**: Project Operations uporablja fiksni nabor privzetih vrednosti vrste obračunavanja, ki jih je treba preslikati v lastnosti vrstic storitve za finance.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="4f7f5-127">Ustvarite zapis za vsako vrsto obračunavanja: **Ni določeno**, **Se zaračuna**, **Se ne zaračuna**, **Brezplačno** in **Ni na voljo**.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="4f7f5-128">**Privzete vrednosti za kategorije projektov**: izberite privzete kategorije projektov, ki se bodo uporabljale za vsako vrsto transakcije.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="4f7f5-129">Te privzete vrednosti se bodo uporabljale pri možnosti **Dnevnik integracij za Project Operations** in pri ocenah, kjer za dejanske vrednosti projekta ni določena nobena kategorija transakcij.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="4f7f5-130">**Napovedi**: izberite model napovedi, ki se bo uporabljal za oceno časa in stroškov.</span><span class="sxs-lookup"><span data-stu-id="4f7f5-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]