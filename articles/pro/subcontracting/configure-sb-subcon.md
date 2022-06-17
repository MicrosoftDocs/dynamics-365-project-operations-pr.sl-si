---
title: Konfigurirajte ploščo za načrtovanje, da prikaže pogodbene delavce in podizvajalske zmogljivosti
description: V tem članku je opisano, kako konfigurirati ploščo urnika v Microsoftu Dynamics 365 Project Operations za prikaz zmogljivosti virov podizvajalcev pri kadrovskih zahtevah po virih projekta.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b965fd5011a575354f50c47081be198ab43248f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919850"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurirajte ploščo za načrtovanje, da prikaže pogodbene delavce in podizvajalske zmogljivosti 

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Razporedna tabla v Microsoftu Dynamics 365 Project Operations se lahko uporablja za iskanje virov na dva načina:

- Splošno iskanje virov brez konteksta kakršnih koli posebnih zahtev po virih, ki temeljijo na projektu.
- Iskanje virov glede na zahteve, kjer bo zahteva projekta zagotovila kontekst za predlagane vire.

Če želite obvestiti razporedno tablo o zmogljivosti podizvajalcev in pogodbenih delavcih, morate posodobiti nastavitve odbora za razpored. Te posodobitve vključujejo: 
- Posodobite nastavitve plošče urnika za splošno iskanje virov.
- Posodobite nastavitve plošče urnika za iskanje virov na podlagi zahtev.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Posodobite nastavitve plošče urnika za splošno iskanje virov
### <a name="update-filters-for-general-resource-search"></a>Posodobite filtre za splošno iskanje virov
Ko iščete vir, je treba filtre, ki so na voljo na plošči urnika, posodobiti, tako da lahko iščete tudi zunanje vire, tako da navedete nekaj ali vse od naslednjega:
  - Vrsta delavca, ali naj bodo prikazani viri pogodbeni delavci ali zaposleni.
  - Podjetje prodajalca, ki mu mora pripadati vir.
  - Viri, ki pripadajo določeni podizvajalski pogodbi ali vrsti podizvajalcev.
    
### <a name="update-retrieve-resource-query"></a>Posodobite poizvedbo za pridobivanje virov
Poizvedbo, uporabljeno za iskanje, je treba posodobiti tudi za uporabo teh dodatnih atributov filtra. Uporabite naslednje korake za posodobitev konfiguracije Schedule Board za splošno iskanje virov:  
1. Odprto **Razporedite nastavitve plošče** za določen razpored.
2. Odprite **Splošne nastavitve** zavihek in se pomaknite na **Druge nastavitve**.
3. Na seznamu nastavitev v tem razdelku posodobite **Postavitev filtra** do **Privzeta postavitev filtra za Project Operations Lite**.
4. Nadgradnja **Pridobi poizvedbo o virih** do **Privzeta poizvedba za pridobivanje virov za Project Operations Lite**.

![Posodobite nastavitve plošče urnika za splošno iskanje virov](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Posodobite nastavitve plošče urnika za iskanje virov na podlagi zahtev
### <a name="update-filters-for-requirement-specific-resource-search"></a>Posodobite filtre za iskanje virov glede na zahteve 
Ko iščete vir, je treba filtre, ki so na voljo na plošči urnika, posodobiti, tako da lahko iščete tudi zunanje vire, tako da navedete nekaj ali vse od naslednjega:
 - Vrsta delavca, ali naj bodo prikazani viri pogodbeni delavci ali zaposleni.
 - Podjetje prodajalca, ki mu mora pripadati vir.
 - Viri, ki pripadajo določeni podizvajalski pogodbi ali vrsti podizvajalcev.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Posodobite poizvedbo za pridobivanje virov za iskanje po viru, ki je odvisno od zahtev 
Poizvedbo, uporabljeno za iskanje, je treba posodobiti tudi za uporabo teh dodatnih atributov filtra. Za posodobitev konfiguracije plošče razporeda za iskanje virov na podlagi zahtev uporabite naslednje korake:

1. Odprto **Razporedite nastavitve plošče** za določeno tablo razporeda in nato izberite **Odprite Privzete nastavitve** da odprete nastavitve za iskanje po zahtevah.
2. Odprite **Splošne nastavitve** zavihek in se pomaknite na **Druge nastavitve**.
3. Na seznamu nastavitev v tem razdelku posodobite **Postavitev filtra** do **Privzeta postavitev filtra za Project Operations Lite**.
4. Nadgradnja **Pridobi poizvedbo o virih** do **Privzeta poizvedba za pridobivanje virov za Project Operations Lite**.
5. Odprite **Vrste urnika** zavihek in pojdite na **Projekt**.
6. Pod nastavitvami za **Projekt**, nadgradnja **Načrtujte poizvedbo za pridobivanje virov pomočnika za načrtovanje** do **Privzeta poizvedba za pridobivanje virov za Project Operations Lite** in posodobite **Poizvedbo za pridobivanje omejitev pomočnika za načrtovanje** do **Privzeta poizvedba o omejitvah pridobivanja za Project Operations Lite**.

![Posodobite nastavitve plošče urnika za iskanje virov na podlagi zahtev](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
