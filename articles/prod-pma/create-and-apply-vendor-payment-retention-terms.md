---
title: Ustvarjanje in uporaba pogojev za zadrževanje plačila dobaviteljem
description: Ta tema vsebuje informacije o tem, kako nastaviti in vzdrževati pogoje za zadrževanje plačila dobaviteljem.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006350"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="76f42-103">Ustvarjanje in uporaba pogojev za zadrževanje plačila dobaviteljem</span><span class="sxs-lookup"><span data-stu-id="76f42-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="76f42-104">Nastavitev pogojev za zadrževanje plačila dobaviteljem za projekt je koristna, če želi vaša organizacija obdržati del plačil dobavitelju.</span><span class="sxs-lookup"><span data-stu-id="76f42-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="76f42-105">Na primer ko želite zadržati plačilo dobavitelju, dokler dobavljeni izdelki ne izpolnijo vaših pričakovanj.</span><span class="sxs-lookup"><span data-stu-id="76f42-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="76f42-106">Pogoje za zadrževanje plačila dobavitelju lahko določite med pogajanjem za pogodbo z dobaviteljem.</span><span class="sxs-lookup"><span data-stu-id="76f42-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="76f42-107">Ustvarjanje pogojev za zadrževanje plačila dobaviteljem</span><span class="sxs-lookup"><span data-stu-id="76f42-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="76f42-108">Vnesete lahko delež plačila dobavitelju, ki ga želite zadržati, in delež predhodno zadržanih zneskov, ki jih želite sprostiti.</span><span class="sxs-lookup"><span data-stu-id="76f42-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="76f42-109">Zneski se samodejno zadržijo na računih dobaviteljev, dokler pogodba ne doseže dogovorjenega stanja izpolnitve.</span><span class="sxs-lookup"><span data-stu-id="76f42-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="76f42-110">Ko nastavite pogoje za zadržanje, lahko te pogoje uporabite za kateri koli projekt tega dobavitelja.</span><span class="sxs-lookup"><span data-stu-id="76f42-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="76f42-111">Uporabite naslednje korake za nastavitev in vzdrževanje pogojev za zadrževanje plačila dobavitelju.</span><span class="sxs-lookup"><span data-stu-id="76f42-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="76f42-112">Odprite **Vodenje projektov in računovodstvo** > **Zadrževanje** > **Pogoji za zadrževanje plačila dobavitelju**.</span><span class="sxs-lookup"><span data-stu-id="76f42-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="76f42-113">Izberite **Novo**, da dodate nov pogoj za zadržanje plačila dobavitelju.</span><span class="sxs-lookup"><span data-stu-id="76f42-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="76f42-114">Vrednost **ID pravila** za novi pogoj se samodejno vnese.</span><span class="sxs-lookup"><span data-stu-id="76f42-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="76f42-115">Vnesite kratek opis v polje **Opis** in v zavihku za hitri dostop **Pogoji** izberite **Dodaj vrstico**, da vnesete vrednosti pogojev za naslednje entitete:</span><span class="sxs-lookup"><span data-stu-id="76f42-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="76f42-116">**Delež dobavljenih enot**: vnesite delež izpolnitve pogoja.</span><span class="sxs-lookup"><span data-stu-id="76f42-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="76f42-117">Zneski se samodejno zadržijo na računih dobaviteljev, dokler stanje izpolnitve projekta ne doseže dogovorjenega deleža.</span><span class="sxs-lookup"><span data-stu-id="76f42-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="76f42-118">Če na primer vnesete 50,00, se zneski zadržijo, dokler projekt ni dokončan do 50 odstotkov.</span><span class="sxs-lookup"><span data-stu-id="76f42-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="76f42-119">**Delež, ki ga je treba zadržati**: vnesite delež zneska računa dobavitelju, ki ga je treba zadržati.</span><span class="sxs-lookup"><span data-stu-id="76f42-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="76f42-120">Če na primer vnesete 10.00, se 10 odstotkov zneska na računu dobavitelja zadrži, dokler projekt ne doseže deleža izpolnitve, kot je določeno v polju **Delež dobavljenih enot**.</span><span class="sxs-lookup"><span data-stu-id="76f42-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="76f42-121">**Delež za sprostitev**: izberite **Dodaj vrstico** za vnos odstotka predhodno zadržanih zneskov, ki se sprostijo ob določeni stopnji dokončanosti projekta.</span><span class="sxs-lookup"><span data-stu-id="76f42-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="76f42-122">Če imate več kot en mejnik za različne stopnje dokončanosti projekta, vnesite ločeno vrstico pogoja za zadrževanje plačila dobavitelju za vsako pravilo za zadrževanje.</span><span class="sxs-lookup"><span data-stu-id="76f42-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="76f42-123">Vsaka vrstica lahko določa drugačen odstotek zadrževanja in drugačen odstotek sprostitve za vsako določeno stopnjo dokončanja projekta.</span><span class="sxs-lookup"><span data-stu-id="76f42-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="76f42-124">Ko ustvarite pogoje za zadržanje plačila dobavitelju, lahko te pogoje uporabite tudi za projekt.</span><span class="sxs-lookup"><span data-stu-id="76f42-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="76f42-125">Uporaba pogojev za zadrževanje plačila dobaviteljem</span><span class="sxs-lookup"><span data-stu-id="76f42-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="76f42-126">Odprite **Vodenje projektov in računovodstvo** > **Projekti** > **Vsi projekti** in odprite projekt s strani s seznamom projektov.</span><span class="sxs-lookup"><span data-stu-id="76f42-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="76f42-127">Na zavihku za hitri dostop **Pogodbe dobaviteljev** izberite **Dodaj vrstico**.</span><span class="sxs-lookup"><span data-stu-id="76f42-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="76f42-128">V polju **Koda kupca** izberite eno od naslednjih možnosti:</span><span class="sxs-lookup"><span data-stu-id="76f42-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="76f42-129">**Tabela**: pogoji za zadrževanje plačila dobavitelju veljajo za enega dobavitelja.</span><span class="sxs-lookup"><span data-stu-id="76f42-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="76f42-130">**Skupina**: pogoji za zadrževanje plačila dobavitelju veljajo za vse dobavitelje v skupini dobaviteljev.</span><span class="sxs-lookup"><span data-stu-id="76f42-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="76f42-131">**Vsi**: pogoji za zadrževanje plačila dobavitelju veljajo za vse dobavitelje.</span><span class="sxs-lookup"><span data-stu-id="76f42-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="76f42-132">V polju **Dobavitelj/skupina dobaviteljev** izberite dobavitelja ali skupino dobaviteljev, za katero naj se uporabijo pogoji za zadrževanje plačila dobavitelju.</span><span class="sxs-lookup"><span data-stu-id="76f42-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="76f42-133">Če ste v prejšnjem koraku izbrali možnost **Vsi**, to polje ne bo na voljo.</span><span class="sxs-lookup"><span data-stu-id="76f42-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="76f42-134">V polju **Pogoji za zadrževanje plačila dobavitelju** izberite pogoje za zadrževanje, ki ste jih ustvarili v prejšnjem postopku.</span><span class="sxs-lookup"><span data-stu-id="76f42-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="76f42-135">Če ima projekt za dobavitelja nastavljene tudi pogoje po načinu plačila ob izvedenem plačilu (PWP), vnesite mejni odstotek za projekt v polju **Mejni odstotek za PWP**.</span><span class="sxs-lookup"><span data-stu-id="76f42-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="76f42-136">Pogoji za zadrževanje plačila dobavitelju so prikazani tudi v naročilnicah, ki jih ustvarite za dobavitelja.</span><span class="sxs-lookup"><span data-stu-id="76f42-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]