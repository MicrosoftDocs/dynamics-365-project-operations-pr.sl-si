---
title: Konfigurirajte plačljive komponente v vrsticah projektnih ponudb
description: Ta članek ponuja informacije o nastavitvi zaračunljivih in nezaračunljivih komponent v vrstici projektne ponudbe.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1e454278a1c5c24ac346c537c778b25448d9ea03
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825538"
---
# <a name="configure-chargeable-components-on-project-quote-lines"></a>Konfigurirajte plačljive komponente v vrsticah projektnih ponudb

_**Velja za:** poenostavljeno uvedbo – posel do izstavitve predračuna, Project Operations za primere, ki temeljijo na virih/nezalogi_

Vrstica projektne pogodbe je sestavljena iz pojmov *vključenih* komponent in komponent, *ki se zaračunajo*.

Za vključene komponente veljajo naslednji elementi:

  - Način zaračunavanja in razdelitve kupcev
  - Omejitve »Ni dovoljeno preseči« 
  - Nastavitve pogostosti izdajanja računov, ki so določene v vrstici ponudbe, ki temelji na projektu

Podmnožico vključenih komponent je v polju **Vrsta obračunavanja** mogoče označiti kot zaračunljive. Polje **Vrsta obračunavanja** predstavlja nabor možnosti, ki v okviru vrstice ponudbe omogoča naslednje vrednosti:

  - Se zaračuna
  - Se ne zaračuna

Komponente, ki se zaračunajo, je mogoče določiti za opravila, vloge in kategorije transakcij.

Možnost zaračunavanja je določena v opravilih za posamezno vrstico ponudbe in velja za vse razrede transakcij, vključene v to vrstico. Če je polje **Vključi opravila** prazno ali nastavljeno na možnost **Ves projekt**, zavihek **Opravila, ki se zaračunajo** ni na voljo.

Možnost zaračunavanja je določena v vlogah za podrobnost projektne pogodbe in velja samo za razred transakcije **Čas**. Če je v vrstici ponudbe polje **Vključi čas** prazno ali nastavljeno na možnost **Ne**, zavihek **Vloge, ki se zaračunajo** ni na voljo.

Plačljivost je določena v kategorijah transakcije za podrobnost projektne pogodbe in velja samo za razred transakcije **Strošek**. Če je v vrstici ponudbe polje **Vključi čas** prazno ali nastavljeno na možnost **Ne**, zavihek **Kategorije, ki se zaračunajo** ni na voljo.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Posodabljanje projektnega opravila kot zaračunljivega ali nezaračunljivega

Projektna naloga je lahko v posamezni vrstici ponudbe, ki temelji na projektu, zaračunljiva ali nezaračunljiva, kar omogoča naslednje nastavitve.

Če vrstica ponudbe, ki temelji na projektu, vključuje možnost **Čas** in opravilo **T1**, je opravilo povezano s ponudbo kot zaračunljivo. Če obstaja druga vrstica ponudbe, ki vključuje možnost **Stroški**, lahko opravilo **T1** v vrstici ponudbe povežete kot nezaračunljivo. Rezultat tega je, da se ves čas, zabeležen za opravilo, zaračuna, vsi zabeleženi stroški pa se ne zaračunajo.

Vrsta obračuna za opravilo je lahko konfigurirana na zavihku **Opravila, ki se zaračunajo** podrobnosti ponudbe, ki temelji na projektih, s posodobitvijo polja **Vrsta obračunavanja** v podmreži **Opravila vrstice pogodbe**. Druga možnost je, da posodobite vrsto obračunavanja za opravilo projekta v polju **Vrsta obračunavanja** v podmreži v nastavitvah obračunavanja opravil projekta, ki prikazuje podrobnosti ponudb, povezane z opravilom.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Posodabljanje vloge kot zaračunljive ali nezaračunljive

Vloga je lahko v okviru določene vrstice ponudbe, ki temelji na projektu, zaračunljiva ali nezaračunljiva.

Vrsta obračuna za vlogo je lahko konfigurirana na zavihku **Vloge, ki se zaračunajo** podrobnosti ponudbe s posodobitvijo polja **Vrsta obračunavanja** v podmreži **Vloge, ki se zaračunajo**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Posodabljanje kategorije transakcije kot zaračunljive ali nezaračunljive

V posamezni vrstici ponudbe se lahko kategorija transakcije zaračuna ali ne zaračuna.

Vrsta obračuna za transakcijo je lahko konfigurirana na zavihku **Kategorije, ki se zaračunajo** podrobnosti ponudbe s posodobitvijo polja **Vrsta obračunavanja** v podmreži **Kategorije, ki se zaračunajo**.

