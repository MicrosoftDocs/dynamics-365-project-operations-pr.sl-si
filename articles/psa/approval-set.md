---
title: Nabori odobritev
description: Ta tema zagotavlja informacije o naboru odobritev, zahtevah in podmnožicah teh postopkov.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e57944b3031ff8b6da163125bb6668875ae77bd06f23a5b8c4ef06f396210e4f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995511"
---
# <a name="approval-sets"></a>Nabori odobritev

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nabori odobritev združujejo zahtev za odobritev v manjše podskupine postopkov. To združevanje omogoča obdelavo odobritev po vrstnem redu po projektu ter vnovični poskus in upoštevanje vrstnega reda. Združevanj izboljšuje zanesljivost in sledljivost obdelave odobritev za velike količine odobritev.

Nabori odobritev kažejo splošno stanje obdelave njihovih povezanih zapisov. Ko je zapis odobritve obdelan z naborom odobritve, se zapis premakne iz **Oddano** v **Odobreno** in je ločen od nabora odobritev. Če zapis ne uspe, ko je predložen v odobritev, ostane v stanju **Oddano**, nabor odobritev pa je označen kot neuspešen. Nabor odobritev zabeleži sporočilo o napaki.

## <a name="processing-approvals-and-approval-sets"></a>Obdelava odobritev in naborov odobritev
Odobritve, ki so v čakalni vrsti za obdelavo, so vidne v pogledu **Obdelava odobritev**. Sistem poskuša večkrat asinhrono obdelati vse vnose, vključno z vnovičnim poskusom odobritve, če prejšnji poskusi niso uspeli.

Polke **Življenjska doba nabora odobritev** beleži število poskusov obdelave niza, preden je označen kot neuspešen.

## <a name="failed-approvals-and-approval-sets"></a>Neuspešne odobritve in nabori odobritev
Pogled **Neuspešne odobritve** navaja vse odobritve, ki zahtevajo posredovanje uporabnika. Odprite povezane dnevnike nabora odobritev, da ugotovite vzrok napake.
Z izbiro možnosti **Poskusi znova** se doda številu življenjske dobe nabora odobritev, premakne nabor odobritev nazaj v stanje **Obdelava** in poskuša obdelati preostale zapise.

## <a name="configure-approval-sets"></a>Konfiguracija naborov odobritev

###  <a name="enable-the-approval-sets-feature"></a>Omogočite funkcijo Nabori odobritev
Preden omogočite funkcijo Nabori odobritev, preverite, ali se trenutno ne obdeluje nobena odobritev.

- Pojdite na stran **Projektni parametri** in izberite možnost **Nadzor funkcij** > **Omogoči sodobne odobritve**.

### <a name="turn-off-the-approval-sets-feature"></a>Izklop funkcije Nabori odobritev
Preden izklopite funkcijo Nabori odobritev, preverite, ali se trenutno ne obdeluje nobena odobritev.

- Pojdite na stran **Projektni parametri** in izberite možnost **Nadzor funkcij** > **Onemogoči sodobne odobritve**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfiguriranje asinhronega praga 
Ko se nabori odobritev ustvarijo, se obdelava premakne v ozadje, ko izbrano število zapisov za odobritev preseže navedeni prag. Uporabite polje **Asinhroni prag** za konfiguracijo, kdaj naj se obdelava odobritve izvaja sinhrono ali asinhrono.
Veljavne vrednosti so:

  - Nič: vse zahteve naj se obdelajo asinhrono. 
  - Številke, večje od nič: odobritve se obdelujejo asinhrono le, če predloženo število odobritev preseže to vrednost.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
