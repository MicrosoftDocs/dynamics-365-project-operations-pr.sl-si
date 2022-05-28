---
title: Pregled podrobnosti ponudb, ki temeljijo na projektih
description: Ta tema vsebuje informacije o uporabi podrobnosti ponudb, ki temeljijo na projektih, za projektno delo.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a9661d9b91ffeece4c66b129846632b30ebebc8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591102"
---
# <a name="project-based-quote-lines-overview"></a>Pregled podrobnosti ponudb, ki temeljijo na projektih 

_**Velja za:** poenostavljeno uvedbo – posel do izstavitve predračuna, Project Operations za primere, ki temeljijo na virih/nezalogi_

Podrobnosti ponudb, ki temeljijo na projektu, so oblikovane tako, da pripomorejo k oceni projektnega dela v okviru interakcije. Struktura podrobnosti ponudb, ki temelji na projektu, je razširjena za ocene projektov z naslednjimi koncepti:

- Način obračunavanja
- Preslikavanje projektov in opravil
- Vključuje razrede transakcij
- Omejitev »Ni dovoljeno preseči«
- Nastavitev možnosti zaračunavanja
- Ocena z uporabo podrobnosti ponudb
- Stranke podrobnosti ponudbe

Naslednja tabela vsebuje informacije o poljih na zavihku **Splošno** pri podrobnosti ponudbe, ki temelji na projektu. Ta polja pomagajo nastaviti osnovo za podrobno, temeljito oceno projektnega dela.

| **Polje** | **Opis** | **Nadaljnji vpliv** |
| --- | --- | --- |
| Imenu | Ime vrstice ponudbe, ki vam pomaga prepoznati posamezno komponento ponudbe, ki se ocenjuje. | Kopirano v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Način obračunavanja | V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja v vrstici priložnosti. To polje vključuje dva glavna pogodbena modela, ki sta podprta v aplikaciji Dynamics 365 Project Operations:</br>- fiksna cena</br>- čas in material| Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena. |
| Project | S tem izbirnim poljem določite projekt, ki se bo uporabljal za izvedbo dela za to interakcijo. Ko je projekt preslikan v podrobnost ponudbe, pripomore k nastavitvi opravil, ki se zaračunajo, in tudi k pripravi ocene, ki temelji na projektu, pri vrstici ponudbe v obliki podrobnosti vrstice ponudbe. Če projekt ni preslikan na vrstico ponudbe, ki temelji na projektu, morate oceno ustvariti ročno z izdelavo vsake podrobnosti vrstice ponudbe. | Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena.|
| Vključena opravila | Označuje, ali se ta podrobnost ponudbe uporablja za vsa ali nekatera projektna opravila za izbrani projekt. To polje ima lahko naslednje vrednosti:</br>- vsa opravila projekta</br>- samo izbrana opravila projekta</br>Prazna vrednost v tem polju je enaka možnosti **Vsa projektna opravila**. | Ko je na strani projekta izbrana možnost **Samo izbrane projektne naloge**, zavihek **Nastavitev obračunavanja opravil** omogoča, da izberete določena opravila in jih povežete s to vrstico ponudbe. Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena. |
| Vključi čas | Vrednost **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudb. Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v oceno v tej vrstici ponudbe. Vrednost **Da** označuje, da bodo časovne transakcije ali stroški dela vključeni v oceno v tej vrstici ponudbe. | Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena. |
| Vključi strošek | Vrednost **Da**/**Ne** označuje, ali bodo stroški za izbrani projekt vključeni v oceno v tej vrstici ponudb. Vrednost **Ne** označuje, da strošek ne bo vključen v oceno v tej vrstici ponudbe. Vrednost **Ne** označuje, da bo strošek vključen v oceno v tej vrstici ponudbe. | Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena. |
| Vključi material | Vrednost **Da**/**Ne** označuje, ali bodo stroški materiala za izbrani projekt vključeni v oceno v tej vrstici ponudb. Vrednost **Ne** označuje, da stroški materiala ne bodo vključeni v oceno v tej vrstici ponudb. Vrednost **Ja** označuje, da bodo stroški materiala vključeni v oceno v tej vrstici ponudb. | Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena. |
| Vključi dajatev | Vrednost **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključene v oceno v tej vrstici ponudb. Vrednost **Ne** označuje, da dajatve ne bodo vključene v oceno v tej vrstici ponudbe. Vrednost **Da** označuje, da bodo dajatve vključene v oceno v tej vrstici ponudbe. | Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena. |
| Znesek ponudbe | To je znesek, ki bo stranki naveden za vse napovedano delo v tej vrstici ponudb, ki temelji na projektu. V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz polja **Proračun stranke** v vrstici priložnosti. Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska v podrobnostih vrstice ponudbe. | Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena. |
| Predvideni davek | To je polje, ki ga je mogoče urejati in v katerem lahko uporabnik doda predviden znesek davka v vrstico ponudbe. Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska davka v podrobnostih vrstice ponudbe. | Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena. |
| Znesek ponudbe po obdavčitvi | To polje je znesek v podrobnosti ponudbe po obdavčitvi in je samo za branje. Znesek v tem polju se izračuna kot *znesek ponudbe + davek*. | Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena. |
| Omejitev »Ni dovoljeno preseči« | To polje je mogoče urejati in je na voljo samo v podrobnostih ponudb, ki temeljijo na projektih in imajo način obračunavanja **Čas in material**. | Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena. |
| Proračun stranke | To polje je mogoče urejati in se kopira iz ustreznega polja v vrstici priložnosti, če je bila ponudba ustvarjena iz priložnosti. | Ta vrednost se kopira v podrobnosti projektne pogodbe, ki je ustvarjena iz te vrstice ponudbe, ko je ponudba pridobljena. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Pravila za preverjanje veljavnosti polj na zavihku Splošno v podrobnostih ponudb, ki temeljijo na projektih

