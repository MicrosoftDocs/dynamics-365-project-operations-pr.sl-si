---
title: Vrstice računa dobavitelja za čas
description: V tem članku je razloženo, kako zabeležiti vrstice računov prodajalca za časovne stroške, ki jih vložijo podizvajalci.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927578"
---
# <a name="vendor-invoice-lines-for-time"></a>Vrstice računa dobavitelja za čas

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Račun prodajalca v Microsoftu Dynamics 365 Project Operations lahko imajo vrstice računov prodajalca za čas. Vodje projektov lahko uporabljajo vrstice računov prodajalca za čas za beleženje stroškov časa podizvajalcev na projektih.

Vrstice faktur prodajalca za čas se lahko sklicujejo na vrstico podizvajalcev za čas ali pa tudi ne. Če se vrstica računa prodajalca za čas sklicuje na podizvajalsko pogodbo, bodo vodje projektov lahko uskladili in preverili čas, ki je bil zaračunan v vrstici računov prodajalca, s časom, ki ga zabeležijo podizvajalci in odobrijo vodje projekta na projektu.

Naslednja tabela vsebuje informacije o poljih v vrsticah računa prodajalca za čas.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime vrstice računa prodajalca za pomoč pri identifikaciji. | To ime bo prikazano kot prvi stolpec v vseh iskanjih, ki temeljijo na vrsticah računov prodajalca. |
| Description | Kratek opis storitev, ki jih prodajalec zaračunava v vrstici faktur za ponudnika. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, na podlagi katere so bile storitve prvotno naročene. | Ko je za račun prodajalca izbrana podizvajalska pogodba, bodo vse vrstice na računu prodajalca podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa prodajalca, ki se sklicujejo na različne podizvajalske pogodbe. |
| Podizvajalska linija | Podizvajalska linija, na kateri so bile storitve naročene. Seznam vrstic podizvajalcev, ki jih je mogoče izbrati, je omejen na vrstice v izbrani podizvajalski pogodbi. | Ko je v vrstici računa prodajalca izbrana vrstica podizvajalcev za čas, privzete vrednosti za **Projekt**, **·**, in **Vir, ki ga je mogoče rezervirati** polja se vnesejo iz ustreznih polj v vrstici podizvajalcev. Če ima izbrana vrstica podizvajalcev vrednosti v **Projekt**, **·**, in **Možno rezervirati** polja, se vrednosti ustreznih polj v vrstici računa prodajalca ne morejo razlikovati od teh vrednosti. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa prodajalca zabeležen v projektu. | Ni priprav ali omejitev |
| Razred transakcije | Privzeta vrednost je **Čas**. | Vrednost **Čas** označuje, da se vrstica računa prodajalca uporablja za beleženje zneska računa podizvajalčevega časa. |
| Projekt | Ime projekta, pri katerem so bile uporabljene storitve, ki se zaračunavajo. | To polje je obvezno in ga ne morete pustiti prazno. |
| opravilo, | Ime projektne naloge, za katero so bile uporabljene storitve, ki se zaračunavajo. To polje je na voljo samo, če je izbran projekt. Izbira projektne naloge je neobvezna. | Če je to polje prazno, lahko vodja projekta uskladi vrstico računa prodajalca s časom, ki ga zabeležijo viri podizvajalcev pri kateri koli nalogi projekta. Če se vrstica računa prodajalca ne sklicuje na vrstico podizvajalcev in je to polje prazno, dejanski stroški, ki jih ustvari vrstica fakture prodajalca, ne bodo povezani z nobeno nezaračunano dejansko prodajo. V tem primeru, če je nastavljeno obračunavanje na podlagi opravil, stroškov morda ne bo mogoče zaračunati končnemu kupcu. |
| Vloga | Vloga virov podizvajalcev, katerih čas se zaračunava. | To polje določa vlogo, ki jo opravljajo podizvajalski viri, katerih čas je zaračunan na računu prodajalca. |
| Vir, ki ga je mogoče rezervirati | Ime podizvajalca, katerega čas se zaračunava. Izbira vira, ki ga je mogoče rezervirati, ni obvezna. | Če to polje ostane prazno, lahko vodja projekta uskladi vrstico računa prodajalca s časom, ki ga zabeleži kateri koli vir, ki pripada prodajalcu v vrstici računa prodajalca. |
| Količina | V vrstico za račun vnesite število ur, ki jih prodajalec zaračuna. |Ni priprav ali omejitev |
| Skupina enot | Privzeta vrednost je **Skupina časovnih enot** in se ne da spremeniti. | Ni priprav ali omejitev |
| Enota | Privzeta vrednost je osnovna enota ur iz skupine časovnih enot. To vrednost lahko spremenite za nakup v kateri koli enoti skupine časovnih enot, na primer dan ali teden. | Kombinacija **Vloga** in **enota** vrednosti bodo uporabljene kot privzeta ali izračunana vrednost za **Cena na enoto** polje v vrstici računa prodajalca. |
| Cena enote | Privzeta cena na enoto uporablja kombinacijo **Vloga** in **enota** vrednosti iz cenika projekta, ki velja za datum transakcije v vrstici računa prodajalca. | Če je cena za veljavni cenik projekta nastavljena v enoti, ki se razlikuje od enote v vrstici računa prodajalca, sistem uporabi pretvorbo enote za izračun cene na enoto. |
| Delna vsota | To polje samo za branje se izračuna kot *Količina*&times;*Cena na enoto*, če so vrednosti vnesene v obe **Količina** polje in **Cena na enoto** polje. Če sta eno ali obe polji prazni, lahko v to polje vnesete vrednost. | Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek v vrstici računa prodajalca, vključno z davki. To polje se izračuna kot *Vmesni seštevek* + *Davek od prodaje*. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
