---
title: Konfiguriranje komponent, ki se zaračunajo, za podrobnosti pogodbe, ki temelji na projektu – poenostavljena različica
description: Ta tema ponuja informacije o tem, kako v aplikaciji Project Operations v podrobnost pogodbe dodati komponente, ki se zaračunajo.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf3f2a28fc992d6444b35d6ffa0c3f6cadcf16ea
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273938"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Konfiguriranje komponent, ki se zaračunajo, za podrobnosti pogodbe, ki temelji na projektu – poenostavljena različica

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Projektna podrobnost pogodbe je sestavljena iz *vključenih* komponent in komponent, *ki se zaračunajo*.

Vključene komponente so komponente, za katere velja:

  - Način zaračunavanja in razdelitve kupcev
  - Omejitve »Ni dovoljeno preseči« 
  - Nastavitve pogostosti izdajanja računov, ki je določena v podrobnosti pogodbe, ki temelji na projektu

Podmnožico vključenih komponent je v polju **Vrsta obračunavanja** mogoče označiti kot zaračunljive. Polje **Vrsta obračunavanja** predstavlja nabor možnosti, ki v okviru podrobnosti pogodbe omogoča naslednje vrednosti:

  - Se zaračuna
  - Se ne zaračuna

Komponente, ki se zaračunajo, je mogoče določiti za opravila, vloge in kategorije transakcij.

Zaračunavanje je določeno v opravilih za posamezno podrobnost pogodbe in velja za vse razrede transakcij, vključene v podrobnost. Če je v podrobnosti pogodbe polje **Vključi opravila** prazno ali nastavljeno na možnost **Ves projekt**, zavihek **Opravila, ki se zaračunajo** ni na voljo.

Zaračunavanje, določeno v vlogah za podrobnost projektne pogodbe, velja samo za razred transakcije **Čas**. Če je v podrobnosti pogodbe polje **Vključi čas** prazno ali nastavljeno na možnost **Ne**, zavihek **Vloge, ki se zaračunajo** ni na voljo.

Plačljivost, določena v kategorijah transakcije za podrobnost projektne pogodbe, velja samo za razred transakcije **Strošek**. Če je polje **Vključi stroške** prazno ali nastavljeno na možnost **Ne**, zavihek **Kategorije, ki se zaračunajo** ni na voljo.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Posodobite projektno opravilo kot zaračunljivo ali nezaračunljivo

Projektna naloga se lahko v posamezni podrobnosti pogodbe zaračuna ali ne zaračuna, kar omogoča naslednje nastavitve:

Če podrobnost pogodbe, ki temelji na projektu, vključuje možnost **Čas** in določeno opravilo, se možnost **T1** z njo poveže kot zaračunljiva. Če obstaja druga podrobnost pogodbe, ki vključuje možnost **Stroški**, lahko opravilo T1 v podrobnosti pogodbe povežete kot nezaračunljivo. Rezultat tega je, da se ves čas, zabeležen za opravilo, zaračuna, vsi stroški pa se ne zaračunajo.

Vrsta obračuna za opravilo je lahko konfigurirana na zavihku **Opravila, ki se zaračunajo** podrobnosti pogodbe s posodobitvijo polja **Vrsta obračunavanja** v podmreži opravil vrstice pogodbe. Druga možnost je, da posodobite polje **Vrsta obračunavanja** v podmreži nastavitve obračunavanja opravil projekta, ki prikazuje podrobnosti pogodbe, povezane z opravilom.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Posodabljanje vloge kot zaračunljive ali nezaračunljive

V posamezni podrobnosti pogodbe je lahko vloga zaračunljiva ali nezaračunljiva.

Način obračunavanja vloge je mogoče nastaviti na zavihku **Vloge, ki se zaračunajo** v podrobnosti pogodbe. To storite tako, da posodobite polje **Vrsta obračunavanja** v podmreži **Vloge, ki se zaračunajo**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Posodabljanje kategorije transakcije kot zaračunljive ali nezaračunljive

V posamezni podrobnosti pogodbe je lahko kategorija transakcije zaračunljiva ali nezaračunljiva.

Način obračunavanja transakcije je mogoče nastaviti na zavihku **Kategorije, ki se zaračunajo** v podrobnosti pogodbe. To storite tako, da posodobite polje **Vrsta obračunavanja** v podmreži **Kategorije, ki se zaračunajo**.

### <a name="resolve-chargeability"></a>Razrešitev možnosti zaračunavanja

Ocena ali dejanska vrednost, ustvarjena za čas, se šteje za zaračunljivo le, če je v podrobnosti pogodbe vključen **Čas** ter če sta v podrobnosti pogodbe **Opravilo** in **Vloga** konfigurirana kot zaračunljiva.

Ocena ali dejanska vrednost, ustvarjena za strošek, se šteje za zaračunljivo le, če je v podrobnosti pogodbe vključena možnost **Strošek** ter če sta v podrobnosti pogodbe kategoriji **Opravilo** in **Transakcija** konfigurirani kot zaračunljivi.


| Čas je vključen | Strošek je vključen | Vključena so opravila | Vloga           | Kategoriji       | Opravilo                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Da           | Da              | Ves projekt | Se zaračuna     | Se zaračuna     | Obračun po dejanskem času: **Se zaračuna** </br> Vrsta obračuna za dejansko vrednost stroška: **Se zaračuna**           |
| Da           | Da              | Izbrana opravila | Se zaračuna     | Se zaračuna     | Obračun po dejanskem času: **Se zaračuna** </br> Vrsta obračuna za dejansko vrednost stroška: **Se zaračuna**           |
| Da           | Da              | Izbrana opravila | Se ne zaračuna | Se zaračuna     | Obračun po dejanskem času: **Se ne zaračuna** </br> Vrsta obračuna za dejansko vrednost stroška: **Se zaračuna**       |
| Da           | Da              | Izbrana opravila | Se zaračuna     | Se zaračuna     | Obračun po dejanskem času: **Se ne zaračuna** </br> Vrsta obračuna za dejansko vrednost stroška:   **Se ne zaračuna** |
| Da           | Da              | Izbrana opravila | Se ne zaračuna | Se zaračuna     | Obračun po dejanskem času: **Se ne zaračuna** </br> Vrsta obračuna za dejansko vrednost stroška:   **Se ne zaračuna** |
| Da           | Da              | Izbrana opravila | Se ne zaračuna | Se ne zaračuna | Obračun po dejanskem času: **Se ne zaračuna** </br> Vrsta obračuna za dejansko vrednost stroška:   **Se ne zaračuna** |
| No            | Da              | Ves projekt | Ni mogoče nastaviti   | Se zaračuna     | Obračun po dejanskem času: **Ni na voljo**</br>Vrsta obračuna za dejansko vrednost stroška: **Se zaračuna**          |
| No            | Da              | Ves projekt | Ni mogoče nastaviti   | Se ne zaračuna | Obračun po dejanskem času: **Ni na voljo**</br> Vrsta obračuna za dejansko vrednost stroška: **Se ne zaračuna**     |
| Da           | No               | Ves projekt | Se zaračuna     | Ni mogoče nastaviti   | Obračun po dejanskem času: **Se zaračuna** </br> Vrsta obračuna za dejansko vrednost stroška: **Ni na voljo**        |
| Da           | No               | Ves projekt | Se ne zaračuna | Ni mogoče nastaviti   | Obračun po dejanskem času: **Se ne zaračuna** </br>Vrsta obračuna za dejansko vrednost stroška: **Ni na voljo**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]