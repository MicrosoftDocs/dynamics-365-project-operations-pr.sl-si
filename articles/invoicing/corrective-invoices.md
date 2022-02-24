---
title: Ustvarjanje popravljalnih računov, ki temeljijo na projektih
description: Ta tema vsebuje informacije o popravljalnih računih v aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788898"
---
# <a name="create-corrective-project-based-invoices"></a>Ustvarjanje popravljalnih računov, ki temeljijo na projektih 

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Potrjeni račun projekta je mogoče popraviti v skladu s spremembami ali dobroimetjem po dogovoru s stranko in vodjo projekta.

Če želite urediti potrjeni račun, odprite potrjeni račun in izberite **Popravi ta račun**. 

> [!NOTE]
> Ta možnost je na voljo samo za potrjene račune projektov.

Iz potrjenega računa se ustvari nov osnutek računa. Vse podrobnosti vrstice računa iz predhodno potrjenega računa so kopirane v novi osnutek. Sledi nekaj ključnih točk, s katerimi boste lažje razumeli podrobnosti vrstice na novem popravljenem računu:

- Vse količine se posodobijo na nič. To predvideva, da so vsi zaračunani elementi v celoti knjiženi v dobro. Po potrebi lahko te količine ročno posodobite, tako da odražajo količino, ki se zaračuna, in ne količine, ki se knjiži v dobro. Na podlagi vnesene količine aplikacija izračuna količino dobroimetja. Ta znesek se odraža v dejanskih vrednostih, ki se ustvarijo ob potrditvi popravljenega računa. Če spreminjate znesek davka, morate vnesti pravilen znesek davka in ne zneska davka, ki se knjiži v dobro.
- Popravki mejnika so vedno obdelani kot polno dobroimetje.
- Zneske honorarja ali predujma je mogoče popraviti, če je bila stranki zaračunana napačna vrednost.
- Uskladitve honorarjev in predujmov je mogoče popraviti, če je bil uporabljen nepravilen znesek za uskladitev stroškov na predhodno potrjenem računu.

> [!IMPORTANT]
> Podrobnosti vrstice računa, ki so popravki drugih že zaračunanih stroškov, imajo polje **Popravek** nastavljeno na vrednost **Da**. Računi s popravljenimi podrobnostmi vrstice računa imajo polje **Vsebuje popravke**, ki je prav tako nastavljeno na **Da**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Dejanske vrednosti, ustvarjene ob potrditvi popravljenega računa

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
            <td width="216" rowspan="4" valign="top">
                <p>
Potrdite popravek predračuna ali honorarja.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev Ta znesek je pozitiven, saj naj bi odpravil negativno vrednost, ki je nastala ob izdaji računa za honorar ali predujem.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Dejanska vrednost stornacije zaračunane prodaje se ustvari za znesek honorarja ali predujma za stornacijo prvotno zaračunane prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost obračunane prodaje se ustvari za popravljeni znesek vrstice računa na podlagi honorarja ali predujma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Dejanska vrednost neobračunane prodaje negativnega zneska popravljene vrstice računa na podlagi honorarja ali predujma, ki se uporabi za uskladitev.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Potrditev popravka predhodno usklajenega honorarja ali predujma.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje neobračunanega honorarja ali predplačila, ki je bil ustvarjen za uskladitev Ta znesek je pozitiven in naj bi odpravil negativno vrednost, ki je nastala ob prejšnji uskladitvi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Dejanska vrednost stornirane obračunane prodaje za znesek na prejšnjem računu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova dejanska vrednost obračunane prodaje za popravljeni honorar, ki se uporabi pri popravljenem računu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Neobračunana dejanska vrednost prodaje z negativnim zneskom iz popravljenega preostanka honorarja ali predujma, ki se uporabi za uskladitev pri nadaljnjih računih.
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
Niso podprti </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
