---
title: Nastavitev cenikov
description: Ta tema vsebuje informacije o nastavitvi cenikov za stroške in prodajo.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 000c22944b187b6250f2e982d73020028093fde6
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180212"
---
# <a name="set-up-price-lists"></a>Nastavitev cenikov

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Ceniki v storitvi Dynamics 365 Project Operations predstavljajo katalog cen. Zneski izražajo zneske stroške, prodaje in obračuna. Kontekst cenika je odvisen od tega, ali cenik izraža znesek stroška, prodaje ali obračuna, in je lahko ali **Prodaja** ali **Strošek**.

Naslednje razširitve so specifične za Project Operations in se uporabljajo za cenike iz storitve Dynamics 365 Sales.

- **Kontekst**: to polje ima podprte vrednosti **Strošek** in **Prodaja**. Vrednost **Nakup** ni podprta. Nastavite kontekst na **Strošek** za izdelavo cenika z lastnimi cenami ali nastavite kontekst na vrednost **Prodaja** za prodajni cenik. Ceniki z lastnimi cenami opredeljujejo ceno za vrsto stroškov pri zapisih ocenjenih ali dejanskih vrednosti. Prodajni ceniki opredeljujejo ceno pri zapisih ocenjenih ali dejanskih vrednosti za neobračunane in obračunane vrste prodaje.
- **Časovna enota**: to je privzeta časovna enota, za katero je cena nastavljena v povezani tabeli **Cena vloge** za ta cenik.
- **Entiteta cenika**: to skrito polje se v storitvi Project Operations uporablja za razlikovanje cenikov, ki veljajo za ponudbo ali pogodbo, od tistih, ki so standardni in globalno veljavni.

## <a name="price-list-header"></a>Glava cenika

Naslednja tabela vključuje polja na zavihku cenika **Splošno**, ki je edinstven za Project Operations ali ima bistvene spremembe v vedenju od cenikov v storitvi Sales.

| Polje | LOkacija | Opis | Nadaljnji vpliv |
| --- | --- | --- | --- |
| Imenu | Zavihek **Splošno** in obrazci za **hitro ustvarjanje** | Identiteta cenika. | Cenik je s to vrednostjo prikazan na vseh straneh s seznami in v spustnih seznamih.|
| Kontekst | Zavihek **Splošno** in obrazci za **hitro ustvarjanje** | To polje lahko nastavite na **Strošek** ali **Prodaja**. | Cenik, nastavljen na **Strošek**, se uporablja za iskanje cen za ocene stroškov in dejanske stroške. Cenik, nastavljen na **Prodaja**, se uporablja za iskanje cen za ocene prodaje in dejansko prodajo. Samo ceniki, katerih kontekst je nastavljen na **Prodaja**, je mogoče priložiti cenikom projektov za stranke, projektne ponudbe in projektne pogodbe. |
| Datum začetka | Zavihek **Splošno** in obrazci za **hitro ustvarjanje** | Datum začetka obdobja, za katerega velja cenik | S poljem **Končni datum** se določi, kateri cenik se uporablja za določeno vrstico za oceno ali dejansko vrednost. |
| Končni datum | Zavihek **Splošno** in obrazci za **hitro ustvarjanje** | Datum konca obdobja, za katerega velja cenik. | S poljem **Začetni datum** se določi, kateri cenik se uporablja za določeno vrstico za oceno ali dejansko vrednost. |
| Valuta | Zavihek **Splošno** in obrazci za **hitro ustvarjanje** | To polje se uporablja za privzeto nastavitev valute za vsako vrstico vloge, kategorije ali elementa cenika, povezane s tem cenikom. | Pri **prodajnih** ceniki ni mogoče ustvariti cenikov, vlog, kategorij ali elementov cenika v nobeni drugi valuti, razen v tej valuti. V cenikih za **stroške** lahko ustvarite vrstico za ceno vloge v kateri koli valuti. Tukaj določena valuta se uporablja kot privzeta. Uporabniške nastavitve, povezane s cenami vlog, lahko preglasijo to vrednost, da omogočijo nastavitev mere stroškov za delo v kateri koli valuti. Mere stroškov za kategorije in stroške elementov cenika lahko nastavite samo v tukaj določeni valuti. |
| Časovna enota | Zavihek **Splošno** in obrazci za **hitro ustvarjanje** | To polje se uporablja za privzeto nastavitev časovne enote za vsako vrstico vloge, povezane s tem cenikom. | Ta vrednost polja se uporablja samo pri nastavitvi cene za povezano vlogo. V cenikih za **stroške** in **prodajo** lahko ustvarite vrstico za ceno vloge v kateri koli časovni enoti. Tukaj določena časovna enota se uporablja kot privzeta. Uporabniške nastavitve, povezane s cenami vlog, lahko preglasijo to vrednost, da omogočijo nastavitev mere stroškov in obračuna za delo v kateri koli časovni enoti. |
| Opis | Zavihek **Splošno** in obrazci za **hitro ustvarjanje** | V tem besedilnem polju lahko navedete opis cenika v več vrsticah. | To polje je prikazano v pogledih **Povezani** na cenikih v različnih entitetah s povezanimi ceniki. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]