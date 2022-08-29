---
title: Vrstice računa dobavitelja za kategorije stroškov
description: V tem članku je razloženo, kako zabeležiti vrstice računa dobavitelja za kategorije stroškov.
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

Račun dobavitelja v Microsoftu Dynamics 365 Project Operations lahko ima vrstice računa dobavitelja za kategorije stroškov. Vodje projektov lahko uporabijo vrstice računa dobavitelja za kategorije stroškov za beleženje stroškov storitev, ki so nabavljene kot kategorije stroškov.

Vrstice računa dobavitelja za kategorije stroškov se lahko nanašajo na podizvajalsko vrstico za kategorije stroškov ali pa tudi ne. Če se vrstica računa dobavitelja za kategorije stroškov sklicuje na podizvajalsko pogodbo, bodo vodje projektov lahko primerjali in preverili stroške, ki jih fakturira vrstica računa dobavitelja, s stroški, ki so zabeleženi v teh kategorijah stroškov in so jih odobrili vodje projektov v projektu.

Naslednja tabela vsebuje informacije o poljih v vrsticah računa dobavitelja za kategorije stroškov.

| Polje | Description | Funkcionalni vpliv |
| --- | --- | --- |
| Imenu | Ime vrstice računa dobavitelja za pomoč pri identifikaciji. | To ime bo prikazano kot prvi stolpec pri vseh iskanjih, ki temeljijo na vrsticah računa dobavitelja. |
| Description | Kratek opis storitev, ki jih prodajalec fakturira v vrstici računa dobavitelja. | Ni priprav ali omejitev |
| Podizvajalska pogodba | Podizvajalska pogodba, na podlagi katere so bile storitve prvotno naročene. | Ko je za račun dobavitelja izbrana podizvajalska pogodba, bodo vse vrstice na računu dobavitelja podedovale to izbiro. Račun dobavitelja ne sme vsebovati vrstic računa dobavitelja, ki se nanašajo na različne podizvajalske pogodbe. |
| Podizvajalska linija | Podizvajalska linija, na kateri so bile naročene storitve. Seznam podizvajalskih postavk, ki jih je mogoče izbrati, je omejen na postavke na izbrani podizvajalski pogodbi. | Ko je izbrana podizvajalska vrstica v vrstici računa dobavitelja za kategorije stroškov, privzete vrednosti za **Projekt**, **·**, in **Kategorija transakcije** polja se vnesejo iz ustreznih polj na podizvajalski vrstici. Če ima izbrana podizvajalska vrstica vrednosti v **Projekt**, **naloga**, in **Kategorija transakcije** polj, se vrednosti ustreznih polj v vrstici računa dobavitelja ne morejo razlikovati od teh vrednosti. |
| Datum transakcije | Datum, ko bo dejanski strošek vrstice računa dobavitelja zabeležen v projektu. |Ni priprav ali omejitev |
| Razred transakcije | Izberite **Stroški** za beleženje računa dobavitelja za kategorijo stroškov. | Vrednost **Stroški** označuje, da se vrstica računa dobavitelja uporablja za beleženje zneska računa za storitve, ki so bile nabavljene kot kategorije stroškov. |
| Projekt | Ime projekta, pri katerem so bile uporabljene storitve, ki se fakturirajo. | To polje je obvezno in ne sme biti prazno. |
| opravilo, | Ime projektne naloge, za katero so bile uporabljene storitve, ki se fakturirajo. To polje je na voljo le, če je izbran projekt. Izbira projektne naloge je neobvezna. | Če je to polje prazno, lahko vodja projekta poveže vrstico računa dobavitelja s stroški, ki so zabeleženi pri kateri koli nalogi projekta. Če se vrstica računa dobavitelja ne sklicuje na vrstico podizvajalca in je to polje prazno, dejanski strošek, ki ga ustvari vrstica računa dobavitelja, ne bo povezan z nobenimi neobračunanimi dejanskimi vrednostmi prodaje. V tem primeru, če je nastavljeno obračunavanje na podlagi nalog, stroškov morda ne bo mogoče zaračunati končnemu kupcu. |
| Kategorija transakcije | Kategorija transakcije, ki se fakturira. Za izbrano kategorijo transakcij je treba ustvariti ustrezno kategorijo stroškov. | Kombinacija **Kategorija transakcije** in **Enota** vrednosti bodo uporabljene kot privzete ali izračunane vrednosti za **Cena na enoto** polje v vrstici računa dobavitelja. |
| Količina | V vrstico računa vnesite količino, ki jo fakturira prodajalec. |Ni priprav ali omejitev|
| Skupina enot | Privzeta vrednost se vnese glede na skupino enot izbrane kategorije posla. | Ni priprav ali omejitev |
| Enota | Privzeta vrednost je osnovna enota izbrane skupine enot. To vrednost lahko spremenite za nakup v kateri koli enoti skupine enot. | Kombinacija **Kategorija transakcije** in **Enota** vrednosti bodo uporabljene kot privzete ali izračunane vrednosti za **Cena na enoto** polje v vrstici računa dobavitelja. |
| Cena enote | Privzeta cena na enoto uporablja kombinacijo **Kategorija transakcije** in **Enota** vrednosti iz cenika projekta, ki velja za datum transakcije v vrstici računa dobavitelja. | Če je cena za veljavni cenik projekta nastavljena v enoti, ki se razlikuje od enote v vrstici računa dobavitelja, sistem uporabi pretvorbo enote za izračun cene na enoto. |
| Delna vsota | To polje samo za branje se izračuna kot *Količina*&times;*Cena na enoto*, če so vrednosti vnesene v oba **Količina** polje in **Cena na enoto** polje. Če sta eno ali obe polji prazni, lahko v to polje vnesete vrednost.| Ni priprav ali omejitev |
| Prometni davek | Vnesite znesek prometnega davka. | Ni priprav ali omejitev |
| Skupni znesek | Skupni znesek v vrstici računa dobavitelja, vključno z davki. To polje se izračuna kot *Vmesni seštevek* + *Davek od prodaje*. | Ni priprav ali omejitev |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
