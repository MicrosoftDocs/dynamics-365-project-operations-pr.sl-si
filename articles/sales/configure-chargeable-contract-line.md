---
title: Konfiguriranje zaračunljivih komponent podrobnosti pogodbe, ki temelji na projektu
description: Ta tema ponuja informacije o vključenih, zaračunljivih in nezaračunljivih komponentah v podrobnostih pogodbe.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d6f67d5dc6b94148d437b3399229c1235c702c6a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128721"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfiguriranje zaračunljivih komponent podrobnosti pogodbe, ki temelji na projektu

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Posamezna podrobnost pogodbe, ki temelji na projektu, je opremljena s pojmi vključenih, zaračunljivih in nezaračunljivih komponent.

Za vključene komponente veljajo način obračunavanja, razdelitev kupcev, omejitve, ki ne smejo biti presežene, in nastavitve pogostosti izdajanja računov, določene v podrobnosti pogodbe, ki temelji na projektu.

Podmnožico vključenih komponent je v polju **Vrsta obračunavanja** mogoče posodobiti kot zaračunljive.

Komponente, ki se zaračunajo, je mogoče določiti za vloge in kategorije transakcij.

Za podrobnost projektne pogodbe možnost zaračunavanja, določena v vlogi, velja samo za razred transakcije **Čas**. Če je v podrobnosti pogodbe polje **Vključi čas** nastavljeno na možnost **Ne**, zavihek **Vloge, ki se zaračunajo** ni na voljo.

Plačljivost, določena v kategorijah transakcije za podrobnost projektne pogodbe, velja samo za razred transakcije **Strošek**. Če je v podrobnosti pogodbe polje **Vključi stroške** nastavljeno na možnost **Ne**, zavihek **Kategorije, ki se zaračunajo** ni na voljo.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Posodabljanje vloge kot zaračunljive ali nezaračunljive

V posamezni podrobnosti pogodbe, ki temelji na projektu, se lahko vloga zaračuna ali ne zaračuna.

Na zavihku **Vloge, ki se zaračunajo** podrobnosti pogodbe, ki temeljijo na projektu, v podmreži **Vloge, ki se zaračunajo** v polju **Vrsta obračunavanja** posodobite vrsto obračunavanja za vlogo.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Posodabljanje kategorije transakcije kot zaračunljive ali nezaračunljive

V posamezni podrobnosti pogodbe, ki temelji na projektu, se lahko kategorija transakcije zaračuna ali ne zaračuna.

Na zavihku **Kategorije, ki se zaračunajo** podrobnosti pogodbe, ki temeljijo na projektu, v podmreži **Kategorije, ki se zaračunajo** v polju **Vrsta obračunavanja** posodobite vrsto obračunavanja za transakcijo.

### <a name="resolve-chargeability"></a>Razrešitev možnosti zaračunavanja

Ocena ali dejanska vrednost, ustvarjena za čas, se šteje za zaračunljivo le, če je v podrobnosti pogodbe vključen čas in če je v podrobnosti pogodbe vloga konfigurirana kot zaračunljiva.

Ocena ali dejanska vrednost, ustvarjena za strošek, se šteje za zaračunljivo le, če je v podrobnosti pogodbe vključena možnost Strošek in če je v podrobnosti pogodbe kategorija opravilo konfigurirana kot zaračunljiva.

| Čas je vključen | Strošek je vključen | Vloga | Kategoriji | Opravilo |
| --- | --- | --- | --- | --- |
| Da | Da | Se zaračuna | Se zaračuna | Obračun po dejanskem času: Se zaračuna </br>Vrsta obračuna za dejansko vrednost stroška: Se zaračuna |
| Da | Da | Se ne zaračuna | Se zaračuna | Obračun po dejanskem času: Se ne zaračuna </br>Vrsta obračuna za dejansko vrednost stroška: Se zaračuna |
| Da | Da | Se ne zaračuna | Se ne zaračuna | Obračun po dejanskem času: Se ne zaračuna </br>Vrsta obračuna za dejansko vrednost stroška: Se ne zaračuna |
| No | Da | Ni mogoče nastaviti | Se zaračuna | Obračun po dejanskem času: Ni na voljo </br>Vrsta obračuna za dejansko vrednost stroška: Se zaračuna |
| No | Da | Ni mogoče nastaviti | Se ne zaračuna | Obračun po dejanskem času: Ni na voljo </br>Vrsta obračuna za dejansko vrednost stroška: Se ne zaračuna |
| Da | No | Se zaračuna | Ni mogoče nastaviti | Obračun po dejanskem času: Se zaračuna </br>Vrsta obračuna za dejansko vrednost stroška: Ni na voljo |
| Da | No | Se ne zaračuna | Ni mogoče nastaviti | Obračun po dejanskem času: Se ne zaračuna </br> Vrsta obračuna za dejansko vrednost stroška: Ni na voljo |
