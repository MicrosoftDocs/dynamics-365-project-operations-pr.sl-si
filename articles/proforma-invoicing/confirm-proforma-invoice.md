---
title: Potrditev predračuna
description: Ta tema vsebuje informacije o potrditvi predračuna.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287888"
---
# <a name="confirm-a-proforma-invoice"></a>Potrditev predračuna

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Po potrditvi predračuna se stanje računa projekta posodobi na **Potrjeno**. Ko je račun potrjen, postane na voljo samo za branje. V prihodnje je račun lahko popravljen le, če popravke ali dobropis zahteva stranka oz. če je račun označen kot plačan.

V spodnji tabeli so navedeni dejanski podatki, ki jih je ustvaril sistem. Ti dejanski podatki so ustvarjeni, ko se pred potrditvijo osnutka računa za projekt izvedejo določene operacije.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Scenarij</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Dejanski podatki, ustvarjeni ob potrditvi</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Izdajanje računov za časovno transakcijo brez sprememb na osnutku računa
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Dejanska vrednost obračunane prodaje za ure in znesek ob prvotni odobritvi časa
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Izdajanje računov za časovno transakcijo, ki je bila urejena za zmanjšanje količine
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za ure in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek ur in zneska na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Izdajanje računov za časovno transakcijo, ki je bila urejena za povečanje količine
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje neobračunane prodaje za ure in znesek ob prvotni odobritvi časa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za ure in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Izdajanje računov za transakcijo stroška brez sprememb na osnutku računa
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Obračunana dejanska vrednost prodaje za količino in znesek ob prvotni odobritvi stroškov
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Izdajanje računov za transakcijo stroška, ki je bila urejena za zmanjšanje količine
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek količine in zneska na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Izdajanje računov za transakcijo stroška, ki je bila urejena za povečanje količine
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje neobračunane prodaje za količino in znesek ob prvotni odobritvi stroškov
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neplačane prodaje, ki se zaračuna za količino in znesek na urejeni podrobnosti vrstice računa, storniranje neobračunane dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Izdajanje računa za dajatev
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje neobračunane prodaje za znesek dajatev v prvotni vrstici dnevnika
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Obračunana dejanska vrednost prodaje za količino in znesek v prvotni vrstici dnevnika
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Izdajanje računa za mejnik
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Obračunana dejanska vrednost prodaje za znesek mejnika iz prvotnega mejnika v podrobnosti projektne pogodbe
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]