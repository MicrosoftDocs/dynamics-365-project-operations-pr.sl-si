---
title: Pošiljanje zahteve za vir
description: Ta tema vsebuje informacije o pošiljanju zahteve za vir projekta.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084849"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="8e7fd-103">Pošiljanje zahteve za vir</span><span class="sxs-lookup"><span data-stu-id="8e7fd-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8e7fd-104">Ustvarjen zahtevani pogoj za vir lahko pošljete kot zahtevo za vir.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="8e7fd-105">Zahteva se nato pošlje upravitelju virov v izpolnitev.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="8e7fd-106">V aplikaciji Project Service Automation (PSA) na strani **Projekti** kliknite zavihek **Skupina** , če si želite ogledati seznam virov, ki jih je mogoče rezervirati.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="8e7fd-107">Izberite splošni vir, ki ima zahtevani pogoj za vir, s seznama in nato kliknite **Pošlji zahtevo**.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Pošiljanje zahteve za vir](media/RM-how-to-18.png)

<span data-ttu-id="8e7fd-109">Status zahteve splošnega člana ekipe se bo spremenil v **Poslano**.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="8e7fd-110">Ko upravitelj virov izpolni zahtevo, bo imenovani vir nadomestil splošni vir, v primeru da upravitelj virov izpolni zahtevo z rezervacijo imenovanega vira.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="8e7fd-111">V nasprotnem primeru bo splošni vir ostal v ekipi in se bo stanje zahteve spremenilo v **Potreben pregled** , če je upravitelj virov predlagal imenovani vir.</span><span class="sxs-lookup"><span data-stu-id="8e7fd-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review** , if the resource manager has proposed a named resource.</span></span>
