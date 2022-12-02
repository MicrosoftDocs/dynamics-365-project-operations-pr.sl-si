---
title: Novosti za maj 2021 – poenostavljeno uvajanje Project Operations
description: Ta članek vsebuje informacije o posodobitvah kakovosti, ki so bile na voljo v izdaji za poenostavljeno uvajanje Project Operations maja 2021.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a5d67159b732e0309e03c64fb6dadcc7b8cbff51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934202"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Novosti za maj 2021 – poenostavljeno uvajanje Project Operations

_Velja za: poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta članek velja za naslednje komponente in različice aplikacije Dynamics 365 Project Operations:

   - Project Operations v okolju Dataverse različice 4.10.0.186.

## <a name="features-included-in-this-release"></a>Funkcije, ki so na voljo v tej izdaji:

V to izdajo so vključene naslednje funkcije:

- [Načini razporejanja](../../project-management/scheduling-modes.md): vodje projektov lahko zdaj določijo, ali naj se projekt upravlja z nespremenljivim trajanjem, nespremenljivim delom ali načinom razporejanja nespremenljivih enot.

## <a name="quality-updates"></a>Posodobitve kakovosti

| **Območje funkcij** | **Številka sklica** | **Posodobitev kakovosti** |
| --- | --- | --- |
| Zaračunavanje in cene | 2224568 | Dodana logika za omogočanje prilagoditev, ki vključujejo priklic vtičnika za potrditev računa. |
| Zaračunavanje in cene | 2101098 | Logika privzetih polj za predračun je izboljšana. Ta polja vključujejo **Naslov plačnika**, **Ime plačnika** in **Plačilne pogoje**. Polja so zdaj privzeto pridobljena iz ustreznega zapisa stranke za projektno pogodbo. |
| Zaračunavanje in cene | 2021413 | Posodobljeni polji **Dejanski stroški** in **Prodaja** v entiteti **Opravilo**, da se vključi prodajne vrednosti iz naslova neobračunanih in obračunanih stroškov za opravila. |
| Zaračunavanje in cene | 2182110 | Pri kopiranju projektne pogodbe se ID podrobnosti pogodbe znova ustvari v ciljni projektni pogodbi, da se zagotovi njegova edinstvenost. |
| Upravljanje priložnosti | 2186741 | Dodana preverjanja veljavnosti, da se zagotovi, da polj **Izvor** in vrsta transakcije ni mogoče posodobiti pri obstoječih podrobnostih o ponudbi. |
| Upravljanje priložnosti | 2191353 | Ustvarjanje mejnikov ne sme biti dovoljeno v podrobnosti pogodbe za čas in material. |
| Upravljanje priložnosti | 2216956 | Odpravite težave z možnostjo **Posodobi cene**. |
| Načrtovanje in sledenje | 2182979 | Izboljšana je funkcija kopiranja projekta, ki zagotavlja kopiranje vrstic za oceno stroškov iz prvotnega projekta. |
| Načrtovanje in sledenje | 2184144 | Izboljšana je funkcija kopiranja projekta, ki zagotavlja kopiranje imena položaja vira iz prvotnega projekta. |
| Načrtovanje in sledenje | 2184799 | Poostren je nadzor pri kopiranju projekta, ki zagotavlja, da predvidenega začetnega datuma ni mogoče spremeniti med kopiranjem. |
| Načrtovanje in sledenje | 2185134 | Med kopiranjem projekta je predvideni začetni datum ciljnega projekta nastavljen na današnji datum. |
| Načrtovanje in sledenje | 2196373 | Zagotovite, da se zapisi vodje projekta in članov ekipe pri kopiranju projekta v projektni skupini ne podvajajo. |
| Načrtovanje in sledenje | 2211833 | Opravila virov se kopirajo iz izvornega projektnega opravila v ciljni projekt. |
| Načrtovanje in sledenje | 2186541 | Odpravljene težave na mreži **Ocene** pri razvrščanju po **virih**. |
| Načrtovanje in sledenje | 2166906 | Kategorija transakcije iz opravila je treba kopirati v entiteto **Dodelitev virov**. |
| Upravljanje virov | 2125362 | Odpravljene težave z ustvarjanjem splošnega člana ekipe z uporabo metode dodeljevanja na podlagi ur. |
| Čas in strošek | 2113603 | Odpravljena težava, povezana s prilagoditvijo, z odstranjevanjem atributov iz strani **Vnos časa**. Sistem preveri, ali atribut obstaja na strani, preden do atributa dostopa s pomočjo skripta. |
| Čas in strošek | 2204377 | Ko izberete **Kopiraj teden**, se morajo kopirani časovni listi prikazati samodejno. |
| Čas in strošek | 2209059 | Polje **Stanje** je mogoče urejati za časovne vnose v storitvi Dynamics 365 Field Service. |
