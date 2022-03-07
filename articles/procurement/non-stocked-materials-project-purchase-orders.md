---
title: Naročanje materialov, ki niso na zalogi, za projekt, ki uporablja naročilnice za projekte
description: Ta tema pojasnjuje, kako lahko naročite materiale, ki niso na zalogi, za projekt, ki uporablja naročilnice za projekte.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: MT
ms.contentlocale: sl-SI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563042"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Naročanje materialov, ki niso na zalogi, za projekt, ki uporablja naročilnice za projekte

_**Velja za:** scenarije v storitvi Project Operations , ki temeljijo na virih/nezalogi_

Nabavni oddelek v vaši organizaciji bi lahko uporabil [naročilnice](/dynamics365/supply-chain/procurement/purchase-order-overview) za sledenje naročil blaga in storitev. Naročilnice za materiale, ki niso na zalogi, so lahko dodeljene projektu. Zaračunavanje teh naročilnic beleži stroške projekta.

## <a name="prerequisites"></a>Zahteve
Upoštevajte naslednje korake, da omogočite funkcijo naročilnic projektov.

1. V storitvi Dynamics 365 Finance izberite delovni prostor **Upravljanje funkcij**.
2. Na seznamu funkcij poiščite in izberite funkcijo **Omogoči naročilnice projektov v aplikaciji Project Operations za scenarije, ki temeljijo na virih/nezalogi**.
3. Izberite **Omogoči**.
4. Konfigurirajte materiale, ki niso na zalogi, in račune dobaviteljev v čakanju, kot je opisano v razdelku [Konfiguracija materialov, ki niso na zalogi, in računov dobaviteljev v čakanju](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Ustvarite naročilnico projekta s seznama naročilnic projektov

1. V razdelku za finance odprite možnost **Upravljanje projektov in vodenje računov** > **Projekti** > **Vsi projekti** in izberite projekt.
2. V podoknu za dejanja v zavihku **Upravljanje** v skupini **Novo** izberite **Opravilo elementa** > **Naročilnica**.
3. Na strani **Ustvarite naročilnico** izberite dobavitelja, pri katerem želite oddati naročilo, vnesite ustrezne druge podatke in nato izberite možnost **V redu**.
4. Na strani **Naročilnica** v mreži **Vrstice naročilnic** izberite **Dodaj vrstico**.
5. Vnesite številko izdelka, količino, enoto, ceno enote in druge ustrezne podatke.

    > [!NOTE]
    > Z naročilnicami projektov je mogoče uporabljati samo izdelke in storitve, ki niso na zalogi. Založeni izdelki in kategorije nabave niso podprti.

6. Po potrebi dodajajte izdelke in potrdite naročilnico.

    Potrdilo o blagu in storitvah lahko zabeležite tako, da ustvarite in objavite potrdilo o izdelku.

    > [!NOTE]
    > Potrdila o izdelkih se ne beležijo v dejanskih vrednosti projekta v storitvi Microsoft Dataverse in ne vplivajo na analitično evidenco projekta.

    Potem ko dobavitelj pošlje račun za izdelke in storitve na naročilnici, lahko dobavni oddelek ustvari račun za naročilnico tako, da v podoknu za dejanja odpre možnost **Račun** > **Ustvari** > **Račun**. Za več informacij o čakajočih računih dobaviteljev glejte razdelek [Nakup materialov, ki niso na zalogi, z uporabo čakajočega računa dobavitelja](pending-vendor-invoices.md).
