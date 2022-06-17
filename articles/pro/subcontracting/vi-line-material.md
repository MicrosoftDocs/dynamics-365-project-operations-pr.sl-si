---
title: Vrstice računa dobavitelja za izdelke
description: Ta članek pojasnjuje, kako zabeležiti vrstice računov prodajalca za izdelke in uporabiti različna polja za beleženje nakupov izdelkov pri prodajalcih.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 206dd36a1a1e7141678da27d76a99561ac89044b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931396"
---
# <a name="vendor-invoice-lines-for-products"></a>Vrstice računa dobavitelja za izdelke

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Račun prodajalca v Microsoftu Dynamics 365 Project Operations lahko imajo vrstice računov prodajalca za izdelke (imenovane tudi materiali). Vodje projektov lahko uporabljajo vrstice računov prodajalca za izdelke za beleženje stroškov izdelkov, ki so bili kupljeni v projektih.

Vrstice računov prodajalca za izdelke se lahko sklicujejo na vrstico podizvajalcev za materiale ali pa tudi ne. Če se vrstica faktur prodajalca za izdelke sklicuje na podizvajalsko pogodbo, bodo vodje projektov lahko uskladili in preverili izdelke, ki se fakturirajo v vrstici računov prodajalca, glede na uporabo kupljenih izdelkov, ki jih evidentirajo in odobrijo vodje projekta.

Naslednja tabela vsebuje informacije o poljih v vrsticah računov prodajalca za izdelke.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime vrstice računa prodajalca za pomoč pri identifikaciji. | To ime bo prikazano kot prvi stolpec v vseh iskanjih, ki temeljijo na vrsticah računov prodajalca. |
| Description | Kratek opis izdelkov, ki jih prodajalec zaračunava v vrstici za račun prodajalca. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, po kateri so bili izdelki prvotno naročeni. | Ko je za račun prodajalca izbrana podizvajalska pogodba, bodo vse vrstice na računu prodajalca podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa prodajalca, ki se sklicujejo na različne podizvajalske pogodbe. |
| Podizvajalska linija | Podizvajalska linija, na kateri so bili izdelki naročeni. Seznam vrstic podizvajalcev, ki jih je mogoče izbrati, je omejen na vrstice v izbrani podizvajalski pogodbi. | Ko je v vrstici računa prodajalca izbrana vrstica podizvajalcev za izdelke, se privzete vrednosti za **Projekt**, **·**, in **Izdelek** polja se vnesejo iz ustreznih polj v vrstici podizvajalcev. Če ima izbrana vrstica podizvajalcev vrednosti v **Projekt**, **·**, in **Izdelek** polja, se vrednosti ustreznih polj v vrstici računa prodajalca ne morejo razlikovati od teh vrednosti. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa prodajalca zabeležen v projektu. | Ni priprav ali omejitev|
| Razred transakcije | Ko so izdelki zaračunani, je treba to polje nastaviti na **Material**. | Vrednost **Material** označuje, da se vrstica računa prodajalca uporablja za evidentiranje zneska računa za material, ki je bil kupljen. |
| Projekt | Ime projekta, pri katerem so bili uporabljeni izdelki, ki se fakturirajo. | To polje je obvezno in ga ne morete pustiti prazno. |
| opravilo, | Ime projektne naloge, za katero so bili uporabljeni izdelki, ki se fakturirajo. To polje je na voljo samo, če je izbran projekt. Izbira projektne naloge je neobvezna. | Če to polje ostane prazno, lahko vodja projekta poveže vrstico računa prodajalca s kupljenim izdelkom, ki se uporablja pri kateri koli nalogi projekta. Če se vrstica računa prodajalca ne sklicuje na vrstico podizvajalcev in je to polje prazno, dejanski stroški, ki jih ustvari vrstica fakture prodajalca, ne bodo povezani z nobeno nezaračunano dejansko prodajo. V tem primeru, če je nastavljeno obračunavanje na podlagi opravil, stroškov ne bo mogoče zaračunati končnemu kupcu. |
| Izbira izdelka | Izberite, ali je izdelek, ki se zaračunava, obstoječi izdelek iz kataloga ali vpisani izdelek. | Privzeta vrednost se vnese iz vrstice podizvajalcev, ko je izbrana vrstica podizvajalcev. |
| izdelek, | Izberite izdelek iz kataloga. Če je izdelek vpisani izdelek, vnesite ime izdelka. | To polje se uporablja za vnos privzetih nabavnih cen za obstoječe izdelke. |
| Količina | V to vrstico računa vnesite količino materiala, ki ga zaračuna prodajalec. | Ni priprav ali omejitev |
| Skupina enot | Izberite skupino enot enote, v kateri je izražena količina, ki se obračunava. | Ni priprav ali omejitev |
| Enota | Privzeta vrednost je osnovna enota izbrane skupine enot. To vrednost lahko spremenite za plačilo v kateri koli enoti izbrane skupine enot. | Kombinacija **Izdelek** in **enota** vrednosti bodo uporabljene kot privzeta ali izračunana vrednost za **Cena na enoto** polje v vrstici računa prodajalca. |
| Cena enote | Privzeta cena na enoto uporablja kombinacijo **Izdelek** in **enota** vrednosti iz cenika projekta, ki velja za datum transakcije v vrstici računa prodajalca. | Ni priprav ali omejitev |
| Delna vsota | To polje samo za branje se izračuna kot *Količina*&times;*Cena na enoto*, če so vrednosti vnesene v obe **Količina** polje in **Cena na enoto** polje. Če sta eno ali obe polji prazni, lahko v to polje vnesete vrednost. | Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek v vrstici računa prodajalca, vključno z davki. To polje se izračuna kot *Vmesni seštevek* + *Davek od prodaje*. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
