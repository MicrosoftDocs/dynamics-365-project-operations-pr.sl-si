---
title: Domača stran za poročanje
description: Ta tema vsebuje informacije o poročanju v aplikaciji Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 78c62f69c6529669789a461f1ded8e3ea5f8219e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283298"
---
# <a name="reporting-home-page"></a><span data-ttu-id="b989d-103">Domača stran poročanja</span><span class="sxs-lookup"><span data-stu-id="b989d-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b989d-104">Storitev Microsoft Dynamics 365 Project Service Automation omogoča učinkovito upravljanje poslovanja organizacijam, v katerih poslovanje poteka na podlagi projektov.</span><span class="sxs-lookup"><span data-stu-id="b989d-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="b989d-105">Pri vsakem projektu morajo člani ekipe upravljati priložnosti, pošiljati ponudbe in načrtovati delo, razporejati vire za projekte, upravljati delo v skladu z načrtom, obračunati delo in opraviti vse potrebno za dokončanje projekta.</span><span class="sxs-lookup"><span data-stu-id="b989d-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="b989d-106">Zmožnost poročanja o postopkih je ključnega pomena za določanje stanja organizacije in sprejemanje potrebnih popravljalnih dejanj.</span><span class="sxs-lookup"><span data-stu-id="b989d-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="b989d-107">PSA uporablja metode in tehnologije poročanja, uporabljene v aplikaciji Microsoft Dynamics 365, za vse svoje postopke poročanja.</span><span class="sxs-lookup"><span data-stu-id="b989d-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="b989d-108">Za več informacij o možnostih poročanja si oglejte [Vodnik za pisanje poročil za Dynamics 365 Customer Engagement (on-premises), različica 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="b989d-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="b989d-109">Čarovnik za poročila</span><span class="sxs-lookup"><span data-stu-id="b989d-109">Report Wizard</span></span>

<span data-ttu-id="b989d-110">Čarovnik za poročila omogoča ustvarjanje preprostih poročil uporabnikom, ki niso razvijalci.</span><span class="sxs-lookup"><span data-stu-id="b989d-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="b989d-111">Ker je aplikacija zgrajena na obstoječi platformi, je izkušnja enaka kot tista, opisana v temi [Ustvarjanje ali urejanje poročila s Čarovnikom za poročila](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="b989d-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="b989d-112">Uporabili pa boste entitete, specifične za Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b989d-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="b989d-113">Poročila po meri za storitve SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="b989d-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="b989d-114">Če vaše podjetje zahteva posebno poročilo, ki ga ni mogoče ustvariti s Čarovnikom za poročila, lahko ustvarite poročilo po meri.</span><span class="sxs-lookup"><span data-stu-id="b989d-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="b989d-115">Nameščeno morate imeti aplikacijo Microsoft Visual Studio, skupaj z ustreznimi razširitvami za ustvarjanje poročil in za Microsoft SQL Server Data Tools.</span><span class="sxs-lookup"><span data-stu-id="b989d-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="b989d-116">Za več informacij o orodjih in različicah glejte temo [Okolje za pisanje poročil z uporabo SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="b989d-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="b989d-117">Za več informacij o ustvarjanju poročil po meri glejte temo [Ustvarjanje novega poročila z uporabo SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="b989d-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="b989d-118">Aplikacije za vpogled Power BI</span><span class="sxs-lookup"><span data-stu-id="b989d-118">Power BI insights apps</span></span>

<span data-ttu-id="b989d-119">Skupna uporaba aplikacij Microsoft Power BI in Dynamics 365 predstavlja učinkovit način za delo s podatki v obliki aplikacij za vpogled.</span><span class="sxs-lookup"><span data-stu-id="b989d-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="b989d-120">Za več informacij o razpoložljivosti aplikacij za vpogled glejte temo [Stran z aplikacijami za vpogled Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="b989d-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="b989d-121">Dodatni viri</span><span class="sxs-lookup"><span data-stu-id="b989d-121">Additional resources</span></span>
<span data-ttu-id="b989d-122">Za več informacij o poročanju v PSA si oglejte naslednje teme:</span><span class="sxs-lookup"><span data-stu-id="b989d-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="b989d-123">Delo s podatkovnim modelom storitve Project Service</span><span class="sxs-lookup"><span data-stu-id="b989d-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="b989d-124">Nadzorne plošče</span><span class="sxs-lookup"><span data-stu-id="b989d-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]