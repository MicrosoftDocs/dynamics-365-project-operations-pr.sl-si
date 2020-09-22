---
title: Ustvarjanje polj in entitet po meri
description: V tej temi je pojasnjeno, kako ustvarite nabor možnosti in entitete v svoji rešitvi v platformi Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755861"
---
# <a name="create-custom-fields-and-entities"></a>Ustvarjanje polj in entitet po meri 

Če želite ustvariti nabor možnosti ali entiteto po meri v platformi Power Apps, upoštevajte spodnje korake.  
Postopke v tej temi morate izvesti s spletnim vmesnikom aplikacije Project Service Automation (PSA).

> [!IMPORTANT]
> Priporočamo, da vse cenovne razsežnosti po meri spremenite v ločeni rešitvi. Ta pomembna najboljša praksa zagotavlja nadaljnjo prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi, pomaga pri ponovni uporabi vašega dela in olajša prenos teh sprememb v drug primerek. Ko naredite vse zahtevane spremembe, izvozite to rešitev kot **upravljano rešitev** in jo uvozite v druge primerke, da znova uporabite nastavitev cen.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Ustvarjanje rešitve po meri za cenovne razsežnosti
1. V PSA kliknite **Nastavitve** > **Rešitve** in nato **Novo**, da ustvarite novo rešitev. 
2. Poimenujte rešitev, **\<ime organizacije> cenovne razsežnosti**, vnesite ostale zahtevane podatke in kliknite **Shrani.**

> ![Ustvarjanje rešitve po meri za cenovne razsežnosti](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Ustvarjanje polj po meri in naborov možnosti v rešitvi za cenovne razsežnosti

Cenovna razsežnost je lahko nabor možnosti ali entiteta. Oboje morate ustvariti v svoji rešitvi za določanje cen. Koraki v tem postopku pojasnjujejo, kako ustvarite razsežnosti, ki temeljijo na entiteti, in razsežnosti, ki temeljijo na naboru možnosti.

### <a name="entity-based-dimensions"></a>Razsežnosti na osnovi entitete

1. V PSA kliknite **Nastavitve** > **Rešitve** in nato dvokliknite **\<ime organizacije> cenovne razsežnosti**.
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete**.
3. Kliknite **Novo**, da ustvarite novo entiteto **Standardni naziv**. Vnesite ostale zahtevane informacije in kliknite **Shrani**.

> ![Definicija entitete standardnega naziva](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Razsežnosti na osnovi nabora možnosti 
Ustvarite lahko dve razsežnosti na osnovi nabora možnosti. Uporabite **Lokacija dela vira**, da sledite ceni za lokacijo dela **Doma** in **Na lokaciji**, ter **Delovni čas vira** z vrednostmi **Redno** in **Nadure**, da uporabite pribitek, ko je delo končano.


1. V PSA kliknite **Nastavitve** > **Rešitve** in nato dvokliknite **\<ime organizacije> cenovne razsežnosti**. 
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Nabori možnosti**. 
3. Kliknite **Novo**, da ustvarite nov nabor možnosti, vnesite ostale zahtevane podatke in kliknite **Shrani**.

> ![Cenovna razsežnost na osnovi nabora možnosti, imenovana »Lokacija dela vira« ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Cenovna razsežnost na osnovi nabora možnosti, imenovana »Delovne ure vira« ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Ustvarjanje podatkov za razsežnosti na osnovi entitete

Podatke za razsežnosti na osnovi entitete lahko ustvarite ročno ali z uvozom v aplikaciji Microsoft Excel oz. s klici storitve. Uporabite korake v tem postopku, da iz razsežnosti na osnovi entitete **Standardni naziv** ustvarite dva standardna naziva, in sicer **Sistemski inženir** in **Višji sistemi inženir**. Če je količina podatkov, ki jih želite ustvariti, majhna, kot v spodnjem primeru, lahko uporabite standardni obrazec.

1. V PSA kliknite **Napredno iskanje**. Izberite entiteto **Standardni naziv** in nato kliknite **Rezultati**. Prikazane bodo vse vrstice v entiteti **Standardni naziv**.
2. Kliknite **Novo**. V polje **Ime** vnesite »Sistemski inženir« in nato kliknite **Shrani**.
3. Zaprite obrazec. 
4. Ponovite korake od 1 do 3, da ustvarite drug standardni naziv za »Višji sistemski inženir«.

> ![Vzorčni podatki za entiteto standardnega naziva ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodajanje vseh zahtevanih entitet PSA in povezanih komponent v rešitev za cenovne razsežnosti
V svojo rešitev za določanje cen boste morali dodati spodnje entitete rešitve Project Service. S koraki v tem postopku naredite nekaj pomembnih sprememb sheme v rešitvi za določanje cen, tako da se entitete seznanijo z novimi cenovnimi razsežnostmi.

1. V PSA kliknite **Nastavitve** > **Rešitve** in nato dvokliknite **\<ime organizacije> cenovne razsežnosti**. 
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

> ![Dodajanje obstoječih entitet v rešitev za cenovne razsežnosti](media/Existing-entities-to-PD-solution.png)

> ![Izbira komponent rešitve](media/Dimension-Components.png)

> [!NOTE]
> Poskrbite, da boste vključili vse obrazce in poglede za posamezne izbrane entitete.

4. Ko ste pozvani, da vključite vse odvisne entitete za zgoraj izbrane entitete, kliknite **Ne**.

> ![Ne vključi vseh povezanih komponent](media/Do-not-include-required.png)


