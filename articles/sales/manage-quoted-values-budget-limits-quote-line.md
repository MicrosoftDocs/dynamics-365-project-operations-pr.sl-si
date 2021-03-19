---
title: Pregled podrobnosti ponudb, ki temeljijo na projektih
description: Ta tema vsebuje informacije o uporabi podrobnosti ponudb, ki temeljijo na projektih, za projektno delo.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e61a9fbf357123884397b930662d11f22bfdeaa0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277808"
---
# <a name="project-based-quote-lines-overview"></a>Pregled podrobnosti ponudb, ki temeljijo na projektih

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Podrobnosti ponudb, ki temeljijo na projektu, so oblikovane tako, da pripomorejo k oceni projektnega dela v okviru interakcije. Struktura podrobnosti ponudb, ki temelji na projektu, je razširjena za ocene projektov z naslednjimi koncepti:

- Način obračunavanja
- Preslikavanje projektov
- Vključuje razrede transakcij
- Omejitev »Ni dovoljeno preseči«
- Nastavitev možnosti zaračunavanja
- Ocena z uporabo podrobnosti ponudb
- Stranke podrobnosti ponudbe

Naslednja tabela vsebuje informacije o poljih na zavihku **Splošno** pri podrobnosti ponudbe, ki temelji na projektu. Ta polja pomagajo nastaviti osnovo za podrobno, temeljito oceno projektnega dela.

| **Polje** | **Opis** | **Nadaljnji vpliv** |
| --- | --- | --- |
| Imenu | Ime podrobnosti ponudbe, ki bi vam pomagala prepoznati ločeno komponento ponudbe, ki jo ocenjujete. | Kopirano v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Način obračunavanja | V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz ustreznega polja v vrstici priložnosti. To polje vključuje dva glavna pogodbena modela, ki sta podprta v aplikaciji Dynamics 365 Project Operations:</br>- fiksna cena</br>- čas in material| Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Project | S tem izbirnim poljem določite projekt, ki se bo uporabljal za izvedbo dela za to interakcijo. Ko je projekt preslikan v podrobnost ponudbe, pripomore k nastavitvi opravil, ki se zaračunajo, in tudi k pripravi ocene, ki temelji na projektu, pri vrstici ponudbe v obliki podrobnosti vrstice ponudbe. Če projekt ni preslikan na vrstico ponudbe, ki temelji na projektu, morate oceno ustvariti ročno z izdelavo vsake podrobnosti vrstice ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Vključi čas | Zastava **Da**/**Ne** označuje, ali bodo časovne transakcije ali stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe. Vrednost **Ne** označuje, da časovne transakcije ali stroški dela ne bodo vključeni v oceno v tej vrstici ponudbe. Vrednost **Da** označuje, da bodo časovne transakcije ali stroški dela vključeni v oceno v tej vrstici ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Vključi strošek | Zastava **Da**/**Ne** označuje, ali bodo stroški dela za izbrani projekt vključeni v oceno v tej vrstici ponudbe. Vrednost **Ne** označuje, da strošek ne bo vključen v oceno v tej vrstici ponudbe. Vrednost **Ne** označuje, da bo strošek vključen v oceno v tej vrstici ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Vključi dajatev | Zastava **Da**/**Ne** označuje, ali bodo dajatve za izbrani projekt vključene v oceno v tej vrstici ponudbe. Vrednost **Ne** označuje, da dajatve ne bodo vključene v oceno v tej vrstici ponudbe. Vrednost **Da** označuje, da bodo dajatve vključene v oceno v tej vrstici ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Znesek ponudbe | To je znesek, ki bo stranki podan v ponudbi za vso delo, napovedano v tej podrobnosti ponudbe, ki temelji na projektu. V ponudbi, ustvarjeni iz priložnosti, se ta vrednost kopira iz polja **Proračun stranke** v vrstici priložnosti. Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska v podrobnostih vrstice ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Predvideni davek | To je polje, ki ga je mogoče urejati in v katerem lahko uporabnik doda predviden znesek davka v vrstico ponudbe. Če ima vrstica ponudbe, ki temelji na projektu, podrobnosti, je to polje zaklenjeno za urejanje in je povzeto iz zneska davka v podrobnostih vrstice ponudbe. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Znesek ponudbe po obdavčitvi | To polje je znesek v podrobnosti ponudbe po obdavčitvi in je samo za branje. Znesek v tem polju se izračuna kot *znesek ponudbe + davek*. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Omejitev »Ni dovoljeno preseči« | To polje je mogoče urejati in je na voljo samo v podrobnostih ponudb, ki temeljijo na projektih in imajo način obračunavanja **Čas in material**. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |
| Proračun stranke | To polje je mogoče urejati in se kopira iz ustreznega polja v vrstici priložnosti, če je bila ponudba ustvarjena iz priložnosti. | Ta vrednost polja je kopirana v podrobnost projektne pogodbe, ki je ustvarjena iz te podrobnosti ponudbe, ko je ponudba pridobljena. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Pravila za preverjanje veljavnosti polj na zavihku Splošno v podrobnostih ponudb, ki temeljijo na projektih

**1. pravilo**: določen razred transakcije v izbranem projektu je mogoče vključiti samo v eno podrobnost ponudbe, ki temelji na projektih.

**2. pravilo** : če ima priložnost več ponudb, so lahko podrobnosti ponudbe za različne ponudbe, ki se vse sklicujejo na isti projekt in vključujejo isti razred transakcije.

**3. pravilo**: če ponudbe ne pripadajo isti priložnosti, ne morejo vključevati istega projekta in razreda transakcije.

<table border="1" cellspacing="0" cellpadding="0">
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
                    <strong>dajatev</strong>
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
Kršitev 1. pravila. Čas, stroški in dajatve za projekt Proj1 so vključeni v obe podrobnosti ponudbe: PodrPon1 in PodrPon2.
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
Kršitev 1. pravila. Čas in dajatve za projekt Proj1 so vključeni v obe podrobnosti ponudbe: PodrPon1 in PodrPon2.
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
Ni prekrivanja glede tega, kar je vključeno v vsako podrobnost ponudbe, tako da je veljavno.
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
Kršitev zgornjega 1. pravila </p>
                <p>
Pon1 vključuje čas, stroške in dajatve za celoten projekt P1.
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
Glede na 2. pravilo sta Pon1 in Pon2 dve ponudbi za isto priložnost, tako da lahko oba ocenjujeta enake komponente projekta.
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
PodrPon1 pri Pon2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Proj1 </p>
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
Glede na 3. pravilo sta Pon1 in Pon2 dve ponudbi za različni priložnosti, tako da ne moreta obe ocenjevati enakih komponent istega projekta.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]