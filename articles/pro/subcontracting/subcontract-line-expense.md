---
title: Podrobnosti podizvajalske pogodbe za kategorije stroškov
description: V tej temi je pojasnjeno, kako zapisovati podrobnosti podizvajalske pogodbe za stroške in kako polja uporabiti za beleženje odkupa časa od dobaviteljev.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9eba8b70aeb98389515ee679e4bfb1426736ee2c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591700"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Podrobnosti podizvajalske pogodbe za kategorije stroškov

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Podizvajalska pogodba v storitvi Dynamics 365 Project Operations lahko vsebuje vrstico za kategorije stroškov. Podrobnosti podizvajalske pogodbe glede kategorij stroškov vodji projekta omogočijo, da od dobaviteljev, ki jih lahko vključijo v projekt, naročajo kategorije storitev in izdelkov.

Izvedite spodnje korake in v storitvi Project Operations ustvarite vrstice podizvajalske pogodbe za kategorije stroškov.

1. V podoknu za krmarjenje izberite **Podizvajalske pogodbe**, nato pa odprite podizvajalsko pogodbo, s katero želite delati.
2. Na zavihku **Vrstice podizvajalske pogodbe** izberite **Novo** in tako ustvarite novo vrstico podizvajalske pogodbe.
3. Na strani **Hitro ustvarjanje**, in sicer v polju **Razred transakcije**, izberite možnost **Stroški** in vnesite ali izberite druge zahtevane podatke o polju.

Spodnja tabela vsebuje informacije o poljih na strani s podrobnostmi **Vrstica podizvajalske pogodbe** in strani **Hitro ustvarjanje**.

| **Polje** | **Opis** | **Funkcionalni vpliv** |
| --- | --- | --- |
| Imenu | Ime podrobnosti podizvajalske pogodbe za pomoč pri identifikaciji. | To bo prikazano kot prvi stolpec v vseh iskanjih na podlagi podrobnosti podizvajalske pogodbe. |
| Opis | Kratek opis kategorij stroškov, ki se kupujejo v podrobnostih podizvajalske pogodbe. | Brez |
|Vrsta vrstice | Privzeta vrednost tega polja je **Temelji na količini**. |Brez |
| Način obračunavanja | To je nabor možnosti, ki predstavlja dva glavna pogodbena modela, ki ju aplikacija Project Operations podpira: **Fiksna cena** in **Čas in material**. | Razpored za izdajanje računov, ki temelji na mejnikih, je na voljo za podrobnosti podizvajalske pogodbe, če je izbran način obračunavanja s fiksno ceno. |
| Razred transakcije | Privzeta vrednost tega polja je **Čas**. Če želite ustvariti vrstice podizvajalske pogodbe za nakup izdelkov, polje **Razred transakcije** nastavite na možnost **Strošek**.  | To kaže, da se podrobnosti podizvajalske pogodbe uporabljajo za evidentiranje nakupa kategorije stroškov, ki se bodo uporabljali pri projektih. |
| Kategorija transakcije | Prikaže seznam aktivnih kategorij transakcij v sistemu. |Brez |
| Zahtevani datum začetka | Vnesite datum, ko morajo biti kategorije nakupa na voljo od dobavitelja. | Zahtevani začetek se uporablja za izbiro cenika projekta iz cenikov projektov, priloženih podizvajalski pogodbi. Cena kategorije v podrobnostih podizvajalske pogodbe izhaja iz tega cenika. |
| Zahtevani konec | Vnesite datum, ko kategorije nakupa ne bodo več potrebne. | To bo uporabljeno za prikaz opozoril, ko vodja projekta te podrobnosti podizvajalske pogodbe poveže z določenimi ocenami stroškov projekta, ki so potrebne po tem datumu. |
| Naročena količina | Količina kategorije, ki jo kupite pri dobavitelju. | To bo uporabljeno za prikaz opozoril, ko vodja projekta črpa čez to količino.|
| Skupina enot | Privzeta vrednost temelji na privzeti skupini enot, ki je nastavljena za izbrano kategorijo. |Brez |
| Enota | Privzeta vrednost temelji na privzeti enoti, ki je nastavljena za izbrano kategorijo.  | Kombinacija možnosti **Kategorija** in **Enota** bo uporabljena kot privzeta ali izračunana za ceno enote za podrobnosti podizvajalske pogodbe.  |
| Cena enote | Privzeta vrednost uporablja kombinacijo možnosti **Kategorija** in **Enota** iz cen kategorij, ki so povezane s cenikom projekta, ki velja za zahtevani začetek podrobnosti podizvajalske pogodbe. |Brez |
| Delna vsota | To je polje samo za branje, ki se izračuna kot količina X cena na enoto, če vnesete vrednosti količine in cene enote. Če je prazno eno ali obe polji, lahko v to polje vnesete vrednost. |Brez |
| Prometni davek | Vnesite znesek prometnega davka. |Brez |
| Skupni znesek | Skupni znesek vrstice podizvajalske pogodbe z vključenimi davki. Vrednost tega polja je izračunana na naslednji način: delni znesek + prometni davek. |Brez |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
