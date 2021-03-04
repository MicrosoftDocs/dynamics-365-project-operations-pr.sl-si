---
title: Preskušanje demo podatkov
description: Navodila za prenos in preskušanje demo podatkov za Project Service Automation.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
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
ms.openlocfilehash: e1f3ebf8d0cd6c8e25fcab6775cd92d544867af8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151138"
---
# <a name="experiment-with-demo-data-project-service"></a><span data-ttu-id="aadbc-103">Preskušanje demo podatkov (Project Service)</span><span class="sxs-lookup"><span data-stu-id="aadbc-103">Experiment with demo data (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="aadbc-104">Za seznanitev z aplikacijo Dynamics 365 Project Service Automation je koristno uporabiti predhodno konfigurirano okolje za raziskovanje.</span><span class="sxs-lookup"><span data-stu-id="aadbc-104">To become familiar with Dynamics 365 Project Service Automation, it’s useful to have a pre-configured environment to explore.</span></span> <span data-ttu-id="aadbc-105">Za to smo ustvarili ločen namestitveni paket z vzorčnimi podatki (tokrat na voljo le v angleščini), ki olajša učenje o teh rešitvah.</span><span class="sxs-lookup"><span data-stu-id="aadbc-105">For this purpose, we’ve created a separate sample data installation package (English-language only at this time) that makes it easier to learn about these solutions.</span></span> 

<span data-ttu-id="aadbc-106">Namestitveni paket je na voljo v [Microsoftovem centru za prenose](https://go.microsoft.com/fwlink/?linkid=859966).</span><span class="sxs-lookup"><span data-stu-id="aadbc-106">The installation package is available on the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=859966).</span></span>  

<span data-ttu-id="aadbc-107">Zagon orodja za namestitev aplikacije Package Deployer povzroči naslednja dejanja:</span><span class="sxs-lookup"><span data-stu-id="aadbc-107">Running the Package Deployer install performs the following actions:</span></span> 
  
-   <span data-ttu-id="aadbc-108">Ustvari ali nastavi privzete parametre, ki poganjajo vedenje rešitve Project Service</span><span class="sxs-lookup"><span data-stu-id="aadbc-108">Creates or sets default parameters that drive behavior of Project Service</span></span>  
  
-   <span data-ttu-id="aadbc-109">Uvozi vzorčne podatke, kot so viri, ki jih je mogoče rezervirati, vloge, prodaja in ceniki z lastnimi cenami, organizacijske enote, ustrezni zapisi o prodajnem postopku, delovni nalogi in projekti.</span><span class="sxs-lookup"><span data-stu-id="aadbc-109">Imports sample data such as Bookable Resources, Roles, Sales and Cost Price lists, Organizational Units, relevant sales process records, Work Orders and Projects</span></span>    
  
> [!IMPORTANT]
> <span data-ttu-id="aadbc-110">**Predstavitvenih podatkov ni mogoče odstraniti.**</span><span class="sxs-lookup"><span data-stu-id="aadbc-110">**There is no way to un-install the demo data.**</span></span> <span data-ttu-id="aadbc-111">Zato upoštevajte, da je ta paket namenjen samo uporabi v sistemih za predstavitev, ocenjevanje, usposabljanje in preskušanje.</span><span class="sxs-lookup"><span data-stu-id="aadbc-111">Therefore, you should only use this package on demonstration, evaluation, training and test systems.</span></span>

<span data-ttu-id="aadbc-112">Za več informacij si oglejte ta [spletni dnevnik](https://blogs.msdn.microsoft.com/crm/2017/10/24/microsoft-dynamics-365-for-field-service-and-project-service-automation-sample-data).</span><span class="sxs-lookup"><span data-stu-id="aadbc-112">For more information, see this [blog](https://blogs.msdn.microsoft.com/crm/2017/10/24/microsoft-dynamics-365-for-field-service-and-project-service-automation-sample-data).</span></span>





  
### <a name="see-also"></a><span data-ttu-id="aadbc-113">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="aadbc-113">See Also</span></span>  
 <span data-ttu-id="aadbc-114">[Priročnik za skrbnike](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="aadbc-114">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="aadbc-115">[Priročnik za upravitelja kupcev](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="aadbc-115">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="aadbc-116">[Priročnik za vodje projektov](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="aadbc-116">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="aadbc-117">[Priročnik za upravitelje virov](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="aadbc-117">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="aadbc-118">Vodnik po času, stroških in sodelovanju</span><span class="sxs-lookup"><span data-stu-id="aadbc-118">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
