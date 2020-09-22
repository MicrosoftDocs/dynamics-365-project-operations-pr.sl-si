---
title: Omogočanje funkcij aplikacije Project Finder Mobile
description: Kako omogočiti funkcije aplikacije Project Finder Mobile za rešitev Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755730"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Omogočanje funkcij aplikacije Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vaši viri lahko aplikacijo Project Finder Mobile v svojih telefonih uporabljajo skupaj s programom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], da najdejo nove delovne projekte in posodobijo svoje veščine.  
  
 Aplikacija je na voljo za naprave [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] in [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 V nastavitvah parametrov vaše organizacijske enote je treba nastaviti določene možnosti, s čimer uporabnikom omogočite ogled zahtevanih veščin za izvedbo projektov in posodobitev svojih veščin.  
  
> [!NOTE]
>  Aplikacija Project Finder Mobile deluje le z aplikacijo [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], ne pa s primerki, nameščenimi na mestu uporabe.  
  
1. Odprite **Project Service > Parametri**.  
  
2. Kliknite nastavitev parametrov, ki jih želite uporabiti za omogočanje funkcij aplikacije Project Finder Mobile.  
  
3. V razdelku **Splošno** možnost **Zahtevani pogoji za vir so vidni virom** nastavite na **Da**.  
  
4. Možnost **Dovoli virom posodobitev znanja** nastavite na **Da**.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   To je splošna nastavitev. Vodje projektov lahko nastavijo, ali naj bo posamezen projekt viden na strani **projektne ekipe**, ki ga izvaja.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-poštna obvestila  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pošilja e-poštna sporočila glede zahtev za vire tem prejemnikom ob naslednjih dogodkih:  
  
|Prejemnik|Dogodek|  
|---------------|-----------|  
|Vodja projektov|-   Ko se vir prijavi za projekt v aplikaciji Project Finder Mobile.|  
|Vir|-   Ko projektno delo, za katerega se je vir prijavil, že opravi drug vir.<br />-   Ko je zahteva vira za odobritev znanja odobrena ali zavrnjena.<br />-   Ko je prijava vira za projekt odobrena ali zavrnjena.|  
  
## <a name="privacy-notice"></a>Obvestilo o zasebnosti  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Glejte tudi  
 [Nastavitev virov](../project-service/set-up-resources.md)
