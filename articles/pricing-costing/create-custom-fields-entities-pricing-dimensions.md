---
title: Ustvarjanje polj in entitet po meri kot cenovnih razsežnosti
description: Ta tema vsebuje informacije o tem, kako ustvariti nabore možnosti ali entitete po meri.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642833"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Ustvarjanje polj in entitet po meri kot cenovnih razsežnosti

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Če želite ustvariti nabor možnosti ali entiteto po meri, da bi jo uporabili kot cenovno razsežnost, upoštevajte spodnje korake. Za več informacij glejte razdelek [Pregled cenovnih razsežnosti](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Priporočamo, da vse cenovne razsežnosti po meri spremenite v ločeni rešitvi. Ta pomembna najboljša praksa zagotavlja nadaljnjo prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi. To bo pomagalo tudi pri ponovni uporabi opravljenega dela in olajšalo prenos teh sprememb na drug primerek. Ko izvedete vse zahtevane spremembe, izvozite to rešitev kot **Upravljano rešitev** in jo uvozite v druge primerke, da ponovno uporabite nastavljeno oblikovanje cen.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Ustvarjanje polj po meri in naborov možnosti v rešitvi za cenovne razsežnosti

Cenovna razsežnost je lahko nabor možnosti ali entiteta. Oboje morate ustvariti v svoji rešitvi za določanje cen. Koraki v tem postopku pojasnjujejo, kako ustvarite razsežnosti, ki temeljijo na entiteti, in razsežnosti, ki temeljijo na naboru možnosti.

### <a name="entity-based-dimensions"></a>Razsežnosti na osnovi entitete
Če želite ustvariti razsežnosti, ki temeljijo na entitetah, sledite tem korakom:

1. Odprite **Nastavitve** > **Rešitve**, nato dvokliknite **\<your organization name> cenovne razsežnosti**.
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Entitete**.
3. Izberite **Novo**, da ustvarite novo entiteto **Standardni naziv**. 
4. Vnesite ostale zahtevane informacije in nato izberite **Shrani**.

> ![Definicija entitete standardnega naziva](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Razsežnosti na osnovi nabora možnosti 
Ustvarite lahko dve razsežnosti na osnovi nabora možnosti. 

- Uporabite **Lokacija dela vira** za sledenje ceni lokacije dela, opravljenega **Doma** in **Na lokaciji**. 
- Uporabite **Delovni čas vira** z vrednostmi **Redno** in **Nadure**, da se prikaže oznaka, ko je delo končano.

Naslednja slika prikazuje pogled razsežnosti **Lokacija dela vira**. 

> ![Cenovna razsežnost na osnovi nabora možnosti, imenovana »Lokacija dela vira«](media/Option-set-PD-called-Resource-Work-Location.png)

Naslednja slika prikazuje pogled razsežnosti **Delovni čas vira**. 

> ![Cenovna razsežnost na osnovi nabora možnosti, imenovana »Delovne ure vira«](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Odprite **Nastavitve** > **Rešitve**, nato dvokliknite **\<your organization name> cenovne razsežnosti**. 
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Nabori možnosti**. 
3. Izberite **Novo**, da ustvarite nov nabor možnosti, vnesite ostale zahtevane podatke in nato izberite **Shrani**.

## <a name="create-data-for-entity-based-dimensions"></a>Ustvarjanje podatkov za razsežnosti na osnovi entitete

Podatke za razsežnosti na osnovi entitete lahko ustvarite ročno ali z uvozom v aplikaciji Microsoft Excel oz. s klici storitve. Uporabite korake v tem postopku, da iz razsežnosti na osnovi entitete **Standardni naziv** ustvarite dva standardna naziva, in sicer **Sistemski inženir** in **Višji sistemi inženir**. Če je količina podatkov, ki jih želite ustvariti, majhna, kot v spodnjem primeru, lahko uporabite standardni obrazec.

1. Izberite **Napredno iskanje**.
2. Izberite entiteto **Standardni naziv** in nato izberite **Rezultati**. Prikazane bodo vse vrstice v entiteti **Standardni naziv**.
3. Izberite **Novo** in v polje **Ime** vnesite »Sistemski inženir« in nato izberite **Shrani**.
4. Zaprite stran. 
5. Ponovite korake od 1 do 3, da ustvarite drug standardni naziv za »Višji sistemski inženir«.

> ![Vzorčni podatki za entiteto standardnega naziva](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]