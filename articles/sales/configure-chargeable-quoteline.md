---
title: Konfiguriranje plačljivih komponent podrobnosti ponudb, ki temeljijo na projektih
description: Ta tema vsebuje informacije o vključenih, plačljivih in neplačljivih komponentah v podrobnostih ponudb, ki temeljijo na projektih.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642563"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Konfiguriranje plačljivih komponent podrobnosti ponudb, ki temeljijo na projektih

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Podrobnosti ponudbe, ki temelji na projektu, lahko imajo vključene in plačljive komponente.

Za vključene komponente je treba upoštevati način obračunavanja, razdelitev strank, omejitve, ki ne smejo biti presežene, in nastavitve pogostosti računov, določene v podrobnostih ponudbe, ki temelji na projektu.
Podmnožico vključenih komponent lahko označimo kot plačljivo, tako da uporabimo **Vrsta obračunavanja**. V okviru podrobnosti ponudbe lahko v polju **Način obračunavanja** izberete eno od naslednjih možnosti:

   - Se zaračuna
   - Se ne zaračuna

Komponente, ki se zaračunajo, je mogoče določiti za vloge in kategorije transakcij.

Plačljivost, ki je določena v vlogah za podrobnosti projektne ponudbe, velja samo za transakcijski razred **Čas**. Če imajo podrobnosti pogodbene ponudbe nastavljeno možnost **Vključi čas** = **Ne**, zavihek **Plačljive vloge** ni na voljo.

Plačljivost, ki je določena v transakcijskih kategorijah za podrobnosti projektne ponudbe, velja samo za transakcijski razred **Strošek**. Če imajo podrobnosti pogodbene ponudbe nastavljeno možnost **Vključi stroške** = **Ne**, zavihek **Plačljive kategorije** ni na voljo.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Posodabljanje vloge kot zaračunljive ali nezaračunljive
Vloga je lahko plačljiva ali neplačljiva v podrobnostih projektne ponudbe. Način obračunavanja v vlogi lahko nastavite v zavihku **Plačljive vloge** v podrobnostih ponudbe, ki temelji na projektu. To storite tako, da posodobite polje **Vrsta obračunavanja** v podmreži **Vloge, ki se zaračunajo**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Posodabljanje kategorije transakcije kot zaračunljive ali nezaračunljive
Transakcijska kategorija je lahko plačljiva ali neplačljiva v podrobnostih projektne ponudbe. Način obračunavanja v transakciji lahko nastavite v zavihku **Plačljive kategorije** v podrobnostih ponudbe, ki temelji na projektu. To storite tako, da posodobite polje **Vrsta obračunavanja** v podmreži **Kategorije, ki se zaračunajo**. 

## <a name="resolve-chargeability"></a>Razrešitev možnosti zaračunavanja

Ocena ali dejanska vrednost, ustvarjena za čas, se šteje za plačljivo le, če je čas vključen v podrobnosti ponudbe in če je vloga nastavljena kot plačljiva.
Ocena ali dejanska vrednost, ustvarjena za strošek, se šteje za plačljivo le, če je strošek vključen v podrobnosti ponudbe in če je kategorija transakcije nastavljena kot plačljiva v podrobnostih ponudbe. Spodnja tabela prikazuje, kako se plačljivost privzeto nastavi za vsako dejansko vrednost. Privzete vrednosti temeljijo na vključenih komponentah in načinu obračunavanja, ki je nastavljen v podrobnostih ponudbe.

| Čas je vključen | Strošek je vključen | Vloga | Kategoriji | Opravilo |
| --- | --- | --- | --- | --- |
| Da | Da | Se zaračuna | Se zaračuna | Obračun po dejanskem času: Se zaračuna </br>Vrsta obračuna za dejansko vrednost stroška: Se zaračuna |
| Da | Da | Se ne zaračuna | Se zaračuna | Obračun po dejanskem času: Se ne zaračuna </br>Vrsta obračuna za dejansko vrednost stroška: Se zaračuna |
| Da | Da | Se ne zaračuna | Se ne zaračuna | Obračun po dejanskem času: Se ne zaračuna </br>Vrsta obračuna za dejansko vrednost stroška: Se ne zaračuna |
| No | Da | Ni mogoče nastaviti | Se zaračuna | Obračun po dejanskem času: Ni na voljo </br>Vrsta obračuna za dejansko vrednost stroška: Se zaračuna |
| No | Da | Ni mogoče nastaviti | Se ne zaračuna | Obračun po dejanskem času: Ni na voljo </br>Vrsta obračuna za dejansko vrednost stroška: Se ne zaračuna |
| Da | No | Se zaračuna | Ni mogoče nastaviti | Obračun po dejanskem času: Se zaračuna </br>Vrsta obračuna za dejansko vrednost stroška: Ni na voljo |
| Da | No | Se ne zaračuna | Ni mogoče nastaviti | Obračun po dejanskem času: Se ne zaračuna </br> Vrsta obračuna za dejansko vrednost stroška: Ni na voljo |