---
title: Transakcijske povezave - Povežite dejansko stanje različnih vrst transakcij
description: Ta tema pojasnjuje, kako se transakcijska povezava uporablja za povezovanje dejanskih dejstev različnih vrst za pomoč pri sledenju dobičkonosnosti, zaostankov obračunavanja in izračunov zaračunanega v primerjavi z nezaračunanim prihodkom.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580798"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Transakcijske povezave - Povežite dejansko stanje različnih vrst transakcij

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Zapisi o transakcijskih povezavah so ustvarjeni za povezavo dejanskih dejstev različnih vrst, ko se poraba časa, stroškov ali materiala premika v njegovem življenjskem ciklu od stopnje ponudbe ali predprodaje v fazo pogodbe, odobritve in/ali odpoklici, izdajanje računov in morebitno kreditno ali korektivno fakturiranje.

Naslednji primer prikazuje običajno obdelavo časovnih vnosov v življenjskem ciklu projekta v aplikaciji Project Operations.

> ![Obdelava vnosov časa v projektnih operacijah.](media/basic-guide-17.png)

Obdelava časovnih vnosov v življenjskem ciklu projekta Project Operations sledi tem korakom: 

1. Predložitev časovnega vnosa povzroči, da se ustvarita dve vrstici dnevnika: ena za stroške in ena za neobračunano prodajo. 
2. Končna odobritev časovnega vnosa povzroči, da se ustvarita dve dejanski vrednosti: ena za stroške in ena za neobračunano prodajo. Ti 2 dejanski vrednosti sta povezani s transakcijskimi povezavami.
3. Ko uporabnik ustvari račun projekta, se transakcija vrstice računa ustvari z uporabo podatka iz dejanske vrednosti neobračunane prodaje.
4. Ko je račun potrjen, se ustvarita dve novi dejanski vrednosti: neobračunana razveljavitev prodaje in zaračunana dejanska prodaja. Nezaračunana razveljavitev prodaje in prvotna neobračunana dejanska prodaja sta povezana s povezavami obrnjene transakcije. Zaračunana prodaja in prvotna neobračunana dejanska prodaja sta povezana tudi, da pokažeta povezave med prihodki, ki so bili nekoč zaostanki ali nedokončane dejavnosti (WIP), in zdajšnjim zaračunanim prihodkom.   

Vsak dogodek v delovnem toku obdelave sproži ustvarjanje zapisov v **Transakcijska povezava** mizo. To pomaga zgraditi sled Odnosi med zapisi, ki so ustvarjeni med podatki o časovnem vnosu, vrstici dnevnika, dejanski in fakturni vrstici.

Naslednja tabela prikazuje zapise v **Transakcijska povezava** subjekt za prejšnji potek dela.

|Dogodek                   |Transakcija 1                 |Vloga transakcije 1 |Vrsta transakcije 1       |Transakcija 2          |Vloga transakcije 2 |Vrsta transakcije 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Pošiljanje časovnega vnosa   |GUID vrstice dnevnika (prodaje)     |Neobračunana prodaja |msdyn_journalline            |GUID vrstice dnevnika (stroška)     |Stroški            |msdyn_journalline  |
|Odobritev časa           |GUID dejanskega neobračunanega zneska (prodaje)  |Neobračunana prodaja |msdyn_actual                 |GUID dejanske vrednosti stroška (strošek)       |Stroški            |msdyn_actual       |
|Ustvarjanje računa        |GUID podrobnosti vrstice računa      |Obračunana prodaja   |msdyn_invoicelinetransaction |GUID dejanskega neobračunanega zneska prodaje   |Neobračunana prodaja  |msdyn_actual       |
|Potrditev računa    |GUID storniranega dejanskega zneska         |Storniranje      |msdyn_actual                 |GUID izvorne neobračunane prodaje |Izvirnik        |msdyn_actual       |
|                        |GUID obračunane prodaje             |Obračunana prodaja   |msdyn_actual                 |GUID dejanskega neobračunanega zneska prodaje   |Neobračunana prodaja  |msdyn_actual       |
|Popravek osnutka računa |GUID transakcije vrstice računa|Nadomeščanje      |msdyn_invoicelinetransaction |GUID obračunane prodaje            |Izvirnik        |msdyn_actual       |
|Potrditev popravka računa|GUID storniranja obračunane prodaje  |Storniranje      |msdyn_actual                 |GUID obračunane prodaje            |Izvirnik        |msdyn_actual       |
|                        |Nov GUID nezaračunane prodaje |Nadomeščanje            |msdyn_actual                 |GUID obračunane prodaje            |Izvirnik        |msdyn_actual       |


Naslednja slika prikazuje povezave, ki so ustvarjene med različnimi vrstami dejanskega stanja na različnih dogodkih na primeru časovnih vnosov v Operacijah projekta.

> ![Kako so dejanski podatki različnih vrst med seboj povezani v projektnih operacijah.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
