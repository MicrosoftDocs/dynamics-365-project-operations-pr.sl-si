---
title: Ustvarjanje rešitev po meri za cenovne razsežnosti
description: V tej temi je opisano, kako pri ustvarjanju cenovnih razsežnosti po meri ustvarite rešitev po meri.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084765"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Ustvarjanje rešitev po meri za cenovne razsežnosti

> [!IMPORTANT]
> Vse spremembe cenovnih razsežnosti morajo biti v ločeni rešitvi. Ta pomembna najboljša praksa zagotavlja nadaljnjo prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi, pomaga pri ponovni uporabi vašega dela in olajša prenos teh sprememb v drug primerek. Ko naredite vse zahtevane spremembe, izvozite to rešitev kot **upravljano rešitev** in jo uvozite v druge primerke, da znova uporabite nastavitev cen.

1. Izberite **Nastavitve** > **Rešitve** in nato izberite **Novo**. 
2. Poimenujte rešitev **Cenovne razsežnosti za \<your organization name>** , vnesite ostale zahtevane podatke in izberite **Shrani**.

> ![Ustvarjanje rešitve po meri za cenovne razsežnosti](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodajanje vseh zahtevanih entitet in povezanih komponent v rešitev za cenovne razsežnosti
V svojo rešitev za določanje cen boste morali dodati spodnje entitete rešitve Project Service. S koraki v tem postopku naredite nekaj pomembnih sprememb sheme v rešitvi za določanje cen, tako da se entitete seznanijo z novimi cenovnimi razsežnostmi.

1. Izberite **Nastavitve** > **Rešitve** , nato dvokliknite **\<your organization name> cenovne razsežnosti**. 
2. V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Dodaj obstoječe** > **Entitete**.
3. V pogovornem oknu **Komponente rešitve** izberite eno od teh entitet:

- Dejansko
- Vir, ki ga je mogoče rezervirati
- Vrstica ocene
- Projektno opravilo
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

4. Ko ste pozvani, da vključite vse odvisne entitete za izbrane entitete, izberite **Ne**.

> ![Ne vključi vseh povezanih komponent](media/Do-not-include-required.png)


