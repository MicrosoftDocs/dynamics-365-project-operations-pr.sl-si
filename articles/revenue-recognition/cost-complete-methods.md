---
title: Metode za izračun stroškov za dokončanje
description: Ta tema vsebuje informacije o metodah, uporabljenih za izračun stroškov za dokončanje projekta.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531556"
---
# <a name="cost-to-complete-methods"></a>Metode za izračun stroškov za dokončanje

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Ta tema vsebuje informacije o metodah, uporabljenih za izračun stroškov za dokončanje projekta. Obstaja več metod, s katerimi lahko izračunate stroške za dokončanje projekta. 

Ko ustvarite oceno za projekt, lahko na strani **Ustvari oceno** v polju **Metoda za izračun stroškov za dokončanje** izberete eno od naslednjih metod za izračun stroškov za dokončanje.

| Metoda za izračun stroškov za dokončanje    | Opis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Skupni strošek – dejanski            | Predvidene stroške vnesite ročno v polje **Skupni stroški** ali **Skupna količina** z gumbom **Ocena stroškov** na strani **Ocena**. Sistem odšteje dejanske stroške od vsote, ki ste jo vnesli. Skupni znesek označuje strošek za dokončanje projekta. Ta metoda ne uporablja ocen stroškov in dodelitev virov, vnesenih v aplikacijo Project Operations znotraj Microsoft Dataverse. Skupni strošek ali skupno količino lahko ročno posodobite po potrebi.  |
| Predvideni dejanski skupni stroški        | Za določitev predvidenega skupnega zneska projekta se uporabljajo dodelitve virov in ocene stroškov. Dejanski stroški se primerjajo s to napovedjo za izračun stroškov za dokončanje.                                                                                                                                                                                                                                                                          |
| Kot pri prejšnji oceni         | Pri tem se uporabljajo enake metode ocenjevanja kot v prejšnjem obdobju. Za to metodo je potreben model napovedi, če je bil potreben tudi v predhodnem obdobju.                                                                                                                                                                                                                                                                                                                           |
| Nastavite strošek za dokončanje na nič | Ta metoda se običajno uporablja pred izločitvijo ocenjevanega projekta, kjer ta metoda primerja skupno vrednost ocene s knjiženimi dejanskimi transakcijami in počisti stolpec **Stroški za dokončanje**. Ob koncu je rezultat vedno 100-odstoten. Za vsako vrstico cene, ki jo ustvarite, se potrditveno polje **Napoved** počisti in skupna ocena prekopira iz prejšnje ocene stroškov. Dejanska poraba za ocenjeno obdobje se odšteje od stroška za dokončanje projekta.              |
| Iz predloge stroškov           | Metoda za izračun stroškov za dokončanje, ki je nastavljena v predlogi stroškov, povezani z izbranim projektom ocenjevanja.                                                                                                                                                                                                                                                                                                                                                                          |