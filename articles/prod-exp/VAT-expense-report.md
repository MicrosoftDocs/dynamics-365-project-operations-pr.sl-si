---
title: Izterjava DDV
description: V tej temi je pojasnjeno, kako prejemati vračila za transakcije z davkom na dodano vrednost (DDV).
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ab390e399e0c709cd72219f0a1d85116b33b84e
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683006"
---
# <a name="vat-recovery"></a>Izterjava DDV 

Če želi podjetje ali organizacija prejeti vračila za upravičene transakcije z davkom na dodano vrednost (DDV), mora prepoznati, zbrati, preveriti in predložiti natančne podatke. Ta postopek vključuje več nalog in glede na velikost vašega podjetja lahko vključuje več zaposlenih ali vlog.

Za izterjavo DDV z uporabo mobilnega delovnega prostora za upravljanje stroškov morajo biti izpolnjeni naslednji predpogoji:

- Za države/regije, ki so razvrščene v kategorije stroškov, je treba ustvariti kode davkov.
- Za vsako kodo davka je treba ustvariti skupino prometnega davka.
- Za vsako skupino prometnega davka je treba ustvariti tudi kodo prometnega davka za element.

Po izpolnitvi predpogojev zaposleni upoštevajo naslednje korake za zahtevanje vračil za transakcije z DDV.

1. V poročilo o stroških vnesite davčne podatke o transakcijah s kreditnimi karticami, da ugotovite upravičena vračila DDV.
2. Preverite, ali so vsi davčni podatki popolni, in nato objavite poročilo o stroških.
3. Stroški obdelave, ki so upravičeni za mednarodno izterjavo DDV.
4. Pošljite podatke o izterjavi DDV neodvisnemu ponudniku, da vloži zahtevek za mednarodno izterjavo.
5. Stroški obdelave za domačo izterjavo DDV.

Naslednji razdelki vsebujejo primere, ki prikazujejo, kako zaposleni v podjetju Contoso opravijo vsak korak.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>V poročilo o stroških vnesite davčne podatke o transakcijah s kreditnimi karticami, da ugotovite upravičena vračila DDV

Nancy, prodajna zastopnica podjetja Contoso s sedežem v ZDA, se je pred kratkim vrnila s službenega potovanja na področju prodaje v Združeno kraljestvo. Med potovanjem je Nancy imela nekaj osebnih stroškov na kreditni kartici za prehrano. Nancy mora zdaj pripraviti poročilo o stroških, da uskladi svoje stroške.

Ko Nancy vnese podatke v svoje poročilo o stroških, izbere **Združeno kraljestvo** v polju **Država/regija** na strani **Uredi poročilo o stroških**. Nato se seznam skupin prometnega davka filtrira, tako da prikazuje samo skupine, ki veljajo za Združeno kraljestvo. Nancy izbere skupino prometnega davka **Združeno kraljestvo 001** in nato izbere skupino prometnega davka za izdelek **Prehrana**. Nancy nato doda novo transakcijo za svojo nastanitev. Ker sta za nastanitev v Združenem kraljestvu na voljo le ena skupina prometnega davka in skupina prometnega davka za element, se te informacije samodejno vnesejo v Nancyjino poročilo o stroških.

V skladu s pravilnikom podjetja Contoso morajo vsi stroški imeti ustrezen račun. Zato Nancy po tem, ko shrani poročilo o stroških, prejme sporočilo, v katerem piše, da mora priložiti račun za vsako transakcijo, ki jo je navedla v poročilu o stroških. Nancy preveri, ali je poročilu o stroških priložila digitalno sliko vsakega potrdila o transakciji, nato pa svoje poročilo pošlje v odobritev. Nato fizične račune pošlje skupini za ekipi za zaledno obdelavo. Ta ekipa bo podatke o izterjavi DDV poslala neodvisnemu ponudniku, ki za Contoso vloži zahtevek za mednarodno izterjavo DDV.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Preverite, ali so vsi davčni podatki popolni, in nato objavite poročilo o stroških

April, koordinatorica za obveznosti v podjetju Contoso, mora pred objavo poročila o stroških vnesti vse davčne podatke, ki v njem manjkajo. Odpre stran **Podrobnosti poročila o stroških** in vidi Nancyjino odobreno poročilo o stroških. April nato odpre poročilo o stroških, da si ogleda podrobnosti transakcij. Vidi, da Nancy za eno od transakcij ni skupine prometnega davka za izdelek. Ker ta informacije ni vnesena, April ne more objaviti poročila o stroških. Zato April pogleda na stran **Davčne konfiguracije** pri upravljanju stroškov in poišče ustrezno skupino prometnega davka za element za državo/regijo in vrsto transakcije. April lahko zdaj poročilo o stroških objavi v glavni knjigi.

Ko April objavi poročilo o stroških, se ustvari delovna naloga z obnovljivim DDV. Ta delovna naloga se dodeljena članu ekipe za zaledno obdelavo. April prejme sporočilo, ki potrjuje, da je bila objava uspešna. V tem sporočilu je navedeno tudi število transakcij z DDV, ki so bile prepoznane za izterjavo.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Stroški obdelave, ki so upravičeni za mednarodno izterjavo DDV

Arnie, član Contosove ekipe za zaledno obdelavo, je odgovoren za potrjevanje, da so v poročila o stroških vključene vse potrebne informacije za izterjavo DDV. Odpre stran **Izterjava davka za stroške** in izbere poročilo o stroških, ki ga je predložila Nancy. Arnie nato preveri, ali so priloženi vsi zahtevani računi in ali so bile vnesene pravilne skupine prometnega davka in kode prometnega davka za element.

Ko Arnie od Nancy prejme fizične račune, jih preveri glede na digitalne račune in nato spremeni stanje poročila o stroških v **Pripravljeno za izterjavo**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Pošljite podatke o izterjavi DDV neodvisnemu ponudniku, da vloži zahtevek za mednarodno izterjavo

Ko je Arnie pripravljen na pošiljanje podatkov o poročilu o stroških neodvisnemu ponudniku, ki bo vložil zahtevek za izterjavo DDV, odpre stran **Izterjava davka za stroške**. Stran filtrira tako, da prikazuje samo poročila o stroških, ki so označena kot **Pripravljeno za izterjavo**. Arnie nato izbere možnost **Datoteka** &gt; **Izvozi v Excel**. Podatki o DDV iz poročil o stroških se izvozijo v delovni list Microsoft Excel. Arnie ta delovni list predloži neodvisnemu ponudniku in vključi sporočilo, v katerem je navedeno, da so fizični računi poslani prek kurirja.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Stroški obdelave za domačo izterjavo DDV

Arnie mora preveriti, ali so transakcije poročila o stroških primerne za izterjavo DDV in ali so digitalni računi priloženi poročilom. Za začetek obdelave primerih stroškov za domačo izterjavo Arnie odpre stran **Izterjava davka za stroške** in izbere poročilo o stroških, ki ga je treba preveriti. Preveri, ali so računi izdani na ime podjetja, in ne na ime zaposlenega. Za izterjavo DDV morajo biti računi izdani na ime podjetja. Arnie nato potrdi, da so bile uporabljene ustrezne skupine prometnega davka in kode prometnega davka za element.

Ko Arnie prejme fizične račune, spremeni stanje poročila o stroških na **Pripravljeno za izterjavo**. Nato lahko zahtevek vloži pri ustreznem davčnem organu. V tem primeru je ustrezen davčni organ davčna uprava ZDA (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]