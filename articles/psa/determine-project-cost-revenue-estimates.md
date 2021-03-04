---
title: Ocena stroškov in prihodkov projekta
description: Navodila za določanje stroškov projekta in ocenjenih prihodkov v rešitvi Project Service
author: ruhercul
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
ms.openlocfilehash: a91e988632d2b2cdebfe7fd17516c5d6886728fc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148843"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Ocena stroškov in prihodkov projekta 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ocene projekta omogočajo finančni pregled za predvideno in načrtovano delo v strukturirani členitvi dela projekta. Pogled ocen vam prikaže stroške in prihodke načrtovanega dela. Pogled ocen zagotavlja orodje za prikaz informacij o številnih predhodno določenih dimenzijah, da boste o finančnem vplivu projekta kar najbolje obveščeni.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Stroški in prodajna vrednost projekta  
Ceniki [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] določajo stroške in zneske računov za vloge, ki se uporabljajo v projektih. Glede na vloge, povezane z opravilom v strukturirani členitvi dela projekta, lahko določite stroške in prihodke vključenega dela.  
  
## <a name="cost-price-defaulting"></a>Privzeto nastavljanje lastne cene  
Vsak projekt pripada organizacija (označeno v možnosti **Lastniška enota** v projektu). Lastno ceno enote določa cenik, povezan z lastniško organizacijsko enoto. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] določajo lastne cene za vloge tako, da v ceniku z lastnimi cenami poiščejo kombinacijo vloge, enote in organizacijske enote ter tako dobijo ustrezno lastno ceno z datumom začetka veljavnosti v vrsticah z ocenami.  
  
Če kombinacija vloge, enote in organizacijske enote ne ustvari lastne cene s cenika lastniške enote, se enota prezre v korist kombinaciji vloge in organizacijske enote. Če obstaja lastna cena, je ta cena pretvorjena v enoto, ki jo izberete v vrstici z ocenami.  
  
Če kombinacija vloge in organizacijske enote ne ustvari lastne cene, se organizacijsko enoto prezre v korist kombinaciji vloge in enote, cena pa je privzeto nastavljena, po tem ko uporabite poljubno pretvorbo, če je to potrebno.  
  
 Če za vlogo ni cene, je lastna cena v vrstici z ocenami privzeto nastavljena na 0,00.  
  
 Vsi zneski stroškov v vrsticah z ocenami stroškov projekta so navedeni v valuti lastniške organizacijske enote.  
  
## <a name="sales-price-defaulting"></a>Privzeto nastavljanje prodajne cene  
Cenik prodaje temelji na entiteti prodaje, s katero je povezan projekt. Ceno prodaje določa cenik prodaje, povezan s ponudbo ali pogodbo. Če ima ponudba ali pogodba cenik po meri, je to privzeti cenik prodaje za ocene projekta. Če povezave z entitetami prodaje ni, bo privzeti cenik prodaje v nastavitvah parametrov privzeti cenik prodaje za projekt. Vsaka vrstica z ocenami ima organizacijsko enoto z viri, ki je povezana z označevanjem organizacijske enote, prek katere bodo rezervirani viri za dokončanje opravila. Prodajna cena za povezane vloge je določena tako, da v ceniku prodaje poiščejo kombinacijo vloge, enote in organizacijske enote vira ter tako dobijo ustrezno prodajno ceno z datumom začetka veljavnosti v vrsticah z ocenami.  
  
Če kombinacija vloge, enote in organizacijske enote vira ne prinese lastne prodajne cene s cenika prodaje, sistem enoto prezre in poišče kombinacijo vloge in organizacijske enote vira. Če je najdena prodajna cena, se pretvori v enoto, ki jo izberete v vrstici z ocenami prodaje.  
  
Če sistem za vlogo ne najde cene, mora biti prodajna cena v vrstici z ocenami privzeto nastavljena na 0,00.  
  
Ogled ocen je mrežni pogled, ki prikazuje ravno mrežo vrstic z ocenami z enoto in skupnimi stroški ter prodajno ceno.  
  
