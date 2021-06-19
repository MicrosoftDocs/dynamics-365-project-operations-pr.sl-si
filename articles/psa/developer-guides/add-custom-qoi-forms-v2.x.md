---
title: Dodajanje novih obrazcev entitet po meri (Project Service Automation 2.x)
description: V tej temi so navedene informacije o dodajanju obrazcev entitet po meri za priložnosti, ponudbe, naročila ali račune v aplikaciji Dynamics 365 Project Service Automation 2. x.
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
ms.openlocfilehash: 400d817ee7cbae6f6da95db4286ad6c4d6ff349a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008016"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="d8c44-103">Dodajanje novih obrazcev entitet po meri (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="d8c44-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="d8c44-104">Polje »Vrsta«</span><span class="sxs-lookup"><span data-stu-id="d8c44-104">Type field</span></span> 

<span data-ttu-id="d8c44-105">Dynamics 365 Project Service Automation uporablja polje **Vrsta** (**msdyn\_ordertype**) za entitete priložnosti, ponudbe, naročila in računa za ločevanje različic teh entitet, ki **temeljijo na delu**, od različic, ki **temeljijo na elementu** in **temeljijo na storitvi**.</span><span class="sxs-lookup"><span data-stu-id="d8c44-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="d8c44-106">Različice teh entitet, ki temeljijo na delu, obravnava PSA.</span><span class="sxs-lookup"><span data-stu-id="d8c44-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="d8c44-107">Precej poslovne logike na strani odjemalca in strežnika rešitve je odvisne od polja **Vrsta**.</span><span class="sxs-lookup"><span data-stu-id="d8c44-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="d8c44-108">Zato je pomembno, da je polje v začetku izpolnjeno s pravilno vrednostjo, ko so entitete ustvarjene.</span><span class="sxs-lookup"><span data-stu-id="d8c44-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="d8c44-109">Nepravilna vrednost lahko povzroči nepravilne postopke, del poslovne logike pa morda ne bo pravilno izveden.</span><span class="sxs-lookup"><span data-stu-id="d8c44-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="d8c44-110">Samodejni preklop obrazcev</span><span class="sxs-lookup"><span data-stu-id="d8c44-110">Automatic form switching</span></span>

<span data-ttu-id="d8c44-111">Da se prepreči poškodovanje podatkov in nepričakovano delovanje, ki ga povzroči nepravilno prvotno izpolnjevanje in urejanje zapisov prodajnih entitet, PSA za vnaprej pripravljene obrazce zdaj vključuje logiko samodejnega preklopa obrazcev.</span><span class="sxs-lookup"><span data-stu-id="d8c44-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="d8c44-112">Ta logika uporabnike usmeri na pravilen obrazec za delo z različico, ki temelji na delu, ali katero koli drugo vrsto entitete priložnosti, ponudbe, naročila ali računa.</span><span class="sxs-lookup"><span data-stu-id="d8c44-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="d8c44-113">Ko uporabnik odpre različico entitete priložnosti, ponudbe, naročila ali računa, ki temelji na delu, se preklopi na obrazec **Podatki o projektu**.</span><span class="sxs-lookup"><span data-stu-id="d8c44-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="d8c44-114">Logika samodejnega preklapljanja med obrazci uporablja preslikavo med vrednostjo **formId** in poljem **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="d8c44-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="d8c44-115">V to preslikavo so bili dodani vsi vnaprej pripravljeni obrazci.</span><span class="sxs-lookup"><span data-stu-id="d8c44-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="d8c44-116">Obrazce po meri pa je treba ročno dodati, pri čemer je treba navesti, katero različico entitete naj obravnavajo.</span><span class="sxs-lookup"><span data-stu-id="d8c44-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="d8c44-117">To temelji na polju **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="d8c44-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="d8c44-118">Če med preslikavo manjka obrazec, s katerega se preklaplja, bo logika preklopila na vnaprej pripravljen obrazec na podlagi vrednosti, ki je shranjena v polju **msdyn\_ordertype** entitete.</span><span class="sxs-lookup"><span data-stu-id="d8c44-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="d8c44-119">Dodajanje obrazcev po meri in vklop logike za preklapljanja obrazcev</span><span class="sxs-lookup"><span data-stu-id="d8c44-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="d8c44-120">Ta primer prikazuje, kako dodate obrazec po meri, imenovan **Moji podatki o projektu**, da bo deloval s priložnostmi, ki temeljijo na delu.</span><span class="sxs-lookup"><span data-stu-id="d8c44-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="d8c44-121">Isti postopek se uporablja za dodajanje obrazcev po meri, da delujejo s ponudbami, naročili in računi.</span><span class="sxs-lookup"><span data-stu-id="d8c44-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="d8c44-122">Upoštevajte ta navodila in ustvarite različico obrazca **Podatki o projektu** po meri.</span><span class="sxs-lookup"><span data-stu-id="d8c44-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="d8c44-123">V entiteti »Priložnost« odprite obrazec za **Podatki o projektu** in shranite kopijo z imenom **Moji podatki o projektu**.</span><span class="sxs-lookup"><span data-stu-id="d8c44-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="d8c44-124">Odprite nov obrazec in nato v lastnostih preverite, ali so prisotni skripti za inicializacijo obrazca iz obrazca **Podatki o projektu**.</span><span class="sxs-lookup"><span data-stu-id="d8c44-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="d8c44-125">Skriptov ne odstranjujte.</span><span class="sxs-lookup"><span data-stu-id="d8c44-125">Don't remove the scripts.</span></span> <span data-ttu-id="d8c44-126">Če to storite, bodo nekateri podatki morda nepravilno inicializirani.</span><span class="sxs-lookup"><span data-stu-id="d8c44-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="d8c44-127">Preverite, ali je polje **Vrsta** (**msdyn\_ordertype**) prisotno na obrazcu.</span><span class="sxs-lookup"><span data-stu-id="d8c44-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="d8c44-128">Tega polja ne odstranjujte.</span><span class="sxs-lookup"><span data-stu-id="d8c44-128">Don't remove this field.</span></span> <span data-ttu-id="d8c44-129">Če to storite, skripti za inicializacijo ne bodo uspešni.</span><span class="sxs-lookup"><span data-stu-id="d8c44-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="d8c44-130">Poiščite vrednost **formId** novega obrazca.</span><span class="sxs-lookup"><span data-stu-id="d8c44-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="d8c44-131">Ta korak lahko izvedete na dva načina:</span><span class="sxs-lookup"><span data-stu-id="d8c44-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="d8c44-132">Izvozite obrazec **Moji podatki o projektu** kot del neupravljane rešitve in nato poiščite vrednost **formid** v datoteki customization.xml izvožene rešitve.</span><span class="sxs-lookup"><span data-stu-id="d8c44-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="d8c44-133">Odprite obrazec **Moji podatki o projektu** v urejevalniku obrazcev in poiščite globalni enolični identifikator (GUID) pri parametri **fromid** v URL-ju, kot je prikazano na spodnji sliki.</span><span class="sxs-lookup"><span data-stu-id="d8c44-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Vrednost formId novega obrazca v URL-ju](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="d8c44-135">Ustvarite preslikavo vrste **msdyn\_ordertype** za vrednost **formId** tako, da uredite spletni vir msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="d8c44-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="d8c44-136">Odstranite kodo iz vira in jo zamenjajte z naslednjo kodo.</span><span class="sxs-lookup"><span data-stu-id="d8c44-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="d8c44-137">Shranite prilagoditve in jih nato objavite.</span><span class="sxs-lookup"><span data-stu-id="d8c44-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]