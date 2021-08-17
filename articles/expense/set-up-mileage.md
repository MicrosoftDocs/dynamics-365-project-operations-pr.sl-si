---
title: Nastavitev prevožene razdalje s stopnjami prevožene razdalje
description: Ta tema vsebuje podatke o prevoženi razdalji in stopnjah prevožene razdalje.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 030c6abca169b712312ad70ed2ac8262f3d0777bcf93dcccfd956f2f9e0ea77c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993081"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Nastavitev prevožene razdalje s stopnjami prevožene razdalje

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ko se poroča o strošku in je izbrana kategorija stroškov **Prevožena razdalja**, se znesek za to vrstico stroškov izračuna v skladu z zneskom *stopnje na prevoženo razdaljo*. Ta znesek se določi z določenimi stopnjami prevožene razdalje ali, če ni določena nobena stopnja prevožene razdalje, z upoštevanjem standardne stopnje za prevoženo razdaljo. 

Stopnje prevožene razdalje lahko nastavite tako, da odprete zavihek **Upravljanje stroškov** > **Nastavitev** > **Splošno** > **Kategorije stroškov** > **Prevožena razdalja** > **Nastavitev kategorije**.

Če vaša organizacija po nadgradnji na različico 10.0.18 uporablja kategorijo stroškov prevožene razdalje, po pregledu spodnjih sprememb oblikovanja razmislite o omogočanju funkcije prevožene razdalje. 

Novo oblikovanje ravni za stopnjo prevožene razdalje vpliva na to, kako se obdela vrednost v polju **Količina**. Pred izdajo različice 10.0.18 je bila vrednost v polju **Količina** spodnja meja. Ko je kopičenje preseglo to vrednost, je bila uporabljena ustrezna stopnja.  Od različice 10.0.18 naprej je vrednost v polju **Količina** zgornja meja. Ustrezna stopnja se uporablja, kadar je kopičenje prevožene razdalje manjše od vrednosti v polju **Količina**.  Novi model stopenj prevožene razdalje pomaga pri doslednosti v stopnjah prevožene razdalje in boljši uporabnosti.   

Vsa odobrena poročila o stroških se bodo med knjiženjem preračunala v skladu z novim oblikovanjem.

## <a name="example"></a>Primer
 
### <a name="before-version-10018"></a>Pred različico 10.0.18
Z dvema stopnjama prevožene razdalje polje **Količina** na vsaki stopnji predstavlja spodnjo mejo prevožene razdalje. Trenutno ima prva raven vrednost nič (0) in stopnjo 0,45, druga raven pa vrednost 1000 in stopnjo 0,25. Če nakopičene milje ali kilometri presežejo vrednost v polju, se uporabi ustrezna stopnja. Če ni vrstic z ničelno količino, sistem uporabi stopnjo prevožene razdalje, ki je določena v upravljanju stroškov. 
 
Če zaposleni predloži poročilo o stroških s 1.500 miljami, sta dve vrstici prevožene razdalje v objavljenem poročilu o stroških: 1000 (stopnja 0,45) + 500 (stopnja 0,25) = 575,00.

### <a name="after-version-10018"></a>Po različici 10.0.18
V različici 10.0.18 polje **Količina** na vsaki ravni predstavlja zgornjo mejo ravni. Trenutno ima prva raven vrednost nič (999) in stopnjo 0,45, druga raven pa vrednost 999.999.999,00 in stopnjo 0,25. Če nakopičene milje ali kilometri presežejo vrednost v polju **Količina**, se uporabi ustrezna stopnja. Če so presežene vse zgornje meje, sistem uporabi stopnjo prevožene razdalje, ki je določena v upravljanju stroškov. 
 
Če želite pravilno izračunati isti scenarij, je treba spremeniti nastavljeno raven. Polje **Količina** ima na prvi ravni vrednost 999,00 in vrednost 999.999.999,00 na drugi ravni. Če zaposleni preseže skupno količino milj ali kilometrov na prvi ravni, sistem uporabi stopnjo prevožene razdalje, ki je določena v upravljanju stroškov. 
  
Če zaposleni predloži poročilo o stroških s 1.500 miljami, sta dve vrstici prevožene razdalje v objavljenem poročilu o stroških: 1000 (stopnja 0,45) + 500 (stopnja 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Omogočanje izračuna količine prevožene razdalje za več ravni prevoženih kilometrov z isto funkcijo stopnje

Funkcija **Omogočanje izračuna količine prevožene razdalje za več ravni prevožene razdalje z isto funkcijo stopnje** izboljša izračun stopnje prevožene razdalje. Za omogočanje te funkcije sledite naslednjim korakom.

1. Odprite zavihek **Delovni prostori** > **Upravljanje funkcije**. 
2. Na seznamu poiščite in izberite **Izračun količine prevožene razdalje za več ravni prevožene razdalje z enako stopnjo** ter nato izberite možnost **Omogoči zdaj**.

Ko omogočite funkcijo, ponastavite ravni prevožene razdalje, da bodo pravilno odražale vrednost v polju **Količina**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
