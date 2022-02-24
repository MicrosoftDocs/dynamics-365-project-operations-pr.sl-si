---
title: Pregled cenovnih razsežnosti
description: Ta tema vsebuje informacije o cenovnih razsežnostih v aplikaciji Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 33f55976eafedd046fba952ab6381c297ab4e271
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650231"
---
# <a name="pricing-dimensions-overview"></a>Pregled cenovnih razsežnosti

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Razsežnosti, ki se uporabljajo v človeških virih za nastavitev določanja cen in stroškov, se delijo v dve kategoriji:

- Osebe
- Načrtovano delo

Zaradi tega obstajata dve vrsti vrednosti cenovnih razsežnosti, ki so na voljo:

- **Nabori možnosti**: razsežnosti, ki so nespremenljiva oštevilčenja za nabor vrednosti.
- **Vrednosti, ki temeljijo na entitetah**: razsežnosti, ki so lahko spremenljiv nabor vrednosti.

## <a name="pricing-dimensions"></a>Cenovne razsežnosti

Dynamics 365 Project Operations vključuje privzet nabor cenovnih razsežnosti. Te cenovne razsežnosti si lahko ogledate v **Project Operations** > **Parametri**. V zapisu parametra na zavihku **Cenovna razsežnost na podlagi zneska** preverite, ali sta pri vlogi **msdyn_resourcecategory** in organizacijski enoti za vire **msdyn_organizationalunit** polji **Mogoče uporabiti za prodajo** in **Mogoče uporabiti za ceno** nastavljeni na **Da**. Z omogočenimi temi polji lahko nastavite ceno in strošek za vsako kombinacijo vloge in organizacijske enote.

![Prikaz parametrov v aplikaciji Project Service z označeno možnostjo »Mogoče uporabiti za prodajo«](media/PS-OOB-parameters.png)

Če morate zagotoviti ceno ali strošek za svoje vire z dodatnimi atributi, lahko ustvarite polja, entitete in razsežnosti po meri. Za več informacij glejte naslednjo temo. 
  
  > [!NOTE]
  > Postopki morajo biti zaključeni v vrstnem redu, v katerem so bili navedeni.

1. [Ustvarjanje rešitve za cenovne razsežnosti po meri](../sales/create-solution-custompd.md)
2. [Ustvarjanje polj in entitet po meri](create-custom-fields-entities-pricing-dimensions.md)
3. [Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete ](add-custom-fields-price-setup-transactional-entities.md)
4. [Nastavitev polj po meri kot cenovnih razsežnosti ](set-up-custom-fields-pricing-dimensions.md)
5. [Posodabljanje atributov vtičnikov za vključitev novih cenovnih razsežnosti](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Določanje cene časa človeških virov
Kako organizacija določi cene za čas človeških virov je pogosto pomemben strateški vidik, ki neposredno vpliva na dobičkonosnost organizacije. Ko se je vaša organizacija pripravljena opredeliti, kako želi nastaviti mere stroškov in deleže obračunavanja za čas človeških virov, sodelujte s finančnimi ekipami in vodji praks.

Drugi vidiki določanja cen vključujejo tudi to, ali naj se znova uporabijo polja ali entitete, ki trenutno niso cenovne razsežnosti, vendar se uporabljajo kot cenovna razsežnost za vašo organizacijo. Polja, kot sta **Kategorija transakcije** (**msdyn_transactioncategory**) in **Viri, ki jih je mogoče rezervirati** (**bookableresource**), so primeri možnih razsežnosti. 

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
