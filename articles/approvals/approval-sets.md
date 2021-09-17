---
title: Nabori odobritev
description: V tej temi je pojasnjeno, kako upravljati z nabori odobritev in zahtevami ter s podmnožicami teh postopkov.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323256"
---
# <a name="approval-sets"></a>Nabori odobritev

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Nabori odobritev združujejo zahtev za odobritev v manjše podskupine postopkov. To združevanje omogoča, da projekt v določenem vrstnem redu obdela odobritve, poleg tega pa omogoča tudi ponovne poizkuse in oblikovanje zaporedja. Z združevanjem zahtev za odobritev se povečata zanesljivost in sledljivost obdelave velikega števila odobritev.

Nabori odobritev kažejo splošno stanje obdelave njihovih povezanih zapisov. Ko odobritveni zapis obdelamo z uporabo nabora odobritev, se stanje zapisa **Poslano** spremeni v **Odobreno**, in zapis ni več povezan z naborom odobritev. Če zapis ne uspe, ko je predložen v odobritev, ostane v stanju **Oddano**, nabor odobritev pa je označen kot neuspešen. Nabor odobritev zabeleži sporočilo o napaki.

## <a name="processing-approvals-and-approval-sets"></a>Obdelava odobritev in naborov odobritev
Odobritve, ki so v čakalni vrsti za obdelavo, so vidne v pogledu **Obdelava odobritev**. Sistem večkrat asinhrono obdela vse vnose; če so bili predhodni poskusi neuspešni, pa prav tako ponovno poskusi z odobritvijo.

Polke **Življenjska doba nabora odobritev** beleži število poskusov obdelave niza, preden je označen kot neuspešen.

## <a name="failed-approvals-and-approval-sets"></a>Neuspešne odobritve in nabori odobritev
Pogled **Neuspešne odobritve** ponuja seznam vseh odobritev, za katere mora posredovati uporabnik. Odprite povezane dnevnike nabora odobritev, da ugotovite vzrok napake.
Z izbiro možnosti **Poskusi znova** se doda številu življenjske dobe nabora odobritev, premakne nabor odobritev nazaj v stanje **Obdelava** in poskuša obdelati preostale zapise.

## <a name="configure-approval-sets"></a>Konfiguracija naborov odobritev

### <a name="enable-the-approval-sets-feature"></a>Omogočite funkcijo Nabori odobritev
Preden omogočite funkcijo Nabori odobritev, preverite, ali se trenutno ne obdeluje nobena odobritev.

- Pojdite na stran **Projektni parametri** in izberite možnost **Nadzor funkcij** > **Omogoči sodobne odobritve**.

### <a name="turn-off-the-approval-sets-feature"></a>Izklop funkcije Nabori odobritev
Preden izklopite funkcijo Nabori odobritev, preverite, ali se trenutno ne obdeluje nobena odobritev.

- Pojdite na stran **Projektni parametri** in izberite možnost **Nadzor funkcij** > **Onemogoči sodobne odobritve**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfiguriranje asinhronega praga 
Ko se nabori odobritev ustvarijo, se obdelava premakne v ozadje, ko izbrano število zapisov za odobritev preseže navedeni prag. Uporabite polje **Asinhroni prag** za konfiguracijo, kdaj naj se obdelava odobritve izvaja sinhrono ali asinhrono. Izberite eno od naslednjih vrednosti:

  - Nič: vse zahteve naj se obdelajo asinhrono. 
  - Številke, večje od nič: odobritve se obdelujejo asinhrono le, če predloženo število odobritev preseže to vrednost.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
