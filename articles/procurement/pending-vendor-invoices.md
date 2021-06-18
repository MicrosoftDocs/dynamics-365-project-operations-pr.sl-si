---
title: Nakup materialov, ki niso na zalogi, s čakajočim računom dobavitelja
description: V tej temi je pojasnjeno, kako zabeležiti čakajoče račune dobavitelja.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993833"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="ff643-103">Nakup materialov, ki niso na zalogi, s čakajočim računom dobavitelja</span><span class="sxs-lookup"><span data-stu-id="ff643-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="ff643-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="ff643-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ff643-105">Ker podjetje za projekt nabavlja materiale, ki niso na zalogi, lahko stroške takoj zabeležimo glede na projekt.</span><span class="sxs-lookup"><span data-stu-id="ff643-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="ff643-106">Podjetje Contoso Robotics US na primer izvaja projekt obnove opreme in potrebuje licence za programsko opremo.</span><span class="sxs-lookup"><span data-stu-id="ff643-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="ff643-107">Te licence dobavlja neodvisni dobavitelj.</span><span class="sxs-lookup"><span data-stu-id="ff643-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="ff643-108">Z aplikacijo Dynamics 365 Finance uradnik za obveznosti zabeleži dokument čakajočega računa dobavitelja in neposredno pripiše stroške licence projektu obnove opreme.</span><span class="sxs-lookup"><span data-stu-id="ff643-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="ff643-109">Preden uporabite funkcijo, opisano v tej temi, preglejte zahtevane konfiguracije in jih uporabite.</span><span class="sxs-lookup"><span data-stu-id="ff643-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="ff643-110">Za več informacij glejte [Omogočanje materialov, ki niso na zalogi, in čakajočih računov dobavitelja](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="ff643-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="ff643-111">Knjiženje čakajočega računa dobavitelja, povezanega s projektom</span><span class="sxs-lookup"><span data-stu-id="ff643-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="ff643-112">Čakajoče račune dobavitelja lahko zabeležite na strani **Čakajoči računi dobavitelja** (**Obveznosti** > **Računi** > **Čakajoči računi dobavitelja**).</span><span class="sxs-lookup"><span data-stu-id="ff643-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="ff643-113">Izvedite naslednje korake, če želite knjižiti čakajoči račun dobavitelja, ki je povezan s projektom:</span><span class="sxs-lookup"><span data-stu-id="ff643-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="ff643-114">V razdelku **Obveznosti** > **Računi** izberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ff643-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="ff643-115">V polju **Račun za obračun** izberite dobavitelja, v polje **Številka** pa vnesite identifikacijo računa dobavitelja.</span><span class="sxs-lookup"><span data-stu-id="ff643-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="ff643-116">Na račun dobavitelja dodajte vrstico in v polju **Številka elementa** izberite element, ki ni na zalogi, kupljen pri dobavitelju.</span><span class="sxs-lookup"><span data-stu-id="ff643-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ff643-117">Vrstic računa dobavitelja, ki temeljijo na kategoriji nabave, ni mogoče zabeležiti glede na projekt.</span><span class="sxs-lookup"><span data-stu-id="ff643-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="ff643-118">Dodajte količino kupljenega.</span><span class="sxs-lookup"><span data-stu-id="ff643-118">Add the quantity purchased.</span></span> <span data-ttu-id="ff643-119">Sistem bo zapolnil ceno enote glede na konfiguracijo cene elementa, ki ni na zalogi.</span><span class="sxs-lookup"><span data-stu-id="ff643-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="ff643-120">V vrstici preverite skupni znesek in druge zahtevane podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="ff643-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="ff643-121">V podrobnostih vrstice na zavihku **Projekt** izberite ID projekta, v katerega bo ta element zabeležen.</span><span class="sxs-lookup"><span data-stu-id="ff643-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="ff643-122">Po želji izberite številko dejavnosti in posodobite kategorijo projekta in lastnost vrstice.</span><span class="sxs-lookup"><span data-stu-id="ff643-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="ff643-123">Knjižite čakajoči račun dobavitelja.</span><span class="sxs-lookup"><span data-stu-id="ff643-123">Post pending vendor invoice.</span></span> <span data-ttu-id="ff643-124">Ko je račun knjižen, sistem zabeleži:</span><span class="sxs-lookup"><span data-stu-id="ff643-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="ff643-125">znesek stanja dobavitelja,</span><span class="sxs-lookup"><span data-stu-id="ff643-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="ff643-126">znesek prometnega davka,</span><span class="sxs-lookup"><span data-stu-id="ff643-126">The sales tax amount.</span></span>
    - <span data-ttu-id="ff643-127">stroške glede na projekt so zabeleženi na račun za integracijo naročil,</span><span class="sxs-lookup"><span data-stu-id="ff643-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="ff643-128">dejansko transakcijo projekta v storitvi Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ff643-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="ff643-129">Ta transakcija se nadalje obdeluje z [dnevnikom integracij za Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="ff643-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="ff643-130">Knjiženje tega dnevnika premakne znesek z računa za integracijo naročil na račun stroškov projekta.</span><span class="sxs-lookup"><span data-stu-id="ff643-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
