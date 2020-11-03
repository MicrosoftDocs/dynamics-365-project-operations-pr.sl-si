---
title: Nastavitev in uporaba plačil dobavitelju, ki se izvedejo po prejemu plačila
description: Ta tema razlaga, kako ustvariti pogoje za plačilo, ki se izvede po prejemu plačila (PWP), da lahko dobavitelju izplačate delna plačila na podlagi plačil, ki jih prejmete od strank.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084735"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Nastavitev in uporaba plačil dobavitelju, ki se izvedejo po prejemu plačila

[!include [banner](../includes/banner.md)]

Ko dobavitelju odobrite, da dela kot podizvajalec, boste morda želeli zadržati plačilo dobavitelju, dokler vam stranka ne plača za projekt. V tem primeru lahko nastavite pogoje za plačilo, ki se izvede po prejemu plačila (PWP), ko skupaj z dobaviteljem nastavite naročilnico (PO).

Na primer, ko stranka plača določen znesek na računu projekta, lahko izplačate del zneska računa dobavitelja ali celoten znesek. Preprosto nastavite pogoje za plačilo, ki se izvede po prejemu plačila, ki določajo, da boste dobavitelju izplačali plačilo, ko boste od stranke prejeli odstotek povezanega plačila. Če od stranke prejmete delno plačilo, lahko ročno izplačate nekatere povezane račune prodajalcev za plačilo.

Naslednji primer opisuje postopek, ko se uporabljajo pogoji za plačilo, ki se izvede po prejemu plačila.

## <a name="example"></a>Primer

Vaša organizacija se strinja, da bo stranki zagotovila 100 računalnikov z nameščeno programsko opremo po ceni 150,00 ameriških dolarjev (USD) na računalnik. Nato najamete dobavitelja, ki vam priskrbi računalnike z nameščeno programsko opremo. V skladu z dogovorom mora stranka odobriti kakovost računalnikov, preden plača vaši organizaciji. Pravilnik vaše organizacije je, da se plačilo dobavitelju ne izplača, dokler od stranke ne prejmete plačila. Zato projekt nastavite tako, da je odstotek plačilo, ki se izvede po prejemu plačila, 100-odstotni.

Dobavitelj vam pošlje 100 računalnikov, v katerih je nameščena programska oprema, skupaj z računom za 10.000,00 USD. Ker so za vaš projekt nastavljeni pogoji za plačilo, ki se izvede po prejemu plačila, dobavitelju ne plačate po prejemu računalnikov. Namesto tega računalnike pošljete stranki skupaj z računom za 15.000,00. Stranka pregleda računalnike in odobri celoten znesek računa projekta.

Ko od stranke prejmete celotno plačilo, plačate dobavitelju 10.000,00, celotni znesek računa dobavitelja.

## <a name="set-up-pwp-terms-for-a-project"></a>Nastavitev pogojev za plačilo, ki se izvede po prejemu plačila, za projekt

Ko za projekt nastavite pogoje za plačilo, ki se izvede po prejemu plačila, morate v odstotkih določiti najnižji znesek, ki vam ga mora stranka plačati za projekt, preden boste plačali dobavitelju. Mejna vrednost se samodejno izračuna na računih strank za projekt. Če želite za pogoje za plačilo, ki se izvede po prejemu plačila, nastaviti mejni odstotek, upoštevajte te korake.

1. Odprite **Vodenje projekta in računovodstvo** \> **Projekti** \> **Vsi projekti**.
2. Poiščite in odprite projekt, za katerega želite nastaviti pogoje za plačilo, ki se izvede po prejemu plačila.
3. Na zavihku za hitri dostop **Pogodbe dobaviteljev** izberite **Dodaj vrstico**.
3. V polju **Koda kupca** izberite eno od naslednjih možnosti:

    - **Tabela** – pogoji za plačilo, ki se izvede po prejemu plačila, veljajo za enega dobavitelja.
    - **Skupina** – pogoji za plačilo, ki se izvede po prejemu plačila, veljajo za vse dobavitelje v skupini dobaviteljev.
    - **Vse** – pogoji za plačilo, ki se izvede po prejemu plačila, veljajo za vse dobavitelje.

