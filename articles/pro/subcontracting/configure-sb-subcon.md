---
title: Konfigurirajte ploščo za načrtovanje, da prikaže pogodbene delavce in podizvajalske zmogljivosti
description: Ta članek opisuje, kako konfigurirati tablo razporedov v Microsoftu Dynamics 365 Project Operations za prikaz zmogljivosti virov podizvajalcev, ko kadrovanje zahteva vire projekta.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262237"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurirajte ploščo za načrtovanje, da prikaže pogodbene delavce in podizvajalske zmogljivosti 

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Tabla urnikov v Microsoftu Dynamics 365 Project Operations se lahko uporablja za iskanje virov na dva načina:

- Splošno iskanje virov brez konteksta kakršnih koli specifičnih projektnih zahtev glede virov.
- Iskanje virov, specifičnih za zahteve, kjer bo projektna zahteva zagotovila kontekst za predlagane vire.

Če želite tablo razporedov obvestiti o zmogljivosti podizvajalskih virov in pogodbenih delavcih, morate posodobiti nastavitve plošče razporedov. Te posodobitve vključujejo: 
- Posodobite nastavitve plošče razporedov za splošno iskanje virov.
- Posodobite nastavitve plošče razporedov za iskanje virov na podlagi zahtev.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Posodobite nastavitve plošče razporedov za splošno iskanje virov
### <a name="update-filters-for-general-resource-search"></a>Posodobite filtre za splošno iskanje virov
Ko iščete vir, je treba posodobiti filtre, ki so na voljo na plošči razporeda, tako da lahko iščete tudi zunanje vire, tako da podate katero koli ali vse od naslednjega:
  - Vrsta delavca, ali naj bodo prikazani viri pogodbeni delavci ali zaposleni.
  - Prodajalno podjetje, ki bi mu moral pripadati vir.
  - Viri, ki pripadajo določenemu podizvajalcu ali podizvajalski liniji.
    
### <a name="update-retrieve-resource-query"></a>Posodobi poizvedbo za pridobitev vira
Poizvedbo, ki se uporablja za iskanje, je prav tako treba posodobiti za uporabo teh dodatnih atributov filtra. Uporabite naslednje korake za posodobitev konfiguracije Schedule Board za splošno iskanje virov:  
1. Odprto **Nastavitve plošče razporeda** za določeno tablo urnikov.
2. Odprite **Splošne nastavitve** in se pomaknite do **Druge nastavitve**.
3. Na seznamu nastavitev v tem razdelku posodobite **Postavitev filtra** do **Privzeta postavitev filtra za Project Operations Lite**.
4. Nadgradnja **Poizvedba za pridobivanje virov** do **Privzeta poizvedba za pridobivanje virov za Project Operations Lite**.

![Posodobite nastavitve plošče razporedov za splošno iskanje virov](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Posodobite nastavitve plošče razporedov za iskanje virov na podlagi zahtev
### <a name="update-filters-for-requirement-specific-resource-search"></a>Posodobite filtre za iskanje virov glede na zahteve 
Ko iščete vir, je treba posodobiti filtre, ki so na voljo na plošči razporeda, tako da lahko iščete tudi zunanje vire, tako da podate katero koli ali vse od naslednjega:
 - Vrsta delavca, ali naj bodo prikazani viri pogodbeni delavci ali zaposleni.
 - Prodajalno podjetje, ki bi mu moral pripadati vir.
 - Viri, ki pripadajo določenemu podizvajalcu ali podizvajalski liniji.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Posodobite poizvedbo za pridobitev vira za iskanje po sredstvih glede na zahteve 
Poizvedbo, ki se uporablja za iskanje, je prav tako treba posodobiti za uporabo teh dodatnih atributov filtra. Uporabite naslednje korake za posodobitev konfiguracije Schedule Board za iskanje virov na podlagi zahtev:

1. Odprto **Nastavitve plošče razporeda** za določeno tablo razporedov in nato izberite **Odprite Privzete nastavitve** da odprete nastavitve za iskanje glede na zahteve.
2. Odprite **Splošne nastavitve** in se pomaknite do **Druge nastavitve**.
3. Na seznamu nastavitev v tem razdelku posodobite **Postavitev filtra** do **Privzeta postavitev filtra za Project Operations Lite**.
4. Nadgradnja **Poizvedba za pridobivanje virov** do **Privzeta poizvedba za pridobivanje virov za Project Operations Lite**.
5. Odprite **Vrste urnikov** zavihek in pojdite na **Projekt**.
6. Pod nastavitvami za **Projekt**, nadgradnja **Pomočnik za razporejanje Poizvedba za pridobivanje virov** do **Privzeta poizvedba za pridobivanje virov za Project Operations Lite** in posodobite **Pomočnik za razporejanje poizvedbe o omejitvah** do **Privzeta poizvedba za omejitve pridobivanja za Project Operations Lite**.

![Posodobite nastavitve plošče razporedov za iskanje virov na podlagi zahtev](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
