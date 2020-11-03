---
title: Potrditev predračuna
description: Ta tema vsebuje informacije o potrjevanju predračunov v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b67ee6848efdcb85cf732c1eaa3e40cdc51a2e2
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084664"
---
# <a name="confirming-a-proforma-invoice"></a>Potrditev predračuna

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_


Po potrditvi predračuna se stanje računa projekta posodobi na **Potrjeno**. Ko je račun potrjen, postane na voljo samo za branje. V prihodnje se račun lahko popravi le, če popravke ali dobropis zahteva stranka oz. če je račun označen kot plačan.

V spodnji tabeli so navedeni dejanski podatki, ki jih je ustvaril sistem. Ti dejanski podatki so ustvarjeni, ko se pred potrditvijo osnutka računa za projekt izvedejo določene operacije.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenarij</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Dejanski podatki, ustvarjeni ob potrditvi</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Račun za predujem ali honorar </p>
            </td>
            <td width="408" valign="top">
                <p>
Dejanska vrednost obračunane prodaje vrste <strong>Honorar</strong> je ustvarjena za znesek predplačila ali honorarja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Neobračunana dejanska vrednost prodaje negativnega zneska honorarja ali predplačila, ki se uporabi za uskladitev.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Po popolni uskladitvi honorarja ali predplačila na računu
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev Ta znesek je pozitiven, saj naj bi odpravil negativno vrednost, ki je nastala ob izdaji računa za honorar ali predplačilo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Dejanska vrednost obračunane prodaje za znesek na tem računu
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Po delni uskladitvi honorarja ali predplačila na računu
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev Ta znesek je pozitiven, saj naj bi odpravil negativno vrednost, ki je nastala ob izdaji računa za honorar ali predplačilo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Dejanska vrednost obračunane prodaje za znesek na tem računu
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Neobračunana negativna dejanska vrednost prodaje preostanka zneska honorarja ali predplačila, ki se uporabi za usklajevanje prihodnjih računov.
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
Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za ure in znesek na urejeni podrobnosti vrstice računa, storniranje dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje, ki po odštetju popravljenih vrednosti ni zaračunljiva za preostanek ur in zneska na urejeni podrobnosti vrstice računa, storniranje dejanske vrednosti prodaje in enakovredna obračunana dejanska vrednost prodaje
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
Obračunana dejanska vrednost prodaje za količino in znesek ob prvotni odobritvi stroškov </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Izdajanje računa za podrobnost pogodbe, ki temelji na izdelku
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Dejanska vrednost obračunane prodaje za linijo izdelkov s količino in zneskom iz podrobnosti pogodbe, ki temelji na izdelku
                </p>
            </td>
        </tr>
    </tbody>
</table>
