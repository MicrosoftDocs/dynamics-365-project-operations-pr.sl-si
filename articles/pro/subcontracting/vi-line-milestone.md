---
title: Vrstice računa dobavitelja za mejnike
description: V tem članku je pojasnjeno, kako ustvariti vrstice računa dobavitelja za mejnike v podizvajalski pogodbi.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261049"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Vrstice računa dobavitelja za mejnike

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Račun dobavitelja ima lahko v aplikaciji Microsoft Dynamics 365 Project Operations vrstice računa dobavitelja za mejnike, ki so opredeljeni v podrobnostih podizvajalske pogodbe. Vodje projektov lahko uporabijo vrstice računa dobavitelja za mejnike, da zabeležijo stroške storitev, ki so nabavljene kot stroški na podlagi mejnikov, ki nastanejo pri storitvah ali izdelkih, nabavljenih za projekt.

Vrstice računa dobavitelja za mejnike se morajo vedno sklicevati na podrobnosti podizvajalske pogodbe, ki ima metodo obračunavanja »Nespremenljiva cena«. Ko se vrstica računa dobavitelja za mejnike sklicuje na podrobnosti podizvajalske pogodbe, bodo vodje projektov lahko primerjali in preverili osnovne stroške časa, stroške ali materiale, ki se sklicujejo na te podrobnosti podizvajalske pogodbe, z mejnikom, za katerega dobavitelj izdaja račun.

V spodnji tabeli so informacije o poljih v vrsticah računa dobavitelja za mejnike.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime podrobnosti računa dobavitelja za pomoč pri identifikaciji. | Ime bo prikazano kot prvi stolpec v vseh iskanjih, ki temeljijo na vrsticah računa dobavitelja. |
| Description | Kratek opis storitev, za katere dobavitelj izda račun, v vrstici računa dobavitelja. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, na podlagi katere so bile storitve prvotno naročene. | Ko je za račun dobavitelja izbrana podizvajalska pogodba, bodo vse vrstice na računu dobavitelja podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa dobavitelja, ki se nanašajo na različne podizvajalske pogodbe. |
| Podrobnosti podizvajalske pogodbe | Podrobnosti podizvajalske pogodbe, na podlagi katerih so bile storitve naročene. Seznam podrobnosti podizvajalske pogodbe, ki jih je mogoče izbrati, je omejen na vrstice na izbrani podizvajalski pogodbi. | Ko so v vrstici računa dobavitelja za mejnike izbrane podrobnosti podizvajalske pogodbe, polja **Vloga** in **Kategorija transakcije** in polja, povezana z izdelkom, niso pomembna in niso na voljo. Polja **Količina**, **Enota** in **Skupina enot** prav tako niso ustrezna za vrstice računa dobavitelja na podlagi mejnikov. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa dobavitelja zabeležen v projektu. | Ni priprav ali omejitev |
| Razred transakcije | Izberite **Mejnik** za zapisovanje računa dobavitelja za opravljen mejnik, ki je bil opredeljen v podrobnostih podizvajalske pogodbe. | Ni priprav ali omejitev |
| Mejnik | Izberite mejnik, ki je opredeljen v povezanih podrobnostih podizvajalske pogodbe, ki so označene kot **Pripravljeno za izdajanje računov**. | Mejnike podrobnosti podizvajalske pogodbe, ki imajo stanje **Pripravljeno za izdajanje računov**, je mogoče izbrati v vrstici računa dobavitelja. |
| Projekt | Ime projekta, pri katerem so bile uporabljene storitve, za katere se izdaja račun. | To polje je obvezno in ne sme biti prazno. |
| opravilo, | Ime opravila projekta, pri katerem so bile uporabljene storitve, za katere se izdaja račun. To polje je na voljo le, če je izbran projekt. Izbira opravila projekta ni obvezna. | Če je to polje prazno, lahko vodja projekta poveže vrstico računa dobavitelja z razredom transakcije na povezanih podrobnostih podizvajalske pogodbe, ki se beležijo pri katerem koli opravilu projekta. Če se vrstica računa dobavitelja ne sklicuje na podrobnosti podizvajalske pogodbe in je to polje prazno, dejanski strošek, ki ga ustvari vrstica računa dobavitelja, ne bo povezan z morebitnimi neobračunanimi dejanskimi vrednostmi prodaje. Če je nastavljeno obračunavanje na podlagi opravil, v tem primeru končni stranki morda ne bo mogoče izdati računa za stroške. |
| Znesek mejnika | Vnesite vrednost mejnika, ki je opredeljen v podrobnostih podizvajalske pogodbe, ki so pripravljene za izdajanje računov. | Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek vrstice računa dobavitelja z vključenimi davki. To polje se izračuna kot *Znesek mejnika* + *Prometni davek*. | Ni priprav ali omejitev |

> [!NOTE]
> Ko je ustvarjena vrstica računa dobavitelja, ki se sklicuje na mejnik podrobnosti podizvajalske pogodbe, se stanje mejnika podizvajalske pogodbe na **Račun dobavitelja je ustvarjen**. Ko je ta račun dobavitelja potrjen, se stanje mejnika podrobnosti podizvajalske pogodbe posodobi na **Račun dobavitelja je potrjen**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
