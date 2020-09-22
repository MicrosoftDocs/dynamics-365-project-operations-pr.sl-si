---
title: Kako prilagodim potek poslovnega procesa stopenj projekta?
description: Pregled prilagajanja poteka poslovnega procesa stopenj projekta.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755751"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Kako prilagodim potek poslovnega procesa stopenj projekta?
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

V starejših različicah aplikacije Project Service obstaja znana omejitev, da se morajo imena stopenj v poteku poslovnega procesa stopenj projekta natančno ujemati s pričakovanimi angleškimi imeni (**Quote**, **Plan**, **Close**). Sicer poslovna logika, ki temelji na angleških imenih stopenj, ne deluje po pričakovanjih. Zato v obrazcu projekta niso na voljo znana dejanja, kot je **Preklopi proces** ali **Uredi proces**, prav tako pa se ne spodbuja prilagajanje poteka poslovnega procesa. 

Ta omejitev je bila obravnavana v različici 2.4.5.48 in novejših različicah. Ta članek ponuja predlagane rešitve, če morate prilagoditi privzeti potek poslovnega procesa za starejše različice.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Poslovna logika zahteva natančno ujemanje z angleškimi imeni stopenj

Potek poslovnega procesa stopenj projekta vključuje poslovno logiko, ki spodbuja naslednje načine delovanja v aplikaciji:
- Ko je projekt povezan s ponudbo, koda nastavi potek poslovnega procesa na stopnjo **Quote**.
- Ko je projekt povezan s pogodbo, koda nastavi potek poslovnega procesa na stopnjo **Plan**.
- Ko se potek poslovnega procesa pomakne na stopnjo **Close**, je zapis projekta deaktiviran. Ko je projekt deaktiviran, sta obrazec projekta in strukturirana členitev dela (SČD) nastavljena samo za branje, rezervacije poimenovanih virov so izdane in vsi povezani ceniki so deaktivirani.

Ta poslovna logika temelji na angleških imenih za stopnje projekta. Ta odvisnost od angleških imen stopenj je glavni razlog, zakaj se ne spodbuja prilagajanje poteka poslovnega procesa stopenj projekta in zakaj v entiteti projekta ne vidite skupnih dejanj poteka poslovnega procesa, kot je **Preklopi proces** ali **Uredi proces**.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Kaj se zgodi, če se imena stopenj ne ujemajo z angleškimi imeni?

V aplikaciji Project Service, različica 1.x na platformi 8.2, poslovna logika, ki nastavi pravo stopnjo za ponudbe ali pogodbe oziroma zapre projekt, preskoči, če se imena stopenj v poteku poslovnega procesa ne ujemajo natančno z angleškimi imeni stopenj. Sporočila o napakah niso prikazana. Zato se zdi, da lahko prilagodite potek poslovnega procesa stopenj projekta. Vendar ne boste videli nobenega samodejnega procesa, ki deluje za ponudbe, pogodbe in zapiranje projekta.

V aplikaciji Project Service, različica 2.4.4.30 ali starejša različica na platformi 9.0, je prišlo do pomembne arhitekturne spremembe potekov poslovnih procesov, zaradi česar je bilo treba ponovno napisati poslovno logiko poteka poslovnega procesa. Če se imena stopenj procesa ne ujemajo s pričakovanimi angleškimi imeni, posledično prejmete sporočilo o napaki. 

Če torej želite prilagoditi potek poslovnega procesa stopenj projekta za entiteto projekta, lahko privzetemu poteku poslovnega procesa za entiteto projekta dodate le povsem nove stopnje, pri tem pa ohranite stopnje **Quote**, **Plan** in **Close** v takšni obliki, kot so. Ta omejitev zagotavlja, da ne prejemate napak iz poslovne logike, ki pričakuje angleška imena stopenj v poteku poslovnega procesa.

V različici 2.4.5.48 ali novejših različicah je bila poslovna logika, ki je opisana v tem članku, odstranjena iz privzetega poteka poslovnega procesa za entiteto projekta. Če aplikacijo nadgradite na to različico ali novejšo različico, boste lahko prilagodili privzeti potek poslovnega procesa ali ga zamenjali s svojim. 

## <a name="workarounds-for-earlier-versions"></a>Rešitve za starejše različice

Če nadgradnja ne pride v poštev, lahko prilagodite potek poslovnega procesa stopenj projekta za entiteto projekta na enega od teh dveh načinov:

