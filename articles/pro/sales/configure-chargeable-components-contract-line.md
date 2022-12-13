---
title: Konfiguriranje plačljivih komponent za podrobnosti projektne pogodbe
description: Ta članek ponuja informacije o tem, kako v aplikaciji Project Operations v podrobnost pogodbe dodati komponente, ki se zaračunajo.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 33296c93964cc88499e7a98d499b99463e59d62a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825585"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Konfiguriranje plačljivih komponent za podrobnosti projektne pogodbe

_**Velja za:** poenostavljeno uvedbo – posel do izstavitve predračuna, Project Operations za primere, ki temeljijo na virih/nezalogi_

Linija projektne pogodbe ima *vključene* komponente in *plačljive* komponente.

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

Ocena ali dejansko ustvarjena vrednost za čas šteje za plačljivo le v naslednjih primerih:

   - **Čas** je vključen v podrobnosti pogodbe.
   - **Vloga** je v podrobnosti pogodbe nastavljena kot plačljiva.
   - **Vključena opravila** so v podrobnostih pogodbe nastavljena na **Izbrana opravila**.
 
 Če so te tri stvari resnične, je tudi opravilo konfigurirano tudi kot plačljivo. 

Ocena ali dejansko ustvarjena vrednost za stroške šteje za plačljivo le v naslednjih primerih:

   - **Stroški** so vključeni v podrobnosti pogodbe
   - **Kategorija transakcije** je v podrobnostih pogodbe nastavljena kot plačljiva
   - **Vključena opravila** so v podrobnostih pogodbe nastavljena na **Izbrano opravilo**
  
 Če so te tri stvari resnične, je tudi **Opravilo** konfigurirano tudi kot plačljivo. 

Ocena ali dejansko ustvarjena vrednost za material šteje za plačljivo le v naslednjih primerih:

   - **Materiali** so vključeni v podrobnosti pogodbe
   - **Vključena opravila** so v podrobnostih pogodbe nastavljena na **Izbrana opravila**

Če sta ti dve stvari resnični, je tudi **Opravilo** konfigurirano tudi kot plačljivo. 

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
Obračun po dejanskem času: <strong>Se zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanske stroške: <strong>Se zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanski material: <strong>plačljivo</strong>
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
Obračun po dejanskem času: <strong>Se zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanske stroške: <strong>Se zaračuna</strong>
                </p>
                <p>
Vrsta obračuna za dejanski material: <strong>plačljivo</strong>
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
