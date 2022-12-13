---
title: Pregled projektnih pogodbenih linij
description: Ta članek vsebuje informacije o delu s pogodbenimi vrsticami projekta v Project Operations.
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f5a529233692a39b0674417cd4ea225e40243086
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824647"
---
# <a name="project-contract-lines-overview"></a>Pregled projektnih pogodbenih linij

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Podrobnosti pogodbe, ki temelji na projektu, v aplikaciji Dynamics 365 Project Operations so zasnovane, da hranijo dogovore o oceni in obračunavanju za določene komponente dela na projektu v interakciji. Struktura podrobnosti pogodbe, ki temeljijo na projektu, je razširjena za ocene projektov in scenarije obračunavanja z naslednjimi koncepti:

- Način obračunavanja
- Preslikavanje projektov in opravil
- Vključuje razrede transakcij
- Omejitev »Ni dovoljeno preseči«
- Nastavitev možnosti zaračunavanja
- Ocene s podrobnosti vrstice pogodbe
- Stranke podrobnosti pogodbe

Naslednja tabela vključuje polja na zavihku **Splošno** podrobnosti pogodbe, ki temeljijo na projektu, ki pomagajo nastaviti podlago za podrobno, celovito oceno in dogovore za obračunavanje za delo, ki temelji na projektu.

| Polje | Opis | Nadaljnji vpliv |
| --- | --- | --- |
| **Ime** | Ime podrobnosti pogodbe. To opredeljuje posamezno komponento pogodbe, ki se ocenjuje. Za projektno pogodbo, ustvarjeno iz ponudbe, je ta vrednost kopirana iz pripadajoče vrednosti podrobnosti ponudbe, ki temelji na projektu. | Ime, kopirano v projektno vrstico računa, ki je ustvarjena iz teh podrobnosti pogodbe, ko je ustvarjen račun. |
| **Način obračunavanja** | V projektni pogodbi, ustvarjeni iz ponudbe, je ta vrednost kopirana iz pripadajočega polja podrobnosti ponudbe. To je nabor možnosti, ki predstavlja dva glavna pogodbena modela, ki ju podpira Project Operations:</br>- **Fiksna cena**</br>- **Čas in material** | Na podlagi metode obračunavanja v sklicevanih podrobnostih pogodbe bo dejanska transakcija obdelana. Če imajo podrobnosti pogodbe, sklicevane z dejansko vrednostjo, način obračunavanja časa in materiala, sta ustvarjena zapisa stroška in dejanska vrednost neobračunane prodaje. Če imajo podrobnosti pogodbe, na katere se sklicuje dejanska vrednost, način obračunavanja fiksne cene, je ustvarjena samo dejanska vrednost stroška. |
| **Project** | Uporabite to polje za prepoznavanje projekta, ki bo uporabljen za zagotavljanje dela za to interakcijo. | Ta vrednost se bo uporabljala skupaj z **vključenimi opravili** in **vključenimi razredi transakcij** za razrešitev sklica podrobnosti pogodbe v zapisu dejanske vrstice ali ocene vrstice. |
| **Vključena opravila** | Označuje, ali te podrobnosti pogodbe vključujejo vsa projektna opravila za izbrani projekt ali samo podnabor opravil. To je nabor možnosti, ki ima naslednje možne vrednosti:</br>- **Vsa opravila projekta**</br>- **Samo izbrana opravila projekta**. Privzeta vrednost v tem polju je enaka izbiri možnosti **Vsa opravila projekta**. | Če je izbrana možnost **Samo izbrana opravila**, lahko izberete določena opravila in jih povežete s temi podrobnostmi pogodbe na zavihku **Nastavitev obračunavanja opravil** strani **Projekt**. Vrednost bo uporabljena v povezavi z možnostma **Projekt** in **Vključeni razredi transakcij** za odpravljanje sklica podrobnosti pogodbe v zapisu dejanskih ali ocenjenih podrobnosti. |
| **Vključi čas** | Vrednost **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v v tej pogodbeni vrstici. Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v te podrobnosti pogodbe. Vrednost **Da** označuje, da bodo. | Ta vrednost se uporablja skupaj s projektom za razrešitev sklica na pogodbeno vrstico v zapisu vrstice dejanske vrednosti ali ocene. |
| **Vključi strošek** | Vrednost **Da**/**Ne** označuje, ali bodo stroški za izbrani projekt vključeni v oceno v tej pogodbeni vrstici. Vrednost **Ne** označuje, da stroški ne bodo vključeni v te podrobnosti pogodbe. Vrednost **Da** označuje, da bodo. | Ta vrednost se uporablja skupaj s projektom za razrešitev sklica na pogodbeno vrstico v zapisu vrstice dejanske vrednosti ali ocene. |
| **Vključi materiale** | Vrednost **Da**/**Ne** označuje, ali bodo stroški materiala za izbrani projekt vključeni v oceno v tej pogodbeni vrstici. Vrednost **Ne** označuje, da stroški materiala ne bodo vključeni v oceno v tej pogodbeni vrstici. Vrednost **Da** označuje, da bodo. | Ta vrednost se uporablja skupaj s projektom za razrešitev sklica na pogodbeno vrstico v zapisu vrstice dejanske vrednosti ali ocene. |
| **Vključi dajatev** | Vrednost **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključeni v oceno v tej pogodbeni vrstici. Vrednost **Ne** označuje, da dajatve ne bodo vključene v te podrobnosti pogodbe. Vrednost **Da** označuje, da bodo. | Ta vrednost se uporablja skupaj s projektom za razrešitev sklica na pogodbeno vrstico v zapisu vrstice dejanske vrednosti ali ocene. |
| **Pogodbeni znesek** | V podrobnostih pogodbe za fiksno ceno je ta znesek dogovorjena vrednost, ki bo zaračunana stranki za vse komponente dela, povezane s temi podrobnostmi pogodbe. V podrobnostih pogodbe za čas in material je ta znesek ocenjena vrednost, kaj bo zaračunano stranki za vse komponente dela, povezane s temi podrobnostmi pogodbe. V projektni pogodbi, ki je ustvarjena iz ponudbe, je ta vrednost kopirana iz pripadajočega polja podrobnosti ponudbe. Ko imajo podrobnosti pogodbe, ki temeljijo na projektu, podrobnosti vrstice, je to polje zaklenjeno za urejanje in je povzeto z zneska v podrobnostih vrstice pogodbe. | Ko imajo podrobnosti pogodbe podrobnosti vrstice, je mogoče to vrednost spremeniti s spremembo zneskov v podrobnostih vrstice. V podrobnostih pogodbe za fiksno ceno je ta vrednost uporabljena za ustvarjanje zneska pred davkom v rednih mejnikih obračunavanja. |
| **Predvideni davek** | Uporabnik lahko uredi to polje za vnos ocenjenega zneska davka v podrobnosti pogodbe. Ko imajo podrobnosti pogodbe, ki temeljijo na projektu, podrobnosti vrstice, je to polje zaklenjeno za urejanje in je povzeto z zneska davka v podrobnostih vrstice pogodbe. | Ko imajo podrobnosti pogodbe podrobnosti vrstice, je mogoče to vrednost spremeniti s spremembo zneskov davka v podrobnostih vrstice. V podrobnostih pogodbe za fiksno ceno je ta vrednost uporabljena za ustvarjanje davka v rednih mejnikih obračunavanja. |
| **Pogodbeni znesek po obdavčitvi** | Znesek podrobnosti pogodbe po obdavčitvi. To polje je samo za branje in je izračunano kot **Pogodbeni znesek + davek**. | V podrobnostih pogodbe za fiksno ceno je ta vrednost uporabljena za ustvarjanje rednih mejnikov obračunavanja. |
| **Omejitev »Ni dovoljeno preseči«** | Uporabnik lahko to polje ureja ter je na voljo samo za podrobnosti pogodbe, ki temeljijo na projektu, ki imajo način obračunavanja nastavljen na čas in material. | Uporabnik lahko ureja to polje. Ko se dejanska vrednost za čas in material sklicuje na te podrobnosti pogodbe za čas in material, je znesek dejanske vrednosti ocenjen glede na omejitev, ki je ni dovoljeno preseči, v podrobnostih pogodbe. To ocenjevanje je izvedeno potem, ko so že porabljeni in potrjeni zneski upoštevani. |
| **Proračun stranke** | To polje je mogoče urejati in je kopirano iz pripadajočega polja za podrobnosti ponudbe, če je bila pogodba ustvarjena iz ponudbe. | To polje se uporablja samo za informacije in nima pomena v poteku navzdol. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Veljavnostna pravila za možnosti na zavihku »Splošno« podrobnosti pogodbe, ki temelji na projektu

