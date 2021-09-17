---
title: Podrobnosti podizvajalske pogodbe za kategorije stroškov
description: V tej temi je pojasnjeno, kako zapisovati podrobnosti podizvajalske pogodbe za stroške in kako polja uporabiti za beleženje odkupa časa od dobaviteljev.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323841"
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

| **Polje** |  **Opis** |
| ----------| ---------------- |
| Imenu | Ime podrobnosti podizvajalske pogodbe. |
| Opis | Kratek opis kategorij storitev in izdelkov, naročilo katerih je opredeljeno v podrobnostih podizvajalske pogodbe. |
| Vrsta vrstice | Privzeta vrednost tega polja je **Temelji na količini**.  |
| Način obračunavanja | Način obračunavanja za podrobnosti podizvajalske pogodbe. Na podlagi načina obračunavanja podrobnosti je za metodo obračunavanja s fiksno ceno na voljo razpored za izstavljanje računov, ki temelji na mejnikih.  |
| Razred transakcije | Privzeta vrednost tega polja je **Čas**. Če želite ustvariti vrstice podizvajalske pogodbe za nakup izdelkov, polje **Razred transakcije** nastavite na možnost **Stroški**. Ta vrednost polja označuje, da se podrobnosti podizvajalske pogodbe uporabljajo za evidentiranje nakupa kategorije izdelkov ali storitev, ki bodo uporabljeni v okviru projektov. |
| Kategorija transakcije | Izberite kategorijo transakcije. |
| Zahtevani datum začetka | Datum, ko morajo biti dobaviteljeve kategorije za nakup na voljo. Zahtevani datum začetka je relevanten tudi za izbiro cenika projekta iz nabora tistih cenikov, ki so priloženi podizvajalski pogodbi. Cena kategorije v podrobnosti podizvajalske pogodbe je privzeto določena na podlagi tega cenika. |
| Zahtevani datum konca | Datum, ko kategorije za nakup niso več potrebne. Na ta datum je poslano sporočilo, in sicer takrat, ko vodja projekta podrobnost pogodbe poveže z določenimi ocenami stroškov v okviru projektov, ki nosijo poznejši datum od zadevnega. |
| Naročena količina | Količina kategorij, kupljenih pri dobavitelju. Če vodja projekta prekorači količino kupljenih elementov, se prikaže opozorilo.  |
| Skupina enot | Ta vrednost polja je privzeto nastavljena na podlagi privzete skupine enot, ki je nastavljena za izbrano kategorijo. |
| Enota | Ta vrednost polja je privzeto nastavljena na podlagi privzete enote, ki je nastavljena za izbrano kategorijo. Kombinacija kategorije in enote se uporablja za privzeto določanje cene enote v podrobnosti podizvajalske pogodbe. |
| Cena enote | Vrednost polja s ceno enote je privzeto določena na podlagi kombinacije kategorije in enote iz cen kategorije, ki so povezane s cenikom projekta, ki velja za zahtevani datum začetka za vrstico podizvajalske pogodbe.  |
| Delna vsota | To polje, ki je namenjeno samo za branje, se samodejno izračuna kot cena enote po količini, če je vnesena tako vrednost količine kot vrednost cene enote. Če je najmanj eno izmed polj prazno, lahko vrednost ročno vnesete v zadevno polje.  |
| Prometni davek | Vnesite znesek prometnega davka.  |
| Skupni znesek | Skupni znesek vrstice podizvajalske pogodbe z vključenimi davki. Vrednost tega polja je izračunana na naslednji način: delni znesek + prometni davek.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
