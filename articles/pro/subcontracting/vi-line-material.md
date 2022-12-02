---
title: Vrstice računa dobavitelja za izdelke
description: Ta članek pojasnjuje, kako zapisovati vrstice računa dobavitelja za izdelke in uporabiti različna polja za beleženje nakupov izdelkov pri dobaviteljih.
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

Račun dobavitelja ima lahko v aplikaciji Microsoft Dynamics 365 Project Operations vrstice računov dobavitelja za izdelke (imenovane tudi materiali). Vodje projektov lahko uporabijo vrstice računov dobavitelja za izdelke za beleženje stroškov izdelkov, ki so bili kupljeni za projekte.

Vrstice računa dobavitelja za izdelke se lahko nanašajo na podrobnosti podizvajalske pogodbe za materiale ali pa tudi ne. Če se vrstica računa dobavitelja za izdelke sklicuje na podizvajalsko pogodbo, bodo vodje projektov lahko primerjali in preverili izdelke, za katere vrstica računa dobavitelja izda račun, glede na uporabo kupljenih izdelkov, ki so jih zabeležili in odobrili vodje projektov.

V spodnji tabeli so informacije o poljih v vrsticah računa dobavitelja za izdelke.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime podrobnosti računa dobavitelja za pomoč pri identifikaciji. | Ime bo prikazano kot prvi stolpec v vseh iskanjih, ki temeljijo na vrsticah računa dobavitelja. |
| Description | Kratek opis izdelkov, za katere dobavitelj izda račun, v vrstici računa dobavitelja. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, na podlagi katere so bili izdelki prvotno naročeni. | Ko je za račun dobavitelja izbrana podizvajalska pogodba, bodo vse vrstice na računu dobavitelja podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa dobavitelja, ki se nanašajo na različne podizvajalske pogodbe. |
| Podrobnosti podizvajalske pogodbe | Podrobnosti podizvajalske pogodbe, na podlagi katerih so bili izdelki naročeni. Seznam podrobnosti podizvajalske pogodbe, ki jih je mogoče izbrati, je omejen na vrstice na izbrani podizvajalski pogodbi. | Ko je v vrstici računa dobavitelja za izdelke izbrane podrobnosti podizvajalske pogodbe, se privzete vrednosti za polja **Projekt**, **Opravilo** in **Izdelek** vnesejo iz ustreznih polj v podrobnostih podizvajalske pogodbe. Če imajo izbrane podrobnosti podizvajalske pogodbe vrednosti v poljih **Projekt**, **Opravilo** in **Izdelek**, se vrednosti ustreznih polj v vrstici računa dobavitelja ne morejo razlikovati od teh vrednosti. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa dobavitelja zabeležen v projektu. | Ni priprav ali omejitev|
| Razred transakcije | Ko se za izdelka izdajo računi, mora biti to polje nastavljeno na **Material**. | Vrednost **Material** označuje, da se vrstica računa dobavitelja uporablja za beleženje zneska računa za materiale, ki so bili kupljeni. |
| Projekt | Ime projekta, pri katerem so bili uporabljeni izdelke, za katere se izdaja račun. | To polje je obvezno in ne sme biti prazno. |
| opravilo, | Ime opravila projekta, pri katerem so bili uporabljeni izdelke, za katere se izdaja račun. To polje je na voljo le, če je izbran projekt. Izbira opravila projekta ni obvezna. | Če je to polje prazno, lahko vodja projekta poveže vrstico računa dobavitelja s kupljenim izdelkom, ki se uporablja pri katerem koli opravilu projekta. Če se vrstica računa dobavitelja ne sklicuje na podrobnosti podizvajalske pogodbe in je to polje prazno, dejanski strošek, ki ga ustvari vrstica računa dobavitelja, ne bo povezan z morebitnimi neobračunanimi dejanskimi vrednostmi prodaje. Če je nastavljeno obračunavanje na podlagi opravil, v tem primeru končni stranki ne bo mogoče izdati računa za stroške. |
| Izbira izdelka | Izberite, ali je izdelek, za katerega se izdaja račun, obstoječ izdelek v katalogu ali gre za izdelek, ki ni v katalogu. | Privzeta vrednost se vnese iz podrobnosti podizvajalske pogodbe, ko so izbrane podrobnosti podizvajalske pogodbe. |
| izdelek, | Izberite izdelek iz kataloga. Če gre ta izdelek, ki ni v katalogu, vnesite ime izdelka. | To polje se uporablja za vnos privzetih nabavnih cen za obstoječe izdelke. |
| Količina | V to vrstico računa vnesite količino materiala, ki ga zaračuna dobavitelj. | Ni priprav ali omejitev |
| Skupina enot | Izberite skupino enot za enoto, v kateri je izražena količina, za katero je izdan račun. | Ni priprav ali omejitev |
| Enota | Privzeta vrednost je osnovna enota izbrane skupine enot. To vrednost lahko spremenite, če želite plačati v kateri koli enoti izbrane skupine enot. | Kombinacija vrednosti **Izdelek** in **Enota** bo uporabljena kot privzeta ali izračunana za vrednost polja **Cena enote** v vrstici računa dobavitelja. |
| Cena enote | Privzeta cena enote uporablja kombinacijo vrednosti **Izdelek** in **Enota**, zapisane na ceniku projekta, ki velja za datum transakcije vrstice računa dobavitelja. | Ni priprav ali omejitev |
| Delna vsota | To polje samo za branje se samodejno izračuna kot *Količina* &times; *Cena enote*, če je vnesena tako vrednost polja **Količina** kot tudi **Cena enote**. Če je prazno eno ali obe polji, lahko v to polje vnesete vrednost. | Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek vrstice računa dobavitelja z vključenimi davki. Vrednost tega polja je izračunana na naslednji način: *delni znesek* + *prometni davek*. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