4. Če ste v prejšnjem koraku izbrali možnost **Tabela** ali **Skupina** , v polju **Dobavitelj/skupina dobaviteljev** izberite dobavitelja ali skupino dobaviteljev, za katere veljajo pogoji za plačilo, ki se izvede po prejemu plačila. Če ste v prejšnjem koraku izbrali možnost **Vse** , polja **Dobavitelj/skupina dobaviteljev** ni mogoče urejati.
5. Če so za dobavitelja v projektu nastavljeni pogoji zadržanja, v polju **Pogoji zadržanja plačila dobavitelju** izberite ID pravila za pogoje zadržanja.
6. V polju **Mejni odstotek plačila, ki se izvede po prejemu plačila** vnesite mejni odstotek za projekt. Odstotek, ki ga vnesete za projekt, določa najnižji znesek, ki vam ga mora stranka plačati, preden boste plačali dobavitelju.

## <a name="create-a-po-that-has-pwp-terms"></a>Ustvarjanje naročilnice, ki vsebuje pogoje za plačilo, ki se izvede po prejemu plačila

Če objavite račun dobavitelja in zanj veljajo pogoji za plačilo, ki se izvede po prejemu plačila, so ti pogoji prikazani v vrsticah naročilnice. Če želite ustvariti naročilnico, ki vsebuje pogoje za plačilo, ki se izvede po prejemu plačila, upoštevajte te korake.

1. Pomaknite se v razdelek **Nabava in iskanje dobaviteljev** \> **Naročilnice** \> **Vse naročilnice**.
2. V podoknu za dejanja izberite **Novo**. Nato v pogovornem oknu **Ustvarjanje naročilnice** vnesite zahtevane podatke in izberite **V redu**.

    Ali pa odprite obstoječo naročilnico na strani s seznamom **Vse naročilnice**.

4. Na strani **Naročilnica** na zavihku za hitri dostop **Vrstice naročilnic** , preglejte podrobnosti vrstice naročilnice za dobavitelja. Možnost **Plačilo, ki se izvede po prejemu plačila** je samodejno izbrana, vrednost v polju **Mejni odstotek plačila, ki se izvede po prejemu plačila** pa se samodejno kopira iz polja **Mejni odstotek plačila, ki se izvede po prejemu plačila** na strani **Projekti**.
6. Če za dobavitelja za vrstico naročilnice ne želite uveljaviti pogojev za plačilo, ki se izvede po prejemu plačila, počistite možnost **Plačilo, ki se izvede po prejemu plačila**. V tem primeru je polje **Mejni odstotek plačila, ki se izvede po prejemu plačila** za vrstico naročilnice ponastavljeno na 0 (nič).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Posodobitev plačila stranke in plačilo dobavitelju

Ko dobavitelj zaključi delo na projektu in vam pošlje račun, morate pregledati stanje projekta in račune strank, da ugotovite, ali so za projekt izpolnjeni pogoji za plačilo, ki se izvede po prejemu plačila. Če so pogoji za plačilo, ki se izvede po prejemu plačila, za dobavitelja izpolnjeni, lahko na podlagi plačil strank za projekt določite, katere vrstice na računu dobavitelja izplačati. Če se odločite plačati dobavitelju, čeprav pogoji za plačilo, ki se izvede po prejemu plačila, niso bili izpolnjeni, lahko pogoje za plačilo, ki se izvede po prejemu plačila, preglasite na strani **Račun dobavitelja s plačilom, ki se izvede po prejemu plačila**.

1. Pomaknite se v razdelek **Vodenje projektov in računovodstvo** \> **Poizvedbe in poročila** \> **Poizvedbe o zadrževanju** \> **Račun dobavitelja s plačilom, ki se izvede po prejemu plačila**.
2. Na strani **Račun dobavitelja s plačilom, ki se izvede po prejemu plačila** v iskalno polje vnesite vrednosti, da poiščete račun dobavitelja, ki ga želite pregledati, in nato izberite **Iskanje**.
3. Na zavihku za hitri dostop **Vrstnice računa dobavitelja** izberite vrstice, ki jih želite spremeniti.
4. Če so pogoji za **plačilo, ki se izvede po prejemu plačila** , za vrstico računa izpolnjeni, izberite **Izplačaj plačilo dobavitelju**. Možnost **Plačilo, ki se izvede po prejemu plačila** je počiščena in vrednost polja **Pripravljeno za plačilo** se spremeni v **Da**.
