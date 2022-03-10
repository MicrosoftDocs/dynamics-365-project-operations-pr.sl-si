---
title: Popravljalni računi, ki temeljijo na projektih
description: Ta tema vsebuje informacije o tem, kako v aplikaciji Project Operations ustvariti in potrditi popravljalne račune, ki temeljijo na projektu.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aaa61c8473da0aab369bbb25acb10e9a3661379997737acbcc0b3d4ab33e0ce9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997176"
---
# <a name="corrective-project-based-invoices"></a>Popravljalni računi, ki temeljijo na projektih

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Potrjeni račun projekta je mogoče popraviti v skladu s spremembami ali dobroimetjem po dogovoru s stranko in vodjo projekta.

Če želite urediti potrjeni račun, odprite potrjeni račun in izberite **Popravi ta račun**. 

> [!NOTE]
> Ta izbira ni na voljo, razen če je račun za projekt potrjen ali če račun, ki temelji na projektu, vsebuje predujme, honorarje ali usklajevanja predujmov ali honorarjev.

Iz potrjenega računa se ustvari nov osnutek računa. Vse podrobnosti vrstice računa iz predhodno potrjenega računa so kopirane v novi osnutek. Spodaj so naštete nekatere ključne točke, ki jih je treba razumeti glede podrobnosti vrstice na novem popravljenem računu:

- Vse količine se posodobijo na nič. Dynamics 365 Project Operations predvideva, da so vsi zaračunani elementi v celoti knjiženi v dobro. Po potrebi lahko te količine ročno posodobite, tako da odražajo količino, ki se zaračuna, in ne količine, ki se knjiži v dobro. Na podlagi vnesene količine aplikacija izračuna količino dobroimetja. Ta znesek se odraža v dejanskih vrednostih, ki se ustvarijo ob potrditvi popravljenega računa. Če spreminjate znesek davka, morate vnesti pravilen znesek davka in ne zneska davka, ki se knjiži v dobro.
- Popravki mejnika so vedno obdelani kot polno dobroimetje.


> [!IMPORTANT]
> Podrobnosti vrstice računa, ki so popravki drugih že zaračunanih stroškov, imajo polje **Popravek** nastavljeno na vrednost **Da**. Računi s popravljenimi podrobnostmi vrstice računa imajo polje **Vsebuje popravke** nastavljeno na vrednost **Da**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Dejanske vrednosti, ustvarjene ob potrditvi popravljenega računa

V naslednji tabeli so navedene dejanske vrednosti, ki se ustvarijo, ko je popravljalni račun potrjen.

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
Izdajanje računov za celotno dobroimetje predhodno zaračunane časovne transakcije.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Stornacija obračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za čas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za čas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Izdajanje računov za delno dobroimetje pri časovni transakciji.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Stornacija obračunane prodaje za ure in znesek, zaračunan na prvotni vrstici računa za čas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za ure in znesek na urejeni podrobnosti vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za preostale ure in zneske po odštetju popravljenih številk na podrobnostih vrstice računa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Izdajanje računov za celotno dobroimetje predhodno zaračunane transakcije stroška.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Stornacija obračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za strošek.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za strošek.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Izdajanje računov za delno dobroimetje predhodno zaračunane transakcije stroška.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Stornacija obračunane prodaje za količino in znesek, zaračunan na prvotnih podrobnostih vrstice računa za strošek.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za količino in znesek na popravljenih podrobnostih vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za preostalo količino in zneske po odštetju popravljenih številk na podrobnostih vrstice računa.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Izdajanje računov predhodno zaračunanih materialnih transakcij v celoti v dobro.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje obračunane prodaje za količino in znesek v izvirnih podrobnostih vrstice računa za material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova neobračunana dejanska prodaja za količino in znesek v izvirnih podrobnostih vrstice računa za material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Račun za delno dobroimetje pri materialni transakciji.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje obračunane prodaje za količino in znesek, zaračunan v izvirnih podrobnostih vrstice računa za material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova neobračunana dejanska prodaja, ki se zaračuna za količino in znesek v podrobnostih vrstice računa, storno in vrednost obračuna dejanske prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje, ki se zaračuna za preostalo količino in zneske po odštetju popravljenih številk na podrobnostih vrstice računa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Izdajanje računov za celotno dobroimetje predhodno zaračunane transakcije dajatve.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Stornacija obračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za dajatev.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje za količino in znesek na prvotnih podrobnostih vrstice računa za dajatev.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Izdajanje računov za delno dobroimetje predhodno zaračunane transakcije dajatve.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Stornacija obračunane prodaje za količino in znesek, zaračunan na prvotnih podrobnostih vrstice računa za dajatev.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost neobračunane prodaje, ki je zaračunljiva za količino in znesek na urejenih in popravljenih podrobnostih vrstice računa, storniranje te vrednosti in enakovredna obračunana dejanska vrednost prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Izdajanje računov za celotno dobroimetje predhodno zaračunanega mejnika.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Stornacija obračunane prodaje za ure in znesek na prvotnih podrobnostih vrstice računa za mejnik.
                </p>
                <p>
Stanje računa na mejniku se posodablja od <b>Račun stranke je objavljen</b> do <b>Pripravljeno za račun</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Izdajanje računov za delno dobroimetje predhodno zaračunanega mejnika.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Ta scenarij ni podprt.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