**1. pravilo**: če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta**, je projekt vključen v podrobnost ponudbe.

**2. pravilo**: če je polje **Vključena opravila** prazno ali če je nastavljeno na **Vsa opravila projekta**, je projekt in izbran razred transakcije mogoče vključiti samo v eno podrobnost ponudbe, ki temelji na projektu.

**3. pravilo**: če je polje **Vključena opravila** nastavljeno na **Samo izbrana opravila projekta**, je projekt in izbran razred transakcije mogoče vključiti v več podrobnosti ponudbe, ki temeljijo na projektu.

**4. pravilo** : če ima priložnost več ponudb, so lahko podrobnosti ponudbe za različne ponudbe, ki se vse sklicujejo na isti projekt in vključujejo isti razred transakcije.

**5. pravilo**: če ponudbe ne pripadajo isti priložnosti, ne morejo vključevati istega projekta in razreda transakcije.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Priložnost</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Ponudba</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Podrobnost ponudbe</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Vključena opravila</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Vključi čas</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Vključi strošek</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Vključi material</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Vključi</strong>
                </p>
                <p>
                    <strong>Dajatev</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Veljavno/neveljavno</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Razlog</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neveljavno </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kršitev 2. pravila. Čas, stroški in dajatve za projekt P1 so vključeni v podrobnosti ponudbe QL1 in QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neveljavno </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kršitev 2. pravila. Čas, material in dajatve za projekt P1 so vključeni v podrobnosti ponudbe QL1 in QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Veljavno </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Čas, material in dajatve za projekt P1 so vključeni v QL1 <br>
Stroški za projekt P1 so vključeni v QL2 <br>
Ni prekrivanja tega, kar je vključeno v vsako vrstico ponudbe in je zato veljavno.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Samo izbrana opravila </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neveljavno </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kršitev 2. pravila </p>
                <p>
Q1 vključuje čas, material, stroške in nadomestila za podmnožico opravil v projektu P1 </p>
                <p>
QL2 vključuje čas, stroške in dajatve za celoten projekt P1 in se torej prekriva s tem, kar je vključeno v Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Samo izbrana opravila </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Veljavno </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Po 3. pravilu, </p>
                <p>
Q1 vključuje čas, material, stroške in nadomestila za podmnožico opravil v projektu P1.
                </p>
                <p>
QL2 vključuje čas, material, stroške in nadomestila za podmnožico opravil v projektu P1.
                </p>
                <p>
Edino dodatno preverjanje se izvaja okoli podmnožice opravil za QL1, ki se razlikuje od podmnožice opravil za QL2, da se prepreči prekrivanje. To opravi sistem, ko so opravila povezana.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon2 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Samo izbrana opravila </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vsa opravila projekta ali prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Veljavno </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Po 5. pravilu sta Q1 in Q2 dve ponudbi za isto priložnost, tako da lahko obe ocenjujeta enake komponente projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
2. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vsa opravila projekta ali prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vsa opravila projekta ali prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Neveljavno </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Po 4. pravilu sta Q1 in Q2 dve ponudbi za različni priložnosti, tako da ne moreta obe ocenjevati enakih komponente istega projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
Pril2 </p>
            </td>
            <td width="39" valign="top">
                <p>
1. četrt. </p>
            </td>
            <td width="40" valign="top">
                <p>
PodrPon1 </p>
            </td>
            <td width="41" valign="top">
                <p>
O1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vsa opravila projekta ali prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
