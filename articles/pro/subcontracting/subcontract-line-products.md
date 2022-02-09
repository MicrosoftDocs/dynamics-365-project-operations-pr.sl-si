---
title: Vrstice podizvajalske pogodbe za izdelke
description: Ta tema pojasnjuje, kako zapisovati vrstice podizvajalske pogodbe za izdelke in uporabiti različna polja za beleženje nakupov izdelkov pri dobaviteljih.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cda2db2b6beafb943738b35857d091f7ad17390d
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558567"
---
# <a name="subcontract-lines-for-products"></a>Vrstice podizvajalske pogodbe za izdelke

[!include [banner](../../includes/dataverse-preview.md)]

_**Velja za:** Poenostavljeno uvajanje – od posla do izstavitve predračuna_

Podizvajalska pogodba v storitvi Dynamics 365 Project Operations lahko vsebuje vrstico podizvajalske pogodbe za izdelke. Te vrstice vodji projektov omogočajo nakup izdelkov od dobaviteljev, ki jih lahko nato uporabijo pri projektnih opravilih.

Dokončajte spodnje korake, da ustvarite vrstico podizvajalske pogodbe za izdelke v storitvi Project Operations.

1. Na strani za krmarjenje izberite **Podizvajalske pogodbe** in nato odprite podizvajalsko pogodbo, s katero želite delati. 
2. V zavihku **Vrstice podizvajalske pogodbe** izberite **+ Novo**, da ustvarite novo vrstico podizvajalske pogodbe.
3. Na strani **Hitro ustvarjanje**, v polju **Razred transakcije** izberite **Material** in vnesite ali izberite zahtevane podatke o polju. 
4. Izberite **Shrani**.

Spodnja tabela vsebuje informacije o poljih na straneh **Podrobnosti vrstice podizvajalske pogodbe** in **Hitro ustvarjanje**, saj so pomembne za nakup izdelkov.

| Polje | Opis | Funkcionalni vpliv|
| ----- | ----------- | ----------- |
| Imenu | Ime podrobnosti podizvajalske pogodbe za pomoč pri identifikaciji. |To bo prikazano kot prvi stolpec v vseh iskanjih na podlagi podrobnosti podizvajalske pogodbe.
| Opis | Kratek opis izdelkov, ki jih naročate v vrstici podizvajalske pogodbe. | Brez |
| Vrsta vrstice | Privzeta vrednost tega polja je **Temelji na količini**. |Brez |
| Način obračunavanja | To je nabor možnosti, ki predstavlja dva glavna pogodbena modela, ki ju aplikacija Project Operations podpira: **Fiksna cena** in **Čas in material**. | Na podlagi izbranega načina obračunavanja je na voljo razpored za izdajanje računov, ki temelji na mejnikih, za podrobnosti podizvajalske pogodbe z načinom obračunavanja fiksne cene. |
| Razred transakcije |Privzeta vrednost tega polja je **Čas**. Da ustvarite podrobnosti podizvajalske pogodbe za nakup izdelkov, nastavite polje **Razred transakcije** na **Gradivo**.  | To kaže, da se podrobnosti podizvajalske pogodbe uporabljajo za evidentiranje nakupa izdelkov, ki se bodo uporabljali pri projektih. |
| Izberite Izdelek | Izberite, ali se izdelek, ki ga kupujete, nahaja v katalogu izdelkov ali ne. |Brez |
| Izdelku | Izberite izdelek iz kataloga. To polje je na voljo le, kadar je polje **Izberi izdelek** nastavljeno na **V katalogu**. |Kombinacija **Izdelek** in **Enota** bo uporabljena kot privzeta ali izračunana za ceno enote za podrobnosti podizvajalske pogodbe.
| Izdelek, ki ni v katalogu | Vnesite ime izdelka, ki ni v katalogu. To polje je na voljo le, kadar je polje **Izberi izdelek** nastavljeno na **Ni v katalogu**.  |Nakupna cena se ne bo samodejno izpolnila za izdelke, ki niso v katalogu.|
| Zahtevani datum dostave | Vnesite zahtevani datum dostave za izdelke.| Ta datum se uporablja tudi za izbiro cenika projekta iz cenikov projektov, ki so priloženi podizvajalski pogodbi. Cena izdelka v vrstici podizvajalske pogodbe nato izvira iz tega cenika. |
| Pogodbeni datum dostave | Vnesite datum, ko je pogodbeno dogovorjeno, da bodo izdelki dostavljeni.  |Brez|
| Naročena količina | Vnesite količino izdelka, ki ga kupujete od dobavitelja.| To bo uporabljeno za prikaz opozoril, ko vodja projekta črpa čez to količino.|
| Skupina enot | Ta vrednost je privzeta samo za kataloške izdelke. |Ko izberete **Izdelek** in **Zahtevani datum dostave**, sistem izbere veljavni cenik glede na datum dostave. Poizvedba sorodnih izdelkov iz cenika se zažene za ustrezni izdelek. Vrednosti enote in skupine enot so privzeto nastavljene v zapisu elementa cenika. |
| Enota | Ta vrednost je privzeto nastavljena na enoto, nastavljeno v zapisu elementa cenika. Po potrebi lahko spremenite enoto.| Kombinacija izdelka in enote se uporablja za privzeto ceno na enoto v vrstici podizvajalske pogodbe za obstoječe kataloške izdelke. |
| Cena enote | Privzeta cena na enoto je kombinacija izdelka in enote iz elementov cenika, povezana s cenikom projekta, ki velja za zahtevani datum dostave vrstice podizvajalske pogodbe.  |Brez |
| Delna vsota | To polje samo za branje se izračuna kot »Količina« x »Cena na enoto«, če imata obe polji vneseni vrednosti. Če je prazno bodisi polje **Količina**, **Cena na enoto** ali pa sta prazna oba, lahko vrednost vnesete ročno.  |Brez |
| Prometni davek | Vnesite vrednost prometnega davka. |Brez |
| Skupni znesek | Ta polje z izračunom prikazuje skupni znesek vrstice podizvajalske pogodbe po vključitvi davkov. Vrednost v tem polju se izračuna kot delni znesek + davek. |Brez |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]