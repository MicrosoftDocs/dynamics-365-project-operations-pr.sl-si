---
title: Pošiljanje zahteve za vir
description: Ustvarjen zahtevani pogoj za vir lahko pošljete kot zahtevo za vir. Zahteva se nato pošlje upravitelju virov v izpolnitev.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279158"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="5943b-104">Pošiljanje zahteve za vir</span><span class="sxs-lookup"><span data-stu-id="5943b-104">Submit a resource request</span></span>

<span data-ttu-id="5943b-105">_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="5943b-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5943b-106">Ustvarjen zahtevani pogoj za vir lahko pošljete kot zahtevo za vir.</span><span class="sxs-lookup"><span data-stu-id="5943b-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="5943b-107">Zahteva se nato pošlje upravitelju virov v izpolnitev.</span><span class="sxs-lookup"><span data-stu-id="5943b-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="5943b-108">V aplikaciji Dynamics 365 Project Operations na strani **Projekti** izberite zavihek **Skupina**, če si želite ogledati seznam virov, ki jih je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="5943b-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="5943b-109">Izberite splošni vir, ki ima zahtevani pogoj za vir, s seznama in nato kliknite **Pošlji zahtevo**.</span><span class="sxs-lookup"><span data-stu-id="5943b-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="5943b-110">Status zahteve splošnega člana ekipe se bo spremenil v **Poslano**.</span><span class="sxs-lookup"><span data-stu-id="5943b-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="5943b-111">Ko je zahteva iz izpolnjena, se splošni vir zamenja z imenovanim virom, v primeru da upravitelj virov izpolni zahtevo z rezervacijo imenovanega vira.</span><span class="sxs-lookup"><span data-stu-id="5943b-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="5943b-112">V nasprotnem primeru, če upravitelj virov predlaga imenovani vir, bo splošni vir ostal v ekipi in se bo stanje zahteve spremenilo v **Potreben pregled**.</span><span class="sxs-lookup"><span data-stu-id="5943b-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]