Pravilo 1: Če je polje **Vključena opravila** prazno ali nastavljeno na **Vsa opravila projekta**, so vsa opravila projekta vključena v podrobnosti pogodbe.

Pravilo 2: Če je polje **Vključena opravila** prazno ali izrecno nastavljeno na **Vsa opravila projekta**, sta lahko projekt in določen razred transakcije vključena samo v en sklop podrobnosti pogodbe, ki temeljijo na projektu, pogodbe.

Pravilo 3: Če je polje **Vključena opravila** nastavljeno na **Samo izbrana opravila projekta**, sta lahko projekt in določen razred transakcije vključena v več sklopov podrobnosti pogodbe, ki temeljijo na projektu, pogodbe.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Pogodba</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Podrobnosti pogodbe</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
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
                    <strong>Vključi materiale</strong>
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
            <td width="53" valign="top">
                <p>
                    <strong>Veljavno/neveljavno</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Razlog</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Neveljavno </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kršitev 2. pravila. Čas, stroški, materiali in dajatve za projekt P1 so vključeni v podrobnostih pogodbe CL1 in CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Neveljavno </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kršitev 2. pravila. Čas, materiali in dajatve za projekt P1 so vključeni v podrobnostih pogodbe CL1 in CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Veljavno </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Čas, materiali in dajatve za projekt P1 so vključeni v CL1.
                </p>
                <ul>
                    <li>
Stroški za projekt P1 so vključeni v CL2.
                    </li>
                </ul>
                <p>
Ni prekrivanja tega, kar je vključeno v vsako podrobnosti pogodbe in je zato veljavno.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Neveljavno </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kršitev 2. pravila </p>
                <p>
C1 vključuje čas, materiale, stroške in nadomestila za podmnožico opravil v projektu P1.
                </p>
                <p>
CL2 vključuje čas, materiale, stroške in dajatve za celoten projekt P1 in se torej prekriva s tem, kar je vključeno v C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Veljavno </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Po 3. pravilu, </p>
                <p>
C1 vključuje čas, stroške, materiale in nadomestila za podmnožico opravil v projektu P1.
                </p>
                <p>
CL2 vključuje čas, stroške, materiale in nadomestila za podmnožico opravil v projektu P1.
                </p>
                <p>
Edino dodatno preverjanje se izvaja okoli podmnožice opravil za CL1, ki se razlikuje od podmnožice opravil za CL2, da se prepreči prekrivanje. To opravi sistem, ko so opravila povezana.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
O1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
