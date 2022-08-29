---
title: Vrstice računa dobavitelja za izdelke
description: V tem članku je razloženo, kako zabeležiti vrstice računa dobavitelja za izdelke in uporabiti različna polja za beleženje nakupov izdelkov od prodajalcev.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261579"
---
# <a name="vendor-invoice-lines-for-products"></a>Vrstice računa dobavitelja za izdelke

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Račun dobavitelja v Microsoftu Dynamics 365 Project Operations ima lahko vrstice računov dobavitelja za izdelke (imenovane tudi materiali). Vodje projektov lahko uporabijo vrstice računov dobaviteljev za izdelke za beleženje stroškov izdelkov, ki so bili kupljeni na projektih.

Vrstice računa dobavitelja za izdelke se lahko nanašajo na podizvajalsko vrstico za materiale ali pa tudi ne. Če se vrstica računa dobavitelja za izdelke sklicuje na podizvajalsko pogodbo, bodo vodje projektov lahko primerjali in preverili izdelke, ki jih fakturira vrstica računa dobavitelja, glede na uporabo kupljenih izdelkov, ki so jih zabeležili in odobrili vodje projektov.

Naslednja tabela vsebuje informacije o poljih v vrsticah računa dobavitelja za izdelke.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime vrstice računa dobavitelja za pomoč pri identifikaciji. | To ime bo prikazano kot prvi stolpec pri vseh iskanjih, ki temeljijo na vrsticah računa dobavitelja. |
| Description | Kratek opis izdelkov, ki jih prodajalec fakturira v vrstici računa dobavitelja. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, na podlagi katere so bili izdelki prvotno naročeni. | Ko je za račun dobavitelja izbrana podizvajalska pogodba, bodo vse vrstice na računu dobavitelja podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa dobavitelja, ki se nanašajo na različne podizvajalske pogodbe. |
| Podizvajalska linija | Podizvajalska linija, na kateri so bili naročeni izdelki. Seznam podizvajalskih postavk, ki jih je mogoče izbrati, je omejen na postavke na izbrani podizvajalski pogodbi. | Ko je v vrstici računa dobavitelja za izdelke izbrana podizvajalska vrstica, se privzete vrednosti za **Projekt**, **·**, in **Izdelek** polja se vnesejo iz ustreznih polj v vrstici podizvajalca. Če ima izbrana podizvajalska vrstica vrednosti v **Projekt**, **·**, in **Izdelek** polj, se vrednosti ustreznih polj v vrstici računa dobavitelja ne morejo razlikovati od teh vrednosti. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa dobavitelja zabeležen v projektu. | Ni priprav ali omejitev|
| Razred transakcije | Ko se izdelki fakturirajo, mora biti to polje nastavljeno na **Material**. | Vrednost **Material** označuje, da se vrstica računa dobavitelja uporablja za beleženje zneska računa za materiale, ki so bili kupljeni. |
| Projekt | Ime projekta, pri katerem so bili uporabljeni izdelki, za katere se izda račun. | To polje je obvezno in ne sme biti prazno. |
| opravilo, | Ime projektne naloge, pri kateri so bili uporabljeni izdelki, ki se fakturirajo. To polje je na voljo le, če je izbran projekt. Izbira projektne naloge je neobvezna. | Če je to polje prazno, lahko vodja projekta poveže vrstico računa dobavitelja s kupljenim izdelkom, ki se uporablja pri kateri koli nalogi projekta. Če se vrstica računa dobavitelja ne sklicuje na vrstico podizvajalca in je to polje prazno, dejanski strošek, ki ga ustvari vrstica računa dobavitelja, ne bo povezan z nobenimi neobračunanimi dejanskimi vrednostmi prodaje. V tem primeru, če je nastavljeno obračunavanje na podlagi nalog, stroškov ne bo mogoče zaračunati končnemu kupcu. |
| Izbira izdelka | Izberite, ali je izdelek, ki se fakturira, obstoječi izdelek iz kataloga ali izdelek za vpis. | Privzeta vrednost se vnese iz podizvajalske vrstice, ko je izbrana podizvajalska vrstica. |
| izdelek, | Izberite izdelek iz kataloga. Če je izdelek izdelek za vpis, vnesite ime izdelka. | To polje se uporablja za vnos privzetih nabavnih cen za obstoječe izdelke. |
| Količina | V to vrstico računa vnesite količino materiala, ki jo fakturira prodajalec. | Ni priprav ali omejitev |
| Skupina enot | Izberite skupino enot enote, v kateri je izražena količina, ki se fakturira. | Ni priprav ali omejitev |
| Enota | Privzeta vrednost je osnovna enota izbrane skupine enot. To vrednost lahko spremenite za plačilo v kateri koli enoti izbrane skupine enot. | Kombinacija **Izdelek** in **Enota** vrednosti bodo uporabljene kot privzete ali izračunane vrednosti za **Cena na enoto** polje v vrstici računa dobavitelja. |
| Cena enote | Privzeta cena na enoto uporablja kombinacijo **Izdelek** in **Enota** vrednosti iz cenika projekta, ki velja za datum transakcije v vrstici računa dobavitelja. | Ni priprav ali omejitev |
| Delna vsota | To polje samo za branje se izračuna kot *Količina*&times;*Cena na enoto*, če so vrednosti vnesene v oba **Količina** polje in **Cena na enoto** polje. Če sta eno ali obe polji prazni, lahko v to polje vnesete vrednost. | Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek v vrstici računa dobavitelja, vključno z davki. To polje se izračuna kot *Vmesni seštevek* + *Davek od prodaje*. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
