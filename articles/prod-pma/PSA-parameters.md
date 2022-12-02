---
title: Parametri integracije rešitve Project Service Automation
description: V tem članku je pojasnjeno, kako konfigurirati način vnosa privzetih podatkov med integracijo rešitve Microsoft Dynamics 365 for Project Service Automation z rešitvijo Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a4abeb2960981196ed1d7c453e7daa0558e326ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932316"
---
# <a name="project-service-automation-integration-parameters"></a>Parametri integracije rešitve Project Service Automation

[!include[banner](../includes/banner.md)]

Na strani **Parametri integracije rešitve Project Service Automation** lahko nastavite, kako se vnašajo privzeti podatki pri integraciji rešitve Dynamics 365 Project Service Automation z rešitvijo Dynamics 365 Finance. Za uspešno sinhronizacijo projektov iz rešitve Project Service Automation v Finance morate nastaviti naslednja polja.

Če želite odpreti stran **Parametri integracije rešitve Project Service Automation**, se pomanite v razdelek **Upravljanje projekta in računovodstvo** \> **Nastavitve** \> **Parametri integracije rešitve Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - V različici 8.0 so na voljo integracija projektnih opravil, kategorije transakcije stroškov, ocene delovnih ur, ocene stroškov in zaklepanje funkcionalnosti.
> - Integracija dejanskih vrednosti je na voljo v različici 8.0.1 ali novejši.


| Tabulator                    | Polje                | Opis |
|------------------------|----------------------|-------------|
| Splošno                | Privzeta vrsta projekta | Izberite privzeto vrsto projekta. Ko se projekti sinhronizirajo iz rešitve Project Service Automation, se uporabi ta vrednost, če v integracijski predlogi niste navedli privzete vrednosti. Med sinhronizacijo je polje novih projektov **Vrsta projekta** nastavljeno na to vrednost. Vendar se lahko vrednost posodobi, ko se podrobnosti projektne pogodbe sinhronizirajo iz rešitve Project Service Automation. |
|                        | Kategorija časa        | Izberite privzeto kategorijo časa. Ta vrednost se uporablja, ko se ocene delovnih ur sinhronizirajo iz rešitve Project Service Automation. Ko se ocene delovnih ur in dejanske delovne ure sinhronizirajo iz rešitve Project Service Automation, se v rešitvi Finance polje novih napovedi delovnih ur projekta **Kategorija** nastavi na to vrednost. |
|                        | Kategorija pristojbin         | Izberite privzeto kategorijo pristojbin. Ta vrednost se uporablja, ko se dejanski podatki o pristojbinah sinhronizirajo iz rešitve Project Service Automation. Ko se dejanski podatki o pristojbinah sinhronizirajo iz rešitve Project Service Automation, se v rešitvi Finance polje novih transakcij s pristojbinami **Kategorija** nastavi na to vrednost. |
| Privzete vrednosti projektne skupine | Vrsta projekta         | Kliknite **Novo**, da dodate vrstico, v kateri lahko izberete vrsto projekta, za katero želite nastaviti privzeto projektno skupino. Določeno vrsto projekta lahko v konfiguraciji izberete le enkrat. |
|                        | Projektna skupina        | Izberite privzeto projektno skupino za izbrano vrsto projekta. Ko se novi projekti sinhronizirajo iz rešitve Project Service Automation, se polje **Projektna skupina** nastavi na privzeto vrednost za vrsto projekta, če v integracijski predlogi niste navedli privzete vrednosti. |
| Privzete vrednosti vrste obračunavanja  | Vrsta obračunavanja         | Kliknite **Novo**, da dodate vrstico, v kateri lahko izberete vrsto obračunavanja, za katero želite nastaviti privzeto lastnost vrstice. Določeno vrsto obračunavanja lahko v konfiguraciji izberete le enkrat. |
|                        | Lastnost vrstice        | Izberite privzeto lastnost vrstice za izbrano vrsto obračunavanja. Ko se nove ocene delovnih ur, nove ocene stroškov ali novi dejanski podatki sinhronizirajo iz rešitve Project Service Automation, se polje **Lastnost vrstice** nastavi na privzeto vrednost za vrsto obračunavanja. |
| Zaklepanje funkcionalnosti  | Ni na voljo.       | Izberite funkcionalnost, ki jo želite onemogočiti v rešitvi Finance, za projekte in pogodbe, ki izvirajo iz rešitve Project Service Automation. Na primer: izklopite lahko možnost urejanja pogodb in projektov, ustvarjate strukturirano členitev dela in vnesete časovne liste v rešitev Finance. Polja, povezana z računovodstvom, bodo še naprej omogočena, tudi če z nastavitvijo za parametre niso na voljo. Privzeto je omogočena vsa funkcionalnost. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]