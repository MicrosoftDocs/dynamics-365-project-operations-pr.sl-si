---
title: Razčlenitev stroškov
description: Ta tema pojasnjuje, kako razčleniti stroške z uporabo prenovljenega delovnega prostora Expense.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 34b11c6bd8be729957973a60fccccc2dd32c2669
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574542"
---
# <a name="expense-itemization"></a>Razčlenitev stroškov

[!include [banner](../includes/banner.md)]

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Organizacije pogosto zahtevajo, da zaposleni zagotovijo podrobno razčlenitev stroškov, nastalih med potovanjem. Na primer, hotelski list lahko vsebuje več razčlenjenih vrstic za ceno sobe, davek, parkiranje in druge različne stroške, ki nastanejo vsak dan med trajanjem bivanja. Ali pa bo zaradi stroškov obroka morda potrebno, da zagotovite bolj natančno razčlenitev za zajtrk, kosilo ali večerjo. Ne glede na potrebe organizacije lahko vsako kategorijo stroškov nastavite tako, da odraža podkategorije ali postavke vrstic, ki sestavljajo strošek. Medtem ko je bila razvrščanje po artiklih vedno podprto v **Upravljanje odhodkov**, **stroški** delovni prostor omogoča učinkovitejše razdeljevanje elementov, ko funkcija, **Sposobnost hitrega razvrščanja ponavljajočih se stroškov** je omogočeno.  

## <a name="enable-quick-itemization"></a>Omogoči hitro razvrščanje elementov 

Lahko uporabite **Sposobnost hitrega razvrščanja ponavljajočih se stroškov** funkcija za hitro razvrščanje ponavljajočih se stroškov, hkrati pa se izognete potrebi po vnosu dnevnih stroškov vsakič za čas bivanja. Izpolnite naslednje korake, da omogočite hitro razvrščanje elementov.

1. Pojdite na **Upravljanje funkcij** delovni prostor in na seznamu funkcij poiščite in izberite, **Prenovljena poročila o stroških**. 
2. Izberite **Omogoči zdaj**. 
3. Na seznamu funkcij poiščite in izberite, **Sposobnost hitrega razvrščanja ponavljajočih se stroškov**.
4. Izberite **Omogoči zdaj**. 

## <a name="itemization-grid"></a>Mreža za razvrščanje 

Če ima kategorija stroškov podkategorije ali različne komponente, ki sestavljajo ta odhodek, ga je mogoče razčleniti. Če želite razčleniti odhodek, izberite vrstico odhodkov v poročilu o stroških in v **Podrobnosti o stroških** podokno, izberite **Dejanja** > **Razčlenite**. The **Razdelitev po razdelkih** drsnik razkrije mrežo s polji. Naslednja tabela prikazuje primer vsakega polja v mreži in kako je polje upodobljeno v poročilu o stroških. 

|     Polje          |     Description                                                                                  |     Primer              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Podkategorija    |     Seznam podkategorij, konfiguriranih pod vrsto kategorije stroškov, **Hotel**.             |     Dnevna cena sobe      |
|     Datum začetka     |     Datum, ko je bil odhodek prvič nastal.                                           |     09. 2021           |
|     Dnevna stopnja     |     Znesek, nastal za postavko odhodka.                                                    |     200                  |
|     Količina       |     Kolikokrat se polnjenje ponovi v neprekinjenem obdobju.                       |     3                    |

![Navedite stroške.](media/Itemization%20screen%201.png)

Ko shranite postavko, boste videli posamezno razčlenjeno vrstico za količino, določeno v mreži razdelkov. Vsaka vrstica se začne na datum, ki je naveden v mreži.

![Podrobno poročilo.](media/Itemization%20screen%202.png)

