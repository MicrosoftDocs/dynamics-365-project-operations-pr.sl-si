---
title: Projekti ocene prihodkov s fiksno ceno
description: Ta tema vsebuje informacije o prihodkih s fiksno ceno v projektih.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278933"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="eb773-103">Projekti ocene prihodkov s fiksno ceno</span><span class="sxs-lookup"><span data-stu-id="eb773-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="eb773-104">_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_</span><span class="sxs-lookup"><span data-stu-id="eb773-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eb773-105">Ko ustvarite podrobnosti pogodbe projekta z naslednjimi atributi v aplikaciji Dynamics 365 Project Operations prek Microsoft Dataverse, sistem samodejno ustvari projekt ocene prihodka s fiksno ceno.</span><span class="sxs-lookup"><span data-stu-id="eb773-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="eb773-106">Informacije v tem projektu temeljijo na naslednjih dejavnikih:</span><span class="sxs-lookup"><span data-stu-id="eb773-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="eb773-107">Način obračunavanja po fiksni ceni.</span><span class="sxs-lookup"><span data-stu-id="eb773-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="eb773-108">Povezani projekt.</span><span class="sxs-lookup"><span data-stu-id="eb773-108">An associated project.</span></span>
  - <span data-ttu-id="eb773-109">Vsaj en mejnik, opredeljen v zavihku **Razpored izdajanja računov** na strani **Podrobnosti pogodbe projekta**.</span><span class="sxs-lookup"><span data-stu-id="eb773-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="eb773-110">Pregled projektov ocen prihodkov s fiksno ceno</span><span class="sxs-lookup"><span data-stu-id="eb773-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="eb773-111">Če želite pregledati projekte ocen prihodkov s fiksnimi cenami, izvedite naslednje korake:</span><span class="sxs-lookup"><span data-stu-id="eb773-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="eb773-112">V okolju Dynamics 365 Finance odprite **Upravljanje projektov in računovodstvo** > **Projekti** > **Projekti ocene prihodkov s fiksno ceno**.</span><span class="sxs-lookup"><span data-stu-id="eb773-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="eb773-113">Izberite projekt, ki si ga želite ogledati, in dvokliknite možnost **ID ocene projekta**, da odprete zapis in pregledate podrobnosti projekta.</span><span class="sxs-lookup"><span data-stu-id="eb773-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="eb773-114">Razširite zavihek **Projekt**. Projekt se vam bo prikazal v mreži **Izbrani projekti**.</span><span class="sxs-lookup"><span data-stu-id="eb773-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="eb773-115">Sistem ga uporablja kot privzeti projekt, saj je povezan s podrobnostmi pogodbe projekta.</span><span class="sxs-lookup"><span data-stu-id="eb773-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="eb773-116">Če želite spremeniti povezavo, izberite dodatne projekte in jih dodajte v mrežo **Izbrani projekti**.</span><span class="sxs-lookup"><span data-stu-id="eb773-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="eb773-117">Če je v tej mreži izbranih več projektov, se odstotek dokončanosti projekta in ocene prihodkov izračunajo skupaj za vse izbrane projekte.</span><span class="sxs-lookup"><span data-stu-id="eb773-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="eb773-118">Stroške projekta, profil prihodka, predlogo stroškov in kodo obdobja lahko nastavite ročno.</span><span class="sxs-lookup"><span data-stu-id="eb773-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="eb773-119">Če jih ne nastavite ročno, se med prvim izračunom ocene projekta uporabijo privzete vrednosti s pomočjo pravil, konfiguriranih za stroške projekta in profile prihodkov.</span><span class="sxs-lookup"><span data-stu-id="eb773-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]