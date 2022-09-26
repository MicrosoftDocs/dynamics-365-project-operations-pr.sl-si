---
title: Plačajte, ko plačate plačila prodajalca
description: Ta tema pojasnjuje, kako uporabiti scenarij plačila ob plačilu (PWP).
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
# <a name="pay-when-paid-vendor-payments"></a>Plačajte, ko plačate plačila prodajalca

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Ta tema pojasnjuje, kako uporabiti scenarij plačila ob plačilu (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Ustvarite naročilnico, ki ima pogoje PWP

Ko objavite račun od prodajalca, če za prodajalca veljajo pogoji PWP, so ti pogoji prikazani v vrsticah naročilnice (PO). Če želite ustvariti naročilnico, ki vsebuje pogoje za plačilo, ki se izvede po prejemu plačila, upoštevajte te korake.

1. notri Microsoft Dynamics 365 Finance sledite enemu od teh korakov:

    - Pomaknite se v razdelek **Nabava in iskanje dobaviteljev** \> **Naročilnice** \> **Vse naročilnice**. V podoknu za dejanja izberite **Novo**. V **Ustvarite naročilnico** pogovornem oknu izberite prodajalca, za katerega so v projektu nastavljeni pogoji PWP, vnesite druge zahtevane informacije in nato izberite **V REDU**.
    - Odprite **Vodenje projekta in računovodstvo** \> **Projekti** \> **Vsi projekti**. V podoknu z dejanji na **Upravljaj** zavihek izberite **Naloga predmeta**. Izberite naročilnico. Izberite prodajalca, za katerega so v projektu nastavljeni pogoji PWP, in nato izberite **v redu**.

2. Na **Naročilnica** stran, na **Vrstice naročilnic** Hitri zavihek, izberite **Dodaj vrstico** za ustvarjanje vrstice naročilnice.
3. Izberite številko artikla ali kategorijo nabave in vnesite druge zahtevane podrobnosti. Preglejte podrobnosti naročilnice za prodajalca.

    Možnost **Plačilo, ki se izvede po prejemu plačila** je samodejno izbrana, vrednost v polju **Mejni odstotek plačila, ki se izvede po prejemu plačila** pa se samodejno kopira iz polja **Mejni odstotek plačila, ki se izvede po prejemu plačila** na strani **Projekti**.

4. Če za dobavitelja za vrstico naročilnice ne želite uveljaviti pogojev za plačilo, ki se izvede po prejemu plačila, počistite možnost **Plačilo, ki se izvede po prejemu plačila**. V tem primeru je **Odstotek praga PWP** polje za vrstico PO bo ponastavljeno na **0** (nič).
5. Na **Naročilnica** strani, v podoknu z dejanji, na **Nakup** zavihek izberite **Potrdi** za potrditev naročila.
6. V podoknu z dejanji na **Račun** zavihek izberite **Račun** za generiranje računa za naročilo.

## <a name="create-a-project-invoice-proposal"></a>Ustvarite predlog računa za projekt

Predlogi projektnih računov se uporabljajo za izdelavo projektnih računov za stranko. V scenariju PWP so plačila dobavitelja odvisna od plačil strank v skladu z nastavitvami PWP. Vendar pa obstajajo možnosti, ki vam omogočajo sprostitev plačil brez plačil strank, kot želite. Če želite ustvariti projektni račun za stranko, sledite tem korakom.

1. V aplikacijah za sodelovanje s strankami pojdite na **Projekt** \> **Projekti** in izberite projekt.
2. Na **Dejansko** izberite dejansko vrstico, ki jo ustvari naročilnica, ki ima **Nezaračunana prodaja** vrsto transakcije. Nato izberite **Pripravljeno za račun**.
3. Pojdi do **Prodaja** \> **Prodaja** \> **Projektna pogodba** in izberite projektno pogodbo.
4. V podoknu dejanj izberite **Račun** za ustvarjanje računa stranke.
5. V Financah pojdite na **Vodenje projektov in računovodstvo** \> **Periodično** \> **Uvoz iz uprizoritvene tabele** in izberite **v redu** za ustvarjanje dnevnika integracije projektnih operacij.
6. Pojdi do **Vodenje projektov in računovodstvo** \> **Projektni računi** \> **Predlog računa za projekt** in izberite **Objavi** za knjiženje predloga računa, ki je bil ustvarjen za projekt.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Posodobitev plačila stranke in plačilo dobavitelju

Ko prodajalec zaključi svoje delo na projektu in vam pošlje račun, morate pregledati status projekta in račune strank, da ugotovite, ali so bili za projekt izpolnjeni pogoji PWP. Če so pogoji za plačilo, ki se izvede po prejemu plačila, za dobavitelja izpolnjeni, lahko na podlagi plačil strank za projekt določite, katere vrstice na računu dobavitelja izplačati. Če se odločite plačati dobavitelju, čeprav pogoji za plačilo, ki se izvede po prejemu plačila, niso bili izpolnjeni, lahko pogoje za plačilo, ki se izvede po prejemu plačila, preglasite na strani **Račun dobavitelja s plačilom, ki se izvede po prejemu plačila**.

1. V Financah pojdite na **Vodenje projektov in računovodstvo** \> **Projekti** \> **Vsi projekti** in izberite projekt.
2. V podoknu dejanj izberite **Nadzor** in nato izberite **Računi prodajalcev** za prikaz vseh računov dobaviteljev, ki so bili ustvarjeni za projekt.
3. Na strani **Račun dobavitelja s plačilom, ki se izvede po prejemu plačila** v iskalno polje vnesite vrednosti, da poiščete račun dobavitelja, ki ga želite pregledati, in nato izberite **Iskanje**.
4. Izberite **Plačaj, ko je plačano** možnost ogleda samo računov PWP.
5. Na **Vrstice računa dobavitelja** Fast Tab izberite vrstice, ki jih želite sprostiti za plačilo.
6. Izberite **Sprostite plačilo prodajalca**. Možnost **Plačilo, ki se izvede po prejemu plačila** je počiščena in vrednost polja **Pripravljeno za plačilo** se spremeni v **Da**.
