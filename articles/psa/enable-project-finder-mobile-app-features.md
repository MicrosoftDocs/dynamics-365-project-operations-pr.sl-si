---
title: Omogočanje funkcij aplikacije Project Finder Mobile
description: Kako omogočiti funkcije aplikacije Project Finder Mobile za rešitev Project Service
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
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132983"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="a2cf8-103">Omogočanje funkcij aplikacije Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="a2cf8-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a2cf8-104">Vaši viri lahko aplikacijo Project Finder Mobile v svojih telefonih uporabljajo skupaj s programom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], da najdejo nove delovne projekte in posodobijo svoje veščine.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="a2cf8-105">Aplikacija je na voljo za naprave [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] in [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="a2cf8-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="a2cf8-106">V nastavitvah parametrov vaše organizacijske enote je treba nastaviti določene možnosti, s čimer uporabnikom omogočite ogled zahtevanih veščin za izvedbo projektov in posodobitev svojih veščin.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a2cf8-107">Aplikacija Project Finder Mobile deluje le z aplikacijo [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], ne pa s primerki, nameščenimi na mestu uporabe.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="a2cf8-108">Odprite **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="a2cf8-109">Kliknite nastavitev parametrov, ki jih želite uporabiti za omogočanje funkcij aplikacije Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="a2cf8-110">V razdelku **Splošno** možnost **Zahtevani pogoji za vir so vidni virom** nastavite na **Da**.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="a2cf8-111">Možnost **Dovoli virom posodobitev znanja** nastavite na **Da**.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="a2cf8-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="a2cf8-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="a2cf8-113">To je splošna nastavitev.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-113">This is a global setting.</span></span> <span data-ttu-id="a2cf8-114">Vodje projektov lahko nastavijo, ali naj bo posamezen projekt viden na strani **projektne ekipe**, ki ga izvaja.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="a2cf8-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="a2cf8-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="a2cf8-116">E-poštna obvestila</span><span class="sxs-lookup"><span data-stu-id="a2cf8-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="a2cf8-117">pošilja e-poštna sporočila glede zahtev za vire tem prejemnikom ob naslednjih dogodkih:</span><span class="sxs-lookup"><span data-stu-id="a2cf8-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="a2cf8-118">Prejemnik</span><span class="sxs-lookup"><span data-stu-id="a2cf8-118">Recipient</span></span>|<span data-ttu-id="a2cf8-119">Dogodek</span><span class="sxs-lookup"><span data-stu-id="a2cf8-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="a2cf8-120">Vodja projektov</span><span class="sxs-lookup"><span data-stu-id="a2cf8-120">Project manager</span></span>|<span data-ttu-id="a2cf8-121">-   Ko se vir prijavi za projekt v aplikaciji Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="a2cf8-122">Vir</span><span class="sxs-lookup"><span data-stu-id="a2cf8-122">Resource</span></span>|<span data-ttu-id="a2cf8-123">-   Ko projektno delo, za katerega se je vir prijavil, že opravi drug vir.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="a2cf8-124">-   Ko je zahteva vira za odobritev znanja odobrena ali zavrnjena.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="a2cf8-125">-   Ko je prijava vira za projekt odobrena ali zavrnjena.</span><span class="sxs-lookup"><span data-stu-id="a2cf8-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="a2cf8-126">Obvestilo o zasebnosti</span><span class="sxs-lookup"><span data-stu-id="a2cf8-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="a2cf8-127">Glejte tudi</span><span class="sxs-lookup"><span data-stu-id="a2cf8-127">See Also</span></span>  
 [<span data-ttu-id="a2cf8-128">Nastavitev virov</span><span class="sxs-lookup"><span data-stu-id="a2cf8-128">Set up resources</span></span>](../psa/set-up-resources.md)
