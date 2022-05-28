---
title: Novosti za april 2021 – poenostavljeno uvajanje Project Operations
description: Ta tema vsebuje informacije o posodobitvah kakovosti, ki so bile na voljo v izdaji za poenostavljeno uvajanje Project Operations aprila 2021.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 10d9498636d8c5f72b7544be4ec30f399d5e0311
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598140"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Novosti za april 2021 – poenostavljeno uvajanje Project Operations

_Velja za: poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta tema velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

  - Project Operations v okolju Dataverse različice 4.9.0.221 

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

V to izdajo so vključene naslednje funkcije:

- Materiali, ki niso na zalogi, za projekte. Ključne zmožnosti vključujejo:
  - Ocenjevanje in določanje cen materialov, ki niso na zalogi, med prodajnim ciklom za projekt. Za več informacij glejte [Nastavitev cen in stopenj prodaje za izdelke iz kataloga – poenostavljena različica](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Sledenje uporabi materialov, ki niso na zalogi, med izvajanjem projekta. Za več informacij glejte [Beleženje uporabe materiala v projektih in projektnih nalogah](../../material/material-usage-log.md).
  - Izdajanje računov za stroške materialov, ki niso na zalogi. Za več informacij glejte [Upravljanje nedokončanih opravil obračunavanja – poenostavljena različica](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Novi API-ji v storitvi Dynamics 365 Dataverse omogočajo postopke ustvarjanja, posodabljanja in brisanja z **entitetami razporejanja**. Za več informacij glejte [Uporaba API-jev razporeda za izvajanje opravil z entitetami razporejanja](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Posodobitve kakovosti

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| Zaračunavanje in cene | 2224568 | Dodana logika za omogočanje prilagoditev, ki vključujejo priklic vtičnika za potrditev računa. |
| Zaračunavanje in cene | 2101098 | Izboljšana logika privzetih polj za predračun: **Naslov plačnika**, **Ime plačnika** in **Plačilni pogoji** se zdaj privzeto prikažejo iz ustreznega zapisa stranke o pogodbi o projektu. |
| Zaračunavanje in cene | 2021413 | Posodobljeni polji **Dejanski stroški** in **Prodaja** v entiteti **Opravilo**, da se vključi prodajne vrednosti iz naslova neobračunanih in obračunanih stroškov za opravila. |
| Zaračunavanje in cene | 2182110 | Pri kopiranju projektne pogodbe se ID podrobnosti pogodbe znova ustvari v ciljni projektni pogodbi, da se zagotovi njegova edinstvenost. |
| Upravljanje priložnosti | 2186741 | Dodana preverjanja veljavnosti, da se zagotovi, da polj **Izvor** in **Vrsta transakcije** ni mogoče posodobiti pri obstoječih podrobnostih o ponudbi. |
| Upravljanje priložnosti | 2191353 | Mejniki ne smejo biti ustvarjeni v podrobnosti pogodbe za čas in material. |
| Upravljanje priložnosti | 2216956 | Odpravite težave z možnostjo **Posodobi cene**. |
| Načrtovanje in sledenje | 2182979 | Izboljšana je funkcija kopiranja projekta, ki zagotavlja kopiranje vrstic za oceno stroškov iz prvotnega projekta. |
| Načrtovanje in sledenje | 2184144 | Izboljšana je funkcija kopiranja projekta, ki zagotavlja kopiranje imena položaja vira iz prvotnega projekta. |
| Načrtovanje in sledenje | 2184799 | Kopija projekta: poostren nadzor za zagotovitev, da predvidenega začetnega datuma ni mogoče spremeniti med kopiranjem. |
| Načrtovanje in sledenje | 2185134 | Kopija projekta: Predviden datum začetka ciljnega projekta je današnji datum. |
| Načrtovanje in sledenje | 2196373 | Kopija projekta: Zagotovite, da se zapisi vodje projekta in članov ekipe v projektni skupini ne podvajajo. |
| Načrtovanje in sledenje | 2211833 | Kopija projekta: Opravila virov se kopirajo iz izvornega projektnega opravila v ciljni projekt. |
| Načrtovanje in sledenje | 2186541 | Odpravljene težave na mreži **Ocene** pri razvrščanju po virih. |
| Načrtovanje in sledenje | 2166906 | Kategorija transakcije iz opravila je treba kopirati v entiteto **Dodelitev virov**. |
| Upravljanje virov | 2125362 | Odpravljene težave z ustvarjanjem splošnega člana ekipe z uporabo metode dodeljevanja na podlagi ur. |
| Čas in strošek | 2113603 | Odpravljena težava, povezana s prilagoditvijo, z odstranjevanjem atributov iz strani **Vnos časa**. Sistem zdaj preveri, ali atribut obstaja na strani, preden do njih dostopa s pomočjo skripta. |
| Čas in strošek | 2204377 | Ko izberete **Kopiraj teden** med vnosom časa, se kopirani časovni listi morajo prikazati samodejno. |
| Čas in strošek | 2209059 | Polje **Stanje** lahko urejate za časovne vnose Dynamics 365 Field Service. |
