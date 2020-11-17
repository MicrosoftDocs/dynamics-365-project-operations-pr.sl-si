---
title: Konfiguracija nastavitev dodatnih parametrov
description: Navodila za konfiguracijo nastavitev dodatnih parametrov v rešitvi Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 24a4fe83471da916fb91cfe20e739279c08d8e5e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084756"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Konfiguracija nastavitev dodatnih parametrov (rešitev Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ko ste konfigurirali elemente v prejšnjih temah, morate nastaviti še dodatne parametre projekta, ki jih boste uporabljali za svoje projekte. Ob prvi namestitvi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ste ustvarili nastavitev parametrov, s katero ste najprej ustvarili vse zapise, ki so potrebni za delovanje [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Zdaj je čas, da se vrnete nazaj in konfigurirate dodatna polja za te nastavitve.  
  
 Konfigurirati boste morali naslednje nastavitve:  
  
-   Organizacijska enota  
  
-   Pogostost izdajanja računov  
  
-   Predloga delovnih ur  
  
-   Cenik  
 
V tem koraku tudi navedite, katero vrsto dodeljevanja sredstev želite:  
  
- **Osrednji**. Le upravitelji virov lahko projektom dodeljujejo vire.  
  
- **Hibridno**. Upravitelji virov, upravitelji projektov in upravitelji kupcev lahko projektom dodeljujejo vire.  
  
 
Nastavitev parametra projekta:  
  
1. Odprite **Project Service > Parametri**.  
  
2. Kliknite nastavitev parametrov, ki jo želite konfigurirati (tisto, ki ste jo ustvarili, ko ste prvič namestili [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), ali pa kliknite **Novo** , če želite ustvariti novo nastavitev.  
  
3. V območju **Splošno** nastavite vse možnosti za svoje parametre projekta.  
  
4. Če želite dodati cenik, v območju **Cenik** kliknite **+** , da izberete cenik s spustnega seznama **Cenik parametra projekta** , in nato kliknite **Shrani**.  
  
5. Kliknite gumb **Shrani** v spodnjem desnem kotu zaslona.  

> [!NOTE]
> Zapis parametra projekta mora biti vzdrževan, da rešitev Project Service deluje pravilno. Tega zapisa se ne sme izbrisati.

### <a name="see-also"></a>Glejte tudi  
 [Nastavitev virov](../psa/set-up-resources.md)