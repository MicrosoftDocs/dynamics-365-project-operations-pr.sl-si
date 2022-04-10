---
title: Denarni predujem
description: Ta tema vsebuje informacije o denarnih predujmih.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6881fc8251a2d3c7d6af0016780a92358ce63397d09b9a0cde201126cd2912cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988536"
---
# <a name="cash-advance"></a>Denarni predujem

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Denarni predujem zaposlenim omogoča, da si pri svojem podjetju izposodijo denar pred nastankom kakršnih koli stroškov. Ko je zahtevan denarni predujem odobren in plačan, lahko zaposleni denar uporabi za morebitne poslovne stroške. 

## <a name="create-and-submit-a-cash-advance-request"></a>Ustvarjanje in oddaja zahteve za denarni predujem
Če želite ustvariti nov denarni predujem in poslati zahtevo za denarni predujem, naredite to: 

1. Pod možnostjo **Moji stroški** izberite **Denarni predujmi** > **Novo**. 
2. Na strani **Nova zahteva za denarni predujem** vnesite namen stroškov in izberite stroškovno mesto.
3. Vnesite zahtevani znesek in valuto ter nato izberite možnost **Shrani**. 
4. Ko ste pripravljeni na oddajo zahteve za denarni predujem, na strani **Zahteva za denarni predujem** odprite razdelek **Potek dela** > **Pošlji**.

## <a name="modify-a-cash-advance-request"></a>Spreminjanje zahteve za denarni predujem

Zahtevo za denarni predujem lahko spremenite, če še ni bila poslana v odobritev.

1. Pod možnostjo **Moji stroški: Denarni predujmi** poiščite in izberite denarni predujem, ki ga želite urediti.
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

Ko ustvarite in pošljete poročilo o stroških za denarni predujem, ki ste ga že prejeli, se stroški samodejno prilagodijo glede na ta predujem. Če je denarni predujem večji od porabljenega zneska, morate preostala sredstva vrniti podjetju s kategorijo stroška **Vrni sredstva**. Če je denarni predujem, ki ga je plačalo podjetje, manjši od zneska, ki ste ga porabili, vam mora podjetje vrniti razliko. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Izberite denarne predujme, ki se nanašajo na vaše stroške
Preden oddate poročilo o stroških, lahko izberete denarni predujem, ki je v skladu s transakcijami stroškov v poročilu. Če želite uporabljati to funkcijo, morate v delovnem prostoru **Upravljanje funkcij** omogočiti naslednji dve funkciji:

  - Prenovljena poročila o stroških
  - Sposobnost preslikave denarnih predujmov v vrstice stroškov
 
 Ko so te funkcije omogočene:
 
  - Za vsako vrstico stroškov lahko dodate enega ali več denarnih predujmov.
  - Razpoložljivo stanje denarnega predujma je v realnem času vidno, ko se shrani poročilo o stroških. To vam omogoča obdelavo transakcij stroškov in hkrati vrnitev transakcij gotovine.
  - Za eno transakcijo stroškov lahko izberet več denarnih predujmov.
  - Podatki o uskladitvi denarnega predujma so na voljo prek poizvedbe. 
 
Če teh funkcij ne uporabljate, bo funkcionalnost ostala nespremenjena, obstoječi denarni predujmi pa se bodo samodejno zmanjšali, ko bodo stroški poslani.

### <a name="example"></a>Primer 
Načrtujete potovanje iz Seattla v New York na konferenco. Zahtevo za denarni predujem za 3000,00 USD ustvarite na podlagi ocenjenih stroškov vstopnice za konferenco, letov, hotela, obrokov in taksija. Če vodja te zahteve ne odobri, plačilo ni izvršeno. Ko je zahteva odobrena, je denarni predujem v vrednosti 3000,00 USD nakazan na vaš bančni račun. Nato se udeležite konference. Po končanem potovanju ugotovite, da so skupni izdatki znašali le 2790,00 USD. V polju **Način plačila** izberite **Gotovina** in navedite svoje stroške za 2790,00 USD. Poslani znesek stroškov se samodejno prilagodi denarnemu predujmu v vrednosti 3000,00 USD, ki vam je bilo posojen. Razlika na računu je zdaj 210,00 USD (3000,00 - 2790,00), ki jo podjetju lahko vrnete z uporabo kategorije stroška **Vračilo gotovine**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
