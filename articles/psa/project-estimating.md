---
title: Stroški in prihodki projekta
description: Ta tema vsebuje informacije o ocenjevanju stroškov in prihodkov projekta.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ecac3a08b2405e697eb260bbab991458dbe69f4e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581902"
---
# <a name="project-costs-and-revenue"></a>Stroški in prihodki projekta

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ocene projekta omogočajo finančni pregled za predvideno in načrtovano delo v razporedu projekta. Zavihek **Ocene** na strani **Projekti** prikazuje vpliv stroškov in prihodkov dela, ki ga načrtujete. Vsebuje tudi informacije o številnih vnaprej določenih razsežnostih. 

> ![Zavihek »Ocene«.](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Vrednost stroškov in prodajna vrednost projekta

Ceniki določajo stroške in deleže obračunavanja za vloge v projektih. Vpliv dela na stroške in prihodke lahko določite na podlagi vlog, ki so povezane z nazivom delovnega mesta in poimenovanim virom, ki je dodeljen opravilu. Če obstajajo opravila, ki nimajo dodelitev (splošnih ali poimenovanih), ne morete pridobiti ocen stroškov ali prodaje. Vrednosti stroškov in prodajne vrednosti upoštevajo datum, ki je naveden v ceniku.

### <a name="default-cost-price"></a>Privzeta lastna cena  

Vsak projekt pripada organizaciji. Ta organizacija je prikazana v polju **Pogodbena enota** v projektu. Cenik, ki je povezan s pogodbeno enoto, se uporablja za določanje lastne cene enote. Za določanje pravilnih lastnih cen v vlogah za datum, ki je naveden v vrsticah ocene, v ceniku z lastnimi cenami poiščite kombinacijo vloge, enote in organizacijske enote. 

Za izračun lastnih cen opravil morajo biti vsa opravila dodeljena viru. Vsa nedodeljena opravila imajo lastno ceno 0,00.

Če kombinacija vloge, enote in organizacijske enote ne vrne lastne cene iz cenika pogodbene enote, sistem prezre enoto. Namesto tega poišče kombinacijo zgolj vloge in organizacijske enote. Če je najdena lastna cena, jo faktorji za pretvorbo pretvorijo v enoto, ki ste jo izbrali v vrstici ocene.

Če kombinacija vloge in organizacijske enote ne vrne lastne cene, sistem prezre organizacijsko enoto. Namesto tega poišče kombinacijo vloge in enote, da nastavi privzeto ceno (po uporabi katere koli pretvorbe).

Če sistem ne najde cene za vlogo, je lastna cena v vrstici ocene nastavljena na privzeto vrednost **0,00**. Vsi zneski stroškov v vrsticah z ocenami stroškov projekta so zabeleženi v valuti pogodbene enote.

> [!NOTE]
> Microsoft Dynamics 365 privzeto shranjuje zneske stroškov v vaši osnovni valuti. Vendar pa so zneski stroškov, ki so prikazani na zavihku **Ocene**, v valuti pogodbene enote.  

### <a name="default-sales-price"></a>Privzeta prodajna cena 

Prodajni cenik določi entiteta za prodajo, ki ji je priložen projekt, ali stranka projekta. Če je entiteta za prodajo, na primer priložnost, ponudba ali pogodba, povezana s projektom, je prodajna cena entitete za prodajo določena s cenikom, ki je povezan s ponudbo ali pogodbo. Če ima ponudba ali pogodba cenik po meri, se ta cenik uporabi kot privzeti prodajni cenik za ocene projekta. Če ni povezave z entitetami za prodajo, se kot privzeti prodajni cenik projekta uporabi privzeti prodajni cenik iz parametrov, skupaj z valuto stranke, ki je navedena v projektu.

Vsaka vrstica ocene ima enoto vira, ki je povezana z njo. Enota vira označuje organizacijsko enoto, iz katere so viri rezervirani za dokončanje opravila. Če želite določiti prodajno ceno za povezane vloge, v prodajnem ceniku poiščite kombinacijo vloge, enote in enote vira. Če v opravilu ni dodelitev, je prodajna cena za opravilo 0,00.

Če kombinacija vloge, enote in enote vira ne vrne prodajne cene iz prodajnega cenika, sistem prezre enoto. Namesto tega poišče kombinacijo zgolj vloge in enote vira. Če je najdena prodajna cena, jo faktorji za pretvorbo pretvorijo v enoto, ki ste jo izbrali v vrstici ocene prodaje. 

Če kombinacija vloge in enote vira ne vrne prodajne cene iz prodajnega cenika, sistem prezre enoto vira. Namesto tega poišče kombinacijo vloge in enote, da nastavi privzeto ceno (po uporabi katere koli pretvorbe).

Če sistem ne najde cene za vlogo, je prodajna cena v vrstici ocene nastavljena na privzeto vrednost **0,00**.

Zavihek **Ocene** ima pogled mreže, ki prikazuje vrstice ocene. Mreža vključuje stolpce za enoto, skupno lastno ceno in skupno prodajno ceno, kot je prikazano na spodnji sliki. 

> ![Pogled mreže na zavihku »Ocene«.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Časovno razporejeni pogled ocen projekta

Časovno razporejen pogled ocen projekta prikazuje podatke o oceni iz pogleda omrežja skozi časovnico v izbranem časovnem merilu. Podatki o oceni so privzeto zavrteni v razsežnosti **Vloga**.

> ![Časovno razporejeni pogled za ocene projekta.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Dodeljevanje ocenjenega obsega dela glede na način opravila

V časovno razporejenem prikazu porazdelite skupni obseg dela, ki je ocenjen za opravilo, tako, da dodelite ure obsega dela na časovno obdobje enote v izbranem časovnem merilu. Način opravila določa dodeljevanje obsega dela v času trajanja opravila. Dve vrsti dodelitve sta **Enakomerno** in **Glede na delovne ure**.

### <a name="work-hours-based-allocation"></a>Dodelitev glede na delovne ure
 
V načinu opravila samodejnega razporejanja so dnevne privzete ure za vire opravil nastavljene pri polnem delovnem času. To velja, kadar je obseg dela dodeljen tako, da ga razdelite glede na trajanje opravila v časovno razporejenem prikazu. Če na primer ocenite, da bo v časovnem merilu **Dan** opravilo dokončal en vir, obseg dela, ki je dodeljen na dan, ne bo presegel delovnih ur na dan, ki so določene v koledarju projekta. Zato je z dodeljevanjem obsega dela vedno poskrbljeno, da so viri ocenjeni za uporabo za cel dan.

### <a name="even-allocation"></a>Enakomerna dodelitev

V načinu ročno razporejenega opravila se delovni čas iz koledarja projekta ne uporablja. Namesto tega razpored opravila temelji na uporabnikovem vnosu. Pri teh opravilih dodeljevanje obsega dela na časovno obdobje enote v izbranem časovnem merilu nima omejitvenih dejavnikov. Skupen obseg dela, povezan z opravilom, se enakomerno razdeli in dodeli za vsako časovno obdobje enote v izbranem časovnem merilu. Zato način opravila, ki je določen v opravilu, določa porazdelitev obsega dela ali dodelitev obsega dela na časovno obdobje enote v časovno razporejenih ocenah.

## <a name="grouping-and-time-phasing-options"></a>Možnosti združevanja in časovnega razporejanja

Časovno razporejen pogled prikaže porazdelitev ocen obsega dela, stroškov in prodaje za vsak dan, teden, mesec ali leto. Podatki o oceni so privzeto zavrteni v razsežnosti **Vloga**. Lahko pa uporabite možnost **Združi po** za vrtenje v drugih dveh razsežnostih: **Kategorija** in **Vir**.

V pogledu mreže in časovno razporejenem pogledu lahko izberete polja za prikaz. Vsote za vsak časovni okvir so prikazane na dnu projekta. Prikazujejo skupni ocenjeni obseg dela, stroške in prodajo za dan, teden, mesec ali leto. Privzeta lastna cena in prodajna cena imata datum začetka veljavnosti. To pomeni, da se spremenita za vsak vir glede na časovno razporejen pogled, ki ga izberete.

## <a name="expense-estimates"></a>Ocena stroškov

Gumb **Dodaj novo oceno stroškov** v pogledu mreže omogoča beleženje vseh stroškov, ki nastanejo v projektu, vendar niso neposredno povezani z delom. Ocene stroškov lahko zabeležite za določeno opravilo ali za celoten projekt. Izberite kategorije stroškov in predvideni datum, ko pričakujete, da bodo nastali stroški. Če imata povezani cenik z lastnimi cenami in prodajni cenik privzete cene (ali če so odstotki pribitka določeni za kategorije stroškov), so te samodejno vnesene v vrstico ocene, ko pride do povezave.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
