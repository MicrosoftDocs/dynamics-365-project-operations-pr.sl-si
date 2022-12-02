---
title: Dodajanje novih obrazcev entitet po meri (Project Service Automation 2.x)
description: V tem članku so navedene informacije o dodajanju obrazcev entitet po meri za priložnosti, ponudbe, naročila ali račune v aplikaciji Dynamics 365 Project Service Automation 2. x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: b7e5cbefd9d9705e0bafcb2551e1ce56457a187e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922748"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Dodajanje novih obrazcev entitet po meri (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Polje »Vrsta« 

Dynamics 365 Project Service Automation uporablja polje **Vrsta** (**msdyn\_ordertype**) za entitete priložnosti, ponudbe, naročila in računa za ločevanje različic teh entitet, ki **temeljijo na delu**, od različic, ki **temeljijo na elementu** in **temeljijo na storitvi**. Različice teh entitet, ki temeljijo na delu, obravnava PSA. Precej poslovne logike na strani odjemalca in strežnika rešitve je odvisne od polja **Vrsta**. Zato je pomembno, da je polje v začetku izpolnjeno s pravilno vrednostjo, ko so entitete ustvarjene. Nepravilna vrednost lahko povzroči nepravilne postopke, del poslovne logike pa morda ne bo pravilno izveden.

## <a name="automatic-form-switching"></a>Samodejni preklop obrazcev

Da se prepreči poškodovanje podatkov in nepričakovano delovanje, ki ga povzroči nepravilno prvotno izpolnjevanje in urejanje zapisov prodajnih entitet, PSA za vnaprej pripravljene obrazce zdaj vključuje logiko samodejnega preklopa obrazcev. Ta logika uporabnike usmeri na pravilen obrazec za delo z različico, ki temelji na delu, ali katero koli drugo vrsto entitete priložnosti, ponudbe, naročila ali računa. Ko uporabnik odpre različico entitete priložnosti, ponudbe, naročila ali računa, ki temelji na delu, se preklopi na obrazec **Podatki o projektu**.

Logika samodejnega preklapljanja med obrazci uporablja preslikavo med vrednostjo **formId** in poljem **msdyn\_ordertype**. V to preslikavo so bili dodani vsi vnaprej pripravljeni obrazci. Obrazce po meri pa je treba ročno dodati, pri čemer je treba navesti, katero različico entitete naj obravnavajo. To temelji na polju **msdyn\_ordertype**. Če med preslikavo manjka obrazec, s katerega se preklaplja, bo logika preklopila na vnaprej pripravljen obrazec na podlagi vrednosti, ki je shranjena v polju **msdyn\_ordertype** entitete.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Dodajanje obrazcev po meri in vklop logike za preklapljanja obrazcev

Ta primer prikazuje, kako dodate obrazec po meri, imenovan **Moji podatki o projektu**, da bo deloval s priložnostmi, ki temeljijo na delu. Isti postopek se uporablja za dodajanje obrazcev po meri, da delujejo s ponudbami, naročili in računi.

Upoštevajte ta navodila in ustvarite različico obrazca **Podatki o projektu** po meri.

1. V entiteti »Priložnost« odprite obrazec za **Podatki o projektu** in shranite kopijo z imenom **Moji podatki o projektu**.
2. Odprite nov obrazec in nato v lastnostih preverite, ali so prisotni skripti za inicializacijo obrazca iz obrazca **Podatki o projektu**. 

    > [!IMPORTANT]
    > Skriptov ne odstranjujte. Če to storite, bodo nekateri podatki morda nepravilno inicializirani.

3. Preverite, ali je polje **Vrsta** (**msdyn\_ordertype**) prisotno na obrazcu. 

    > [!IMPORTANT]
    > Tega polja ne odstranjujte. Če to storite, skripti za inicializacijo ne bodo uspešni.

4. Poiščite vrednost **formId** novega obrazca. Ta korak lahko izvedete na dva načina:

    - Izvozite obrazec **Moji podatki o projektu** kot del neupravljane rešitve in nato poiščite vrednost **formid** v datoteki customization.xml izvožene rešitve.
    - Odprite obrazec **Moji podatki o projektu** v urejevalniku obrazcev in poiščite globalni enolični identifikator (GUID) pri parametri **fromid** v URL-ju, kot je prikazano na spodnji sliki.

    ![Vrednost formId novega obrazca v URL-ju.](media/how-to-add-custom-forms-in-v2.0.png)

5. Ustvarite preslikavo vrste **msdyn\_ordertype** za vrednost **formId** tako, da uredite spletni vir msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Odstranite kodo iz vira in jo zamenjajte z naslednjo kodo.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Shranite prilagoditve in jih nato objavite.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