1. Privzeti konfiguraciji dodajte dodatne stopnje, pri tem pa ohranite angleška imena stopenj za **Quote**, **Plan** in **Close**.

   > [!div class="mx-imgBorder"] 
   > ![Posnetek zaslona dodajanja stopenj privzeti konfiguraciji](media/FAQ-Customize-BPF-1.png)
 
2. Ustvarite svoj potek poslovnega procesa in ga spremenite v primarni potek poslovnega procesa za entiteto projekta, ki omogoča poimenovanje stopenj s poljubnimi imeni. Če želite uporabiti iste standardne stopnje projekta **Quote**, **Plan** in **Close**, pa morate izvesti nekatere prilagoditve, ki omogočajo uporabo imen stopenj po meri. Bolj zapletena logika obstaja pri zapiranju projekta, ki ga lahko še vedno sprožite z deaktiviranjem zapisa projekta.

   > [!div class="mx-imgBorder"] 
   > ![Posnetek zaslona prilagajanja BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Dodatni vidiki za aplikacijo Project Service, različica 2.4.4.30 ali starejša različica na platformi 9.0

V aplikaciji Project Service, različica 2.4.4.30 ali starejša različica na platformi 9.0, se polje **Ime stopnje** s potekom poslovnega procesa po meri v entiteti projekta, ki se uporablja v grafikonu **Projekt po stopnjah** in pogledih seznamov projektov, ne bo posodobilo, saj je povezano s privzetim potekom poslovnega procesa stopenj projekta. To težavo lahko odpravite na naslednji način:

- Dodajte polje po meri, da zajamete trenutno stopnjo poteka poslovnega procesa, ki se posodobi, ko se uporabnik pomika po poteku poslovnega procesa po meri.

- Spremenite grafikon **Projekt po stopnjah**, da boste lahko uporabljali polje po meri, namesto privzete konfiguracije.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Koraki za ustvarjanje lastnega poteka poslovnega procesa za entiteto projekta

Če želite ustvariti lastni potek poslovnega procesa za entiteto projekta, naredite naslednje:

1. Odprite **Nastavitve** > **Središče procesov**. Ne kopirajte poteka poslovnega procesa stopenj projekta, saj boste s tem kopirali tudi poslovno logiko za Project Service.

   > [!div class="mx-imgBorder"] 
   > ![Posnetek zaslona prilagajanja BPF](media/FAQ-Customize-BPF-3.png)

2. Z oblikovalnikom procesov ustvarite poljubna imena stopenj. Če želite enake funkcije, kot so funkcije privzetih stopenj za **Quote**, **Plan** in **Close**, jih boste morali ustvariti na podlagi vaših imen stopenj poteka poslovnega procesa po meri.

   > [!div class="mx-imgBorder"] 
   > ![Posnetek zaslona oblikovalnika procesov za prilagajanje BPF](media/FAQ-Customize-BPF-4.png) 

3. V oblikovalniku procesov kliknite **Potek procesa naročila**, da potek poslovnega procesa po meri spremenite v primarni potek poslovnega procesa za entiteto projekta tako, da ga premaknete na vrh seznama nad potek poslovnega procesa stopenj projekta.

   > [!div class="mx-imgBorder"] 
   > ![Posnetek zaslona uporabe poteka procesa naročila](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Naslednji koraki veljajo za aplikacijo Project Service, različica 2.4.4.30 ali starejša različica na platformi 9.0

4. Entiteti projekta dodajte novo polje po meri, da v svojem poteku poslovnega procesa po meri zajamete stopnje po meri. Za posodobitev tega polja boste morali dodati poslovno logiko (vtičnik/potek dela), če je stopnja poteka poslovnega procesa po meri posodobljena.

   > [!div class="mx-imgBorder"] 
   > ![Posnetek zaslona prilagajanja entitete projekta](media/FAQ-Customize-BPF-6-720.png)

5. Spremenite grafikon **Projekt po stopnjah**, da boste lahko za stopnje uporabili novo polje po meri.

   > [!div class="mx-imgBorder"] 
   > ![Posnetek zaslona uporabe grafikona »Projekt po stopnjah«](media/FAQ-Customize-BPF-7-720.png)

6. Spremenite vse poglede za entiteto projekta, da boste za stopnje lahko vključili novo polje po meri.

   > [!div class="mx-imgBorder"] 
   > ![Posnetek zaslona spreminjanja pogledov v entiteti projekta](media/FAQ-Customize-BPF-8-720.png)

