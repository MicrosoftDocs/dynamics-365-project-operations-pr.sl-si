---
title: Izterjava DDV pri upravljanju stroškov
description: Ta tema vsebuje razlago, kako prejemati vračila za upravičene transakcije z davkom na dodano vrednost (DDV).
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a840c808a76c96dd5f9dfb863c230801718c203c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001716"
---
# <a name="vat-recovery-in-expense-management"></a>Izterjava DDV pri upravljanju stroškov

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/manjkajoči zalogi_

Če želi podjetje ali organizacija prejeti vračila za upravičene transakcije z davkom na dodano vrednost (DDV), mora prepoznati, zbrati, preveriti in predložiti natančne podatke. Ta postopek vključuje več nalog in glede na velikost vašega podjetja lahko vključuje več zaposlenih ali vlog.

Za izterjavo DDV v modulu **Upravljanje stroškov** morajo biti izpolnjeni naslednji predpogoji:

- Za države/regije, ki so razvrščene v kategorije stroškov, je treba ustvariti kode davkov.
- Za vsako kodo davka je treba ustvariti skupino prometnega davka.
- Za vsako skupino prometnega davka je treba ustvariti tudi kodo prometnega davka za element.

Po izpolnitvi predpogojev je treba izvesti naslednje korake za zahtevanje vračil za transakcije z DDV.

1. V poročilo o stroških vnesite davčne podatke o transakcijah s kreditnimi karticami, da ugotovite upravičena vračila DDV.
2. Preverite, ali so vsi davčni podatki popolni, in nato objavite poročilo o stroških.
3. Stroški obdelave, ki so upravičeni za mednarodno izterjavo DDV.
4. Pošljite podatke o izterjavi DDV neodvisnemu ponudniku, da vloži zahtevek za mednarodno izterjavo.
5. Stroški obdelave za domačo izterjavo DDV.

V naslednjih razdelkih so primeri, ki kažejo, kako zaposleni v podjetju Contoso opravijo vsak korak.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Vnašanje davčnih podatkov o transakcijah s kreditnimi karticami, da se ugotovijo upravičena vračila DDV

Nancy, prodajna zastopnica podjetja Contoso, ki se nahaja v ZDA, se je pred kratkim vrnila s prodajnega potovanja v Združeno kraljestvo. Med potovanjem je Nancy imela nekaj osebnih stroškov na kreditni kartici za prehrano. Nancy mora zdaj pripraviti poročilo o stroških, da bo uskladila stroške.

Ko Nancy vnese podatke v poročilo o stroških, izbere **Združeno kraljestvo** v polju **Država/regija** na strani **Uredi poročilo o stroških**. Nato se seznam skupin prometnega davka filtrira, tako da prikazuje samo skupine, ki veljajo za Združeno kraljestvo. Nancy izbere skupino prometnega davka **Združeno kraljestvo 001** in nato izbere skupino prometnega davka za izdelek **Prehrana**. Nancy nato doda novo transakcijo za nastanitev. Ker sta na voljo le ena skupina prometnega davka in skupina prometnega davka za izdelek za Združeno kraljestvo, se te informacije samodejno vnesejo v Nancyjino poročilo o stroških.

Na podlagi pravilnika podjetja Contoso morajo imeti vsi stroški ustrezen račun. Zato Nancy po tem, ko shrani poročilo o stroških, prejme sporočilo, v katerem piše, da mora priložiti račun za vsako transakcijo, ki jo je navedla v poročilu o stroških. Nancy preveri, ali je poročilu o stroških priložila digitalno sliko vsakega potrdila o transakciji, nato pa svoje poročilo pošlje v odobritev. Nato fizične račune pošlje skupini za ekipi za zaledno obdelavo. Ta skupina bo podatke o izterjavi DDV-ja poslala neodvisnemu dobavitelju, ki vloži mednarodne izterjave DDV-ja za podjetje Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Preverjanje davčnih podatkov in objavljanje poročila o stroških

Preden lahko April, koordinatorka za obveznosti pri podjetju Contoso, objavi poročilo o stroških, mora vnesti vse manjkajoče davčne podatke. Odpre stran **Podrobnosti poročila o stroških** in vidi Nancyjino odobreno poročilo o stroških. April nato odpre poročilo o stroških, da si ogleda podrobnosti transakcij. Vidi, da Nancy za eno od transakcij ni skupine prometnega davka za izdelek. Ker ta informacije ni vnesena, April ne more objaviti poročila o stroških. Zato pogleda na stran **Davčne konfiguracije** pri upravljanju stroškov in poišče ustrezno skupino prometnega davka za izdelek za državo/regijo in vrsto transakcije. April lahko zdaj poročilo o stroških objavi v glavni knjigi.

Ko April objavi poročilo o stroških, se ustvari delovna naloga z obnovljivim DDV. Ta delovna naloga se dodeljena članu ekipe za zaledno obdelavo. April prejme sporočilo, ki potrjuje, da je bila objava uspešna. V tem sporočilu je navedeno tudi število transakcij z DDV, ki so bile prepoznane za izterjavo.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Stroški obdelave, ki so upravičeni za mednarodno izterjavo DDV

Arnie, član zaledne ekipe za obdelavo pri podjetju Contoso, je odgovoren za preverjanje, ali so vsi potrebni podatki za izterjavo DDV-ja vključeni v poročila o stroških. Odpre stran **Izterjava davka za stroške** in izbere poročilo o stroških, ki ga je predložila Nancy. Arnie nato preveri, ali so priloženi vsi zahtevani računi in ali so bile vnesene pravilne skupine prometnega davka in kode prometnega davka za element.

Ko Arnie od Nancy prejme fizične račune, jih preveri glede na digitalne račune in nato spremeni stanje poročila o stroških v **Pripravljeno za izterjavo**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Pošiljanje podatkov za izterjavo DDV neodvisnemu ponudniku

Ko je Arnie pripravljen na pošiljanje podatkov o poročilu o stroških neodvisnemu ponudniku, ki bo vložil zahtevek za izterjavo DDV, odpre stran **Izterjava davka za stroške**. Stran filtrira tako, da prikazuje samo poročila o stroških, ki so označena kot **Pripravljeno za izterjavo**. Arnie nato izbere možnost **Datoteka** &gt; **Izvozi v Excel**. Podatki o DDV iz poročil o stroških se izvozijo v delovni list Microsoft Excel. Arnie ta delovni list predloži neodvisnemu ponudniku in vključi sporočilo, v katerem je navedeno, da so fizični računi poslani prek kurirja.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Stroški obdelave za domačo izterjavo DDV

Arnie mora preveriti, ali so transakcije poročila o stroških primerne za izterjavo DDV in ali so digitalni računi priloženi poročilom. Za začetek obdelave primerih stroškov za domačo izterjavo Arnie odpre stran **Izterjava davka za stroške** in izbere poročilo o stroških, ki ga je treba preveriti. Preveri, ali so računi izdani na ime podjetja, in ne na ime zaposlenega. (Za izterjavo DDV morajo biti računi izdani na ime podjetja.) Arnie nato preveri, ali so priloženi vsi zahtevani računi in ali so bile vnesene pravilne skupine prometnega davka in kode prometnega davka za element.

Ko Arnie prejme fizične račune, spremeni stanje poročila o stroških na **Pripravljeno za izterjavo**. Nato lahko zahtevek vloži pri ustreznem davčnem organu. V tem primeru je ustrezen davčni organ davčna uprava ZDA (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]