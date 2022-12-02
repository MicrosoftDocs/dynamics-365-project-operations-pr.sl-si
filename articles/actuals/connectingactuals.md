---
title: Povezave transakcij – povezovanje dejanskih vrednosti različnih vrst transakcij
description: V tem članku je pojasnjeno, kako se povezava transakcije uporablja za povezovanje dejanskih vrednosti različnih vrst za pomoč pri sledenju dobičkonosnosti, nedokončanim opravilom obračunavanja in izračunom obračunanih in neobračunanih prihodkov.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926106"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Povezave transakcij – povezovanje dejanskih vrednosti različnih vrst transakcij

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Zapisi povezav transakcije so ustvarjeni za povezovanje dejanskih vrednosti različnih vrst, ko se čas, stroški ali poraba materiala premikajo v življenjskem ciklu od faze ponudbe ali predprodaje do faze pogodbe, odobritev in/ali odpoklicev, izstavljanja računov in morebitnega dobropisa ali izstavljanja popravljenih računov.

Naslednji primer prikazuje običajno obdelavo časovnih vnosov v življenjskem ciklu projekta v aplikaciji Project Operations.

> ![Obdelava časovnih vnosov v aplikaciji Project Operations.](media/basic-guide-17.png)

Obdelava časovnih vnosov v življenjskem ciklu projekta v aplikaciji Project Operations poteka po naslednjih korakih: 

1. Pošiljanje časovnega vnosa povzroči ustvarjanje dveh vrstic dnevnika: eno za strošek in eno za neobračunano prodajo. 
2. Morebitna odobritev časovnega vnosa povzroči ustvarjanje dveh dejanskih vrednosti: eno za strošek in eno za neobračunano prodajo. Ti dve dejanski vrednosti sta povezani s povezavami transakcij.
3. Ko uporabnik ustvari račun projekta, se transakcija vrstice računa ustvari z uporabo podatka iz dejanske vrednosti neobračunane prodaje.
4. Ko je račun potrjen, sta ustvarjeni dve novi dejanski vrednosti: stornirana neobračunana prodaja in dejanska vrednost obračunane prodaje. Stornirana neobračunana prodaja in izvirna neobračunana dejanska prodaja sta povezani s povezavami razveljavitvene transakcije. Obračunana prodaja in izvirna neobračunana dejanska prodaja sta prav tako povezani, da prikažeta povezave med prihodki, ki so bili nekoč nedokončani ali delo v teku (WIP), zdaj pa so obračunani.   

Vsak dogodek v poteku dela obdelave sproži ustvarjanje zapisov v tabeli **Povezava transakcije**. To omogoča ustvarjanje sledi odnosov med zapisi, ki so ustvarjeni v časovnem vnosu, vrstici dnevnika, dejanski vrednosti in podrobnostih vrstice računa.

Spodnja tabela prikazuje zapise v entiteti **Povezava transakcije** za predhodni potek dela.

|Dogodek                   |Transakcija 1                 |Vloga transakcije 1 |Vrsta transakcije 1       |Transakcija 2          |Vloga transakcije 2 |Vrsta transakcije 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Pošiljanje časovnega vnosa   |GUID vrstice dnevnika (prodaje)     |Neobračunana prodaja |msdyn_journalline            |GUID vrstice dnevnika (stroška)     |Stroški            |msdyn_journalline  |
|Odobritev časa           |GUID dejanskega neobračunanega zneska (prodaje)  |Neobračunana prodaja |msdyn_actual                 |GUID dejanske vrednosti stroška (strošek)       |Stroški            |msdyn_actual       |
|Ustvarjanje računa        |GUID podrobnosti vrstice računa      |Obračunana prodaja   |msdyn_invoicelinetransaction |GUID dejanskega neobračunanega zneska prodaje   |Neobračunana prodaja  |msdyn_actual       |
|Potrditev računa    |GUID storniranega dejanskega zneska         |Storniranje      |msdyn_actual                 |GUID izvorne neobračunane prodaje |Izvirnik        |msdyn_actual       |
|                        |GUID obračunane prodaje             |Obračunana prodaja   |msdyn_actual                 |GUID dejanskega neobračunanega zneska prodaje   |Neobračunana prodaja  |msdyn_actual       |
|Popravek osnutka računa |GUID transakcije vrstice računa|Nadomeščanje      |msdyn_invoicelinetransaction |GUID obračunane prodaje            |Izvirnik        |msdyn_actual       |
|Potrditev popravka računa|GUID storniranja obračunane prodaje  |Storniranje      |msdyn_actual                 |GUID obračunane prodaje            |Izvirnik        |msdyn_actual       |
|                        |Nova neobračunana prodaja GUID |Nadomeščanje            |msdyn_actual                 |GUID obračunane prodaje            |Izvirnik        |msdyn_actual       |


Naslednja slika prikazuje povezave, ki so ustvarjene med različnimi vrstami dejanskih vrednosti ob različnih dogodkih z uporabo primera časovnih vnosov v aplikaciji Project Operations.

> ![Kako so dejanske vrednosti različnih vrst med seboj povezane v aplikaciji Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
