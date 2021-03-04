---
title: Nastavitev prodajnega cenika
description: Ta tema vsebuje informacije o prodajnih cenikih pri določanju cen za projekt.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176271"
---
# <a name="set-up-a-sales-price-list"></a>Nastavitev prodajnega cenika

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Za projektne ponudbe in pogodbe ima cenik projekta drugačen vzorec preglasitve cen kot cenik izdelkov. V vrstici ponudbe, ki temelji na katalogu izdelkov, lahko preglasite ceno za vloge in kategorije neposredno v vrstici ponudbe, saj vsaka vrstica ponudbe predstavlja natanko en kataloški izdelek. V vrstici ponudbe, ki temelji na projektu, pa ni mogoče preglasiti cene za vloge in kategorije neposredno v vrstici ponudbe. Cenik projekta lahko uporabite za delo z dvema različnima vzorcema preglasitve.

> [!NOTE]
> Priporočamo, da zaradi razlik v delovanju obeh pri preglasitvi cen uporabljate ločen cenik za svoje projektne vire in za katalog izdelkov.

Vsaka od naslednjih entitet ima lahko enega ali več povezanih prodajnih cenikov za cene v okviru projekta:

- Stranka (račun) 
- Priložnost 
- Ponudba 
- Projektna pogodba

Povezovanje teh entitet s cenikom določajo ceniki projektov. S prodajnimi entitetami »Stranka«, »Priložnost«, »Ponudba«, »Projektna pogodba« lahko povežete enega ali več cenikov.

Privzeti cenik projekta ni samodejno vnesen v zapisu stranke. Vendar pa lahko cenik projekta zapisu stranke ročno priložite. Kljub temu cenik projekta ročno priložite samo, če imate s stranko dogovorjene posebne cene. 

Ko je prodajni entiteti priloži cenik projekta, se preverijo naslednje informacije:

- Kontekst cenika je **Prodaja**. 
- Valuta cenika se ujema z valuto stranke. 

V projektni pogodbi se za samodejno nastavitev povezanih cenikov projekta uporabi naslednji vrstni red:

1. Citat
2. Priložnost
3. Stranki 
4. Globalne nastavitve 

Ko je cenik projekta privzeto vnesen, sistem preveri, ali se valuta ujema z valuto stranke in ali so privzeti ceniki bili vneseni s kontekstom **Prodaja**.

Z entitetami »Stranka«, »Priložnost«, »Ponudba«, »Projektna pogodba« lahko povežete več cenikov projekta. Ta zmožnost podpira datumsko določene privzete cene za dolgoročne projektne pogodbe, kjer boste morda potrebovali več kot en cenik, da se upošteva posodobitev cen, do katere pride zaradi inflacije. Če pa imajo ceniki, ki jih povežete z entiteto »Stranka«, »Priložnost«, »Ponudba«, »Projektna pogodba«, prekrivajočo datumsko veljavnost, so lahko privzete cene napačne. Zato se prepričajte, da ceniki projektov, ki imajo prekrivajočo datumsko veljavnost, niso povezani s temi entitetami.


[!INCLUDE[footer-include](../includes/footer-banner.md)]