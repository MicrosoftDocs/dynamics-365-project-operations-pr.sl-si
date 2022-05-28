---
title: Spremembe entitete, kontrolnika in uporabniškega vmesnika (Project Service Automation 3.x)
description: V tej temi so opisane spremembe rešitve za Microsoft Dynamics Project Service Automation 3.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
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
ms.openlocfilehash: da43e0d15e655977c0c1be7348192a0189a56a6c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597588"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Spremembe entitete, kontrolnika in uporabniškega vmesnika (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Z izdajo rešitve Microsoft Dynamics Project Service Automation (PSA) 3.x je v entitetah, kontrolnikih, pogledih in uporabniškem vmesniku prišlo do številnih sprememb. V tej temi najdete informacije o teh pomembnih spremembah.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Odnosi nadrejeni-podrejeni za entitete prodajnega dokumenta, vrstice prodajnega dokumenta in podrobnosti vrstice prodajnega dokumenta
V različicah rešitve Dynamics 365 Project Service Automation (PSA), ki so bile izdane pred različico 3.0, so bili nekateri odnosi med entitetami prodajnih dokumentov, vrstic prodajnega dokumenta in podrobnosti vrstice prodajnega dokumenta uporabljeni prek polj z nizi s ponazoritvijo GUID-a povezane entitete. To je bila posledica omejitev platforme, ki so zahtevale pomembno kodo po meri v strežniku in v odjemalcu rešitve, da so ti odnosi delovali podobno kot tipični odnosi entitete programa Dynamics CRM in da so polja z nizi delovala kot polja za iskanje.

Rešitev PSA 3.0 je bila posodobljena za uporabi novih odnosov entitete med entitetami prodajnih dokumentov in vrstic prodajnega dokumenta.

Ker se polja za iskanje zdaj lahko uporabijo za označevanje sklicev na entitete, polja, ki so imela v prejšnjih različicah vrednost GUID-a povezane entitete, niso več potrebna in so bila zato opuščena. Koda po meri v odjemalcu in strežniku, ki ureja odnose, ki jih določajo podedovana polja z nizi, je bila prav tako opuščena.

### <a name="entity-schema-changes"></a>Spremembe sheme entitete
Spodnja tabela vsebuje seznam opuščenih polj z nizi in nova polja za iskanje za entitete. 

 Entiteta |   Opuščeno polje (niz) | Novo polje (iskanje)
--- | --- | ---
invoicedetail (vrstica računa) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (dejanska vrednost) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (razpored izdajanja računov v vrstici projektne pogodbe) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (mejnik v vrstici projektne pogodbe) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (dejstvo) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (podrobnosti vrstice računa) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (vrstica dnevnika) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (kategorija vira v vrstici projektne pogodbe) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (podrobnost vrstice projektne pogodbe) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (kategorija transakcije v vrstici projektne pogodbe) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (klasifikacija transakcije v vrstici projektne pogodbe) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (razpored izdajanja računov v vrstici ponudbe) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (kategorija vira v vrstici ponudbe) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (mejnik v vrstici ponudbe) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (podrobnost vrstice ponudbe) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (kategorija transakcij v vrstici ponudbe) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (klasifikacija transakcij v vrstici ponudbe) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (vrstica naročila) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Opuščeni pogledi in kontrolniki po meri
Spodnji pogledi in kontrolniki po meri ter njihovi povezani artefakti so bili opuščeni.

- Pogled možnosti zaračunavanja.
- Kontrolniki mreže po meri za prikaz podrobnosti vrstice ponudbe na strani **Podatki o projektu** za vrstico ponudbe.
- Kontrolniki mreže po meri za prikaz podrobnosti vrstice projektne pogodbe na strani **Podatki o projektu** za vrstico prodajnega naloga.

> [!NOTE]
> Za celoten seznam opuščenih virov glejte [Zastareli spletni viri v rešitvi Project Service Automation 3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Modul aplikacije poenotenega odjemalskega vmesnika
Z uvedbo modulov aplikacije poenotenega odjemalskega vmesnika so bili vnosi zemljevida mesta v PSA odstranjeni iz sistema.  
Funkcija, povezana s preklapljanjem obrazcev za priložnost, ponudbo, naročilo in račun, je bila opuščena, saj ni več potrebna, ker so v modulu aplikacije poenotenega odjemalskega vmesnika samo različice PSA za obrazce.  

Spodnji spletni viri so bili opuščeni:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Za celoten seznam opuščenih virov glejte [Zastareli spletni viri v rešitvi Project Service Automation 3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
