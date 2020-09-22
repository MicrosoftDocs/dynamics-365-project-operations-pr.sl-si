---
title: Pregled nedokončanih opravil za izdajo računov pri projektih in projektnih pogodbah
description: Ta tema vsebuje informacije o tem, kako pregledati nedokončana opravila za čas, stroške in izdelke in kako jih označiti kot pripravljene za izdajo računa.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: db15ea136b9939c0a0631936bcadab538bf2dd4a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755845"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Pregled nedokončanih opravil za izdajo računov pri projektih in projektnih pogodbah

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ko je za transakcijo mogoče ustvariti in obdelati račun, mora biti označena z možnostjo **Pripravljeno za izdajanje računov**. Ta tema opisuje vrste transakcij, ki jih je mogoče ustvariti.

## <a name="review-the-time-and-material-billing-backlog"></a>Pregled nedokončanih opravil obračunavanja časa in materiala

Ko je časovni ali stroškovni vnos predložen in odobren za določen projekt, PSA ustvari dejanske vrednosti projekta. Če se projekt in razred transakcije skupaj preslikata v podrobnosti pogodbe za projekt, za katerega je potreben tako čas kot material, se ob odobritvi vnosa ustvarita dve dejanski vrednosti:

- Dejanska cena 
- Dejanski nezaračunani znesek prodaje

Dejanski nezaračunani zneski prodaje predstavljajo nedokončana opravila obračunavanja, zato je treba njihovo stanje obračunavanja nastaviti na **Pripravljeno na izdajanje računov**. Ko ustvarite račun za projekt, se dejanski nezaračunani zneski prodaje, označeni kot **Pripravljeno za izdajanje računov**, prekopirajo kot podrobnosti vrstice računa.

Če želite pregledati nezaračunana opravila obračunavanja za čas in materiale, odprite možnost **Prodaja** \> **Obračunavanje** \> **Nedokončana opravila obračunavanja časa in materiala**. Izberite vse dejanske nezaračunane zneske prodaje, ki so pripravljeni za izdajo računa, in nato izberite možnost **Pripravljeno za izdajanje računov**. Stanje obračunavanja teh dejanskih zneskov se bo spremenilo v **Pripravljeno na izdajanje računov**.

![Nedokončana opravila obračunavanja časa in materiala](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Pregled nedokončanih opravil obračunavanja izdelkov

Če ima projektna pogodba v PSA podrobnosti pogodbe na podlagi izdelkov, se te podrobnosti upoštevajo pri izdaji računov ob vsakokratnem ustvarjanju računa za projektno pogodbo. Vsi izdelki, katerih podrobnosti pogodbe so označene kot **Pripravljeno na izdajanje računov**, se prekopirajo v račun projekta v obliki projektnih vrstic računa.

Če želite pregledati nedokončana opravila obračunavanja izdelkov, pojdite v **Prodaja** \> **Obračunavanje** \> **Nedokončana opravila obračunavanja izdelkov**. Izberite vse podrobnosti pogodbe na podlagi izdelka, ki so pripravljene za izdajo računa, in nato izberite možnost **Pripravljeno za izdajanje računov**. Stanje obračunavanja teh podrobnosti se bo spremenilo v **Pripravljeno na izdajanje računov**.

![Nedokončana opravila obračunavanja izdelkov](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Pregled mejnikov obračunavanja za pogodbe s fiksno ceno

Vsaka podrobnost projektne pogodbe, ki uporablja način obračunavanja s fiksno ceno, mora določiti mejnike pogodbe. Za te mejnike pogodbe je mogoče izdati račun le, če so označeni kot **Pripravljeno za izdajanje računov**. 

Če želite pregledati mejnike obračunavanja, odprite možnost **Prodaja** \> **Obračunavanje** \> **Mejniki s fiksno ceno**. Izberite mejnike, ki so pripravljeni za izdajo računa, in nato izberite možnost **Pripravljeno za izdajanje računov**. Stanje obračunavanja teh mejnikov se bo spremenilo v **Pripravljeno na izdajanje računov**.

![Mejniki s fiksno ceno](media/FPBacklog.png)
