---
title: Domača stran razsežnosti za določanje cen in razčlenitev stroškov
description: Ta članek ponuja pregled dimenzij cen.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 88c77d90bccaa5f10e8f75d60ae121d699bc0976
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925462"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Domača stran razsežnosti za določanje cen in razčlenitev stroškov

[!include [banner](../includes/psa-now-project-operations.md)]

Na dimenzije, ki se uporabljajo za določanje cen dela in stroškov v organizacijah, ki temeljijo na projektih, vplivajo naslednji atributi:

- Ljudje, ki opravljajo delo v skladu z njihovimi izkušnjami, vlogo ali zemljepisno lokacijo
- Delo, ki se izvaja v skladu z zahtevnostjo in časom v dnevu

Glede na naravo teh atributov dela in ljudi, ki so potrebni za izvedbo dela, sta v rešitvi Project Service Automation na voljo dve vrsti vrednosti cenovnih razsežnosti: 

- **Nabori možnosti** – atributi, ki so nespremenljiva oštevilčenja za nabor vrednosti.
- **Vrednosti, ki temeljijo na entitetah** – atributi, ki imajo lahko različne nabore vrednosti, ki so končne, vendar se lahko sčasoma spreminjajo.

## <a name="pricing-dimensions"></a>Cenovne razsežnosti

Storitev PSA vključuje privzet nabor cenovnih razsežnosti. Te si lahko ogledate v **Project Service** > **Parametri**. V zapisu parametra na zavihku **Cenovna razsežnost na podlagi zneska** preverite, ali sta pri vlogi **msdyn_resourcecategory** in organizacijski enoti za vire **msdyn_organizationalunit** polji **Mogoče uporabiti za prodajo** in **Mogoče uporabiti za ceno** nastavljeni na **Da**. To vam bo omogočilo, da nastavite ceno in ceno za vsako kombinacijo vloge in organizacijske enote.

![Prikaz parametrov v aplikaciji Project Service z označeno možnostjo »Mogoče uporabiti za prodajo«.](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Če ste uporabljali vnaprej pripravljena polja vloge in organizacijske enote kot cenovne razsežnosti pred različico 3 aplikacije PSA, ne bo nobene opazne spremembe. Project Service lahko še naprej uporabljate kot običajno. 

Če morate zagotoviti ceno ali strošek za svoje vire z dodatnimi atributi, lahko ustvarite polja, entitete in razsežnosti po meri. Za več informacij si oglejte naslednje članke, vendar upoštevajte, da morate postopke izvesti v spodnjem vrstnem redu:

- [Ustvarjanje polj in entitet po meri](create-custom-fields-entities.md)
- [Dodajanje polj po meri v entitete za nastavitev cene in transakcijske entitete](field-references.md)
- [Nastavitev polj po meri kot cenovnih razsežnosti ](set-up-pricing-dimensions.md)
- [Posodabljanje atributov vtičnikov za vključitev novih cenovnih razsežnosti](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Določanje cene časa človeških virov
Kako organizacija določi cene za čas človeških virov je pogosto pomemben strateški vidik, ki neposredno vpliva na dobičkonosnost organizacije. Ko se je vaša organizacija pripravljena opredeliti, kako želi nastaviti mere stroškov in deleže obračunavanja za čas človeških virov, sodelujte s finančnimi ekipami in vodji praks.

Drugi vidiki določanja cen vključujejo tudi to, ali naj se znova uporabijo polja ali entitete, ki trenutno niso cenovne razsežnosti, vendar se uporabljajo kot cenovna razsežnost za vašo organizacijo. Polja, kot sta **Kategorija transakcije** (**msdyn_transactioncategory**) in **Viri, ki jih je mogoče rezervirati** (**bookableresource**), so primeri možnih razsežnosti. 

Razmislite, ali naj bo vaša cenovna razsežnost tabela ali nabor možnosti. Če predvidevate spremembe vrednosti razsežnosti, ki bodo presegle vrednost 10 ali 12, in potrebujete dodatne atribute za te vrednosti, namesto nabora možnosti raje ustvarite entiteto. Za vzdrževanje nabora možnosti, na primer dodajanje ali odstranjevanje vrednosti, je potreben skrbnik ali razvijalec, dodajanje novih vrstic v tabelo pa lahko opravi večina poslovnih uporabnikov.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
