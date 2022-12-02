---
title: Vrstice računa dobavitelja za čas
description: V tem članku je pojasnjeno, kako zabeležiti vrstice računov dobavitelja za časovne stroške, ki jih zabeležijo podizvajalci.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262033"
---
# <a name="vendor-invoice-lines-for-time"></a>Vrstice računa dobavitelja za čas

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Račun dobavitelja ima lahko v aplikaciji Microsoft Dynamics 365 Project Operations vrstice računa dobavitelja za čas. Vodje projektov lahko uporabijo vrstice računov dobavitelja za čas za beleženje stroškov časa podizvajalca za projekte.

Vrstice računa dobavitelja za čas se lahko nanašajo na podrobnosti podizvajalske pogodbe za čas ali pa tudi ne. Če se vrstica računa dobavitelja za čas sklicuje na podizvajalsko pogodbo, bodo vodje projektov lahko primerjali in preverili čas, za katere vrstica računa dobavitelja izda račun, glede na čas, ki so ga za projekt zabeležili podizvajalci in odobrili vodje projektov.

V spodnji tabeli so informacije o poljih v vrsticah računa dobavitelja za čas.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime podrobnosti računa dobavitelja za pomoč pri identifikaciji. | Ime bo prikazano kot prvi stolpec v vseh iskanjih, ki temeljijo na vrsticah računa dobavitelja. |
| Description | Kratek opis storitev, za katere dobavitelj izda račun, v vrstici računa dobavitelja. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, na podlagi katere so bile storitve prvotno naročene. | Ko je za račun dobavitelja izbrana podizvajalska pogodba, bodo vse vrstice na računu dobavitelja podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa dobavitelja, ki se nanašajo na različne podizvajalske pogodbe. |
| Podrobnosti podizvajalske pogodbe | Podrobnosti podizvajalske pogodbe, na podlagi katerih so bile storitve naročene. Seznam podrobnosti podizvajalske pogodbe, ki jih je mogoče izbrati, je omejen na vrstice na izbrani podizvajalski pogodbi. | Ko so v vrstici računa dobavitelja za čas izbrane podrobnosti podizvajalske pogodbe, se privzete vrednosti za polja **Projekt**, **Vloga** in **Vir, ki ga je mogoče rezervirati** vnesejo iz ustreznih polj v podrobnosti podizvajalske pogodbe. Če imajo izbrane podrobnosti podizvajalske pogodbe vrednosti v poljih **Projekt**, **Vloga** in **Vir, ki ga je mogoče rezervirati**, se vrednosti ustreznih polj v vrstici računa dobavitelja ne morejo razlikovati od teh vrednosti. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa dobavitelja zabeležen v projektu. | Ni priprav ali omejitev |
| Razred transakcije | Privzeta vrednost je **Čas**. | Vrednost **Čas** označuje, da se vrstica računa dobavitelja uporablja za beleženje zneska računa za čas podizvajalca. |
| Projekt | Ime projekta, pri katerem so bile uporabljene storitve, za katere se izdaja račun. | To polje je obvezno in ne sme biti prazno. |
| opravilo, | Ime opravila projekta, pri katerem so bile uporabljene storitve, za katere se izdaja račun. To polje je na voljo le, če je izbran projekt. Izbira opravila projekta ni obvezna. | Če je to polje prazno, lahko vodja projekta poveže vrstico računa dobavitelja s časom, ki ga viri podizvajalca zabeležijo pri katerem koli opravilu projekta. Če se vrstica računa dobavitelja ne sklicuje na podrobnosti podizvajalske pogodbe in je to polje prazno, dejanski strošek, ki ga ustvari vrstica računa dobavitelja, ne bo povezan z morebitnimi neobračunanimi dejanskimi vrednostmi prodaje. Če je nastavljeno obračunavanje na podlagi opravil, v tem primeru končni stranki morda ne bo mogoče izdati računa za stroške. |
| Vloga | Vloga virov podizvajalske pogodbe, katerih čas se zaračunava. | To polje določa vlogo, ki jo izvajajo podizvajalski viri, katerih čas je zaračunan na računu dobavitelja. |
| Vir, ki ga je mogoče rezervirati | Ime virov podizvajalske pogodbe, katerih čas se zaračunava. Izbira vira, ki ga je mogoče rezervirati, ni obvezna. | Če je to polje prazno, lahko vodja projekta poveže vrstico računa dobavitelja s časom, ki ga zabeleži kateri koli vir, ki pripada dobavitelju v vrstici računa dobavitelja. |
| Količina | Vnesite število ur, za katere dobavitelj izda račun, v vrstici računa dobavitelja. |Ni priprav ali omejitev |
| Skupina enot | Privzeta vrednost je **Skupina časovnih enot**, česar ni mogoče spremeniti. | Ni priprav ali omejitev |
| Enota | Privzeta vrednost je nastavljena na osnovno enoto ur iz skupine časovne enote. To vrednost lahko spremenite, če želite kupiti katero koli enoto skupine časovnih enot, na primer dan ali teden. | Kombinacija vrednosti **Vloga** in **Enota** bo uporabljena kot privzeta ali izračunana za vrednost polja **Cena enote** v vrstici računa dobavitelja. |
| Cena enote | Privzeta cena enote uporablja kombinacijo vrednosti **Vloga** in **Enota**, zapisane na ceniku projekta, ki velja za datum transakcije vrstice računa dobavitelja. | Kadar je cena v veljavnem ceniku projekta določena v drugačni enoti kot enota v vrstici računa dobavitelja, sistem za izračun cene na enoto uporabi pretvorbo enote. |
| Delna vsota | To polje samo za branje se samodejno izračuna kot *Količina* &times; *Cena enote*, če je vnesena tako vrednost polja **Količina** kot tudi **Cena enote**. Če je prazno eno ali obe polji, lahko v to polje vnesete vrednost. | Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek vrstice računa dobavitelja z vključenimi davki. Vrednost tega polja je izračunana na naslednji način: *delni znesek* + *prometni davek*. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
