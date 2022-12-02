---
title: Pravilno obračunavanje osnutkov predlogov za račune projekta
description: V tem članku je pojasnjeno, kako prilagoditi z računovodstvom povezane informacije na osnutku predloga za račun.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921230"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Pravilno obračunavanje osnutkov predlogov za račune projekta

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

*Podrobnosti operacije* računov za projekte vodja projekta hrani na predračunu. V podrobnosti so vključene odločitve o urah, stroških, gradivu ali mejnikih, za katere mora biti izdan račun, cene ter izdaja zneska predujmov in honorarjev. Ko potrdite izvirni predračun, lahko operativne podrobnosti prilagodite tako, da ustvarite [popravljalni predračun](../proforma-invoicing/corrective-invoices.md) in ga potrdite.

*Računovodske podrobnosti* o računih za projekte so shranjene v računu za stranke. V podrobnosti so vključeni izračuni prometnega davka in finančne razsežnosti, uporabljene za račun. V ta članek so vključeni podatki o tem, kako prilagoditi računovodske podrobnosti na osnutku predloga za račun.

## <a name="adjust-sales-tax"></a>Prilagoditev prometnega davka

Privzete skupine za obračun prometnega davka in skupine davka od prodaje izdelkov je mogoče prilagoditi neposredno v dokumentu predloga za račun. Če želite prilagoditi skupine, izberite možnost **Uredi**, nato pa v vsako vrstico predloga za račun projekta, in sicer v polje **Skupina prometnega davka** ali polje **Skupina davka od prodaje izdelkov**, vnesite novo vrednost.

## <a name="adjust-financial-dimensions"></a>Prilagoditev finančnih razsežnosti

### <a name="header-dimensions"></a>Razsežnosti glave

Privzeto so finančne razsežnosti računa izpeljane iz zapisov o neobračunanih transakcijah projekta, za katere se izda račun. Vendar pa vam sistemske nastavitve omogočajo uporabo finančnih razsežnosti v glavi predlogov za račune projekta za knjiženje stanj strank. Če želite omogočiti to funkcijo, izberite **Dovoli posodobitve projektnih razsežnosti za terjatve** v zavihku **Finance** na strani **Vodenje projekta in računovodski parametri**.

Finančne razsežnosti v glavah računa je mogoče urediti, preden je račun knjižen. Na strani **Predlog za račune projekta** preklopite na pogled **Glava** in nato uredite vrednosti v zavihku **Finančne razsežnosti**.

Pogled **Glava** je na voljo šele potem, ko skrbnik sistema omogoči funkcijo **Uporabi predlog za račune projekta in obrazce dnevnikov računov s pogledom »Glava« in »Vrstice«** v delovnem prostoru **Upravljanje funkcij**. Ta funkcija zahteva posodobitev aplikacije Finance na različico 10.0.25 ali novejšo.

### <a name="line-dimensions"></a>Razsežnosti vrstic

Finančnih razsežnosti ni mogoče urejati neposredno v vrstici predloga za račun projekta. Če želite prilagoditi finančne razsežnosti v predlogu za račun projekta, sledite naslednjim korakom.

1. V predlogu za račun projekta izberite možnost **Izbriši vse** in tako odstranite vrstice v njem.

    Gumb **Izbriši vse** je na voljo šele potem, ko skrbnik sistema omogoči funkcijo **Izbriši vrstice predloga za račun projekta ob uporabi aplikacije Project Operations za scenarije, ki temeljijo na virih/nezalogi** v delovnem prostoru **Upravljanje funkcij**.

2. Prilagodite finančne razsežnosti:

    - **Transakcije na računu (mejniki obračunavanja)**: pojdite na **Vsi projekti** \> **Upravljanje** \> **Transakcije na računu** in izberite mejnik, ki ga je treba prilagoditi. Nato na zavihku **Finančne razsežnosti** po potrebi posodobite vrednosti.
    - **Časovne, stroškovne in materialne transakcije**: na strani **Knjižene projektne transakcije** izberite možnost **Prilagoditev obračuna** in tako posodobite finančne razsežnosti.

3. Ko zaključite s prilagajanjem vrednosti finančnih razsežnosti, pojdite na **Upravljanje projektov in računovodstvo** \> **Periodično** \> **Integracije za aplikacijo Project Operations**, izberite možnost **Uvozi iz pripravljalne tabele** in tako zaženite periodični postopek. V ta postopek so vključene posodobljene vrednosti finančnih dimenzij za ponovno ustvarjanje vrstic predloga za račun projekta. Ko je račun za projekt knjižen, so posodobljene vrednosti uporabljene v njegovi podknjigi in glavni knjigi.
