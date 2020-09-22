---
title: Domača stran razsežnosti za določanje cen in razčlenitev stroškov
description: V tej temi je na voljo pregled cenovnih razsežnosti.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755777"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Domača stran razsežnosti za določanje cen in razčlenitev stroškov

Razsežnosti, ki se uporabljajo v človeških virih za nastavitev določanja cen in stroškov, se delijo v dve kategoriji:

- Osebe
- Načrtovano delo

Zaradi tega obstajata dve vrsti vrednosti cenovnih razsežnosti, ki so na voljo v aplikaciji Project Service Automation (PSA): 

- **Nabori možnosti** – razsežnosti, ki so nespremenljiva oštevilčenja za nabor vrednosti.
- **Vrednosti, ki temeljijo na entitetah** – razsežnosti, ki so lahko spremenljiv nabor vrednosti.

## <a name="pricing-dimensions"></a>Cenovne razsežnosti

Storitev PSA vključuje privzet nabor cenovnih razsežnosti. Te si lahko ogledate v **Project Service** > **Parametri**. V zapisu parametra na zavihku **Cenovna razsežnost na podlagi zneska** preverite, ali sta pri vlogi **msdyn_resourcecategory** in organizacijski enoti za vire **msdyn_organizationalunit** polji **Mogoče uporabiti za prodajo** in **Mogoče uporabiti za ceno** nastavljeni na **Da**. To vam bo omogočilo, da nastavite ceno in ceno za vsako kombinacijo vloge in organizacijske enote.

![Prikaz parametrov v aplikaciji Project Service z označeno možnostjo »Mogoče uporabiti za prodajo«](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Če ste uporabljali vnaprej pripravljena polja vloge in organizacijske enote kot cenovne razsežnosti pred različico 3 aplikacije PSA, ne bo nobene opazne spremembe. Project Service lahko še naprej uporabljate kot običajno. 

Če morate zagotoviti ceno ali strošek za svoje vire z dodatnimi atributi, lahko ustvarite polja, entitete in razsežnosti po meri. Če želite več informacij, glejte spodnje teme, vendar upoštevajte, da morate dokončati postopke v spodaj navedenem vrstnem redu:

- [Ustvarjanje polj in entitet po meri](create-custom-fields-entities.md)
- [Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete](field-references.md)
- [Nastavitev polj po meri kot cenovnih razsežnosti](set-up-pricing-dimensions.md)
- [Posodabljanje atributov vtičnikov za vključitev novih cenovnih razsežnosti](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Določanje cene časa človeških virov
Kako organizacija določi cene za čas človeških virov je pogosto pomemben strateški vidik, ki neposredno vpliva na dobičkonosnost organizacije. Ko se je vaša organizacija pripravljena opredeliti, kako želi nastaviti mere stroškov in deleže obračunavanja za čas človeških virov, sodelujte s finančnimi ekipami in vodji praks.

Drugi vidiki določanja cen vključujejo tudi to, ali naj se znova uporabijo polja ali entitete, ki trenutno niso cenovne razsežnosti, vendar se uporabljajo kot cenovna razsežnost za vašo organizacijo. Polja, kot sta **Kategorija transakcije** (**msdyn_transactioncategory**) in **Viri, ki jih je mogoče rezervirati** (**bookableresource**), so primeri možnih razsežnosti. 

Razmislite tudi o tem, ali naj bo vaša cenovna razsežnost tabela ali nabor možnosti. Če predvidevate spremembe vrednosti razsežnosti, ki bodo presegle 10 ali 12, in potrebujete dodatne atribute v teh vrednosti, namesto nabora možnosti raje ustvarite entiteto. Vzdrževanje nabora možnosti, na primer dodajanje ali odstranjevanje vrednosti, zahteva skrbnika ali razvijalca, dodajanje novih vrstic v tabelo pa lahko opravi večina uporabnikov.

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
