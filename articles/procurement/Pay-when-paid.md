---
title: Plačila dobavitelju, ki se izvedejo po prejemu plačila
description: Ta tema pojasnjuje, kako uporabiti scenarij plačila po prejemu plačila (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525394"
---
# <a name="pay-when-paid-vendor-payments"></a>Plačila dobavitelju, ki se izvedejo po prejemu plačila

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta tema pojasnjuje, kako uporabiti scenarij plačila po prejemu plačila (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Ustvarjanje naročilnice, ki ima pogoje za plačilo, ki se izvede po prejemu plačila

Če objavite račun dobavitelja in zanj veljajo pogoji za plačilo, ki se izvede po prejemu plačila, so ti pogoji prikazani v vrsticah naročilnice (PO). Če želite ustvariti naročilnico, ki vsebuje pogoje za plačilo, ki se izvede po prejemu plačila, upoštevajte te korake.

1. V storitvi Microsoft Dynamics 365 Finance upoštevajte enega od teh korakov:

    - Pomaknite se v razdelek **Nabava in iskanje dobaviteljev** \> **Naročilnice** \> **Vse naročilnice**. V podoknu za dejanja izberite **Novo**. V pogovornem oknu **Ustvari naročilnico** izberite dobavitelja, za katerega so v projektu nastavljeni pogoji za plačilo, ki se izvede po prejemu plačila, vnesite druge zahtevane informacije in nato izberite možnost **V redu**.
    - Odprite **Vodenje projekta in računovodstvo** \> **Projekti** \> **Vsi projekti**. V podoknu za dejanja v zavihku **Upravljanje** izberite **Opravilo elementa**. Izberite naročilnico. Izberite dobavitelja, za katerega so v projektu nastavljeni pogoji za plačilo, ki se izvede po prejemu plačila, in nato izberite **V redu**.

2. Na strani **Naročilnica** na zavihku za hiter dostop **Vrstice naročilnic** izberite **Dodaj vrstico** za ustvarjanje vrstice naročilnice.
3. Izberite številko elementa ali kategorijo za nabavo in vnesite druge zahtevane podrobnosti. Preglejte podrobnosti vrstice naročilnice za dobavitelja.

    Možnost **Plačilo, ki se izvede po prejemu plačila** je samodejno izbrana, vrednost v polju **Mejni odstotek plačila, ki se izvede po prejemu plačila** pa se samodejno kopira iz polja **Mejni odstotek plačila, ki se izvede po prejemu plačila** na strani **Projekti**.

4. Če za dobavitelja za vrstico naročilnice ne želite uveljaviti pogojev za plačilo, ki se izvede po prejemu plačila, počistite možnost **Plačilo, ki se izvede po prejemu plačila**. V tem primeru je polje **Mejni odstotek plačila, ki se izvede po prejemu plačila** za vrstico naročilnice ponastavljeno na **0** (nič).
5. Na strani **Naročilnica** v podoknu za dejanja v zavihku **Nakup** izberite **Potrdi** za potrditev naročilnice.
6. V podoknu za dejanja v zavihku **Račun** izberite **Račun** za ustvarjanje računa za naročilnico.

## <a name="create-a-project-invoice-proposal"></a>Ustvarjanje predloga za račune projekta

Predlogi za račune projekta se uporabljajo za izdelavo računov projekta za stranko. V scenariju za plačilo, ki se izvede po prejemu plačila (PWP), so plačila dobavitelju odvisna od plačil strank v skladu z nastavitvami PWP. Vendar pa obstajajo možnosti, ki vam omogočajo sprostitev plačil brez plačil strank. Za ustvarjanje računa projekta za stranko sledite tem korakom.

1. V aplikacijah za interakcijo s strankami odprite **Projekt** \> **Projekti** in izberite projekt.
2. V zavihku **Dejanske vrednosti** dejansko vrstico, ki jo ustvari naročilnica, ki ima vrsto transakcije **Neobračunana prodaja**. Nato izberite **Pripravljeno za izdajo računa**.
3. Odprite razdelek **Prodaja** \> **Prodaja** \> **Projektna pogodba** in izberite projektno pogodbo.
4. V podoknu za dejanja izberite **Račun** za ustvarjanje računa za stranko.
5. V aplikaciji Finance odprite razdelek **Upravljanje projektov in računovodstvo** \> **Občasno** \> **Uvoz iz pripravljalne tabele** in izberite **V redu**, da ustvarite dnevnik integracija za Project Operations.
6. Odprite razdelek **Upravljanje projektov in računovodstvo** \> **Računi za projekt** \> **Predlog za račun za projekt** in izberite **Knjiži** za knjiženje predloga za račun, ki je bil ustvarjen za projekt.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Posodobitev plačila stranke in plačilo dobavitelju

Ko dobavitelj zaključi delo na projektu in vam pošlje račun, morate pregledati stanje projekta in račune strank, da ugotovite, ali so za projekt izpolnjeni pogoji za plačilo, ki se izvede po prejemu plačila. Če so pogoji za plačilo, ki se izvede po prejemu plačila, za dobavitelja izpolnjeni, lahko na podlagi plačil strank za projekt določite, katere vrstice na računu dobavitelja izplačati. Če se odločite plačati dobavitelju, čeprav pogoji za plačilo, ki se izvede po prejemu plačila, niso bili izpolnjeni, lahko pogoje za plačilo, ki se izvede po prejemu plačila, preglasite na strani **Račun dobavitelja s plačilom, ki se izvede po prejemu plačila**.

1. V razdelku za finance odprite možnost **Upravljanje projektov in vodenje računov** \> **Projekti** \> **Vsi projekti** in izberite projekt.
2. V podoknu za dejanja izberite **Nadzor** in nato izberite **Računi dobavitelja** za prikaz vseh računov dobavitelja, ki so bili ustvarjeni za projekt.
3. Na strani **Račun dobavitelja s plačilom, ki se izvede po prejemu plačila** v iskalno polje vnesite vrednosti, da poiščete račun dobavitelja, ki ga želite pregledati, in nato izberite **Iskanje**.
4. Izberite možnost **Plačilo, ki se izvede po prejemu plačila** za ogled samo računov za plačila, ki se izvedejo po prejemu plačila.
5. Na zavihku za hitri dostop **Vrstnice računa dobavitelja** izberite vrstice, ki jih želite sprostiti za plačilo.
6. Izberite **Izplačaj plačilo dobavitelju**. Možnost **Plačilo, ki se izvede po prejemu plačila** je počiščena in vrednost polja **Pripravljeno za plačilo** se spremeni v **Da**.
