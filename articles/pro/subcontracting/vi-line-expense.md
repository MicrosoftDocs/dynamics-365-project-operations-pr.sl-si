---
title: Vrstice računov prodajalca za kategorije stroškov
description: Ta tema pojasnjuje, kako zabeležiti vrstice računov prodajalca za kategorije stroškov.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579556"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Vrstice računov prodajalca za kategorije stroškov

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Račun prodajalca v Microsoftu Dynamics 365 Project Operations lahko imajo vrstice računov prodajalca za kategorije stroškov. Vodje projektov lahko uporabljajo vrstice računov prodajalca za kategorije stroškov, da zabeležijo stroške storitev, ki so nabavljene kot kategorije stroškov.

Vrstice računov prodajalca za kategorije stroškov se lahko sklicujejo na vrstico podizvajalcev za kategorije stroškov ali pa tudi ne. Če se vrstica faktur prodajalca za kategorije stroškov sklicuje na podizvajalsko pogodbo, bodo vodje projekta lahko uskladili in preverili stroške, ki so zaračunani v vrstici faktur prodajalca, s stroški, ki so zabeleženi v teh kategorijah stroškov in jih odobrijo vodje projekta na projektu.

Naslednja tabela vsebuje informacije o poljih v vrsticah računov dobavitelja za kategorije stroškov.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime vrstice računa prodajalca za pomoč pri identifikaciji. | To ime bo prikazano kot prvi stolpec v vseh iskanjih, ki temeljijo na vrsticah računov prodajalca. |
| Description | Kratek opis storitev, ki jih prodajalec zaračunava v vrstici faktur za ponudnika. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, na podlagi katere so bile storitve prvotno naročene. | Ko je za račun prodajalca izbrana podizvajalska pogodba, bodo vse vrstice na računu prodajalca podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa prodajalca, ki se sklicujejo na različne podizvajalske pogodbe. |
| Podizvajalska linija | Podizvajalska linija, na kateri so bile storitve naročene. Seznam vrstic podizvajalcev, ki jih je mogoče izbrati, je omejen na vrstice v izbrani podizvajalski pogodbi. | Ko je v vrstici računa prodajalca izbrana vrstica podizvajalcev za kategorije stroškov, privzete vrednosti za **Projekt**, **·**, in **Kategorija transakcije** polja se vnesejo iz ustreznih polj v vrstici podizvajalcev. Če ima izbrana vrstica podizvajalcev vrednosti v **Projekt**, **naloga**, in **Kategorija transakcije** polja, se vrednosti ustreznih polj v vrstici računa prodajalca ne morejo razlikovati od teh vrednosti. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa prodajalca zabeležen v projektu. |Ni priprav ali omejitev |
| Razred transakcije | Izberite **Stroški** za evidentiranje računa prodajalca za kategorijo stroškov. | Vrednost **Stroški** označuje, da se vrstica računa prodajalca uporablja za evidentiranje zneska računa za storitve, ki so bile nabavljene kot kategorije stroškov. |
| Projekt | Ime projekta, pri katerem so bile uporabljene storitve, ki se zaračunavajo. | To polje je obvezno in ga ne morete pustiti prazno. |
| opravilo, | Ime projektne naloge, za katero so bile uporabljene storitve, ki se zaračunavajo. To polje je na voljo samo, če je izbran projekt. Izbira projektne naloge je neobvezna. | Če to polje ostane prazno, lahko vodja projekta poveže vrstico računa prodajalca s stroški, ki so zabeleženi pri kateri koli nalogi projekta. Če se vrstica računa prodajalca ne sklicuje na vrstico podizvajalcev in je to polje prazno, dejanski stroški, ki jih ustvari vrstica fakture prodajalca, ne bodo povezani z nobeno nezaračunano dejansko prodajo. V tem primeru, če je nastavljeno obračunavanje na podlagi opravil, stroškov morda ne bo mogoče zaračunati končnemu kupcu. |
| Kategorija transakcije | Kategorija transakcije, ki se zaračuna. Za izbrano kategorijo transakcij je treba ustvariti ustrezno kategorijo stroškov. | Kombinacija **Kategorija transakcije** in **enota** vrednosti bodo uporabljene kot privzeta ali izračunana vrednost za **Cena na enoto** polje v vrstici računa prodajalca. |
| Količina | V vrstico računa vnesite količino, ki jo zaračuna prodajalec. |Ni priprav ali omejitev|
| Skupina enot | Privzeta vrednost se vnese na podlagi skupine enot izbrane kategorije transakcij. | Ni priprav ali omejitev |
| Enota | Privzeta vrednost je osnovna enota izbrane skupine enot. To vrednost lahko spremenite za nakup v kateri koli enoti skupine enot. | Kombinacija **Kategorija transakcije** in **enota** vrednosti bodo uporabljene kot privzeta ali izračunana vrednost za **Cena na enoto** polje v vrstici računa prodajalca. |
| Cena enote | Privzeta cena na enoto uporablja kombinacijo **Kategorija transakcije** in **enota** vrednosti iz cenika projekta, ki velja za datum transakcije v vrstici računa prodajalca. | Če je cena za veljavni cenik projekta nastavljena v enoti, ki se razlikuje od enote v vrstici računa prodajalca, sistem uporabi pretvorbo enote za izračun cene na enoto. |
| Delna vsota | To polje samo za branje se izračuna kot *Količina*&times;*Cena na enoto*, če so vrednosti vnesene v obe **Količina** polje in **Cena na enoto** polje. Če sta eno ali obe polji prazni, lahko v to polje vnesete vrednost.| Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek v vrstici računa prodajalca, vključno z davki. To polje se izračuna kot *Vmesni seštevek* + *Davek od prodaje*. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
