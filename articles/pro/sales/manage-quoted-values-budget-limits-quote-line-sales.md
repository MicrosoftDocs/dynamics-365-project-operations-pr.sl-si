---
title: Podrobnosti ponudb, ki temeljijo na projektih (Pro)
description: Ta tema vsebuje informacije o uporabi podrobnosti ponudb, ki temeljijo na projektih, za projektno delo. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084686"
---
# <a name="project-based-quote-lines-pro"></a>Podrobnosti ponudb, ki temeljijo na projektih (Pro)

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Podrobnosti ponudb, ki temeljijo na projektu, so oblikovane tako, da pripomorejo k oceni projektnega dela v okviru interakcije. Struktura podrobnosti ponudb, ki temelji na projektu, je razširjena za ocene projektov z naslednjimi koncepti:

- Način obračunavanja
- Preslikavanje projektov in opravil
- Vključuje razrede transakcij
- Omejitev »Ni dovoljeno preseči«
- Nastavitev možnosti zaračunavanja
- Ocena z uporabo podrobnosti ponudb
- Stranke podrobnosti ponudbe

Naslednja tabela vsebuje informacije o poljih na zavihku **Splošno** pri podrobnosti ponudbe, ki temelji na projektu. Ta polja pomagajo nastaviti osnovo za podrobno, temeljito oceno projektnega dela.

