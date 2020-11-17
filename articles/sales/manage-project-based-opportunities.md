---
title: Upravljanje priložnosti, ki temeljijo na projektu
description: Ta tema vsebuje informacije o tem, kako delati s priložnostmi, povezanimi s projekti.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 39ce52d5da4c7027ee2f2fa44579c0d4bf74925e
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: sl-SI
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088109"
---
# <a name="manage-project-based-opportunities"></a>Upravljanje priložnosti, ki temeljijo na projektu

_**Velja za:** Project Operations za scenarije, ki temeljijo na virih/manjkajoči zalogi, poenostavljeno uvedbo – posel do izstavitve predračuna_

Običajno imajo podjetja, ki temeljijo na projektih, postopke za dostavo razvejane po več državah in regijah. Stroški izvajanja in dostave projekta se lahko razlikujejo glede na to, katera regija ali oddelek upravlja dostavo. To pa lahko vpliva na marže posla. Izvajanje projektnih storitev običajno vključuje velike količine porabljenega časa kadra, znatne potne stroške, materialne stroške in druge stroške.

Priložnosti, ki temeljijo na projektu, so v storitvi Dynamics 365 Project Operations zasnovane z razširitvami za Dynamics 365 Sales. Ta tema vsebuje podrobnosti o različnih poljih in poslovni logiki, vključeni v dodatno funkcionalnost, ki jo potrebujejo podjetja, ki temeljijo na projektih, za upravljanje projektnih priložnosti.

## <a name="view-all-project-based-opportunities"></a>Ogled vseh priložnosti, ki temeljijo na projektu

Seznam vseh priložnosti, ki temeljijo na projektu, si lahko ogledate na strani s seznamom **Priložnost**. 

1. Odprite možnost **Prodaja** > **Priložnosti**.
2. Uporabite **Preklopnik pogleda** , da izberete druge filtrirane poglede priložnosti. Za konfiguracijo teh pogledov in možnosti navigacije lahko ustvarite svoje poglede s prilagojenimi merili filtra.

Projektne priložnosti lahko ustvarite ali izbrišete s te strani s seznamom ali strani s podrobnostmi.

## <a name="business-process-flow-for-project-based-deals"></a>Potek poslovnega procesa za posle, ki temeljijo na projektu

Za posle, ki temeljijo na projektu, v storitvi Project Operations so podprti naslednji poteki poslovnih procesov:

- Poslovni proces od možne stranke do priložnosti
- Prodajni proces priložnosti

### <a name="lead-to-opportunity-business-process"></a>Poslovni proces od možne stranke do priložnosti 
Poslovni proces od možne stranke do priložnosti podpira naslednje stopnje:

| Faza | Preslikana entiteta | Funkcionalnost |
| --- | --- | --- |
| Kvalificiraj | Možna stranka | Potrdite možno stranko za ustvarjanje kupca, stika in priložnosti. |
| Razvoj | Priložnost | Razvijte priložnost za dodajanje več informacij o vključenem delu, ključnih zainteresiranih skupinah in konkurenci. |
| Predlaganje | Priložnost | Razvijte predlog in pridobite odobritev od skupine za notranji pregled. |
| Zaprto | Priložnost | Pridobite priložnost za sklenitev posla. |

### <a name="opportunity-sales-process"></a>Prodajni proces priložnosti
Prodajni postopek za priložnost v aplikaciji Project Operations je razširitev poteka poslovnega procesa prodaje za priložnost v aplikaciji Sales. Ta poslovni proces ima vnaprej pripravljeno zasnovo, ki podpira naslednje faze v priložnosti, ki temelji na projektu.

| Faza | Preslikana entiteta | Funkcionalnost |
| --- | --- | --- |
| Kvalificiraj | Priložnost | Potrdite možno stranko za ustvarjanje kupca, stika in priložnosti. |
| Predlaganje | Citat | Razvijte predlog s projektnimi ponudbami in pridobite odobritev od skupine za notranji pregled. |
| Pogodba | Projektna pogodba | Pridobite ponudbo, da ustvarite pogodbo in začnete izvajati projekt, ki ga na koncu dostavite. |
| Zaprto | Projektna pogodba | Z delom uspešno zaključite in zaprite projektno pogodbo. |

> [!NOTE]
> Če se je vaš projektni posel začel z možno stranko, ima poslovni proces možne stranke prednost pred priložnostjo.
>
> Če se je vaš projektni posel začel s priložnostjo, ima prednost poslovni proces prodaje za priložnost.

Potek poslovnega procesa za izdelek lahko uredite ali ustvarite lastne poteke poslovnega procesa, da po potrebi spremljate svoj prodajni proces. Za več informacij o poteku poslovnega procesa glejte [Pregled potekov poslovnega procesa](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).