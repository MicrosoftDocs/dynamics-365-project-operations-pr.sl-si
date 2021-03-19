---
title: Preglasitev prodajnih cenikov za projekte
description: Ta tema vsebuje informacije o ustvarjanju prodajnih cenikov po meri.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275558"
---
# <a name="override-project-sales-price-lists"></a>Preglasitev prodajnih cenikov za projekte

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/nezalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

## <a name="customer-specific-project-price-lists"></a>Ceniki za projekte za določeno stranko

Dogovore o cenah za posamezno stranko lahko nastavite kot cenike za projekt na zapisu kupca v aplikaciji Dynamics 365 Project Operations.

Če želite nastaviti cenik za projekt za posamezno stranko, se v območju **Prodaja** pomaknite do zapisa kupca.

1. Odprite stran s seznamom **Kupci**.
2. Poiščite in dvokliknite zapis stranke, da odprete stran s podrobnostmi **Kupec**.
3. Na zavihku **Ceniki za projekte** izberite možnost **+ Nov cenik za projekt**.
4. Na strani **Nov cenik za projekt** s spustnega menija izberite cenik. Samo ceniki, ki imajo kontekst nastavljen na **Prodaja** in ki imajo ujemajočo se valuto z valuto kupca.
5. Poimenujte povezavo in nato izberite **Shrani**. Ustvarjen je cenik za projekt za posamezno stranko. Ta cenik se uporablja za nastavljanje privzetih cen projekta za projektne ponudbe ali pogodbe, ustvarjene za to stranko, ko se datum izdelave ponudbe ali projektne pogodbe prekriva z datumom veljavnosti cenika.

## <a name="custom-pricing-on-project-quotes"></a>Cene po meri za projektne ponudbe

Na projektnih ponudbah lahko določite cene za projekte, ki se začnejo s privzetim standardnim cenikom, ki sledi privzetim nastavitvam stranke ali projektnih parametrov.

Če na določeni ponudbi potrebujete cene po meri za delo, povezano s projektom, jih lahko dobite v povezani entiteti s ceniki projekta.

Upoštevajte spodnje korake, če želite nastaviti cene za projekte za posamezne ponudbe.

1. V projektni ponudbi odprite zavihek **Ceniki projektov**.
2. V podmreži izberite **Ustvarjanje cen po meri**.

Vsi ceniki projekta, ki so priloženi ponudbi, se kopirajo v nove cenike. Imena novih cenikov odražajo ime ponudbe z žigom datuma in časa, ko so bili ceniki ustvarjeni.

Vsakega od teh cenikov lahko uporabite in posodobite cene dela (cena vloge) in cene stroškov (cena kategorije). Te cene bodo veljale samo za to ponudbo za projekt.

## <a name="price-lists-on-a-project-contract"></a>Ceniki v projektni pogodbi

Pri projektni pogodbi so cene vedno privzete kot cenik po meri z imenom pogodbe in ustvarjenim žigom datuma in časa, ki je priložen imenu. To velja, ne glede na to, ali je bila pogodba ustvarjena, ko je bila ponudba pridobljena, ali če je bila pogodba ustvarjena povsem od začetka. Po potrebi lahko to povezavo s cenikom po meri odstranite in namesto tega s projektno pogodbo povežete standardni cenik.

Ko standardni cenik povežete s ceniki za projekte na ponudbi ali pogodbi, bodo vse spremembe cen v ceniku vplivale na vse ponudbe in pogodbe, ki uporabljajo cenik.


[!INCLUDE[footer-include](../includes/footer-banner.md)]