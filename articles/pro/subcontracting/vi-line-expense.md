---
title: Vrstice računa dobavitelja za kategorije stroškov
description: V tem članku je pojasnjeno, kako zapisati vrstice računa dobavitelja za kategorije stroškov.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261720"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Vrstice računa dobavitelja za kategorije stroškov

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Račun dobavitelja ima lahko v aplikaciji Microsoft Dynamics 365 Project Operations vrstice računa dobavitelja za kategorije stroškov. Vodje projektov lahko uporabijo vrstice računa dobavitelja za kategorije stroškov za zapisovanje stroškov storitev, ki so nabavljene kot kategorije stroškov.

Vrstice računa dobavitelja za kategorije stroškov se lahko nanašajo na podrobnosti podizvajalske pogodbe za stroške kategorij ali pa tudi ne. Če se vrstica računa dobavitelja za kategorije stroškov sklicuje na podizvajalsko pogodbo, bodo vodje projektov lahko primerjali in preverili stroške, za katere vrstica računa dobavitelja izda račun, glede na stroške, ki so jih za te kategorije stroškov zabeležili in odobrili vodje projektov.

V spodnji tabeli so informacije o poljih v vrsticah računa dobavitelja za kategorije stroškov.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime podrobnosti računa dobavitelja za pomoč pri identifikaciji. | Ime bo prikazano kot prvi stolpec v vseh iskanjih, ki temeljijo na vrsticah računa dobavitelja. |
| Description | Kratek opis storitev, za katere dobavitelj izda račun, v vrstici računa dobavitelja. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, na podlagi katere so bile storitve prvotno naročene. | Ko je za račun dobavitelja izbrana podizvajalska pogodba, bodo vse vrstice na računu dobavitelja podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa dobavitelja, ki se nanašajo na različne podizvajalske pogodbe. |
| Podrobnosti podizvajalske pogodbe | Podrobnosti podizvajalske pogodbe, na podlagi katerih so bile storitve naročene. Seznam podrobnosti podizvajalske pogodbe, ki jih je mogoče izbrati, je omejen na vrstice na izbrani podizvajalski pogodbi. | Ko so v vrstici računa dobavitelja za kategorije stroškov izbrane podrobnosti podizvajalske pogodbe, se privzete vrednosti za polja **Projekt**, **Opravilo** in **Kategorija transakcij** vnesejo iz ustreznih polj v podrobnostih podizvajalske pogodbe. Če imajo izbrane podrobnosti podizvajalske pogodbe vrednosti v poljih **Projekt**, **Opravilo projekta** in **Kategorija transakcij**, se vrednosti ustreznih polj v vrstici računa dobavitelja ne morejo razlikovati od teh vrednosti. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa dobavitelja zabeležen v projektu. |Ni priprav ali omejitev |
| Razred transakcije | Izberite možnost **Stroški** za beleženje računa dobavitelja za kategorijo stroškov. | Vrednost **Stroški** označuje, da se vrstica računa dobavitelja uporablja za beleženje zneska računa za storitve, ki so bile nabavljene kot kategorije stroškov. |
| Projekt | Ime projekta, pri katerem so bile uporabljene storitve, za katere se izdaja račun. | To polje je obvezno in ne sme biti prazno. |
| opravilo, | Ime opravila projekta, pri katerem so bile uporabljene storitve, za katere se izdaja račun. To polje je na voljo le, če je izbran projekt. Izbira opravila projekta ni obvezna. | Če je to polje prazno, lahko vodja projekta poveže vrstico računa dobavitelja za stroške, ki so zapisani pri katerem koli opravilu projekta. Če se vrstica računa dobavitelja ne sklicuje na podrobnosti podizvajalske pogodbe in je to polje prazno, dejanski strošek, ki ga ustvari vrstica računa dobavitelja, ne bo povezan z morebitnimi neobračunanimi dejanskimi vrednostmi prodaje. Če je nastavljeno obračunavanje na podlagi opravil, v tem primeru končni stranki morda ne bo mogoče izdati računa za stroške. |
| Kategorija transakcije | Kategorija transakcije, za katero se izdaja račun. Za izbrano kategorijo transakcij je treba ustvariti ustrezno kategorijo stroškov. | Kombinacija vrednosti **Kategorija transakcij** in **Enota** bo uporabljena kot privzeta ali izračunana za vrednost polja **Cena enote** v vrstici računa dobavitelja. |
| Količina | V to vrstico računa vnesite količino, ki ga zaračuna dobavitelj. |Ni priprav ali omejitev|
| Skupina enot | Privzeta vrednost je vnesena na skupini enot, ki je izbrana za kategorijo transakcij. | Ni priprav ali omejitev |
| Enota | Privzeta vrednost je osnovna enota izbrane skupine enot. To vrednost lahko spremenite, če želite kupiti v kateri koli enoti skupine enot. | Kombinacija vrednosti **Kategorija transakcij** in **Enota** bo uporabljena kot privzeta ali izračunana za vrednost polja **Cena enote** v vrstici računa dobavitelja. |
| Cena enote | Privzeta cena enote uporablja kombinacijo vrednosti **Kategorija transakcij** in **Enota**, zapisane na ceniku projekta, ki velja za datum transakcije vrstice računa dobavitelja. | Kadar je cena v veljavnem ceniku projekta določena v drugačni enoti kot enota v vrstici računa dobavitelja, sistem za izračun cene na enoto uporabi pretvorbo enote. |
| Delna vsota | To polje samo za branje se samodejno izračuna kot *Količina* &times; *Cena enote*, če je vnesena tako vrednost polja **Količina** kot tudi **Cena enote**. Če je prazno eno ali obe polji, lahko v to polje vnesete vrednost.| Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek vrstice računa dobavitelja z vključenimi davki. Vrednost tega polja je izračunana na naslednji način: *delni znesek* + *prometni davek*. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
