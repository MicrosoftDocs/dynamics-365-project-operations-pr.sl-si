---
title: Ustvarjanje projektne predloge
description: Navodila za ustvarjanje predloge projekta v rešitvi Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 07/19/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8159e0390441e5029f9beb0228cffcbc4d683479
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177446"
---
# <a name="create-a-project-template-project-service"></a>Ustvarjanje predloge projekta (rešitev Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Če se vaše podjetje redno poteguje za podobne vrste projektov, boste s projektnimi predlogami prihranili čas. Vsebujejo standardni nabor vlog in predvidenih ur za določeno vrsto projekta. Vodje za upravljanje kupcev in vodje projektov lahko ustvarijo projekte, ki temeljijo na projektni predlogi, ali pa kopirajo predlogo in naredijo svojo.  
  
## <a name="components-of-project-template"></a>Komponente projektne predloge
 Projektna predloga je sestavljena iz treh delov:  
  
- **Strukturirana členitev dela**: strukturirana členitev dela v projektni predlogi vsebuje enak nabor elementov kot v projektu. Ustvarite lahko hierarhijo opravil, nalogi povežete vloge, definirate atribute urnika, nastavite odvisnosti in si ogledate vse podatke v Gantt. Struktura razčlenitve dela v projektnih predlogah podpira tudi načine opravil za vsako opravilo. Med predlogo projekta in projektom pri izdelavi urnika dela ni razlike.  
  
- **Ocene za projekte**: v predlogah ocene za projekte delujejo na enak način kot v projektih, saj so z izjemo cenikov za privzeto lastne in prodajne cene vedno privzete lastne in prodajne cene cenikov, ki so določeni s parametri [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Preostale funkcije so enake kot v projektu.  
  
- **Oblikovanje projektne ekipe**: ko za projektno predlogo oblikujete projektno ekipo, v predlogi ne morete rezervirati poimenskega vira. Če želite ustvariti nabor splošnih virov, lahko v strukturirani členitvi dela uporabite **Ustvari projektno ekipo**. Za splošne vire lahko določite tudi zahtevane spretnosti in usposobljenost. V predlogah projekta ne morete nadomestiti splošnega vira z virom, ki ga je mogoče rezervirati.  

## <a name="create-a-project-template-from-an-existing-project"></a>Ustvarite predlogo projekta iz obstoječega projekta
Predlogo projekta lahko ustvarite iz projekta na naslednje načine:

- **Struktura razčlenitve dela** : Struktura razčlenitve dela v predlogi, ki izhaja iz projekta, bo kopirala vse naloge in odvisnosti. Ustvarjene dodelitve bodo temeljile na generičnih članih skupine, ki so dodani projektni skupini, ko je ustvarjena predloga projekta.
- **Ocene projekta** : Ko je predloga projekta ustvarjena iz obstoječega projekta, se ocene iz izvornega projekta prekopirajo v predlogo projekta.
- **Člani projektne skupine** : Ko je predloga ustvarjena iz obstoječega projekta, so vsi imenovani člani skupine nadomeščeni z generičnim virom organizacije. Ohranjajo se vsa imena položajev in vloge.

## <a name="create-a-project-from-a-template"></a>Ustvari projekt iz predloge  
 Projekt lahko ustvarite iz predloge na naslednje načine:  
  
-   Če ustvarjate projekt iz ponudbe, lahko projektno predlogo izberete v obrazcu za hitro ustvarjanje projekta.  
  
-   Če ustvarite projekt s klikom **Nov projekt**, se obrazec projekta prikaže, še preden shranite zapis. Tukaj lahko kliknete polje **Izberi predlogo** in jo izberete s seznama vnaprej določenih projektnih predlog v vaši organizaciji.  
  
-   Na strani **Projektna predloga** kliknite **Ustvari projekt iz predloge**, da ustvarite projekt iz predloge.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Kopiranje komponent predloge v projekt  
 Ko kopirate komponente predloge v projekt, morate vedeti nekaj stvari.  
  
 **Kopiranje strukturirane členitve dela**: če ima projekt drugačen projektni koledar kot predloga, bodo po kopiranju strukturirane členitve dela iz projektne predloge pri načrtovanju opravil uporabljene delovne ure iz koledarja projekta. To prilagodi načrtovanje varnostnemu koledarju projekta. Podobno ima tudi prvo opravilo v strukturirani členitvi dela začetni datum projekta, da se preostanek načrtovanja hierarhije opravil posodobi glede na trajanje in odvisnosti, ki sta navedena v strukturirani členitvi dela predloge.  
  
 **Kopiranje ocen projekta**: pri kopiranju čez vrstice projektnih ocen se ceniki posodobijo glede na lastniško enoto projekta za cenik z lastnimi cenami in stranke za prodajni cenik. Lastne cene in prodajne cene enote se določijo iz teh cenikov za projekte, ki so povezani z entiteto prodaje.  
  
 **Kopiranje projektne ekipe**: Ko projektno ekipo kopirate iz predloga v projekt, se prekopirajo tudi splošni viri, skupaj s spretnostmi in usposobljenostjo, opredeljenimi v predlogi. Ohranijo se tudi naloge splošnega vira tako kot v projektni predlogi.  
  
### <a name="see-also"></a>Glejte tudi  
 [Priročnik za vodje projektov](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
