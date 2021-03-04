---
title: Omogočanje funkcij aplikacije Project Finder Mobile
description: Kako omogočiti funkcije aplikacije Project Finder Mobile za rešitev Project Service
author: JohnPBurrows
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: 1b70182125d607aa17528ef3dc4ea2345b76acd1
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144568"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Omogočanje funkcij aplikacije Project Finder Mobile (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vaši viri lahko uporabljajo aplikacijo Project Finder Mobile v svojih telefonih skupaj z rešitvijo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], da najdejo nove delovne projekte in nadgradijo svoje veščine.  
  
 Aplikacija je na voljo za naprave [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] in [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
    
 Če želite uporabnikom omogočiti ogled zahtevanih pogojev za vir projekta in nadgradnjo veščin, morate v nastavitvah parametrov vaše organizacijske enote izbrati možnosti.
  
> [!NOTE]
>  Aplikacija Project Finder Mobile deluje le z aplikacijo [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], ne pa s primerki, nameščenimi na mestu uporabe.  
  
1. Odprite **Project Service > Parametri**.  
  
2. Kliknite nastavitev parametrov, ki jih želite uporabiti za omogočanje funkcij aplikacije Project Finder Mobile.  
  
3. V razdelku **Splošno** možnost **Zahtevani pogoji za vir so vidni virom** nastavite na **Da**.  
  
4. Možnost **Dovoli virom posodobitev znanja** nastavite na **Da**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   To je splošna nastavitev. Vodje projektov lahko nastavijo, ali naj bo posamezen projekt viden na strani **projektne ekipe**, ki ga izvaja.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>E-poštna obvestila  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pošilja e-poštna sporočila glede zahtev za vire tem prejemnikom ob naslednjih dogodkih:  
  
|Prejemnik|Dogodek|  
|---------------|-----------|  
|Vodja projektov|– Vir se prijavi za projekt v aplikaciji Project Finder Mobile.|  
|Vir|– Projektno delo, za katerega se je prijavil vir, je že opravil drug vir.<br />– Zahteva za odobritev veščin je odobrena ali zavrnjena.<br />– Zahteva za prijavo na projektno delo je odobrena ali zavrnjena.|  
  
## <a name="privacy-notice"></a>Izjava o zasebnosti  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Glejte tudi  
 [Nastavitev virov](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]