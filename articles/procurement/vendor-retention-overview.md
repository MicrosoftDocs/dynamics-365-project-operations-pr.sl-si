---
title: Pregled zadrževanja dobaviteljev
description: Ta tema vsebuje pregled zmogljivosti zadrževanja dobaviteljev.
author: sigitac
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5f89904af5fb00eac46de834a438f412b371e74e
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594629"
---
# <a name="vendor-retention-overview"></a>Pregled zadrževanja dobaviteljev

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Vaša organizacija bo morda želela zadržati del plačil dobaviteljem, ki delajo na projektih za vašo organizacijo. Na primer, preden plačate dobavitelju, se boste morda želeli prepričati, da izdelki in storitve, ki so jih zagotovili, ustrezajo vašim pričakovanjem.

Ko se z dobavitelji pogajate o nakupih za projekte, lahko določite pogoje zadrževanja dobavitelja, ki vključujejo odstotek ali znesek za zadržanje. Ko dobavitelj zagotavlja izdelke in storitve, odbijete navedeni odstotek zadržanja ali znesek od plačila dobavitelju. Ko je projekt končan ali doseže vmesno stopnjo, kot je določeno v pogodbi dobavitelja, sprostite zadržani znesek in ustvarite plačilo dobavitelju.

## <a name="vendor-retention-example"></a>Primer zadrževanja dobaviteljev

Naslednji primer prikazuje, kako se odstotek od zneska računa dobavitelja zadrži na podlagi odstotka, ki je dokončan za projekt.

Contoso Robotics ZDA je sklenil pogodbo z dobaviteljem Fabrikam za zagotovitev 100 ur usposabljanja za projekt obnovitve opreme. Skupna vrednost pogodbe je 30.000 USD z dogovorjeno nakupno ceno 300 USD na uro.

Usposabljanje bo potekalo v treh fazah po naslednjem urniku:

- 1. faza: 50 ur ali 50 odstotkov projekta
- 2. faza: 30 ur ali skupno 80 odstotkov projekta
- 3. faza: 20 ur ali 100 odstotkov projekta

V naslednji tabeli so navedeni pogoji zadrževanja.

| **Odstotek dobavljenih enot** | **Odstotek za zadrževanje** | **Odstotek za sprostitev** |
| --- | --- | --- |
| 50 % | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100 % | 0 % | 100 % |

Posledice transakcij so naslednji zneski:

- 1. faza:
  - Znesek za plačilo je 50 x 300 ali 15.000.
  - 20 odstotkov zneska ali 3000 se zadrži in bo sproščeno v poznejši fazi.
  - Znesek, ki je plačan dobavitelju, je 12.000.
- 2. faza:
  - Znesek za plačilo je 30 x 300 ali 9000.
  - 10 odstotkov zneska ali 900 se zadrži.
  - 10 odstotkov od 3000, ki so bili zadržani v 1. fazi, ali 300 se sprosti.
  - Znesek, ki je plačan dobavitelju, je 8400. Ta znesek je 9000 minus zadrževanje 900 plus 300, ki so bili sproščeni iz zadrževanja v 1. fazi.
- 3. faza:
  - Znesek za plačilo je 20 x 300 ali 6000.
  - Noben znesek se ne zadrži.
  - Znesek, ki je sproščen, je 3600. Ta znesek je sestavljen iz 3000, ki so bili zadržani v 1. fazi minus 300 iz 1. faze, ki so bili sproščeni v 2. fazi, plus 900, ki so bili zadržani v 2. fazi.
  - Znesek, ki je plačan dobavitelju, je 9600. Ta znesek obsega zadržani znesek 3600 plus 6000 za dokončanje 3. faze.

Skupni znesek, plačan dobavitelju po končanih treh fazah, je 30.000, kar je skupni znesek naročilnice (15.000 + 9000 + 6000).
