---
title: Pravilno obračunavanje osnutkov predlogov za račune projekta
description: V tej temi je pojasnjeno, kako prilagoditi z računovodstvom povezane informacije na osnutku predloga za račun.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bf0a3d6b97880920b133cb3b30389adf0c83111c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575094"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Pravilno obračunavanje osnutkov predlogov za račune projekta

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

*Podrobnosti operacije* računov za projekte vodja projekta hrani na predračunu. V podrobnosti so vključene odločitve o urah, stroških, gradivu ali mejnikih, za katere mora biti izdan račun, cene ter izdaja zneska predujmov in honorarjev. Ko potrdite izvirni predračun, lahko operativne podrobnosti prilagodite tako, da ustvarite [popravljalni predračun](../proforma-invoicing/corrective-invoices.md) in ga potrdite.

*Računovodske podrobnosti* o računih za projekte so shranjene v računu za stranke. V podrobnosti so vključeni izračuni prometnega davka in finančne razsežnosti, uporabljene za račun. V to temo so vključeni podatki o tem, kako prilagoditi računovodske podrobnosti na osnutku predloga za račun.

## <a name="adjust-sales-tax"></a>Prilagoditev prometnega davka

Privzete skupine za obračun prometnega davka in skupine davka od prodaje izdelkov je mogoče prilagoditi neposredno v dokumentu predloga za račun. Če želite prilagoditi skupine, izberite možnost **Uredi**, nato pa v vsako vrstico predloga za račun projekta, in sicer v polje **Skupina prometnega davka** ali polje **Skupina davka od prodaje izdelkov**, vnesite novo vrednost.

## <a name="adjust-financial-dimensions"></a>Prilagoditev finančnih razsežnosti

### <a name="header-dimensions"></a>Dimenzije glave

Finančne razsežnosti računa so privzeto izpeljane iz nezaračunanih zapisov projektnih transakcij, ki se fakturirajo. Vendar pa sistemske nastavitve omogočajo uporabo finančnih razsežnosti v glavi predlogov računov projekta za knjiženje stanja strank. Če želite omogočiti to funkcijo, izberite **Dovoli posodobitve dimenzij projekta za terjatve** na **Finance** zavihek na **Vodenje projektov in računovodski parametri** stran.

Finančne razsežnosti v glavah računov je mogoče urediti, preden je račun objavljen. Na **Predlog računa projekta** stran, preklopite na **Glava** si oglejte in nato uredite vrednosti na **Finančne razsežnosti** zavihek.

The **Glava** pogled je na voljo šele, ko skrbnik sistema omogoči **Uporabite predlog računov projekta in obrazce dnevnika računov s pogledom Glava in vrstice** značilnost v **Upravljanje funkcij** delovni prostor. Ta funkcija zahteva posodobitev Finance 10.0.25 ali novejšo.

### <a name="line-dimensions"></a>Dimenzije črt

Finančnih razsežnosti ni mogoče urejati neposredno v vrstici predloga za račun projekta. Če želite prilagoditi finančne razsežnosti v predlogu za račun projekta, sledite naslednjim korakom.

1. V predlogu za račun projekta izberite možnost **Izbriši vse** in tako odstranite vrstice v njem.

    Gumb **Izbriši vse** je na voljo šele potem, ko skrbnik sistema omogoči funkcijo **Izbriši vrstice predloga za račun projekta ob uporabi aplikacije Project Operations za scenarije, ki temeljijo na virih/nezalogi** v delovnem prostoru **Upravljanje funkcij**.

2. Prilagodite finančne razsežnosti:

    - **Transakcije na računu (mejniki obračunavanja)**: pojdite na **Vsi projekti** \> **Upravljanje** \> **Transakcije na računu** in izberite mejnik, ki ga je treba prilagoditi. Nato na zavihku **Finančne razsežnosti** po potrebi posodobite vrednosti.
    - **Časovne, stroškovne in materialne transakcije**: na strani **Knjižene projektne transakcije** izberite možnost **Prilagoditev obračuna** in tako posodobite finančne razsežnosti.

3. Ko zaključite s prilagajanjem vrednosti finančnih razsežnosti, pojdite na **Upravljanje projektov in računovodstvo** \> **Periodično** \> **Integracije za aplikacijo Project Operations**, izberite možnost **Uvozi iz pripravljalne tabele** in tako zaženite periodični postopek. V ta postopek so vključene posodobljene vrednosti finančnih dimenzij za ponovno ustvarjanje vrstic predloga za račun projekta. Ko je račun za projekt knjižen, so posodobljene vrednosti uporabljene v njegovi podknjigi in glavni knjigi.
