---
title: Denarni predujem
description: Ta tema vsebuje informacije o denarnih predujmih.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908598"
---
# <a name="cash-advance"></a>Denarni predujem

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Denarni predujem zaposlenim omogoča, da si pri svojem podjetju izposodijo denar pred nastankom kakršnih koli stroškov. Ko je zahtevan denarni predujem odobren in plačan, lahko zaposleni denar uporabi za morebitne poslovne stroške. 

## <a name="create-and-submit-a-cash-advance-request"></a>Ustvarjanje in oddaja zahteve za denarni predujem

1. V razdelku **Moji stroški** izberite razdelek **Denarni predujmi** > **Novo**, da ustvarite nov denarni predujem. 
2. Na strani **Nova zahteva za denarni predujem** vnesite namen stroškov in izberite stroškovno mesto.
3. Vnesite zahtevani znesek in valuto ter nato izberite možnost **Shrani**. 
4. Ko ste pripravljeni na oddajo zahteve za denarni predujem, na strani **Zahteva za denarni predujem** odprite razdelek **Potek dela** > **Pošlji**.

## <a name="modify-a-cash-advance-request"></a>Spreminjanje zahteve za denarni predujem

Zahtevo za denarni predujem lahko spremenite, če še ni bila poslana v odobritev.

1. Na zavihku **Moji stroški: denarni predujem** poiščite in izberite denarni predujem, ki ga želite urediti.
2. Izberite možnost **Uredi** in v zahtevi za denarni predujem vnesite potrebne spremembe. 
3. Izberite **Shrani in zapri**.


## <a name="view-cash-advance-requests"></a>Ogled zahtev za denarni predujem
V razdelku **Moji stroški: denarni predujmi** lahko pregledate seznam vseh denarnih predujmov, ki so v osnutku, oddani, v pregledu ali plačani. 

## <a name="approve-cash-advance-requests"></a>Odobritev zahtev za denarni predujem

Upravitelji ali uporabniki, ki so v poteku dela določeni kot odobritelji, lahko odobrijo predujme, ki so jim poslani v pregled. 

1. Za odobritev denarnega predujma v razdelku **Obdelava denarnih predujmov** izberite možnost **Denarni predujmi za moj pregled**.
2. Izberite denarni predujem, ki ga morate pregledati, in izberite možnost **Odobri**.  

## <a name="pay-cash-advances"></a>Izplačilo denarnih predujmov 
Naslednji postopek običajno izvede računovodja ali uporabnik z računovodskimi dovoljenji.

1. Če želite objaviti odobrene denarne predujme, izberite možnost **Odobreni denarni predujmi** in nato možnost **Plačilo in nakazilo**.  
2. Navedite podrobnosti dnevnika za predujme in izberite možnost **V redu**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Pošiljanje poročila o stroških glede izplačanega denarnega predujma 

Ko ustvarite in pošljete poročilo o stroških za že prejeti denarni predujem, se stroški samodejno prilagodijo temu predujmu. Če je denarni predujem večji od porabljenega zneska, morate preostala sredstva vrniti podjetju s kategorijo stroška **Vrni sredstva**. Če je denarni predujem, ki ga je izplačalo podjetje, manjši od zneska, ki ste ga porabili, vam mora podjetje povrniti razliko. 

### <a name="example"></a>Primer
Načrtujete potovanje na konferenco iz Seattla v New York. Ustvarite zahtevo za gotovinsko predplačilo v vrednosti 3000,00 USD, saj ocenjujete, da so to okvirni stroški konferenčne vozovnice, letov, hotela, obrokov in taksija. Sredstva niso izplačana, dokler vaš upravitelj te zahteve ne odobri. Ko je zahteva odobrena, je denarni predujem v vrednosti 3000,00 USD nakazan na vaš bančni račun. Nato se udeležite konference. Po končanem potovanju ugotovite, da so skupni izdatki znašali le 2790,00 USD. V polju **Način plačila** izberite možnost **Denar** in pošljite svoje stroške, ki znašajo 2790,00 USD. Poslani znesek stroškov se samodejno prilagodi denarnemu predujmu v vrednosti 3000,00 USD, ki vam je bilo posojen. Zdaj podjetju dolgujete preostanek v znesku 210,00 USD (3000,00 – 2790,00), ki ga lahko podjetju vrnete s pomočjo kategorije stroškov**Vrni sredstva**. 
