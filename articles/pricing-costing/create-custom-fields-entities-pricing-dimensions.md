---
title: Ustvarjanje polj in entitet po meri kot cenovnih razsežnosti
description: Ta tema vsebuje informacije o tem, kako ustvariti nabore možnosti ali entitete po meri.
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084794"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Ustvarjanje polj in entitet po meri kot cenovnih razsežnosti

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Če želite ustvariti nabor možnosti ali entiteto po meri, upoštevajte spodnje korake.

> [!IMPORTANT]
> Priporočamo, da vse cenovne razsežnosti po meri spremenite v ločeni rešitvi. Ta pomembna najboljša praksa zagotavlja nadaljnjo prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi, pomaga pri ponovni uporabi vašega dela in olajša prenos teh sprememb v drug primerek. Ko naredite vse zahtevane spremembe, izvozite to rešitev kot **upravljano rešitev** in jo uvozite v druge primerke, da znova uporabite nastavitev cen.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Ustvarjanje rešitve po meri za cenovne razsežnosti
1. Odprite **Nastavitve** > **Rešitve** in nato izberite **Novo** , da ustvarite novo rešitev. 
2. Poimenujte rešitev **Cenovne razsežnosti za \<your organization name>** , vnesite ostale zahtevane podatke in izberite **Shrani**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Ustvarjanje polj po meri in naborov možnosti v rešitvi za cenovne razsežnosti

Cenovna razsežnost je lahko nabor možnosti ali entiteta. Oboje morate ustvariti v svoji rešitvi za določanje cen. Koraki v tem postopku pojasnjujejo, kako ustvarite razsežnosti, ki temeljijo na entiteti, in razsežnosti, ki temeljijo na naboru možnosti.

### <a name="entity-based-dimensions"></a>Razsežnosti na osnovi entitete

1. Odprite **Nastavitve** > **Rešitve** , nato dvokliknite **\<your organization name> cenovne razsežnosti**.
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete**.
3. Izberite **Novo** , da ustvarite novo entiteto **Standardni naziv**. 
4. Vnesite ostale zahtevane informacije in nato izberite **Shrani**.


### <a name="option-set-based-dimensions"></a>Razsežnosti na osnovi nabora možnosti 
Ustvarite lahko dve razsežnosti na osnovi nabora možnosti. Uporabite **Lokacija dela vira** , da sledite ceni za lokacijo dela **Doma** in **Na lokaciji** , ter **Delovni čas vira** z vrednostmi **Redno** in **Nadure** , da uporabite pribitek, ko je delo končano.


1. Odprite **Nastavitve** > **Rešitve** , nato dvokliknite **\<your organization name> cenovne razsežnosti**. 
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Nabori možnosti**. 
3. Izberite **Novo** , da ustvarite nov nabor možnosti, vnesite ostale zahtevane podatke in nato izberite **Shrani**.

## <a name="create-data-for-entity-based-dimensions"></a>Ustvarjanje podatkov za razsežnosti na osnovi entitete

Podatke za razsežnosti na osnovi entitete lahko ustvarite ročno ali z uvozom v aplikaciji Microsoft Excel oz. s klici storitve. Uporabite korake v tem postopku, da iz razsežnosti na osnovi entitete **Standardni naziv** ustvarite dva standardna naziva, in sicer **Sistemski inženir** in **Višji sistemi inženir**. Če je količina podatkov, ki jih želite ustvariti, majhna, kot v spodnjem primeru, lahko uporabite standardni obrazec.

1. Izberite **Napredno iskanje** , izberite entiteto **Standardni naslov** in nato izberite **Rezultati**. Prikazane bodo vse vrstice v entiteti **Standardni naziv**.
2. Izberite **Novo** in v polje **Ime** vnesite »Sistemski inženir« in nato izberite **Shrani**.
3. Zaprite obrazec. 
4. Ponovite korake od 1 do 3, da ustvarite drug standardni naziv za »Višji sistemski inženir«.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodajanje vseh zahtevanih entitet in povezanih komponent v rešitev za cenovne razsežnosti
V svojo rešitev za določanje cen boste morali dodati spodnje entitete. S koraki v tem postopku naredite nekaj pomembnih sprememb sheme v rešitvi za določanje cen, tako da se entitete seznanijo z novimi cenovnimi razsežnostmi.

1. Izberite **Nastavitve** > **Rešitve** , nato dvokliknite **\<your organization name> cenovne razsežnosti**. 
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Dodaj obstoječe** > **Entitete**.
3. V pogovornem oknu **Komponente rešitve** izberite eno od teh entitet:

  - Dejansko
  - Vir, ki ga je mogoče rezervirati
  - Vrstica ocene
  - Podrobnosti vrstice računa
  - Vrstica dnevnika
  - Podrobnost vrstice projektne pogodbe
  - Član projektne ekipe
  - Podrobnosti vrstice ponudbe
  - Pribitek na ceno vloge
  - Cena vloge 
  - Časovni vnos 


> [!NOTE]
> Poskrbite, da boste vključili vse obrazce in poglede za posamezne izbrane entitete.

4. Ko ste pozvani, da vključite vse odvisne entitete za zgoraj izbrane entitete, izberite **Ne**.

