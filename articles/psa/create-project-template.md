---
title: Ustvarjanje projektne predloge
description: Navodila za ustvarjanje predloge projekta v rešitvi Project Service
author: ruhercul
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
ms.openlocfilehash: 700d1bb1fd7299b49b6c6f8e4d84d14bc1d52c1a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084769"
---
# <a name="create-a-project-template-project-service"></a>Ustvarjanje predloge projekta (rešitev Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Če se vaše podjetje redno poteguje za podobne vrste projektov, boste s projektnimi predlogami prihranili čas. Vsebujejo standardni nabor vlog in predvidenih ur za določeno vrsto projekta. Vodje za upravljanje kupcev in vodje projektov lahko ustvarijo projekte, ki temeljijo na projektni predlogi, ali pa kopirajo predlogo in naredijo svojo.  
  
## <a name="components-of-project-template"></a>Komponente projektne predloge
 Projektna predloga je sestavljena iz treh delov:  
  
- **Strukturirana členitev dela** : strukturirana členitev dela v projektni predlogi vsebuje enak nabor elementov kot v projektu. Ustvarite lahko hierarhijo opravil, povežete vloge z opravilom, določite atribute načrtovanja, nastavite odvisnosti in si vse podatke ogledate v Ganttovem grafikonu. Strukturirana členitev dela v projektnih predlogah za vsako opravilo podpira tudi način opravila. Če ustvarjate načrtovanje dela, med projektno predlogo in projektom ni razlik.  
  
- **Ocene za projekte** : v predlogah ocene za projekte delujejo na enak način kot v projektih, saj so z izjemo cenikov za privzeto lastne in prodajne cene vedno privzete lastne in prodajne cene cenikov, ki so določeni s parametri [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Preostale funkcije so enake kot v projektu.  
  
- **Oblikovanje projektne ekipe** : ko za projektno predlogo oblikujete projektno ekipo, v predlogi ne morete rezervirati poimenskega vira. Če želite ustvariti nabor splošnih virov, lahko v strukturirani členitvi dela uporabite **Ustvari projektno ekipo**. Za splošne vire lahko določite tudi zahtevane spretnosti in usposobljenost. V predlogah projekta ne morete nadomestiti splošnega vira z virom, ki ga je mogoče rezervirati.  
  
## <a name="create-a-project-from-a-template"></a>Ustvari projekt iz predloge  
 Iz predloge lahko projekt ustvarite na naslednje načine:  
  
-   Če ustvarjate projekt iz ponudbe, lahko projektno predlogo izberete v obrazcu za hitro ustvarjanje projekta.  
  
-   Če ustvarite projekt s klikom **Nov projekt** , se obrazec projekta prikaže, še preden shranite zapis. Tukaj lahko kliknete polje **Izberi predlogo** in jo izberete s seznama vnaprej določenih projektnih predlog v vaši organizaciji.  
  
-   Na strani **Projektna predloga** kliknite **Ustvari projekt iz predloge** , da ustvarite projekt iz predloge.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Kopiranje komponent predloge v projekt  
 Ko kopirate komponente predloge v projekt, morate vedeti nekaj stvari.  
  
 **Kopiranje strukturirane členitve dela** : če ima projekt drugačen projektni koledar kot predloga, bodo po kopiranju strukturirane členitve dela iz projektne predloge pri načrtovanju opravil uporabljene delovne ure iz koledarja projekta. To prilagodi načrtovanje varnostnemu koledarju projekta. Podobno ima tudi prvo opravilo v strukturirani členitvi dela začetni datum projekta, da se preostanek načrtovanja hierarhije opravil posodobi glede na trajanje in odvisnosti, ki sta navedena v strukturirani členitvi dela predloge.  
  
 **Kopiranje ocen projekta** : pri kopiranju čez vrstice projektnih ocen se ceniki posodobijo glede na lastniško enoto projekta za cenik z lastnimi cenami in stranke za prodajni cenik. Lastne cene in prodajne cene enote se določijo iz teh cenikov za projekte, ki so povezani z entiteto prodaje.  
  
 **Kopiranje projektne ekipe** : Ko projektno ekipo kopirate iz predloga v projekt, se prekopirajo tudi splošni viri, skupaj s spretnostmi in usposobljenostjo, opredeljenimi v predlogi. Ohranijo se tudi naloge splošnega vira tako kot v projektni predlogi.  
  
### <a name="see-also"></a>Glejte tudi  
 [Priročnik za vodje projektov](../psa/project-manager-guide.md)
