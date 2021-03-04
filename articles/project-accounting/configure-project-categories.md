---
title: Konfiguracija kategorij projekta
description: Ta tema vsebuje informacije o nastavitvah kategorij projekta.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131948"
---
# <a name="configure-project-categories"></a>Konfiguracija kategorij projekta

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Aplikacija Project Operations ponuja zanesljive zmogljivosti za kategorizacijo prihodkov in odhodkov za posamezni projekt. Kategorije omogočajo poročanje in analizo projektnih transakcij ter vodenje knjiženja v glavni knjigi.

Naslednji diagram prikazuje korelacijo med kategorijami transakcij, skupnimi kategorijami in kategorijami projektov. 

Kategorije transakcij so osnovna skupina za projektne transakcije. Znotraj te skupine obstaja nabor skupnih kategorij, ki jih je mogoče deliti med aplikacijami in moduli. Še bolj podrobno, kategorije projekta so najbolj natančna raven kategorij. Kategorije projektov so lastne posamezni pravni osebi, modulu in aplikaciji.

![Korelacija med kategorijami transakcij, skupnimi kategorijami in kategorijami projektov](media/project-categories.png)

## <a name="transaction-categories"></a>Kategorije transakcij

Kategorije transakcij predstavljajo osnovno razvrščanje projektnih transakcij in niso določene glede na podjetje ali vrsto transakcije. Družba Contoso Robotics na primer za razvrščanje projektnih transakcij uporablja kategorije načrtovanja, potovanja, namestitve in storitvenih transakcij.

Kategorije transakcij so definirane v modulu Project Operations. 
1. Obrazec lahko odprete v razdelku **Nastavitve** \> **Kategorije transakcij**. 
2. Ustvarite novo kategorijo transakcij bodisi z izbiro možnosti **Novo** ali pa z izbiro možnosti **Uvoz iz Excela**.

## <a name="shared-categories"></a>Kategorije v skupni rabi

Rešitev Dynamics 365 uporablja skupno rabo kategorij za kategorizacijo stroškov v različnih aplikacijah, kot so npr. Dynamics 365 Finance, Dynamics 365 Supply Chain in Dynamics 365 Project Operations. Za vsako ustvarjeno kategorijo transakcij aplikacija Project Operations samodejno ustvari štiri povezane kategorije v skupni rabi: ure, stroški, provizije in postavka. Kategorije v skupni rabi lahko pregledate in prilagodite v razdelku **Vodenje projektov in računovodstvo** \> **Nastavitve** \> **Kategorije** \> **Kategorije v skupni rabi**.

## <a name="project-categories"></a>Projektne kategorije

Projektne kategorije predstavljajo najpodrobnejšo raven konfiguracije kategorij. Projektni računovodja jih mora konfigurirati posebej in za vsako posamezno podjetje.

1. Odprite razdelek **Vodenje projektov in računovodstvo** \> **Nastavitve** \> **Kategorije** \> **Kategorije projektov**.
2. Izberite **Novo**.
3. Izberite **ID kategorije** v skupni rabi, ki ste jo ustvarili v prejšnjem razdelku. Aplikacija Project Operations omogoča uporabo samo tistih kategorij v skupni rabi, ki so povezane s kategorijami transakcij.
4. Izberite skupino kategorij.

## <a name="category-groups"></a>Skupine kategorij

Skupine kategorij se uporabljajo za skupno rabo lastnosti, predvsem knjiženje profilov med sorodnimi kategorijami projekta. Za vsako vrsto transakcije mora obstajati vsaj ena skupina kategorij, vsaki kategoriji projekta pa je dodeljena skupina.

Specifikacije knjiženja v aplikaciji Project Operations so opredeljene s pravili za profil stroškov in prihodkov, kategorijami projektov in skupinami kategorij. Skupine kategorij lahko nastavite v razdelku **Vodenje projektov in računovodstvo** \> **Nastavitve** \> **Kategorije** \> **Skupine kategorij**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]