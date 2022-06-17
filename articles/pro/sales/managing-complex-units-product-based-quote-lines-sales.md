---
title: Upravljanje kompleksnih enot, na primer za uporabnika in za vsak mesec posebej, za podrobnosti ponudb, ki temeljijo na izdelkih – poenostavljeno
description: Ta članek vsebuje informacije o upravljanju kompleksnih enot za ponudbe na podlagi izdelkov.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88173468cd2e898331c4aa0a398792d9a0f3df10
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929924"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Upravljanje kompleksnih enot, na primer za uporabnika in za vsak mesec posebej, za podrobnosti ponudb, ki temeljijo na izdelkih – poenostavljeno

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Aplikacija Dynamics 365 Project Operations uporablja količnike za količino, ki podpirajo prodajo naročniških izdelkov. Pri naročniških izdelkih je količina v vrstici ponudbe ali projektne pogodbe izražena kot število mesecev uporabe.

Običajno je cena naročniške programske opreme shranjena v katalogu kot cena na uporabnika na mesec. Med prodajnim postopkom je cena v vrstici ponudbe običajno cena na uporabnika na mesec, ki jo je izpogajal in znižal prodajni agent za IT. Vsak posel ima različno število uporabnikov in različno število naročniških mesecev. Količina, ki se uporablja za izračun vrstice ponudbe, je produkt števila uporabnikov in števila mesecev naročnine.

Za podporo tej vrsti prodaje je Project Operations uvedla koncept količnikov za količino. Količniki za količino temeljijo na atributih izdelka v aplikaciji Dynamics 365. Ko konfigurirate določene lastnosti za izdelek, vam Project Operations omogoči označevanje podmnožice ali vseh lastnosti kot količnikov za količino.

Project Operations preveri, da so kot količniki za količino označene samo številske lastnosti ali lastnosti izdelka s številskim podatkovnim tipom. Ko v vrstico ponudbe dodate izdelek s količniki za količino, postane polje **Količina** na voljo samo za branje. Ko vnesete vrednosti za lastnosti izdelka, ki so količniki za količino, Project Operations izračuna količino vrstice ponudbe.

Dynamics 365 Sales ima lahko na primer te lastnosti:

- **Št. uporabnikov**: število uporabnikov.
- **Št. mesecev**: število mesecev naročnine.
- **Inventarna številka izdelka**

Lastnosti **Št. uporabnikov** in **Št. mesecev** lahko označite kot količnike za količino tako, da uredite lastnosti vrstice izdelkov.

Če želite iz lastnosti izdelka ustvariti količnike za količino, upoštevate te korake:

1. V levem podoknu za krmarjenje Project Operations odprite **Prodaja** > **Izdelki**.
2. Odprite izdelek, za katerega morate konfigurirati količnike za količino. Prepričajte se, da ima izdelek že konfigurirane lastnosti.
3. Na strani **Podatki o projektu** za izdelek izberite zavihek **Količniki za količino**.
4. V podmreži izberite **+ Nov izračun polja**.
5. Vnesite ime količnika za količino in izberite vrednost lastnosti, ki se preslika v izračun polja.
6. Shranite in zaprite obrazec. Ponovite te korake za vse lastnosti, ki jih želite uporabiti za izračun količine pri podrobnosti ponudbe, ki temelji na izdelku.

Ko za izdelek ustvarite podrobnost ponudbe, ki temelji na izdelku, se podrobnost ponudbe zaklene. Količina bo izračunana kot produkt vrednosti lastnosti, ki ste jih vnesli za to podrobnost ponudbe.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]