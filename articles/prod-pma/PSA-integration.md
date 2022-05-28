---
title: Pregled rešitve Project Service Automation
description: Ta tema vsebuje informacije o Dynamics 365 Project Service Automation na Dynamics 365 Finance integracijsko rešitev.
author: ruhercul
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b8588e664f140ca1b0dd740d27fe6a5137da595
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685582"
---
# <a name="project-service-automation-overview"></a>Pregled rešitve Project Service Automation

[!include[banner](../includes/banner.md)]


Integracijska rešitev Project Service Automation to Finance uporablja funkcijo integracije podatkov za sinhronizacijo podatkov med primerki Dynamics 365 Finance in Dynamics 365 Project Service Automation preko Common Data Service. Predloge za integracijo, ki so na voljo s funkcijo za integracijo podatkov, omogočajo pretok projektov, projektne pogodbe, podrobnosti projektnih pogodb, mejnike podrobnosti projektnih pogodb, opravila projekta, kategorije transakcije stroškov, ocene delovnih ur in ocene stroškov iz rešitve Project Service Automation v Finance.

> [!NOTE]
> - Če uporabljate različico 7.3.0, morate namestiti KB 4074835. Potem boste lahko vključili projekte s fiksno ceno.
> - Če uporabljate različico 7.3.0 in transakcije s pristojbinami pridobivate iz rešitve Project Service Automation, morate namestiti KB 4345320, da te pristojbine vključite v račun projekta.
> - Če uporabljate različico 8.0, vam je na voljo integracija projektnih opravil, kategorije transakcije stroškov, ocene delovnih ur, ocene stroškov in zaklepanje funkcionalnosti.
> - Če uporabljate različico 8.0.1 ali novejšo, lahko sinhronizirate dejanske podatke.

Preden lahko integrirate rešitev Project Service Automation Finance, morate konfigurirati parametre integracije rešitve Project Service Automation. Za več informacij glejte [Parametri integracije rešitve Project Service Automation](PSA-parameters.md).

Ta rešitev za integracijo omogoča neposredno sinhronizacijo v naslednjih scenarijih:

- Vzdrževanje projektnih pogodb v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.
- Ustvarjanje projektov v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.
- Vzdrževanje podrobnosti projektne pogodbe v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.
- Vzdrževanje mejnike podrobnosti projektne pogodbe v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.
- Vzdrževanje opravil projekta v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.
- Vzdrževanje kategorij transakcije stroškov v rešitvi Finance in njihova sinhronizacija neposredno iz rešitve Finance v Project Service Automation.
- Ustvarjanje ocen delovnih ur projekta v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.
- Ustvarjanje ocen stroškov projekta v rešitvi Project Service Automation in njihova sinhronizacija neposredno iz rešitve Project Service Automation v Finance.
- Ustvarjanje dejanskih podatkov o času, stroških in pristojbinah v rešitvi Project Service Automation in ustvarjanje transakcije projektov v dnevnikih za integracijo rešitve Project Service Automation, tako da jih je mogoče objaviti v rešitvi Finance.

## <a name="data-synchronization"></a>Sinhronizacija podatkov

Naslednja ilustracija prikazuje, kako se podatki sinhronizirajo kot del integracije rešitve Project Service Automation v Finance.

> [!NOTE]
> Na voljo so le nekatere predloge. Predloge bodo objavljene, ko bodo dokončane.

[![Integracija rešitve Project Service Automation s rešitvijo Finance.](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Sistemske zahteve za Finance

Če želite uporabiti rešitev za integracijo rešitve Project Service Automation v Finance, morate namestiti različico Enterprise Edition 7.3 s posodobitvijo platforme na 12 ali novejšo.

## <a name="system-requirements-for-project-service-automation"></a>Sistemske zahteve za Project Service Automation

Če želite uporabiti rešitev za integracijo rešitve Project Service Automation v Finance, morate namestiti naslednje komponente:

- Dynamics 365 Project Service Automation, različica 9.0.0.0 ali novejša
- Rešitev za pretvorbo možne stranke v stranko za Dynamics 365 Sales, različica 1.14.0.0 (v14) ali novejša
- Rešitev Project Service Automation v Finance za Dynamics 365 Project Service Automation različice 1.0.0.0 ali novejša

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Namestite rešitev za integracijo rešitve Project Service Automation v Finance v svoj primerek rešitve Project Service Automation

Prenesite rešitev za integracijo rešitve Project Service Automation v Finance iz [Microsoftovega centra za prenose](https://www.microsoft.com/download/details.aspx?id=57016) in upoštevajte navodila, ki so priložena rešitvi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]