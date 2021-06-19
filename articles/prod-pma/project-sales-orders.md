---
title: Projektni prodajni nalogi za časovne in materialne projekte
description: Ta tema pojasnjuje, kako ustvariti prodajne naloge na podlagi projekta za časovne in materialne projekte.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009681"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="2b725-103">Projektni prodajni nalogi za časovne in materialne projekte</span><span class="sxs-lookup"><span data-stu-id="2b725-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2b725-104">Ta tema opisuje, kako ustvariti prodajni nalog za projekt.</span><span class="sxs-lookup"><span data-stu-id="2b725-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="2b725-105">Prodajni nalog je mogoče ustvariti samo za projekte tipa **čas in material**.</span><span class="sxs-lookup"><span data-stu-id="2b725-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="2b725-106">Če ima časovni in materialni projekt po pogodbi več virov financiranja, morate omogočiti parameter **Omogoči prodajne naloge za projekte z več viri financiranja** na strani **Parametri za vodenje projektov in računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="2b725-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="2b725-107">Podpora za projektne prodajne naloge z več viri financiranja je na voljo v aplikaciji 10.0.2 ali novejši različici.</span><span class="sxs-lookup"><span data-stu-id="2b725-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="2b725-108">Parameter za omogočanje podpore za projektne prodajne naloge z več viri financiranja bo odstranjen v izdaji aprila 2020, po njej pa bo ta funkcionalnost vedno omogočena.</span><span class="sxs-lookup"><span data-stu-id="2b725-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="2b725-109">Prodajne naloge na podlagi projektov lahko ustvarite na dva načina:</span><span class="sxs-lookup"><span data-stu-id="2b725-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="2b725-110">Pojdite v sam projekt.</span><span class="sxs-lookup"><span data-stu-id="2b725-110">Go to the project itself.</span></span> <span data-ttu-id="2b725-111">V podoknu za dejanja izberite **Upravljanje > Opravila elementa > Prodajni nalog**.</span><span class="sxs-lookup"><span data-stu-id="2b725-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="2b725-112">Privzeto bodo prikazane informacije o projektu za prodajni nalog iz projekta.</span><span class="sxs-lookup"><span data-stu-id="2b725-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="2b725-113">Če ima projektna pogodba več kot en vir financiranja, boste morali izbrati vir financiranja, če boste želeli nastaviti stranko za prodajni nalog.</span><span class="sxs-lookup"><span data-stu-id="2b725-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="2b725-114">Če za projekt obstaja samo en vir financiranja, bo stranka samodejno nastavljena.</span><span class="sxs-lookup"><span data-stu-id="2b725-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="2b725-115">Pojdite na stran s seznamom **Vsi prodajni nalogi** in ustvarite nov prodajni nalog.</span><span class="sxs-lookup"><span data-stu-id="2b725-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="2b725-116">Izbrati boste morali projekt za prodajni nalog.</span><span class="sxs-lookup"><span data-stu-id="2b725-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="2b725-117">Ko bo projekt izbran, bo stranka nastavljena iz vira financiranja, če pa ima projektna pogodba več virov financiranja, boste morali izbrati vir financiranja.</span><span class="sxs-lookup"><span data-stu-id="2b725-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]