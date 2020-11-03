---
title: Pregled cenovnih razsežnosti
description: Ta tema vsebuje informacije o cenovnih razsežnostih v storitvi Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084863"
---
# <a name="pricing-dimensions-overview"></a>Pregled cenovnih razsežnosti

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Razsežnosti, ki se uporabljajo v človeških virih za nastavitev določanja cen in stroškov, se delijo v dve kategoriji:

- Osebe
- Načrtovano delo

Zaradi tega obstajata dve vrsti vrednosti cenovnih razsežnosti, ki so na voljo:

- **Nabori možnosti** : razsežnosti, ki so nespremenljiva oštevilčenja za nabor vrednosti.
- **Vrednosti, ki temeljijo na entitetah** : razsežnosti, ki so lahko spremenljiv nabor vrednosti.

## <a name="pricing-dimensions"></a>Cenovne razsežnosti

Dynamics 365 Project Operations vključuje privzet nabor cenovnih razsežnosti. Te cenovne razsežnosti si lahko ogledate v **Project Operations** > **Parametri**. V zapisu parametra na zavihku **Cenovna razsežnost na podlagi zneska** preverite, ali sta pri vlogi **msdyn_resourcecategory** in organizacijski enoti za vire **msdyn_organizationalunit** polji **Mogoče uporabiti za prodajo** in **Mogoče uporabiti za ceno** nastavljeni na **Da**. Z omogočenimi temi polji lahko nastavite ceno in strošek za vsako kombinacijo vloge in organizacijske enote.

Če morate zagotoviti ceno ali strošek za svoje vire z dodatnimi atributi, lahko ustvarite polja, entitete in razsežnosti po meri.

## <a name="pricing-human-resource-time"></a>Določanje cene časa človeških virov
Kako organizacija določi cene za čas človeških virov je pogosto pomemben strateški vidik, ki neposredno vpliva na dobičkonosnost organizacije. Ko se je vaša organizacija pripravljena opredeliti, kako želi nastaviti mere stroškov in deleže obračunavanja za čas človeških virov, sodelujte s finančnimi ekipami in vodji praks.

Drugi vidiki določanja cen vključujejo tudi to, ali naj se znova uporabijo polja ali entitete, ki trenutno niso cenovne razsežnosti, vendar se uporabljajo kot cenovna razsežnost za vašo organizacijo. Polja, kot sta **Kategorija transakcije** ( **msdyn_transactioncategory** ) in **Viri, ki jih je mogoče rezervirati** ( **bookableresource** ), so primeri možnih razsežnosti. 

Razmislite, ali naj bo vaša cenovna razsežnost tabela ali nabor možnosti. Če predvidevate spremembe vrednosti razsežnosti, ki bodo presegle 10 ali 12, in potrebujete dodatne atribute v teh vrednosti, namesto nabora možnosti raje ustvarite entiteto. Vzdrževanje nabora možnosti, na primer dodajanje ali odstranjevanje vrednosti, zahteva skrbnika ali razvijalca, dodajanje novih vrstic v tabelo pa lahko opravi večina uporabnikov.

Spodnji primer prikazuje deleže obračunavanja, ki so nastavljeni na podlagi vloge in organizacijske enote organizacije vira, ki ji pripada vir. Mere stroškov običajno temeljijo na razponu plače zaposlenega in organizacijski enoti, ki ji pripada. V tem primeru bodo tabele z deležem obračunavanja in mero stroškov videti, kot je prikazano spodaj.

**Vzorčni deleži obračunavanja**

| Vloga        | Organizacijska enota    |Enota      |Cena      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Developer   | Contoso, ZDA  |Ura | 200|USD     |
| Developer   | Contoso Indija |Ura|   112|USD     |


**Vzorčne mere stroškov**

| Razpon plače     | Organizacijska enota    |Enota      |Cena      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| Moje podjetje_razpon1 | Contoso, ZDA  |Ura | 145|USD     |
| Moje podjetje_razpon2 | Contoso Indija |Ura|   67|USD     |
