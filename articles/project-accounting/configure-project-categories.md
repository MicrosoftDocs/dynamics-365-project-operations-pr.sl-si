---
title: Konfiguracija kategorij projekta
description: Ta tema vsebuje informacije o nastavitvah kategorij projekta.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 94b66feef4164f3cd52d5fe917071647f731b047
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591562"
---
# <a name="configure-project-categories"></a>Konfiguracija kategorij projekta

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Aplikacija Project Operations ponuja zanesljive zmogljivosti za kategorizacijo prihodkov in odhodkov za posamezni projekt. Kategorije omogočajo poročanje in analizo projektnih transakcij ter vodenje knjiženja v glavni knjigi.

Naslednji diagram prikazuje korelacijo med kategorijami transakcij, skupnimi kategorijami in kategorijami projektov. 

Kategorije transakcij so osnovna skupina za projektne transakcije. Znotraj te skupine obstaja nabor skupnih kategorij, ki jih je mogoče deliti med aplikacijami in moduli. Še bolj podrobno, kategorije projekta so najbolj natančna raven kategorij. Kategorije projektov so lastne posamezni pravni osebi, modulu in aplikaciji.

![Korelacija med kategorijami transakcij, kategorijami v skupni rabi in kategorijami projektov.](media/project-categories.png)

## <a name="transaction-categories"></a>Kategorije transakcij

Kategorije transakcij predstavljajo osnovno razvrščanje projektnih transakcij in niso določene glede na podjetje ali vrsto transakcije. Družba Contoso Robotics na primer za razvrščanje projektnih transakcij uporablja kategorije načrtovanja, potovanja, namestitve in storitvenih transakcij.

Kategorije transakcij so definirane v modulu Project Operations. 
1. Obrazec lahko odprete v razdelku **Nastavitve** \> **Kategorije transakcij**. 
2. Ustvarite novo kategorijo transakcij bodisi z izbiro možnosti **Novo** ali pa z izbiro možnosti **Uvoz iz Excela**.

## <a name="shared-categories"></a>Kategorije v skupni rabi

Dynamics 365 uporablja koncept skupnih kategorij za kategorizacijo stroškov v različnih aplikacijah, kot so Dynamics 365 Finance, Dynamics 365 Supply Chain in Dynamics 365 Project Operations. Za vsako ustvarjeno kategorijo transakcij aplikacija Project Operations samodejno ustvari štiri povezane kategorije v skupni rabi: ure, stroški, provizije in postavka. Kategorije v skupni rabi lahko pregledate in prilagodite v razdelku **Vodenje projektov in računovodstvo** \> **Nastavitve** \> **Kategorije** \> **Kategorije v skupni rabi**.

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