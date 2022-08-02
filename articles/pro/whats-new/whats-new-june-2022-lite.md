---
title: Novosti za junij 2022 – poenostavljeno uvajanje aplikacije Project Operations
description: V tem članku so informacije o posodobitvah kakovosti, ki so na voljo v izdaji Microsofta junija 2022 Dynamics 365 Project Operations enostavna uvedba.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031213"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Novosti za junij 2022 – poenostavljeno uvajanje aplikacije Project Operations

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Ta članek se nanaša na naslednje komponente in različice Microsofta Dynamics 365 Project Operations:

- Projektne operacije v a Dataverse okoljska različica 4.43.0.77 ali 4.43.0.119

## <a name="quality-updates"></a>Posodobitve kakovosti

| Območje funkcij | Številka sklica | Posodobitev kakovosti |
| --- | --- | --- |
| Podizvajanje | 2708885 | Odpravljeno je sporočilo o napaki, ki se prikaže, ko uporabnik ustvari zapis glave rezervacije vira, ki ga je mogoče rezervirati, kjer ni izpolnjen vir, ki ga je mogoče rezervirati. |
| Načrtovanje in sledenje projektov | 2629441 | Popravljena je bila logika sprožitve delovnega toka, da bi preprečili neskončno zanko, ko so projektne naloge posodobljene. |
| Čas in strošek | 2641209 | Uvozi časovnih vnosov iz dodelitev/rezervacij morajo ohraniti referenco vira, ki ga je mogoče rezervirati. |
| Načrtovanje in sledenje projektov | 2651148 | Glava projektnega dokumenta mora biti varovana.|
| Načrtovanje in sledenje projektov | 2653145 | Dodana preverjanja veljavnosti za zagotovitev, da ni mogoče ustvariti zapisa projekta, ki ima v imenu neveljavne znake. |
| Čas in strošek | 2654710 | Popravljeno filtriranje na **Odobritve** strani. |
| Zaračunavanje in cene | 2667805 | Dodana preverjanja veljavnosti za pomoč pri preprečevanju ustvarjanja zaračunanih dejanskih prodajnih vrednosti, če podporne nezaračunane dejanske prodajne vrednosti ne obstajajo. |
| Zaračunavanje in cene | 2668378 | Dodana preverjanja veljavnosti za pomoč pri preprečevanju dodajanja dimenzij cen po meri, razen če sta izpolnjena logično ime in ime polja. |
| Čas in strošek | 2700428 | Izboljšana je logika odobritev za zagotovitev, da je mogoče obdelati druge nize odobritev za projekt, tudi če je eden od nizov odobritev obtičal v sistemskih opravilih. |
