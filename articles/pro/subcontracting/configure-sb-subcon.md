---
title: Konfigurirajte ploščo za načrtovanje, da prikaže pogodbene delavce in podizvajalske zmogljivosti
description: Ta članek opisuje, kako konfigurirati ploščo razporeda v programu Microsoft Dynamics 365 Project Operations za prikaz zmogljivosti vira v podizvajanju pri kadrovskih zahtevah za projektne vire.
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

Plošča razporeda v programu Microsoft Dynamics 365 Project Operations se lahko uporablja za iskanje virov na dva načina:

- Splošno iskanje virov brez konteksta kakršnih koli specifičnih projektnih zahtev glede virov.
- Iskanje virov glede na zahteve, kjer bo zahteva za projekt zagotovila kontekst za predlagane vire.

Če želite ploščo razporeda obvestiti o zmogljivosti vira v podizvajanju in pogodbenih delavcih, morate posodobiti nastavitve plošče razporeda. Te posodobitve vključujejo: 
- Posodobitev nastavitev plošče razporeda za splošno iskanje virov.
- Posodobitev nastavitev plošče razporeda za iskanje virov glede na zahteve.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Posodobitev nastavitev plošče razporeda za splošno iskanje virov
### <a name="update-filters-for-general-resource-search"></a>Posodobitev filtrov za splošno iskanje virov
Ko iščete vir, bi morali biti filtri, ki so na voljo na plošči razporeda, posodobljeni, da lahko iščete tudi zunanje vire tako, da določite kar koli ali vse od naslednjega:
  - Vrsta delavca; ali naj bodo prikazani viri pogodbeni delavci ali zaposleni.
  - Podjetje dobavitelja, ki bi mu moral pripadati vir.
  - Viri, ki pripadajo določenemu podizvajalcu ali podrobnostim podizvajalske pogodbe.
    
### <a name="update-retrieve-resource-query"></a>Posodobitev poizvedbe za pridobivanje virov
Poizvedbo, uporabljeno za iskanje, je prav tako treba posodobiti za uporabo teh dodatnih atributov filtra. Uporabite naslednje korake za posodobitev konfiguracije plošče razporeda za splošno iskanje virov:  
1. Odprite **Nastavitve plošče razporeda** za določeno ploščo razporeda.
2. Odprite zavihek **Splošne nastavitve** in se pomaknite do možnosti **Druge nastavitve**.
3. Na seznamu nastavitev v tem razdelku posodobite **Postavitev filtra** na **Privzeta postavitev filtra za Project Operations Lite**.
4. Posodobite **Poizvedba za pridobivanje virov** na **Privzeta poizvedba za pridobivanje virov za Project Operations Lite**.

![Posodobitev nastavitev plošče razporeda za splošno iskanje virov](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Posodobitev nastavitev plošče razporeda za iskanje virov glede na zahteve
### <a name="update-filters-for-requirement-specific-resource-search"></a>Posodobitev filtrov za iskanje virov glede na zahteve 
Ko iščete vir, bi morali biti filtri, ki so na voljo na plošči razporeda, posodobljeni, da lahko iščete tudi zunanje vire tako, da določite kar koli ali vse od naslednjega:
 - Vrsta delavca; ali naj bodo prikazani viri pogodbeni delavci ali zaposleni.
 - Podjetje dobavitelja, ki bi mu moral pripadati vir.
 - Viri, ki pripadajo določenemu podizvajalcu ali podrobnostim podizvajalske pogodbe.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Posodobitev poizvedbe za pridobivanje virov za iskanje virov glede na zahteve 
Poizvedbo, uporabljeno za iskanje, je prav tako treba posodobiti za uporabo teh dodatnih atributov filtra. Uporabite naslednje korake za posodobitev konfiguracije plošče razporeda za iskanje virov glede na zahteve:

1. Odprite **Nastavitve plošče razporeda** za določeno ploščo razporeda in nato izberite **Odpri privzete nastavitve**, da odprete nastavitve za iskanje glede na zahteve.
2. Odprite zavihek **Splošne nastavitve** in se pomaknite do možnosti **Druge nastavitve**.
3. Na seznamu nastavitev v tem razdelku posodobite **Postavitev filtra** na **Privzeta postavitev filtra za Project Operations Lite**.
4. Posodobite **Poizvedba za pridobivanje virov** na **Privzeta poizvedba za pridobivanje virov za Project Operations Lite**.
5. Odprite zavihek **Vrste razporedov** in nato **Projekt**.
6. Pod nastavitvami za **Projekt**, posodobite **Poizvedba za pridobivanje virov pomočnika za razporejanje** na **Privzeta poizvedba za pridobivanje virov za Project Operations Lite** in posodobite **Poizvedba za pridobivanje z omejitvami pomočnika za razporejanje** na **Privzeta poizvedba o omejitvah pridobivanja za Project Operations Lite**.

![Posodobitev nastavitev plošče razporeda za iskanje virov glede na zahteve](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
