---
title: Ustvarjanje ročnega predračuna – poenostavljena različica
description: Ta tema vsebuje informacije o ustvarjanju ročnih predračunov v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764523"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="917d4-103">Ustvarjanje ročnega predračuna – poenostavljena različica</span><span class="sxs-lookup"><span data-stu-id="917d4-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="917d4-104">_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_</span><span class="sxs-lookup"><span data-stu-id="917d4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="917d4-105">V aplikaciji Dynamics 365 Project Operations se predračuni lahko ustvarijo ročno po potrebi.</span><span class="sxs-lookup"><span data-stu-id="917d4-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="917d4-106">Predračun lahko ročno ustvarite iz strani s seznamom **Projektne pogodbe** ali s strani s podrobnostmi **Projektna pogodba**.</span><span class="sxs-lookup"><span data-stu-id="917d4-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="917d4-107">Stran s seznamom projektnih pogodb</span><span class="sxs-lookup"><span data-stu-id="917d4-107">Project Contracts list page</span></span>

<span data-ttu-id="917d4-108">Na strani s seznamom **Projektne pogodbe** izberite eno ali več projektnih pogodb in ustvarite račune za vse izbrane zapise.</span><span class="sxs-lookup"><span data-stu-id="917d4-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="917d4-109">Sistem preveri, katera od izbranih projektnih pogodb ima nedokončana opravila **Pripravljeno na izdajanje računa**, ki so bila ustvarjena pred današnjim dnem.</span><span class="sxs-lookup"><span data-stu-id="917d4-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="917d4-110">Iz teh pogodb sistem ustvari osnutke predračunov.</span><span class="sxs-lookup"><span data-stu-id="917d4-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="917d4-111">Če ima projektna pogodba več strank, je lahko ustvarjen en račun na stranko in več računov na projektno pogodbo.</span><span class="sxs-lookup"><span data-stu-id="917d4-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="917d4-112">Vsi ustvarjeni projektni računi so na voljo na strani **Račun** v razdelku **Obračunavanje** območja **Prodaja**.</span><span class="sxs-lookup"><span data-stu-id="917d4-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="917d4-113">Stran s podrobnostmi o projektni pogodbi</span><span class="sxs-lookup"><span data-stu-id="917d4-113">Project Contract details page</span></span>

<span data-ttu-id="917d4-114">Predračun lahko ustvarite tudi na strani s podrobnostmi o **projektni pogodbi**.</span><span class="sxs-lookup"><span data-stu-id="917d4-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="917d4-115">Sistem preveri, ali ima projektna pogodba nedokončano opravilo **Pripravljeno na izdajanje računa**, ki je bilo ustvarjeno pred današnjim dnem.</span><span class="sxs-lookup"><span data-stu-id="917d4-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="917d4-116">Iz teh pogodb sistem ustvari osnutke predračunov na podlagi števila strank v vsaki podrobnosti pogodbe.</span><span class="sxs-lookup"><span data-stu-id="917d4-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="917d4-117">Ko je ustvarjen prvi predračun, se odpre stran **Račun**.</span><span class="sxs-lookup"><span data-stu-id="917d4-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="917d4-118">Če je za to projektno pogodbo ustvarjenih več računov, se odpre stran s seznamom **Računi**, na katerem so prikazani vsi ustvarjeni računi.</span><span class="sxs-lookup"><span data-stu-id="917d4-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
