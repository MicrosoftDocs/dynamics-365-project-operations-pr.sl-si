---
title: Ustvarjanje rešitev po meri za cenovne razsežnosti
description: V tej temi je opisano, kako pri ustvarjanju cenovnih razsežnosti po meri ustvarite rešitev po meri.
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
ms.openlocfilehash: 4dea80d8e4645675d3e89e846532ca7c0f292faa328c45938941c50dc15486fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995286"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Ustvarjanje rešitev po meri za cenovne razsežnosti

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Vse spremembe cenovnih razsežnosti morajo biti v ločeni rešitvi. Ta pomembna najboljša praksa zagotavlja nadaljnjo prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi, pomaga pri ponovni uporabi vašega dela in olajša prenos teh sprememb v drug primerek. Ko naredite vse zahtevane spremembe, izvozite to rešitev kot **upravljano rešitev** in jo uvozite v druge primerke, da znova uporabite nastavitev cen.

1. Izberite **Nastavitve** > **Rešitve** in nato izberite **Novo**. 
2. Poimenujte rešitev **Cenovne razsežnosti za \<your organization name>**, vnesite ostale zahtevane podatke in izberite **Shrani**.

> ![Ustvarjanje rešitve po meri za cenovne razsežnosti.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodajanje vseh zahtevanih entitet in povezanih komponent v rešitev za cenovne razsežnosti
V svojo rešitev za določanje cen boste morali dodati spodnje entitete rešitve Project Service. S koraki v tem postopku naredite nekaj pomembnih sprememb sheme v rešitvi za določanje cen, tako da se entitete seznanijo z novimi cenovnimi razsežnostmi.

1. Izberite **Nastavitve** > **Rešitve**, nato dvokliknite **\<your organization name> cenovne razsežnosti**. 
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

> ![Dodajanje obstoječih entitet v rešitev za cenovne razsežnosti.](media/Existing-entities-to-PD-solution.png)

> ![Izberite komponente rešitve.](media/Dimension-Components.png)

> [!NOTE]
> Poskrbite, da boste vključili vse obrazce in poglede za posamezne izbrane entitete.

4. Ko ste pozvani, da vključite vse odvisne entitete za izbrane entitete, izberite **Ne**.

> ![Ne vključi vseh povezanih komponent.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]