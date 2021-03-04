---
title: Upravljanje kompleksnih enot za podrobnosti pogodbe, ki temeljijo na izdelkih – poenostavljena različica
description: V tej temi so na voljo informacije o podpori prodaje naročniških izdelkov.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177396"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Upravljanje kompleksnih enot za podrobnosti pogodbe, ki temeljijo na izdelkih – poenostavljena različica

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Dynamics 365 Project Operations uporablja količnike za količino, ki podpirajo prodajo naročniških izdelkov. Pri naročniških izdelkih je količina v pogodbi ali podrobnostih pogodbe projekta izražena kot število mesecev uporabe.

Cena naročniške programske opreme je shranjena v katalogu kot cena na uporabnika na mesec. Med prodajnim postopkom je cena v podrobnostih pogodbe običajno cena na uporabnika na mesec, ki jo je izpogajal in znižal prodajni agent. Vsak posel ima različno število uporabnikov in različno število naročniških mesecev. Količina, ki se uporablja za izračun zneska podrobnosti pogodbe, je produkt števila uporabnikov in števila mesecev naročnine.

Za podporo te vrste prodaje rešitev Project Operations podpira koncept *količniki za količino*. Količniki za količino temeljijo na atributih izdelka. Ko konfigurirate določene lastnosti za izdelek, lahko označite podmnožico teh lastnosti ali vseh lastnosti kot količnike za količino.

Project Operations preveri, da so kot količniki za količino označene samo številske lastnosti ali lastnosti izdelka s številskim podatkovnim tipom. Ko je izdelek s konfiguriranimi količniki za količino dodan v podrobnosti pogodbe, polje **Količina** postane samo za branje. Ko vnesete vrednosti za lastnosti izdelka, ki so količniki za količino, Project Operations izračuna količino podrobnosti pogodbe.

Dynamics 365 Sales ima lahko na primer te lastnosti:

- **Št. uporabnikov**: število uporabnikov.
- **Št. mesecev**: število mesecev naročnine.
- **Inventarna številka izdelka**: inventarna številka (SKU) za izdelek

Lastnosti **Št. uporabnikov** in **Št. mesecev** lahko označite kot količnike za količino tako, da uredite lastnosti vrstice izdelkov.

Za ustvarjanje količnikov za količino za lastnosti izdelkov, izvedite naslednje korake.

1. V možnosti **Project Operations** izberite **Sales-Products**.
2. Odprite izdelek, za katerega morate nastaviti količnike za količino. Prepričajte se, da ima izdelek že nastavljene lastnosti.
3. Na strani **Podatki o projektu** izberite zavihek **Količniki za količino**.
4. V podmreži izberite **+ Nov izračun polja**.
5. Vnesite ime za **Količnik za količino** in izberite vrednost lastnosti, ki se preslika v izračun polja.
6. Shranite in zaprite obrazec.
7. Ponovite korake 2–6 za vse lastnosti, ki skupaj predstavljajo količino za podrobnosti pogodbe, ki temeljijo na izdelkih.

Z nastavljenimi količniki za količino, ko uporabnik ustvari podrobnosti pogodbe za ta izdelek, je količina podrobnosti pogodbe zaklenjena. Količina je nato izračunana kot izdelke vrednosti lastnosti za te podrobnosti pogodbe.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]