### <a name="resolve-chargeability"></a>Razrešitev možnosti zaračunavanja
Ocena ali dejansko ustvarjena vrednost za čas šteje za plačljivo le v naslednjih primerih:

   - **Čas** je vključen v vrstico ponudbe.
   - **Vloga** je v vrstici ponudbe nastavljena kot plačljiva.
   - **Vključena opravila** so v vrstici ponudbe nastavljena na **Izbrana opravila**. 

Če so te tri stvari resnične, je tudi **Opravilo** konfigurirano kot plačljivo. 

Ocena ali dejansko ustvarjena vrednost za stroške šteje za plačljivo le v naslednjih primerih: 

   - **Strošek** je vključen v vrstico ponudbe.
   - **Kategorija transakcije** je v vrstici ponudbe nastavljena kot plačljiva.
   - **Vključena opravila** so v vrstici ponudbe nastavljena na **Izbrana opravila**.

Če so te tri stvari resnične, je tudi **Opravilo** konfigurirano kot plačljivo. 

Ocena ali dejansko ustvarjena vrednost za material šteje za plačljivo le v naslednjih primerih:

   - **Materiali** so vključeni v vrstico ponudbe.
   - **Vključena opravila** so v vrstici ponudbe nastavljena na **Izbrana opravila**.

Če sta ti dve stvari resnični, mora biti tudi **Opravilo** konfigurirano kot plačljivo. 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Čas je vključen</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Strošek je vključen</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Vključuje materiale</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Vključena opravila</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Vloga</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategoriji</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Opravilo</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Vpliv plačljivosti</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Celoten projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="70" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="65" valign="top">
                <p>
Ni mogoče nastaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: Se zaračuna </p>
                <p>
Vrsta obračuna za dejansko vrednost stroška: Se zaračuna </p>
                <p>
Vrsta obračuna za dejanski material: plačljivo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo izbrana opravila </p>
            </td>
            <td width="65" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="70" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="65" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: Se zaračuna </p>
                <p>
Vrsta obračuna za dejansko vrednost stroška: Se zaračuna </p>
                <p>
Vrsta obračuna za dejanski material: plačljivo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo izbrana opravila </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Se ne zaračuna</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="65" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejansko vrednost stroška: Se zaračuna </p>
                <p>
Vrsta obračuna za dejanski material: plačljivo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo izbrana opravila </p>
            </td>
            <td width="65" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="70" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Se ne zaračuna</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanski material: <strong>Se ne zaračuna</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo izbrana opravila </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Se ne zaračuna</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Se ne zaračuna</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanski material: <strong>Se ne zaračuna</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Samo izbrana opravila </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Se ne zaračuna</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Se ne zaračuna</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanski material: plačljivo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Celoten projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Ni mogoče nastaviti </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Se zaračuna</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ni mogoče nastaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: <strong>Ni na voljo</strong>
                </p>
                <p>
Vrsta obračuna za dejansko vrednost stroška: Se zaračuna </p>
                <p>
Vrsta obračuna za dejanski material: plačljivo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Celoten projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Ni mogoče nastaviti </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Se ne zaračuna</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ni mogoče nastaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: <strong>Ni na voljo</strong>
                </p>
                <p>
Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanski material: plačljivo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Celoten projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="70" valign="top">
                <p>
Ni mogoče nastaviti </p>
            </td>
            <td width="65" valign="top">
                <p>
Ni mogoče nastaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: Se zaračuna </p>
                <p>
Vrsta obračuna za dejanske stroške:<strong> Ni na voljo</strong>
                </p>
                <p>
Vrsta obračuna za dejanski material: plačljivo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Da </p>
            </td>
            <td width="75" valign="top">
                <p>
Celoten projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Se ne zaračuna</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Ni mogoče nastaviti </p>
            </td>
            <td width="65" valign="top">
                <p>
Ni mogoče nastaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanske stroške:<strong> Ni na voljo</strong>
                </p>
                <p>
Vrsta obračuna za dejanski material: plačljivo </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Celoten projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="70" valign="top">
                <p>
Se zaračuna </p>
            </td>
            <td width="65" valign="top">
                <p>
Ni mogoče nastaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: Se zaračuna </p>
                <p>
Vrsta obračuna za dejansko vrednost stroška: Se zaračuna </p>
                <p>
Vrsta obračuna za dejanski material: <strong>Ni na voljo</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Da </p>
            </td>
            <td width="78" valign="top">
                <p>
Da </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Celoten projekt </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Se ne zaračuna</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Se ne zaračuna</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ni mogoče nastaviti </p>
            </td>
            <td width="350" valign="top">
                <p>
Obračun po dejanskem času: <strong>Se ne zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanske stroške: <strong>Se ne zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanski material: <strong>Ni na voljo</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
