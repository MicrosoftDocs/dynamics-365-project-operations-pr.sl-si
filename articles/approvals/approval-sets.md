---
title: Nabori odobritev
description: V tej temi je pojasnjeno, kako upravljati z nabori odobritev in zahtevami ter s podmnožicami teh postopkov.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6809e01d8c3c93841125d0100d898dc208577019
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576244"
---
# <a name="approval-sets"></a>Nabori odobritev

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Nabori odobritev združujejo zahtev za odobritev v manjše podskupine postopkov. To združevanje omogoča, da projekt v določenem vrstnem redu obdela odobritve, poleg tega pa omogoča tudi ponovne poizkuse in oblikovanje zaporedja. Z združevanjem zahtev za odobritev se povečata zanesljivost in sledljivost obdelave velikega števila odobritev.

Nabori odobritev kažejo splošno stanje obdelave njihovih povezanih zapisov. Ko odobritveni zapis obdelamo z uporabo nabora odobritev, se stanje zapisa **Poslano** spremeni v **Odobreno**, in zapis ni več povezan z naborom odobritev. Če zapis ne uspe, ko je predložen v odobritev, ostane v stanju **Oddano**, nabor odobritev pa je označen kot neuspešen. Nabor odobritev zabeleži sporočilo o napaki.

## <a name="processing-approvals-and-approval-sets"></a>Obdelava odobritev in naborov odobritev
Odobritve, ki so v čakalni vrsti za obdelavo, so vidne v pogledu **Obdelava odobritev**. Sistem večkrat asinhrono obdela vse vnose; če so bili predhodni poskusi neuspešni, pa prav tako ponovno poskusi z odobritvijo.

Polke **Življenjska doba nabora odobritev** beleži število poskusov obdelave niza, preden je označen kot neuspešen.

Nabori odobritev se obdelujejo s periodično aktivacijo na podlagi a **Oblačni tok** imenovani **Projektna storitev – Redno načrtujte komplete za odobritev projekta**. To se nahaja v **Rešitev** imenovani **Projektne operacije**. 

Prepričajte se, da je pretok aktiviran, tako da dokončate naslednje korake.

1. Kot skrbnik se prijavite v [flow.microsoft.com](https://powerautomate.microsoft.com).
2. V zgornjem desnem kotu preklopite na okolje, za katerega uporabljate Dynamics 365 Project Operations.
3. Izberite **Rešitve** navesti rešitve, ki so nameščene v okolju.
4. Na seznamu rešitev izberite **Projektne operacije**.
5. Zamenjajte filter iz **vse** do **Oblačni tokovi**.
6. Preverite, da je **Projektna storitev – Redno načrtujte komplete za odobritev projekta** pretok je nastavljen na **Vklopljeno**. Če ni, izberite tok in nato izberite **Vklopiti**.
7. Preverite, ali se obdelava izvaja vsakih pet minut, tako da pregledate **Sistemska delovna mesta** seznam v **Nastavitve** območje znotraj vašega projektnega delovanja Dataverse okolje.

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
