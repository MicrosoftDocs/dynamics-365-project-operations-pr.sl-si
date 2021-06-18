---
title: Dodajanje naročnine na Azure projektu LCS
description: Ta tema vsebuje informacije o povezovanju naročnine Azure s projektom LCS.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6daa86d453ec5022cdd75dff0394c8818292406c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000636"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="eb47d-103">Dodajanje naročnine na Azure projektu LCS</span><span class="sxs-lookup"><span data-stu-id="eb47d-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="eb47d-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="eb47d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eb47d-105">Okolja, ki se jih gosti v oblaku, je treba uvesti z obstoječo naročnino na Azure.</span><span class="sxs-lookup"><span data-stu-id="eb47d-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="eb47d-106">Ta tema pojasnjuje, kako lahko povežete obstoječo naročnino na Azure s projektom LCS.</span><span class="sxs-lookup"><span data-stu-id="eb47d-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="eb47d-107">Podelitev soglasja skrbnika</span><span class="sxs-lookup"><span data-stu-id="eb47d-107">Grant admin consent</span></span>

1. <span data-ttu-id="eb47d-108">V projektu LCS v razdelku **Okolja** izberite **Nastavitve Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="eb47d-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Nastavitve Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="eb47d-110">Na strani **Nastavitve projekta** na zavihku **Povezovalniki Azure** izberite **Pooblasti**.</span><span class="sxs-lookup"><span data-stu-id="eb47d-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="eb47d-111">To omogoča uvedbo okolij v ta projekt.</span><span class="sxs-lookup"><span data-stu-id="eb47d-111">This allows environments to be deployed to this project.</span></span>

![Povezovalniki Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="eb47d-113">Znova izberite **Pooblasti**, da zagotovite soglasje skrbnika.</span><span class="sxs-lookup"><span data-stu-id="eb47d-113">Select **Authorize** again to provide admin consent.</span></span>

![Podelitev soglasja skrbnika](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="eb47d-115">Sprejmite zahtevo za dovoljenja.</span><span class="sxs-lookup"><span data-stu-id="eb47d-115">Accept the permissions request.</span></span>

![Sprejmite zahtevo za dovoljenja](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="eb47d-117">Pooblastitev je zdaj končana.</span><span class="sxs-lookup"><span data-stu-id="eb47d-117">The authorization is now complete.</span></span> 

![Pooblastitev je bila uspešna](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="eb47d-119">Omogočite dostop do storitev za uvajanje Dynamics za naročnino Azure</span><span class="sxs-lookup"><span data-stu-id="eb47d-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="eb47d-120">Odprite [Obračunavanje Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) in izberite naročnino.</span><span class="sxs-lookup"><span data-stu-id="eb47d-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="eb47d-121">Storitve za uvajanje Dynamics morajo imeti dostop do te naročnine, da lahko uvajajo okolja.</span><span class="sxs-lookup"><span data-stu-id="eb47d-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Podrobnosti o naročnini Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="eb47d-123">V podoknu za krmarjenje izberite **Nadzor dostopa (IAM)** in nato izberite **Dodaj dodelitev vloge**.</span><span class="sxs-lookup"><span data-stu-id="eb47d-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="eb47d-124">Pri drsniku na desni strani izberite **Vloga sodelujočega** ter na podanem seznamu poiščite in izberite **Storitve za uvajanje Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="eb47d-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="eb47d-125">Izberite **Shrani**.</span><span class="sxs-lookup"><span data-stu-id="eb47d-125">Select **Save**.</span></span>

![Dostop do naročnine](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="eb47d-127">Dodajanje povezovalnika naročnine na projekt LCS</span><span class="sxs-lookup"><span data-stu-id="eb47d-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="eb47d-128">V projektu LCS na strani z **nastavitvami Microsoft Azure** izberite **Dodaj**, da dodate nov povezovalnik.</span><span class="sxs-lookup"><span data-stu-id="eb47d-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="eb47d-129">Vnesite ID naročnine na Azure.</span><span class="sxs-lookup"><span data-stu-id="eb47d-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="eb47d-130">ID naročnine na Azure lahko najdete v [portalu Azure](https://ms.portal.azure.com/), pod možnostjo **Nastavitve** v spodnjem levem kotu zaslona.</span><span class="sxs-lookup"><span data-stu-id="eb47d-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="eb47d-131">V polju **Konfiguriraj za uporabo storitve Azure Resource Manager** izberite **Da**.</span><span class="sxs-lookup"><span data-stu-id="eb47d-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="eb47d-132">Prepričajte se, da se domena najemnika AAD za naročnino AAD ujema z naročnino na Azure, ki jo uporabljate in je lastnik domene, in izberite **Naprej**.</span><span class="sxs-lookup"><span data-stu-id="eb47d-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="eb47d-133">Na zaslonu **Nastavitev Microsoft Azure** izberite **Naprej**, da potrdite izbiro.</span><span class="sxs-lookup"><span data-stu-id="eb47d-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="eb47d-134">Če se na tem zaslonu prikaže napaka, se vrnite v razdelek [Omogočite dostop do storitev za uvajanje Dynamics za naročnino Azure](#provide) v tej temi in se prepričajte, da ste opravili vse korake.</span><span class="sxs-lookup"><span data-stu-id="eb47d-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="eb47d-135">Prenesite potrdilo o upravljanju Azure v lokalno mapo v računalniku.</span><span class="sxs-lookup"><span data-stu-id="eb47d-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="eb47d-136">Prosite skrbnika naročnine za Azure, da potrdilo naloži na portal za upravljanje Azure tako, da izbere naročnino in odpre razdelek **Nastavitve** > **Potrdila o upravljanju**.</span><span class="sxs-lookup"><span data-stu-id="eb47d-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="eb47d-137">To potrdilo omogoča LCS, da v vašem imenu komunicira z Azure.</span><span class="sxs-lookup"><span data-stu-id="eb47d-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="eb47d-138">Ta korak lahko preskočite, če ima vaš uporabnik dostop do naročnine.</span><span class="sxs-lookup"><span data-stu-id="eb47d-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="eb47d-139">Izberite **Naprej**.</span><span class="sxs-lookup"><span data-stu-id="eb47d-139">Select  **Next**.</span></span>
8. <span data-ttu-id="eb47d-140">Izberite regijo Azure, v kateri želite uvesti to možnost, in izberite podatkovno središče, ki je blizu mesta, kjer nameravate uporabljati ta sistem.</span><span class="sxs-lookup"><span data-stu-id="eb47d-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="eb47d-141">Izberite **Poveži**.</span><span class="sxs-lookup"><span data-stu-id="eb47d-141">Select  **Connect**.</span></span>

<span data-ttu-id="eb47d-142">Uspešno ste povezali naročnino na Azure.</span><span class="sxs-lookup"><span data-stu-id="eb47d-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="eb47d-143">Zdaj lahko uvedete okolja Dynamics 365 Finance, ki se jih gosti v oblaku.</span><span class="sxs-lookup"><span data-stu-id="eb47d-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
