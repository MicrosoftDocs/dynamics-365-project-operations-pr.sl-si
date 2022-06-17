---
title: Ustvarjanje polj in entitet po meri
description: Ta članek pojasnjuje, kako ustvariti nabore možnosti in entitete v lastni rešitvi v Power Apps platforma.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 3b6f675d604f3b6a6f2465c413ceff3d16815e12
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926934"
---
# <a name="create-custom-fields-and-entities"></a>Ustvarjanje polj in entitet po meri 

[!include [banner](../includes/psa-now-project-operations.md)]

Če želite ustvariti nabor možnosti ali entiteto po meri v platformi Power Apps, upoštevajte spodnje korake.  
Postopke v tem članku je treba izvesti s spletnim vmesnikom Project Service Automation (PSA).

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
