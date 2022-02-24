---
title: Ustvarjanje rešitve za cenovne razsežnosti po meri
description: Ta tema vsebuje informacije o ustvarjanju rešitev za cenovne razsežnosti po meri.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514025"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Ustvarjanje rešitve za cenovne razsežnosti po meri

 _**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_ 

>[!IMPORTANT]
>Vse spremembe cenovnih razsežnosti morajo biti v ločeni rešitvi. Ta pomembna najboljša praksa omogoča prilagodljivost pri posodabljanju ali odstranjevanju sprememb po potrebi, pomaga pri ponovni uporabi vašega dela in olajša prenos teh sprememb v druge primerke. Ko naredite vse zahtevane spremembe, izvozite to rešitev kot **Upravljano** rešitev in jo nato uvozite še v druge primerke za ponovno uporabo.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Ustvarjanje rešitve za cenovne razsežnosti po meri

1.  Izberite **Nastavitve** > **Rešitve** in nato izberite **Novo**.
2.  Poimenujte rešitev *Cenovne razsežnosti <your organization name>*.
3. Vnesite ostale zahtevane informacije in nato izberite **Shrani**.

  ![Ustvarjanje rešitve za cenovne razsežnosti po meri](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Dodajanje vseh zahtevanih entitet in povezanih komponent v rešitev za cenovne razsežnosti

V rešitev za določanje cen dodajte naslednje entitete storitve Project Service, da boste v rešitev za določanje cen lahko uvedli pomembne spremembe sheme. Ko boste dokončali ta postopek, bodo entitete prepoznale nove cenovne razsežnosti.

1.  Kliknite **Nastavitve** > **Rešitve** in nato dvokliknite **<*ime vaše organizacije*> cenovne razsežnosti**.
2.  V raziskovalcu rešitev v podoknu za krmarjenje na levi izberite **Dodaj obstoječe** > **Entitete**.
3.  V pogovornem oknu **Komponente rešitve** izberite eno od teh entitet:
 
   - **Dejansko**
   - **Vir, ki ga je mogoče rezervirati**
   - **Vrstica ocene**
   - **Projektno opravilo**
   - **Podrobnosti vrstice računa**
   - **Vrstica dnevnika**
   - **Podrobnost vrstice projektne pogodbe**
   - **Član projektne ekipe**
   - **Podrobnosti vrstice ponudbe**
   - **Pribitek na ceno vloge**
   - **Cena vloge**
   - **Časovni vnos**
 
   ![Dodajanje obstoječih entitet po meri v rešitev za cenovne razsežnosti](./media/Existing-entities-to-PD-solution.png)
 
 4. Za vsako entiteto preglejte komponente, ki jih dodajate, in končni seznam sredstev za vsako entiteto. 

   >[!NOTE]
   > Vključite vse obrazce in poglede za posamezne izbrane entitete.

  ![Dodane entitete](./media/solution-component-selection.png)


5.  Ko boste pozvani, da v izbrane entitete vključite vse odvisne entitete, izberite **Ne, ne vključi obveznih komponent.**

    ![Vključno z odvisnimi entitetami](./media/Do-not-include-required.png)
