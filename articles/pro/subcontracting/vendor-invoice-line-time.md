---
title: Vrstice računa dobavitelja za čas
description: V tem članku je razloženo, kako zabeležiti vrstice računov dobavitelja za časovne stroške, ki jih naložijo podizvajalci.
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

Račun dobavitelja v Microsoftu Dynamics 365 Project Operations lahko ima vrstice računov dobavitelja za čas. Vodje projektov lahko uporabijo vrstice računov dobavitelja za čas, da zabeležijo stroške časa podizvajalcev na projektih.

Vrstice računa dobavitelja za čas se lahko nanašajo na podizvajalsko vrstico za čas ali pa tudi ne. Če se vrstica računa dobavitelja za čas sklicuje na podizvajalsko pogodbo, bodo vodje projektov lahko primerjali in preverili čas, ki ga fakturira vrstica računa dobavitelja, s časom, ki so ga zabeležili podizvajalci in odobrili vodje projektov v projektu.

Naslednja tabela vsebuje informacije o poljih v vrsticah računa dobavitelja za čas.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime vrstice računa dobavitelja za pomoč pri identifikaciji. | To ime bo prikazano kot prvi stolpec pri vseh iskanjih, ki temeljijo na vrsticah računa dobavitelja. |
| Description | Kratek opis storitev, ki jih prodajalec fakturira v vrstici računa dobavitelja. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, na podlagi katere so bile storitve prvotno naročene. | Ko je za račun dobavitelja izbrana podizvajalska pogodba, bodo vse vrstice na računu dobavitelja podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa dobavitelja, ki se nanašajo na različne podizvajalske pogodbe. |
| Podizvajalska linija | Podizvajalska linija, na kateri so bile naročene storitve. Seznam podizvajalskih postavk, ki jih je mogoče izbrati, je omejen na postavke na izbrani podizvajalski pogodbi. | Ko je v vrstici računa dobavitelja za čas izbrana podizvajalska vrstica, se privzete vrednosti za **Projekt**, **·**, in **Vir, ki ga je mogoče rezervirati** polja se vnesejo iz ustreznih polj na podizvajalski vrstici. Če ima izbrana podizvajalska vrstica vrednosti v **Projekt**, **·**, in **Možno rezervirati** polj, se vrednosti ustreznih polj v vrstici računa dobavitelja ne morejo razlikovati od teh vrednosti. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa dobavitelja zabeležen v projektu. | Ni priprav ali omejitev |
| Razred transakcije | Privzeta vrednost je **Čas**. | Vrednost **Čas** označuje, da se vrstica računa dobavitelja uporablja za beleženje zneska računa za čas podizvajalca. |
| Projekt | Ime projekta, pri katerem so bile uporabljene storitve, ki se fakturirajo. | To polje je obvezno in ne sme biti prazno. |
| opravilo, | Ime projektne naloge, za katero so bile uporabljene storitve, ki se fakturirajo. To polje je na voljo le, če je izbran projekt. Izbira projektne naloge je neobvezna. | Če je to polje prazno, lahko vodja projekta poveže vrstico računa dobavitelja s časom, ki ga zabeležijo viri podizvajalcev pri kateri koli nalogi projekta. Če se vrstica računa dobavitelja ne sklicuje na vrstico podizvajalca in je to polje prazno, dejanski strošek, ki ga ustvari vrstica računa dobavitelja, ne bo povezan z nobenimi neobračunanimi dejanskimi vrednostmi prodaje. V tem primeru, če je nastavljeno obračunavanje na podlagi nalog, stroškov morda ne bo mogoče zaračunati končnemu kupcu. |
| Vloga | Vloga virov podizvajalcev, katerih čas se fakturira. | To polje določa vlogo, ki jo izvajajo viri podizvajalcev, katerih čas je fakturiran na računu dobavitelja. |
| Vir, ki ga je mogoče rezervirati | Ime podizvajalca, katerega čas se fakturira. Izbira vira, ki ga je mogoče rezervirati, ni obvezna. | Če je to polje prazno, lahko vodja projekta poveže vrstico računa dobavitelja s časom, ki ga zabeleži kateri koli vir, ki pripada prodajalcu v vrstici računa dobavitelja. |
| Količina | V vrstico računa vnesite število ur časa, ki jih je fakturiral prodajalec. |Ni priprav ali omejitev |
| Skupina enot | Privzeta vrednost je **Skupina časovnih enot** in se ne da spremeniti. | Ni priprav ali omejitev |
| Enota | Privzeta vrednost je osnovna enota ur iz skupine časovnih enot. To vrednost lahko spremenite za nakup v kateri koli enoti skupine časovnih enot, kot je dan ali teden. | Kombinacija **Vloga** in **Enota** vrednosti bodo uporabljene kot privzete ali izračunane vrednosti za **Cena na enoto** polje v vrstici računa dobavitelja. |
| Cena enote | Privzeta cena na enoto uporablja kombinacijo **Vloga** in **Enota** vrednosti iz cenika projekta, ki velja za datum transakcije v vrstici računa dobavitelja. | Če je cena za veljavni cenik projekta nastavljena v enoti, ki se razlikuje od enote v vrstici računa dobavitelja, sistem uporabi pretvorbo enote za izračun cene na enoto. |
| Delna vsota | To polje samo za branje se izračuna kot *Količina*&times;*Cena na enoto*, če so vrednosti vnesene v oba **Količina** polje in **Cena na enoto** polje. Če sta eno ali obe polji prazni, lahko v to polje vnesete vrednost. | Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek v vrstici računa dobavitelja, vključno z davki. To polje se izračuna kot *Vmesni seštevek* + *Davek od prodaje*. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
