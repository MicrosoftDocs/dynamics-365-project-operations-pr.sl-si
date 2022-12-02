---
title: Razčlenitev stroškov
description: V tem članku je pojasnjeno, kako razčleniti stroške z uporabo prenovljenega delovnega prostora za stroške.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920954"
---
# <a name="expense-itemization"></a>Razčlenitev stroškov

[!include [banner](../includes/banner.md)]

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Organizacije od zaposlenih pogosto zahtevajo, da zagotovijo podrobno razčlenitev stroškov, nastalih med potovanjem. Na primer, mapa hotela lahko vsebuje več razčlenjenih vrstic za ceno sobe, davek, parkiranje in druge stroške, ki nastanejo vsak dan med trajanjem bivanja. Na primer stroški obroka lahko zahtevajo bolj natančno razčlenitev za zajtrk, kosilo ali večerjo. Ne glede na potrebe organizacije je mogoče vsako kategorijo stroškov nastaviti tako, da odraža podkategorije ali vrstične postavke, ki sestavljajo stroške. Čeprav je bila razčlenitev vedno podprta v možnosti **Upravljanje stroškov**, delovni prostor **Prenovljeni stroški** omogoča učinkovitejšo razčlenitev, če je omogočena funkcija **Sposobnost hitrega razčlenjevanja ponavljajočih se stroškov**.  

## <a name="enable-quick-itemization"></a>Omogočanje hitre razčlenitve 

Za hitro razčlenjevanje ponavljajočih se stroškov lahko uporabite funkcijo **Sposobnost hitrega razčlenjevanja ponavljajočih se stroškov**, pri čemer se izognete potrebi po vsakokratnem vnosu dnevnih stroškov za čas bivanja. Izvedite naslednje korake, da omogočite hitro razčlenjevanje.

1. Odprite delovni prostor **Upravljanje funkcij** in na seznamu funkcij poiščite in izberite možnost **Prenovljena poročila o stroških**. 
2. Izberite **Omogoči zdaj**. 
3. Na seznamu funkcij poiščite in izberite **Sposobnost hitrega razčlenjevanja ponavljajočih se stroškov**.
4. Izberite **Omogoči zdaj**. 

## <a name="itemization-grid"></a>Mreža razčlenitve 

Če ima kategorija stroškov podkategorije ali različne komponente, ki sestavljajo te stroške, jih je mogoče razčleniti. Če želite razčleniti stroške, izberite vrstico stroškov v poročilu o stroških in v podoknu **Podrobnosti o stroških** izberite **Dejanja** > **Razčlenitev**. Drsnik **Razčlenitev** razkrije mrežo s polji. Naslednja tabela ponuja primer vsakega polja v mreži in kako je polje upodobljeno v poročilu o stroških. 

|     Polje          |     Description                                                                                  |     Primer              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Podkategorija    |     Seznam podkategorij, konfiguriranih pod vrsto kategorije stroškov, **Hotel**.             |     Dnevna cena za sobo      |
|     Datum začetka     |     Datum, ko je prvič nastal element stroška.                                           |     13. 9. 2021           |
|     Dnevna cena     |     Znesek, ki je nastal za element stroška.                                                    |     200                  |
|     Količina       |     Število ponovitev stroška v neprekinjenem obdobju.                       |     3                    |

![Razčlenite strošek.](media/Itemization%20screen%201.png)

Ko shranite razčlenitev, boste videli posamezno razčlenjeno vrstico za količino, navedeno v mreži »Razčlenitev«. Vsaka vrstica se začne na datum, ki je naveden v mreži.

![Razčlenjeno poročilo.](media/Itemization%20screen%202.png)

