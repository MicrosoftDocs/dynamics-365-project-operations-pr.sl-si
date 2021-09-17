---
title: Vrstice podizvajalske pogodbe za izdelke
description: Ta tema pojasnjuje, kako zapisovati vrstice podizvajalske pogodbe za izdelke in uporabiti različna polja za beleženje nakupov izdelkov pri dobaviteljih.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323706"
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

| Polje | Opis |
| ----- | ----------- |
| Imenu | Ime podrobnosti podizvajalske pogodbe. |
| Opis | Kratek opis izdelkov, ki jih naročate v vrstici podizvajalske pogodbe. |
| Vrsta vrstice | Ta vrednost polja je privzeto nastavljena na **Temelji na količini**. |
| Način obračunavanja |  Način obračunavanja za podrobnosti podizvajalske pogodbe. Za metode obračunavanja po fiksni ceni je na voljo razpored za izdajanje računov, ki temelji na mejniku. |
| Razred transakcije | Ta vrednost polja je privzeto nastavljena na **Čas**. Če želite ustvariti vrstice podizvajalske pogodbe za nakup izdelkov, v polju **Razred transakcije** izberite **Material**. Ta izbira označuje, da se vrstica podizvajalske pogodbe uporablja za evidentiranje nakupa izdelkov, ki bodo uporabljeni pri projektih. |
| Izberite Izdelek | Izberite, ali se izdelek, ki ga kupujete, nahaja v katalogu izdelkov ali ne. |
| Izdelku | Izberite izdelek iz kataloga. To polje je na voljo le, kadar je polje **Izberi izdelek** nastavljeno na **V katalogu**. |
| Izdelek, ki ni v katalogu | Vnesite ime izdelka, ki ni v katalogu. To polje je na voljo le, kadar je polje **Izberi izdelek** nastavljeno na **Ni v katalogu**.  |
| Zahtevani datum dostave | Izberite želeni datum dostave izdelkov. Ta datum se uporablja tudi za izbiro cenika projekta iz cenikov projektov, ki so priloženi podizvajalski pogodbi. Cena izdelka v vrstici podizvajalske pogodbe nato izvira iz tega cenika. |
| Pogodbeni datum dostave | Izberite datum, ki ste ga pogodbeno določili za dostavo izdelkov.  |
| Naročena količina | Vnesite količino izdelka, ki ga kupujete od dobavitelja. Če vodja projekta prekorači to količino, se prikaže opozorilo. |
| Skupina enot | Ta vrednost je privzeta samo za kataloške izdelke. Ko izberete **Izdelek** in **Zahtevani datum dostave**, sistem izbere veljavni cenik glede na datum dostave. Poizvedba sorodnih izdelkov iz cenika se zažene za ustrezni izdelek. Vrednosti enote in skupine enot so privzeto nastavljene v zapisu elementa cenika. |
| Enota | Ta vrednost je privzeto nastavljena na enoto v zapisu elementa cenika. Po potrebi lahko spremenite enoto. Kombinacija izdelka in enote se uporablja za privzeto ceno na enoto v vrstici podizvajalske pogodbe za obstoječe kataloške izdelke. |
| Cena enote | Privzeta cena na enoto je kombinacija izdelka in enote iz elementov cenika, povezana s cenikom projekta, ki velja za zahtevani datum dostave vrstice podizvajalske pogodbe.  |
| Delna vsota | To polje samo za branje se izračuna kot »Količina« x »Cena na enoto«, če imata obe polji vneseni vrednosti. Če je prazno bodisi polje **Količina**, **Cena na enoto** ali pa sta prazna oba, lahko vrednost vnesete ročno.  |
| Prometni davek | Vnesite vrednost prometnega davka. |
| Skupni znesek | Ta polje z izračunom prikazuje skupni znesek vrstice podizvajalske pogodbe po vključitvi davkov. Vrednost v tem polju se izračuna kot delni znesek + davek. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
