---
title: Ustvarjanje polj in entitet po meri
description: V tej temi je pojasnjeno, kako ustvarite nabor možnosti in entitete v svoji rešitvi v platformi Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
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
ms.openlocfilehash: f501bcc106a296f35bba996b6ab3a8b758cefb1926033faf04ee23c42bc94d39
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992451"
---
# <a name="create-custom-fields-and-entities"></a>Ustvarjanje polj in entitet po meri 

[!include [banner](../includes/psa-now-project-operations.md)]

Če želite ustvariti nabor možnosti ali entiteto po meri v platformi Power Apps, upoštevajte spodnje korake.  
Postopke v tej temi morate izvesti s spletnim vmesnikom aplikacije Project Service Automation (PSA).

> [!IMPORTANT]
> Priporočamo, da vse cenovne razsežnosti po meri spremenite v ločeni rešitvi. Ta pomembna najboljša praksa zagotavlja nadaljnjo prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi, pomaga pri ponovni uporabi vašega dela in olajša prenos teh sprememb v drug primerek. Ko naredite vse zahtevane spremembe, izvozite to rešitev kot **upravljano rešitev** in jo uvozite v druge primerke, da znova uporabite nastavitev cen.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Ustvarjanje polj po meri in naborov možnosti v rešitvi za cenovne razsežnosti

Cenovna razsežnost je lahko nabor možnosti ali entiteta. Oboje morate ustvariti v svoji rešitvi za določanje cen. Koraki v tem postopku pojasnjujejo, kako ustvarite razsežnosti, ki temeljijo na entiteti, in razsežnosti, ki temeljijo na naboru možnosti.

### <a name="entity-based-dimensions"></a>Razsežnosti na osnovi entitete

1. V rešitvi PSA kliknite **Nastavitve** > **Rešitve**, nato pa dvokliknite **\<your organization name> – cenovne razsežnosti**.
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete**.
3. Kliknite **Novo**, da ustvarite novo entiteto **Standardni naziv**. Vnesite ostale zahtevane informacije in kliknite **Shrani**.

> ![Definicija entitete standardnega naziva.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Razsežnosti na osnovi nabora možnosti 
Ustvarite lahko dve razsežnosti na osnovi nabora možnosti. Uporabite **Lokacija dela vira**, da sledite ceni za lokacijo dela **Doma** in **Na lokaciji**, ter **Delovni čas vira** z vrednostmi **Redno** in **Nadure**, da uporabite pribitek, ko je delo končano.


1. V rešitvi PSA kliknite **Nastavitve** > **Rešitve**, nato pa dvokliknite **\<your organization name> – cenovne razsežnosti**. 
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Nabori možnosti**. 
3. Kliknite **Novo**, da ustvarite nov nabor možnosti, vnesite ostale zahtevane podatke in kliknite **Shrani**.

> ![Cenovna razsežnost na osnovi nabora možnosti, imenovana »Lokacija dela vira«.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Cenovna razsežnost na osnovi nabora možnosti, imenovana »Delovni čas vira«.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Ustvarjanje podatkov za razsežnosti na osnovi entitete

Podatke za razsežnosti na osnovi entitete lahko ustvarite ročno ali z uvozom v aplikaciji Microsoft Excel oz. s klici storitve. Uporabite korake v tem postopku, da iz razsežnosti na osnovi entitete **Standardni naziv** ustvarite dva standardna naziva, in sicer **Sistemski inženir** in **Višji sistemi inženir**. Če je količina podatkov, ki jih želite ustvariti, majhna, kot v spodnjem primeru, lahko uporabite standardni obrazec.

1. V PSA kliknite **Napredno iskanje**. Izberite entiteto **Standardni naziv** in nato kliknite **Rezultati**. Prikazane bodo vse vrstice v entiteti **Standardni naziv**.
2. Kliknite **Novo**. V polje **Ime** vnesite »Sistemski inženir« in nato kliknite **Shrani**.
3. Zaprite obrazec. 
4. Ponovite korake od 1 do 3, da ustvarite drug standardni naziv za »Višji sistemski inženir«.

> ![Vzorčni podatki za entiteto standardnega naziva.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]