| **Polje** | **Ustreznost, namen in smernice** | **Nadaljnji vpliv** |
| --- | --- | --- |
| Imenu | Ime podrobnosti ponudbe, ki bi vam pomagala prepoznati ločeno komponento ponudbe, ki jo ocenjujete. | Kopirano v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Način obračunavanja | V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja v vrstici priložnosti. To polje vključuje dva glavna pogodbena modela, ki ju podpira Dynamics 365 Project Operations:</br>- fiksna cena</br>- čas in material| Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Project | S tem izbirnim poljem določite projekt, ki se bo uporabljal za izvedbo dela za to interakcijo. Ko je projekt preslikan v podrobnost ponudbe, pripomore k nastavitvi opravil, ki se zaračunajo, in tudi k pripravi ocene, ki temelji na projektu, pri vrstici ponudbe v obliki podrobnosti vrstice ponudbe. Če projekt ni preslikan na vrstico ponudbe, ki temelji na projektu, morate oceno ustvariti ročno z izdelavo vsake podrobnosti vrstice ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena.|
| Vključena opravila | Označuje, ali se ta podrobnost ponudbe uporablja za vsa ali nekatera projektna opravila za izbrani projekt. To polje ima lahko naslednje vrednosti:</br>- vsa opravila projekta</br>- samo izbrana opravila projekta</br>Prazna vrednost v tem polju je enaka možnosti **Vsa projektna opravila**. | Ko je izbrana možnost **Samo izbrana opravila projekta** , lahko na strani projekta na zavihku **Nastavitev obračunavanja opravil** izberete povezavo posameznih opravil s to podrobnostjo ponudbe. Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Vključi čas | Zastava **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe. Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v oceno v tej vrstici ponudbe. Vrednost **Da** označuje, da bodo časovne transakcije ali stroški dela vključeni v oceno v tej vrstici ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Vključi strošek | Zastava **Da**/**Ne** označuje, ali bodo stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe. Vrednost **Ne** označuje, da strošek ne bo vključen v oceno v tej vrstici ponudbe. Vrednost **Ne** označuje, da bo strošek vključen v oceno v tej vrstici ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Vključi dajatev | Zastava **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključene v oceno v tej vrstici ponudbe. Vrednost **Ne** označuje, da dajatve ne bodo vključene v oceno v tej vrstici ponudbe. Vrednost **Da** označuje, da bodo dajatve vključene v oceno v tej vrstici ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Znesek ponudbe | To je znesek, ki bo stranki podan v ponudbi za vso delo, napovedano v tej podrobnosti ponudbe, ki temelji na projektu. V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz polja **Proračun stranke** v vrstici priložnosti. Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska v podrobnostih vrstice ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Predvideni davek | To je polje, ki ga je mogoče urejati in v katerem lahko uporabnik doda predviden znesek davka v vrstico ponudbe. Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska davka v podrobnostih vrstice ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Znesek ponudbe po obdavčitvi | To polje je znesek v podrobnosti ponudbe po obdavčitvi in je samo za branje. Znesek v tem polju se izračuna kot *znesek ponudbe + davek*. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Omejitev »Ni dovoljeno preseči« | To polje je mogoče urejati in je na voljo samo v podrobnostih ponudb, ki temeljijo na projektih in imajo način obračunavanja **Čas in material**. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Proračun stranke | To polje je mogoče urejati in se kopira iz ustreznega polja v vrstici priložnosti, če je bila ponudba ustvarjena iz priložnosti. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Pravila za preverjanje veljavnosti polj na zavihku Splošno v podrobnostih ponudb, ki temeljijo na projektih

**1. pravilo** : če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta** , je projekt vključen v podrobnost ponudbe.

**2. pravilo** : če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta** , je projekt in izbran razred transakcije mogoče vključiti samo v eno podrobnost ponudbe, ki temelji na projektu.

**3. pravilo** : če je polje **Vključena opravila** nastavljeno na **Samo izbrana opravila projekta** , je projekt in izbran razred transakcije mogoče vključiti v več podrobnosti ponudbe, ki temeljijo na projektu.

**4. pravilo** : če ima priložnost več ponudb, so lahko podrobnosti ponudbe za različne ponudbe, ki se vse sklicujejo na isti projekt in vključujejo isti razred transakcije.

**5. pravilo** : če ponudbe ne pripadajo isti priložnosti, ne morejo vključevati istega projekta in razreda transakcije.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Priložnost</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Ponudba</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Podrobnost ponudbe</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Projekt</strong>
                </p>
            </td>
            <td width="90" valign="top">
                <p>
                    <strong>Vključena opravila</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Vključi čas</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Vključi strošek</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Vključi</strong>
                </p>
                <p>
                    <strong>Dajatev</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Veljavno/neveljavno</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Razlog</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Neveljavno </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kršitev 2. pravila. Čas, stroški in dajatve za projekt Proj1 so vključeni v podrobnosti ponudbe PodrPon1 in PodrPon2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Neveljavno </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kršitev 2. pravila. Čas in dajatve za projekt Proj1 so vključeni v podrobnosti ponudbe PodrPon1 in PodrPon2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Veljavno </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
Čas in dajatve za projekt Proj1 so vključeni v PodrPon1.
Stroški za projekt P1 so vključeni v PodrPon2.
Ni prekrivanja glede tega, kar je vključeno v vsako podrobnost ponudbe in je veljavno.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Samo izbrana opravila </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Neveljavno </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kršitev zgornjega 2. pravila </p>
                <p>
Pon1 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.
                </p>
                <p>
PodrPon2 vključuje čas, stroške in dajatve za celoten projekt P1 ter se prekriva s tistim, kar je vključeno v Pon1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Samo izbrana opravila </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Veljavno </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
V skladu z zgornjim 3. pravilom </p>
                <p>
Pon1 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.
                </p>
                <p>
Pon2 vključuje čas, stroške in dajatve za podmnožico opravil v projektu Proj1.
                </p>
                <p>
Edino dodatno preverjanje velja okoli podmnožice opravil v PodrPon1, ki se razlikujejo od podmnožice nalog v PodrPon2. To zagotavlja, da ne bo prekrivanja. To opravi sistem, ko so opravila povezana.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Samo izbrana opravila </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Vsa opravila projekta ali prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="54" valign="top">
                <p>
Veljavno </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Glede na 5. pravilo sta Pon1 in Pon2 dve ponudbi za isto priložnost, tako da lahko oba ocenjujeta enake komponente projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon2 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Vsa opravila projekta ali prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Vsa opravila projekta ali prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="54" valign="top">
                <p>
Veljavno </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Glede na 4. pravilo sta Pon1 in Pon2 dve ponudbi za različni priložnosti, tako da ne moreta obe ocenjevati enakih komponent istega projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
Pril2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Pon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Vsa opravila projekta ali prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="54" valign="top">
                <p>
Neveljavno </p>
            </td>
        </tr>
    </tbody>
</table>

