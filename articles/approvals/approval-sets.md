---
title: Nabori odobritev
description: V tem članku je pojasnjeno, kako upravljati z nabori odobritev in zahtevami ter s podmnožicami teh postopkov.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524937"
---
# <a name="approval-sets"></a>Nabori odobritev

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Nabori odobritev združujejo zahtev za odobritev v manjše podskupine postopkov. To združevanje omogoča, da projekt v določenem vrstnem redu obdela odobritve, poleg tega pa omogoča tudi ponovne poizkuse in oblikovanje zaporedja. Z združevanjem zahtev za odobritev se povečata zanesljivost in sledljivost obdelave velikega števila odobritev.

Nabori odobritev kažejo splošno stanje obdelave njihovih povezanih zapisov. Ko odobritveni zapis obdelamo z uporabo nabora odobritev, se stanje zapisa **Poslano** spremeni v **Odobreno**, in zapis ni več povezan z naborom odobritev. Če zapis ne uspe, ko je predložen v odobritev, ostane v stanju **Oddano**, nabor odobritev pa je označen kot neuspešen. Nabor odobritev zabeleži sporočilo o napaki.

## <a name="processing-approvals-and-approval-sets"></a>Obdelava odobritev in naborov odobritev
Odobritve, ki so v čakalni vrsti za obdelavo, so vidne v pogledu **Obdelava odobritev**. Sistem večkrat asinhrono obdela vse vnose; če so bili predhodni poskusi neuspešni, pa prav tako ponovno poskusi z odobritvijo.

Polke **Življenjska doba nabora odobritev** beleži število poskusov obdelave niza, preden je označen kot neuspešen.

Nabori odobritev se obdelujejo s periodično aktivacijo na podlagi **toka za oblak**, ki je poimenovan **Project Service – ponavljajoče se načrtovanje naborov odobritev projekta**. To najdemo v možnosti **Rešitev**, ki je poimenovana **Project Operations**. 

Prepričajte se, da je tok aktiviran tako, da dokončate naslednje korake.

1. Kot skrbnik se prijavite v [flow.microsoft.com](https://powerautomate.microsoft.com).
2. V zgornjem desnem kotu preklopite na okolje, ki ga uporabljate za Dynamics 365 Project Operations.
3. Izberite možnost **Rešitve** za seznam rešitev, ki so nameščene v okolju.
4. Na seznamu rešitev izberite **Project Operations**.
5. Spremenite filter z **Vse** na **Tokovi za oblak**.
6. Preverite, ali je tok **Project Service – ponavljajoče se načrtovanje naborov odobritev projekta** nastavljen na **Vklopljeno**. Če ni, izberite tok in nato možnost **Vklopi**.
7. Preverite, ali se obdelava izvaja vsakih pet minut tako, da pregledate seznam **Sistemski posli** v območju **Nastavitve** znotraj vašega okolja Project Operations Dataverse.

## <a name="failed-approvals-and-approval-sets"></a>Neuspešne odobritve in nabori odobritev
Pogled **Neuspešne odobritve** ponuja seznam vseh odobritev, za katere mora posredovati uporabnik. Odprite povezane dnevnike nabora odobritev, da ugotovite vzrok napake.
Z izbiro možnosti **Poskusi znova** se doda številu življenjske dobe nabora odobritev, premakne nabor odobritev nazaj v stanje **Obdelava** in poskuša obdelati preostale zapise.

## <a name="configure-approval-sets"></a>Konfiguracija naborov odobritev

### <a name="enable-the-approval-sets-feature"></a>Omogočite funkcijo Nabori odobritev
Preden omogočite funkcijo Nabori odobritev, preverite, ali se trenutno ne obdeluje nobena odobritev. Ko je ta funkcija omogočena, je ni več mogoče onemogočiti.

- Pojdite na stran **Projektni parametri** in izberite možnost **Nadzor funkcij** > **Omogoči sodobne odobritve**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfiguriranje asinhronega praga 
Ko se nabori odobritev ustvarijo, se obdelava premakne v ozadje, ko izbrano število zapisov za odobritev preseže navedeni prag. Uporabite polje **Asinhroni prag** za konfiguracijo, kdaj naj se obdelava odobritve izvaja sinhrono ali asinhrono. Izberite eno od naslednjih vrednosti:

  - Nič: vse zahteve naj se obdelajo asinhrono. 
  - Številke, večje od nič: odobritve se obdelujejo asinhrono le, če predloženo število odobritev preseže to vrednost.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