## <a name="time-phased-view-of-project-estimates"></a>Časovno razporejeni pogled ocen projekta  
V časovno razporejenem prikazu za ocene projekta so ocenjeni podatki iz pogleda mreže privzeto obrnjeni glede na vlogo in kažejo razširitev ocenjenih podatkov prek časovnice v izbranem časovnem merilu.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Ocenjena dodelitev obsega dela glede na način opravila  
V časovno razporejenem prikazu je skupna ocenjena dodelitev obsega dela porazdeljena tako, da se dodeli določeno število ur obsega dela na časovno obdobje enote izbranega časovnega merila. V rešitvi Project Service način opravila določa razporejenost obsega dela v času trajanja opravila. Dve vrsti dodelitve sta enakomerna dodelitev in dodelitev glede na delovne ure. 
  
## <a name="work-hours-based-allocation"></a>Dodelitev glede na delovne ure  
Način opravila samodejnega načrtovanja za opravilo določa, da so številni viri, ocenjenih v sklopu opravila, ocenjeni za uporabo za polni delovni čas na dan. To velja pri dodeljevanju obsega dela tako, da ga razdelite glede na trajanje opravil tudi v časovno razporejenem prikazu. Na primer časovno merilo na »Dan« za opravilo, za katerega se oceni, da ga dokonča en vir, obseg dela na dan ne bo presegel delovnih ur na dan, ki so določene v koledarju projekta. Zato je z dodeljevanjem obsega dela vedno poskrbljeno, da so viri ocenjeni za uporabo cel dan.  
  
## <a name="even-distribution"></a>Enakomerna porazdelitev  
Način ročno načrtovanih opravil ne spoštuje delovnih ur, koledarja projekta ali števila virov, določenih za opravilo. Urnik opravil temelji na vnosu uporabnika. Za take naloge dodeljevanje obsega dela na časovno obdobje enote izbranega časovnega merila nima omejitvenih dejavnikov. Skupen obseg dela, povezan z opravilom, se enakomerno razdeli in dodeli za vsako časovno obdobje enote na izbranem časovnem merilu.  
  
Na ta način opravilo, določeno v sklopu opravila, določa porazdelitev obsega dela ali dodelitev obsega dela na časovno obdobje enote v časovno razporejenih ocenah.  
  
## <a name="grouping-and-time-phasing-options"></a>Možnosti združevanja in časovnega razporejanja  
Ta pogled vam pomaga razumeti porazdelitev obsega dela, stroškov in ocen prodaje na dan, teden, mesec ali leto. Možnost »Združi po« omogoča obračanje podatkov ocenjevanja še v sklopu dveh dimenzij: kategorija in viri. Tako v pogledu mreže kot tudi v časovno razporejenem pogledu lahko izberete polja za prikaz. Skupne vrednosti za posamezne časovne bloke so prikazane na dnu, prikazani so tudi skupni ocenjeni obseg dela, stroški in prodaja za dan, teden, mesec ali leto.  
  
Privzeta lastna cena in prodajna cena imata datum začetka veljavnosti. Ko se spremenijo tečaji za vloge, bo prikaz bolj jasen v časovnem razporedu, kjer si lahko ogledate ocenjene podatke, obrnjene v možnosti »Vir« in časovno razporejene na teden.  
  
## <a name="expense-estimates"></a>Ocena stroškov  
Vse stroške, ki bodo nastali v projektu in niso neposredno povezani z delom, lahko zabeležite v ocene projekta v mrežnem pogledu. Uporabite možnost **Dodaj oceno stroškov** v mrežnem pogledu in to lahko izvedete. Ocene stroškov lahko zabeležite za določeno opravilo ali za celoten projekt. V teh vrsticah lahko izberete kategorije stroškov in predvideni datum, ko naj bi nastali stroški. Če imajo povezani stroški in cenik prodaje privzete cene ali odstotke pribitka, določene za kategorije stroškov, bo to privzeto vključeno v vrstico z ocenami družbe.  
  
### <a name="see-also"></a>Glejte tudi  
 [Priročnik za vodje projektov](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]