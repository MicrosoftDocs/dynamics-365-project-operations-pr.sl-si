---
title: Konfiguracija komponent v vrstici ponudbe, ki se zaračunajo
description: Ta tema ponuja informacije o nastavitvi zaračunljivih in nezaračunljivih komponent v vrstici projektne ponudbe.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084877"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Konfiguracija komponent v vrstici ponudbe, ki se zaračunajo

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Vrstica projektne pogodbe je sestavljena iz pojmov *vključenih* komponent in komponent, *ki se zaračunajo*.

Za vključene komponente veljajo naslednji elementi:

  - Način zaračunavanja in razdelitve kupcev
  - Omejitve »Ni dovoljeno preseči« 
  - Nastavitve pogostosti izdajanja računov, ki so določene v vrstici ponudbe, ki temelji na projektu

Podmnožico vključenih komponent je v polju **Vrsta obračunavanja** mogoče označiti kot zaračunljive. Polje **Vrsta obračunavanja** predstavlja nabor možnosti, ki v okviru vrstice ponudbe omogoča naslednje vrednosti:

  - Se zaračuna
  - Se ne zaračuna

Komponente, ki se zaračunajo, je mogoče določiti za opravila, vloge in kategorije transakcij.

Možnost zaračunavanja je določena v opravilih za posamezno vrstico ponudbe in velja za vse razrede transakcij, vključene v to vrstico. Če je polje **Vključi opravila** prazno ali nastavljeno na možnost **Ves projekt** , zavihek **Opravila, ki se zaračunajo** ni na voljo.

Možnost zaračunavanja je določena v vlogah za podrobnost projektne pogodbe in velja samo za razred transakcije **Čas**. Če je v vrstici ponudbe polje **Vključi čas** prazno ali nastavljeno na možnost **Ne** , zavihek **Vloge, ki se zaračunajo** ni na voljo.

Plačljivost je določena v kategorijah transakcije za podrobnost projektne pogodbe in velja samo za razred transakcije **Strošek**. Če je v vrstici ponudbe polje **Vključi čas** prazno ali nastavljeno na možnost **Ne** , zavihek **Kategorije, ki se zaračunajo** ni na voljo.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Posodabljanje projektnega opravila kot zaračunljivega ali nezaračunljivega

Projektna naloga je lahko v posamezni vrstici ponudbe, ki temelji na projektu, zaračunljiva ali nezaračunljiva, kar omogoča naslednje nastavitve:

Če vrstica ponudbe, ki temelji na projektu, vključuje možnost **Čas** in opravilo **T1** , je opravilo povezano s ponudbo kot zaračunljivo. Če obstaja druga vrstica ponudbe, ki vključuje možnost **Stroški** , lahko opravilo **T1** v vrstici ponudbe povežete kot nezaračunljivo. Rezultat tega je, da se ves čas, zabeležen za opravilo, zaračuna, vsi zabeleženi stroški pa se ne zaračunajo.

Vrsto obračunavanja opravila lahko konfigurirate v vrstici ponudbe na zavihku **Opravila, ki se zaračunajo** tako, da v podmreži za **opravilo v vrstici ponudbe** posodobite polje **Vrsta obračunavanja**. V nastavitvah projekta za obračunavanje na podmreži opravila lahko tudi posodobite polje **Vrsta obračunavanja** , ki prikazuje vrstice ponudbe, povezane z opravilom.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Posodabljanje vloge kot zaračunljive ali nezaračunljive

Vloga je lahko v okviru določene vrstice ponudbe, ki temelji na projektu, zaračunljiva ali nezaračunljiva.

Vrsto obračunavanja vloge lahko konfigurirate v vrstici ponudbe na zavihku **Vloge, ki se zaračunajo** tako, da v podmreži za **opravilo v vrstici ponudbe** posodobite polje **Vrsta obračunavanja**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Posodabljanje kategorije transakcije kot zaračunljive ali nezaračunljive

V posamezni vrstici ponudbe se lahko kategorija transakcije zaračuna ali ne zaračuna.

Vrsto obračunavanja transakcije lahko konfigurirate v vrstici ponudbe na zavihku **Kategorije, ki se zaračunajo** tako, da v podmreži za **Kategorije, ki se zaračunajo** posodobite polje **Vrsta obračunavanja**.

### <a name="resolve-chargeability"></a>Razrešitev možnosti zaračunavanja
Ocena ali dejanska vrednost, ustvarjena za čas, se šteje za zaračunljivo le, če je v vrstici ponudbe vključen **Čas** ter če sta v vrstici ponudbe možnosti **Opravilo** in **Vloga** konfigurirani kot zaračunljivi.

Ocena ali dejanska vrednost, ustvarjena za strošek, se šteje za zaračunljivo le, če je v vrstici ponudbe vključena možnost **Strošek** ter če sta v vrstici ponudbe možnosti **Opravilo** in **Kategorija transakcije** konfigurirani kot zaračunljivi.

| Čas je vključen | Strošek je vključen | Vključena opravila | Vloga | Kategoriji | Opravilo | Obračunavanje |
| --- | --- | --- | --- | --- | --- | --- |
| Da | Da | Ves projekt | Se zaračuna | Se zaračuna | Ni mogoče nastaviti | Obračun po dejanskem času: Se zaračuna </br>Vrsta obračuna za dejansko vrednost stroška: Se zaračuna |
| Da | Da | Samo izbrana opravila | Se zaračuna | Se zaračuna | Se zaračuna | Obračun po dejanskem času: Se zaračuna</br>Vrsta obračuna za dejansko vrednost stroška: Se zaračuna |
| Da | Da | Samo izbrana opravila | Se ne zaračuna | Se zaračuna | Se zaračuna | Obračun po dejanskem času: Se ne zaračuna</br>Vrsta obračuna za dejansko vrednost stroška: Se zaračuna |
| Da | Da | Samo izbrana opravila | Se zaračuna | Se zaračuna | Se ne zaračuna | Obračun po dejanskem času: Se ne zaračuna</br> Vrsta obračuna za dejansko vrednost stroška: Se ne zaračuna |
| Da | Da | Samo izbrana opravila | Se ne zaračuna | Se zaračuna | Se ne zaračuna | Obračun po dejanskem času: Se ne zaračuna</br> Vrsta obračuna za dejansko vrednost stroška: Se ne zaračuna |
| Da | Da | Samo izbrana opravila | Se ne zaračuna | Se ne zaračuna | Se zaračuna | Obračun po dejanskem času: Se ne zaračuna</br> Vrsta obračuna za dejansko vrednost stroška: Se ne zaračuna |
| No | Da | Ves projekt | Ni mogoče nastaviti | Se zaračuna | Ni mogoče nastaviti | Obračun po dejanskem času: Ni na voljo </br>Vrsta obračuna za dejansko vrednost stroška: Se zaračuna |
| No | Da | Ves projekt | Ni mogoče nastaviti | Se ne zaračuna | Ni mogoče nastaviti | Obračun po dejanskem času: Ni na voljo </br>Vrsta obračuna za dejansko vrednost stroška: Se ne zaračuna |
| Da | No | Ves projekt | Se zaračuna | Ni mogoče nastaviti | Ni mogoče nastaviti | Obračun po dejanskem času: Se zaračuna</br>Vrsta obračuna za dejansko vrednost stroška: Ni na voljo |
| Da | No | Ves projekt | Se ne zaračuna | Ni mogoče nastaviti | Ni mogoče nastaviti | Obračun po dejanskem času: Se ne zaračuna </br>Vrsta obračuna za dejansko vrednost stroška: Ni na voljo |
