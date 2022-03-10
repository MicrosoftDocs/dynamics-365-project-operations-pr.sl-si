---
title: Pravilno obračunavanje osnutkov predlogov za račune projekta
description: V tej temi je pojasnjeno, kako prilagoditi z računovodstvom povezane informacije na osnutku predloga za račun.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999336"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Pravilno obračunavanje osnutkov predlogov za račune projekta

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

*Podrobnosti operacije* računov za projekte vodja projekta hrani na predračunu. V podrobnosti so vključene odločitve o urah, stroških, gradivu ali mejnikih, za katere mora biti izdan račun, cene ter izdaja zneska predujmov in honorarjev. Ko potrdite izvirni predračun, lahko operativne podrobnosti prilagodite tako, da ustvarite [popravljalni predračun](../proforma-invoicing/corrective-invoices.md) in ga potrdite.

*Računovodske podrobnosti* o računih za projekte so shranjene v računu za stranke. V podrobnosti so vključeni izračuni prometnega davka in finančne razsežnosti, uporabljene za račun. V to temo so vključeni podatki o tem, kako prilagoditi računovodske podrobnosti na osnutku predloga za račun.

## <a name="adjust-sales-tax"></a>Prilagoditev prometnega davka

Privzete skupine za obračun prometnega davka in skupine davka od prodaje izdelkov je mogoče prilagoditi neposredno v dokumentu predloga za račun. Če želite prilagoditi skupine, izberite možnost **Uredi**, nato pa v vsako vrstico predloga za račun projekta, in sicer v polje **Skupina prometnega davka** ali polje **Skupina davka od prodaje izdelkov**, vnesite novo vrednost.

## <a name="adjust-financial-dimensions"></a>Prilagoditev finančnih razsežnosti

Finančnih razsežnosti ni mogoče urejati neposredno v vrstici predloga za račun projekta. Če želite prilagoditi finančne razsežnosti v predlogu za račun projekta, sledite naslednjim korakom.

1. V predlogu za račun projekta izberite možnost **Izbriši vse** in tako odstranite vrstice v njem.

    > [!NOTE]
    > Gumb **Izbriši vse** je na voljo šele potem, ko skrbnik sistema omogoči funkcijo **Izbriši vrstice predloga za račun projekta ob uporabi aplikacije Project Operations za scenarije, ki temeljijo na virih/nezalogi** v delovnem prostoru **Upravljanje funkcij**.

2. Prilagodite finančne razsežnosti:

    - **Transakcije na računu (mejniki obračunavanja)**: pojdite na **Vsi projekti** \> **Upravljanje** \> **Transakcije na računu** in izberite mejnik, ki ga je treba prilagoditi. Nato na zavihku **Finančne razsežnosti** po potrebi posodobite vrednosti.
    - **Časovne, stroškovne in materialne transakcije**: na strani **Knjižene projektne transakcije** izberite možnost **Prilagoditev obračuna** in tako posodobite finančne razsežnosti.

3. Ko zaključite s prilagajanjem vrednosti finančnih razsežnosti, pojdite na **Upravljanje projektov in računovodstvo** \> **Periodično** \> **Integracije za aplikacijo Project Operations**, izberite možnost **Uvozi iz pripravljalne tabele** in tako zaženite periodični postopek. V ta postopek so vključene posodobljene vrednosti finančnih dimenzij za ponovno ustvarjanje vrstic predloga za račun projekta. Ko je račun za projekt knjižen, so posodobljene vrednosti uporabljene v njegovi podknjigi in glavni knjigi.
